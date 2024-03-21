---
title: "About Cones and Singularities"
collection: Blogs
permalink: /Blogs/2024-03-21-About-Cones-and-Singularities
excerpt_separator: <!--more-->
date: 2024-03-21
---
Here we will introduce some well-known results about the cones which is the simplest examples of terminal, canonical, etc. singularities.
Here we will follow the book [Kol13][^1].
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

**[Remark 1.2]** Note that we let $X\subset\mathbb{P}^n$, then we also have the classical affine cone in $\mathbb{A}^{n+1}$ and its closure $\mathsf{PC}(X)$ in $\mathbb{P}^{n+1}$ which is the classical projective cone (see also the more general case of classical cones in [GW1][^2]). Now consider $\mathsf{PC}(X,\mathscr{O}(1))\to\mathsf{PC}(X)$ is a natural finite morphism which is an isomorphism away from the vertex. If $X$ normal, then this is a normalization. So an advantage of our general notion is that if $X$ is normal (resp. S2) then
$\mathsf{AC}(X,\mathscr{L})$ and $\mathsf{PC}(X,\mathscr{L})$ are also normal (resp. S2). $\blacktriangleleft$

Now we a natural partial resolution in both cases:

(i) We have

$$
p_A:\mathsf{BAC}(X,\mathscr{L}):=\underline{\mathrm{Spec}}_X \bigoplus_{m\geq0}\mathscr{L}^{\otimes m}\to\mathsf{AC}(X,\mathscr{L})=\mathrm{Spec}\bigoplus_{m\geq0}H^0(X,\mathscr{L}^{\otimes m})
$$

which is an isomorphism over the punctured affine cone $\mathsf{AC}(X,\mathscr{L})\backslash\{\text{vertex}\}$. The exceptional divisor is $E\cong X$.

(ii) We have 

$$
p_P:\mathsf{BPC}(X,\mathscr{L}):=\underline{\mathrm{Proj}}_X\bigoplus_{m\geq0}\left(\bigoplus_{r=0}^m \mathscr{L}^{\otimes r}\otimes\mathscr{O}_X^{\oplus m-r}\right)\to\mathsf{PC}(X,\mathscr{L})=\mathrm{Proj}\bigoplus_{m\geq0}\left(\bigoplus_{r=0}^m H^0(X,\mathscr{L}^{\otimes r})x^{m-r}\right).
$$

Now we will discuss some more results about them and we mainly focus on $\mathsf{AC}(X,\mathscr{L})$.





[^1]: [Kol13] János Kollár. Singularities of the Minimal Model Program. Cambridge University Press, 2013.

[^2]: [GW1] Ulrich Görtz and Torsten Wedhorn. Algebraic Geometry I: Schemes. Springer Spektrum Wiesbaden, 2020.