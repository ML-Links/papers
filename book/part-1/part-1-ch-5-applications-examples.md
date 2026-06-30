# Part I, Section 5: Applications and Examples

## Phase 1: Preparatory Foundations

### Objectives and Checklist

By the end of this section, the reader will:

- [ ] Derive the velocity field of an infinite straight vortex filament and map it to the magnetic field of an infinite straight current-carrying wire.
- [ ] Understand why the pressure potential $p(\phi)$ surrounding a line current is a **multi-valued helical function** of angle, providing the geometric foundation for multi-valued scalar potentials in magnetostatics.
- [ ] Derive the linear pressure gradient and field distribution along the axis of a solenoid, mapping the fluid flow to the magnetic field of a uniformly wound coil.
- [ ] Calculate the shielded force between two localized magnetic poles in a resistive medium using the virtual energy density framework.
- [ ] Recognize the **fundamental limitations** of the fluid analogy (no time dependence, no displacement current, scalar potential only) and appreciate how they motivate the transition to the vector potential ($\mathbf{A}$) in Part II.

---

### Terminology Mapping: Applications to Specific Geometries

The following table maps the fluid concepts to their electromagnetic analogues for the specific applications in this section:

| Application | Fluid Configuration | Fluid Result | Electromagnetic Analog |
| :--- | :--- | :--- | :--- |
| **Infinite Straight Wire** | Vortex filament of strength $\Gamma$ along $z$-axis | $\mathbf{v} = \frac{\Gamma}{2\pi\rho} \hat{\boldsymbol{\phi}}$ | Magnetic field of infinite wire: $\mathbf{B} = \frac{\mu I}{2\pi\rho} \hat{\boldsymbol{\phi}}$ |
| **Solenoid** | Uniform distribution of vortex filaments over a cylindrical surface | $\mathbf{v} = v_0 \hat{\mathbf{z}}$ (interior), $\mathbf{v} = 0$ (exterior) | Magnetic field along solenoid axis: $\mathbf{B} = \mu n I \hat{\mathbf{z}}$ |
| **Forces Between Magnetic Poles** | Two point sources/sinks in a resistive medium | Force scaled by reluctivity: $\mathbf{F} = -k \frac{m_1 m_2}{r^2} \hat{\mathbf{r}}$ | Force between shielded poles: $\mathbf{F} = \frac{1}{\mu} \frac{m_1 m_2}{r^2} \hat{\mathbf{r}}$ |

**Critical Note on the Vortex Filament:** In the fluid model, the vortex filament is a **mathematical singularity**—an infinitely thin line around which the fluid circulates. The flow is irrotational everywhere except at the filament itself, where the vorticity is concentrated in a Dirac delta distribution. This is the exact analogue of an infinite straight wire carrying a steady current.

**Critical Note on the Solenoid:** Maxwell models the solenoid as a cylindrical surface covered with a uniform distribution of vortex filaments (or, equivalently, a surface current). The superposition of their individual velocity fields produces a uniform flow inside the solenoid and zero flow outside—the exact analogue of the magnetic field inside a long solenoid.

---

### Mathematical Note: Derivation of Fields for Canonical Geometries

#### 1. Infinite Straight Wire (Vortex Filament)

Consider an ideal line vortex of circulation strength $\Gamma$ aligned along the $z$-axis. In cylindrical coordinates $(\rho, \phi, z)$, the velocity field is:

$$\mathbf{v} = \frac{\Gamma}{2\pi\rho} \hat{\boldsymbol{\phi}}$$

The flow is incompressible ($\nabla \cdot \mathbf{v} = 0$) and irrotational ($\nabla \times \mathbf{v} = 0$) everywhere outside the singular core ($\rho > 0$).

**Pressure Potential Distribution:** The pressure potential for this flow is obtained by integrating Darcy's Law:

$$\nabla p = -k\mathbf{v} \implies \frac{\partial p}{\partial \rho} \hat{\boldsymbol{\rho}} + \frac{1}{\rho}\frac{\partial p}{\partial \phi} \hat{\boldsymbol{\phi}} + \frac{\partial p}{\partial z} \hat{\mathbf{z}} = -k \left(\frac{\Gamma}{2\pi\rho}\right) \hat{\boldsymbol{\phi}}$$

Equating the vector components yields:

$$\frac{\partial p}{\partial \rho} = 0, \quad \frac{\partial p}{\partial z} = 0, \quad \frac{\partial p}{\partial \phi} = -k \frac{\Gamma}{2\pi}$$

Integrating with respect to the angular coordinate $\phi$ gives:

$$p(\phi) = -k \frac{\Gamma}{2\pi} \phi + p_0$$

**The Multi-Valued Potential:** This result reveals a critical physical property: the pressure potential $p(\phi)$ is a **multi-valued helical function** of position [1]. If a fluid element circulates once around the wire, the pressure drops by a discrete unit:

$$\Delta p = -k\Gamma$$

This is the exact mathematical analogue of the **magnetic scalar potential ($\Omega$)** surrounding a current-carrying wire. Because the loop encloses a current, the line integral of the gradient is non-zero, requiring $\Omega$ to be multi-valued ($\oint \nabla \Omega \cdot d\mathbf{l} = -I_{\text{enc}}$).

#### 2. Solenoid (Uniform Surface Distribution of Vortex Filaments)

Consider a cylindrical surface of radius $R$ and infinite length, covered with a uniform distribution of vortex filaments carrying a surface density of circulation $\gamma = \Gamma / (2\pi R)$ along the $z$-axis.

**Velocity Field:** By symmetry, the velocity field is uniform and axial in the interior, and zero in the exterior:

$$\mathbf{v}_{\text{inside}} = v_0 \hat{\mathbf{z}} \quad \text{and} \quad \mathbf{v}_{\text{outside}} = 0$$

Applying Stokes' Theorem to a loop spanning the surface yields $v_0 = \gamma$.

**Pressure Potential Distribution:** 
*   **Interior Potential:** Because the fluid is flowing through a resistive medium of uniform resistance $k$, the uniform velocity $\mathbf{v} = \gamma \hat{\mathbf{z}}$ requires a driving force. Thus, the interior pressure potential must **decrease linearly** along the solenoid axis:
    $$\frac{\partial p}{\partial z} = -k v_0 \implies p_{\text{inside}}(z) = -k \gamma z + p_0$$
*   **Exterior Potential:** Since the fluid is at rest in the exterior region ($\mathbf{v} = 0$), the exterior pressure potential remains constant:
    $$p_{\text{outside}} = \text{constant}$$

This demonstrates that a pressure gradient is necessary to maintain flow against resistance, even when the flow is uniform.

#### 3. Shielded Forces Between Two Localized Magnetic Poles

Consider two point sources in a resistive medium $k$ (where $k = 1/\mu$). Each source generates a pressure potential scaled by the medium's resistance [2]:

$$p_i(\mathbf{r}) = -\frac{k m_i}{|\mathbf{r} - \mathbf{r}_i|}$$

where $m_i$ represents the source strength (analogous to magnetic pole strength). The combined pressure field is the superposition $p(\mathbf{r}) = p_1(\mathbf{r}) + p_2(\mathbf{r})$.

The total virtual energy density of this field is $U = \frac{1}{2k}|\nabla p|^2$. Integrating the interaction term of this energy density over all space yields the interaction energy:

$$\mathcal{W}_{\text{interaction}} = -k \frac{4\pi m_1 m_2}{|\mathbf{r}_1 - \mathbf{r}_2|}$$

Taking the gradient of this interaction energy with respect to $\mathbf{r}_1$ yields the shielded mechanical force between the poles:

$$\mathbf{F}_{12} = -\nabla_1 \mathcal{W}_{\text{interaction}} = -k \, \frac{4\pi m_1 m_2}{|\mathbf{r}_1 - \mathbf{r}_2|^2} \hat{\mathbf{r}}_{12}$$

**Mapping to Magnetostatics:** Mapping $k \to 1/\mu$ and converting to unrationalized units:

$$\mathbf{F}_{12} = -\frac{1}{\mu} \frac{m_1 m_2}{|\mathbf{r}_1 - \mathbf{r}_2|^2} \hat{\mathbf{r}}_{12}$$

This is the physically correct Coulomb's Law for magnetic poles. The force is **inversely proportional to the permeability $\mu$** (directly proportional to reluctivity $k$), reflecting the shielding effect of the medium.

---

### Limitations of the Fluid Analogy Exposed by These Applications

While Part I successfully models static field configurations, these applications expose the fundamental limits of the fluid analogy:

1.  **No Time Dependence:** The fluid model is strictly steady-state. It cannot describe time-varying fields, electromagnetic induction, or wave propagation.
2.  **No Displacement Current:** The equation of continuity $\nabla \cdot \mathbf{v} = 0$ strictly enforces incompressibility. There is no mechanism for current accumulation or displacement in a dielectric.
3.  **Scalar Potential Restrictions:** The fluid model is driven by a scalar pressure potential $p$. It cannot represent vector fields with intrinsic directionality, such as the vector potential $\mathbf{A}$.

**These limitations are the driving force behind Part II.** Maxwell recognizes that the fluid analogy must be superseded by a more general mathematical framework—the vector potential and the electro-tonic state—to account for the dynamic phenomena of electromagnetism.

---

### Pre-Reading Checklist for Phase 2

Before proceeding to the active reading of Maxwell's applications and examples, the reader should confirm:

- [ ] The derivation of the multi-valued helical pressure potential $p(\phi)$ for a vortex filament is understood.
- [ ] The linear potential gradient $p(z)$ required to maintain uniform flow inside a solenoid is recognized.
- [ ] The derivation of the shielded Coulomb's Law ($\mathbf{F}_{12} \propto k$) from the virtual interaction energy is understood.
- [ ] The limitations of the fluid analogy (no time dependence, no displacement current, scalar potential only) are recognized.
- [ ] The transition to Part II is anticipated: the need for a vector potential to describe dynamical induction.

---

### Connection to the Rest of the Exegesis

*   **Phase 2 (Active Reading):** The reader will encounter Maxwell's specific applications, including the infinite wire, the solenoid, and the forces between poles. The terminology mapping above will guide the translation of his 19th-century language.
*   **Phase 3 (Mathematical Formalization):** After reading, the reader will formalize these derivations in vector notation, explicitly mapping each fluid result to its electromagnetic counterpart.
*   **Phase 4 (Computational Visualization):** The reader will generate 3D vector field plots of the infinite wire, the solenoid, and the force between poles, visualizing the field configurations and pressure distributions.

---

### References

[1] Bork, A. M. (1966). Physics just before Einstein. *Science*, 152(3722), 597–603.

[2] Jackson, J. D. (1999). *Classical Electrodynamics*. John Wiley & Sons.