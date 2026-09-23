DERIVATION agent for GSMH (Generalized Scalar-Metric-Holographic / Geometric Scalar-Metric-Hybrid - the user hasn't defined the acronym, but the context implies a gravity-like theory modification).
Work from first principles. Do not assume correctness. Be mathematically rigorous.

        1.  Define fields/parameters.
        2.  Construct Action/Equations.
        3.  Derive field equations.
        4.  Covariance/Conservation check.
        5.  Perturbation equations.
        6.  Ghosts/Tachyons/Gradient instabilities.
        7.  Causality/Hyperbolicity.
        8.  Weak-field/Newtonian limit.
        9.  Observable prediction.
        10. Identify what remains unproved.
The "Canonical Model" and "Open Problems" files are currently empty/unpopulated. This means I am essentially *creating* the first rigorous proposal for what GSMH could be, based on the name and the requirements.

    *   *GSMH* suggests a blend of:
        *   **G**ravity (Metric $g_{\mu\nu}$)
        *   **S**calar field ($\phi$)
        *   **M**etric-related (perhaps a second metric or a non-minimal coupling)
        *   **H**olographic (incorporating an entropy-based boundary term or a holographic scale $\ell$ / AdS-like influence).
    *   *Goal:* To avoid the common pitfalls of modified gravity (ghosts, tachyons) while providing a framework that could potentially address Dark Energy/Dark Matter or Quantum Gravity corrections.
    *   *Proposed Ansatz:* A Scalar-Tensor theory with a holographic constraint or a modified kinetic term that incorporates a holographic scale. Let's go with a **Non-minimally coupled Scalar-Metric theory with a Holographic boundary term or a specific potential derived from holographic principles.**

    *   *Refining the Ansatz for Rigor:* Let's define GSMH as a theory where gravity is mediated by a metric $g_{\mu\nu}$ and a scalar field $\phi$, with an action that includes a holographic-inspired term (e.g., a term that scales with the area of the boundary or a specific non-local kernel that mimics holographic behavior, though non-local theories are hard to prove causal).
    *   *Simpler, more rigorous approach:* A Horndeski-like action (the most general scalar-tensor theory with second-order equations) augmented by a holographic potential $V(\phi)$ and a specific coupling to the Gauss-Bonnet invariant (to maintain second-order equations while adding higher-curvature terms).

    *   *Fields:* $g_{\mu\nu}$ (metric), $\phi$ (scalar).
    *   *Parameters:* $\kappa^2 = 8\pi G$, $\alpha$ (coupling constant), $\Lambda$ (cosmological constant), $\ell$ (holographic length scale).

    *   *Action:* $S = \int d^4x \sqrt{-g} \left[ \frac{1}{2\kappa^2} R - \frac{1}{2} g^{\mu\nu} \partial_\mu \phi \partial_\nu \phi - V(\phi) + \alpha \phi \mathcal{G} \right] + S_{boundary} + S_{matter}$.
        *   $\mathcal{G} = R^2 - 4R_{\mu\nu}R^{\mu\nu} + R_{\mu\nu\rho\sigma}R^{\mu\nu\rho\sigma}$ (Gauss-Bonnet). This is the "H" part (Holographic/Higher-curvature) often used in AdS/CFT and string theory.

    *   *Field Equations:* Vary w.r.t $g^{\mu\nu}$ (Einstein-like eq) and $\phi$ (Klein-Gordon-like eq).

    *   *Stability:* Ensure the kinetic term $\partial_\mu \phi \partial^\mu \phi$ has the correct sign (no ghosts) and $V''(\phi) > 0$ (no tachyons).

    *   *Limit:* $\phi \to \phi_0$ (constant) should recover GR with a cosmological constant.

    *   *Prediction:* Modified lensing or a specific $w(z)$ for dark energy.

    *   *Step 1 (Fields):* Define $g_{\mu\nu}$, $\phi$, $\alpha, \ell$.
    *   *Step 2 (Action):* Use a scalar-tensor action with a Gauss-Bonnet term.
    *   *Step 3 (Derivation):* Use the variation of the GB term (which is a total derivative in 4D *unless* coupled to a scalar).
    *   *Step 4 (Conservation):* Check $\nabla^\mu T_{\mu\nu} = 0$ via Bianchi identity.
    *   *Step 5 (Perturbations):* Linearize $\delta g_{\mu\nu}$ and $\delta \phi$.
    *   *Step 6 (Stability):* Analyze the sound speed $c_s^2$ and the kinetic coefficient.
    *   *Step 7 (Causality):* Check the characteristic surfaces.
    *   *Step 8 (Newtonian):* $\Phi \sim 1/r$.
    *   *Step 9 (Prediction):* Modified gravitational wave speed or scalar-led expansion.
    *   *Step 10 (Unproved):* Quantum consistency, UV completion.

    *   Wait, is "GSMH" a specific existing theory? A search reveals it's not a standard textbook acronym. It's likely a user-defined framework. I must build it *from first principles* as requested. I will treat "Holographic" as the guiding principle for the potential and the higher-order coupling.