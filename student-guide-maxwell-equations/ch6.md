# Appendix: Maxwell's Equations in matter

Maxwell's Equations as presented in Chapters 1-4 apply to electric and magnetic fields in matter as well as in free space. However, when you're dealing with fields inside matter, remember the following points:

- The enclosed charge in the integral form of Gauss's law for electric fields (and current density in the differential form) includes ALL charge - bound as well as free.
- The enclosed current in the integral form of the Ampere-Maxwell law (and volume current density in the differential form) includes ALL currents - bound and polarization as well as free.

Since the bound charge may be difficult to determine, in this Appendix you'll find versions of the differential and integral forms of Gauss's law for electric fields that depend only on the free charge. Likewise, you'll find versions of the differential and integral form of the Ampere-Maxwell law that depend only on the free current.

What about Gauss's law for magnetic fields and Faraday's law? Since those laws don't directly involve electric charge or current, there's no need to derive more "matter friendly" versions of them.

**Gauss's law for electric fields:** Within a dielectric material, positive and negative charges may become slightly displaced when an electric field is applied. When a positive charge $Q$ is separated by distance $s$ from an equal negative charge $-Q$, the electric "dipole moment" is given by

$$
\vec{p} = Q\vec{s}, \tag{A.1}
$$

where $\vec{s}$ is a vector directed from the negative to the positive charge with magnitude equal to the distance between the charges. For a dielectric material with $N$ molecules per unit volume, the dipole moment per unit volume is

$$
\vec{P} = N\vec{p}, \tag{A.2}
$$

a quantity which is also called the "electric polarization" of the material. If the polarization is uniform, bound charge appears only on the surface of the material. But if the polarization varies from point to point within the dielectric, there are accumulations of charge within the material, with volume charge density given by

$$
\rho_b = -\vec{\nabla} \circ \vec{P}, \tag{A.3}
$$

where $\rho_b$ represents the volume density of bound charge (charge that's displaced by the electric field but does not move freely through the material).

What is the relevance of this to Gauss's law for electric fields? Recall that in the differential form of Gauss's law, the divergence of the electric field is

$$
\vec{\nabla} \circ \vec{E} = \frac{\rho}{\varepsilon_0},
$$

where $\rho$ is the total charge density. Within matter, the total charge density consists of both free and bound charge densities:

$$
\rho = \rho_f + \rho_b, \tag{A.4}
$$

where $\rho$ is the total charge density, $\rho_f$ is the free charge density, and $\rho_b$ is the bound charge density. Thus, Gauss's law may be written as

$$
\vec{\nabla} \circ \vec{E} = \frac{\rho}{\varepsilon_0} = \frac{\rho_f + \rho_b}{\varepsilon_0}. \tag{A.5}
$$

Substituting the negative divergence of the polarization for the bound charge and multiplying through by the permittivity of free space gives

$$
\vec{\nabla} \circ \varepsilon_0\vec{E} = \rho_f + \rho_b = \rho_f - \vec{\nabla} \circ \vec{P}, \tag{A.6}
$$

or

$$
\vec{\nabla} \circ \varepsilon_0\vec{E} + \vec{\nabla} \circ \vec{P} = \rho_f. \tag{A.7}
$$

Collecting terms within the divergence operator gives

$$
\vec{\nabla} \circ (\varepsilon_0\vec{E} + \vec{P}) = \rho_f. \tag{A.8}
$$

In this form of Gauss's law, the term in parentheses is often written as a vector called the "displacement," which is defined as

$$
\vec{D} = \varepsilon_0\vec{E} + \vec{P}. \tag{A.9}
$$

Substituting this expression into equation (A.8) gives

$$
\vec{\nabla} \circ \vec{D} = \rho_f, \tag{A.10}
$$

which is a version of the differential form of Gauss's law that depends only on the density of free charge.

Using the divergence theorem gives the integral form of Gauss's law for electric fields in terms of the flux of the displacement and enclosed free charge:

$$
\int_S \vec{D} \circ \hat{n}\,da = q_{\mathrm{free,\ enc}}. \tag{A.11}
$$

What is the physical significance of the displacement $\vec{D}$? In free space, the displacement is a vector field proportional to the electric field - pointing in the same direction as $\vec{E}$ and with magnitude scaled by the vacuum permittivity. But in polarizable matter, the displacement field may differ significantly from the electric field. You should note, for example, that the displacement is not necessarily irrotational - it will have curl if the polarization does, as can be seen by taking the curl of both sides of Equation A.9.

The usefulness of $\vec{D}$ comes about in situations for which the free charge is known and for which symmetry considerations allow you to extract the displacement from the integral of Equation A.11. In those cases, you may be able to determine the electric field within a linear dielectric material by finding $\vec{D}$ on the basis of the free charge and then dividing by the permittivity of the medium to find the electric field.

**The Ampere-Maxwell law:** Just as applied electric fields induce polarization (electric dipole moment per unit volume) within dielectrics, applied magnetic fields induce "magnetization" (magnetic dipole moment per unit volume) within magnetic materials. And just as bound electric charges act as the source of additional electric fields within the material, bound currents may act as the source of additional magnetic fields. In that case, the bound current density is given by the curl of the magnetization:

$$
\vec{J}_b = \vec{\nabla} \times \vec{M}. \tag{A.12}
$$

where $\vec{J}_b$ is the bound current density and $\vec{M}$ represents the magnetization of the material.

Another contribution to the current density within matter comes from the time rate of change of the polarization, since any movement of charge constitutes an electric current. The polarization current density is given by

$$
\vec{J}_P = \frac{\partial \vec{P}}{\partial t}. \tag{A.13}
$$

Thus, the total current density includes not only the free current density, but the bound and polarization current densities as well:

$$
\vec{J} = \vec{J}_f + \vec{J}_b + \vec{J}_P. \tag{A.14}
$$

Thus, the Ampere-Maxwell law in differential form may be written as

$$
\vec{\nabla} \times \vec{B} = \mu_0\left(\vec{J}_f + \vec{J}_b + \vec{J}_P + \varepsilon_0\frac{\partial \vec{E}}{\partial t}\right). \tag{A.15}
$$

Inserting the expressions for the bound and polarization current and dividing by the permeability of free space

$$
\frac{1}{\mu_0}\vec{\nabla} \times \vec{B} = \vec{J}_f + \vec{\nabla} \times \vec{M} + \frac{\partial \vec{P}}{\partial t} + \varepsilon_0\frac{\partial \vec{E}}{\partial t}. \tag{A.16}
$$

Gathering curl terms and time-derivative terms gives

$$
\vec{\nabla} \times \frac{\vec{B}}{\mu_0} - \vec{\nabla} \times \vec{M} = \vec{J}_f + \frac{\partial \vec{P}}{\partial t} + \frac{\partial (\varepsilon_0\vec{E})}{\partial t}. \tag{A.17}
$$

Moving the terms inside the curl and derivative operators makes this

$$
\vec{\nabla} \times \left(\frac{\vec{B}}{\mu_0} - \vec{M}\right) = \vec{J}_f + \frac{\partial (\varepsilon_0\vec{E} + \vec{P})}{\partial t}. \tag{A.18}
$$

In this form of the Ampere-Maxwell law, the term in parentheses on the left side is written as a vector sometimes called the "magnetic field intensity" or "magnetic field strength" and defined as

$$
\vec{H} = \frac{\vec{B}}{\mu_0} - \vec{M}. \tag{A.19}
$$

Thus, the differential form of the Ampere-Maxwell law in terms of $\vec{H}$, $\vec{D}$, and the free current density is

$$
\vec{\nabla} \times \vec{H} = \vec{J}_{\mathrm{free}} + \frac{\partial \vec{D}}{\partial t}. \tag{A.20}
$$

Using Stokes' theorem gives the integral form of the Ampere-Maxwell law:

$$
\oint_C \vec{H} \circ d\vec{l} = I_{\mathrm{free,\ enc}} + \frac{d}{dt}\int_S \vec{D} \circ \hat{n}\,da. \tag{A.21}
$$

What is the physical significance of the magnetic intensity $\vec{H}$? In free space, the intensity is a vector field proportional to the magnetic field - pointing in the same direction as $\vec{B}$ and with magnitude scaled by the vacuum permeability. But just as $\vec{D}$ may differ from $\vec{E}$ inside dielectric materials, $\vec{H}$ may differ significantly from $\vec{B}$ in magnetic matter. For example, the magnetic intensity is not necessarily solenoidal - it will have divergence if the magnetization does, as can be seen by taking the divergence of both sides of Equation A.19.

As is the case for electric displacement, the usefulness of $\vec{H}$ comes about in situations for which you know the free current and for which symmetry considerations allow you to extract the magnetic intensity from the integral of Equation A.21. In such cases, you may be able to determine the magnetic field within a linear magnetic material by finding $\vec{H}$ on the basis of free current and then multiplying by the permeability of the medium to find the magnetic field.

Here is a summary of the integral and differential forms of all of Maxwell's Equations in matter:

**Gauss's law for electric fields:**

$$
\int_S \vec{D} \circ \hat{n}\,da = q_{\mathrm{free,\ enc}}
$$

(integral form),

$$
\vec{\nabla} \circ \vec{D} = \rho_{\mathrm{free}}
$$

(differential form).

**Gauss's law for magnetic fields:**

$$
\int_S \vec{B} \circ \hat{n}\,da = 0
$$

(integral form),

$$
\vec{\nabla} \circ \vec{B} = 0
$$

(differential form).

**Faraday's law:**

$$
\oint_C \vec{E} \circ d\vec{l} = -\frac{d}{dt}\int_S \vec{B} \circ \hat{n}\,da
$$

(integral form),

$$
\vec{\nabla} \times \vec{E} = -\frac{\partial \vec{B}}{\partial t}
$$

(differential form).

**Ampere-Maxwell law:**

$$
\oint_C \vec{H} \circ d\vec{l} = I_{\mathrm{free,\ enc}} + \frac{d}{dt}\int_S \vec{D} \circ \hat{n}\,da
$$

(integral form),

$$
\vec{\nabla} \times \vec{H} = \vec{J}_{\mathrm{free}} + \frac{\partial \vec{D}}{\partial t}
$$

(differential form).
