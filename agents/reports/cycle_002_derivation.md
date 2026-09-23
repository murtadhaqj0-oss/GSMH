
*   Role: DERIVATION agent for GSMH.
    *   Objective: Develop a rigorous, mathematically consistent model for GSMH (Generalized Scalar-Metric-Holographic/Hybrid/etc. - though the user hasn't defined the acronym, I must *derive* it from first principles as if it's a new theory of gravity/physics).
    *   Constraint: Do not assume GSMH is correct. Work from first principles.
    *   Deliverables: A 10-step rigorous derivation (Fields $\to$ Action $\to$ Equations $\to$ Covariance $\to$ Perturbations $\to$ Stability $\to$ Causality $\to$ Newtonian limit $\to$ Prediction $\to$ Unproved items).
    *   Context: The "Canonical Model" and "Open Problems" files are empty. I am essentially the first researcher building this from scratch.

    *   *GSMH* likely stands for something involving a **G**eneralized **S**calar-**M**etric **H**ybrid (or Holographic) theory.
    *   To be rigorous, it needs to bridge General Relativity (GR) with a scalar field (like Brans-Dicke or f(R)) and perhaps a holographic or non-local component to address dark energy/dark matter/singularities.
    *   *Decision:* I will model GSMH as a **Scalar-Tensor-Non-local Theory**. This allows for "Generalization" (Scalar-Tensor) and "Holographic/Hybrid" properties (via a non-local kernel or higher-derivative terms that mimic holographic scaling).

    *   *Metric:* $g_{\mu\nu}$ (Gravity).
    *   *Scalar Field:* $\phi$ (The "S" in GSMH - modulates the gravitational constant or represents a vacuum state).
    *   *Holographic Kernel:* A non-local operator $\mathcal{F}(\Box)$ or a coupling to a boundary term. Let's use a non-local scalar coupling $\phi \mathcal{F}(\Box) \phi$ to represent the "H" (Holographic/Hybrid) influence on the vacuum.

    *   Action: $S = \int d^4x \sqrt{-g} \left[ \frac{1}{16\pi G} \phi R - \frac{\omega}{\phi} \partial_\mu \phi \partial^\mu \phi - V(\phi) + \mathcal{L}_{NL} + \mathcal{L}_{m} \right]$.
    *   Wait, let's make it "Generalized." Let the scalar coupling be $f(\phi) R$.
    *   To introduce the "Holographic" part rigorously: Let's add a term that relates the bulk curvature to a non-local integral of the scalar field, or a term proportional to the Ricci scalar and a function of the D'Alembertian: $R \mathcal{F}(\Box) R$. This is common in non-local gravity.
    *   *Revised Action:*
        $S = \int d^4x \sqrt{-g} \left[ \frac{\phi}{16\pi G} R - \frac{1}{2} g^{\mu\nu} \partial_\mu \phi \partial_\nu \phi - V(\phi) - \frac{1}{2} \phi R \frac{1}{\Box} R \right]$ (This is a toy non-local term).
        *Actually, let's keep it slightly more standard for the first derivation to ensure stability, then add the "Generalized" part.*

    *   *Refined Model Proposal:*
        $\mathcal{L} = \frac{1}{16\pi G} \left( \phi R - \frac{\omega}{\phi} (\nabla \phi)^2 \right) - \mathcal{V}(\phi) + \mathcal{L}_{matter}$
        And for the "Holographic" (H) part, let's incorporate a scale-dependent coupling $\lambda(\phi, \Box)$ that modifies the effective Planck mass based on the curvature scale.

    *   *Wait, if I am the Derivation Agent, I must define GSMH myself since the canonical file is empty.*
    *   **GSMH definition for this derivation:** **G**eneralized **S**calar-**M**etric **H**ybrid.
    *   **Core Postulate:** Gravity is mediated by a metric $g_{\mu\nu}$ and a scalar field $\phi$, where the scalar field's kinetic term is non-minimally coupled to the curvature and includes a non-local "holographic" correction to prevent singularities.

    *   *Step 1: Fields.* $g_{\mu\nu}, \phi$.
    *   *Step 2: Action.* $S = \int d^4x \sqrt{-g} \left[ \frac{1}{2\kappa} \phi R - \frac{\omega(\phi)}{\phi} \partial_\mu \phi \partial^\mu \phi - V(\phi) \right]$. (Standard scalar-tensor). To make it "Hybrid/Holographic," let's add a term $\alpha R \log(\Box/\mu^2) R$ or similar. No, let's use a simpler "Hybrid" approach: a coupling between $\phi$ and the Gauss-Bonnet invariant $\mathcal{G}$. This is common in modern string-inspired gravity.
    *   *Action Choice:*
        $S = \int d^4x \sqrt{-g} \left[ \frac{\phi R}{16\pi G} - \frac{\omega}{\phi} g^{\mu\nu} \partial_\mu \phi \partial_\nu \phi - V(\phi) + \xi \phi \mathcal{G} \right]$
        Where $\mathcal{G} = R^2 - 4 R_{\mu\nu} R^{\mu\nu} + R_{\mu\nu\rho\sigma} R^{\mu\nu\rho\sigma}$.

    *   *Step 3: Field Equations.* Vary $S$ w.r.t. $g^{\mu\nu}$ and $\phi$.
    *   *Step 4: Covariance.* Check diffeomorphism invariance.
    *   *Step 5: Perturbations.* $\delta g_{\mu\nu}, \delta \phi$.
    *   *Step 6: Ghosts/Tachyons.* Check the sign of the kinetic terms. $\phi$ must be positive, $\omega > -3/2$.
    *   *Step 7: Causality.* Check if signals propagate $\le c$.
    *   *Step 8: Newtonian limit.* $\phi \to \phi_0$, $g_{\mu\nu} \to \eta_{\mu\nu} + h_{\mu\nu}$.
    *   *Step 9: Prediction.* Modified PPN parameters ($\gamma \neq 1$).
    *   *Step 10: Unproved.* Dark energy explanation, Quantum gravity limit.

    *   Ensure indices are correct.
    *   Ensure the Gauss-Bonnet term's contribution to field equations is handled correctly (it's a total derivative in 4D unless coupled to a scalar).
    *   Be explicit about the "Holographic" aspect: Define the "H" as the coupling to the topological invariant which controls the entropy/boundary of the manifold.