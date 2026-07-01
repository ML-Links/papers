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

## Phase 3: Mathematical & Theoretical Formalization

### Translation Protocol (4 Steps)

The following protocol provides a systematic method for translating Maxwell's 1855 Cartesian component equations into modern vector notation [1]. This protocol should be applied to each mathematical passage encountered during Phase 2.

---

**Step 1: Write Maxwell's Original Cartesian Component Equations**

Record Maxwell's component equations exactly as they appear in the 1855 text, preserving his notation and coordinate conventions.

**Step 2: Identify the Modern Physical Quantities**

Map Maxwell's 19th-century symbols to their modern vector equivalents, maintaining the dual-layered conduction and magnetostatic analogies.

| Maxwell's 1855 Symbol | Physical Quantity | Modern Symbol | Electrostatic Analog | Magnetostatic Analog |
| :--- | :--- | :--- | :--- | :--- |
| $F, G, H$ | Electro-tonic intensity components | $\mathbf{A} = (A_x, A_y, A_z)$ | — | Vector Potential $\mathbf{A}$ |
| $a, b, c$ | Magnetic induction components | $\mathbf{B} = (B_x, B_y, B_z)$ | — | Magnetic Induction $\mathbf{B}$ |
| $\alpha, \beta, \gamma$ | Magnetic intensity components | $\mathbf{H} = (\alpha, \beta, \gamma)$ | — | Magnetic Intensity $\mathbf{H}$ |
| $u, v, w$ | Current density components | $\mathbf{J} = (J_x, J_y, J_z)$ | Current Density $\mathbf{J}$ | Current Density $\mathbf{J}$ |
| $k$ | Media resistance / reluctivity | $k = 1/\mu$ | Resistivity | Reluctivity |
| $\mu$ | Magnetic permeability | $\mu = 1/k$ | Conductivity | Permeability |

> **Notational Warning:** The letter $H$ represents both the scalar $z$-component of the vector potential $\mathbf{A} = (F, G, H)$ and the vector field symbol for Magnetic Intensity $\mathbf{H} = (\alpha, \beta, \gamma)$. This dual usage requires careful contextual differentiation during translation.

**Step 3: Convert to Modern Vector Notation**

Rewrite the component equations as a single vector equation using the operators $\nabla$, $\cdot$, and $\times$.

**Step 4: State the Physical Meaning in Modern English**

Articulate the physical meaning of the translated equation in clear, modern language, with explicit acknowledgment of the dual-layered analogical framework and the physical interpretation of the vector potential.

---

### Component-to-Vector Translation

#### Translation 1: The Vector Poisson Equation Under Coulomb Gauge

**Step 1: Maxwell's Original Component Equations**

Maxwell combines the curl relation $\mathbf{B} = \nabla \times \mathbf{A}$ with Ampère's Law ($\nabla \times \mathbf{H} = 4\pi \mathbf{J}$) under the isotropic media relation $\mathbf{B} = \mu \mathbf{H}$. By imposing the divergence-free condition $\frac{\partial F}{\partial x} + \frac{\partial G}{\partial y} + \frac{\partial H}{\partial z} = 0$, he reduces the equations to three independent Cartesian components [1]:

$$\frac{\partial^2 F}{\partial x^2} + \frac{\partial^2 F}{\partial y^2} + \frac{\partial^2 F}{\partial z^2} = -4\pi\mu u$$
$$\frac{\partial^2 G}{\partial x^2} + \frac{\partial^2 G}{\partial y^2} + \frac{\partial^2 G}{\partial z^2} = -4\pi\mu v$$
$$\frac{\partial^2 H}{\partial x^2} + \frac{\partial^2 H}{\partial y^2} + \frac{\partial^2 H}{\partial z^2} = -4\pi\mu w$$

**Step 2: Identify the Modern Physical Quantities**

| Maxwell's 1855 Symbol | Physical Quantity | Modern Symbol | Electrostatic Analog | Magnetostatic Analog |
| :--- | :--- | :--- | :--- | :--- |
| $F, G, H$ | Electro-tonic intensity components | $\mathbf{A} = (A_x, A_y, A_z)$ | — | Vector Potential $\mathbf{A}$ |
| $u, v, w$ | Current density components | $\mathbf{J} = (J_x, J_y, J_z)$ | Current Density $\mathbf{J}$ | Current Density $\mathbf{J}$ |
| $\mu$ | Magnetic permeability | $\mu = 1/k$ | Conductivity | Permeability |

**Step 3: Convert to Modern Vector Notation**

Using the Laplacian operator $\nabla^2$ on the vector field $\mathbf{A}$ under the Coulomb gauge $\nabla \cdot \mathbf{A} = 0$:

$$\nabla^2 \mathbf{A} = -4\pi\mu\mathbf{J} = -\frac{4\pi}{k}\mathbf{J}$$

**Step 4: State the Physical Meaning in Modern English**

Imposing the Coulomb gauge condition decouples the curl-of-curl operator $\nabla \times (\nabla \times \mathbf{A}) = \nabla(\nabla \cdot \mathbf{A}) - \nabla^2 \mathbf{A}$ into three independent scalar Poisson equations [2].
*   **Physical Interpretation:** Each component of the vector potential is generated by its corresponding component of current density. This indicates that electric currents act as the physical sources of the electro-tonic state, scaled by the magnetic permeability $\mu$ (or the inverse of the medium's resistance, $1/k$).
*   **Media Inhomogeneity:** In regions where the resistance $k$ of the medium varies spatially, the decoupling is no longer straightforward, representing a boundary condition challenge that Maxwell addresses using porous media analogies.

---

#### Translation 2: The Volume Integral Solution of the Potential

**Step 1: Maxwell's Original Component Equations**

By applying Green's potential integration to the decoupled scalar Poisson equations, Maxwell expresses the components of the electro-tonic state at any point in space as volume integrals over all active currents [1]:

$$F = \iiint \frac{\mu u}{r} \, dx \, dy \, dz$$
$$G = \iiint \frac{\mu v}{r} \, dx \, dy \, dz$$
$$H = \iiint \frac{\mu w}{r} \, dx \, dy \, dz$$

**Step 2: Identify the Modern Physical Quantities**

| Maxwell's 1855 Symbol | Physical Quantity | Modern Symbol | Electrostatic Analog | Magnetostatic Analog |
| :--- | :--- | :--- | :--- | :--- |
| $F, G, H$ | Electro-tonic intensity components | $\mathbf{A} = (A_x, A_y, A_z)$ | — | Vector Potential $\mathbf{A}$ |
| $u, v, w$ | Current density components | $\mathbf{J} = (J_x, J_y, J_z)$ | Current Density $\mathbf{J}$ | Current Density $\mathbf{J}$ |
| $\mu$ | Magnetic permeability | $\mu = 1/k$ | Conductivity | Permeability |
| $r$ | Distance from source to field point | $r$ | Distance $r$ | Distance $r$ |

**Step 3: Convert to Modern Vector Notation**

The three component integrals combine into a single vector volume integral:

$$\mathbf{A}(\mathbf{r}) = \iiint_V \frac{\mu \mathbf{J}(\mathbf{r}')}{|\mathbf{r} - \mathbf{r}'|} \, d^3r' = \iiint_V \frac{\mathbf{J}(\mathbf{r}')}{k |\mathbf{r} - \mathbf{r}'|} \, d^3r'$$

**Step 4: State the Physical Meaning in Modern English**

The vector potential $\mathbf{A}$ at a field point $\mathbf{r}$ is the weighted volume sum of all current elements $\mathbf{J}$ in the system, where the contribution of each element decreases inversely with the distance $|\mathbf{r} - \mathbf{r}'|$ [2].
*   **Analogical Mapping:** This integral is mathematically identical to the electrostatic potential integral $\Phi = \iiint \frac{\rho}{r} dV$, demonstrating that each component of the vector potential propagates from current sources in the same manner as the electrostatic potential propagates from charge sources.
*   **Media Influence:** The presence of the reluctivity parameter $k$ in the denominator shows that media with higher resistance to lines of force (lower permeability) shield and diminish the strength of the generated vector potential.

---

#### Translation 3: Coulomb's Law of Point Poles Shielded by Reluctivity

**Step 1: Maxwell's Original Component Equations**

When analyzing the forces exerted between isolated magnetic poles (represented as centers of fluid source and sink lines), Maxwell scales the direct interaction by the resistive property of the intervening medium [1]:

$$F = - \frac{k m_1 m_2}{r^2}$$

**Step 2: Identify the Modern Physical Quantities**

| Maxwell's 1855 Symbol | Physical Quantity | Modern Symbol | Electrostatic Analog | Magnetostatic Analog |
| :--- | :--- | :--- | :--- | :--- |
| $F$ | Force between poles | $\mathbf{F}_{12}$ | Coulomb Force | Magnetostatic Force |
| $m_1, m_2$ | Strengths of magnetic poles | $m_1, m_2$ | Electric Charges $q_1, q_2$ | Pole Strengths $m_1, m_2$ |
| $k$ | Media resistance / reluctivity | $k = 1/\mu$ | $1/\epsilon$ | Reluctivity $1/\mu$ |

**Step 3: Convert to Modern Vector Notation**

Expressing the interaction as a vector force acting along the unit vector $\hat{\mathbf{r}}$:

$$\mathbf{F}_{12} = -k \frac{m_1 m_2}{r^2} \hat{\mathbf{r}} = -\frac{1}{\mu} \frac{m_1 m_2}{r^2} \hat{\mathbf{r}}$$

**Step 4: State the Physical Meaning in Modern English**

The force between two magnetic poles is directly proportional to their pole strengths and inversely proportional to the square of the distance separating them, scaled by the reluctivity $k$ of the medium [2].
*   **Physical Interpretation:** This formulation shows that the magnetic force is shielded by the medium's reluctivity (resistance $k = 1/\mu$). A highly resistive medium (high $k$, low permeability $\mu$) increases the force because it resists the dispersion of the lines of force, focusing them along the axis of interaction.
*   **Unified Analogy:** By formulating the force with the parameter $k$, Maxwell keeps the magnetostatic interaction consistent with the fluid pressure gradients of Part I, where the force is proportional to the resistance to the flow.

---

#### Translation 4: The Distinction Between Scalar and Vector Potentials

**Step 1: Maxwell's Original Component Equations**

Maxwell contrasts the irrotational magnetic intensity $\mathbf{H}$ represented by a scalar potential gradient in Part I with the solenoidal magnetic induction $\mathbf{B}$ represented by the curl of the vector potential in Part II [1]:

$$\alpha = -\frac{\partial \Omega}{\partial x}, \quad \beta = -\frac{\partial \Omega}{\partial y}, \quad \gamma = -\frac{\partial \Omega}{\partial z}$$
$$a = \frac{\partial H}{\partial y} - \frac{\partial G}{\partial z}, \quad b = \frac{\partial F}{\partial z} - \frac{\partial H}{\partial x}, \quad c = \frac{\partial G}{\partial x} - \frac{\partial F}{\partial y}$$

**Step 2: Identify the Modern Physical Quantities**

| Maxwell's 1855 Symbol | Physical Quantity | Modern Symbol | Electrostatic Analog | Magnetostatic Analog |
| :--- | :--- | :--- | :--- | :--- |
| $\Omega$ | Scalar magnetic potential | $\Omega$ | Electric Potential $\phi$ | Scalar Potential $\Omega$ |
| $F, G, H$ | Electro-tonic intensity components | $\mathbf{A} = (A_x, A_y, A_z)$ | — | Vector Potential $\mathbf{A}$ |
| $\alpha, \beta, \gamma$ | Magnetic intensity components | $\mathbf{H} = (H_x, H_y, H_z)$ | — | Magnetic Intensity $\mathbf{H}$ |
| $a, b, c$ | Magnetic induction components | $\mathbf{B} = (B_x, B_y, B_z)$ | — | Magnetic Induction $\mathbf{B}$ |

**Step 3: Convert to Modern Vector Notation**

The scalar potential and vector potential relations are written respectively as:

$$\mathbf{H} = -\nabla \Omega \quad \text{(Irrotational field description)}$$
$$\mathbf{B} = \nabla \times \mathbf{A} \quad \text{(Solenoidal field description)}$$

**Step 4: State the Physical Meaning in Modern English**

The two potential formulations represent distinct topological properties of the magnetic field [2].
*   **Scalar Potential $\Omega$:** This is valid only in source-free regions where no electric currents flow ($\nabla \times \mathbf{H} = 0$). In regions enclosing current loops, the scalar potential is multi-valued ($\oint \mathbf{H} \cdot d\mathbf{l} = 4\pi I_{\text{enc}}$), limiting its mathematical utility.
*   **Vector Potential $\mathbf{A}$:** This is valid everywhere, including inside active conductors. Because it is defined via a curl relation, it remains single-valued throughout all space, making it a more complete representation of the field's physical state.

---

### Standardized Commentary Block

*   **The Goal:** Maxwell's objective in Part II, Section 2 is to mathematically construct the vector potential components from physical current sources, establishing a continuous differential framework for the electro-tonic state.
*   **The Method:** He applies the Coulomb gauge $\nabla \cdot \mathbf{A} = 0$ to decouple the Cartesian curl-of-curl operations. This allows him to use Poisson's equations and Green's volume integration to solve for $(F, G, H)$ as potentials generated by the current components $(u, v, w)$.
*   **The Limitation:** Although mathematically rigorous, the formulation in Paper 1 is restricted to steady-state systems. It lacks the displacement current term, meaning the equations do not yet describe the propagation of electromagnetic waves through the medium.
*   **The Legacy:** By decoupling the components of the vector potential and expressing them as integrals over current distributions, Maxwell laid the groundwork for the dynamical equations of the electromagnetic field in Paper 3 and modern classical electrodynamics.

---

### Exegesis Workflow Callout

#### Zone 2 Quality Control Verification
Prior to beginning active analysis of Section 2, the reader must verify that:
1. The notation $(F, G, H)$ is preserved without modern subscripts.
2. The reluctivity parameter $k$ is explicitly defined as $1/\mu$ in the Poisson equation and Coulomb force translations.
3. The double-duty of the letter $H$ is highlighted in the translation notes to prevent confusion during reading.

#### Post-Reading Reconciliation & Status Lock
Upon completing the active analysis and Phase 4 visualization:
1. Reconcile the volume integrals of Translation 2 with the visual models of current loops developed in Phase 4.
2. Confirm that the boundaries of media with varying reluctivity $k$ are correctly treated in the code.
3. Update the tracking metadata at the top of the file, changing the status from `skeleton` to `complete`.

---

### Connections to Later Papers

| Concept in Paper 1 | Later Development |
| :--- | :--- |
| $\nabla^2 \mathbf{A} = -4\pi\mu\mathbf{J}$ (Vector Poisson) | **Paper 3 (1865):** Expanded to include the dynamic displacement current: $\nabla^2 \mathbf{A} - \mu\epsilon \frac{\partial^2 \mathbf{A}}{\partial t^2} = -4\pi\mu\mathbf{J}$. |
| $\mathbf{A}(\mathbf{r}) = \iiint \frac{\mu\mathbf{J}}{r} dV$ (Potential Integral) | **Paper 3 (1865):** Standardized as the retarded potential solution when electromagnetic propagation delays are introduced. |
| $F_{12} = -k \frac{m_1 m_2}{r^2} \hat{\mathbf{r}}$ (Shielded Force) | **Treatise (1873):** Re-derived in terms of magnetic energy density stored within the surrounding medium. |
| Single-valuedness of $\mathbf{A}$ vs. Multi-valuedness of $\Omega$ | **Heaviside (1893):** Heaviside mathematically bypassed the scalar potential multi-valuedness using curl equations directly, marginalizing the vector potential. |

---

### References Integration Callout

#### The Treatise on Electricity and Magnetism (1873)

The following articles of Maxwell's *Treatise* provide direct commentary on the mathematical formulation of the potential:

| *Treatise* Article | Connection to Section 2 |
| :--- | :--- |
| **Articles 405–406** | Mathematical proof of the single-valuedness of the vector potential in the presence of currents [2]. |
| **Article 617** | The derivation of the component Poisson equations from the curl relation under the Coulomb gauge [2]. |
| **Article 618** | The volume integration of current density components to yield the vector potential [2]. |

#### Heaviside's Electromagnetic Theory (1893)

Heaviside's vector reformulations provide a modern perspective on the potential formulation:

| Heaviside Section | Connection to Section 2 |
| :--- | :--- |
| **Volume I, Section 32** | Treatment of Poisson's equation in vector notation [3]. |
| **Volume II, Section 224** | Historical critique of the physical reality of the vector potential and the introduction of the modern vector equations [3]. |

#### Integration Instructions

During Phase 2 (Active Reading), the reader should:
1. Cross-reference Maxwell's volume integrals for $F$, $G$, and $H$ with Article 618 of the *Treatise* to see how the mathematical notation evolved.
2. Note how Heaviside’s avoidance of the vector potential in Section 32 affects the expression of the field's boundary conditions.

---

### References

[1] Maxwell, J. C. (1858). *On Faraday's Lines of Force*. Transactions of the Cambridge Philosophical Society, Vol. X, Part I. *(Read in two parts: Part I on Dec 10, 1855; Part II on Feb 11, 1856. Published in 1858.)*

[2] Maxwell, J. C. (1873). *A Treatise on Electricity and Magnetism*. Oxford: Clarendon Press.

[3] Heaviside, O. (1893). *Electromagnetic Theory*. London: The Electrician Printing and Publishing Company.

[4] Jackson, J. D. (1999). *Classical Electrodynamics*. John Wiley & Sons.

[5] Bork, A. M. (1966). Physics just before Einstein. *Science*, 152(3722), 597–603.

[6] Jackson, J. D. (1999). *Classical Electrodynamics*. John Wiley & Sons.

[7] Aharonov, Y., & Bohm, D. (1959). Significance of electromagnetic potentials in the quantum theory. *Physical Review*, 115(3), 485–491.

[8] Heaviside, O. (1893). *Electromagnetic Theory*. London: The Electrician Printing and Publishing Company.