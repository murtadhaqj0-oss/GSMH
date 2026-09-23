
*   Role: DERIVATION agent for GSMH.
    *   Objective: Develop the most rigorous, mathematically consistent model for GSMH from first principles.
    *   Constraint: Do not assume GSMH is correct. Work from first principles.
    *   Required Deliverables:
        1.  Fields and parameters.
        2.  Action/Equations.
        3.  Field equations derivation.
        4.  Covariance/Conservation checks.
        5.  Perturbation equations.
        6.  Stability checks (ghosts, tachyons, gradients).
        7.  Causality/Hyperbolicity.
        8.  Weak-field/Newtonian limit.
        9.  Observable prediction.
        10. Identification of unproved items.
    *   Context: The "Canonical Model" and "Open Problems" are currently empty/unpopulated. This means I am essentially defining the "GSMH" theory for the first time based on the acronym and the implied goal (likely "General Scalar-Metric-Holographic" or similar, though the user hasn't explicitly defined the acronym, I must derive a model that fits the likely intent of a modified gravity theory involving scalars, metrics, and potentially holographic principles).

    *   *Wait, what is "GSMH"?* The prompt doesn't define it. However, looking at the requirements (Action, covariance, GR limit, binary pulsars, etc.), it is clearly a theory of gravitation/cosmology.
    *   If GSMH is not defined, I must *propose* a mathematically rigorous model that satisfies these requirements.
    *   Common components in "Modified Gravity" (MG) that align with the acronym GSMH could be:
        *   **G**: General/Gravitational (Metric $g_{\mu\nu}$).
        *   **S**: Scalar (Scalar field $\phi$).
        *   **M**: Metric/Matter (Energy-momentum tensor $T_{\mu\nu}$).
        *   **H**: Holographic/Higher-derivative/Horndeski (Higher-order terms or holographic boundary constraints).
    *   *Self-Correction:* To be most rigorous and avoid arbitrary "guessing," I will construct a **General Scalar-Metric-Holographic (GSMH)** model based on the **Horndeski-class** (the most general second-order scalar-tensor theory) but augmented with a **Holographic Constraint** (e.g., a boundary term or a specific scaling law derived from the holographic principle) to justify the "H".

    *   *Fields:* Metric $g_{\mu\nu}$, Scalar field $\phi$.
    *   *Action:* Start with the Einstein-Hilbert action + Horndeski terms + a Holographic Entropy bound term.
    *   *Holographic aspect:* To make it "Holographic," I can introduce a term where the effective cosmological constant or the scalar potential is coupled to the boundary area of the observable horizon (a common approach in holographic dark energy). Alternatively, a more fundamental approach is a boundary action.
    *   *Decision:* Let's build a model that uses a scalar field coupled to the Gauss-Bonnet invariant (which is a topological invariant in 4D but becomes dynamical if coupled to a scalar), as this is a common "advanced" gravity model that allows for rigorous testing and is often associated with string-theoretic (holographic) corrections.

    *   *Action:* $S = \int d^4x \sqrt{-g} \left[ \frac{M_{pl}^2}{2} R - \frac{1}{2}(\partial \phi)^2 - V(\phi) + \alpha(\phi) \mathcal{G} \right] + S_m$.
        *   $\mathcal{G} = R^2 - 4R_{\mu\nu}R^{\mu\nu} + R_{\mu\nu\rho\sigma}R^{\mu\nu\rho\sigma}$ (Gauss-Bonnet).
    *   *Refinement for "Holographic" (H):* Incorporate a constraint that the vacuum energy density $\rho_\Lambda$ is proportional to $L^{-2}$ where $L$ is the IR cutoff (Hubble scale), making it a Holographic Dark Energy model.

    *Step 1: Fields/Params*
    *   $g_{\mu\nu}$: Spacetime metric.
    *   $\phi$: Scalar field.
    *   $\alpha(\phi)$: Coupling function (the "Holographic" weight).
    *   $V(\phi)$: Potential.

    *Step 2: Action*
    *   $S = \int d^4x \sqrt{-g} \left[ \frac{M_{pl}^2}{2} R - \frac{1}{2} \nabla^\mu \phi \nabla_\mu \phi - V(\phi) + \alpha(\phi) (R^2 - 4R_{\mu\nu}R^{\mu\nu} + R_{\mu\nu\rho\sigma}R^{\mu\nu\rho\sigma}) \right] + S_{matter}$.

    *Step 3: Field Equations*
    *   Vary w.r.t. $g_{\mu\nu}$ $\rightarrow$ modified Einstein equations.
    *   Vary w.r.t. $\phi$ $\rightarrow$ modified Klein-Gordon equation.

    *Step 4: Covariance/Conservation*
    *   Diff-invariance is guaranteed by the action's form.
    *   Bianchi identity implies $\nabla^\mu T_{\mu\nu} = 0$.

    *Step 5: Perturbations*
    *   $g_{\mu\nu} = \bar{g}_{\mu\nu} + h_{\mu\nu}$, $\phi = \bar{\phi} + \delta \phi$.
    *   Linearize.

    *Step 6: Ghosts/Tachyons*
    *   Check Ostrogradsky instability. (Gauss-Bonnet + Scalar is known to be second-order, so no Ostrogradsky ghosts).
    *   Tachyons: $m_\phi^2 = V''(\phi) > 0$.
    *   Gradients: Kinetic term must be positive.

    *Step 7: Causality*
    *   Characteristic surfaces. Check if the speed of sound $c_s^2 \le 1$.

    *Step 8: Limits*
    *   Weak field: $\alpha \to 0$ or $\phi \to \phi_0$.
    *   Newtonian limit: Poisson equation $\nabla^2 \Phi = 4\pi G \rho$.

    *Step 9: Prediction*
    *   Modified GW propagation speed $c_T$ or modified lensing potential.

    *Step 10: Unproved*
    *   UV completion, quantum stability, etc.

    *   I need to ensure the "H" is not just a label but a mathematical feature. I will define $\alpha(\phi)$ such that it emerges from a holographic boundary renormalization, or more simply, treat the coupling to the Euler density as the "Holographic" correction (as these often arise from string theory/AdS-CFT).

    *   Use LaTeX for equations.
    *   Maintain the "Agent" persona: rigorous, skeptical, methodical.