# Part I, Section 3: Hydrodynamic Circulation (Theorems)

## Phase 1: Preparatory Foundations

### Objectives and Checklist

By the end of this section, the reader will:

- [ ] Understand the definition of **circulation** as the line integral of velocity around a closed curve: $\Gamma = \oint_C \mathbf{v} \cdot d\mathbf{l}$.
- [ ] Recognize the physical interpretation of intensity circulation $\oint_C (k\mathbf{v}) \cdot d\mathbf{l}$ as the total work done (per unit volume) against resistance along a closed path.
- [ ] Derive the relationship between velocity circulation and **vorticity** ($\nabla \times \mathbf{v}$) via Stokes' Theorem: $\Gamma = \iint_S (\nabla \times \mathbf{v}) \cdot d\mathbf{S}$.
- [ ] Understand how a non-zero curl of velocity is generated either by **singularities** (vortex filaments) or by **spatial gradients in the medium's resistance** ($\nabla k \times \nabla p$).
- [ ] Understand **Theorem I (Ampère's Law analogue):** The circulation of intensity around any closed curve equals the total flux of vorticity through any surface spanning the curve.
- [ ] Map the circulation theorem to its electrostatic and magnetostatic analogues, noting the role of vorticity as the analogue of current density.
- [ ] Distinguish clearly between the **hydrodynamic theorems** of Part I (static, mathematical analogies) and the **electromagnetic laws** of Part II (dynamic, induction laws).

---

### Terminology Mapping: Circulation, Vortex Filaments, and the Curl

In Section 3, Maxwell introduces the concept of circulation within the fluid model and relates it to the local rotation of the fluid. The following table maps the fluid concepts to their electromagnetic analogues, maintaining the corrected intensity-quantity mappings from Sections 1 and 2:

| Fluid Concept | Symbol / Operator | Mathematical Definition | Electrostatic Analog | Magnetostatic Analog |
| :--- | :--- | :--- | :--- | :--- |
| **Velocity Circulation** | $\Gamma_{\mathbf{v}}$ | $\oint_C \mathbf{v} \cdot d\mathbf{l}$ | Kinematic circulation | Magnetic flux circulation |
| **Intensity Circulation (Work)** | $\Gamma_{\text{intensity}}$ | $\oint_C (k\mathbf{v}) \cdot d\mathbf{l} = \oint_C (-\nabla p) \cdot d\mathbf{l}$ | Electromotive force (EMF) around a closed circuit (requires a battery/pump singularity) | Magnetomotive force (MMF): $\oint_C \mathbf{H} \cdot d\mathbf{l}$ |
| **Vorticity (Vortices)** | $\boldsymbol{\omega}$ | $\nabla \times \mathbf{v}$ | — (zero in irrotational electrostatics) | Current Density $\mathbf{J}$ (via Ampère's Law) |
| **Flux of Vorticity** | — | $\iint_S \boldsymbol{\omega} \cdot d\mathbf{S}$ | — | Total current enclosed $I_{\text{enc}}$ |
| **Theorem I (Integral Form)** | — | $\oint_C (k\mathbf{v}) \cdot d\mathbf{l} = \iint_S (\nabla \times (k\mathbf{v})) \cdot d\mathbf{S}$ | — | Ampère's Law: $\oint_C \mathbf{H} \cdot d\mathbf{l} = I_{\text{enc}}$ |
| **Theorem I (Local Form)** | — | $\nabla \times (k\mathbf{v}) = \mathbf{J}$ (representing source) | — | Ampère's Law (local): $\nabla \times \mathbf{H} = \mathbf{J}$ |

**Critical Distinction:** In the resistive fluid model, the velocity field $\mathbf{v} = -\frac{1}{k} \nabla p$ is driven by the potential gradient. The curl of a gradient is identically zero:

$$\nabla \times (\nabla p) = 0$$

This implies that **in a simply connected region with a uniform resistive medium ($k = \text{const}$), the circulation around any closed curve is identically zero.** This is the hydrodynamic analogue of the electrostatic field being conservative.

However, Maxwell introduces non-zero circulation into his model via two distinct physical mechanisms:
1.  **Spatial Variations in Resistance:** If the medium's resistance is non-uniform ($\nabla k \neq 0$), a non-zero curl of velocity is generated: $\nabla \times \mathbf{v} = \frac{1}{k^2} \nabla k \times \nabla p$. This represents the refraction and shear of lines of force across boundaries.
2.  **Singularities (Vortex Filaments):** Localized lines in space where the potential $p$ becomes multi-valued (so $\oint dp \neq 0$). These singularities correspond directly to **electric currents**, which act as the sources of the magnetic field.

---

### Mathematical Note: Circulation, Vorticity, and Theorem I

#### 1. Definition of Circulation and Physical Work

For a closed curve $C$ in the fluid, the **circulation of velocity** is the line integral:

$$\Gamma_{\mathbf{v}} = \oint_C \mathbf{v} \cdot d\mathbf{l}$$

In the resistive fluid model, the actual force per unit volume driving the fluid against resistance is the intensity vector $\mathbf{F} = -\nabla p = k\mathbf{v}$. The **total work done per unit volume** against the medium's resistance along a closed path is the line integral of this intensity vector:

$$\Gamma_{\text{work}} = \oint_C (k\mathbf{v}) \cdot d\mathbf{l} = \oint_C (-\nabla p) \cdot d\mathbf{l}$$

If the potential $p$ is a single-valued, continuous function, the integral of its gradient around any closed path is zero:

$$\oint_C (-\nabla p) \cdot d\mathbf{l} = -\oint_C dp = 0$$

The flow is **irrotational**. Non-zero circulation only arises if we introduce active sources of work (such as localized fluid pumps in electrostatics) or singular regions where the potential becomes multi-valued (such as vortex filaments in magnetostatics).

#### 2. The Two Sources of Vorticity

Applying Stokes' Theorem, the circulation around a closed curve is equal to the flux of the curl of the field through any surface $S$ spanning the curve:

$$\oint_C \mathbf{v} \cdot d\mathbf{l} = \iint_S (\nabla \times \mathbf{v}) \cdot d\mathbf{S}$$

The vector field $\boldsymbol{\omega} = \nabla \times \mathbf{v}$ represents the **vorticity** (local angular rotation) of the fluid. Taking the curl of the constitutive relation $\mathbf{v} = -\frac{1}{k}\nabla p$ reveals how vorticity is generated:

$$\nabla \times \mathbf{v} = \nabla \times \left(-\frac{1}{k}\nabla p\right) = -\nabla\left(\frac{1}{k}\right) \times \nabla p - \frac{1}{k}\nabla \times (\nabla p)$$

$$\nabla \times \mathbf{v} = \frac{1}{k^2} \nabla k \times \nabla p$$

This vector identity reveals that **vorticity is generated whenever the gradient of the medium's resistance ($\nabla k$) is not parallel to the pressure gradient ($\nabla p$)** [1]. This is the mathematical foundation Maxwell uses to represent the refraction of lines of force at boundaries between different materials.

#### 3. The Singular Mathematics of a Vortex Filament

To represent a localized electric current in a uniform medium ($k = \text{const}$), Maxwell introduces the concept of a **vortex filament**—an infinitely thin singular line along which the fluid is in rotational motion. 

Consider an idealized line vortex of circulation strength $\Gamma$ aligned along the $z$-axis. In cylindrical coordinates $(\rho, \phi, z)$, the velocity field is:

$$\mathbf{v} = \frac{\Gamma}{2\pi \rho} \hat{\boldsymbol{\phi}}$$

Taking the curl of this velocity field for any region excluding the $z$-axis ($\rho > 0$) yields:

$$\nabla \times \mathbf{v} = \left[ \frac{1}{\rho} \frac{\partial}{\partial \rho} \left(\rho v_{\phi}\right) \right] \hat{\mathbf{z}} = \left[ \frac{1}{\rho} \frac{\partial}{\partial \rho} \left(\frac{\Gamma}{2\pi}\right) \right] \hat{\mathbf{z}} = 0$$

The flow is irrotational everywhere except at the origin $\rho = 0$. Integrating the velocity along a closed circular path of radius $R$ enclosing the origin yields:

$$\oint_C \mathbf{v} \cdot d\mathbf{l} = \int_{0}^{2\pi} \left(\frac{\Gamma}{2\pi R}\right) R \, d\phi = \Gamma$$

Applying Stokes' Theorem, we represent the vorticity distribution at the singular core using the 2D Dirac delta function $\delta(\boldsymbol{\rho})$:

$$\boldsymbol{\omega} = \nabla \times \mathbf{v} = \Gamma \delta(\boldsymbol{\rho}) \hat{\mathbf{z}}$$

This is the exact mathematical structure of the magnetic field surrounding an infinite straight wire carrying a current $I$ [2]:

$$\mathbf{B} = \frac{\mu I}{2\pi \rho} \hat{\boldsymbol{\phi}} \implies \nabla \times \mathbf{B} = \mu I \delta(\boldsymbol{\rho}) \hat{\mathbf{z}}$$

#### 4. Theorem I (Hydrodynamic Circulation Theorem)

**Theorem I:** The circulation of the intensity vector $k\mathbf{v}$ around any closed curve is equal to the total flux of the curl of the intensity vector through any surface spanning the curve:

$$\oint_C (k\mathbf{v}) \cdot d\mathbf{l} = \iint_S (\nabla \times (k\mathbf{v})) \cdot d\mathbf{S}$$

In the magnetostatic analogue, where $k\mathbf{v} \leftrightarrow \mathbf{H}$ (Magnetic Intensity) and the local source of circulation is the current density $\nabla \times \mathbf{H} = \mathbf{J}$, Theorem I translates directly into the integral form of **Ampère's Law**:

$$\oint_C \mathbf{H} \cdot d\mathbf{l} = \iint_S \mathbf{J} \cdot d\mathbf{S} = I_{\text{enc}}$$

---

### Pre-Reading Checklist for Phase 2

Before proceeding to the active reading of Maxwell's text on circulation and Theorem I, the reader should confirm:

- [ ] The definition of circulation $\Gamma = \oint_C \mathbf{v} \cdot d\mathbf{l}$ is clearly understood.
- [ ] The distinction between velocity circulation and intensity circulation ($\oint_C (k\mathbf{v}) \cdot d\mathbf{l}$) is internalized.
- [ ] The mathematical generation of vorticity due to non-uniform media ($\nabla \times \mathbf{v} = \frac{1}{k^2} \nabla k \times \nabla p$) is recognized.
- [ ] The singular field representation of a vortex filament ($\mathbf{v} = \frac{\Gamma}{2\pi \rho} \hat{\boldsymbol{\phi}}$) is understood as the direct analogue of an infinite straight current-carrying wire.
- [ ] The distinction between **Theorems** (hydrodynamic, Part I) and **Laws** (electromagnetic, Part II) is clear.

---

### Connection to the Rest of the Exegesis

*   **Phase 2 (Active Reading):** The reader will encounter Maxwell's derivation of Theorem I, his discussion of vortex filaments, and his geometric interpretation of circulation. The terminology mapping above will guide the translation of his 19th-century language.
*   **Phase 3 (Mathematical Formalization):** After reading, the reader will formalize the circulation theorem in vector notation, derive the local form $\nabla \times \mathbf{v} = \boldsymbol{\omega}$, and explicitly map it to Ampère's Law.
*   **Phase 4 (Computational Visualization):** The reader will generate vector field visualizations of a current-carrying wire, showing the circulation of $\mathbf{B}$ around the wire. Animations will demonstrate the relationship between current direction and the direction of circulation (right-hand rule).

---

### References

[1] Bork, A. M. (1966). Physics just before Einstein. *Science*, 152(3722), 597–603.

[2] Schey, H. M. (2005). *Div, Grad, Curl, and All That: An Informal Text on Vector Calculus*. W. W. Norton & Company.