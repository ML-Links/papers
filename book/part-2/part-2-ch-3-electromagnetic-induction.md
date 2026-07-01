# Part II, Section 3: Electromagnetic Induction

## Phase 1: Preparatory Foundations

### Objectives and Checklist

By the end of this section, the reader will:

- [ ] Understand Maxwell's 1855 derivation of the total induced electric field, including both the local transformer EMF and the motional EMF: $\mathbf{E} = \mathbf{u} \times \mathbf{B} - \frac{\partial \mathbf{A}}{\partial t} - \nabla \Psi$.
- [ ] Recognize the distinction between the **electrostatic potential** $\Psi$ (conservative), the **transformer EMF** $-\partial \mathbf{A}/\partial t$ (local, time-varying), and the **motional EMF** $\mathbf{u} \times \mathbf{B}$ (convective).
- [ ] Derive Faraday's law in integral form: $\oint \mathbf{E} \cdot d\mathbf{l} = -\frac{d\Phi}{dt}$, accounting for both stationary and moving circuits.
- [ ] Rigorously derive the Lorentz force law from the canonical momentum framework ($\mathbf{p} = m\mathbf{u} + q\mathbf{A}$), validating the interpretation of $\mathbf{A}$ as field momentum.

---

### Terminology Mapping: Electromagnetic Induction and the Electro-tonic State

In Part II, Section 3, Maxwell derives the equations of electromagnetic induction from the time-rate of change of the electro-tonic state. The following table maps the 19th-century terminology to modern vector calculus:

| 19th-Century Term | Maxwell's Symbol | Modern Vector Equivalent | Physical Interpretation |
| :--- | :--- | :--- | :--- |
| **Electro-tonic Intensity** | $F, G, H$ | $\mathbf{A} = (A_x, A_y, A_z)$ | The vector potential field (time-dependent) |
| **Motional Coordinates** | $\frac{dx}{dt}, \frac{dy}{dt}, \frac{dz}{dt}$ | $\mathbf{u} = (u_x, u_y, u_z)$ | The physical velocity of the conductor/charge |
| **Electrostatic Potential** | $\Psi$ (or $\psi$) | $\Psi$ (or scalar $\phi$) | The conservative electric potential |
| **Motional EMF** | $c\frac{dy}{dt} - b\frac{dz}{dt}$, etc. | $\mathbf{u} \times \mathbf{B}$ | The convective, velocity-dependent part of the electric field |
| **Transformer EMF** | $-\frac{dF}{dt}$, etc. | $-\frac{\partial \mathbf{A}}{\partial t}$ | The local, time-varying part of the electric field |
| **Total Electric Field** | $P, Q, R$ (components) | $\mathbf{E} = \mathbf{u} \times \mathbf{B} - \frac{\partial \mathbf{A}}{\partial t} - \nabla \Psi$ | The complete electric field vector acting on a charge |
| **Faraday's Law (Local)** | — | $\nabla \times \mathbf{E} = -\frac{\partial \mathbf{B}}{\partial t}$ | The curl of the electric field equals the negative time-rate of change of the magnetic induction |

**Critical Distinction:** The total electric field $\mathbf{E}$ acting on a moving charge in Maxwell’s 1855 formulation consists of **three distinct physical contributions** [1]:
$$\mathbf{E} = \underbrace{\mathbf{u} \times \mathbf{B}}_{\text{Motional EMF}} - \underbrace{\frac{\partial \mathbf{A}}{\partial t}}_{\text{Transformer EMF}} - \underbrace{\nabla \Psi}_{\text{Electrostatic EMF}}$$
1.  **Motional EMF ($\mathbf{u} \times \mathbf{B}$):** A convective contribution arising from the physical motion of the conductor through a magnetic induction field.
2.  **Transformer EMF ($-\partial \mathbf{A}/\partial t$):** A local, non-conservative contribution arising from the time-variation of the vector potential.
3.  **Electrostatic EMF ($-\nabla \Psi$):** A conservative contribution arising from static charge distributions.

---

### Mathematical Note: Derivation of the Induction and Force Equations

#### 1. Derivation of the Motional and Transformer EMF

The total magnetic flux $\Phi$ linking a closed loop $C$ is the surface integral of the magnetic induction $\mathbf{B}$ over any spanning surface $S$. Using the curl relation $\mathbf{B} = \nabla \times \mathbf{A}$, Stokes' Theorem allows us to write the flux as a circulation:

$$\Phi = \iint_S \mathbf{B} \cdot d\mathbf{S} = \oint_C \mathbf{A} \cdot d\mathbf{l}$$

If the circuit moves with velocity $\mathbf{u}$ and the magnetic field simultaneously varies over time, the total time rate of change of the flux linking the circuit is given by the Helmholtz transport theorem [2]:

$$\frac{d\Phi}{dt} = \iint_S \frac{\partial \mathbf{B}}{\partial t} \cdot d\mathbf{S} + \oint_C (\mathbf{B} \times \mathbf{u}) \cdot d\mathbf{l}$$

Using the vector identity $(\mathbf{B} \times \mathbf{u}) \cdot d\mathbf{l} = -(\mathbf{u} \times \mathbf{B}) \cdot d\mathbf{l}$ and substituting $\mathbf{B} = \nabla \times \mathbf{A}$ into the first term yields:

$$\frac{d\Phi}{dt} = \oint_C \frac{\partial \mathbf{A}}{\partial t} \cdot d\mathbf{l} - \oint_C (\mathbf{u} \times \mathbf{B}) \cdot d\mathbf{l} = \oint_C \left( \frac{\partial \mathbf{A}}{\partial t} - \mathbf{u} \times \mathbf{B} \right) \cdot d\mathbf{l}$$

According to Faraday's experimental law of induction, the electromotive force (EMF) induced in the loop is equal to the negative rate of change of this flux:

$$\text{EMF} = \oint_C \mathbf{E} \cdot d\mathbf{l} = -\frac{d\Phi}{dt} = \oint_C \left( \mathbf{u} \times \mathbf{B} - \frac{\partial \mathbf{A}}{\partial t} \right) \cdot d\mathbf{l}$$

This line integral relation must hold for any arbitrary loop, which implies the local relationship for the induced field:

$$\mathbf{E}_{\text{induced}} = \mathbf{u} \times \mathbf{B} - \frac{\partial \mathbf{A}}{\partial t}$$

Adding the conservative electrostatic potential contribution ($-\nabla \Psi$) yields Maxwell's complete 1855 equation of induction:

$$\mathbf{E} = \mathbf{u} \times \mathbf{B} - \frac{\partial \mathbf{A}}{\partial t} - \nabla \Psi$$

#### 2. Rigorous Derivation of the Lorentz Force from Canonical Momentum

To prove that the vector potential $\mathbf{A}$ represents a physical "field momentum," we evaluate the equations of motion for a particle of mass $m$ and charge $q$ moving with velocity $\mathbf{u}$. The canonical momentum of the particle-field system is [2]:

$$\mathbf{p} = m\mathbf{u} + q\mathbf{A}$$

The Hamiltonian $H$ of the charged particle is formulated as:

$$H = \frac{1}{2m}(\mathbf{p} - q\mathbf{A})^2 + q\Psi$$

According to Hamilton's equations of motion, the time derivative of the canonical momentum is the negative spatial gradient of the Hamiltonian:

$$\frac{d\mathbf{p}}{dt} = -\nabla H = -\nabla \left[ \frac{1}{2m}(\mathbf{p} - q\mathbf{A})^2 \right] - q\nabla \Psi$$

Since the particle's mechanical velocity is $\mathbf{u} = \frac{1}{m}(\mathbf{p} - q\mathbf{A})$, this simplifies to:

$$\frac{d\mathbf{p}}{dt} = q\nabla(\mathbf{u} \cdot \mathbf{A}) - q\nabla \Psi$$

Using the vector identity $\nabla(\mathbf{u} \cdot \mathbf{A}) = (\mathbf{u} \cdot \nabla)\mathbf{A} + \mathbf{u} \times (\nabla \times \mathbf{A})$ (where $\mathbf{u}$ is treated as constant with respect to the spatial gradient operator at a given instant), and substituting $\nabla \times \mathbf{A} = \mathbf{B}$:

$$\frac{d\mathbf{p}}{dt} = q(\mathbf{u} \cdot \nabla)\mathbf{A} + q(\mathbf{u} \times \mathbf{B}) - q\nabla \Psi$$

Now, we evaluate the total time derivative of the canonical momentum definition:

$$\frac{d\mathbf{p}}{dt} = \frac{d}{dt}(m\mathbf{u} + q\mathbf{A}) = \frac{d(m\mathbf{u})}{dt} + q\frac{d\mathbf{A}}{dt}$$

Because $\mathbf{A}(\mathbf{r}(t), t)$ is a function of both position and time, its total time derivative along the particle's trajectory is convective:

$$\frac{d\mathbf{A}}{dt} = \frac{\partial \mathbf{A}}{\partial t} + (\mathbf{u} \cdot \nabla)\mathbf{A}$$

Equating our two expressions for $\frac{d\mathbf{p}}{dt}$ yields:

$$\frac{d(m\mathbf{u})}{dt} + q\frac{\partial \mathbf{A}}{\partial t} + q(\mathbf{u} \cdot \nabla)\mathbf{A} = q(\mathbf{u} \cdot \nabla)\mathbf{A} + q(\mathbf{u} \times \mathbf{B}) - q\nabla \Psi$$

The convective terms $q(\mathbf{u} \cdot \nabla)\mathbf{A}$ on both sides cancel out. Rearranging the remaining terms yields:

$$\frac{d(m\mathbf{u})}{dt} = q\left( -\frac{\partial \mathbf{A}}{\partial t} - \nabla \Psi \right) + q(\mathbf{u} \times \mathbf{B})$$

Substituting the definition of the local electric field $\mathbf{E} = -\frac{\partial \mathbf{A}}{\partial t} - \nabla \Psi$ results in the complete **Lorentz Force Law** [2]:

$$\mathbf{F} = \frac{d(m\mathbf{u})}{dt} = q(\mathbf{E} + \mathbf{u} \times \mathbf{B})$$

This derivation proves that the mechanical force acting on a charged particle is a direct consequence of the conservation of canonical momentum. It confirms that the convective acceleration is driven by momentum exchange with the field potential momentum $q\mathbf{A}$ [2].

---

### Connections to Later Papers

| Concept in Paper 1 | Later Development |
| :--- | :--- |
| $\mathbf{E} = \mathbf{u} \times \mathbf{B} - \partial \mathbf{A}/\partial t - \nabla \Psi$ | **Paper 2 (1861):** This complete induction equation is retained and derived using rotating molecular vortices. |
| $\nabla \times \mathbf{E} = -\partial \mathbf{B}/\partial t$ | **Paper 3 (1865):** This becomes one of the fundamental field equations in his self-contained dynamical theory. |
| Motional and Local EMF | **Paper 2 (1861):** The local transformer EMF is completed by introducing the displacement current $\partial \mathbf{D}/\partial t$ to describe dielectric polarization. |
| Canonical Momentum $\mathbf{p} = m\mathbf{u} + q\mathbf{A}$ | **Paper 3 (1865):** The vector potential is formally defined as "electromagnetic momentum" in his Lagrangian field mechanics. |

---

### Pre-Reading Checklist for Phase 2

Before proceeding to the active reading of Maxwell's derivation of electromagnetic induction, the reader should confirm:

- [ ] The distinction between the electrostatic potential $\Psi$, the transformer EMF $-\partial \mathbf{A}/\partial t$, and the motional EMF $\mathbf{u} \times \mathbf{B}$ is understood.
- [ ] The derivation of Faraday's law in integral form $\oint \mathbf{E} \cdot d\mathbf{l} = -d\Phi/dt$ accounting for moving loops is recognized.
- [ ] The cancellation of convective terms in the canonical momentum derivation ($\mathbf{p} = m\mathbf{u} + q\mathbf{A}$) is understood.
- [ ] The local form $\nabla \times \mathbf{E} = -\partial \mathbf{B}/\partial t$ is recognized.

---

### Connection to the Rest of the Exegesis

*   **Phase 2 (Active Reading):** The reader will encounter Maxwell's derivation of the induction equations, his discussion of the electro-tonic state, and his interpretation of the induced electric field. The terminology mapping above will guide the translation of his 19th-century language.
*   **Phase 3 (Mathematical Formalization):** After reading, the reader will formalize the induction equations in vector notation, derive Faraday's law in both integral and local forms, and discuss the physical interpretation of the vector potential.
*   **Phase 4 (Computational Visualization):** The reader will generate dynamic animations showing a changing magnetic field inducing an electric field in a neighboring loop, visualizing the relationship between $\mathbf{A}$, $\mathbf{B}$, and $\mathbf{E}$.

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
| $P, Q, R$ | Electric field components | $\mathbf{E} = (E_x, E_y, E_z)$ | Electric Field $\mathbf{E}$ | Electric Field $\mathbf{E}$ |
| $\Psi$ | Electrostatic potential | $\Psi$ | Electric Potential $\phi$ | Electric Potential $\phi$ |
| $\frac{dx}{dt}, \frac{dy}{dt}, \frac{dz}{dt}$ | Velocity components of conductor | $\mathbf{u} = (u_x, u_y, u_z)$ | Conductor velocity | Conductor velocity |

> **Notational Warning:** The symbol $\mathbf{u}$ represents the physical velocity of the conductor or charge carrier. This is distinct from the fluid velocity $\mathbf{v}$ used in Part I, which maps to magnetic induction $\mathbf{B}$. Additionally, the letter $H$ serves a dual role as both the $z$-component of $\mathbf{A}$ and the vector symbol for Magnetic Intensity $\mathbf{H}$.

**Step 3: Convert to Modern Vector Notation**

Rewrite the component equations as a single vector equation using the operators $\nabla$, $\cdot$, and $\times$.

**Step 4: State the Physical Meaning in Modern English**

Articulate the physical meaning of the translated equation in clear, modern language, with explicit acknowledgment of the dual-layered analogical framework and the distinction between motional and transformer EMF.

---

### Component-to-Vector Translation

#### Translation 1: The Complete Induction Equation

**Step 1: Maxwell's Original Component Equations**

Maxwell formulates the complete law of electromagnetic induction for a conductor moving with velocity components $(\frac{dx}{dt}, \frac{dy}{dt}, \frac{dz}{dt})$ as [1]:

$$P = c\frac{dy}{dt} - b\frac{dz}{dt} - \frac{dF}{dt} - \frac{d\Psi}{dx}$$
$$Q = a\frac{dz}{dt} - c\frac{dx}{dt} - \frac{dG}{dt} - \frac{d\Psi}{dy}$$
$$R = b\frac{dx}{dt} - a\frac{dy}{dt} - \frac{dH}{dt} - \frac{d\Psi}{dz}$$

**Step 2: Identify the Modern Physical Quantities**

| Maxwell's 1855 Symbol | Physical Quantity | Modern Symbol | Electrostatic Analog | Magnetostatic Analog |
| :--- | :--- | :--- | :--- | :--- |
| $P, Q, R$ | Electric field components | $\mathbf{E} = (E_x, E_y, E_z)$ | Electric Field $\mathbf{E}$ | Electric Field $\mathbf{E}$ |
| $a, b, c$ | Magnetic induction components | $\mathbf{B} = (B_x, B_y, B_z)$ | — | Magnetic Induction $\mathbf{B}$ |
| $F, G, H$ | Electro-tonic intensity components | $\mathbf{A} = (A_x, A_y, A_z)$ | — | Vector Potential $\mathbf{A}$ |
| $\frac{dx}{dt}, \frac{dy}{dt}, \frac{dz}{dt}$ | Conductor velocity components | $\mathbf{u} = (u_x, u_y, u_z)$ | Conductor velocity | Conductor velocity |
| $\Psi$ | Electrostatic potential | $\Psi$ | Electric Potential $\phi$ | Electric Potential $\phi$ |

> **Notational Warning:** Note that the letter "H" represents both the scalar $z$-component of the vector potential $\mathbf{A} = (F, G, H)$ and the vector field symbol for Magnetic Intensity $\mathbf{H} = (\alpha, \beta, \gamma)$.

**Step 3: Convert to Modern Vector Notation**

The three component equations combine into a single vector expression:

$$\mathbf{E} = \mathbf{u} \times \mathbf{B} - \frac{\partial \mathbf{A}}{\partial t} - \nabla \Psi$$

**Step 4: State the Physical Meaning in Modern English**

The total electric field $\mathbf{E}$ acting within a conductor moving through a magnetic field consists of three mathematically distinct physical contributions [1].
*   **Motional EMF ($\mathbf{u} \times \mathbf{B}$):** A convective term arising from the physical translation of the conductor across magnetic lines of force. This represents the Lorentz velocity-dependent term.
*   **Transformer EMF ($-\frac{\partial \mathbf{A}}{\partial t}$):** A local, non-conservative electric field induced by the time-varying electro-tonic state (vector potential). This is the field-representation of Faraday's dynamic induction.
*   **Electrostatic EMF ($-\nabla \Psi$):** A conservative electric field produced by static spatial charge distributions.

---

#### Translation 2: Faraday's Law in Integral Form

**Step 1: Maxwell's Original Component Equations**

By taking the line integral of the components $(P, Q, R)$ around a closed spatial curve $C$, Maxwell relates the net electromotive force to the changing electro-tonic state [1]:

$$\oint_C (P \, dx + Q \, dy + R \, dz) = -\frac{d}{dt} \oint_C (F \, dx + G \, dy + H \, dz)$$

**Step 2: Identify the Modern Physical Quantities**

| Maxwell's 1855 Symbol | Physical Quantity | Modern Symbol | Electrostatic Analog | Magnetostatic Analog |
| :--- | :--- | :--- | :--- | :--- |
| $P, Q, R$ | Electric field components | $\mathbf{E} = (E_x, E_y, E_z)$ | Electric Field $\mathbf{E}$ | Electric Field $\mathbf{E}$ |
| $F, G, H$ | Electro-tonic intensity components | $\mathbf{A} = (A_x, A_y, A_z)$ | — | Vector Potential $\mathbf{A}$ |
| $dx, dy, dz$ | Curve element components | $d\mathbf{l} = (dx, dy, dz)$ | Line element $d\mathbf{l}$ | Line element $d\mathbf{l}$ |

**Step 3: Convert to Modern Vector Notation**

Applying Stokes' Theorem to translate the line integrals into surface integrals:

$$\oint_C \mathbf{E} \cdot d\mathbf{l} = -\frac{d}{dt} \oint_C \mathbf{A} \cdot d\mathbf{l} = -\frac{d}{dt} \iint_S \mathbf{B} \cdot d\mathbf{S} = -\frac{d\Phi}{dt}$$

**Step 4: State the Physical Meaning in Modern English**

The total induced electromotive force (EMF) around a closed loop $C$ is equal to the negative time rate of change of the magnetic flux $\Phi$ passing through any surface $S$ bounded by that loop [1].
*   **Lenz's Law Integration:** The negative sign represents the directional requirement known as Lenz's Law, indicating that the induced current generates its own magnetic field to oppose the flux change.
*   **Unified Formulation:** This integral representation unifies the physical actions of both a temporally varying field (transformer effect) and a spatially moving loop (motional effect) into the total time derivative $\frac{d\Phi}{dt}$.

---

#### Translation 3: Faraday's Law in Local (Differential) Form

**Step 1: Maxwell's Original Component Equations**

For stationary circuits ($\mathbf{u} = 0$), the spatial derivatives of the electric field components are balanced by the temporal rate of change of the magnetic induction components [1]:

$$\frac{\partial R}{\partial y} - \frac{\partial Q}{\partial z} = -\frac{\partial a}{\partial t}$$
$$\frac{\partial P}{\partial z} - \frac{\partial R}{\partial x} = -\frac{\partial b}{\partial t}$$
$$\frac{\partial Q}{\partial x} - \frac{\partial P}{\partial y} = -\frac{\partial c}{\partial t}$$

**Step 2: Identify the Modern Physical Quantities**

| Maxwell's 1855 Symbol | Physical Quantity | Modern Symbol | Electrostatic Analog | Magnetostatic Analog |
| :--- | :--- | :--- | :--- | :--- |
| $P, Q, R$ | Electric field components | $\mathbf{E} = (E_x, E_y, E_z)$ | Electric Field $\mathbf{E}$ | Electric Field $\mathbf{E}$ |
| $a, b, c$ | Magnetic induction components | $\mathbf{B} = (B_x, B_y, B_z)$ | — | Magnetic Induction $\mathbf{B}$ |

**Step 3: Convert to Modern Vector Notation**

Combining the curl equations into a single vector differential relation:

$$\nabla \times \mathbf{E} = -\frac{\partial \mathbf{B}}{\partial t}$$

**Step 4: State the Physical Meaning in Modern English**

A time-varying magnetic induction field generates a non-conservative, rotational electric field in the surrounding space [2].
*   **Field Topology:** Unlike static electric fields which are irrotational ($\nabla \times \mathbf{E}_s = 0$) and originate from charges, the induced electric field has closed, circulating field lines wrapping around the changing magnetic flux.
*   **Maxwell's Equations:** This is one of the four core Maxwell's equations. It demonstrates that temporal variations in one field link directly to spatial variations in the other, establishing the foundational coupling of classical electromagnetism.

---

#### Translation 4: The Rigorous Lorentz Force from Canonical Momentum

**Step 1: Maxwell's Original Component Equations**

Maxwell treats the electro-tonic state $(F, G, H)$ as a form of physical momentum. In the modern Lagrangian framework, the mechanical force acting on a charged particle is derived directly from the canonical momentum [2]:

$$\mathbf{p} = m\mathbf{u} + q\mathbf{A}$$

**Step 2: Identify the Modern Physical Quantities**

| Maxwell's 1855 Symbol | Physical Quantity | Modern Symbol | Electrostatic Analog | Magnetostatic Analog |
| :--- | :--- | :--- | :--- | :--- |
| $\mathbf{A}$ | Electro-tonic intensity | $\mathbf{A}$ | — | Vector Potential $\mathbf{A}$ |
| $m$ | Particle mass | $m$ | — | — |
| $q$ | Electric charge | $q$ | Charge | Charge |
| $\mathbf{u}$ | Particle velocity | $\mathbf{u}$ | — | Conductor velocity |
| $\Psi$ | Electrostatic potential | $\Psi$ | Electric Potential $\phi$ | Electric Potential $\phi$ |

**Step 3: Convert to Modern Vector Notation**

Defining the Hamiltonian of the charged particle:
$$H = \frac{1}{2m}(\mathbf{p} - q\mathbf{A})^2 + q\Psi$$

Applying Hamilton's equations $\frac{d\mathbf{p}}{dt} = -\nabla H$ yields:
$$\frac{d\mathbf{p}}{dt} = q\nabla(\mathbf{u} \cdot \mathbf{A}) - q\nabla \Psi$$

Applying the vector identity $\nabla(\mathbf{u} \cdot \mathbf{A}) = (\mathbf{u} \cdot \nabla)\mathbf{A} + \mathbf{u} \times (\nabla \times \mathbf{A})$:
$$\frac{d\mathbf{p}}{dt} = q(\mathbf{u} \cdot \nabla)\mathbf{A} + q(\mathbf{u} \times \mathbf{B}) - q\nabla \Psi$$

Because the particle is moving, the total time derivative of $\mathbf{A}$ along its trajectory is:
$$\frac{d\mathbf{A}}{dt} = \frac{\partial \mathbf{A}}{\partial t} + (\mathbf{u} \cdot \nabla)\mathbf{A}$$

Differentiating the canonical momentum definition $\frac{d\mathbf{p}}{dt} = \frac{d(m\mathbf{u})}{dt} + q\frac{d\mathbf{A}}{dt}$ and substituting these expressions:
$$\frac{d(m\mathbf{u})}{dt} + q\left[\frac{\partial \mathbf{A}}{\partial t} + (\mathbf{u} \cdot \nabla)\mathbf{A}\right] = q(\mathbf{u} \cdot \nabla)\mathbf{A} + q(\mathbf{u} \times \mathbf{B}) - q\nabla \Psi$$

The convective terms $q(\mathbf{u} \cdot \nabla)\mathbf{A}$ on both sides cancel out, leaving:
$$\frac{d(m\mathbf{u})}{dt} = q\left(-\frac{\partial \mathbf{A}}{\partial t} - \nabla \Psi\right) + q(\mathbf{u} \times \mathbf{B})$$

Substituting the definition of the electric field $\mathbf{E} = -\frac{\partial \mathbf{A}}{\partial t} - \nabla \Psi$ yields the Lorentz Force:
$$\mathbf{F} = \frac{d(m\mathbf{u})}{dt} = q(\mathbf{E} + \mathbf{u} \times \mathbf{B})$$

**Step 4: State the Physical Meaning in Modern English**

The Lorentz force law is the mechanical expression of the conservation of canonical momentum between a charged particle and the electromagnetic field [2].
*   **Momentum Exchange:** The total canonical momentum $\mathbf{p}$ is conserved in the absence of external gradients. Changes in the mechanical momentum $m\mathbf{u}$ of the charge carrier are balanced by reciprocal changes in the field momentum $q\mathbf{A}$ during the process of induction.
*   **Validation of Analogy:** This derivation mathematically validates Maxwell's intuitive 1855 conceptualization of the electro-tonic state as an "electromagnetic momentum."

---

#### Translation 5: The Decomposition of Motional and Transformer EMF

**Step 1: Maxwell's Original Component Equations**

Maxwell expresses the total electromotive force induced in a circuit using the convective transport of the magnetic induction field [1]:

$$\text{EMF}_{\text{total}} = \oint_C \mathbf{E} \cdot d\mathbf{l} = -\frac{d}{dt} \iint_S (a \, dy \, dz + b \, dz \, dx + c \, dx \, dy)$$

**Step 2: Identify the Modern Physical Quantities**

| Maxwell's 1855 Symbol | Physical Quantity | Modern Symbol | Electrostatic Analog | Magnetostatic Analog |
| :--- | :--- | :--- | :--- | :--- |
| $a, b, c$ | Magnetic induction components | $\mathbf{B} = (B_x, B_y, B_z)$ | — | Magnetic Induction $\mathbf{B}$ |
| $\mathbf{E}$ | Induced electric field | $\mathbf{E}$ | Electric Field $\mathbf{E}$ | Electric Field $\mathbf{E}$ |
| $\mathbf{u}$ | Conductor velocity | $\mathbf{u}$ | — | Conductor velocity |

**Step 3: Convert to Modern Vector Notation**

Applying the Helmholtz transport theorem (or Leibniz rule for moving surfaces) to the total time derivative of magnetic flux:

$$\text{EMF}_{\text{total}} = \oint_C \mathbf{E} \cdot d\mathbf{l} = \oint_C (\mathbf{u} \times \mathbf{B}) \cdot d\mathbf{l} - \iint_S \frac{\partial \mathbf{B}}{\partial t} \cdot d\mathbf{S}$$

**Step 4: State the Physical Meaning in Modern English**

The net electromotive force generated within a dynamic circuit is the sum of two distinct induction mechanisms [2].
*   **Motional Contribution:** $\oint_C (\mathbf{u} \times \mathbf{B}) \cdot d\mathbf{l}$ arises from the physical velocity of the boundary relative to the magnetic field.
*   **Transformer Contribution:** $-\iint_S \frac{\partial \mathbf{B}}{\partial t} \cdot d\mathbf{S}$ arises from the time rate of change of the field itself inside the boundary.
*   **Relativity:** The equivalence of these two terms under coordinate transformations is a cornerstone of classical electrodynamics and was a key historical driver in the development of Einstein's Special Theory of Relativity.

---

### Standardized Commentary Block

*   **The Goal:** Maxwell's objective in Part II, Section 3 is to establish a unified mathematical framework for electromagnetic induction that accounts for both stationary induction (changing fields) and motional induction (moving conductors).
*   **The Method:** He introduces time-dependence into the electro-tonic components $(F, G, H)$ and constructs the complete induction equation. By integrating this around a loop, he derives the flux-induction relation, demonstrating how changes in the electro-tonic state relate directly to mechanical force.
*   **The Limitation:** Although the equations successfully describe induction, they lack the displacement current term ($\frac{\partial \mathbf{D}}{\partial t}$). Consequently, the system is mathematically incomplete for time-varying fields outside of closed conductors, and cannot describe electromagnetic wave propagation. This missing term is added later in Paper 2 (1861).
*   **The Legacy:** The local expression $\nabla \times \mathbf{E} = -\frac{\partial \mathbf{B}}{\partial t}$ remains unchanged as one of the four fundamental Maxwell's equations. His identification of the vector potential $\mathbf{A}$ as a field momentum is now standard in classical mechanics, quantum electrodynamics, and modern gauge theories.

---

### Exegesis Workflow Callout

#### Zone 2 Quality Control Verification
Prior to beginning active analysis of Section 3, the reader must verify that:
- [ ] The complete induction equation $\mathbf{E} = \mathbf{u} \times \mathbf{B} - \frac{\partial \mathbf{A}}{\partial t} - \nabla \Psi$ is correctly constructed from Maxwell's component equations.
- [ ] The velocity vector $\mathbf{u}$ is explicitly identified as the physical velocity of the conductor, distinguishing it from the fluid velocity $\mathbf{v}$ used in Part I.
- [ ] The derivation of the Lorentz force from the canonical momentum $m\mathbf{u} + q\mathbf{A}$ shows the cancelation of the convective term $(\mathbf{u} \cdot \nabla)\mathbf{A}$.
- [ ] The chronological placement of this section is correctly identified (Paper 1 introduces time-varying fields, but Paper 2 introduces the displacement current).

#### Post-Reading Reconciliation & Status Lock
Upon completing the active analysis and Phase 4 visualization:
- [ ] Reconcile the derived induction equations with the visual models of motional and transformer EMF.
- [ ] Verify that the visualization shows the spatial curl of $\mathbf{E}$ wrapping around the changing flux of $\mathbf{B}$.
- [ ] Confirm that the canonical momentum exchange is accurately mapped.
- [ ] Update the YAML metadata at the top of the section to `status: complete`.

---

### Connections to Later Papers

| Concept in Paper 1 | Later Development |
| :--- | :--- |
| $\mathbf{E} = \mathbf{u} \times \mathbf{B} - \frac{\partial \mathbf{A}}{\partial t} - \nabla \Psi$ | **Paper 2 (1861):** Interpreted physically in terms of the stresses and linear momentum of rotating molecular vortices. |
| $\nabla \times \mathbf{E} = -\frac{\partial \mathbf{B}}{\partial t}$ | **Paper 3 (1865):** Stated as "Equation B" of the seven fundamental field equations in *A Dynamical Theory of the Electromagnetic Field*. |
| $\mathbf{p} = m\mathbf{u} + q\mathbf{A}$ (Canonical Momentum) | **Paper 3 (1865):** Used to construct the Lagrangian of the electromagnetic field, cementing the vector potential as field momentum. |
| Absence of Displacement Current | **Paper 2 (1861):** The term $\frac{\partial \mathbf{D}}{\partial t}$ is added to satisfy the conservation of charge in dielectric media. |

---

### References Integration Callout

#### The Treatise on Electricity and Magnetism (1873)

The following articles of Maxwell's *Treatise* provide direct commentary on electromagnetic induction:

| *Treatise* Article | Connection to Section 3 |
| :--- | :--- |
| **Article 541** | The experimental basis of Faraday's induction discoveries [2]. |
| **Article 598** | Re-derivation of the complete induction equation using Lagrangian mechanics [2]. |
| **Article 599** | The physical and mechanical interpretation of the electrostatic potential term $\Psi$ under dynamic induction [2]. |

#### Heaviside's Electromagnetic Theory (1893)

Heaviside's vector reformulations provide a modern perspective on the induction equations:

| Heaviside Section | Connection to Section 3 |
| :--- | :--- |
| **Volume I, Section 45** | The representation of Faraday's Law in local form without using the vector potential [3]. |
| **Volume I, Section 47** | Analysis of motional EMF using the convective vector term $\nabla \times (\mathbf{u} \times \mathbf{B})$ [3]. |

#### Integration Instructions

During Phase 2 (Active Reading), the reader should:
1. Compare Maxwell's Cartesian formulation of motional EMF in Section 3 with his Lagrangian re-derivation in Article 598 of the *Treatise*.
2. Note how Heaviside’s vector notation in Section 45 avoids the use of $(F, G, H)$ while maintaining identical physical predictions for closed circuits.

---

### References

[1] Maxwell, J. C. (1858). *On Faraday's Lines of Force*. Transactions of the Cambridge Philosophical Society, Vol. X, Part I. *(Read in two parts: Part I on Dec 10, 1855; Part II on Feb 11, 1856. Published in 1858.)*

[2] Maxwell, J. C. (1873). *A Treatise on Electricity and Magnetism*. Oxford: Clarendon Press.

[3] Heaviside, O. (1893). *Electromagnetic Theory*. London: The Electrician Printing and Publishing Company.

[4] Jackson, J. D. (1999). *Classical Electrodynamics*. John Wiley & Sons.

[5] Bork, A. M. (1966). Physics just before Einstein. *Science*, 152(3722), 597–603.

[6] Jackson, J. D. (1999). *Classical Electrodynamics*. John Wiley & Sons.