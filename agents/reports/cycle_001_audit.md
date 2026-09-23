name: GSMH Autonomous Research

on:
  workflow_dispatch:

permissions:
  contents: write

jobs:
  research:
    runs-on: ubuntu-latest
    timeout-minutes: 360

    env:
      GEMINI_API_KEY: ${{ secrets.GEMINI_API_KEY }}

    steps:
      - name: Checkout GSMH
        uses: actions/checkout@v4

      - name: Setup Python
        uses: actions/setup-python@v5
        with:
          python-version: "3.12"

      - name: Install requests
        run: pip install requests

      - name: Run autonomous GSMH research
        run: |
          mkdir -p agents/reports

          python - <<'PY'
          import os
          import json
          import time
          import requests
          from pathlib import Path

          KEY = os.environ["GEMINI_API_KEY"]
          URL = "https://generativelanguage.googleapis.com/v1beta/models/gemma-4-31b-it:generateContent"

          def ask(prompt):
              for attempt in range(5):
                  try:
                      r = requests.post(
                          URL,
                          headers={
                              "x-goog-api-key": KEY,
                              "Content-Type": "application/json"
                          },
                          json={
                              "contents": [
                                  {"parts": [{"text": prompt}]}
                              ]
                          },
                          timeout=(30, 900)
                      )

                      if r.status_code == 200:
                          data = r.json()
                          return data["candidates"][0]["content"]["parts"][0]["text"]

                      if r.status_code in (429, 500, 502, 503, 504):
                          time.sleep(10 * (attempt + 1))
                          continue

                      raise RuntimeError(r.text)

                  except Exception:
                      if attempt == 4:
                          raise
                      time.sleep(10 * (attempt + 1))

          canonical = Path("memory/CANONICAL_MODEL.md").read_text()
          problems = Path("memory/OPEN_PROBLEMS.md").read_text()

          previous = "No previous research cycle exists."

          for cycle in range(1, 21):

              print(f"=== GSMH CYCLE {cycle} ===")

              derivation = ask(f"""
          You are the DERIVATION AGENT for GSMH.

          GSMH means exactly:

          Gravity Spacetime Memory Hypothesis.

          GSMH proposes that gravitational response may depend on
          present matter-energy AND a mathematically defined history
          of spacetime curvature or matter distribution.

          Do NOT reinterpret GSMH as:
          - holographic gravity
          - scalar-Gauss-Bonnet gravity
          - generic scalar-tensor gravity
          - dark matter
          - an unrelated modified-gravity theory

          If a proposed model cannot represent genuine hereditary
          gravitational memory, reject it.

          Work from first principles.

          Required:

          1. Define the physical fields and parameters.
          2. Construct an action or mathematically equivalent equations.
          3. Derive the equations of motion explicitly.
          4. Establish diffeomorphism covariance.
          5. Establish conservation constraints.
          6. Determine propagating degrees of freedom.
          7. Test ghosts.
          8. Test tachyonic instabilities.
          9. Test gradient instabilities.
          10. Test hyperbolicity and causality.
          11. Distinguish genuine hereditary memory from ordinary
              retarded propagation and curved-spacetime tail effects.
          12. Derive the weak-field/Newtonian limit.
          13. Determine whether the model can modify galactic
              gravitational dynamics without invisible matter.
          14. Derive at least one falsifiable observable.
          15. State every assumption.
          16. Explicitly identify anything not mathematically proven.

          NEVER claim PROVEN merely because the equations look plausible.

          PREVIOUS CYCLE:
          {previous}

          CANONICAL MODEL:
          {canonical}

          OPEN PROBLEMS:
          {problems}
          """)

              audit = ask(f"""
          You are the INDEPENDENT AUDITOR for GSMH.

          Audit the following derivation aggressively.

          GSMH is specifically a history-dependent gravitational
          response hypothesis.

          Do not replace it with another theory.

          Check:

          - mathematical consistency
          - covariance
          - conservation
          - constraints
          - degrees of freedom
          - ghosts
          - tachyons
          - gradient instabilities
          - hyperbolicity
          - causality
          - initial-value formulation
          - GR recovery
          - Newtonian limit
          - Solar-System constraints
          - binary-pulsar constraints
          - gravitational-wave constraints
          - galaxy-scale predictions
          - lensing
          - cluster observations
          - persistence timescale
          - whether the claimed memory is genuinely hereditary
          - whether it is merely a normal retarded/tail effect

          If the derivation fails, identify the exact equation
          or assumption responsible.

          DERIVATION:
          {derivation}
          """)

              synthesis = ask(f"""
          You are the SENIOR GSMH RESEARCHER.

          Combine the derivation and audit.

          Preserve GSMH identity.

          Repair the model only when the repair is mathematically
          justified. Otherwise reject the invalid step.

          Return exactly these sections:

          CANONICAL EQUATIONS
          ACTION
          ASSUMPTIONS
          DERIVATION STATUS
          CONSERVATION STATUS
          STABILITY STATUS
          CAUSALITY STATUS
          NEWTONIAN LIMIT
          OBSERVATIONAL PREDICTION
          STRONGEST FAILURE
          NEXT MATHEMATICAL PROBLEM
          FINAL STATUS

          The FINAL STATUS line MUST contain exactly one of:

          PROVEN
          DERIVED-BUT-UNVERIFIED
          VIABLE-CANDIDATE
          FAILED
          OPEN

          Important:
          PROVEN is allowed ONLY if the mathematical derivation
          actually establishes the claimed GSMH mechanism without
          unresolved contradictions.

          DERIVATION:
          {derivation}

          AUDIT:
          {audit}
          """)

              Path(
                  f"agents/reports/cycle_{cycle:03d}_derivation.md"
              ).write_text(derivation)

              Path(
                  f"agents/reports/cycle_{cycle:03d}_audit.md"
              ).write_text(audit)

              Path(
                  f"agents/reports/cycle_{cycle:03d}_synthesis.md"
              ).write_text(synthesis)

              status_line = ""

              for line in synthesis.splitlines():
                  if line.strip().startswith("FINAL STATUS"):
                      status_line = line.strip()

              state = {
                  "cycle": cycle,
                  "final_status": status_line,
                  "previous_cycle_used": cycle > 1
              }

              Path("agents/state.json").write_text(
                  json.dumps(state, indent=2)
              )

              previous = synthesis

              print(f"Cycle {cycle} completed.")
              print(f"Status: {status_line}")

              if status_line == "FINAL STATUS: PROVEN":
                  print("GSMH reached PROVEN status.")
                  break

          PY

      - name: Save research
        run: |
          git config user.name "GSMH Research Agent"
          git config user.email "41898282+github-actions[bot]@users.noreply.github.com"
          git add agents/reports agents/state.json
          git diff --cached --quiet || git commit -m "GSMH autonomous research cycles"
          git push
