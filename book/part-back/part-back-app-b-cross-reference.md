# Appendix B: Cross-Reference Mapping

```yaml
---
lifecycle_status:
  zone: "Zone 1 (Static Infrastructure)"
  completeness: "90%"
  pending_tasks:
    - "Audit exact Treatise article numbers against completed Phase 3 mathematical translations."
    - "Verify Heaviside vector identities align with Appendix D implementations."
    - "Cross-reference all mappings during the Post-Reading Reconciliation Step (Section 1.2.2)."
---
```

---

## Overview

This appendix provides cross-references between Paper 1 and two major supplementary texts:

1. **Maxwell's *Treatise on Electricity and Magnetism* (1873):** The mature, pedagogical presentation of the electromagnetic theory. The *Treatise* refines and clarifies the ideas first presented in Paper 1.

2. **Heaviside's *Electromagnetic Theory* (1893):** The reformulation of Maxwell's component equations into the four modern vector equations. Heaviside discards the fluid analogy entirely and treats the field quantities ($\mathbf{E}, \mathbf{H}, \mathbf{D}, \mathbf{B}$) as primary. He famously criticized the vector potential $\mathbf{A}$ as "metaphysical clutter" [4].

The integration notes specify exactly when to consult these sources during the exegesis.

---

## B.1 Mapping to Maxwell's *Treatise* (1873)

| Paper 1 Section | Treatise Articles | Purpose | When to Consult |
| :--- | :--- | :--- | :--- |
| **Part I, Section 1** (Fluid Analogy) | Articles 65–70 | Mature treatment of the fluid analogy and the mapping between fluid and field quantities. | After completing Phase 2 (Active Textual Analysis) of Section 1. |
| **Part I, Section 2** (Fundamental Quantities) | Articles 71–78 | General theorems on potentials and the distinction between intensity and quantity. | After completing Phase 3 (Mathematical Formalization) of Section 2. |
| **Part I, Section 3** (Circuit Laws) | Articles 528–535 | The general equations of induction and the vector potential. | After completing Phase 3 (Mathematical Formalization) of Section 3. |
| **Part I, Section 4** (Forces) | Articles 641–646 | The Maxwell stress tensor and the mechanical forces in the field. | After completing Phase 3 (Mathematical Formalization) of Section 4. |
| **Part I, Section 5** (Applications) | Articles 700–710 | Calculation of induction coefficients and practical applications. | After completing Phase 3 (Mathematical Formalization) of Section 5. |
| **Part II, Section 1** (Electro-tonic State) | Articles 405–410 | Mature definition of the vector potential and electromagnetic momentum. | After completing Phase 2 (Active Textual Analysis) of Part II, Section 1. |
| **Part II, Section 2** (Mathematical Formulation) | Articles 590–600 | The general equations of the electromagnetic field in their mature form. | After completing Phase 3 (Mathematical Formalization) of Part II, Section 2. |
| **Part II, Section 3** (Induction) | Articles 541–544 | Faraday's law in its mature form. | After completing Phase 3 (Mathematical Formalization) of Part II, Section 3. |
| **Overall Synthesis** | Articles 1–10 | Maxwell's mature definition of the electromagnetic field as a primary physical entity. | After completing Part II, Section 4 (Synthesis). |

---

## B.2 Mapping to Heaviside's *Electromagnetic Theory* (1893)

| Paper 1 Concept | Heaviside's Reformulation | Purpose | When to Consult |
| :--- | :--- | :--- | :--- |
| **Fluid analogy (all of Part I)** | Heaviside treats $\mathbf{E}, \mathbf{H}, \mathbf{D}, \mathbf{B}$ as primary field quantities, discarding the fluid analogy entirely. | To see how the fluid analogy was historically abandoned and replaced by a purely field-theoretic approach. | After completing Part I, Section 5 (Applications). |
| **Electro-tonic intensity ($\mathbf{A}$)** | Heaviside defines the curl relation $\mathbf{B} = \nabla \times \mathbf{A}$ but actively discourages the physical use of the potential, calling it "metaphysical clutter" and an obstacle to physical clarity [4]. He argued that physics should focus directly on the physical fields $\mathbf{E}$ and $\mathbf{H}$. | To understand the historical debate surrounding potentials vs. physical fields, and to translate component equations into modern curl notation. | After completing Part II, Section 2 (Mathematical Formulation). |
| **Intensity vs. Quantity** | Heaviside formalizes the distinction as $\mathbf{D}$ vs. $\mathbf{E}$ and $\mathbf{B}$ vs. $\mathbf{H}$. | To clarify the distinction in modern terms. | After completing Part I, Section 2 (Fundamental Quantities). |
| **Circuit Laws (Theorems I and II)** | Heaviside reduces Maxwell's twenty component equations to four vector equations: | To see the modern, symmetric form of Maxwell's equations. | After completing Part II, Section 4 (Synthesis). |
| | $\nabla \cdot \mathbf{D} = \rho$ | |
| | $\nabla \cdot \mathbf{B} = 0$ | |
| | $\nabla \times \mathbf{E} = -\partial \mathbf{B}/\partial t$ | |
| | $\nabla \times \mathbf{H} = \mathbf{J} + \partial \mathbf{D}/\partial t$ | |

---

## B.3 Integration Notes

### When to Consult the *Treatise*

| Stage of Exegesis | Articles to Consult | Purpose |
| :--- | :--- | :--- |
| **After Phase 2** (Active Textual Analysis) of a section | The corresponding *Treatise* articles listed in B.1 | To clarify Maxwell's original argument with his mature, pedagogical presentation. |
| **After Phase 3** (Mathematical Formalization) of a section | The corresponding *Treatise* articles listed in B.1 | To confirm the mathematical translation and physical interpretation. |
| **During Post-Reading Reconciliation** (Section 1.2.2) | All relevant articles | To verify that your customized glossary entries and mathematical translations align with the mature definitions and formulations. |
| **After completing the entire paper** | Articles 1–10 | To see Maxwell's mature definition of the field. |

### When to Consult Heaviside

| Stage of Exegesis | Purpose |
| :--- | :--- |
| **After completing Part I** | To understand how the fluid analogy was historically discarded. |
| **After completing Part II, Section 2** | To trace the conceptual origins of why modern physics marginalized the vector potential in favor of direct fields, and to understand Heaviside's critique of $\mathbf{A}$ as "metaphysical clutter." |
| **After completing the entire paper** | To see the reduction of Maxwell's twenty equations to four vector equations. |

### General Guidelines

1. **Do not consult supplementary texts before completing the original reading.** The goal is to engage with Maxwell's original reasoning first, then use the *Treatise* and Heaviside to clarify and confirm.

2. **Use the *Treatise* for clarification.** If a passage is unclear, consult the corresponding *Treatise* article. Maxwell's mature presentation is often clearer than his exploratory 1855 text.

3. **Use Heaviside for translation.** Heaviside's vector notation is closer to modern conventions. Use his reformulation to check the Translation Protocol in Phase 3.

4. **During Post-Reading Reconciliation (Section 1.2.2),** explicitly cross-reference this appendix to ensure all mappings are accurate and complete.

