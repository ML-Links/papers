# Part I, Section 4: Forces Between Lines of Force

## Phase 1: Preparatory Foundations

### Objectives and Checklist

By the end of this section, the reader will:

- [ ] Understand Maxwell's mechanical interpretation of lines of force as entities acting under **longitudinal tension** and **lateral pressure**.
- [ ] Derive the hydrostatic pressure potential distribution in the fluid from the non-inertial constitutive relation $\mathbf{v} = -\frac{1}{k} \nabla p$.
- [ ] Understand how the **aspect ratio of unit cells** ($ds = k \, dn$) encodes the mechanical forces acting on the lines of force.
- [ ] Formulate the virtual energy density $U = \frac{1}{2k}|\nabla p|^2$ and understand how its spatial gradient ($\mathbf{f} = -\nabla U$) drives field-line repulsion.
- [ ] Map the mechanical forces in the fluid model to electromagnetic forces (attraction and repulsion between currents, magnets, and charges).
- [ ] Distinguish clearly between the **isotropic scalar pressure analysis** of Part I (1855) and the **symmetric rank-2 stress tensor** of Paper 2 (1861).

---

### Terminology Mapping: Lateral Pressure, Longitudinal Tension, and Mechanical Forces

In Section 4, Maxwell moves from geometry to mechanics. The fluid model now provides not only a descriptive language for field lines but also a **causal representation** for forces. The following table maps the fluid concepts to their electromagnetic analogues, maintaining consistency with the intensity-quantity mappings from previous sections:

| Fluid Concept | Symbol / Definition | Electrostatic Analog | Magnetostatic Analog |
| :--- | :--- | :--- | :--- |
| **Pressure Potential** | $p$ (scalar potential) | Electrostatic potential $\phi$ | Magnetic potential $\Omega$ |
| **Potential Gradient** | $-\nabla p$ (Intensity vector) | Electric Field $\mathbf{E}$ | Magnetic Intensity $\mathbf{H}$ |
| **Velocity (Quantity)** | $\mathbf{v} = -\frac{1}{k} \nabla p$ | Current Density $\mathbf{J}$ | Magnetic Induction $\mathbf{B}$ |
| **Virtual Energy Density** | $U = \frac{1}{2k} |\nabla p|^2 = \frac{1}{2}k|\mathbf{v}|^2$ | Electrostatic energy density: $\frac{1}{2} \epsilon_0 E^2$ | Magnetic energy density / pressure: $\frac{1}{2\mu} B^2$ |
| **Longitudinal Tension** | $T = U$ (acting along streamlines) | Tension along electric field lines | Tension along magnetic field lines |
| **Lateral Pressure** | $P = U$ (acting transverse to streamlines) | Pressure between field lines | Pressure between field lines |
| **Attraction/Repulsion** | $\mathbf{f} = -\nabla U$ (force density) | Attraction of opposite charges, repulsion of like charges | Attraction of parallel currents, repulsion of anti-parallel currents |

**Critical Distinction:** The pressure potential $p$ in the fluid model is **not** the physical pressure of a gas or liquid. It is the scalar potential whose gradient drives the flow. However, Maxwell uses the concept of "hydrostatic pressure" in the fluid to represent the **mechanical forces** that field lines exert on each other. This is a mathematical analogy: the fluid's pressure distribution is isomorphic to the mechanical stress distribution in the field.

**Historical Warning:** The mechanical interpretation of lines of force in Part I is **qualitative** and based on the resistive fluid analogy. It is not the full mathematical stress tensor of electromagnetism, which Maxwell will develop in Paper 2 (1861) using rotating molecular vortices. The exegesis must maintain this distinction: the "tension" and "pressure" of Part I are hydrodynamic analogues, not the complete Maxwell Stress Tensor.

---

### Mathematical Note: Pressure Distributions and Virtual Stress Fields

#### 1. Non-Inertial Hydrostatic Potential

In the resistive fluid model, the velocity is determined strictly by the first-order force balance (Darcy's Law):

$$\mathbf{v} = -\frac{1}{k} \nabla p$$

Because the medium's resistance instantly balances the pressure gradient, the fluid has no momentum, meaning the flow is governed by non-inertial kinematics. The continuity equation (incompressibility) dictates:

$$\nabla \cdot \mathbf{v} = 0 \implies \nabla^2 p = 0 \quad \text{(in source-free, uniform regions)}$$

The pressure distribution is a solution to Laplace's equation. The geometry of this pressure field determines the virtual mechanical forces.

#### 2. The Energetic Derivation of Virtual Stress ($U = \frac{1}{2k} |\nabla p|^2$)

The rate of work done per unit volume by the pressure gradient against the medium's resistance is:

$$\frac{dW}{dt} = \mathbf{F}_{\text{pressure}} \cdot \mathbf{v} = (-\nabla p) \cdot \mathbf{v} = k |\mathbf{v}|^2 = \frac{1}{k} |\nabla p|^2$$

Following the transport analogies of Fourier and Ohm, we define the **virtual energy density ($U$)** of the flow field as half the rate of localized energy dissipation per unit conductibility ($1/k$):

$$U = \frac{1}{2} k |\mathbf{v}|^2 = \frac{1}{2k} |\nabla p|^2$$

This quadratic form corresponds directly to the electrostatic energy density and the magnetostatic pressure:

$$U_{\text{electrostatic}} = \frac{1}{2}\epsilon_0 E^2 \quad \text{and} \quad U_{\text{magnetic}} = \frac{1}{2\mu} B^2$$

#### 3. The Geometric Origin of Field Repulsion ($\mathbf{f} = -\nabla U$)

To understand how these virtual forces act on the field lines, we evaluate a 2D unit cell under the normalizations $dQ = 1$ and $dp = 1$. From Section 2, the cell width $ds$ (streamline spacing) and length $dn$ (equipotential spacing) satisfy the aspect-ratio relation:

$$ds = k \, dn \implies dn = \frac{ds}{k}$$

The potential gradient magnitude within the cell is:

$$|\nabla p| = \frac{dp}{dn} = \frac{1}{dn} = \frac{k}{ds}$$

Substituting this into our virtual energy density expression yields:

$$U = \frac{1}{2k} \left(\frac{k}{ds}\right)^2 = \frac{k}{2(ds)^2}$$

This demonstrates that **the virtual energy density of the field scales inversely with the square of the streamline spacing ($ds$)** [1]. If adjacent streamlines converge (crowding the lines of force together), $ds$ decreases, causing a localized surge in the virtual energy density $U$.

To satisfy the variational principle of least resistance, the system exerts a transverse force density to spread the streamlines apart and minimize the integrated energy:

$$\mathbf{f}_{\text{lateral}} = -\nabla U$$

This gradient of energy density is the mathematical origin of **lateral field-line repulsion**. Conversely, along the length of the streamlines, the potential gradient acts as a longitudinal tension, pulling the lines of force along their length to minimize their total path.

#### 4. Forces Between Parallel Currents

Consider two parallel current-carrying wires, modeled in Part I as vortex filaments (sources of circulation). 
*   **The Non-Inertial Mechanism:** Because the fluid is non-inertial, **there is no Bernoulli's principle** in this model. The forces between the filaments are not driven by localized $v^2$ velocity pressure drops. Instead, the force is derived hydrostatically by integrating the total virtual energy density $U$ of the combined field.
*   **Parallel Currents (Same Direction):** The circulation fields surrounding the two filaments reinforce each other in the outer regions but oppose (and cancel) each other in the intermediate space between them. This cancellation reduces the local streamline density ($ds$ increases) between the filaments, lowering the intermediate energy density $U$. The surrounding higher-energy field exerts a net compressive force, pushing the filaments together (**attraction**).
*   **Anti-Parallel Currents (Opposite Directions):** The circulation fields reinforce each other in the intermediate space between the filaments, crowding the streamlines ($ds$ decreases) and causing a severe surge in the local energy density $U$. The gradient of this energy density pushes the filaments apart (**repulsion**).

---

### Pre-Reading Checklist for Phase 2

Before proceeding to the active reading of Maxwell's text on forces between lines of force, the reader should confirm:

- [ ] The mechanical interpretation of field lines as entities under **tension** and **pressure** is understood.
- [ ] The fatal error of invoking Bernoulli's principle in a non-inertial Darcy flow is recognized.
- [ ] The derivation of the virtual energy density $U = \frac{1}{2k}|\nabla p|^2$ from the rate of energy dissipation is understood.
- [ ] The geometric mechanism of lateral repulsion ($\mathbf{f} = -\nabla U$, where $U \propto 1/(ds)^2$) is internalized.
- [ ] The distinction between the **isotropic scalar pressure** of Part I and the **symmetric rank-2 stress tensor** of Paper 2 is clear.

---

### Connection to the Rest of the Exegesis

*   **Phase 2 (Active Reading):** The reader will encounter Maxwell's derivation of the forces between lines of force, his discussion of tension and pressure, and his application to parallel currents and magnetic poles. The terminology mapping above will guide the translation of his 19th-century mechanical language.
*   **Phase 3 (Mathematical Formalization):** After reading, the reader will formalize the pressure distributions in vector notation, derive the force per unit area on field lines, and explicitly map the fluid pressure to the electromagnetic stress.
*   **Phase 4 (Computational Visualization):** The reader will generate 2D pressure-field contour maps for parallel and anti-parallel current configurations, visualizing the lateral pressure and tension in the field lines.

---

### Historical Note: The Anticipation of the Maxwell Stress Tensor

The analysis of forces between lines of force in Part I is a remarkable anticipation of the Maxwell Stress Tensor, which Maxwell will formulate in Paper 2 (1861). However, the two are distinct:

*   **Part I (1855):** The pressure analysis is **hydrostatic** and based on the resistive fluid analogy. The pressure is represented by an isotropic scalar quantity ($p$), and the forces are derived from its gradient. Because a scalar potential has only one degree of freedom, it cannot mathematically represent shear stresses or independent directional tensions. It is a qualitative mathematical analogue.
*   **Paper 2 (1861):** The stress tensor is **mechanical** and based on the molecular vortex model. The stress is a symmetric, rank-2 tensor quantity ($\mathbf{T}$) with nine independent components [2]:
    $$T_{ij} = \frac{1}{\mu} B_i B_j - \frac{1}{2\mu} B^2 \delta_{ij}$$
    The forces are derived from the divergence of this tensor ($\mathbf{f} = \nabla \cdot \mathbf{T}$). This is a physical model of the ether, with rotating vortices transmitting stress directionally.

The exegesis must maintain this distinction: Part I's pressure analysis is a **mathematical analogy** that happens to produce the correct qualitative predictions. Paper 2's stress tensor is a **physical model** that provides a rigorous, directional mathematical framework for all electromagnetic forces.


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
| $k\mathbf{v} = -\nabla p$ | Intensity vector | $k\mathbf{v}$ | Electric Field $\mathbf{E}$ | Magnetic Intensity $\mathbf{H}$ |
| $U$ | Virtual energy density | $U$ | Electrostatic energy density $\frac{1}{2}\epsilon_0 E^2$ | Magnetic energy density $\frac{1}{2\mu}B^2$ |
| $\mathbf{f}$ | Force density | $\mathbf{f}$ | Force density on charges | Force density on currents |

**Step 3: Convert to Modern Vector Notation**

Rewrite the component equations as a single vector equation using the operators $\nabla$, $\cdot$, and $\times$.

**Step 4: State the Physical Meaning in Modern English**

Articulate the physical meaning of the translated equation in clear, modern language, with explicit acknowledgment of the non-inertial framework and the distinction between the isotropic scalar pressure of Part I and the tensor stress of Paper 2.

---

### Component-to-Vector Translation

#### Translation 1: The Virtual Energy Density (Stress Potential)

**Step 1: Maxwell's Original Component Equations**

In Part I, Section 4, Maxwell relates the local rate of energy dissipation per unit volume to a virtual scalar stress potential $U$ [1, 2]:

$$U = \frac{1}{2k} \left[ \left(\frac{\partial p}{\partial x}\right)^2 + \left(\frac{\partial p}{\partial y}\right)^2 + \left(\frac{\partial p}{\partial z}\right)^2 \right]$$

**Step 2: Identify the Modern Physical Quantities**

| Maxwell's Symbol | Physical Quantity | Modern Symbol | Electrostatic Analog | Magnetostatic Analog |
| :--- | :--- | :--- | :--- | :--- |
| $p$ | Pressure potential | $p$ | Potential $\phi$ | Potential $\Omega$ |
| $k$ | Resistance of the medium | $k$ | Resistivity $1/\sigma$ | Reluctivity $1/\mu$ |
| $\frac{\partial p}{\partial x}$, etc. | Potential gradient components | $\nabla p$ | Gradient $\nabla \phi$ | Gradient $\nabla \Omega$ |

**Step 3: Convert to Modern Vector Notation**

This sum of squared partial derivatives is written compactly in vector notation as:

$$U = \frac{1}{2k} |\nabla p|^2 = \frac{1}{2} k |\mathbf{v}|^2$$

**Step 4: State the Physical Meaning in Modern English**

The virtual energy density $U$ of the flow field is a quadratic function of the local potential gradient (or local velocity). 
*   **Conduction Mapping:** $U$ corresponds to the rate of energy dissipation per unit conductibility: $U \leftrightarrow \frac{1}{2}\sigma E^2$.
*   **Magnetostatic Mapping:** $U$ maps to the magnetic energy density: $U \leftrightarrow \frac{1}{2\mu} B^2 = \frac{1}{2}\mu H^2$.

**The Non-Inertial Caveat:** Because the fluid is non-inertial ($\rho = 0$), $U = \frac{1}{2} k|\mathbf{v}|^2$ is **not** physical kinetic energy ($\frac{1}{2}\rho v^2$). It is a *virtual* stress potential derived from the local rate of transport work, preventing any retroactive insertion of momentum-based fluid dynamics.

---

#### Translation 2: Isotropic Hydrostatic Force Density

**Step 1: Maxwell's Original Component Equations**

In Part I, Section 4, Maxwell expresses the mechanical force components ($f_x, f_y, f_z$) acting on the medium as the spatial derivatives of the pressure field potential [1]:

$$f_x = -\frac{\partial U}{\partial x}, \quad f_y = -\frac{\partial U}{\partial y}, \quad f_z = -\frac{\partial U}{\partial z}$$

**Step 2: Identify the Modern Physical Quantities**

| Maxwell's Symbol | Physical Quantity | Modern Symbol | Electrostatic Analog | Magnetostatic Analog |
| :--- | :--- | :--- | :--- | :--- |
| $U$ | Virtual energy density | $U$ | Electrostatic energy density | Magnetic energy density |
| $f_x, f_y, f_z$ | Force density components | $\mathbf{f} = (f_x, f_y, f_z)$ | Electrostatic force density | Magnetostatic force density |

**Step 3: Convert to Modern Vector Notation**

The three scalar force components combine into a single gradient relation:

$$\mathbf{f} = -\nabla U = -\nabla \left( \frac{1}{2k} |\nabla p|^2 \right)$$

**Step 4: State the Physical Meaning in Modern English**

The mechanical force density $\mathbf{f}$ acting on the medium is the negative gradient of the virtual energy density $U$. This represents the principle of virtual work: the field system exerts forces to drive the geometry toward a state of minimum potential energy (least resistance). In the magnetostatic analogue, this maps to the magnetic force density ($\mathbf{f} = -\nabla U_m$), which drives the attraction and repulsion of magnetic media.

---

#### Translation 3: Geometric Force Scaling via Streamline Spacing (2D)

**Step 1: Maxwell's Original Component Equations**

Substituting the 2D unit cell relation $ds = k \, dn$ (with $dp = 1$ and $dQ = 1$, where $ds$ is the streamline spacing and $dn$ is the equipotential spacing) into the virtual energy density:

$$U = \frac{1}{2k} \left( \frac{k}{ds} \right)^2 = \frac{k}{2(ds)^2}$$

The force components are written as the spatial derivatives of this geometric spacing:

$$f_{\text{lateral}} = -\frac{\partial}{\partial n} \left( \frac{k}{2(ds)^2} \right)$$

**Step 2: Identify the Modern Physical Quantities**

| Maxwell's Symbol | Physical Quantity | Modern Symbol | Electrostatic Analog | Magnetostatic Analog |
| :--- | :--- | :--- | :--- | :--- |
| $ds$ | Streamline spacing | $ds$ | Field line spacing | Field line spacing |
| $k$ | Resistance of the medium | $k$ | Resistivity $1/\sigma$ | Reluctivity $1/\mu$ |
| $f_{\text{lateral}}$ | Transverse force density | $\mathbf{f}_{\text{lateral}}$ | Transverse force | Lateral field pressure |

**Step 3: Convert to Modern Vector Notation**

The lateral force density perpendicular to the streamlines (along the normal direction $\hat{\mathbf{n}}$) is:

$$\mathbf{f}_{\text{lateral}} = -\nabla U \propto \frac{k}{(ds)^3} \frac{\partial (ds)}{\partial n} \hat{\mathbf{n}}$$

**Step 4: State the Physical Meaning in Modern English**

Because the virtual energy density scales inversely with the square of the streamline spacing ($U \propto 1/(ds)^2$), any crowding of the streamlines ($ds$ decreasing) causes a sharp localized surge in energy density. To minimize this energy, the field exerts a transverse force density pushing the streamlines apart. This is the precise mathematical and geometric origin of **lateral field-line repulsion**.

---

#### Translation 4: Shielded Force Between Point Poles

**Step 1: Maxwell's Original Component Equations**

For two localized point sources (magnetic poles) of strengths $m_1$ and $m_2$ separated by a distance $r$ in a medium of uniform resistance $k$, Maxwell derives the components of the mechanical force acting between them [1]:

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
*   **Magnetostatic Mapping:** Since resistance $k$ maps to reluctivity $1/\mu$, this is the mathematically correct unrationalized Coulomb's Law for magnetic poles:
    $$\mathbf{F}_{12} = -\frac{1}{\mu} \frac{m_1 m_2}{r^2} \hat{\mathbf{r}}_{12}$$
    The force is inversely proportional to permeability $\mu$ (scaled by reluctivity $k$), reflecting the physical shielding of the pole forces by the magnetic medium [2].

---

#### Translation 5: Force Between Parallel current Filaments

**Step 1: Maxwell's Original Component Equations**

For two parallel current filaments of circulation strengths $\Gamma_1$ and $\Gamma_2$ separated by distance $r$ in a medium of uniform resistance $k$, Maxwell derives the transverse force per unit length [1]:

$$F_{\text{per length}} = \frac{k \Gamma_1 \Gamma_2}{2\pi r}$$

**Step 2: Identify the Modern Physical Quantities**

| Maxwell's Symbol | Physical Quantity | Modern Symbol | Electrostatic Analog | Magnetostatic Analog |
| :--- | :--- | :--- | :--- | :--- |
| $\Gamma_1, \Gamma_2$ | Circulation strengths | $\Gamma_1, \Gamma_2$ | — | Currents $\mu I_1, \mu I_2$ |
| $k$ | Resistance of the medium | $k$ | — | Reluctivity $1/\mu$ |
| $r$ | Separation distance | $r$ | — | Separation distance |

**Step 3: Convert to Modern Vector Notation**

The transverse force per unit length is formulated vectorially as:

$$\mathbf{F}_{12} = \frac{k \Gamma_1 \Gamma_2}{2\pi r} \hat{\mathbf{r}}$$

**Step 4: State the Physical Meaning in Modern English**

The force per unit length between two parallel current filaments is proportional to the product of their circulation strengths and inversely proportional to the distance separating them.
*   **Magnetostatic Mapping:** With $k = 1/\mu$ and $\Gamma \leftrightarrow \mu I$, this yields the classical force between parallel current-carrying wires:
    $$F_{\text{per length}} = \frac{\mu I_1 I_2}{2\pi r}$$
    The force is attractive for parallel circulations ($\Gamma_1 \Gamma_2 > 0$) and repulsive for anti-parallel circulations ($\Gamma_1 \Gamma_2 < 0$).

**The Non-Inertial Mechanism:** Because the fluid has no inertia, **Bernoulli's principle does not apply**. This attraction/repulsion is driven strictly by the spatial gradient of the integrated virtual energy density $U$ ($\mathbf{f} = -\nabla U$). In the region between parallel currents, the circulations oppose and cancel, lowering $U$. The surrounding higher-energy density exerts a net compressive force, pushing the wires together.

---

### Standardized Commentary Block

*   **The Goal:** Maxwell's objective in Section 4 is to derive the mechanical forces between lines of force from the virtual energy density of the fluid model. This provides a mathematical foundation for the forces between currents, magnets, and charges within the analogical framework.
*   **The Method:** Maxwell defines a virtual energy density $U = \frac{1}{2k}|\nabla p|^2 = \frac{1}{2}k|\mathbf{v}|^2$ from the rate of work done by the pressure gradient. He then shows that the force density is the negative gradient of this energy density ($\mathbf{f} = -\nabla U$). Using the unit cell geometry ($ds = k \, dn$), he demonstrates that $U \propto 1/(ds)^2$, providing the geometric origin of lateral repulsion.
*   **The Limitation:** The pressure analysis of Section 4 is based on an **isotropic scalar pressure** $p$. It cannot represent shear stresses, directional tensions, or the full mechanical stress tensor of electromagnetism. The forces are hydrostatic, not directional.
*   **The Legacy:** The scalar pressure analysis of Part I anticipates the Maxwell Stress Tensor of Paper 2 (1861). The concept of field energy density and the principle of virtual work established here laid the foundation for the mechanical interpretation of electromagnetic fields.

---

### Exegesis Workflow Callout

Before proceeding to Phase 4 (Visualization), the reader must execute the **Post-Reading Reconciliation Protocol (Section 1.2.2)**:
1.  Verify that your customized glossary entries in Appendix A align with the dual-layered mappings derived in this section, particularly the virtual energy density $U$ and the force density $\mathbf{f} = -\nabla U$.
2.  Audit your Cartesian-to-vector derivations against the **Zone 2 Quality Control Check (Section 1.2.1)** to ensure:
    *   **No Bernoulli Principle Invoked:** The forces are derived from the energy gradient, not from velocity-squared pressure drops.
    *   **Correct Scaling:** The energy density scales as $U \propto 1/(ds)^2$ from the unit cell relation.
    *   **Scalar vs. Tensor:** The distinction between the scalar pressure of Part I and the tensor stress of Paper 2 is clearly articulated.

---

### Connections to Later Papers

| Concept in Paper 1 | Later Development |
| :--- | :--- |
| $U = \frac{1}{2k}|\nabla p|^2$ (Virtual energy density) | **Paper 2 (1861):** Becomes the magnetic energy density $\frac{1}{2\mu}B^2$ in the molecular vortex model. |
| $\mathbf{f} = -\nabla U$ (Force density from energy gradient) | **Paper 2 (1861):** Generalized to the stress tensor divergence: $\mathbf{f} = \nabla \cdot \mathbf{T}$. |
| Lateral repulsion $U \propto 1/(ds)^2$ | **Paper 2 (1861):** Reinterpreted as the pressure exerted by magnetic field lines on each other. |
| Scalar pressure $p$ | **Paper 2 (1861):** Replaced by the symmetric rank-2 Maxwell Stress Tensor $\mathbf{T}$ [2]. |
| Forces between parallel currents | **Paper 3 (1865):** Retained as a consequence of the full electromagnetic field equations. |

---

### References Integration Callout

#### The Treatise on Electricity and Magnetism (1873)

The following articles of Maxwell's *Treatise* (1873) provide direct commentary on the forces between lines of force:

| *Treatise* Article | Connection to Section 4 |
| :--- | :--- |
| **Articles 81–85** | Maxwell's discussion of the mechanical forces on lines of force [2]. |
| **Article 82** | The definition of "tension" and "pressure" in the context of field lines [2]. |
| **Article 84** | The application of the pressure-tension framework to calculate forces between currents [2]. |
| **Article 85** | The limitations of the scalar pressure model and the need for the stress tensor [2]. |
| **Articles 641–646** | The full Maxwell Stress Tensor as developed in the *Treatise* [2]. |

#### Heaviside's Electromagnetic Theory (1893)

Heaviside's vector reformulations provide a modern perspective on the forces derived in Section 4:

| Heaviside Section | Connection to Section 4 |
| :--- | :--- |
| **Volume I, Chapter 5** | Heaviside's treatment of field energy density and the principle of virtual work [3]. |
| **Volume I, Chapter 6** | The derivation of forces on currents from the field energy [3]. |
| **Volume II, Chapter 7** | Historical commentary on Maxwell's pressure-tension framework [3]. |


---

### References

[1] Darrigol, O. (2000). *Electrodynamics from Ampère to Einstein*. Oxford University Press.

[2] Jackson, J. D. (1999). *Classical Electrodynamics*. John Wiley & Sons.

[3] Maxwell, J. C. (1858). *On Faraday's Lines of Force*. Transactions of the Cambridge Philosophical Society, Vol. X, Part I. *(Note: Read in two parts: Part I on Dec 10, 1855; Part II on Feb 11, 1856. Published in 1858.)*

[4] Maxwell, J. C. (1873). *A Treatise on Electricity and Magnetism*. Oxford: Clarendon Press.

[5] Heaviside, O. (1893). *Electromagnetic Theory*. London: The Electrician Printing and Publishing Company.

