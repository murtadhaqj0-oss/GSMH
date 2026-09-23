Synthesis Agent for the Gravity Spacetime Memory Hypothesis (GSMH) project.
Develop a mathematically consistent, covariant, testable alternative to dark matter.
Canonical model is empty; Open Problems are foundational.
Derivation Agent (proposing a model based on "Hereditary Tensors" or "Memory Fields") and Auditor Agent (establishing the "Audit Framework" and "Red Flags").
Construct the strongest defensible GSMH formulation. Preserve only what survives scrutiny. State what is proven, conditionally derived, and remaining as hypothesis.

    *   *Derivation Agent's Core Proposal:*
        *   *Concept:* "Memory" = non-local or delayed response of spacetime to matter.
        *   *Proposed mechanism:* An auxiliary "Memory Tensor" $\mathcal{M}_{\mu\nu}$ that tracks the integrated history of $T_{\mu\nu}$.
        *   *Key Equation:* $G_{\mu\nu} = 8\pi G (T_{\mu\nu} + \mathcal{M}_{\mu\nu})$, where $\mathcal{M}_{\mu\nu}$ satisfies a wave equation $\Box \mathcal{M}_{\mu\nu} + \dots = \dots T_{\mu\nu}$.
        *   *Goal:* Mimic Dark Matter (enhance gravity at large scales/low acceleration).

    *   *Auditor Agent's Core Warning:*
        *   *Concerns:* Covariance, Ghosts (Ostrogradsky), Causality (non-locality), Conservation Laws ($\nabla^\mu G_{\mu\nu} = 0$), and the GR limit (Solar System tests).
        *   *Framework:* Any model must pass a "Stress-Test" involving these five vectors.

    *   *Synthesis Task:* Combine the Derivation's creativity with the Auditor's rigor. I cannot just "accept" the Derivation Agent's report because it's a *proposal*, not a *proven theory*. I must refine the proposal into a formal "Version 0.1" (or a "First Proposal") that explicitly addresses the Auditor's concerns.

    *   *Refining the "Memory" Mechanism:*
        The Derivation Agent suggested $\mathcal{M}_{\mu\nu}$. To make this covariant and ghost-free, I should frame it as a *Proca-like* or *Klein-Gordon-like* auxiliary field. Instead of a full tensor (which adds too many degrees of freedom and potential instabilities), perhaps a scalar field $\Phi$ that modifies the effective coupling $G$ is safer, but the Derivation Agent wants "Memory."
        *Better Synthesis:* A tensor field $\mathcal{M}_{\mu\nu}$ is mathematically heavy. Let's synthesize it as a **Covariant Memory Field** $\Phi$ (scalar) that mediates a non-local correction to the Einstein equations.

    *   *Drafting the "Memory" Action:*
        To avoid ghosts, we use a standard kinetic term for the auxiliary field.
        Action: $S = \int d^4x \sqrt{-g} [ \frac{R}{16\pi G} - \frac{1}{2}(\nabla \Phi)^2 - V(\Phi) + \mathcal{L}_{int}(\Phi, T) + \mathcal{L}_m ]$.
        Wait, the Derivation Agent proposed a "Hereditary Tensor." Let's try to keep that essence but make it rigorous.
        Let $\mathcal{M}_{\mu\nu}$ be a field such that:
        $\Box \mathcal{M}_{\mu\nu} - \mu^2 \mathcal{M}_{\mu\nu} = \alpha T_{\mu\nu}$
        Then $G_{\mu\nu} = 8\pi G (T_{\mu\nu} + \mathcal{M}_{\mu\nu})$.

    *   *Applying the Auditor's Filter:*
        1.  *Covariance:* This is covariant.
        2.  *Conservation:* $\nabla^\mu G_{\mu\nu} = 0$. This implies $\nabla^\mu (T_{\mu\nu} + \mathcal{M}_{\mu\nu}) = 0$. But we know $\nabla^\mu T_{\mu\nu} = 0$. Therefore, we *must* have $\nabla^\mu \mathcal{M}_{\mu\nu} = 0$.
        3.  *Consistency Check:* If $\Box \mathcal{M}_{\mu\nu} - \mu^2 \mathcal{M}_{\mu\nu} = \alpha T_{\mu\nu}$, then $\nabla^\mu (\Box \mathcal{M}_{\mu\nu} - \mu^2 \mathcal{M}_{\mu\nu}) = \alpha \nabla^\mu T_{\mu\nu} = 0$. This requires the memory field's divergence to be conserved, which is a strong constraint on $\mathcal{M}_{\mu\nu}$.

    *   *Synthesizing a "Stronger" Formulation:*
        Instead of $\mathcal{M}_{\mu\nu}$ being a free tensor, let it be a projection of the energy-momentum history.
        Let's propose the **GSMH Scalar-Memory formulation** as the first "stable" candidate, as it's easier to defend against the Auditor.
        Actually, let's go with a "Modified Einstein-Hilbert" action that includes a non-local term (which can be localized via auxiliary fields), as this is the standard way to handle "memory" in modified gravity.

    *   *Final Synthesis structure:*
        1.  **Proposed Formulation (GSMH-v0.1):** Define the action and fields.
        2.  **Mathematical Derivations:** EOMs and Newtonian limit.
        3.  **Status Analysis:** What is proven vs. hypothesized.
        4.  **Remaining Open Problems:** (Incorporating the Auditor's red flags).