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

## Phase 3: Mathematical & Theoretical Formalization

### Translation Protocol (4 Steps)

The following protocol provides a systematic method for translating Maxwell's 1855 Cartesian component equations into modern vector notation. This protocol should be applied to each mathematical passage encountered during Phase 2.

---

**Step 1: Write Maxwell's Original Cartesian Component Equations**

Record Maxwell's component equations exactly as they appear in the 1855 text, preserving his notation and coordinate conventions.

**Step 2: Identify the Modern Physical Quantities**

Map Maxwell's 19th-century symbols to their modern vector equivalents, maintaining the dual-layered conduction and magnetostatic analogies.

| Maxwell's 1855 Symbol | Physical Quantity | Modern Symbol | Electrostatic Analog | Magnetostatic Analog |
| :--- | :--- | :--- | :--- | :--- |
| $u, v, w$ | Fluid velocity components | $\mathbf{v} = (u, v, w)$ | Current Density $\mathbf{J}$ | Magnetic Induction $\mathbf{B}$ |
| $p$ | Pressure potential | $p$ (scalar) | Electric Potential $\phi$ | Magnetic Potential $\Omega$ |
| $k$ | Resistance of the medium | $k$ (scalar) | Resistivity $1/\sigma$ | Reluctivity $1/\mu$ |
| $k\mathbf{v} = - \nabla p$ | Intensity vector | $k\mathbf{v}$ | Electric Field $\mathbf{E}$ | Magnetic Intensity $\mathbf{H}$ |
| $\Gamma$ | Circulation of velocity | $\Gamma$ | Current circulation | Flux circulation |
| $\boldsymbol{\omega} = \nabla \times \mathbf{v}$ | Vorticity of velocity field | $\boldsymbol{\omega}$ | — (zero in electrostatics) | Induction curl: $\nabla \times \mathbf{B}$ |
| $dx, dy, dz$ | Line element components | $d\mathbf{l} = (dx, dy, dz)$ | Line element $d\mathbf{l}$ | Line element $d\mathbf{l}$ |

**Step 3: Convert to Modern Vector Notation**

Rewrite the component equations as a single vector equation using the operators $\nabla$, $\cdot$, and $\times$.

**Step 4: State the Physical Meaning in Modern English**

Articulate the physical meaning of the translated equation in clear, modern language, with explicit acknowledgment of the dual-layered analogical framework and the distinction between velocity circulation and intensity circulation.

---

### Component-to-Vector Translation

#### Translation 1: Definition of Circulation

**Step 1: Maxwell's Original Component Equations**

In Part I, Section 3, Maxwell defines the circulation $\Gamma$ of the velocity field around a closed curve $C$ as the line integral [1]:

$$\Gamma = \oint_C (u \, dx + v \, dy + w \, dz)$$

**Step 2: Identify the Modern Physical Quantities**

| Maxwell's Symbol | Physical Quantity | Modern Symbol | Electrostatic Analog | Magnetostatic Analog |
| :--- | :--- | :--- | :--- | :--- |
| $u, v, w$ | Fluid velocity components | $\mathbf{v} = (u, v, w)$ | Current Density $\mathbf{J}$ | Magnetic Induction $\mathbf{B}$ |
| $dx, dy, dz$ | Line element components | $d\mathbf{l} = (dx, dy, dz)$ | Line element $d\mathbf{l}$ | Line element $d\mathbf{l}$ |
| $\Gamma$ | Velocity circulation | $\Gamma$ | Current circulation | Induction circulation |

**Step 3: Convert to Modern Vector Notation**

The circulation is written compactly as:

$$\Gamma = \oint_C \mathbf{v} \cdot d\mathbf{l}$$

**Step 4: State the Physical Meaning in Modern English**

The circulation $\Gamma$ of the velocity field around a closed curve $C$ is the line integral of the velocity vector along the curve. 
*   **Conduction Mapping:** Maps to the circulation of current density: $\oint_C \mathbf{J} \cdot d\mathbf{l}$ (which is zero in a steady conduction loop unless driven by a localized EMF pump singularity).
*   **Magnetostatic Mapping:** Maps to the circulation of the magnetic induction: $\oint_C \mathbf{B} \cdot d\mathbf{l}$.

**The Intensity Circulation Distinction:** The true analogue of **Magnetomotive Force (MMF)** is the line integral of the local *intensity* vector:
$$\text{MMF} = \oint_C \mathbf{H} \cdot d\mathbf{l} \leftrightarrow \oint_C (k\mathbf{v}) \cdot d\mathbf{l} = \oint_C (-\nabla p) \cdot d\mathbf{l}$$
In a uniform medium of unit resistance ($k=1$), velocity circulation and intensity circulation coincide. In non-uniform media ($k \neq \text{const}$), they diverge.

---

#### Translation 2: Stokes' Theorem and the Vorticity-Circulation Relation

**Step 1: Maxwell's Original Component Equations**

Maxwell applies Stokes' Theorem to relate the circulation around a closed curve to the flux of vorticity through any surface $S$ spanning the curve [1]:

$$\oint_C (u \, dx + v \, dy + w \, dz) = \iint_S \left[ \left( \frac{\partial w}{\partial y} - \frac{\partial v}{\partial z} \right) dy \, dz + \left( \frac{\partial u}{\partial z} - \frac{\partial w}{\partial x} \right) dz \, dx + \left( \frac{\partial v}{\partial x} - \frac{\partial u}{\partial y} \right) dx \, dy \right]$$

**Step 2: Identify the Modern Physical Quantities**

| Maxwell's Symbol | Physical Quantity | Modern Symbol | Electrostatic Analog | Magnetostatic Analog |
| :--- | :--- | :--- | :--- | :--- |
| $u, v, w$ | Fluid velocity components | $\mathbf{v} = (u, v, w)$ | Current Density $\mathbf{J}$ | Magnetic Induction $\mathbf{B}$ |
| $\frac{\partial w}{\partial y} - \dots$ | Vorticity components | $\boldsymbol{\omega} = \nabla \times \mathbf{v}$ | — | Induction curl: $\nabla \times \mathbf{B} = 4\pi\mu\mathbf{J}$ |
| $dy \, dz$, etc. | Area elements | $d\mathbf{S} = (dS_x, dS_y, dS_z)$ | Area element $d\mathbf{S}$ | Area element $d\mathbf{S}$ |

**Step 3: Convert to Modern Vector Notation**

Stokes' Theorem is written compactly as:

$$\oint_C \mathbf{v} \cdot d\mathbf{l} = \iint_S (\nabla \times \mathbf{v}) \cdot d\mathbf{S}$$

**Step 4: State the Physical Meaning in Modern English**

The circulation of the velocity field around any closed curve $C$ equals the total flux of the vorticity $\boldsymbol{\omega} = \nabla \times \mathbf{v}$ through any surface $S$ spanning the curve. 
*   **Magnetostatic Mapping:** This is the mathematical foundation of Ampère's Law for the induction field: the circulation of $\mathbf{B}$ around a closed loop equals the enclosed magnetic flux source $\iint_S (\nabla \times \mathbf{B}) \cdot d\mathbf{S} = 4\pi \iint_S \mu \mathbf{J} \cdot d\mathbf{S}$. The vorticity $\nabla \times \mathbf{v}$ is the local source of velocity circulation, analogous to the scaled current density $4\pi\mu\mathbf{J}$ in unrationalized magnetostatics.

---

#### Translation 3: Vorticity in a Non-Uniform Medium

**Step 1: Maxwell's Original Component Equations**

Taking the curl of the constitutive relation $\mathbf{v} = -\frac{1}{k}\nabla p$ in a medium with spatially varying resistance $k(\mathbf{r})$:

$$\nabla \times \mathbf{v} = \nabla \times \left( -\frac{1}{k} \nabla p \right)$$

In component form, this expands to:

$$\frac{\partial w}{\partial y} - \frac{\partial v}{\partial z} = \frac{1}{k^2} \left( \frac{\partial k}{\partial y} \frac{\partial p}{\partial z} - \frac{\partial k}{\partial z} \frac{\partial p}{\partial y} \right)$$

with analogous expressions for the other components.

**Step 2: Identify the Modern Physical Quantities**

| Maxwell's Symbol | Physical Quantity | Modern Symbol | Electrostatic Analog | Magnetostatic Analog |
| :--- | :--- | :--- | :--- | :--- |
| $\mathbf{v}$ | Fluid velocity | $\mathbf{v}$ | Current Density $\mathbf{J}$ | Magnetic Induction $\mathbf{B}$ |
| $p$ | Pressure potential | $p$ | Potential $\phi$ | Potential $\Omega$ |
| $k$ | Resistance of the medium | $k$ | Resistivity $1/\sigma$ | Reluctivity $1/\mu$ |

**Step 3: Convert to Modern Vector Notation**

Using the vector identity $\nabla \times (f \nabla g) = \nabla f \times \nabla g$ for a scalar function $f$, we obtain:

$$\nabla \times \mathbf{v} = \frac{1}{k^2} \nabla k \times \nabla p$$

**Step 4: State the Physical Meaning in Modern English**

In a non-uniform medium, vorticity is generated whenever the gradient of the medium's resistance $\nabla k$ is not parallel to the potential gradient $\nabla p$ [1]. 
*   **Magnetostatic Mapping:** Since resistance $k$ maps to reluctivity $1/\mu$, a spatial variation in $k$ represents a spatial variation in magnetic permeability ($\nabla \mu \neq 0$). The non-zero curl $\nabla \times \mathbf{v}$ generated at the interface between different media represents the **bound surface currents** (magnetization currents) that arise at boundaries where magnetic properties change abruptly.

---

#### Translation 4: The Singular Vortex Filament (Infinite Straight Wire)

**Step 1: Maxwell's Original Component Equations**

For a line vortex of circulation strength $\Gamma$ aligned along the $z$-axis, the velocity field in cylindrical coordinates $(\rho, \phi, z)$ is [1]:

$$v_\rho = 0, \quad v_\phi = \frac{\Gamma}{2\pi\rho}, \quad v_z = 0$$

In Cartesian components:

$$u = -\frac{\Gamma}{2\pi} \frac{y}{x^2 + y^2}, \quad v = \frac{\Gamma}{2\pi} \frac{x}{x^2 + y^2}, \quad w = 0$$

**Step 2: Identify the Modern Physical Quantities**

| Maxwell's Symbol | Physical Quantity | Modern Symbol | Electrostatic Analog | Magnetostatic Analog |
| :--- | :--- | :--- | :--- | :--- |
| $\Gamma$ | Circulation strength | $\Gamma$ | — | $\mu I$ (enclosed current) |
| $\rho$ | Radial distance from axis | $\rho = \sqrt{x^2 + y^2}$ | Radial distance | Radial distance |

**Step 3: Convert to Modern Vector Notation**

The velocity field is written compactly as:
$$\mathbf{v} = \frac{\Gamma}{2\pi\rho} \hat{\boldsymbol{\phi}}$$
The vorticity is concentrated at the singular core:
$$\nabla \times \mathbf{v} = \Gamma \delta(\boldsymbol{\rho}) \hat{\mathbf{z}}$$
where $\delta(\boldsymbol{\rho})$ is the 2D Dirac delta function in the $xy$-plane.

**Step 4: State the Physical Meaning in Modern English**

A vortex filament is a singular line source of circulation. The flow is irrotational everywhere except at the filament itself ($\rho = 0$), where the vorticity is concentrated in a Dirac delta distribution. 
*   **Magnetostatic Mapping:** This is the exact mathematical structure of the magnetic induction field surrounding an infinite straight wire carrying a current $I$:
    $$\mathbf{B} = \frac{\mu I}{2\pi\rho} \hat{\boldsymbol{\phi}} \implies \nabla \times \mathbf{B} = \mu I \delta(\boldsymbol{\rho}) \hat{\mathbf{z}}$$
    The circulation of $\mathbf{B}$ around any path enclosing the wire equals $\mu$ times the enclosed current.

---

#### Translation 5: Theorem I (Hydrodynamic Circulation Theorem)

**Step 1: Maxwell's Original Component Equations**

Maxwell's Theorem I states that the circulation of the intensity vector around any closed curve equals the total flux of the curl of the intensity vector through any surface spanning the curve [1]:

$$\oint_C (k u \, dx + k v \, dy + k w \, dz) = \iint_S \left[ \left( \frac{\partial (k w)}{\partial y} - \frac{\partial (k v)}{\partial z} \right) dy \, dz + \cdots \right]$$

**Step 2: Identify the Modern Physical Quantities**

| Maxwell's Symbol | Physical Quantity | Modern Symbol | Electrostatic Analog | Magnetostatic Analog |
| :--- | :--- | :--- | :--- | :--- |
| $k u, k v, k w$ | Intensity vector components | $k\mathbf{v} = -\nabla p$ | Electric Field $\mathbf{E}$ | Magnetic Intensity $\mathbf{H}$ |
| $\nabla \times (k\mathbf{v})$ | Curl of intensity | $\nabla \times (k\mathbf{v})$ | — | Current Density $4\pi \mathbf{J}$ |

**Step 3: Convert to Modern Vector Notation**

Theorem I is written compactly as:
$$\oint_C (k\mathbf{v}) \cdot d\mathbf{l} = \iint_S (\nabla \times (k\mathbf{v})) \cdot d\mathbf{S}$$

**Step 4: State the Physical Meaning in Modern English**

**Theorem I (Hydrodynamic Circulation Theorem):** The circulation of the intensity vector $k\mathbf{v}$ around any closed curve $C$ equals the total flux of its curl through any surface $S$ spanning the curve.
*   **Magnetostatic Mapping:** Since $k\mathbf{v} \leftrightarrow \mathbf{H}$ (Magnetic Intensity) and $\nabla \times (k\mathbf{v}) \leftrightarrow 4\pi \mathbf{J}$ (Current Density), Theorem I translates directly into the integral form of **Ampère's Law**:
    $$\oint_C \mathbf{H} \cdot d\mathbf{l} = 4\pi \iint_S \mathbf{J} \cdot d\mathbf{S} = 4\pi I_{\text{enc}} \quad \text{(unrationalized units)}$$
    This is a purely mathematical *Theorem* of the fluid model, distinct from the physical *Laws* of induction in Part II.

---

### Standardized Commentary Block

- **The Goal:** Maxwell's objective in Section 3 is to establish the mathematical relationship between the circulation of the velocity field around a closed curve and the vorticity (curl) of the field through any surface spanning the curve. This provides the mathematical foundation for Ampère's Law within the fluid analogy.

- **The Method:** Maxwell defines the circulation as the line integral of velocity around a closed curve ($\Gamma = \oint_C \mathbf{v} \cdot d\mathbf{l}$). Applying Stokes' Theorem, he relates this circulation to the flux of vorticity ($\nabla \times \mathbf{v}$) through any spanning surface. He then derives the vorticity in a non-uniform medium ($\nabla \times \mathbf{v} = \frac{1}{k^2} \nabla k \times \nabla p$) and the singular representation of a vortex filament. The result is Theorem I: the circulation of the intensity vector equals the flux of its curl.

- **The Limitation:** Section 3 is restricted to **steady-state, time-independent** hydrodynamic circulation. It does not address time-varying fields or electromagnetic induction. The "vortex filaments" are mathematical constructs, not physical models of the ether.

- **The Legacy:** Theorem I is the direct precursor to Ampère's Law in its integral form. The concept of circulation and vorticity provided the mathematical language for describing the rotational properties of vector fields, which would become essential in the full electromagnetic theory.

---

### Exegesis Workflow Callout

Before proceeding to Phase 4 (Visualization), the reader must execute the **Post-Reading Reconciliation Protocol (Section 1.2.2)**:
1.  Verify that your customized glossary entries in Appendix A align with the dual-layered mappings derived in this section, particularly the distinction between velocity circulation ($\oint_C \mathbf{v} \cdot d\mathbf{l}$) and intensity circulation ($\oint_C (k\mathbf{v}) \cdot d\mathbf{l}$).
2.  Audit your Cartesian-to-vector derivations against the **Zone 2 Quality Control Check (Section 1.2.1)** to ensure:
    *   The distinction between mathematical Theorems (Part I) and physical Laws (Part II) is maintained.
    *   The non-uniform vorticity expression $\nabla \times \mathbf{v} = \frac{1}{k^2} \nabla k \times \nabla p$ is correctly derived.
    *   The singular representation of the vortex filament uses the Dirac delta function correctly.

---

### Connections to Later Papers

| Concept in Paper 1 | Later Development |
| :--- | :--- |
| Theorem I: $\oint_C (k\mathbf{v}) \cdot d\mathbf{l} = \iint_S (\nabla \times (k\mathbf{v})) \cdot d\mathbf{S}$ | **Paper 3 (1865):** This becomes Ampère's Law in integral form: $\oint_C \mathbf{H} \cdot d\mathbf{l} = I_{\text{enc}}$ (rationalized). |
| $\nabla \times \mathbf{v} = \frac{1}{k^2} \nabla k \times \nabla p$ | **Paper 2 (1861):** The refraction of lines of force at boundaries is re-interpreted in the molecular vortex model. |
| Vortex filament $\mathbf{v} = \frac{\Gamma}{2\pi\rho} \hat{\boldsymbol{\phi}}$ | **Paper 2 (1861):** Replaced by rotating molecular vortices of Paper 2 which provide a physical mechanism for field circulation. |
| $\nabla \times \mathbf{v} = \Gamma \delta(\boldsymbol{\rho}) \hat{\mathbf{z}}$ | **Paper 3 (1865):** This becomes the local form of Ampère's Law: $\nabla \times \mathbf{H} = \mathbf{J}$. |

---

### References Integration Callout

#### The Treatise on Electricity and Magnetism (1873)

The following articles of Maxwell's *Treatise* (1873) provide direct commentary on the circulation theorems of Section 3:

| *Treatise* Article | Connection to Section 3 |
| :--- | :--- |
| **Articles 76–80** | Maxwell's discussion of circulation and the application of Stokes' Theorem to vector fields [2]. |
| **Article 77** | The definition of circulation and its relation to the curl of the field [2]. |
| **Article 79** | The application of circulation theorems to magnetic fields and currents [2]. |
| **Article 80** | The distinction between irrotational and rotational fields [2]. |

#### Heaviside's Electromagnetic Theory (1893)

Heaviside's vector reformulations provide a modern perspective on the circulation theorems of Section 3:

| Heaviside Section | Connection to Section 3 |
| :--- | :--- |
| **Volume I, Chapter 4** | Heaviside's treatment of curl, circulation, and Stokes' Theorem in vector notation [3]. |
| **Volume II, Chapter 7** | Historical commentary on Maxwell's use of circulation in the fluid analogy [3]. |
| **Volume III, Chapter 12** | The relationship between Maxwell's 1855 circulation theorem and Ampère's Law [3]. |


---

### References

[1] Bork, A. M. (1966). Physics just before Einstein. *Science*, 152(3722), 597–603.

[2] Schey, H. M. (2005). *Div, Grad, Curl, and All That: An Informal Text on Vector Calculus*. W. W. Norton & Company.

[3] Maxwell, J. C. (1858). *On Faraday's Lines of Force*. Transactions of the Cambridge Philosophical Society, Vol. X, Part I. *(Note: Read in two parts: Part I on Dec 10, 1855; Part II on Feb 11, 1856. Published in 1858.)*

[4] Maxwell, J. C. (1873). *A Treatise on Electricity and Magnetism*. Oxford: Clarendon Press.

[5] Heaviside, O. (1893). *Electromagnetic Theory*. London: The Electrician Printing and Publishing Company.

