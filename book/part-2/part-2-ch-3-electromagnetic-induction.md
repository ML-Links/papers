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

### References

[1] Bork, A. M. (1966). Physics just before Einstein. *Science*, 152(3722), 597–603.

[2] Jackson, J. D. (1999). *Classical Electrodynamics*. John Wiley & Sons.