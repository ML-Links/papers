# Part I, Section 2: Defining the Fundamental Quantities

## Phase 1: Preparatory Foundations

### Objectives and Checklist

By the end of this section, the reader will:

- [ ] Understand Maxwell's geometric definition of the **unit flow tube** as a tubular bundle of streamlines carrying a constant unit of flux ($dQ = 1$).
- [ ] Understand the 3D **unit cell** as the segment of a unit flow tube bounded by two equipotential surfaces separated by a unit potential drop ($dp = 1$).
- [ ] Recognize the precise reciprocal relationship between the spacing of streamlines ($ds$ or $dA$) and the spacing of equipotential surfaces ($dn$).
- [ ] Formalize the distinction between **geometric quantity** (flux, velocity vector $\mathbf{v}$) and **geometric intensity** (driving force, negative pressure gradient $-\nabla p$) within the fluid model.
- [ ] Derive Laplace's equation for the potential in source-free regions, and Poisson's equation in regions containing sources, with the proper resistance scaling factor $k$.
- [ ] Appreciate how these normalized geometric constructs allow the physical properties of a medium ($k$) to be encoded directly into the shape of its fields.

---

### Terminology Mapping: Geometric Quantity vs. Geometric Intensity

In Part I, Section 2, Maxwell introduces a critical terminological distinction that permeates all subsequent electromagnetic theory: the separation of field properties into *intensive* (local, gradient-based) and *extensive* (integral, flux-based) quantities. Within the fluid analogy, these map as follows:

| Geometric Construct | Fluid Interpretation | Electrostatic Analog | Magnetostatic Analog |
| :--- | :--- | :--- | :--- |
| **Intensity** | Negative pressure gradient $-\nabla p$ (driving force per unit volume) | Electric Field $\mathbf{E} = -\nabla \phi$ | Magnetic Intensity $\mathbf{H} = -\nabla \Omega$ |
| **Quantity** | Fluid velocity $\mathbf{v}$ (volume flux per unit area) | Current Density $\mathbf{J}$ | Magnetic Induction $\mathbf{B}$ |
| **Unit Flow Tube** | A bundle of streamlines carrying a normalized constant flux ($dQ = 1$ through any cross-section) | Tube of current | Tube of magnetic induction |
| **Unit Cell (3D)** | The volume segment of a unit flow tube bounded by two equipotential surfaces with a unit potential drop ($dp = 1$) | Elementary region of the potential field | Elementary region of the magnetic potential field |
| **Flux through a tube** | $Q = \iint_S \mathbf{v} \cdot d\mathbf{S}$ | Electric Current $I$ | Magnetic Flux $\Phi$ |
| **Potential Difference** | $\Delta p = p_1 - p_2$ (pressure drop along a tube) | Voltage $\Delta \phi$ | Magnetomotive Force (MMF) |

**Conceptual Note:** The *unit flow tube* is Maxwell's geometrical translation of Faraday's qualitative line of force. Faraday's lines were discrete; Maxwell's tubes are continuous, quantifiable bundles whose total flux is invariant along their length. This invariance is a direct consequence of the incompressibility condition $\nabla \cdot \mathbf{v} = 0$.

The *unit cell* is the fundamental building block of the field geometry: its shape encodes the local relationship between intensity (how closely spaced the equipotentials are) and quantity (how closely spaced the streamlines are). This relationship will prove essential when Maxwell derives the forces between lines of force in Section 4.

---

### Mathematical Note: The Geometry of Flow Tubes and Unit Cells

#### 1. The Unit Flow Tube and Flux Invariance

Consider a bundle of streamlines forming a tube. Let $S_1$ and $S_2$ be two cross-sectional surfaces of the tube at different locations along its length. Since the fluid is incompressible ($\nabla \cdot \mathbf{v} = 0$) and no sources exist within the tube, the flux through any cross-section is invariant:

$$Q = \iint_{S_1} \mathbf{v} \cdot d\mathbf{S}_1 = \iint_{S_2} \mathbf{v} \cdot d\mathbf{S}_2 = \text{constant}$$

In terms of the constitutive relation $\mathbf{v} = -\frac{1}{k} \nabla p$, this becomes:

$$Q = -\frac{1}{k} \iint_S \nabla p \cdot d\mathbf{S} = \text{constant along the tube}$$

This implies that if the cross-sectional area of the tube decreases, the potential gradient (and hence the intensity) must increase proportionally. This is the geometric origin of the inverse relationship between field line density and intensity: **lines of force crowd together where the field is strong**.

#### 2. The Unit Cell and Orthogonality (Dimensional Analysis)

In an isotropic medium ($k$ is a scalar), the velocity vector $\mathbf{v}$ is everywhere parallel to $-\nabla p$. Therefore:

*   **Streamlines** are curves representing the path of steepest pressure drop.
*   **Equipotential surfaces** are surfaces of constant pressure $p$.

Streamlines and equipotential surfaces intersect at right angles, forming a **curvilinear coordinate system**. 

To define a **unit cell**, we apply two strict mathematical normalizations:
1.  The cell must be bounded by a unit flow tube carrying a unit flux: $dQ = 1$.
2.  The cell must be bounded along its length by two equipotential surfaces separated by a unit potential difference: $dp = 1$.

##### Planar (2D) Geometry
For a simplified two-dimensional flow, let $ds$ represent the streamline spacing (width of the tube) and $dn$ represent the equipotential spacing (length of the cell). The local flux through the cell cross-section (assuming unit depth) is:

$$dQ = |\mathbf{v}| \, ds = \frac{1}{k} |-\nabla p| \, ds$$

Since $|-\nabla p| = \frac{dp}{dn}$, we write:

$$dQ = \frac{1}{k} \frac{dp}{dn} \, ds$$

Applying our unit normalizations ($dQ = 1$ and $dp = 1$) yields:

$$1 = \frac{1}{k} \frac{1}{dn} \, ds \implies ds = k \, dn$$

This relation has profound physical implications: in a uniform medium of unit resistance ($k = 1$), **the 2D unit cells are mathematically perfect squares ($ds = dn$)** [1]. If the medium's resistance $k$ varies, the cells distort into rectangles whose aspect ratio ($ds/dn = k$) encodes the local resistance of the medium.

##### Spatial (3D) Geometry
In three-dimensional space, the cross-sectional area of the unit flow tube is $dA$, and the equipotential spacing is $dn$. The unit flux relation is formulated as:

$$dQ = \frac{1}{k} \frac{dp}{dn} \, dA \implies 1 = \frac{1}{k} \frac{1}{dn} \, dA \implies dA = k \, dn$$

The local cross-sectional area $dA$ of a unit flow tube is scaled directly by the local equipotential spacing $dn$ and the local resistance $k$. Thus, the local volume of a 3D unit cell is:

$$dV = dA \cdot dn = k \, (dn)^2$$

In a medium of unit resistance ($k=1$), the cross-sectional area of a tube is exactly equal to the cell's length ($dA = dn$), and the volume scales as the square of the equipotential spacing [1].

#### 3. Laplace's and Poisson's Equations in the Unit Cell Framework

Combining the constitutive relation $\mathbf{v} = -\frac{1}{k}\nabla p$ with the continuity equation $\nabla \cdot \mathbf{v} = 0$ (in source-free regions) gives:

$$\nabla \cdot \left(-\frac{1}{k} \nabla p\right) = 0 \implies \nabla^2 p = 0 \quad \text{(Laplace's equation)}$$

In regions containing fluid sources of density $s$ (where $\nabla \cdot \mathbf{v} = 4\pi s$), the equation becomes:

$$\nabla \cdot \left(-\frac{1}{k} \nabla p\right) = 4\pi s \implies \nabla^2 p = -4\pi k s \quad \text{(Poisson's equation)}$$

**Interpretation:** The potential $p$ satisfies Laplace's equation where no sources exist. Sources create a local curvature in the potential field, with the magnitude of the curvature scaled by the resistance $k$ of the medium. In the electromagnetic analogues, this becomes:

*   **Electrostatics:** $\nabla \cdot (\sigma \nabla \phi) = -4\pi \rho$ (for non-uniform conductivity).
*   **Magnetostatics:** $\nabla^2 \Omega = -4\pi m$ (where $m$ is the magnetic pole density, with the scaling $k = 1/\mu$ if mapping to $\mathbf{B}$).

#### 4. The Potential Function and Its Geometric Meaning

Maxwell defines the potential function $p$ such that:

*   The **difference in potential** between two points is the work done (per unit volume of fluid) against the resistance in moving from one point to the other.
*   The **equipotential surfaces** are surfaces of constant $p$; no flow occurs across them.
*   The **streamlines** cross equipotential surfaces orthogonally, representing the paths of steepest descent of the potential.

This is the direct geometric analogue of the electrostatic potential $\phi$: equipotential surfaces are surfaces of constant voltage, and electric field lines cross them orthogonally.

---

### Pre-Reading Checklist for Phase 2

Before proceeding to the active reading of Maxwell's text on fundamental quantities, the reader should confirm:

- [ ] The distinction between **intensity** ($-\nabla p$) and **quantity** ($\mathbf{v}$) is clearly understood at both the local and global levels.
- [ ] The geometric construction of the **unit flow tube** (carrying a unit of flux $dQ = 1$) is visualized.
- [ ] The 3D **unit cell** (bounded by the tube and two equipotentials with potential drop $dp=1$) is understood.
- [ ] The geometric aspect-ratio relations ($ds = k \, dn$ in 2D and $dA = k \, dn$ in 3D) are internalized.
- [ ] Laplace's equation $\nabla^2 p = 0$ and Poisson's equation $\nabla^2 p = -4\pi k s$ are recognized as the governing differential equations for the potential.
- [ ] The resistance factor $k$ in Poisson's equation is understood as scaling the source strength relative to the medium's resistance.

---

### Connection to the Rest of the Exegesis

*   **Phase 2 (Active Reading):** The reader will encounter Maxwell's explicit definitions of the "unit flow tube" and the "unit cell." The terminology mapping above will guide the translation of his 19th-century geometric language.
*   **Phase 3 (Mathematical Formalization):** After reading, the reader will formalize the divergence theorem in the context of the unit flow tube and derive the integral form of flux conservation. The distinction between local (differential) and global (integral) quantities will be expressed using the divergence theorem.
*   **Phase 4 (Computational Visualization):** The reader will generate 2D and 3D representations of unit flow tubes bounded by streamlines, visualizing how flux is conserved along the tube and how the tube cross-section changes in regions of varying field intensity.

----


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
| $p$ | Pressure (scalar potential) | $p$ (scalar) | Electric Potential $\phi$ | Magnetic Potential $\Omega$ |
| $k$ | Resistance of the medium | $k$ (scalar) | Resistivity $1/\sigma$ | Reluctivity $1/\mu$ |
| $-\frac{\partial p}{\partial x}$, etc. | Negative potential gradient | $-\nabla p$ | Electric Field $\mathbf{E}$ | Magnetic Intensity $\mathbf{H}$ |
| $dQ$ | Unit flux element | $dQ$ | Unit current element $dI$ | Unit flux element $d\Phi$ |
| $ds$ | Streamline spacing | $ds$ | Streamline spacing | Streamline spacing |
| $dn$ | Equipotential spacing | $dn$ | Equipotential spacing | Equipotential spacing |

**Step 3: Convert to Modern Vector Notation**

Rewrite the component equations as a single vector equation using the operators $\nabla$, $\cdot$, and $\times$.

**Step 4: State the Physical Meaning in Modern English**

Articulate the physical meaning of the translated equation in clear, modern language, with explicit acknowledgment of the dual-layered analogical framework and the geometric normalization conditions.

---

### Component-to-Vector Translation

#### Translation 1: Flux Through a Surface

**Step 1: Maxwell's Original Component Equations**

In Part I, Section 2, Maxwell defines the total flux $Q$ through a surface $S$ as the integral of the normal component of velocity [2]:

$$Q = \iint_S (u \, dy \, dz + v \, dz \, dx + w \, dx \, dy)$$

**Step 2: Identify the Modern Physical Quantities**

| Maxwell's Symbol | Physical Quantity | Modern Symbol | Electrostatic Analog | Magnetostatic Analog |
| :--- | :--- | :--- | :--- | :--- |
| $u, v, w$ | Fluid velocity components | $\mathbf{v} = (u, v, w)$ | Current Density $\mathbf{J}$ | Magnetic Induction $\mathbf{B}$ |
| $dy \, dz$, etc. | Area elements | $d\mathbf{S} = (dS_x, dS_y, dS_z)$ | Area element $d\mathbf{S}$ | Area element $d\mathbf{S}$ |
| $Q$ | Total flux | $Q$ | Total Current $I$ | Magnetic Flux $\Phi$ |

**Step 3: Convert to Modern Vector Notation**

The surface integral is written compactly in modern notation as:

$$Q = \iint_S \mathbf{v} \cdot d\mathbf{S}$$

**Step 4: State the Physical Meaning in Modern English**

The total flux $Q$ through a surface $S$ is the integral of the normal component of the velocity field $\mathbf{v}$ over the surface. 
*   **Conduction Mapping:** This represents the total electric current $I = \iint_S \mathbf{J} \cdot d\mathbf{S}$ flowing through a conducting cross-section.
*   **Magnetostatic Mapping:** This represents the total magnetic flux $\Phi = \iint_S \mathbf{B} \cdot d\mathbf{S}$ passing through the surface.

---

#### Translation 2: The Unit Flow Tube and Flux Conservation

**Step 1: Maxwell's Original Component Equations**

For a unit flow tube (a bundle of streamlines carrying unit flux), Maxwell states that the flux through any cross-section is constant [2]:

$$dQ = u \, dy \, dz + v \, dz \, dx + w \, dx \, dy = \text{constant along the tube}$$

In terms of the constitutive relation, this becomes:

$$dQ = -\frac{1}{k} \left( \frac{\partial p}{\partial x} \, dy \, dz + \frac{\partial p}{\partial y} \, dz \, dx + \frac{\partial p}{\partial z} \, dx \, dy \right)$$

**Step 2: Identify the Modern Physical Quantities**

| Maxwell's Symbol | Physical Quantity | Modern Symbol | Electrostatic Analog | Magnetostatic Analog |
| :--- | :--- | :--- | :--- | :--- |
| $dQ$ | Unit flux element | $dQ$ | Unit current element $dI$ | Unit flux element $d\Phi$ |
| $\mathbf{v}$ | Fluid velocity | $\mathbf{v}$ | Current Density $\mathbf{J}$ | Magnetic Induction $\mathbf{B}$ |
| $p$ | Pressure potential | $p$ | Potential $\phi$ | Potential $\Omega$ |
| $k$ | Resistance of the medium | $k$ | Resistivity $1/\sigma$ | Reluctivity $1/\mu$ |

**Step 3: Convert to Modern Vector Notation**

The flux through a cross-section of the tube is:

$$dQ = \iint_{S_{\text{cross}}} \mathbf{v} \cdot d\mathbf{S} = -\frac{1}{k} \iint_{S_{\text{cross}}} \nabla p \cdot d\mathbf{S}$$

Flux conservation along the length of the tube is expressed as:

$$\frac{\partial (dQ)}{\partial s} = 0 \quad \text{(along the tube)}$$

where $s$ is the coordinate parameterizing the streamline curve.

**Step 4: State the Physical Meaning in Modern English**

A unit flow tube is a bundle of streamlines carrying a constant flux $dQ = 1$. The total flux through any arbitrary cross-section of this tube is invariant along its length, which is a direct mathematical consequence of the divergence-free condition $\nabla \cdot \mathbf{v} = 0$. 
*   **Conduction Mapping:** Maps to a "unit current tube" carrying a constant current $dI$.
*   **Magnetostatic Mapping:** Maps to a "unit flux tube" carrying a constant magnetic flux $d\Phi$. This invariance represents the continuous, closed-loop topology of magnetic induction lines.

---

#### Translation 3: The Unit Cell and the Aspect Ratio ($ds = k \, dn$ and $dA = k \, dn$)

**Step 1: Maxwell's Original Component Equations**

In a 2D planar geometry, Maxwell defines the unit cell as the region bounded by two adjacent streamlines (separated by distance $ds$) and two adjacent equipotential surfaces (separated by potential difference $dp$). The local flux is formulated as [2]:

$$dQ = |\mathbf{v}| \, ds = \frac{1}{k} |-\nabla p| \, ds = \frac{1}{k} \frac{dp}{dn} \, ds$$

where $dn$ is the spacing between equipotential surfaces.

**Step 2: Identify the Modern Physical Quantities**

| Maxwell's Symbol | Physical Quantity | Modern Symbol | Electrostatic Analog | Magnetostatic Analog |
| :--- | :--- | :--- | :--- | :--- |
| $dQ$ | Unit flux element | $dQ$ | Unit current element $dI$ | Unit flux element $d\Phi$ |
| $ds$ | Streamline spacing | $ds$ | Streamline spacing | Streamline spacing |
| $dn$ | Equipotential spacing | $dn$ | Equipotential spacing | Equipotential spacing |
| $dp$ | Potential difference | $dp$ | Potential difference $d\phi$ | Potential difference $d\Omega$ |
| $k$ | Resistance of the medium | $k$ | Resistivity $1/\sigma$ | Reluctivity $1/\mu$ |

**Step 3: Convert to Modern Vector Notation**

##### Planar (2D) Formulation
The flux through a 2D unit cell of unit depth is:
$$dQ = \frac{1}{k} \frac{dp}{dn} \, ds$$
Applying the unit normalizations $dQ = 1$ and $dp = 1$ yields:
$$1 = \frac{1}{k} \frac{1}{dn} \, ds \implies ds = k \, dn$$

##### Spatial (3D) Formulation
In physical 3D space, a unit cell is a volume segment of a unit flow tube (cross-sectional area $dA$) bounded by two equipotential surfaces (spacing $dn$). The unit flux relation is formulated as:
$$dQ = \frac{1}{k} \frac{dp}{dn} \, dA \implies 1 = \frac{1}{k} \frac{1}{dn} \, dA \implies dA = k \, dn$$
The differential volume $dV$ of this 3D unit cell is:
$$dV = dA \cdot dn = k \, (dn)^2$$

**Step 4: State the Physical Meaning in Modern English**

The aspect ratio and volumetric scaling of a unit cell are determined directly by the medium's local resistance $k$:
*   **In 2D Space:** The streamline spacing $ds$ equals the equipotential spacing $dn$ scaled by $k$ ($ds = k \, dn$). If the medium is uniform and has unit resistance ($k=1$), **the unit cells are mathematically perfect squares ($ds = dn$)** [1]. If $k$ varies, the cells distort into rectangles.
*   **In 3D Space:** The tube cross-sectional area scales as $dA = k \, dn$. If $k=1$, the area equals the cell's length ($dA = dn$), and the cell's volume scales quadratically with the equipotential spacing ($dV = (dn)^2$). This geometric scaling allows the physical properties of the medium ($k$) to be encoded directly into the shape of the field cells.

---

#### Translation 4: Laplace's Equation from Flux Conservation

**Step 1: Maxwell's Original Component Equations**

Combining the constitutive relation $u = -\frac{1}{k}\frac{\partial p}{\partial x}$, etc., with the continuity equation (incompressibility) in source-free regions [2]:

$$\frac{\partial}{\partial x} \left( \frac{1}{k} \frac{\partial p}{\partial x} \right) + \frac{\partial}{\partial y} \left( \frac{1}{k} \frac{\partial p}{\partial y} \right) + \frac{\partial}{\partial z} \left( \frac{1}{k} \frac{\partial p}{\partial z} \right) = 0$$

For a uniform medium ($k = \text{constant}$), this simplifies to:

$$\frac{\partial^2 p}{\partial x^2} + \frac{\partial^2 p}{\partial y^2} + \frac{\partial^2 p}{\partial z^2} = 0$$

**Step 2: Identify the Modern Physical Quantities**

| Maxwell's Symbol | Physical Quantity | Modern Symbol | Electrostatic Analog | Magnetostatic Analog |
| :--- | :--- | :--- | :--- | :--- |
| $p$ | Pressure potential | $p$ | Potential $\phi$ | Potential $\Omega$ |
| $k$ | Resistance of the medium | $k$ | Resistivity $1/\sigma$ | Reluctivity $1/\mu$ |
| $\frac{\partial^2 p}{\partial x^2} + \dots$ | Laplacian of potential | $\nabla^2 p$ | Laplacian $\nabla^2 \phi$ | Laplacian $\nabla^2 \Omega$ |

**Step 3: Convert to Modern Vector Notation**

For a uniform medium, Laplace's equation is:
$$\nabla^2 p = 0$$
For a non-uniform medium, the general divergence form is:
$$\nabla \cdot \left( \frac{1}{k} \nabla p \right) = 0$$

**Step 4: State the Physical Meaning in Modern English**

In source-free regions of a uniform medium, the potential $p$ satisfies Laplace's equation. The potential is harmonic, with no local extrema in the interior.
*   **Topological Caveat:** This local relation holds in any source-free region. However, if the region is multiply connected (e.g., enclosing a line current singularity as derived in Section 5), the global potential becomes a multi-valued function of angle ($p(\phi) = -k\frac{\Gamma}{2\pi}\phi + p_0$), meaning the global field is non-conservative ($\oint \nabla p \cdot d\mathbf{l} \neq 0$).

---

#### Translation 5: Poisson's Equation (Sources Present)

**Step 1: Maxwell's Original Component Equations**

In regions containing fluid sources of density $s$, the continuity equation is generalized to [2]:

$$\frac{\partial u}{\partial x} + \frac{\partial v}{\partial y} + \frac{\partial w}{\partial z} = 4\pi s$$

Substituting the constitutive relation $u = -\frac{1}{k}\frac{\partial p}{\partial x}$, etc., and assuming $k$ is uniform:

$$-\frac{1}{k} \left( \frac{\partial^2 p}{\partial x^2} + \frac{\partial^2 p}{\partial y^2} + \frac{\partial^2 p}{\partial z^2} \right) = 4\pi s$$

**Step 2: Identify the Modern Physical Quantities**

| Maxwell's Symbol | Physical Quantity | Modern Symbol | Electrostatic Analog | Magnetostatic Analog |
| :--- | :--- | :--- | :--- | :--- |
| $p$ | Pressure potential | $p$ | Potential $\phi$ | Potential $\Omega$ |
| $k$ | Resistance of the medium | $k$ | Resistivity $1/\sigma$ | Reluctivity $1/\mu$ |
| $s$ | Source density | $s$ | Charge density $\rho$ | Pole density $m$ |

**Step 3: Convert to Modern Vector Notation**

The component equation is written compactly as:
$$\nabla^2 p = -4\pi k s$$
For a non-uniform medium, the general form is:
$$\nabla \cdot \left( \frac{1}{k} \nabla p \right) = -4\pi s$$

**Step 4: State the Physical Meaning in Modern English**

In regions containing sources, the potential satisfies Poisson's equation. The source density $s$ creates a local curvature in the potential field, with the magnitude of the curvature scaled by the medium's resistance $k$.
*   **Conduction Mapping:** Maps to the unrationalized Poisson equation for electric potential in a conducting medium: $\nabla^2 \phi = -4\pi \frac{\rho}{\sigma} = -4\pi k \rho$.
*   **Modern SI Comparison (Rationalized vs. Unrationalized):** In modern rationalized SI units, the electrostatic Poisson equation is written without the $4\pi$ factor: $\nabla^2 \phi = -\rho / \epsilon$. The explicit $4\pi$ factor in Maxwell's equation is a direct consequence of the unrationalized ESU/Gaussian unit systems of the 19th century [1, 2].

---

### Standardized Commentary Block

*   **The Goal:** Maxwell's objective in Section 2 is to define the geometric constructs—the unit flow tube and the unit cell—that translate the continuous field quantities of the fluid model into a discrete, quantifiable geometric framework. This provides a visual and mathematical language for Faraday's lines of force.
*   **The Method:** Maxwell introduces the concepts of the **unit flow tube** ($dQ = 1$) and the **unit cell** ($dp = 1$). By imposing these normalizations and applying the constitutive relation $\mathbf{v} = -\frac{1}{k}\nabla p$, he derives the exact aspect ratio of the cells: in 2D, $ds = k \, dn$; in 3D, $dA = k \, dn$. This encodes the medium's resistance directly into the geometry of the field.
*   **The Limitation:** The geometric framework of Section 2 is restricted to **steady-state, source-free** (or simply sourced) configurations in uniform or piecewise-uniform media. It does not address time-varying fields, electromagnetic induction, or the propagation of waves.
*   **The Legacy:** The concepts of unit flow tubes and unit cells established the visual language of field line topology and laid the groundwork for the mathematical treatment of flux, intensity, and potential in all subsequent field theories.

---

### Exegesis Workflow Callout

Before proceeding to Phase 4 (Visualization), the reader must execute the **Post-Reading Reconciliation Protocol (Section 1.2.2)**:
1.  Verify that your customized glossary entries in Appendix A align with the dual-layered mappings derived in this section, particularly the geometric definitions of the unit flow tube and unit cell.
2.  Audit your Cartesian-to-vector derivations against the **Zone 2 Quality Control Check (Section 1.2.1)** to ensure:
    *   The aspect-ratio relations ($ds = k \, dn$ in 2D and $dA = k \, dn$ in 3D) are correctly derived.
    *   The unrationalized $4\pi$ factor in Poisson's equation is properly distinguished from the modern rationalized SI form.
    *   The topological constraint of multiply connected domains is recognized when evaluating Laplace's equation.

---

### Connections to Later Papers

| Concept in Paper 1 | Later Development |
| :--- | :--- |
| Unit flow tube ($dQ = 1$) | **Paper 2 (1861):** The concept of flux tubes is retained in the molecular vortex model, with vortices forming continuous tubes of magnetic induction. |
| Aspect ratio $ds = k \, dn$ | **Paper 2 (1861):** The geometry of the unit cell is reinterpreted in terms of the directional mechanical stress transmitted by the rotating vortices. |
| $\nabla \cdot \mathbf{v} = 0$ (Flux conservation) | **Paper 3 (1865):** Generalized to $\nabla \cdot \mathbf{B} = 0$, one of Maxwell's fundamental field equations. |
| Laplace's equation $\nabla^2 p = 0$ | **Paper 3 (1865):** Retained as the equation for the electrostatic potential in charge-free regions. |
| Poisson's equation $\nabla^2 p = -4\pi k s$ | **Paper 3 (1865):** Generalizes to $\nabla^2 \phi = -4\pi \frac{\rho}{\epsilon}$ for electrostatics and $\nabla^2 \mathbf{A} = -\frac{4\pi}{k}\mathbf{J}$ for the vector potential. |

---

### References Integration Callout

#### The Treatise on Electricity and Magnetism (1873)

The following articles of Maxwell's *Treatise* (1873) provide direct commentary on the geometric constructs of Section 2:

| *Treatise* Article | Connection to Section 2 |
| :--- | :--- |
| **Articles 71–75** | Maxwell's discussion of the "unit tube" and "unit cell" in the context of electric and magnetic fields [2]. |
| **Article 72** | The definition of the "quantity of flow" and the "intensity of flow" in geometric terms [2]. |
| **Article 74** | The aspect ratio of the unit cell and its relation to the properties of the medium [2]. |
| **Article 75** | The application of the unit cell geometry to the calculation of forces between lines of force [2]. |

#### Heaviside's Electromagnetic Theory (1893)

Heaviside's vector reformulations provide a modern perspective on the geometric constructs of Section 2:

| Heaviside Section | Connection to Section 2 |
| :--- | :--- |
| **Volume I, Chapter 3** | Heaviside's discussion of flux and intensity in vector notation [3]. |
| **Volume I, Chapter 4** | The geometric interpretation of divergence and curl in terms of flux tubes and circulation [3]. |
| **Volume II, Chapter 7** | Historical commentary on Maxwell's use of geometric constructs in the fluid analogy [3]. |

---

### References

[1] Bork, A. M. (1966). Physics just before Einstein. *Science*, 152(3722), 597–603.

[2] Maxwell, J. C. (1873). *A Treatise on Electricity and Magnetism*. Oxford: Clarendon Press.

[3] Heaviside, O. (1893). *Electromagnetic Theory*. London: The Electrician Printing and Publishing Company.

