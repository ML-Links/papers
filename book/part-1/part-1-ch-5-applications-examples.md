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
| $u, v, w$ | Fluid velocity components | $\mathbf{v} = (u, v, w)$ | Current Density $\mathbf{J}$ | Magnetic Induction $\mathbf{B}$ |
| $p$ | Pressure potential | $p$ (scalar) | Electric Potential $\phi$ | Magnetic Potential $\Omega$ |
| $k$ | Resistance of the medium | $k$ (scalar) | Resistivity $1/\sigma$ | Reluctivity $1/\mu$ |
| $\Gamma$ | Circulation strength | $\Gamma$ | — | $\mu I$ (enclosed current) |
| $\rho$ | Radial distance | $\rho = \sqrt{x^2 + y^2}$ | Radial distance | Radial distance |
| $\phi$ | Angular coordinate | $\phi = \tan^{-1}(y/x)$ | Angular coordinate | Angular coordinate |

**Step 3: Convert to Modern Vector Notation**

Rewrite the component equations as a single vector equation using the operators $\nabla$, $\cdot$, and $\times$.

**Step 4: State the Physical Meaning in Modern English**

Articulate the physical meaning of the translated equation in clear, modern language, with explicit acknowledgment of the dual-layered analogical framework and the limitations exposed by these applications.

---

### Component-to-Vector Translation

#### Translation 1: Infinite Straight Wire (Vortex Filament)

**Step 1: Maxwell's Original Component Equations**

For a line vortex of circulation strength $\Gamma$ aligned along the $z$-axis, the velocity field in Cartesian components is [1]:

$$u = -\frac{\Gamma}{2\pi} \frac{y}{x^2 + y^2}, \quad v = \frac{\Gamma}{2\pi} \frac{x}{x^2 + y^2}, \quad w = 0$$

**Step 2: Identify the Modern Physical Quantities**

| Maxwell's Symbol | Physical Quantity | Modern Symbol | Electrostatic Analog | Magnetostatic Analog |
| :--- | :--- | :--- | :--- | :--- |
| $u, v, w$ | Fluid velocity components | $\mathbf{v} = (u, v, w)$ | — | Magnetic Induction $\mathbf{B}$ |
| $\Gamma$ | Circulation strength | $\Gamma$ | — | $\mu I$ (enclosed current) |

**Step 3: Convert to Modern Vector Notation**

In cylindrical coordinates $(\rho, \phi, z)$, the velocity field is written compactly as:

$$\mathbf{v} = \frac{\Gamma}{2\pi\rho} \hat{\boldsymbol{\phi}}$$

The pressure potential corresponding to this flow is obtained by integrating Darcy's Law ($d p = -k v_{\phi} \rho \, d\phi$):

$$p(\phi) = -k\frac{\Gamma}{2\pi}\phi + p_0$$

**Step 4: State the Physical Meaning in Modern English**

The velocity field of a line vortex decreases inversely with the radial distance from the filament. The flow is purely azimuthal (circulating around the filament) with no radial or axial components.
*   **Magnetostatic Mapping:** This maps directly to the magnetic induction field of an infinite straight wire carrying a steady current:
    $$\mathbf{B} = \frac{\mu I}{2\pi\rho} \hat{\boldsymbol{\phi}}$$
    The circulation of $\mathbf{B}$ around any closed curve enclosing the wire equals $\mu$ times the enclosed current, which is the integral form of Ampère's Law.
*   **The Multi-Valued Potential:** The pressure potential $p(\phi)$ is a **multi-valued helical function** of the angular coordinate $\phi$ [1]. Going around the wire once ($0 \le \phi < 2\pi$) drops the pressure potential by exactly $\Delta p = -k\Gamma$. This is the exact mathematical analogue of the **magnetic scalar potential ($\Omega$)** surrounding a current-carrying wire, demonstrating that in multiply connected regions enclosing current singularities, a scalar potential becomes multi-valued ($\oint \nabla \Omega \cdot d\mathbf{l} = -I_{\text{enc}}$).

---

#### Translation 2: Solenoid (Uniform Surface Distribution of Vortex Filaments)

**Step 1: Maxwell's Original Component Equations**

For a cylindrical surface of radius $R$ and infinite length, covered with a uniform distribution of vortex filaments carrying a surface density of circulation $\gamma$ (circulation per unit arc length), Maxwell derives the velocity field [1]:

$$\mathbf{v}_{\text{inside}} = \gamma \hat{\mathbf{z}}, \quad \mathbf{v}_{\text{outside}} = 0$$

The pressure potential inside the solenoid decreases linearly along the $z$-axis:

$$\frac{\partial p}{\partial z} = -k\gamma \implies p(z) = -k\gamma z + p_0$$

**Step 2: Identify the Modern Physical Quantities**

| Maxwell's Symbol | Physical Quantity | Modern Symbol | Electrostatic Analog | Magnetostatic Analog |
| :--- | :--- | :--- | :--- | :--- |
| $\gamma$ | Surface density of circulation | $\gamma$ | — | $\mu n I$ (magnetic field inside solenoid) |
| $k$ | Resistance of the medium | $k$ | Resistivity $1/\sigma$ | Reluctivity $1/\mu$ |
| $p(z)$ | Pressure potential along axis | $p(z)$ | Potential along axis | Magnetic potential along axis |

**Step 3: Convert to Modern Vector Notation**

The velocity field is written compactly as:
$$\mathbf{v} = \begin{cases} \gamma \hat{\mathbf{z}}, & \rho < R \\ 0, & \rho > R \end{cases}$$

The pressure gradient inside the solenoid is:
$$\nabla p = -k\gamma \hat{\mathbf{z}}$$

**Step 4: State the Physical Meaning in Modern English**

The solenoid produces a uniform velocity field in its interior and zero velocity in its exterior. 
*   **Magnetostatic Mapping:** The velocity inside the solenoid maps to the magnetic induction: $\mathbf{B}_{\text{inside}} = \mu n I \hat{\mathbf{z}}$, where $n$ is the number of turns per unit length and $I$ is the current.
*   **The Pressure Gradient and Intensity Mapping:** In a resistive medium, a uniform velocity requires a constant potential gradient to drive the flow against resistance: $\nabla p = -k\gamma \hat{\mathbf{z}}$. Since $-\nabla p \leftrightarrow \mathbf{H}$ (Magnetic Intensity) and $k = 1/\mu$, the intensity inside the solenoid is derived as [2]:
    $$\mathbf{H}_{\text{inside}} = -\nabla p = k \mathbf{v}_{\text{inside}} = \left(\frac{1}{\mu}\right) \mu n I \hat{\mathbf{z}} = n I \hat{\mathbf{z}}$$
    This demonstrates the physical power of the dual-layered analogy: **the magnetic intensity $\mathbf{H}$ inside a long solenoid is independent of the permeability $\mu$ of the medium ($H = n I$)**, whereas the magnetic induction $\mathbf{B}$ scales directly with $\mu$.
*   **Pressure Jump:** At the surface of the solenoid ($\rho = R$), there is a pressure jump. This pressure difference is balanced by the mechanical forces acting on the solenoid windings (the outward magnetic pressure).

---

#### Translation 3: Shielded Force Between Two Magnetic Poles

**Step 1: Maxwell's Original Component Equations**

For two point sources (magnetic poles) of strengths $m_1$ and $m_2$ separated by distance $r$ in a medium of uniform resistance $k$, Maxwell derives the force components [1]:

$$F_x = -k \frac{m_1 m_2}{r^3} x, \quad F_y = -k \frac{m_1 m_2}{r^3} y, \quad F_z = -k \frac{m_1 m_2}{r^3} z$$

**Step 2: Identify the Modern Physical Quantities**

| Maxwell's Symbol | Physical Quantity | Modern Symbol | Electrostatic Analog | Magnetostatic Analog |
| :--- | :--- | :--- | :--- | :--- |
| $m_1, m_2$ | Source strengths | $m_1, m_2$ | Electric Charges $q_1, q_2$ | Magnetic Poles $m_1, m_2$ |
| $k$ | Resistance of the medium | $k$ | Resistivity $1/\sigma$ | Reluctivity $1/\mu$ |
| $r$ | Separation distance | $r = |\mathbf{r}_1 - \mathbf{r}_2|$ | Separation distance | Separation distance |

**Step 3: Convert to Modern Vector Notation**

The component equations combine into the vector force relation:

$$\mathbf{F}_{12} = -k \frac{m_1 m_2}{r^2} \hat{\mathbf{r}}_{12}$$

**Step 4: State the Physical Meaning in Modern English**

The mechanical force between two point sources in a resistive medium is directly proportional to their source strengths, inversely proportional to the square of the distance separating them, and scaled directly by the medium's resistance $k$.
*   **Magnetostatic Mapping:** Since resistance $k$ maps to reluctivity $1/\mu$, this is the mathematically correct unrationalized Coulomb's Law for magnetic poles in a medium [2]:
    $$\mathbf{F}_{12} = -\frac{1}{\mu} \frac{m_1 m_2}{r^2} \hat{\mathbf{r}}_{12}$$
    The force is inversely proportional to permeability $\mu$ (scaled by reluctivity $k$), reflecting the physical shielding of the pole forces by the magnetic medium. In a medium of high permeability, the force between poles is reduced.

---

#### Translation 4: Limitations of the Fluid Analogy

**Step 1: Maxwell's Original Component Equations**

The applications in Section 5 reveal the fundamental limitations of the fluid analogy. Maxwell notes that the fluid model is strictly steady-state and cannot describe time-varying phenomena [1]:

**Step 2: Identify the Modern Physical Quantities**

| Limitation | Description | Why the Fluid Model Fails |
| :--- | :--- | :--- |
| **No Time Dependence** | The fluid model cannot describe time-varying fields or electromagnetic induction. | The equations are strictly $\nabla \cdot \mathbf{v} = 0$ and $\nabla^2 p = 0$ (steady-state). |
| **No Displacement Current** | There is no analogue of the displacement current $\partial \mathbf{D}/\partial t$. | The equation of continuity $\nabla \cdot \mathbf{v} = 0$ enforces strict incompressibility. |
| **Scalar Potential Only** | The fluid model is based on a scalar pressure potential $p$. | A scalar potential cannot represent vector fields with intrinsic directionality. |
| **No Physical Ether Model** | The fluid is a representative medium, not a physical hypothesis. | The model is a mathematical analogy, not a mechanical explanation. |

**Step 3: Convert to Modern Vector Notation**

The limitations can be expressed in terms of the missing terms in the fluid equations:

| Missing Phenomenon | Modern Vector Formulation | When Introduced |
| :--- | :--- | :--- |
| Time-varying fields | $\partial \mathbf{B}/\partial t \neq 0$ | Part II (1855) |
| Displacement current | $\partial \mathbf{D}/\partial t$ | Paper 2 (1861) |
| Vector potential | $\mathbf{A} = (F, G, H)$ | Part II (1855) |
| Mechanical ether model | Molecular vortices | Paper 2 (1861) |

**Step 4: State the Physical Meaning in Modern English**

The fluid analogy of Part I is a powerful mathematical tool for describing static electromagnetic phenomena, but it has fundamental limitations [1]:
1.  **No Time Dependence:** The fluid model is strictly steady-state. It cannot describe electromagnetic induction, which Faraday had shown depends on the *time-variation* of the magnetic field.
2.  **No Displacement Current:** The equation of continuity $\nabla \cdot \mathbf{v} = 0$ enforces strict incompressibility. There is no mechanism for current accumulation or displacement in dielectrics.
3.  **Scalar Potential Only:** The fluid model is based on a scalar pressure potential $p$. It cannot represent vector fields with intrinsic directionality, such as the vector potential $\mathbf{A}$.
4.  **No Physical Ether Model:** The fluid is explicitly a **representative medium**, not a physical hypothesis about the ether. It is a mathematical analogy, not a mechanical explanation.

**These limitations are the driving force behind Part II and ultimately Paper 2.** Maxwell recognizes that the fluid analogy must be superseded by a more general mathematical framework—the vector potential and the electro-tonic state—to account for the dynamical phenomena of electromagnetism [1].

---

### Standardized Commentary Block

- **The Goal:** Maxwell's objective in Section 5 is to apply the fluid analogy to specific geometric configurations—the infinite straight wire, the solenoid, and the forces between magnetic poles—to demonstrate the power of the analogy and to expose its limitations.
- **The Method:** Maxwell derives the velocity fields and pressure distributions for each configuration using the mathematical tools developed in Sections 1–4. He shows that the fluid model correctly predicts the field configurations and forces for static electromagnetic systems.
- **The Limitation:** The applications in Section 5 expose the fundamental limitations of the fluid analogy: no time dependence, no displacement current, scalar potential only, and no physical ether model. These limitations motivate the transition to Part II.
- **The Legacy:** The applications demonstrate the power of analogical reasoning in mathematical physics. The concepts of vortex filaments, flux tubes, and field line topology established here laid the groundwork for the full electromagnetic theory.

---

### Exegesis Workflow Callout

Before proceeding to Phase 4 (Visualization), the reader must execute the **Post-Reading Reconciliation Protocol (Section 1.2.2)**:
1.  Verify that your customized glossary entries in Appendix A align with the dual-layered mappings derived in this section, particularly the vortex filament, solenoid, and force between poles.
2.  Audit your Cartesian-to-vector derivations against the **Zone 2 Quality Control Check (Section 1.2.1)** to ensure:
    *   The multi-valued potential $p(\phi) = -k\frac{\Gamma}{2\pi}\phi + p_0$ is correctly derived and its topological implications are understood.
    *   The solenoid pressure gradient $\nabla p = -k\gamma \hat{\mathbf{z}}$ is correctly derived.
    *   The shielded force $\mathbf{F}_{12} = -k \frac{m_1 m_2}{r^2}\hat{\mathbf{r}}$ correctly reflects the shielding effect of the medium.
    *   The limitations of the fluid analogy are clearly articulated and linked to the transition to Part II.
3.  Confirm that the visualizations generated in Phase 4 accurately represent the field configurations for the infinite wire, solenoid, and force between poles.

---

### Connections to Later Papers

| Concept in Paper 1 | Later Development |
| :--- | :--- |
| Vortex filament $\mathbf{v} = \frac{\Gamma}{2\pi\rho} \hat{\boldsymbol{\phi}}$ | **Paper 2 (1861):** Replaced by rotating molecular vortices as the physical mechanism for magnetic fields. |
| Solenoid $\mathbf{v} = \gamma \hat{\mathbf{z}}$ (interior) | **Paper 2 (1861):** Reinterpreted as the uniform magnetic field produced by a solenoid in the molecular vortex model. |
| Shielded force $\mathbf{F}_{12} = -k \frac{m_1 m_2}{r^2}\hat{\mathbf{r}}$ | **Paper 3 (1865):** Retained as the force between magnetic poles in the full electromagnetic theory. |
| Limitations of fluid analogy | **Part II (1855):** Addressed by introducing the vector potential $\mathbf{A}$. |
| No time dependence | **Part II (1855):** Addressed by introducing the time-varying vector potential $\mathbf{A}$ and the equations of induction. |

---

### References Integration Callout

#### The Treatise on Electricity and Magnetism (1873)

The following articles of Maxwell's *Treatise* (1873) provide direct commentary on the applications of Section 5:

| *Treatise* Article | Connection to Section 5 |
| :--- | :--- |
| **Articles 86–90** | Maxwell's discussion of the magnetic field of a straight wire and solenoid [2]. |
| **Article 87** | The derivation of the magnetic field of an infinite straight wire. |
| **Article 88** | The magnetic field along the axis of a solenoid. |
| **Article 89** | The forces between magnetic poles and currents. |
| **Article 90** | The limitations of the scalar potential model and the transition to the vector potential. |

#### Heaviside's Electromagnetic Theory (1893)

Heaviside's vector reformulations provide a modern perspective on the applications of Section 5:

| Heaviside Section | Connection to Section 5 |
| :--- | :--- |
| **Volume I, Chapter 7** | Heaviside's treatment of the magnetic field of a straight wire and solenoid in vector notation [3]. |
| **Volume II, Chapter 8** | The forces between currents in vector notation. |
| **Volume II, Chapter 9** | Historical commentary on Maxwell's use of the fluid analogy in applications. |

#### Integration Instructions

During Phase 2 (Active Reading), the reader should:

1. **Identify the specific *Treatise* articles** that correspond to the applications in Section 5 and read them in parallel with the source text.
2. **Consult Heaviside's commentary** to understand how the applications were translated into vector notation and how they relate to modern electromagnetic theory.
3. **Note the limitations** of the fluid analogy exposed by these applications and how they motivate the transition to Part II.


---

### References

[1] Maxwell, J. C. (1858). *On Faraday's Lines of Force*. Transactions of the Cambridge Philosophical Society, Vol. X, Part I. *(Note: Read in two parts: Part I on Dec 10, 1855; Part II on Feb 11, 1856. Published in 1858.)*

[2] Maxwell, J. C. (1873). *A Treatise on Electricity and Magnetism*. Oxford: Clarendon Press.

[3] Heaviside, O. (1893). *Electromagnetic Theory*. London: The Electrician Printing and Publishing Company.

[4] Bork, A. M. (1966). Physics just before Einstein. *Science*, 152(3722), 597–603.

[5] Jackson, J. D. (1999). *Classical Electrodynamics*. John Wiley & Sons.