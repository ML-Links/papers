# Appendix A: Glossary of 19th-Century Terminology

```yaml
---
lifecycle_status:
  zone: "Zone 1 (Static Infrastructure)"
  completeness: "85%"
  pending_tasks:
    - "Extract and define localized contextual terms during Phase 2 Active Textual Analysis."
    - "Verify mathematical mappings of Section 4 lateral and longitudinal stresses against Maxwell's original derivations."
    - "Cross-reference all entries with the Post-Reading Reconciliation Step (Section 1.2.2)."
---
```

---

## Overview

This glossary provides a comprehensive alphabetical reference translating Maxwell's 19th-century terminology into modern vector calculus and electromagnetic equivalents. Terms are organized by their primary occurrence in Part I or Part II of Paper 1, with cross-references to the relevant sections.

The glossary serves two purposes:
1. **During Reading:** The reader can quickly look up unfamiliar terms encountered in Maxwell's text.
2. **During Translation:** The reader can confirm the modern equivalent when applying the Translation Protocol in Phase 3.

**Lifecycle Note:** This glossary is 85% complete. The remaining 15% consists of localized contextual terms that will only be identified during the Phase 2 Active Textual Analysis. Placeholder rows have been included to represent these pending entries.

---

## Alphabetical Glossary

| Maxwell's 19th-Century Term | Modern Equivalent | Primary Occurrence | Definition / Notes |
| :--- | :--- | :--- | :--- |
| **Electromotive intensity** | Electric field intensity ($\mathbf{E}$) | Part I, Section 3 | The force per unit charge at a point in the field. In Paper 1, Maxwell uses this term to describe the force that drives electric currents. |
| **Electro-tonic intensity** | Vector potential ($\mathbf{A}$) | Part II, Section 1 | The vector quantity whose curl gives the magnetic induction. Maxwell viewed this as the fundamental physical quantity of his theory. |
| **Electro-tonic state** | Vector potential ($\mathbf{A}$) | Part II, Section 1 | The physical state of tension or strain in the medium that gives rise to electromagnetic forces. The precursor to the vector potential. |
| **Intensity of a force** | Field strength ($\mathbf{E}$ or $\mathbf{H}$) | Part I, Section 2 | The force per unit source (charge or pole) at a point. Distinguished from "quantity" in Maxwell's theory. |
| **Lines of force** | Field lines | Throughout | Curves that are everywhere tangent to the field vector at every point. Faraday's qualitative geometry translated into mathematical physics. |
| **Magnetic force** | Magnetic field intensity ($\mathbf{H}$) | Part I, Section 1 | The force per unit pole at a point in the magnetic field. |
| **Quantity of induction** | Flux ($\Phi$) or flux density ($\mathbf{B}$) | Part I, Section 2 | The total amount of field passing through a surface. Distinguished from "intensity" in Maxwell's theory. **Note:** This term must **not** be mapped to electric displacement ($\mathbf{D}$) in Paper 1, as displacement was not formulated until Maxwell's 1861 paper, *On Physical Lines of Force*. |
| **Sources** | Positive charges ($+q$) | Part I, Section 1 | Points where field lines begin ($\nabla \cdot \mathbf{E} > 0$). In the fluid analogy, sources correspond to positive charges. |
| **Sinks** | Negative charges ($-q$) | Part I, Section 1 | Points where field lines end ($\nabla \cdot \mathbf{E} < 0$). In the fluid analogy, sinks correspond to negative charges. |
| **Unit flow tube** | Flux tube | Part I, Section 2 | A region bounded by field lines where the total flux is constant. The geometric building block of Maxwell's field theory. |

---

## Glossary by Section

### Part I: Theory of the Motion of an Incompressible Fluid

| Section | Term | Definition |
| :--- | :--- | :--- |
| **Section 1** | Fluid velocity ($\mathbf{v}$) | The velocity of the fluid at a point; maps to magnetic intensity ($\mathbf{H}$) or current density ($\mathbf{J}$) depending on the layer of the analogy. |
| **Section 1** | Pressure ($p$) | The scalar pressure of the fluid; maps to electric potential ($\phi$). |
| **Section 1** | Resistance coefficient ($k$) | The permeability of the medium; maps to permeability ($\mu$) or conductivity ($\sigma$). |
| **Section 1** | Sources | Points where fluid is created; maps to positive electric charges. |
| **Section 1** | Sinks | Points where fluid is destroyed; maps to negative electric charges. |
| **Section 2** | Intensity of a force | The force per unit source; maps to field strength ($\mathbf{E}$ or $\mathbf{H}$). |
| **Section 2** | Quantity of induction | The total flux through a surface; maps to magnetic flux ($\Phi$) or flux density ($\mathbf{B}$). |
| **Section 2** | Unit flow tube | A region bounded by streamlines with constant flux. |
| **Section 2** | Unit cell | The intersection of unit flow tubes and equipotential surfaces. |
| **Section 3** | Circulation | The line integral of a vector field around a closed loop. |
| **Section 3** | Vortex filaments | The rotational elements in the fluid; maps to current density ($\mathbf{J}$). |
| **Section 4** | Lateral pressure | The pressure perpendicular to lines of force. |
| **Section 4** | Longitudinal tension | The tension along lines of force. |
| **Section 5** | *[Phase 2 Placeholder]* | *Contextual terms to be identified during active reading. For example: specific geometric terms, boundary condition nomenclature, or descriptive terminology for the solenoid and wire configurations.* |

### Part II: On Faraday's "Electro-tonic State"

| Section | Term | Definition |
| :--- | :--- | :--- |
| **Section 1** | Electro-tonic state | The physical state of tension in the medium. |
| **Section 1** | Electro-tonic intensity ($\mathbf{A}$) | The vector quantity representing the electro-tonic state; maps to vector potential. |
| **Section 2** | Magnetic induction ($\mathbf{B}$) | The curl of the electro-tonic intensity; maps to magnetic flux density. |
| **Section 3** | Electromotive force (EMF) | The force that drives electric currents; derived from the time variation of $\mathbf{A}$. |
| **Section 4** | *[Phase 2 Placeholder]* | *Contextual terms to be identified during active reading. For example: terms related to Maxwell's concluding remarks, his synthesis of the two circuit laws, or his discussion of the conservation of magnetic lines of force.* |
