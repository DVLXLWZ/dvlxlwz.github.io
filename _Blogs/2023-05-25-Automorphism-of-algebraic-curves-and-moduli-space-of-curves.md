---
title: "Primer: Automorphisms of algebraic curves and moduli space of curves"
collection: Blogs
permalink: /Blogs/2023-05-25-Automorphisms-of-algebraic-curves-and-moduli-space-of-curves
excerpt_separator: <!--more-->
date: 2023-05-25
---
Here we will introduce some well-known results about the automorphisms of algebraic curves over an algebraic closed field $k$ and their relations between the moduli space of curves.
<!--more-->

## For $g=0$
If $X$ be a proper smooth curve of genus $0$ over an algebraic closed field $k$, then one can easy to see $X\cong\mathbb{P}^1$ as any two points in $X$ are linear equivalent (consider Jacobian variety). Then we can easy to see that $\mathrm{Aut}(X)=\mathrm{PGL}\_2$. Moreover, if we consider the subgroup fixed $n$ points in $X$, then this subgroup is finite if and only if $n\geq 3$ by easy linear algebra.

## For $g=1$
Let $X$ be a proper smooth curve of genus $1$ over an algebraic closed field $k$. As $X$ is a group variety, then any closed point in $X$ can act on $X$ which forms an automorphism. Hence $\mathrm{Aut}(X)$ is also an infinity group! But if we consider the subgroup fixed $1$ points in $X$, that is, the automorphism group of elliptic curves, then we have:

> **Theorem 1.**

## For $g\geq 2$
Let $X$ be a proper smooth curve of genus $g\geq 2$ over an algebraic closed field $k$. We have the following well-known result:

> **Theorem 2.** The group $\mathrm{Aut}(X)$ is finite.

> *Proof 1. Deformation theory.* We need two following lemmas:
>
>> **Lemma A.** If $X$ be a proper smooth curve, then $\underline{\mathrm{Aut}}(X)\to\mathrm{Spec}k$ is unramified if and only if $\mathrm{Der}\_k(\mathscr{O}\_X,\mathscr{O}\_X)=0$.
>> 
>> *Proof of Lemma A.* Actually $\underline{\mathrm{Aut}}(X)\to\mathrm{Spec}k$ is unramified if and only if $\Omega\_{\underline{\mathrm{Aut}}(X)/k}=0$ if and only if $T\_{\underline{\mathrm{Aut}}(X)/k}=0$ if and only if any automorphism $\alpha:X\times_k\mathrm{Spec}k[\varepsilon]\to X\times_k\mathrm{Spec}k[\varepsilon]$ over $\mathrm{Spec}k[\varepsilon]$ whose restriction to $\mathrm{Spec}k$ is $id$. By [St 0DY9](https://stacks.math.columbia.edu/tag/0DY9) this if and only if $\mathrm{Der}\_k(\mathscr{O}\_X,\mathscr{O}\_X)=0$. $\blacksquare$
>>
>> **Lemma B.** If $X$ be a proper smooth curve of genus $g\geq 2$ over an algebraic closed field $k$, then $\mathrm{Der}\_k(\mathscr{O}\_X,\mathscr{O}\_X)=0$.
>> 
>> *Proof of Lemma B.* As $\deg (T\_{X/k})=2-2g<0$, we get 
>> 
>> $$
>> \mathrm{Der}\_k(\mathscr{O}\_X,\mathscr{O}\_X)=\hom\_{\mathscr{O}\_X}(\Omega\_{X/k},\mathscr{O}\_X)=\Gamma(X,T\_{X/k})=0.
>> $$
>> 
>> Well done. $\blacksquare$
>
> Then the proof finish by Lemma A and B. $\blacksquare$

> *Proof 2. Using ramification and hyperosculations (for charactristic zero).*

> *Proof 3. Using graph trick and numerical equivalence.*

Moreover, for $\mathrm{char}(k)=0$, we have:

> **Theorem 3.** If $X$ be a proper smooth curve of genus $g\geq 2$ over an algebraic closed field $k$ with $\mathrm{char}(k)=0$, then $\sharp(\mathrm{Aut}(X))\leq 84g − 84$.

> *Proof.*

## Moduli space of curves
