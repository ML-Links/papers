# 5 From Maxwell's Equations to the wave equation

Each of the four equations that have come to be known as Maxwell's Equations is powerful in its own right, for each embodies an important aspect of electromagnetic field theory. However, Maxwell's achievement went beyond the synthesis of these laws or the addition of the displacement current term to Ampere's law - it was by considering these equations *in combination* that he reached his goal of developing a comprehensive theory of electromagnetism. That theory elucidated the true nature of light itself and opened the eyes of the world to the full spectrum of electromagnetic radiation.

In this chapter, you'll learn how Maxwell's Equations lead directly to the wave equation in just a few steps. To make those steps, you'll first have to understand two important theorems of vector calculus: the divergence theorem and Stokes' theorem. These two theorems make the transition from the integral form to the differential form of Maxwell's Equations quite straightforward:

**Gauss's law for electric fields:**

$$
\oint_S \vec{E} \circ \hat{n}\,da = q_{\mathrm{in}}/\varepsilon_0
\qquad\Rightarrow\qquad
\vec{\nabla} \circ \vec{E} = \rho/\varepsilon_0.
$$

**Gauss's law for magnetic fields:**

$$
\oint_S \vec{B} \circ \hat{n}\,da = 0
\qquad\Rightarrow\qquad
\vec{\nabla} \circ \vec{B} = 0.
$$

**Faraday's law:**

$$
\oint_C \vec{E} \circ d\vec{l} = -\frac{d}{dt}\int_S \vec{B} \circ \hat{n}\,da
\qquad\Rightarrow\qquad
\vec{\nabla} \times \vec{E} = -\frac{\partial \vec{B}}{\partial t}.
$$

**Ampere-Maxwell law:**

$$
\oint_C \vec{B} \circ d\vec{l} = \mu_0\left(I_{\mathrm{enc}} + \varepsilon_0\frac{d}{dt}\int_S \vec{E} \circ \hat{n}\,da\right)
\qquad\Rightarrow\qquad
\vec{\nabla} \times \vec{B} = \mu_0\left(\vec{J} + \varepsilon_0\frac{\partial \vec{E}}{\partial t}\right).
$$

Along with the divergence theorem and Stokes' theorem, you'll also find a discussion of the gradient operator and some useful vector identities in this chapter. In addition, since the goal is to arrive at the wave equation, here are the expanded views of the wave equation for electric and magnetic fields:

![Expanded page view showing the electric and magnetic wave equations](workspace/ch5/ch5-page-2.png)

*Expanded views of the wave equation for electric and magnetic fields.*

Description: The page shows annotated forms of $\nabla^2\vec{E} = \mu_0\varepsilon_0\,\dfrac{\partial^2 \vec{E}}{\partial t^2}$ and $\nabla^2\vec{B} = \mu_0\varepsilon_0\,\dfrac{\partial^2 \vec{B}}{\partial t^2}$, with arrows labeling the Laplacian, the vector field, permittivity, permeability, and second time derivative terms.

## The divergence theorem

$$
\oint_S \vec{A} \circ \hat{n}\,da = \int_V (\vec{\nabla} \circ \vec{A})\,dV
$$

The divergence theorem is a vector-calculus relation that equates the flux of a vector field to the volume integral of the field's divergence. The relationships between line, surface, and volume integrals were explored by several of the leading mathematical thinkers of the eighteenth and nineteenth centuries, including J. L. Lagrange in Italy, M. V. Ostrogradsky in Russia, G. Green in England, and C. F. Gauss in Germany. In some texts, you'll find the divergence theorem referred to as "Gauss's theorem" (which you should not confuse with Gauss's law).

The divergence theorem may be stated as follows:

> The flux of a vector field through a closed surface $S$ is equal to the integral of the divergence of that field over a volume $V$ for which $S$ is a boundary.

This theorem applies to vector fields that are "smooth" in the sense of being continuous and having continuous derivatives.

To understand the physical basis for the divergence theorem, recall that the divergence at any point is defined as the flux through a small surface surrounding that point divided by the volume enclosed by that surface as it shrinks to zero. Now consider the flux through the cubical cells within the volume $V$ shown in Figure 5.1.

For interior cells (those not touching the surface of $V$), the faces are shared with six adjacent cells (only some of which are shown in Figure 5.1 for clarity). For each shared face, the positive (outward) flux from one cell is identical in amplitude and opposite in sign to the negative (inward) flux of the adjacent cell over that same face. Since all interior cells share faces with adjacent cells, only those faces that lie along the boundary surface $S$ of volume $V$ contribute to the flux through $S$.

This means that adding the flux through all the faces of all the cells throughout volume $V$ leaves only the flux through the bounding surface $S$. Moreover, in the limit of infinitesimally small cells, the definition of divergence tells you that the divergence of the vector field at any point is the outward flux from that point. So, adding the flux of each cell is the same as integrating the divergence over the entire volume. Thus,

$$
\oint_S \vec{A} \circ \hat{n}\,da = \int_V (\vec{\nabla} \circ \vec{A})\,dV. \tag{5.1}
$$

This is the divergence theorem - the integral of the divergence of a vector field over $V$ is identical to the flux through $S$. And how is this useful? For one thing, it can get you from the integral form to the differential form of Gauss's laws. In the case of electric fields, the integral form of Gauss's law is

$$
\oint_S \vec{E} \circ \hat{n}\,da = q_{\mathrm{enc}}/\varepsilon_0.
$$

Or, since the enclosed charge is the volume integral of the charge density $\rho$,

$$
\oint_S \vec{E} \circ \hat{n}\,da = \frac{1}{\varepsilon_0}\int_V \rho\,dV.
$$

Now, apply the divergence theorem to the left side of Gauss's law,

$$
\oint_S \vec{E} \circ \hat{n}\,da = \int_V \vec{\nabla} \circ \vec{E}\,dV = \frac{1}{\varepsilon_0}\int_V \rho\,dV = \int_V \frac{\rho}{\varepsilon_0}\,dV.
$$

Since this equality must hold for all volumes, the integrands must be equal. Thus,

$$
\vec{\nabla} \circ \vec{E} = \rho/\varepsilon_0,
$$

which is the differential form of Gauss's law for electric fields. The same approach applied to the integral form of Gauss's law for magnetic fields leads to

$$
\vec{\nabla} \circ \vec{B} = 0
$$

as you might expect.

![Figure 5.1 page view](workspace/ch5/ch5-page-3.png)

*Figure 5.1 Cubical cells within volume $V$ bounded by surface $S$.*

Description: The lower portion of the page shows a shaded boundary surface enclosing many small cubical cells, with arrows indicating positive and negative flux through shared faces and through the outer boundary.

## Stokes' theorem

$$
\oint_C \vec{A} \circ d\vec{l} = \int_S (\vec{\nabla} \times \vec{A}) \circ \hat{n}\,da
$$

Whereas the divergence theorem relates a surface integral to a volume integral, Stokes' theorem relates a line integral to a surface integral. William Thompson (later Lord Kelvin) referred to this relation in a letter in 1850, and it was G. G. Stokes who made it famous by setting its proof as an exam question for students at Cambridge. You may encounter generalized statements of Stokes' theorem, but the form relevant to Maxwell's Equations (sometimes called the "Kelvin-Stokes theorem") may be stated as follows:

> The circulation of a vector field over a closed path $C$ is equal to the integral of the normal component of the curl of that field over a surface $S$ for which $C$ is a boundary.

This theorem applies to vector fields that are "smooth" in the sense of being continuous and having continuous derivatives.

The physical basis for Stokes' theorem may be understood by recalling that the curl at any point is defined as the circulation around a small path surrounding that point divided by the surface area enclosed by that path as it shrinks to zero. Consider the circulation around the small squares on the surface $S$ shown in Figure 5.2.

For interior squares (those not touching the edge of the surface), each edge is shared with an adjacent square. For each shared edge, the circulation from one square is identical in amplitude and opposite in sign to the circulation of the adjacent square over that same edge. It is only those edges that lie along the boundary path $C$ of surface $S$ that are not shared with an adjacent square, and which contribute to the circulation around $C$.

Thus, adding the circulation around all the edges of all the squares over surface $S$ leaves only the circulation around the bounding path $C$. In addition, in the limit of infinitesimally small squares, the definition of curl tells you that adding the circulation of each square is the same as integrating the normal component of the curl of the vector field over the surface. So,

$$
\oint_C \vec{A} \circ d\vec{l} = \int_S (\vec{\nabla} \times \vec{A}) \circ \hat{n}\,da. \tag{5.2}
$$

Stokes' theorem does for line integrals and the curl what the divergence theorem does for surface integrals and the divergence. In this case, the integral of the normal component of the curl over $S$ is identical to the circulation around $C$. Moreover, just as the divergence theorem leads from the integral to the differential form of Gauss's laws, Stokes' theorem can be applied to the integral form of Faraday's law and the Ampere-Maxwell law.

Consider the integral form of Faraday's law, which relates the circulation of the electric field around a path $C$ to the change in magnetic flux through a surface $S$ for which $C$ is a boundary,

$$
\oint_C \vec{E} \circ d\vec{l} = -\frac{d}{dt}\int_S \vec{B} \circ \hat{n}\,da.
$$

Applying Stokes' theorem to the circulation on the left side gives

$$
\oint_C \vec{E} \circ d\vec{l} = \int_S (\vec{\nabla} \times \vec{E}) \circ \hat{n}\,da
$$

Thus, Faraday's law becomes

$$
\int_S (\vec{\nabla} \times \vec{E}) \circ \hat{n}\,da = -\frac{d}{dt}\int_S \vec{B} \circ \hat{n}\,da.
$$

For stationary geometries, the time derivative can be moved inside the integral, so this is

$$
\int_S (\vec{\nabla} \times \vec{E}) \circ \hat{n}\,da = \int_S \left(-\frac{\partial \vec{B}}{\partial t} \circ \hat{n}\right)\,da,
$$

where the partial derivative indicates that the magnetic field may change over space as well as time. Since this equality must hold over all surfaces, the integrands must be equal, giving

$$
\vec{\nabla} \times \vec{E} = -\frac{\partial \vec{B}}{\partial t},
$$

which is the differential form of Faraday's law, relating the curl of the electric field at a point to the time rate of change of the magnetic field at that point.

Stokes' theorem may also be used to find the differential form of the Ampere-Maxwell law. Recall that the integral form relates the circulation of the magnetic field around a path $C$ to the current enclosed by that path and the time rate of change of electric flux through a surface $S$ bound by path $C$:

$$
\oint_C \vec{B} \circ d\vec{l} = \mu_0\left(I_{\mathrm{enc}} + \varepsilon_0\frac{d}{dt}\int_S \vec{E} \circ \hat{n}\,da\right).
$$

Applying Stokes' theorem to the circulation gives

$$
\oint_C \vec{B} \circ d\vec{l} = \int_S (\vec{\nabla} \times \vec{B}) \circ \hat{n}\,da,
$$

which makes the Ampere-Maxwell law

$$
\int_S (\vec{\nabla} \times \vec{B}) \circ \hat{n}\,da = \mu_0\left(I_{\mathrm{enc}} + \varepsilon_0\frac{d}{dt}\int_S \vec{E} \circ \hat{n}\,da\right).
$$

The enclosed current may be written as the integral of the normal component of the current density

$$
I_{\mathrm{enc}} = \int_S \vec{J} \circ \hat{n}\,da,
$$

and the Ampere-Maxwell law becomes

$$
\int_S (\vec{\nabla} \times \vec{B}) \circ \hat{n}\,da = \mu_0\left(\int_S \vec{J} \circ \hat{n}\,da + \int_S \varepsilon_0\frac{\partial \vec{E}}{\partial t} \circ \hat{n}\,da\right).
$$

Once again, for this equality to hold over all surfaces, the integrands must be equal, meaning

$$
\vec{\nabla} \times \vec{B} = \mu_0\left(\vec{J} + \varepsilon_0\frac{\partial \vec{E}}{\partial t}\right).
$$

This is the differential form of the Ampere-Maxwell law, relating the curl of the magnetic field at a point to the current density and time rate of change of the electric field at that point.

![Figure 5.2 page view](workspace/ch5/ch5-page-5.png)

*Figure 5.2 Squares on surface $S$ bounded by path $C$.*

Description: The lower portion of the page shows a curved surface tiled by small squares and a boundary path $C$, with annotations indicating cancellation of circulation along shared interior edges and remaining circulation along the boundary.

## The gradient

To understand how Maxwell's Equations lead to the wave equation, it is necessary to comprehend a third differential operation used in vector calculus - the gradient. Similar to the divergence and the curl, the gradient involves partial derivatives taken in three orthogonal directions. However, whereas the divergence measures the tendency of a vector field to flow away from a point and the curl indicates the circulation of a vector field around a point, the gradient applies to *scalar fields*. Unlike a vector field, a scalar field is specified entirely by its magnitude at various locations: one example of a scalar field is the height of terrain above sea level.

What does the gradient tell you about a scalar field? Two important things: the magnitude of the gradient indicates how quickly the field is changing over space, and the direction of the gradient indicates the direction in that the field is changing most quickly with distance.

Therefore, although the gradient operates on a scalar field, the result of the gradient operation is a vector, with both magnitude and direction. Thus, if the scalar field represents terrain height, the magnitude of the gradient at any location tells you how steeply the ground is sloped at that location, and the direction of the gradient points *uphill* along the steepest slope.

The definition of the gradient of the scalar field $\psi$ is

$$
\mathrm{grad}(\psi) = \vec{\nabla}\psi = \hat{i}\,\frac{\partial \psi}{\partial x} + \hat{j}\,\frac{\partial \psi}{\partial y} + \hat{k}\,\frac{\partial \psi}{\partial z} \qquad (\text{Cartesian}). \tag{5.3}
$$

Thus, the $x$-component of the gradient of $\psi$ indicates the slope of the scalar field in the $x$-direction, the $y$-component indicates the slope in the $y$-direction, and the $z$-component indicates the slope in the $z$-direction. The square root of the sum of the squares of these components provides the total steepness of the slope at the location at which the gradient is taken.

In cylindrical and spherical coordinates, the gradient is

$$
\vec{\nabla}\psi = \hat{r}\,\frac{\partial \psi}{\partial r} + \hat{\varphi}\,\frac{1}{r}\frac{\partial \psi}{\partial \varphi} + \hat{z}\,\frac{\partial \psi}{\partial z} \qquad (\text{cylindrical}) \tag{5.4}
$$

and

$$
\vec{\nabla}\psi = \hat{r}\,\frac{\partial \psi}{\partial r} + \hat{\theta}\,\frac{1}{r}\frac{\partial \psi}{\partial \theta} + \hat{\varphi}\,\frac{1}{r\sin\theta}\frac{\partial \psi}{\partial \varphi} \qquad (\text{spherical}). \tag{5.5}
$$

## Some useful identities

Here is a quick review of the del differential operator and its three uses relevant to Maxwell's Equations:

**Del:**

$$
\vec{\nabla} = \hat{i}\,\frac{\partial}{\partial x} + \hat{j}\,\frac{\partial}{\partial y} + \hat{k}\,\frac{\partial}{\partial z}
$$

Del (nabla) represents a multipurpose differential operator that can operate on scalar or vector fields and produce scalar or vector results.

**Gradient:**

$$
\vec{\nabla}\psi = \hat{i}\,\frac{\partial \psi}{\partial x} + \hat{j}\,\frac{\partial \psi}{\partial y} + \hat{k}\,\frac{\partial \psi}{\partial z}
$$

The gradient operates on a scalar field and produces a vector result that indicates the rate of spatial change of the field at a point and the direction of steepest increase from that point.

**Divergence:**

$$
\vec{\nabla} \circ \vec{A} \equiv \frac{\partial A_x}{\partial x} + \frac{\partial A_y}{\partial y} + \frac{\partial A_z}{\partial z}
$$

The divergence operates on a vector field and produces a scalar result that indicates the tendency of the field to flow away from a point.

**Curl:**

$$
\vec{\nabla} \times \vec{A} \equiv \left(\frac{\partial A_z}{\partial y} - \frac{\partial A_y}{\partial z}\right)\hat{i} + \left(\frac{\partial A_x}{\partial z} - \frac{\partial A_z}{\partial x}\right)\hat{j} + \left(\frac{\partial A_y}{\partial x} - \frac{\partial A_x}{\partial y}\right)\hat{k}
$$

The curl operates on a vector field and produces a vector result that indicates the tendency of the field to circulate around a point and the direction of the axis of greatest circulation.

Once you're comfortable with the meaning of each of these operators, you should be aware of several useful relations between them (note that the following relations apply to fields that are continuous and that have continuous derivatives).

The curl of the gradient of any scalar field is zero.

$$
\vec{\nabla} \times \vec{\nabla}\psi = 0, \tag{5.6}
$$

which you may readily verify by taking the appropriate derivatives.

Another useful relation involves the divergence of the gradient of a scalar field; this is called the Laplacian of the field:

$$
\vec{\nabla} \circ \vec{\nabla}\psi = \nabla^2 \psi = \frac{\partial^2 \psi}{\partial x^2} + \frac{\partial^2 \psi}{\partial y^2} + \frac{\partial^2 \psi}{\partial z^2} \qquad (\text{Cartesian}). \tag{5.7}
$$

The usefulness of these relations can be illustrated by applying them to the electric field as described by Maxwell's Equations. Consider, for example, the fact that the curl of the electrostatic field is zero (since electric field lines diverge from positive charge and converge upon negative charge, but do not circulate back upon themselves). Equation 5.6 indicates that as a curl-free (irrotational) field, the electrostatic field $\vec{E}$ may be treated as the gradient of another quantity called the scalar potential $V$:

$$
\vec{E} = -\vec{\nabla}V, \tag{5.8}
$$

where the minus sign is needed because the gradient points toward the greatest *increase* in the scalar field, and by convention the electric force on a positive charge is toward *lower* potential. Now apply the differential form of Gauss's law for electric fields:

$$
\vec{\nabla} \circ \vec{E} = \frac{\rho}{\varepsilon_0},
$$

which, combined with Equation 5.8, gives

$$
\nabla^2 V = -\frac{\rho}{\varepsilon_0}. \tag{5.9}
$$

This is called Laplace's equation, and it is often the best way to find the electrostatic field when you are not able to construct a special Gaussian surface. In such cases, it may be possible to solve Laplace's Equation for the electric potential $V$ and then determine $\vec{E}$ by taking the gradient of the potential.

## The wave equation

With the differential form of Maxwell's Equations and several vector operator identities in hand, the trip to the wave equation is a short one. Begin by taking the curl of both sides of the differential form of Faraday's law

$$
\vec{\nabla} \times (\vec{\nabla} \times \vec{E}) = \vec{\nabla} \times \left(-\frac{\partial \vec{B}}{\partial t}\right) = -\frac{\partial (\vec{\nabla} \times \vec{B})}{\partial t}. \tag{5.10}
$$

Notice that the curl and time derivatives have been interchanged in the final term; as in previous sections, the fields are assumed to be sufficiently smooth to permit this.

Another useful vector operator identity says that the curl of the curl of any vector field equals the gradient of the divergence of the field minus the Laplacian of the field:

$$
\vec{\nabla} \times (\vec{\nabla} \times \vec{A}) = \vec{\nabla}(\vec{\nabla} \circ \vec{A}) - \nabla^2\vec{A}. \tag{5.11}
$$

This relation uses a vector version of the Laplacian operator that is constructed by applying the Laplacian to the components of a vector field:

$$
\nabla^2\vec{A} = \frac{\partial^2 A_x}{\partial x^2} + \frac{\partial^2 A_y}{\partial y^2} + \frac{\partial^2 A_z}{\partial z^2} \qquad (\text{Cartesian}). \tag{5.12}
$$

Thus,

$$
\vec{\nabla} \times (\vec{\nabla} \times \vec{E}) = \vec{\nabla}(\vec{\nabla} \circ \vec{E}) - \nabla^2\vec{E} = -\frac{\partial (\vec{\nabla} \times \vec{B})}{\partial t}. \tag{5.13}
$$

However, you know the curl of the magnetic field from the differential form of the Ampere-Maxwell law:

$$
\vec{\nabla} \times \vec{B} = \mu_0\left(\vec{J} + \varepsilon_0\frac{\partial \vec{E}}{\partial t}\right).
$$

So,

$$
\vec{\nabla} \times (\vec{\nabla} \times \vec{E}) = \vec{\nabla}(\vec{\nabla} \circ \vec{E}) - \nabla^2\vec{E} = -\frac{\partial [\mu_0(\vec{J} + \varepsilon_0(\partial \vec{E}/\partial t))]}{\partial t}.
$$

This looks difficult, but one simplification can be achieved using Gauss's law for electric fields:

$$
\vec{\nabla} \circ \vec{E} = \frac{\rho}{\varepsilon_0},
$$

which means

$$
\vec{\nabla} \times (\vec{\nabla} \times \vec{E}) = \vec{\nabla}\left(\frac{\rho}{\varepsilon_0}\right) - \nabla^2\vec{E} = -\frac{\partial [\mu_0(\vec{J} + \varepsilon_0(\partial \vec{E}/\partial t))]}{\partial t}
$$

$$
= -\mu_0\frac{\partial \vec{J}}{\partial t} - \mu_0\varepsilon_0\frac{\partial^2 \vec{E}}{\partial t^2}.
$$

Gathering terms containing the electric field on the left side of this equation gives

$$
\nabla^2\vec{E} - \mu_0\varepsilon_0\frac{\partial^2 \vec{E}}{\partial t^2} = \vec{\nabla}\left(\frac{\rho}{\varepsilon_0}\right) + \mu_0\frac{\partial \vec{J}}{\partial t}.
$$

In a charge- and current-free region, $\rho = 0$ and $\vec{J} = 0$, so

$$
\nabla^2\vec{E} = \mu_0\varepsilon_0\frac{\partial^2 \vec{E}}{\partial t^2}. \tag{5.14}
$$

This is a linear, second-order, homogeneous partial differential equation that describes an electric field that travels from one location to another - in short, a propagating wave. Here is a quick reminder of the meaning of each of the characteristics of the wave equation:

**Linear:** The time and space derivatives of the wave function ($\vec{E}$ in this case) appear to the first power and without cross terms.

**Second-order:** The highest derivative present is the second derivative.

**Homogeneous:** All terms involve the wave function or its derivatives, so no forcing or source terms are present.

**Partial:** The wave function is a function of multiple variables (space and time in this case).

A similar analysis beginning with the curl of both sides of the Ampere-Maxwell law leads to

$$
\nabla^2\vec{B} = \mu_0\varepsilon_0\frac{\partial^2 \vec{B}}{\partial t^2}, \tag{5.15}
$$

which is identical in form to the wave equation for the electric field.

This form of the wave equation doesn't just tell you that you have a wave - it provides the velocity of propagation as well. It is right there in the constants multiplying the time derivative, because the general form of the wave equation is this

$$
\nabla^2\vec{A} = \frac{1}{v^2}\frac{\partial^2\vec{A}}{\partial t^2}, \tag{5.16}
$$

where $v$ is the speed of propagation of the wave. Thus, for the electric and magnetic fields

$$
\frac{1}{v^2} = \mu_0\varepsilon_0,
$$

or

$$
v = \sqrt{\frac{1}{\mu_0\varepsilon_0}}. \tag{5.17}
$$

Inserting values for the magnetic permeability and electric permittivity of free space,

$$
v = \sqrt{\frac{1}{\left[4\pi \times 10^{-7}\,\mathrm{m\ kg/C^2}\right]\left[8.8541878 \times 10^{-12}\,\mathrm{C^2\ s^2/kg\ m^3}\right]}},
$$

or

$$
v = \sqrt{8.987552 \times 10^{16}}\,\mathrm{m^2/s^2} = 2.9979 \times 10^8\ \mathrm{m/s}.
$$

It was the agreement of the calculated velocity of propagation with the measured speed of light that caused Maxwell to write, "light is an electromagnetic disturbance propagated through the field according to electromagnetic laws."
