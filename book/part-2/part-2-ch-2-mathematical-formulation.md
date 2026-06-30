# Part II, Section 2: Mathematical Formulation of the Potential

## Phase 1: Preparatory Foundations

### Objectives and Checklist

By the end of this section, the reader will:

- [ ] Understand Maxwell's component equations for the electro-tonic intensity $(F, G, H)$ and their relationship to the magnetic induction $(a, b, c)$.
- [ ] Derive the vector relationship $\mathbf{B} = \nabla \times \mathbf{A}$ from Maxwell's component equations.
- [ ] Understand how Maxwell uses the **Coulomb gauge condition** ($\nabla \cdot \mathbf{A} = 0$) to decouple the components of $\mathbf{A}$ into three independent Poisson equations.
- [ ] Derive the circulation integral $\oint \mathbf{A} \cdot d\mathbf{l} = \Phi$ and understand its physical interpretation as magnetic flux.
- [ ] Recognize the distinction between the scalar potential $\Omega$ (multi-valued in regions with currents) and the vector potential $\mathbf{A}$ (single-valued everywhere).
- [ ] Prepare for the notational collision of the letter $H$ in the original 1855 text.

---

### Terminology Mapping: The Electro-tonic Intensity and Magnetic Induction

In Part II, Section 2, Maxwell formalizes the mathematical relationship between the electro-tonic intensity and the magnetic induction. The following table maps the 19th-century terminology to modern vector calculus:

| 19th-Century Term | Maxwell's Symbol | Modern Vector Equivalent | Physical Interpretation |
| :--- | :--- | :--- | :--- |
| **Electro-tonic Intensity (components)** | $F, G, H$ | $\mathbf{A} = (A_x, A_y, A_z)$ | The vector potential of the magnetic field |
| **Magnetic Induction (components)** | $a, b, c$ | $\mathbf{B} = (B_x, B_y, B_z)$ | The curl of the vector potential (Quantity field) |
| **Magnetic Intensity (components)** | $\alpha, \beta, \gamma$ | $\mathbf{H} = (H_x, H_y, H_z)$ | The local driving force of the magnetic field |
| **Curl Relation** | $a = \frac{\partial H}{\partial y} - \frac{\partial G}{\partial z}$, etc. | $\mathbf{B} = \nabla \times \mathbf{A}$ | Magnetic induction is the curl of the vector potential |
| **Coulomb Gauge** | $\frac{dF}{dx} + \frac{dG}{dy} + \frac{dH}{dz} = 0$ | $\nabla \cdot \mathbf{A} = 0$ | Divergence-free constraint on the vector potential |
| **Circulation of $\mathbf{A}$** | $\oint (F \, dx + G \, dy + H \, dz)$ | $\oint \mathbf{A} \cdot d\mathbf{l}$ | Magnetic flux through any surface spanning the loop |
| **Magnetic Flux** | $\Phi$ | $\Phi = \iint_S \mathbf{B} \cdot d\mathbf{S}$ | Total magnetic induction through a surface |

**Critical Notational Warning:** The reader must be alert to a prominent notational collision in Maxwell's 1855 paper. Maxwell uses the uppercase letter **$H$** for two completely different quantities:
1.  The scalar **$z$-component of the vector potential**: $\mathbf{A} = (F, G, H)$ (used in the component equations above).
2.  The **vector field symbol for Magnetic Intensity**: $\mathbf{H} = (\alpha, \beta, \gamma)$.
Carefully evaluate the context of each mathematical passage to ensure these two quantities are not conflated.

---

### Mathematical Note: The Component Equations and the Curl Relation

#### 1. Maxwell's Component Equations for the Electro-tonic Intensity

In Part II, Section 2, Maxwell defines the electro-tonic intensity $\mathbf{A}$ with components $(F, G, H)$. The magnetic induction $\mathbf{B}$ with components $(a, b, c)$ is defined as the curl of $\mathbf{A}$:

$$a = \frac{\partial H}{\partial y} - \frac{\partial G}{\partial z}, \quad b = \frac{\partial F}{\partial z} - \frac{\partial H}{\partial x}, \quad c = \frac{\partial G}{\partial x} - \frac{\partial F}{\partial y}$$

In modern vector notation, this system of scalar equations is written compactly as:

$$\mathbf{B} = \nabla \times \mathbf{A}$$

Taking the divergence of both sides satisfies the solenoidal condition ($\nabla \cdot \mathbf{B} = 0$) because the divergence of a curl is identically zero ($\nabla \cdot (\nabla \times \mathbf{A}) = 0$). In Maxwell's component notation:

$$\frac{\partial a}{\partial x} + \frac{\partial b}{\partial y} + \frac{\partial c}{\partial z} = 0$$

#### 2. The Coulomb Gauge and Component Decoupling

The curl relation $\mathbf{B} = \nabla \times \mathbf{A}$ does not uniquely determine $\mathbf{A}$. Adding the gradient of any scalar function ($\nabla \phi$) to $\mathbf{A}$ leaves $\mathbf{B}$ unchanged:

$$\nabla \times (\mathbf{A} + \nabla \phi) = \nabla \times \mathbf{A} = \mathbf{B}$$

To resolve this non-uniqueness and decouple the field equations, **Maxwell explicitly introduces the divergence-free condition in Part II, Section 2** [1]:

$$\frac{dF}{dx} + \frac{dG}{dy} + \frac{dH}{dz} = 0 \implies \nabla \cdot \mathbf{A} = 0$$

To see why this constraint (the **Coulomb gauge**) is mathematically essential, we substitute the curl relation into Ampère's Law ($\nabla \times \mathbf{H} = 4\pi \mathbf{J}$ in a uniform medium of unit permeability, where $\mathbf{B} = \mathbf{H}$):

$$\nabla \times (\nabla \times \mathbf{A}) = 4\pi \mathbf{J}$$

Using the standard vector identity $\nabla \times (\nabla \times \mathbf{A}) = \nabla(\nabla \cdot \mathbf{A}) - \nabla^2 \mathbf{A}$ yields:

$$\nabla(\nabla \cdot \mathbf{A}) - \nabla^2 \mathbf{A} = 4\pi \mathbf{J}$$

Imposing the Coulomb gauge condition ($\nabla \cdot \mathbf{A} = 0$) causes the first term to vanish, leading to the **Vector Poisson Equation** [2]:

$$\nabla^2 \mathbf{A} = -4\pi \mathbf{J}$$

Written out in Cartesian components, this vector relation decouples into three independent scalar Poisson equations:

$$\nabla^2 F = -4\pi u, \quad \nabla^2 G = -4\pi v, \quad \nabla^2 H = -4\pi w$$

where $u, v, w$ are the components of the current density $\mathbf{J}$. This step allowed Maxwell to solve for the components of the vector potential independently using standard scalar potential integration.

#### 3. The Circulation Integral and Magnetic Flux

Applying Stokes' Theorem, the circulation of $\mathbf{A}$ around any closed curve $C$ equals the flux of the magnetic induction $\mathbf{B}$ through any surface $S$ spanning the curve:

$$\oint_C \mathbf{A} \cdot d\mathbf{l} = \iint_S (\nabla \times \mathbf{A}) \cdot d\mathbf{S} = \iint_S \mathbf{B} \cdot d\mathbf{S} = \Phi$$

In Maxwell's coordinate notation, this integral theorem is written as:

$$\oint_C (F \, dx + G \, dy + H \, dz) = \iint_S (a \, dy \, dz + b \, dz \, dx + c \, dx \, dy)$$

This connects the electro-tonic intensity directly to magnetic flux.

---

### Connections to Later Papers

| Concept in Paper 1 | Later Development |
| :--- | :--- |
| $\mathbf{B} = \nabla \times \mathbf{A}$ | **Paper 2 (1861):** This equation is retained as one of Maxwell's fundamental field equations. |
| Coulomb gauge $\nabla \cdot \mathbf{A} = 0$ | **Paper 3 (1865):** Maxwell maintains the Coulomb gauge in his dynamical theory of the field. |
| Circulation integral $\oint \mathbf{A} \cdot d\mathbf{l} = \Phi$ | **Paper 3 (1865):** This relationship is used to derive Faraday's law in integral form. |
| Physical Reality of $\mathbf{A}$ | **Heaviside (1893):** Heaviside actively rejected the potential as "metaphysical clutter" [4]. The physical reality of the vector potential was ultimately vindicated by the quantum-mechanical **Aharonov-Bohm Effect (1959)** [3], demonstrating that $\mathbf{A}$ causes measurable phase shifts in regions where the force fields $\mathbf{E}$ and $\mathbf{B}$ are zero. |

---

### Pre-Reading Checklist for Phase 2

Before proceeding to the active reading of Maxwell's mathematical formulation of the potential, the reader should confirm:

- [ ] The component equations $a = \frac{\partial H}{\partial y} - \frac{\partial G}{\partial z}$, etc., and the dual meaning of the letter $H$ are understood.
- [ ] The vector relationship $\mathbf{B} = \nabla \times \mathbf{A}$ is recognized.
- [ ] The Coulomb gauge condition $\nabla \cdot \mathbf{A} = 0$ is understood as Maxwell's method for decoupling the components of $\mathbf{A}$ into independent Poisson equations.
- [ ] The circulation integral $\oint \mathbf{A} \cdot d\mathbf{l} = \Phi$ is recognized as the magnetic flux through the loop.
- [ ] The single-valuedness of $\mathbf{A}$ (as opposed to the multi-valued scalar potential $\Omega$) is recognized.

---

### Connection to the Rest of the Exegesis

*   **Phase 2 (Active Reading):** The reader will encounter Maxwell's component equations for the electro-tonic intensity, his introduction of the Coulomb gauge condition, and his derivation of the circulation integral. The terminology mapping above will guide the translation of his 19th-century language.
*   **Phase 3 (Mathematical Formalization):** After reading, the reader will formalize the curl relation in vector notation, derive the circulation-flux relationship, and discuss the gauge freedom and its resolution via the Coulomb gauge.
*   **Phase 4 (Computational Visualization):** The reader will generate combined visualizations showing the vector potential $\mathbf{A}$ and its resulting curl field $\mathbf{B}$ for a current loop, visualizing the relationship between the two fields.

---

### References

[1] Bork, A. M. (1966). Physics just before Einstein. *Science*, 152(3722), 597–603.

[2] Jackson, J. D. (1999). *Classical Electrodynamics*. John Wiley & Sons.

[3] Aharonov, Y., & Bohm, D. (1959). Significance of electromagnetic potentials in the quantum theory. *Physical Review*, 115(3), 485–491.

[4] Heaviside, O. (1893). *Electromagnetic Theory*. London: The Electrician Printing and Publishing Company.