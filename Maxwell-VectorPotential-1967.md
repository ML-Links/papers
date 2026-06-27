# Maxwell and the Vector Potential

Author(s): Alfred M. Bork  
Source: *Isis*, Vol. 58, No. 2 (Summer, 1967), pp. 210-222  
Published by: The University of Chicago Press on behalf of The History of Science Society  
Stable URL: https://www.jstor.org/stable/228226  
Accessed: 27-06-2026 12:46 UTC

JSTOR is a not-for-profit service that helps scholars, researchers, and students discover, use, and build upon a wide range of content in a trusted digital archive. We use information technology and tools to increase productivity and facilitate new forms of scholarship. For more information about JSTOR, please contact support@jstor.org.

Your use of the JSTOR archive indicates your acceptance of the Terms & Conditions of Use, available at https://about.jstor.org/terms

# Maxwell and the Vector Potential

By Alfred M. Bork[^*]

The literature of physics today resounds with a common attitude toward the potentials in electromagnetic theory, an attitude presented in several different forms. Sometimes we find an ontological statement that the electric and magnetic fields are real quantities but the potentials are mathematical fictions introduced only for convenience in solving the basic equations of electromagnetic theory. While I consider the distinction between physical and mathematical quantities dubious as a philosophical position, it is not the concern of the present paper; rather, I am interested in what seems to be a historical form of the same idea. According to this historical position, the potentials were first introduced into electromagnetic theory as a mathematical device to help solve the basic equations. This view is found in almost all current literature. For example, a recent series of papers began with the following comment: "In classical electrodynamics, the vector and scalar potentials were first introduced as a convenient mathematical aid for calculating the fields."[^1] Such statements as this appear to make a historical assertion. Here we investigate the introduction of the vector potential in the work of James Clerk Maxwell, and we shall see that the above view is far from accurate in representing the historical situation. We review Maxwell's approach chronologically, primarily in his four papers on electromagnetic theory and in the *Treatise on Electricity and Magnetism*.

## Maxwell to Thomson

The earliest detailed account we have of the beginning of Maxwell's work in electromagnetic theory is in his letters to William Thomson, and there we first meet the concept that interests us. The early letters show Maxwell's increasing interest in electricity and magnetism, and by 13 September 1835[^2] he has outlined a paper. After mentioning lines of force and electrical images, he says:

> I intend to apply to these facts Faraday's notion of an *electrotonic* state.
> I have worked a good deal of mathematical material out of this vein and I
> believe that I have got hold of several truths in the electrotonic state.
> One thing at least it succeeds in, it reduces to one principle not only the
> attraction of currents and the induction of currents but also the attraction
> of electrified bodies without any new assumption.

This concept of the electrotonic state, which we shall trace through Maxwell's own work, is renamed several times by Maxwell and eventually becomes the vector potential in the *Treatise on Electricity and Magnetism*.

## "On Faraday's Lines of Force"

Maxwell's first paper on electromagnetic theory, "On Faraday's Lines of Force,"[^3] published in 1856, is heavily dependent on Faraday. One of the major aspects of this paper is Maxwell's mathematical formulation of Faraday's conception of the electrotonic state,[^4] following the comment in the letter. At the end of the first part of the paper, Maxwell comments about Faraday's ideas:

> A closed conductor in a magnetic field may be supposed to be in a certain
> state arising from the magnetic action. As long as this state remains unchanged
> no effect takes place, but, when the state changes, electro-motive
> forces arise, depending as to their intensity and direction on this change of
> state. I cannot do better here than quote a passage from the first series
> of Faraday's *Experimental Researches*, Art. (60).
>
> While the wire is subject to either volta-electric or magno-electric induction
> it appears to be in a peculiar state, for it resists the formation of an electrical
> current in it; whereas, if in its common condition, such a current would be
> produced; and when left uninfluenced it has the power of originating a
> current, a power which the wire does not possess under ordinary circumstances.
> This electrical condition of matter has not hitherto been recognised,
> but it probably exerts a very important influence in many if not most of
> the phenomena produced by currents of electricity. For reasons which will
> immediately appear (7) I have, after advising with several learned friends,
> ventured to designate it as the electro-tonic state.
>
> ... The idea of the electro-tonic state, however, has not yet presented itself
> to my mind in such a form that its nature and properties may be clearly
> explained without reference to mere symbols, and therefore I propose in the
> following investigation to use symbols freely, and to take for granted
> the ordinary mathematical operations. By a careful study of the laws of
> elastic solids and of the motion of viscous fluids, I hope to discover a method
> of forming a mechanical conception of the electro-tonic state adapted to
> general reasoning.[^5]

Part II of Maxwell's paper is called "On Faraday's 'Electro-tonic State.'" He comments at the end of the first part:

> Considerations of this kind led Professor Faraday to connect with his
> discovery of the induction of electric currents the conception of a state into
> which all bodies are thrown by the presence of magnets and currents. This
> state does not manifest itself by any known phenomenon as long as it is undisturbed,
> but any change in this state is indicated by a current or tendency
> towards a current.[^6]

Maxwell proceeds as he suggests from this verbal description to a mathematical formulation. He introduces three quantities, $\alpha_0$, $\beta_0$, $\gamma_0$, and relates them through integral theorems (attributed to Green and Thomson) to the electromotive force at a point and to magnetism. We shall see the explicit relation, in a slightly different notation, in a moment.

> We have now obtained in the functions $\alpha_0, \beta_0, \gamma_0$, the means of avoiding
> the consideration of the quantity of magnetic induction which passes through
> the circuit. Instead of this artificial method we have the natural one of considering
> the current with reference to the quantities existing in the same
> space with the current itself. To these I give the name of Electro-tonic functions,
> or components of the Electro-tonic intensity.[^7]

Maxwell's intent is clear: he seeks and finds quantities which determine electric induction effects at a particular point, not in terms of a closed circuit and the behavior of magnetic induction inside this circuit, but by using only functions at the same point at which the induction is sought. The equations which realize the goal are

$$
\alpha_2 = -\frac{1}{4\pi}\frac{d\alpha_0}{dt}, \qquad
\beta_2 = -\frac{1}{4\pi}\frac{d\beta_0}{dt}, \qquad
\gamma_2 = -\frac{1}{4\pi}\frac{d\gamma_0}{dt},
$$

while the electrotonic functions are related to the magnetic quantities by three equations of the form

$$
\alpha_1 = \frac{d\beta_0}{dz} - \frac{d\gamma_0}{dy} - \frac{dV}{dx}.
$$

Maxwell apologizes for so much mathematical detail: "I hope to exhibit the theory of the electro-tonic state in a form in which all its relations may be distinctly conceived without reference to analytical calculations."[^8] Perhaps this remark reflects Maxwell's hope, expressed in a letter to Thomson, that Faraday will read the paper.

Maxwell's notation in "On Faraday's Lines of Force" is interesting. He denotes the components of the magnetic field by $\alpha_1$, $\beta_1$, and $\gamma_1$, and he denotes the components of the electric field (the "electromotive forces") by $\alpha_2$, $\beta_2$, and $\gamma_2$. Then for the electrotonic state he introduces a notation that is almost parallel to that used in the electric and magnetic cases. This choice of notation raises the possibility that he intended to establish the electrotonic functions on the same level as those describing the electric and magnetic fields, perhaps developing a three-sided analogy involving the quantities. But formal mathematical properties may have suggested this notation. The mathematical relations involving $\alpha_0$, $\beta_0$, and $\gamma_0$ already begin to resemble those involving the vector potential today.

E. T. Whittaker attributes Maxwell's ideas to William Thomson:

> ... Maxwell discussed how Faraday's "electrotonic state" might be represented
> in mathematical symbols. This problem he solved by borrowing
> from Thomson's investigation of 1847 the vector $\mathbf{a}$, which is defined in terms
> of magnetic induction by the equation $\operatorname{curl}\, \mathbf{a} = \mathbf{B}$.[^9]

Maxwell does give several references to Thomson's 1847 paper "On a Mechanical Representation of Electric, Magnetic, and Galvanic Forces." But it is difficult to see any connection between the formulations in this paper and Maxwell's setting of the electrotonic state. There is a closer mathematical connection with Thomson's "A Mathematical Theory of Magnetism,"[^10] published in the *Philosophical Transactions of the Royal Society* in 1851, where the curl of $F$, $G$, $H$ is termed intensity of magnetization, but where the quantity $F$, $G$, $H$ is left unnamed. Maxwell explicitly uses the mathematical method of the paper in Theorem V in "On Faraday's Lines of Force." But both Maxwell and Thomson attribute the basic details to Green, and Stokes had also used them. At the end of "On Faraday's Lines of Force" Maxwell comments:

> ... the recognition of certain mathematical functions as expressing the
> "electro-tonic state" of Faraday, and the use of them in determining electrodynamic
> potentials and electro-motive forces, is, as far as I am aware, original;
> but the distinct conception of the possibility of the mathematical
> expressions arose in my mind from the perusal of Prof. W. Thomson's
> papers. ...[^11]

## "On Physical Lines of Force"

Maxwell's second paper, "On Physical Lines of Force,"[^12] dated 1861-1862, presents an almost complete version of electromagnetic theory, based on a model, and suggests the electromagnetic theory of light. Early in this paper he refers to the previous paper, commenting on the electrotonic state (Maxwell has now dropped the hyphen):

> In the same paper I have found the geometrical significance of the "electrotonic
> state," and have shewn how to deduce the mathematical relations
> between the electrotonic state, magnetism, electric currents, and the electromotive
> force, using mechanical illustrations to assist the imagination, but
> not to account for the phenomena.[^13]

Later in the paper we encounter the mathematical aspects. He introduces three quantities, $F$, $G$, and $H$, using integral theorems of Stokes.

> We have determined three quantities, $F$, $G$, $H$, from which we can find
> $P$, $Q$, and $R$ by considering these latter quantities as the rates at which the
> former ones vary. In the paper already referred to, I have given reasons for
> considering the quantities $F$, $G$, $H$ as the resolved parts of that which Faraday
> has conjectured to exist, and has called the electrotonic state. In that paper I
> have stated the mathematical relations between this electrotonic state and
> the lines of magnetic force as expressed in equations (55) and also between
> the electrotonic state and electromotive force as expressed in equations (58).[^14]

There is no explanation for using another notation. We have already noted that Thomson had used $F$, $G$, and $H$ in a very similar mathematical context. "On Physical Lines ..." does not maintain the subscripting of "On Faraday's Lines ..." but gives instead a separate set of three consecutive letters for each of the vectorlike quantities introduced. Maxwell does not use explicit vector terminology until the *Treatise*, as we note later; however, he is consistent in his later work, using the same $F$, $G$, and $H$ that he introduces here. This is convenient, for, as we shall see, he is not consistent about the name of the quantities.

After $F$, $G$, and $H$ are introduced, the relations resemble those seen today; Equations 55 are the standard relations between the magnetic field and the vector potential,

$$
\frac{dG}{dz} - \frac{dH}{dy} = \mu\alpha, \qquad
\frac{dH}{dx} - \frac{dF}{dz} = \mu\beta, \qquad
\frac{dF}{dy} - \frac{dG}{dx} = \mu\gamma.
$$

The quantities $\alpha$, $\beta$, and $\gamma$ are the components of magnetic induction; Maxwell has no special notation for a partial derivative. Equation 57 is a "gauge condition,"

$$
\frac{dF}{dx} + \frac{dG}{dy} + \frac{dH}{dz} = 0,
$$

with the divergence of the electrotonic state functions set to zero. Equation 58 is the relation between the electric field and the vector potential with a sign different from the usual modern form. The signs are positive:

$$
P = \frac{dF}{dt}, \qquad Q = \frac{dG}{dt}, \qquad R = \frac{dH}{dt}.
$$

These equations provide the pointlike relation between the inducing agent and the induced electric field with components $P$, $Q$, and $R$, the original purpose of the electrotonic state.

## "A Dynamical Theory of the Electromagnetic Field"

Maxwell's definitive 1865 paper, "A Dynamical Theory of the Electromagnetic Field,"[^15] presents the twenty basic equations of the electromagnetic field, without use of the elaborate mechanical model of the previous paper.

The first appearance of our concept is in the section of the paper dealing primarily with circuits:

> It appears, therefore, that if we admit that the unresisted part of electromotive
> force goes on as long as it acts, generating a self-resistant state of the
> current, which we may call (from mechanical analogy) its electromagnetic
> momentum, and that this momentum depends on circumstances external to
> the conductor, then both induction of currents and electromagnetic attraction
> may be proved by mechanical reasoning.
>
> What I have called the electromagnetic momentum is the same quantity
> which is called by Faraday the electrotonic state of the circuit, every change
> of which involves the action of an electromotive force, just as change of
> momentum involves the action of mechanical force.[^16]

We note immediately that we have a new name: the electromagnetic momentum. The meaning of this name is understandable, coming from an interpretation of the relation between an electric field and vector potential as if it were a mechanical equation; the time rate of change of the electromagnetic momentum gives the electromotive force at a point. But the motivation for this change in name is not clear to me. Given Maxwell's devotion to Faraday, why should he replace Faraday's name?

When Maxwell presents the twenty general equations of the electromagnetic field, he first lists the "twenty variable quantities" which appear in the equations. Three of these quantities are $F$, $G$, and $H$: "Let $F$, $G$, $H$ represent the components of electromagnetic momentum at any point of the field, due to any system of magnets or currents." Again the relation between electric fields and electromagnetic momentum is that the first is the time derivative of the second, but now the minus signs appear as they do today. The General Equations of the Electromagnetic Field have letter names. Equations B, "the relation between the lines of magnetic force and the induction coefficient of a circuit," and Equation D, "the value of the body in the field, the alteration of the field itself, and the variation of the electric potential from one part of the field to another," both involve the electromagnetic momentum. Equations B are identical with Equations 55 in "On Physical Lines of Force," and the middle term in D, that "due to the alteration of the field itself," corresponds to Equation 58 except for the changed sign.

Thus we see that in Maxwell's first attempt to give a complete statement of the electromagnetic field equations, the quantity which we later define as vector potential is occurring in the basic concepts and in the basic equations. Nothing suggests that it is only a mathematical device.

## "Note on the Electromagnetic Theory"

Maxwell's 1868 paper,[^17] which begins by discussing the relation between units, ends with a brief statement on electromagnetic theory. This beautiful paper, little known both in Maxwell's time and today, is of all Maxwell's formulations of electromagnetic theory closest to our present standard version. Here the potentials are absent altogether, probably for the only time in the Maxwell literature. It is interesting to speculate why Maxwell himself did not pursue this lead; when he wrote the *Treatise* he returned to the structure of the 1865 equations in "A Dynamical Theory of the Electromagnetic Field" instead of using this formulation.

## The Correspondence with P. G. Tait

Except for the early correspondence with William Thomson which we have noted, Maxwell's letters give little information concerning the development of electromagnetic theory. But three letters to P. G. Tait between the publication of the 1865 paper and the first edition of the *Treatise* in 1873 relate to the history of the vector potential.

The 12 March 1868 letter shows, as does the 1868 paper, that Maxwell has been reading Riemann and Weber. For Riemann, Maxwell has "great respect and regret." He mentions that Weber's force depends on the distance and on the first and second time derivatives and then goes on: "Riemann says that this is due to the fact that the potential at a point is due to the distribution of electricity elsewhere not at that instant but at times before depending on the distance. In other words potential is propagated through space. ..."[^18] Presumably he is talking about the usual scalar potential here, as that would relate to the force considered by Riemann and Weber. But in Maxwell's field theory the scalar potential is *not* propagated; Maxwell does not write a wave equation for the scalar potential, as his "gauge" is not consistent with such an equation.

There are two letters dated 23 January 1871 in the surviving correspondence, both from Maxwell to Tait. The first is without a signature, and so may have been a draft of the long second one. They started with the same line, "still harping on that Nabla," a reference to Hamilton's $\nabla$ operator. They have similar content, but the second one is expanded and rearranged. The first one is of interest here:

> We know that the equation $\nabla^2 E = x$ with the condition $E = 0$ at $\infty$ has no
> solution but $E = \dfrac{1}{4\pi} \iiint \dfrac{x}{r}\, d\,(\text{volume})$ over all space
> This is true whether $x$ be a scalar or a vector and $E$ is scalar or vector according as $x$ is
> Hence if it is a vector function we can express $\sigma$ as $\sigma = \nabla T$ by finding $T$ from the
> equation $\nabla^2 T = \nabla \sigma$ Now $\nabla \sigma$ is partly scalar $(= m)$ and partly vector
> $(= \alpha)$ Let $P$ be the potential of $m$ and $L\ M\ N$ the constituents of vector
> potential of $\alpha$ then $T$ is expressed by equations of the form
>
> $$
> T = P + iL + jM + kN
> $$
>
> See Stokes on Dynamical Theory of Diffraction Camb Trans. 1849 or 50.

This is the first explicit use by Maxwell of the term "vector potential" I have found. This "new" term is missing from the more detailed letter with signature, and, as we shall see, when Maxwell first introduces the vector potential in the *Treatise* it is in a different context.

Finally, in a letter to Tait dated 2 October 1872 there is a passage similar to one that will appear in the 1873 *Treatise*. In the letter Maxwell even notes the appropriate article number by which the passage will be designated in the *Treatise*. The expressions involve the vector potential, but there are no comments about it.

## *Treatise on Electricity and Magnetism*

Not Maxwell's papers, but his *Treatise*,[^19] became the primary source for most of the later workers in electromagnetic theory. Instead of reviewing the many mentions of the vector potential in the *Treatise*, we confine ourselves to the principal ones in Volume II. (There appear to be no uses in Volume I.) The notation of $F$, $G$, and $H$ for the components is still being used, as well as the alternative notation of quaternions. Maxwell's earlier papers lacked quaternion notation, but partially under the influence of P. G. Tait, Maxwell sparingly introduced some use of quaternions into the *Treatise*. He modified the Hamilton-Tait notation slightly by indicating quaternions (and therefore vectors) by German Gothic letters. From Maxwell's Gothic letters we derive our present symbols for electromagnetic theory, so it is not surprising that the entity which interests us is designated by Gothic $\mathfrak{A}$. It is worth noting that although Maxwell talks about quaternions in the *Treatise*, he employs nothing difficult to understand within a pure vector framework; his quaternions usually have no scalar part.

Article 405 of the *Treatise*[^20] is entitled "The Vector Potential of Magnetic Induction." Maxwell has not, as far as I have been able to determine, previously used the term "vector potential" in print. We identify this section primarily because the components of the vector potential are the same ones as we have seen several times, relating $F$, $G$, and $H$ with the components of magnetic induction. But there is no mention here of the previous work or of the previous names. The chapter is primarily concerned with the magnetic field. In this same section Maxwell explicitly solves for the components of the vector potential for the case of a magnetic dipole and then generalizes the expressions for a magnet of any form.

It seems curious that Maxwell is again introducing a new name-the third one. The name of a quantity tells us nothing or very little about the logical structure of a theory, but it may throw a historical light upon the developer's path. The word "potential" was in general use during this period, both directly and in the expression "potential energy." But it was not commonly used except in the scalar form. In Thomson and Tait's *Treatise*,[^21] published six years after Maxwell's *Treatise*, the concept is attributed to Laplace in a gravitational context and the name is attributed to Green's work of 1828. Thomson often stressed the "immense importance" of the potential, but he does not mention any vector form of potential. Maxwell mentions some of these details in Article 16 of the *Treatise*.

Our main concern is not the concept "potential" itself; indeed this study is only a piece of such a longer undertaking. There are at least four aspects of the use of "potential" that should be mentioned, however. First, $A$ is said to be the potential of $B$ when

$$
A = B/r,
$$

where $r$ is a distance.

The expression on the right might be summed or integrated to take account of a number of "sources." This is the use in Maxwell's January 1871 letter to Tait; Thomson attributes this potential concept to Green. Second, $C$ is said to be the potential of $D$, an entity with three components, when the components of $D$ (except possibly for sign) are the spatial derivatives of $C$. Thus in Article 16 of Volume I of the *Treatise* Maxwell says,

> ... the vector quantity, whose components are $X$, $Y$, $Z$, is said to have
> a potential $\psi$, if
>
> $$
> X = -\left(\frac{d\psi}{dx}\right), \qquad
> Y = -\left(\frac{d\psi}{dy}\right), \qquad
> Z = -\left(\frac{d\psi}{dz}\right).
> $$

This "model" is based on the relations between potential and force in mechanics. Both of these meanings are explicitly used by Maxwell and the followers of Maxwell. As we will see immediately, Maxwell introduces a third sense. Finally there is the modern sense, that potentials are functions whose derivatives (not necessarily first derivatives) in various combinations give the quantities we are interested in. This includes the case just mentioned, but allows a wider use of the term "potential."

Maxwell is concerned with a potential related to a magnetic force, so he is working in the usual situation relating potentials and force, the second of the meanings suggested above. Much earlier in the *Treatise* he used a scalar magnetic potential $V$, and he reminds us of it toward the end of Article 406, writing the quaternion relation between the magnetic force and this potential $\mathfrak{H} = -\nabla V$. The reader should be cautioned that the right-hand side in this equation and the equation in the next quotation is the quaternion product of Hamilton's quaternion operator $\nabla$ with a quaternion, either a scalar or a vector. The conclusion of this section explains the choice of the name "vector potential":

> It appears from the present investigation that the magnetic induction $\mathfrak{B}$
> is derived from the vector-potential $\mathfrak{A}$ by the application of the same operator,
> and that the result is true within the magnet as well as without it.
>
> The application of this operator to a vector-function produces, in general,
> a scalar quantity as well as a vector. The scalar part, however, which we have
> called the convergence of the vector-function, vanished when the vector-function
> satisfies the solenoidal condition
>
> $$
> \frac{dF}{d\xi} + \frac{dG}{d\eta} + \frac{dH}{d\zeta} = 0.
> $$

By differentiating the expressions for $F$, $G$, $H$ in equations 22 [the general expressions mentioned above], we find that this question is satisfied by these quantities.

We may therefore write the relation between the magnetic induction and its vector-potential

$$
\mathfrak{B} = \nabla \mathfrak{A}
$$

which may be expressed in words by saying that the magnetic induction is the curl of its vector potential.

From this passage we see that the new name derives indirectly from Maxwell's recent acquaintance with quaternion notation; the two expressions do *not* have identical forms in the component notation, nor are they similar in modern vector notation. This similarity depends on what we would call today a gauge condition, making the scalar part of the quaternion product, the divergence of the vector-potential, zero. "Curl" is a name of Maxwell's invention. So the third sense of potential is that $A$ is the potential of $B$ when $B$ is the quaternion product of $\nabla$ and $A$. In Article 17 Maxwell used this relation in the scalar sense only: "The geometrical nature of the relation between the potential and the vector thus derived from it receives a great light from Hamilton's discovery of the form of the operator by which the vector is derived from the potential."

Articles 416 and 422 continue to employ the "new" quantity, now using just the component notation. In Article 540, following a discussion of induction of circuits, we encounter a familiar note:

> The conception of such a quantity, on the changes of which, and not on
> its absolute magnitude, the induction current depends, occurred to Faraday
> at an early stage of his researches. He observed that the secondary circuit,
> when at rest in an electromagnetic field which remains of constant intensity,
> does not show any electrical effect, whereas, if the same state of the field had
> been suddenly produced, there would have been a current. Again, if the
> primary circuit is removed from the field, or the magnetic forces abolished,
> there is a current of the opposite kind. He therefore recognized in the secondary
> circuit, within the electromagnetic field, a "peculiar condition of matter"
> to which he gave the name of the Electrotonic State. He afterwards found that
> he could dispense with this idea by means of considerations founded on the
> lines of magnetic force, but even in his latest researches, he says, "Again and
> again the idea of an *electrotonic state* has been forced upon my mind."
>
> The whole history of this idea in the mind of Faraday, as shewn in his
> published researches, is well worthy of study. By a course of experiments,
> guided by intense application of thought, but without the aid of mathematical
> calculation, he was led to recognize the existence of something which
> we now know to be a mathematical quantity, and which may even be called
> the fundamental quantity in the theory of electromagnetism. But as he was
> led up to this conception by a purely experimental path, he ascribed to it
> physical existence, and supposed it to be a peculiar condition of matter,
> though he was ready to abandon this theory as soon as he could explain the
> phenomena by any more familiar forms of thought. Other investigators were
> long afterwards led up to the same idea by a purely mathematical path, but,
> so far as I know, none of them recognized, in the refined mathematical idea
> of the potential of two circuits, Faraday's bold hypothesis of an electrotonic
> state.

We have quoted this long passage because of its close connection with our principal theme. First we note that unlike today's attitude, Maxwell stresses the great importance of the vector potential; he calls it "the fundamental quantity in the theory of electromagnetism." But at the same time Maxwell uses a distinction which the later detractors of the vector potential were to seize upon, the distinction between mathematical and physical quantities. We cannot tell precisely what Maxwell means by this dichotomy, but it seems clear from the context that the designation of the potential as a "mathematical quantity" is not a derogatory comment about the potential. Hence his meaning of "mathematical" and "physical" may well be different from later contrasts between the two. Furthermore, Maxwell is not ruling out the possibility that the vector potential has a physical meaning also.

Chapter 8 begins with familiar considerations concerning current, using the potential of two circuits. He comments in Article 590:

> The vector $\mathfrak{A}$ represents in direction and magnitude the time-integral of
> the electromotive force which a particle placed at the point $x$, $y$, $z$ would
> experience if the primary current were suddenly stopped. We shall therefore
> call it the Electrokinetic Momentum *at the point* $x$, $y$, $z$. It is identical with
> the quantity which we investigated in Art. 405 under the name of the vector-potential
> of magnetic induction.

This is a fourth name, although it differs only slightly from the electromagnetic momentum. Earlier in the article a scalar $p$, the line integral of $\mathfrak{A}$ around a circuit, is called the electrokinetic momentum at a point and these defining equations, Equations A, become the first of the general equations of the electromagnetic field in the form they take in the *Treatise*. In succeeding sections Maxwell develops the remaining fundamental equations.

We have already suggested the similarity between the section of the *Treatise* concerning the general equations of the electromagnetic field and the 1865 paper. These equations in their component notations are stated not in one place, but during a running commentary of two chapters. In the second chapter, "General Equations of the Electromagnetic Field," he starts with the vector potential, repeating the remarks quoted above. At the beginning of the chapter, "We have not ... obtained any data for determining either $\mathfrak{A}$ or $\mathfrak{B}$ from the distribution of currents ...," but at the end he says:

> We may therefore adopt, as a definition of $\mathfrak{A}$ that it is the vector potential
> of the electric current, standing in the same relation to the electric current
> that the scalar potential stands to the matter of which it is the potential, and
> obtained by a similar process of integration, which may be thus described:
> From a given point let a vector be drawn, representing in magnitude and
> direction a given element of an electric current, divided by the numerical
> value of the distance of the element from the given point. Let this be done
> for every element of the electric current. The resultant of all the vectors thus
> found is the potential of the whole current. Since the current is a vector
> quantity, its potential is also a vector.[^22]

Again a slightly new name appears in that $\mathfrak{A}$ is now the vector potential of the *electric current*, and the name is justified through similarities with the scalar potential, using the first sense of the meaning of potential mentioned above. He immediately proceeds to list the basic equations in a quaternion notation. On Maxwell's list of the "principal vectors we have to consider" the second one is "the electromagnetic momentum at a point"; both the Gothic $\mathfrak{A}$ and the components $F$, $G$, and $H$ are listed.

After Maxwell has stated the basic equation in the quaternion notation, there is a brief chapter on units. He groups the quantities of electromagnetic theory, giving three pairs of scalar quantities and then three pairs of quaternion quantities. The first vector pair is the "electrostatic pair," the $D$ and $E$ vectors; the second pair is the "magnetic pair," the $B$ and $H$ vectors; the third pair is the "electrokinetic pair," the first being "the intensity of electric current at a point" and the second the "vector potential of electric currents." Thus again Maxwell groups the vector potential with the fundamental quantities on an equal basis. A few pages later in his list of dimensions, electrostatic and electromagnetic units are given for the vector potential.

The only subsequent appearance of the vector potential in the *Treatise* we shall mention is its important role in Chapter 20, "The Electromagnetic Theory of Light." As might be expected, this is a focal chapter. Maxwell shows, as he did in his 1865 paper, that electromagnetic waves are a consequence of his equations and that the velocity of these waves is just the velocity of light. The vector potential is very prominent. Equations 9 are the wave equations for the components $F$, $G$, and $H$ for a nonconducting medium; later these are solved for plane waves in the $z$ direction with the usual sum of functions depending on $(z-vt)$ and $(z+vt)$ respectively. In working with the crystallized medium, it is again the potentials that play the major role in the development, and the same is true in treating the conducting medium. Wave equations for the vectors of the electric and magnetic fields do not occur at this point, but their propagation is discussed.

## Conclusions

We will briefly summarize the conclusions. The vector potential has as its conceptual origin, stressed over and over again by Maxwell, Faraday's electrotonic state; mathematical details are related to those in Green, Stokes, and Thomson. But it is less clear to me why Maxwell so often changed the name he attached to the quantity. In each case the rationale for the choice of name is easy to follow, but the *need* for changes remains unexplained; perhaps it is significant to note that the other electromagnetic quantities do not have evolving names.

We have Maxwell's own word that this quantity is one of the most important in electromagnetic theory. Nowhere does he imply, as far as I have been able to ascertain, the modern attitude that the vector potential is only a device for generating solutions to the basic equations. It occurs explicitly in Maxwell's general equations of the electromagnetic field in both presentations and is important in the development of the equations in the *Treatise*. Furthermore, it is used heavily by Maxwell in his development of the electromagnetic theory of light. I feel that there is no question that Maxwell viewed the concept not only as important, but as one of his major contributions to electromagnetic theory. In this last regard, one sees that it receives considerably more stress in the *Treatise* than does the displacement current.

Given this discrepancy in the role of the vector potential in electromagnetic theory, one naturally wonders where the currently common attitude began. The form of electromagnetic theory which was used from around 1895 was that developed by Hertz and Heaviside.[^23] Both wrote the fundamental equations with no potentials, and Heaviside in particular stressed the electric and magnetic symmetry of the equations. Both came to regard the potentials as secondary quantities. I intend to study this change in attitude concerning the vector potential in another paper.

Later workers in electromagnetic theory seldom returned to Maxwell. We close with two examples out of many possibilities. Andrew Gray's *Treatise*[^24] of 1898, which acknowledged in its preface a great debt to Heaviside, is already in the modern tradition:

> The use of the vector-potential is sometimes convenient as an analytical
> expedient. But it is not a physical quantity which can be observed experimentally,
> and its use is sometimes attended with difficulty owing to the
> introduction of certain arbitrary functions which there is some trouble in
> interpreting.

Finally, when Larmor[^25] wrote *Aether and Matter* in 1900 there was no hint of Maxwell's attitude: "... it has merely been found desirable, for analytic simplification, to introduce these auxiliary functions, $\psi$, $F$, $G$, $H$, which do not represent actual physical quantities."

[^*]: Reed College. This project was supported by a grant from the National Science Foundation.
[^1]: D. Bohm and Y. Ahanorov, *Physical Review*, 1959, 115:485.
[^2]: J. Larmor, ed., *Origins of Clerk Maxwell's Electrical Ideas as Described in Familiar Letters to William Thomson* (Cambridge: Cambridge Univ. Press, 1937).
[^3]: James Clerk Maxwell, "On Faraday's Lines of Force," *Cambridge Philosophical Transactions*, 1856, 10:27-83.
[^4]: Faraday's changing views toward the electrotonic states are discussed in L. Pearce Williams, *Michael Faraday* (New York: Basic Books, 1965).
[^5]: "On Faraday's Lines ... ," p. 51.
[^6]: Ibid., p. 52.
[^7]: Ibid., p. 63.
[^8]: Ibid., p. 65.
[^9]: E. T. Whittaker, *History of the Theories of Aether and Electricity* (London: Longmans, Green, 1910), p. 272.
[^10]: William Thomson, "A Mathematical Theory of Magnetism," *Philosophical Transactions of the Royal Society*, 1851, 141:243-285. Maxwell refers to p. 283. Also in Thomson, *Reprint of Papers on Electricity and Magnetism* (London: Macmillan, 1872).
[^11]: "On Faraday's Lines ... ," p. 67.
[^12]: Maxwell, "On Physical Lines of Force," *Philosophical Magazine and Journal of Science*, Pt. I of the paper, 1861, 21:161-175; Pt. II of the paper, 1861, 21:281-291 and 338-348; Pt. III, 1862, 23:12-24; Pt. IV, 1862, 23:85-95.
[^13]: Ibid., Pt. I, 1861, 21:162.
[^14]: Ibid., Pt. II, 1861, 21:291.
[^15]: Maxwell, "A Dynamical Theory of the Electromagnetic Field," *Phil. Trans.*, 1865 (read in 1864), 155:459-512.
[^16]: Ibid., p. 471.
[^17]: Maxwell, "On a Method of Making a Direct Comparison of Electrostatic with Electromagnetic Force; with a Note on the Electromagnetic Theory of Light," *Phil. Trans.*, 1868, 157:643-657.
[^18]: The Maxwell-Tait correspondence is in the University Library, Cambridge. I should like to thank the librarian for access to this collection.
[^19]: Maxwell, *A Treatise on Electricity and Magnetism* (Oxford: Oxford Univ. Press; 1st ed., 1873; 2nd ed., 1881; 3rd ed., 1892).
[^20]: Article numbers refer to the 1881 2nd ed.
[^21]: William Thomson and P. G. Tait, *Treatise on Natural Philosophy* (Cambridge: Cambridge Univ. Press, 1879). Reprinted as *Principles of Mechanics and Dynamics* (New York: Dover, 1962).
[^22]: Art. 617.
[^23]: Alfred M. Bork, "Maxwell, Displacement Current, and Symmetry," *American Journal of Physics*, 1963, 31:854-859.
[^24]: Andrew Gray, *A Treatise on Magnetism and Electricity* (London: Macmillan, 1898).
[^25]: Larmor, *Aether and Matter* (Cambridge: Cambridge Univ. Press, 1900).
