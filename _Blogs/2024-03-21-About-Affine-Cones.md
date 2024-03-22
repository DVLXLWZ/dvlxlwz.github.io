---
title: "About Affine Cones"
collection: Blogs
permalink: /Blogs/2024-03-21-About-Affine-Cones
excerpt_separator: <!--more-->
date: 2024-03-21
---
Here we will introduce some well-known results about the cones which is the simplest examples of terminal, canonical, etc. singularities.
Here we will follow the book [Kol13][^1]. We just consider $\mathrm{char}(k)=0$.
<!--more-->

## 1. Basic Constructions

> **[Def 1.1]** Let $X$ be a projective scheme with an ample line bundle $\scr{L}$.
>
> (i) The **affine cone over $X$ with conormal bundle $\scr{L}$** is
> 
> $$
> \mathsf{AC}(X,\mathscr{L}):=\mathrm{Spec}\bigoplus_{m\geq0}H^0(X,\mathscr{L}^{\otimes m}).
> $$
>
> (ii) The **projective cone over $X$ with conormal bundle $\scr{L}$** is
> 
> $$
> \mathsf{PC}(X,\mathscr{L}):=\mathrm{Proj}\bigoplus_{m\geq0}\left(\bigoplus_{r=0}^m H^0(X,\mathscr{L}^{\otimes r})x^{m-r}\right).
> $$

**[Remark 1.2]** Note that we let $X\subset\mathbb{P}^n$, then we also have the classical affine cone in $\mathbb{A}^{n+1}$ and its closure $\mathsf{PC}(X)$ in $\mathbb{P}^{n+1}$ which is the classical projective cone (see also the more general case of classical cones in 13.37 in [GW1][^2]). Now consider $\mathsf{PC}(X,\mathscr{O}(1))\to\mathsf{PC}(X)$ is a natural finite morphism which is an isomorphism away from the vertex. If $X$ normal, then this is a normalization. So an advantage of our general notion is that if $X$ is normal (resp. S2) then
$\mathsf{AC}(X,\mathscr{L})$ and $\mathsf{PC}(X,\mathscr{L})$ are also normal (resp. S2). $\blacktriangleleft$

Here we mainly consider $\mathsf{AC}(X,\mathscr{L})$ and we have a natural partial resolution:

> **[Proposition 1.3]** Let $X$ be a projective scheme with an ample line bundle $\scr{L}$. Then we have
>
> $$
> p_A:\mathsf{BAC}(X,\mathscr{L}):=\underline{\mathrm{Spec}}_X \bigoplus_{m\geq0}\mathscr{L}^{\otimes m}\to\mathsf{AC}(X,\mathscr{L})=\mathrm{Spec}\bigoplus_{m\geq0}H^0(X,\mathscr{L}^{\otimes m})
> $$
>
> which is an isomorphism over the punctured affine cone $\mathsf{AC}(X,\mathscr{L})\backslash\{\text{vertex}\}$. The exceptional divisor is $E\cong X$ which is the zero section of $X$ in $\mathsf{BAC}(X,\mathscr{L})$.

[Proof]

**[Remark 1.4]** For projective case we also have the similar construction: we have 

$$
p_P:\mathsf{BPC}(X,\mathscr{L}):=\underline{\mathrm{Proj}}_X\bigoplus_{m\geq0}\left(\bigoplus_{r=0}^m \mathscr{L}^{\otimes r}\otimes\mathscr{O}_X^{\oplus m-r}\right)\to\mathsf{PC}(X,\mathscr{L})=\mathrm{Proj}\bigoplus_{m\geq0}\left(\bigoplus_{r=0}^m H^0(X,\mathscr{L}^{\otimes r})x^{m-r}\right).
$$

## 2. Properties

Now we will discuss some more results about them and we mainly focus on $\mathsf{AC}(X,\mathscr{L})$.

> **[Proposition 2.1]** Let $X$ be a projective scheme with an ample line bundle $\scr{L}$. Then 
> 
> $$
> \mathbf{R}^ip_{A,*}\mathscr{O}_{\mathsf{BAC}(X,\mathscr{L})}\cong\bigoplus_{m\geq0}H^i(X,\mathscr{L}^{\otimes m}).
> $$

[Proof] Now the exceptional divisor is $E$, we let its ideal sheaf is $\mathscr{I}\subset\mathscr{O}_{\mathsf{BAC}(X,\mathscr{L})}$. Actually by construction of $\mathsf{BAC}(X,\mathscr{L})$, we can easy to see that

$$
\mathscr{O}_{\mathsf{BAC}(X,\mathscr{L})}/\mathscr{I}^m\cong\mathscr{O}_X\oplus\mathscr{L}\oplus\cdots\oplus\mathscr{L}^{\otimes m-1}.
$$

Hence by Theorem on formal functions (c.f. Chapter 24 in [GW2][^3])

> **[Proposition 2.2]** Let $X$ be a normal projective variety with an ample line bundle $\scr{L}$. Then
>
> (i) We have $\mathrm{Pic}(\mathsf{AC}(X,\mathscr{L}))=0$ and $\mathrm{Cl}(\mathsf{AC}(X,\mathscr{L}))=\mathrm{Cl}(X)/\mathbb{Z}\cdot\mathscr{L}$.
>
> (ii) Let $\Delta\_X$ be a $\mathbb{Q}$-divisor on $X$. By pull-back, we get $\mathbb{Q}$-divisors $\Delta_{\mathsf{AC}(X,\mathscr{L})}$ and $\Delta_{\mathsf{BAC}(X,\mathscr{L})}$. Assume that $K_X + \Delta_X$ is $\mathbb{Q}$-Cartier. Then we have
> 
> $$
> K_{\mathsf{BAC}(X,\mathscr{L})}+\Delta_{\mathsf{BAC}(X,\mathscr{L})}=\pi^*(K_X+\Delta_X)-E
> $$
>
> where $\pi:\mathsf{BAC}(X,\mathscr{L})\to X$ is projection from the vertex and $E\cong X$ is the exceptional divisor of $p_A$.

[Proof] 

> **[Proposition 2.3]** Let $X$ be a Cohen-Macaulay projective variety with an ample line bundle $\scr{L}$. Then $\mathsf{AC}(X,\mathscr{L})$ is Cohen-Macaulay if and only if $H^i(X,\mathscr{L}^{\otimes m})=0$ for any $m$ and any $0<i<\dim X$.

[Proof]

> **[Proposition 2.4]** Let $X$ be projective variety with rational singularities with an ample line bundle $\scr{L}$. Then the cone $\mathsf{AC}(X,\mathscr{L})$ has rational singularities if and only if $H^i(X,\mathscr{L}^{\otimes m})=0$ for any $m$ and any $0<i\leq\dim X$.

[Proof]

**[Example 2.5]** Here we will introduce a log-canonical (lc) pair which is not a rational singularity and not Cohen-Macaulay using our theory.


[^1]: [Kol13] János Kollár. Singularities of the Minimal Model Program. Cambridge University Press, 2013.

[^2]: [GW1] Ulrich Görtz and Torsten Wedhorn. Algebraic Geometry I: Schemes. Springer Spektrum Wiesbaden, 2020.

[^3]: [GW2] Ulrich Görtz and Torsten Wedhorn. Algebraic Geometry II: Cohomology of Schemes. Springer Spektrum Wiesbaden, 2023.
