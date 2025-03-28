---
title: "A Brief Introduction to the Virtual Intersection Theory"
collection: Blogs
permalink: /Blogs/2025-01-14-A-Brief-Introduction-to-the-Virtual-Intersection-Theory
excerpt_separator: <!--more-->
date: 2025-01-14
---
This is a basic and quick introduction of the virtual intersection theory introduced by [BF97][^2] and [Man12][^4] and give some more properties of these theories.
This generalize the constructions and results in [my notes](https://dvlxlwz.github.io/files/virtual-fundamental-class.pdf).
<!--more-->

## 0. Background and History

The virtual intersection theory comes from the goal to define the modern enumerative invariants. The most fundamental philosophy in the area of enumerative geometry is that, we need to consider the intersection theory 
in the moduli space of the objects you want to consider.
We have seen this in the problems of classical enumerative geometry:

> **Example 0.1.** For example, for a general cubic $3$-fold $X$, the Fano scheme $F(X)$ (Hilbert scheme of lines) consist of several isolated
reduced points. So what we count is 
\\[N=\int_{[F(X)]}1=27,\\] 
where $[F(X)]$ is the fundamental class of $F(X)$.

But note also that the most of the modern enumerative geometry come from the physics, especially the string theory. Recall that in the world of string theory, general relativity and quantum mechanics are unified at a cost:
\\[\mathsf{SpaceTime}=\mathbb R^3\times\mathbb R^1\times X\\]
where $X$ is a Calabi-Yau $3$-fold which has an extra dimension. So in string theory, our world consist of $4$-dimensional space time 
and a real $6$-dimensional manifold which is Calabi-Yau which exists in the microcosmos.

An important principle of string theory is:
> Physics in $4$-dim space time = geometry of $X$.

So in order to discover the physics in $4$-dim space time, we need to discover the geometry of the Calabi-Yau $3$-folds.
As the world consist of strings (of $1$-dimensional), we may consider the path of the strings in the Calabi-Yau $3$-fold $X$,
and using this to detect the geometry of $X$.
A path of a string is a world sheet in $X$ and the aim of physist is
to calculate the path integral of strings, in the language
of mathematicians, counting the world sheets in $X$.
Now a world sheet is an algebraic curve of $X$, there are three basic idea to consider this enumerative problem:

> - Consider the Hilbert scheme $\mathrm{Hilb}_{\mathrm{codim2}}(X)$ which consider all curves in $X$.
> - Consider the Gromov-Witten invariants, that is, we consider stable maps from curves to $X$ with fixed homological class of the images
    (as another compactification, we can consider the moduli of
     quasimaps which will be omitted here).
> - Consider the Donaldson-Thomas invariants, that is, we consider the ideal sheaves of $X$ which comes from curves.

All these are some bad moduli spaces by the Murphy's law of moduli spaces. Hence for the spaces $\mathcal M$ we consider
could be very singular and has several components with possibly  different dimensions, for example, the Hilbert schemes. So in the intersection theory,
the fundamental class $[\mathcal M]$ does not exists. So we need to find some (virtual) class $[\mathcal M]^{\text{vir}}$ which can be used in the intersection
theory and counting some objects we want.

The most basic model of these given in the Chapter
14.1 in [Ful98][^5]:
> **Example 0.2.**
Let $Y$ be a algebraic scheme over some field $k$ of pure dimension $n$ and a vector bundle $E$ of rank $e$ over it.
For any section $s:Y\to E$ of bundle $E$, let $Z(s)$ be the zero locus of this section which forms the following fiber product:
> ![ ](/CommutativeDiagrams/2025-01-24-144649.png){: .align-center}
>
>Then we define 
> \\[c\_{\mathrm{loc}}(E,s):=0^![Y]=0^*(C\_{Z(s)/Y})\in\text{CH}\_{n-e}(Z(s))\\] 
>be the **localized Chern class** of $E,s$.

In this example, by the basic theory of refined Gysin-pullbacks we have $i\_*c\_{\mathrm{loc}}(E,s)=c\_e(E)\cap[Y]$. So if $s$ intersect
with zero section transversally, then $[Z(s)]=c\_{\mathrm{loc}}(E,s)=c_e(E)\cap[Y]$ up to pushforward.

In our opinion, we wish our moduli space $\mathcal M$has this form locally (the spaces of this type are called the quasi-smooth scheme/stacks). Then we using the similar idea to perturbthe section to get several localized Chern class and then glue them up. Then we can get the virtual class $[\mathcal M]^{\text{vir}}$.
If it is of dimension zero, then we can define our counting-invariant is 
\\[I(\mathcal M)=\int\_{[\mathcal M]^{\text{vir}}}1.\\]
If is has positive dimension, we can integral some Euler classes of bundles over it.

But it seems that this construction depends on the choice 
of that sections of bundles! To solve this, we will consider 
a two-term chain complex $T\_Y|\_{Z(s)}\to E|\_{Z(s)}$ given by 
$ds|\_{Z(s)}$. We only need these data to recover the construction above. This complex is called the (dual of) obstruction theory.

So by this idea, it seems that we only need to consider  this complex globally and then we can also define the virtual class and then we  need  not to do some gluing-process. This is the basic idea of Behrend–Fantechi's famous work [BF97][^2] to define virtual classes via the perfect obstruction theory.

Finally we discuss some history of these theories. Note that the first goal to define the virtual class is to define the Gromov-Witten invariants algebraically. The first paper defining virtual class and Gromov-Witten invariants (algebraically) is [LT96][^3] due to Li-Tian. Then via papers [Beh97][^1]
and [BF97][^2] of Behrend and Fantechi, these theories are clearly completed.
Then using this we can define Donldsaon-Thomas type invariants and several other invariants.

We denote $\mathbb L\_f$ be the Illusie's total cotangent complex and $L_f:=\tau^{\geq-1}\mathbb L\_f$ be the truncated cotangent complex.

## 1. Deformation to the Intrinsic Normal Cones

To globalize the local model due to Fulton, we need to do the following
two things:
> - We need to generalize the theory of deformation to the normal cone due to Fulton. We need to define the deformation space of any DM-morphism of Artin stacks. In particular, we can define this for $\mathcal M\to\text{Spec}\mathbb C$.
>
> - Globalize the localized Chern classes, and then  we can get the virtual classes.

As we have seen, the cones are main objects in intersection theory in [Ful98][^5] (See [Kre99][^6] for the intersection theory of Artin stacks). In virtual
intersection theory, the cone stacks are the analogous main objects. But the general theory of cone stacks are very complicated
(see [BF97][^2] or [my notes](https://dvlxlwz.github.io/files/virtual-fundamental-class.pdf)), we only select the things we need.

> **Definition 1.1.** Let $X$ be an Artin stack and let $F\in\mathbf D^{\leq0}_{\text{coh}}(X)$. An **abelian cone stack** associated to $F$ is the cone stack
> \\[\mathfrak C(F):=h^1/h^0(F^{\vee}):=[E^1/E^0]\\]
> where $\tau^{[0,1]}(F^{\vee})=[E^0\to E^1]$ and the action of $E^0$ (can be seen via $\underline{\text{Spec}}\text{Sym}$
> to be a group scheme over $X$) on $E^1$ defined via $a:E^0\to E^1$ by $e^0\cdot e^1=a(e^0)+e^1$.

> **Definition 1.2.** For a DM-morphism of Artin stacks $f:X\to Y$, we define its **intrinsic normal sheaf** to be 
> \\[\mathfrak N\_f:=\mathfrak C(\mathbb L\_f)\\]
> for the cotangent comples $\mathbb L\_f\in\mathbf D^{\leq0}_{\text{coh}}(X)$.

This is an analogue of normal sheaves. But we also need the analogue
of normal cones:

> **Definition 1.3.** Let $f:X\to Y$ be a DM-morphism of Artin stacks. We define the **intrinsic normal cone** to be the unique subcone stack
> \\[\mathfrak C\_f\subset\mathfrak N\_f\\]
> satisfying the following property: for any commutative square
> ![ ](/CommutativeDiagrams/2025-01-24-144728.png){: .align-center}
> with smooth vertical arrows, and a closed embedding $f'$, we have a cartesian:
> ![ ](/CommutativeDiagrams/2025-01-24-144748.png){: .align-center}
> for some dotted arrow. Here the map $N\_{f'}\to\mathfrak N\_f$ is induced by the canonical map $\mathbb L\_f|_{X'}\to\mathbb L\_{f'}$.

> **Remark 1.4.** - If $f:X\to Y$ be a closed embedding, then we have
> \\[\mathfrak C\_f=[C\_f/T\_{Y/Y}|_X]=C\_f\subset\mathfrak N\_f=[N\_f/T\_{Y/Y}|_X]=N\_f.\\]
> 
> - Note that if we have global factorization, that is,we have $f:X\subset Y'\to Y$ where $Y'\to Y$ is smooth, then $L\_f=[I/I^2\to\Omega\_{Y'/Y}\|_X]$. Hence we have 
> \\[\mathfrak C\_f=[C\_{X/Y'}/T\_{Y'/Y}\|_X]\subset\mathfrak N\_f=[N\_{X/Y'}/T\_{Y'/Y}\|\_X].\\]
>
> - The commutative square in the definition always exists. Indeed, take any smooth cover $U\to Y$ where $U$ is a scheme, as $f$ is DM-morphism we know that $U\times_YX$ is a Deligne-Mumford stack. Take a étale cover $V\to U\times_YX$ where $V$ is a scheme. Then there always exists a scheme $S$ smooth over the ground field. Then we have the following commutative square:
> ![ ](/CommutativeDiagrams/2025-01-24-144809.png){: .align-center}
> Well done.

Finally we will generalize the method of deformation to the normal cone as we discussed before.

> **Definition 1.5.** For a DM-morphism of Artin stacks $f:X\to Y$, we define the deformation space $M^{\circ}\_f\to\mathbb P^1$ such that there exists $m:X\times\mathbb P^1\to M\_f^{\circ}$ such that $m\_{\neq0}=f$ and $m\_{=0}=0\_{\mathfrak C_f}:X\to\mathfrak C\_f$, as follows:
>
>> - If $f$ is a closed embedding of schemes, then this is Fulton's construction:
>>   \\[M^{\circ}\_f=\text{Bl}\_{X\times\{0\}}(Y\times\mathbb P^1)\backslash\text{Bl}\_{X\times\{0\}}(Y\times\{0\}).\\]
>> - If $f$ is an unramified morphism of algebraic spaces, then we have a commutative diagram
>> ![ ](/CommutativeDiagrams/2025-01-24-144830.png){: .align-center}
>> with étale surjective vertical arrows and a closed embedding $f'$ of schemes $X',Y'$. Then we define
>> \\[M^{\circ}\_f:=[M^{\circ}\_{X'\times_XX'/Y'\times_YY'}\rightrightarrows  M^{\circ}\_{X'/Y'}]\\]
>> where $X'\times_XX'\to X'\times\_YX'$ is base change of $\Delta\_f$ with closed embedding $X'\times\_YX'\subset Y'\times\_YY'$.
>>
>> - If $f$ is a DM-morphism of Artin stacks, then we have a commutative diagram
>> ![ ](/CommutativeDiagrams/2025-01-24-144830.png){: .align-center}
>> with smooth surjective vertical arrows and a closed embedding $f'$ of schemes $X',Y'$. Then we define
>> \\[M^{\circ}\_f:=[M^{\circ}\_{X'\times_XX'/Y'\times_YY'}\rightrightarrows  M^{\circ}\_{X'/Y'}]\\]
>> where $X'\times_XX'\to X'\times\_YX'$ is base change of $\Delta\_f$ (which is unramified) with closed embedding $X'\times\_YX'\subset Y'\times\_YY'$.
>
> This is called the **deformation to the intrinsic normal cone**.

Note that the definition is independent of the choice of these diagrams and we refer [Man12][^4] for the proof.
Moreover, the existence of morphism  $m:X\times\mathbb P^1\to M\_f^{\circ}$ is trivial for the case of closed embedding due to Fulton. Others follows by descent.

Using this, we can define the specialization map which is analogue of Fulton's:

> **Definition 1.6.** Let $f:X\to Y$ be a DM morphism of Artin stacks. We define the **specialization map**
> \\[\mathrm{sp}\_f:\text{CH}\_\*(Y)\to\text{CH}\_\*(\mathfrak C\_f)\\]
> to be the unique map that fits into the commutative diagram
> ![ ](/CommutativeDiagrams/2025-01-24-144848.png){: .align-center}
> for any $\zeta\neq0$.

## 2. Perfect Obstruction Theory and Virtual Classes

In this section we need the natural object to define the ``zero of sections of vector bundles".

> **Definition 2.1.** For a DM-morphism of Artin stacks $f:X\to Y$, an **obstruction theory**
> is a morphism \\[\phi:\mathbb F\to L\_f\\] in $\mathbf D_{\text{coh}}^{\leq0}(X)$ such that $h^0(\phi)$ is bijective and $h^{-1}(\phi)$ is surjective
> where $\mathbb F$ is a perfect complex of tor-amplitude $[-d,0]$ for some $d\in \mathbb Z_{\geq0}$. It is called a **perfect obstruction theory** if $\mathbb F$ is a
> perfect complex of tor-amplitude $[-1,0]$.

By the theory of cone stacks, the condition of obstruction theory is equivalent to that the induced 
$\mathfrak N\_f\to\mathfrak C(\mathbb F)$ is a closed embedding.
Note also that a cone stack $\mathfrak E$ is called a vector bundle stack on $X$,
if $\mathfrak E=\mathfrak C(E)$ for some perfect complex of tor-amplitude $[-1,0]$. In [BF97][^2] they also showed that 
a cone stack is smooth over $X$ if and only if it is a vector bundle stack.

As the ordinary intersection theory, we also have the following:

> **Proposition 2.2.** ([Kre99][^6], Prop. 4.3.2) Let $X$ be an Artin stack with affine stabilizers. Let $\mathfrak E$ be a vector bundle stack on $X$, that is, $\mathfrak E=\mathfrak C(E)$ for some perfect complex of tor-amplitude $[-1,0]$. Then the smooth pullback
> \\[\pi\_{\mathfrak E}^{\*}:\text{CH}\_\*(X)\to\text{CH}\_\*(\mathfrak E)\\]
> is an isomorphism. Hence we can define the **Gysin pullback** is $0\_{\mathfrak E}^!:=(\pi\_{\mathfrak E}^*)^{-1}$.

Finally as the definition of refined Gysin pullback, we can define its analogue:

> **Definition 2.3.** Let $f:X\to Y$ be a DM morphism of Artin stacks and let $\phi:\mathbb F\to L\_f$ be a perfect obstruction theory. Assume that $X$
has affine stabilizers. We define the **virtual pullback** as the composition
> <html>
> <head>
>   <meta charset="utf-8">
>   <meta name="viewport" content="width=device-width">
>   <script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
>   <script id="MathJax-script" async
>           src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js">
>   </script>
> </head>
> <body>
> <p>
> \begin{align*}
> &f^!_{\mathrm{vir}}\colon\mathrm{CH}_*(Y)\stackrel{\mathrm{sp}_f}{\to}\mathrm{CH}_*(\mathfrak C_f)\stackrel{\iota_*}{\to}
> \mathrm{CH}_*(\mathfrak C(F))\stackrel{0^！}{\to}\mathrm{CH}_*(X).
> \end{align*}
> </p>
> </body>
> </html>
> 
>
> If $X$ is a Deligne-Mumford stack over some field $k$ with affine stabilizers and perfect obstruction theory $\phi:\mathbb F\to L\_X$, then the **virtual fundamental class** is \\[[X]\_{\phi}^{\text{vir}}:=p^!\_{\mathrm{vir}}[\text{Spec k}]=0\_{\mathfrak C(\mathbb F)}^!(\mathfrak C\_X)\in\text{CH}\_{\mathrm{vdim}}(X)\\] where $p:X\to\text{Spec} k$ be the structure morphism and $\mathrm{vdim}$ is called the **virtual dimension** of it.

> **Remark 2.4.** For the canonical choice of obstruction theory using derived enhancement. For a moduli stack $M$ (which is Deligne-Mumford) with its derived  moduli stack $\mathbf M$ and canonical embedding $i:M\subset\mathbf M$, usually the cotangent complex $\mathbb L_{\mathbf M}$ has very nice form which induce a  morphism 
> \\[\mathbb L\_{\mathbf M}|_M=i^*\mathbb L\_{\mathbf M}\to\mathbb L\_{M}\\]
> which will be an obstrunction theory. If $\mathbf M$ is quasi-smooth,
> then it is perfect.

Several important properties of virtual pullback.

> **Proposition 2.5.**
>> - Virtual pullback has bivariant properties, that is,
>> it is commute with proper push-forward, flat pull-back and lci Gysin pullback (assume some affineness of stabilizers).
>> - Virtual pullback has functoriality. If we have a commutative diagram of DM-morphisms of Artin stacks
>>  ![ ](/CommutativeDiagrams/2025-01-24-144908.png){: .align-center}
>> such that $X,Y$ have affine stabilizers.
>> Assume that we have a triple $(\phi_f:\mathbb F_f\to L_f,\phi_g:\mathbb F_g\to L_g,\phi_h:\mathbb F_h\to L_h)$ of perfect obstruction theories which is compactible, that is, there exists a morphism of distinguished triangles
>>  ![ ](/CommutativeDiagrams/2025-01-24-144927.png){: .align-center}
>> such that $\phi_f=r\circ\phi_f'$ with canonical map $r:L_f'\to\tau^{\geq-1}L_f=L_f$.
>> Then we have
>> \\[h^!\_{\mathrm{vir}}=f^!\_{\mathrm{vir}}\circ g^!\_{\mathrm{vir}}.\\]


## 3. Torus Localization

## 4. Cosection Localization and Reduced Virtual Classes

## 5. K-theoretic Virtual Structure and Virtual Riemann-Roch

## 6. Find the way to generalize

Note that in the definition of virtual pullbacks, we need two technical assumptions for defining virtual pullbacks:
> - $f:X\to Y$ is DM-morphism;
> - $X$ has affine stabilizers.

Need to add. Using Motivic etale Borel-Moore cohomology.




[^1]: [Beh97] K. Behrend. Gromov–witten invariants in algebraic geometry. Invent. Math., 127:601–617, 1997.

[^2]: [BF97] K. Behrend and B. Fantechi. The intrinsic normal cone. Invent. Math., 128:45–88, 1997.

[^3]: [LT96] Jun Li and Gang Tian. Virtual moduli cycles and gromov–witten invariants of algebraic varieties. J. Amer. Math. Soc., 11:119–174, 1996

[^4]: [Man12] Cristina Manolache. Virtual pull-backs. J. Algebraic Geom., 21:201–245, 2012.

[^5]: [Ful98] William Fulton. Intersection Theory. Springer New York, 1998.

[^6]: [Kre99] Andrew Kresch. Cycle groups for artin stacks. Invent. Math., 138:495–536, 1999



