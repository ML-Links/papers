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

### References

[1] Bork, A. M. (1966). Physics just before Einstein. *Science*, 152(3722), 597–603.

[2] Jackson, J. D. (1999). *Classical Electrodynamics*. John Wiley & Sons.