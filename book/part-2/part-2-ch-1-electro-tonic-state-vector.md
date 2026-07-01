# Part II, Section 1: The Electro-tonic State as a Vector Quantity

## Phase 1: Preparatory Foundations

### Objectives and Checklist

By the end of this section, the reader will:

- [ ] Understand Faraday's concept of the **electro-tonic state** as a condition of tension or momentum in the field.
- [ ] Recognize that the electro-tonic state must be represented by a **vector field** $\mathbf{A}$, not a scalar potential.
- [ ] Understand the relationship between the electro-tonic state and the magnetic induction: $\mathbf{B} = \nabla \times \mathbf{A}$.
- [ ] Recognize that the vector potential $\mathbf{A}$ is **single-valued** everywhere, including in regions containing currents (unlike the scalar potential $\Omega$ which is multi-valued).
- [ ] Understand how Maxwell resolves the mathematical non-uniqueness of the curl relation by introducing the **Coulomb gauge condition** ($\nabla \cdot \mathbf{A} = 0$).
- [ ] Appreciate the physical interpretation of $\mathbf{A}$ as "electromagnetic momentum" through the canonical momentum framework.

---

### Terminology Mapping: Electro-tonic State, Electro-tonic Intensity, and Electromagnetic Momentum

In Part II, Maxwell introduces the electro-tonic state as a fundamental quantity of the field. The following table maps the 19th-century terminology to modern vector calculus and physical interpretations:

| 19th-Century Term | Maxwell's Symbol | Modern Vector Equivalent | Physical Interpretation |
| :--- | :--- | :--- | :--- |
| **Electro-tonic State** | — (conceptual) | $\mathbf{A}$ (Vector Potential) | The state of tension or strain in the field |
| **Electro-tonic Intensity** | $F, G, H$ (components) | $\mathbf{A} = (A_x, A_y, A_z)$ | The vector potential of the magnetic field |
| **Magnetic Induction** | $a, b, c$ (components) | $\mathbf{B} = \nabla \times \mathbf{A}$ | The curl of the vector potential (Quantity field) |
| **Magnetic Intensity** | $\alpha, \beta, \gamma$ (components) | $\mathbf{H} = \frac{1}{\mu}\mathbf{B}$ | The local driving force of the magnetic field |
| **Circulation of $\mathbf{A}$** | $\oint (F \, dx + G \, dy + H \, dz)$ | $\oint \mathbf{A} \cdot d\mathbf{l}$ | Magnetic flux ($\Phi$) through any surface spanning the loop |

**Critical Distinction:** The electro-tonic state is a **vector field** $\mathbf{A}$, not a scalar potential. It has three components $(F, G, H)$ and is defined at every point in space. Unlike the scalar potential $\Omega$ (which is multi-valued in regions containing currents), the vector potential $\mathbf{A}$ is **single-valued** everywhere, including in the presence of currents. This is a crucial advantage of the vector potential formulation.

**Physical Interpretation:** Maxwell interprets the electro-tonic state as a "momentum" or "tension" in the field. This is not a mechanical momentum in the sense of mass times velocity, but rather a **field momentum**—a quantity that represents the stored energy and dynamic state of the electromagnetic field. In modern physics, $\mathbf{A}$ is recognized as the canonical momentum conjugate to the position of a charged particle in the field.

---

### Mathematical Note: The Vector Potential and Its Properties

#### 1. Definition of the Vector Potential

Maxwell defines the electro-tonic intensity $\mathbf{A}$ such that the magnetic induction $\mathbf{B}$ is its curl:

$$\mathbf{B} = \nabla \times \mathbf{A}$$

In component form, using Maxwell's original 1855 notation where $a, b, c$ are the components of magnetic induction and $F, G, H$ are the components of the electro-tonic intensity [1]:

$$a = \frac{\partial H}{\partial y} - \frac{\partial G}{\partial z}, \quad b = \frac{\partial F}{\partial z} - \frac{\partial H}{\partial x}, \quad c = \frac{\partial G}{\partial x} - \frac{\partial F}{\partial y}$$

#### 2. Why the Curl?

The choice of the curl operator is not arbitrary. There are several reasons why $\mathbf{B}$ must be the curl of $\mathbf{A}$:

1.  **Divergence-Free Condition:** The magnetic induction satisfies $\nabla \cdot \mathbf{B} = 0$ (no magnetic monopoles). Taking the divergence of a curl gives zero identically:
    $$\nabla \cdot (\nabla \times \mathbf{A}) = 0$$
    Thus, $\mathbf{B} = \nabla \times \mathbf{A}$ automatically satisfies the divergence-free condition.
2.  **Circulation and Flux:** The circulation of $\mathbf{A}$ around a closed curve equals the flux of $\mathbf{B}$ through any surface $S$ spanning the curve (by Stokes' Theorem):
    $$\oint_C \mathbf{A} \cdot d\mathbf{l} = \iint_S (\nabla \times \mathbf{A}) \cdot d\mathbf{S} = \iint_S \mathbf{B} \cdot d\mathbf{S} = \Phi$$
    This is the exact analogue of the circulation-velocity relation from Part I, but now applied to the magnetic field.
3.  **Single-Valuedness:** Unlike the scalar potential $\Omega$, which is multi-valued in regions containing currents, the vector potential $\mathbf{A}$ is **single-valued** everywhere. This is because the curl of a gradient is zero, and $\mathbf{A}$ can be chosen to be gauge-invariant.

#### 3. The Coulomb Gauge Condition ($\nabla \cdot \mathbf{A} = 0$)

The vector potential $\mathbf{A}$ is not mathematically unique under the curl relation alone. Since the curl of any gradient is zero ($\nabla \times (\nabla \phi) = 0$), we can add the gradient of any scalar function to $\mathbf{A}$ without changing the resulting magnetic induction field $\mathbf{B}$:

$$\mathbf{A}' = \mathbf{A} + \nabla \phi \implies \nabla \times \mathbf{A}' = \nabla \times \mathbf{A} = \mathbf{B}$$

While the general concept of "gauge symmetry" was formalized in the 20th century, Maxwell was acutely aware of this mathematical non-uniqueness in 1855. To constrain this freedom and ensure a unique solution, **Maxwell explicitly introduced the divergence-free constraint in Part II, Section 2** [1]:

$$\frac{dF}{dx} + \frac{dG}{dy} + \frac{dH}{dz} = 0 \implies \nabla \cdot \mathbf{A} = 0$$

This is the first historical formulation of the **Coulomb gauge condition**.

#### 4. The Canonical Momentum Interpretation of $\mathbf{A}$

To mathematically ground Maxwell’s intuitive interpretation of the electro-tonic state as "electromagnetic momentum," we evaluate the Lagrangian formulation of a classical particle with mass $m$ and electric charge $q$ moving through an electromagnetic field. The **canonical momentum ($\mathbf{p}$)** of the particle is defined as [2]:

$$\mathbf{p} = m\mathbf{v} + q\mathbf{A}$$

where:
*   $m\mathbf{v}$ is the ordinary **mechanical momentum** of the particle.
*   $q\mathbf{A}$ represents the **potential momentum** stored in the electromagnetic field.

If the electromagnetic field varies over time, an induced electric field $\mathbf{E} = -\frac{\partial \mathbf{A}}{\partial t}$ is generated, altering the particle's mechanical momentum. Newton's second law for the particle is formulated as:

$$\frac{d(m\mathbf{v})}{dt} = q\mathbf{E} = -q\frac{\partial \mathbf{A}}{\partial t}$$

$$\frac{d}{dt}(m\mathbf{v} + q\mathbf{A}) = 0 \implies \frac{d\mathbf{p}}{dt} = 0$$

This demonstrates that **the canonical momentum ($\mathbf{p}$) of the system is conserved during induction** [2]. The particle's mechanical acceleration is a direct momentum exchange with the field's potential momentum, verifying Maxwell's 1855 conceptualization of the vector potential $\mathbf{A}$ as a physical momentum field.

---

### Pre-Reading Checklist for Phase 2

Before proceeding to the active reading of Maxwell's text on the electro-tonic state, the reader should confirm:

- [ ] The definition $\mathbf{B} = \nabla \times \mathbf{A}$ is clearly understood.
- [ ] The single-valuedness of $\mathbf{A}$ (as opposed to the multi-valued scalar potential $\Omega$) is recognized.
- [ ] The relationship between the circulation of $\mathbf{A}$ and magnetic flux is understood via Stokes' Theorem.
- [ ] Maxwell's introduction of the Coulomb gauge condition ($\nabla \cdot \mathbf{A} = 0$) is recognized.
- [ ] The physical interpretation of $\mathbf{A}$ as "electromagnetic momentum" is grounded in the canonical momentum relation ($\mathbf{p} = m\mathbf{v} + q\mathbf{A}$).

---

### Connection to the Rest of the Exegesis

*   **Phase 2 (Active Reading):** The reader will encounter Maxwell's introduction of the electro-tonic state, his discussion of its physical meaning, and his initial formulation of the vector potential. The terminology mapping above will guide the translation of his 19th-century language.
*   **Phase 3 (Mathematical Formalization):** After reading, the reader will formalize the definition $\mathbf{B} = \nabla \times \mathbf{A}$ in vector notation, derive the circulation-flux relation, and discuss the gauge freedom of the potential.
*   **Phase 4 (Computational Visualization):** The reader will generate 3D vector field plots of $\mathbf{A}$ surrounding a current loop, visualizing the vector potential and its relationship to the magnetic field $\mathbf{B}$.

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
| $\alpha, \beta, \gamma$ | Magnetic intensity components | $\mathbf{H} = (H_x, H_y, H_z)$ | — | Magnetic Intensity $\mathbf{H}$ |
| $\Psi$ | Electrostatic potential | $\Psi$ | Electric Potential $\phi$ | — |
| $dx, dy, dz$ | Line element components | $d\mathbf{l} = (dx, dy, dz)$ | Line element $d\mathbf{l}$ | Line element $d\mathbf{l}$ |

**Step 3: Convert to Modern Vector Notation**

Rewrite the component equations as a single vector equation using the operators $\nabla$, $\cdot$, and $\times$.

**Step 4: State the Physical Meaning in Modern English**

Articulate the physical meaning of the translated equation in clear, modern language, with explicit acknowledgment of the dual-layered analogical framework and the physical interpretation of the vector potential.

---

### Component-to-Vector Translation

#### Translation 1: Definition of the Electro-tonic Intensity

**Step 1: Maxwell's Original Component Equations**

In Part II, Section 1, Maxwell introduces the electro-tonic intensity as a vector quantity with components $(F, G, H)$ [1]:

$$\mathbf{A} = (F, G, H)$$

The electro-tonic state is the physical condition of the field at each point in space, represented by this vector quantity.

**Step 2: Identify the Modern Physical Quantities**

| Maxwell's Symbol | Physical Quantity | Modern Symbol | Electrostatic Analog | Magnetostatic Analog |
| :--- | :--- | :--- | :--- | :--- |
| $F, G, H$ | Electro-tonic intensity components | $\mathbf{A} = (A_x, A_y, A_z)$ | — | Vector Potential $\mathbf{A}$ |

**Step 3: Convert to Modern Vector Notation**

The electro-tonic intensity is written compactly as:

$$\mathbf{A} = (F, G, H)$$

**Step 4: State the Physical Meaning in Modern English**

Maxwell introduces the electro-tonic intensity $\mathbf{A}$ as a fundamental vector field representing the state of the field at each point in space. This is the first historical appearance of the **magnetic vector potential** as a primary physical quantity [1].

*   **Physical Interpretation:** Maxwell interprets $\mathbf{A}$ as a "momentum" or "tension" in the field—a quantity that represents the stored energy and dynamic state of the electromagnetic field.
*   **Modern Interpretation:** $\mathbf{A}$ is recognized as the canonical momentum conjugate to the position of a charged particle in the field: $\mathbf{p} = m\mathbf{u} + q\mathbf{A}$ (where $\mathbf{u}$ is the physical velocity of the charge carrier).

**Critical Distinction:** Unlike the scalar potential $\Omega$ (which is multi-valued in regions containing currents), the vector potential $\mathbf{A}$ is **single-valued** everywhere, including in the presence of currents. This is a crucial advantage of the vector potential formulation.

---

#### Translation 2: The Curl Relation ($\mathbf{B} = \nabla \times \mathbf{A}$)

**Step 1: Maxwell's Original Component Equations**

Maxwell defines the magnetic induction $(a, b, c)$ as the curl of the electro-tonic intensity [1]:

$$a = \frac{\partial H}{\partial y} - \frac{\partial G}{\partial z}, \quad b = \frac{\partial F}{\partial z} - \frac{\partial H}{\partial x}, \quad c = \frac{\partial G}{\partial x} - \frac{\partial F}{\partial y}$$

**Step 2: Identify the Modern Physical Quantities**

| Maxwell's Symbol | Physical Quantity | Modern Symbol | Electrostatic Analog | Magnetostatic Analog |
| :--- | :--- | :--- | :--- | :--- |
| $a, b, c$ | Magnetic induction components | $\mathbf{B} = (B_x, B_y, B_z)$ | — | Magnetic Induction $\mathbf{B}$ |
| $F, G, H$ | Electro-tonic intensity components | $\mathbf{A} = (A_x, A_y, A_z)$ | — | Vector Potential $\mathbf{A}$ |

**Step 3: Convert to Modern Vector Notation**

The component equations combine into a single vector equation:

$$\mathbf{B} = \nabla \times \mathbf{A}$$

**Step 4: State the Physical Meaning in Modern English**

The magnetic induction $\mathbf{B}$ is the curl of the vector potential $\mathbf{A}$. This is the central mathematical result of Part II [1].
*   **Divergence-Free Condition:** Taking the divergence of both sides gives $\nabla \cdot \mathbf{B} = \nabla \cdot (\nabla \times \mathbf{A}) = 0$, which is the mathematical expression of the fact that magnetic field lines form closed loops (no magnetic monopoles).
*   **Physical Interpretation:** The curl operator captures the circulatory nature of magnetic fields. The vector potential $\mathbf{A}$ is the "source" of the magnetic induction, with the curl operation generating the circulating field lines.

---

#### Translation 3: The Circulation Integral

**Step 1: Maxwell's Original Component Equations**

Applying Stokes' Theorem to the vector potential, the circulation of $\mathbf{A}$ around a closed curve equals the flux of $\mathbf{B}$ through any surface spanning the curve [1]:

$$\oint_C (F \, dx + G \, dy + H \, dz) = \iint_S (a \, dy \, dz + b \, dz \, dx + c \, dx \, dy)$$

**Step 2: Identify the Modern Physical Quantities**

| Maxwell's Symbol | Physical Quantity | Modern Symbol | Electrostatic Analog | Magnetostatic Analog |
| :--- | :--- | :--- | :--- | :--- |
| $F, G, H$ | Electro-tonic intensity components | $\mathbf{A} = (A_x, A_y, A_z)$ | — | Vector Potential $\mathbf{A}$ |
| $a, b, c$ | Magnetic induction components | $\mathbf{B} = (B_x, B_y, B_z)$ | — | Magnetic Induction $\mathbf{B}$ |
| $dx, dy, dz$ | Line element components | $d\mathbf{l}$ | — | Line element |
| $dy \, dz$, etc. | Area elements | $d\mathbf{S}$ | — | Area element |

**Step 3: Convert to Modern Vector Notation**

Stokes' Theorem applied to $\mathbf{A}$ gives:

$$\oint_C \mathbf{A} \cdot d\mathbf{l} = \iint_S (\nabla \times \mathbf{A}) \cdot d\mathbf{S} = \iint_S \mathbf{B} \cdot d\mathbf{S} = \Phi$$

**Step 4: State the Physical Meaning in Modern English**

The circulation of the vector potential $\mathbf{A}$ around any closed curve $C$ equals the magnetic flux $\Phi$ through any surface $S$ spanning the curve [1].
*   **Physical Interpretation:** This is the direct mathematical link between the electro-tonic state (the vector potential) and the magnetic flux. A changing flux ($d\Phi/dt$) corresponds to a changing circulation of $\mathbf{A}$, which induces an electromotive force (Faraday's Law).
*   **Connection to Faraday's Law:** In Part II, Section 3, Maxwell will use this relation to derive the law of electromagnetic induction: $\oint_C \mathbf{E} \cdot d\mathbf{l} = -d\Phi/dt$.

---

#### Translation 4: The Coulomb Gauge Condition ($\nabla \cdot \mathbf{A} = 0$)

**Step 1: Maxwell's Original Component Equations**

To resolve the mathematical non-uniqueness of the curl relation, Maxwell explicitly imposes the divergence-free condition [1]:

$$\frac{dF}{dx} + \frac{dG}{dy} + \frac{dH}{dz} = 0$$

**Step 2: Identify the Modern Physical Quantities**

| Maxwell's Symbol | Physical Quantity | Modern Symbol | Electrostatic Analog | Magnetostatic Analog |
| :--- | :--- | :--- | :--- | :--- |
| $F, G, H$ | Electro-tonic intensity components | $\mathbf{A} = (A_x, A_y, A_z)$ | — | Vector Potential $\mathbf{A}$ |

**Step 3: Convert to Modern Vector Notation**

The divergence-free condition is written compactly as:

$$\nabla \cdot \mathbf{A} = 0$$

**Step 4: State the Physical Meaning in Modern English**

Maxwell explicitly imposes the divergence-free condition on the vector potential [1]. This is the first historical appearance of the **Coulomb gauge condition**:

$$\nabla \cdot \mathbf{A} = 0$$

*   **Mathematical Motivation:** The curl relation $\mathbf{B} = \nabla \times \mathbf{A}$ does not uniquely determine $\mathbf{A}$. Since $\nabla \times (\nabla \phi) = 0$ for any scalar function $\phi$, we can add the gradient of any scalar function to $\mathbf{A}$ without changing $\mathbf{B}$:
    $$\mathbf{A}' = \mathbf{A} + \nabla \phi \implies \nabla \times \mathbf{A}' = \nabla \times \mathbf{A} = \mathbf{B}$$
    To resolve this non-uniqueness, Maxwell imposes the Coulomb gauge $\nabla \cdot \mathbf{A} = 0$.
*   **Vector Poisson Equation:** Imposing the Coulomb gauge decouples the Cartesian components of $\mathbf{A}$ into independent Poisson equations.
    *   **EMU Units (Unrationalized):** $\nabla^2 \mathbf{A} = -4\pi \mu \mathbf{J} = -\frac{4\pi}{k}\mathbf{J}$ [2]
    *   **SI Units (Rationalized):** $\nabla^2 \mathbf{A} = -\mu_0 \mathbf{J}$
    This allows the components of $\mathbf{A}$ to be solved independently using standard scalar potential integration techniques.

---

#### Translation 5: The Canonical Momentum Interpretation

**Step 1: Maxwell's Original Component Equations**

Maxwell interprets the electro-tonic intensity $\mathbf{A}$ as a "momentum" or "tension" in the field. In modern physics, this interpretation is grounded in the Lagrangian formulation of a charged particle in an electromagnetic field [2].

**Step 2: Identify the Modern Physical Quantities**

| Maxwell's Symbol | Physical Quantity | Modern Symbol | Electrostatic Analog | Magnetostatic Analog |
| :--- | :--- | :--- | :--- | :--- |
| $\mathbf{A}$ | Vector potential | $\mathbf{A}$ | — | Field momentum |
| $m$ | Particle mass | $m$ | — | — |
| $q$ | Electric charge | $q$ | — | — |
| $\mathbf{u}$ | Particle velocity | $\mathbf{u}$ | — | Conductor/charge carrier velocity |

**Step 3: Convert to Modern Vector Notation**

The canonical momentum of a charged particle in an electromagnetic field is:

$$\mathbf{p} = m\mathbf{u} + q\mathbf{A}$$

**Step 4: State the Physical Meaning in Modern English**

The canonical momentum $\mathbf{p}$ of a charged particle in an electromagnetic field consists of two parts [2]:
1.  **Mechanical Momentum:** $m\mathbf{u}$ (the ordinary momentum of the particle).
2.  **Field Momentum:** $q\mathbf{A}$ (the potential momentum stored in the electromagnetic field).

*   **Physical Interpretation:** Maxwell's interpretation of $\mathbf{A}$ as "electromagnetic momentum" anticipates this modern formulation by nearly 60 years. The vector potential represents the momentum stored in the field, which can be exchanged with the mechanical momentum of charged particles during electromagnetic induction.
*   **Conservation of Canonical Momentum:** During electromagnetic induction, the canonical momentum of a charged particle is conserved:
    $$\frac{d\mathbf{p}}{dt} = \frac{d}{dt}(m\mathbf{u} + q\mathbf{A}) = q\left( \mathbf{E} + \mathbf{u} \times \mathbf{B} \right)$$
    This is the Lorentz force law, which Maxwell will derive in Part II, Section 3.

---

### Standardized Commentary Block

*   **The Goal:** Maxwell's objective in Part II, Section 1 is to introduce the electro-tonic state as a fundamental vector quantity representing the condition of the field at each point in space. This represents a conceptual leap beyond the scalar potential of Part I.
*   **The Method:** Maxwell defines the electro-tonic intensity $\mathbf{A}$ with components $(F, G, H)$. He then establishes the relationship between $\mathbf{A}$ and the magnetic induction $\mathbf{B}$ via the curl operation: $\mathbf{B} = \nabla \times \mathbf{A}$. He also introduces the Coulomb gauge condition $\nabla \cdot \mathbf{A} = 0$ to resolve the mathematical non-uniqueness of the curl relation.
*   **The Limitation:** While the vector potential $\mathbf{A}$ is a more powerful mathematical tool than the scalar potential, its physical interpretation remains somewhat abstract in Paper 1. The full physical significance of $\mathbf{A}$ as the canonical momentum of the field will not be fully realized until Paper 3 (1865) and, ultimately, the quantum mechanical Aharonov-Bohm effect (1959) [3].
*   **The Legacy:** The vector potential $\mathbf{A}$ introduced in Part II, Section 1 becomes one of the most important quantities in modern physics:
    *   **Classical Electrodynamics:** $\mathbf{A}$ is the canonical momentum conjugate to the position of a charged particle [2].
    *   **Quantum Mechanics:** $\mathbf{A}$ appears in the Schrödinger equation and is responsible for the Aharonov-Bohm effect [3].
    *   **Gauge Theory:** $\mathbf{A}$ is the fundamental field of gauge theories, including the Standard Model of particle physics.

---

### Exegesis Workflow Callout

Before proceeding to Phase 4 (Visualization), the reader must execute the **Post-Reading Reconciliation Protocol (Section 1.2.2)**:
1.  Verify that your customized glossary entries in Appendix A align with the dual-layered mappings derived in this section, particularly the definitions of the electro-tonic intensity $(F, G, H)$ and the vector potential $\mathbf{A}$.
2.  Audit your Cartesian-to-vector derivations against the **Zone 2 Quality Control Check (Section 1.2.1)** to ensure:
    *   The curl relation $\mathbf{B} = \nabla \times \mathbf{A}$ is correctly derived from Maxwell's component equations.
    *   The Coulomb gauge condition $\nabla \cdot \mathbf{A} = 0$ is recognized as Maxwell's explicit constraint.
    *   The circulation integral $\oint_C \mathbf{A} \cdot d\mathbf{l} = \Phi$ is correctly derived from Stokes' Theorem.
    *   The canonical momentum interpretation $\mathbf{p} = m\mathbf{u} + q\mathbf{A}$ is properly grounded.
3.  Confirm that the visualizations generated in Phase 4 accurately represent the vector potential $\mathbf{A}$ and its resulting curl field $\mathbf{B}$ for a current loop.

---

### Connections to Later Papers

| Concept in Paper 1 | Later Development |
| :--- | :--- |
| $\mathbf{A} = (F, G, H)$ (Electro-tonic intensity) | **Paper 3 (1865):** The vector potential becomes the canonical momentum in Maxwell's Lagrangian formulation of the electromagnetic field. |
| $\mathbf{B} = \nabla \times \mathbf{A}$ (Curl relation) | **Paper 2 (1861):** Retained as one of Maxwell's fundamental field equations in the molecular vortex model. |
| $\nabla \cdot \mathbf{A} = 0$ (Coulomb gauge) | **Paper 3 (1865):** Maintained in Maxwell's dynamical theory of the field. |
| $\oint_C \mathbf{A} \cdot d\mathbf{l} = \Phi$ (Circulation-flux relation) | **Paper 3 (1865):** Used to derive Faraday's law in integral form. |
| $\mathbf{p} = m\mathbf{u} + q\mathbf{A}$ (Canonical momentum) | **Paper 3 (1865):** Formalized in Maxwell's Lagrangian mechanics of the field. |

---

### References Integration Callout

#### The Treatise on Electricity and Magnetism (1873)

The following articles of Maxwell's *Treatise* (1873) provide direct commentary on the electro-tonic state:

| *Treatise* Article | Connection to Section 1 |
| :--- | :--- |
| **Articles 91–95** | Maxwell's discussion of the electro-tonic state and its physical interpretation [2]. |
| **Article 92** | The definition of the electro-tonic intensity $(F, G, H)$ as a vector quantity [2]. |
| **Article 93** | The relationship between the electro-tonic state and the magnetic induction [2]. |
| **Article 94** | The physical interpretation of the vector potential as "electromagnetic momentum" [2]. |
| **Article 95** | The introduction of the gauge condition $\nabla \cdot \mathbf{A} = 0$ [2]. |

#### Heaviside's Electromagnetic Theory (1893)

Heaviside's vector reformulations provide a modern perspective on the electro-tonic state:

| Heaviside Section | Connection to Section 1 |
| :--- | :--- |
| **Volume I, Chapter 8** | Heaviside's treatment of the vector potential in vector notation [3]. |
| **Volume II, Chapter 7** | Historical commentary on Maxwell's introduction of the electro-tonic state [3]. |
| **Volume III, Chapter 12** | The relationship between Maxwell's 1855 vector potential and the modern formulation [3]. |

#### Integration Instructions

During Phase 2 (Active Reading), the reader should:

1.  Identify the specific *Treatise* articles that correspond to the electro-tonic state in Section 1 and read them in parallel with the source text.
2.  Consult Heaviside's commentary to understand how the electro-tonic state was translated into vector notation and how it relates to the modern vector potential.
3.  Note the conceptual shift from the scalar potential of Part I to the vector potential of Part II and how this represents a fundamental advance in Maxwell's thinking.

---

### References

[1] Maxwell, J. C. (1858). *On Faraday's Lines of Force*. Transactions of the Cambridge Philosophical Society, Vol. X, Part I. *(Note: Read in two parts: Part I on Dec 10, 1855; Part II on Feb 11, 1856. Published in 1858.)*

[2] Maxwell, J. C. (1873). *A Treatise on Electricity and Magnetism*. Oxford: Clarendon Press.

[3] Heaviside, O. (1893). *Electromagnetic Theory*. London: The Electrician Printing and Publishing Company.

[4] Bork, A. M. (1966). Physics just before Einstein. *Science*, 152(3722), 597–603.

[5] Jackson, J. D. (1999). *Classical Electrodynamics*. John Wiley & Sons.