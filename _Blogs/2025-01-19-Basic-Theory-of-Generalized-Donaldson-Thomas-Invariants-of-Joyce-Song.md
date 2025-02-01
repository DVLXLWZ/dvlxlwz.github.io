---
title: "Basic Theory of the Generalized Donaldson-Thomas Invariants of Joyce-Song"
collection: Blogs
permalink: /Blogs/2025-01-19-Basic-Theory-of-Generalized-Donaldson-Thomas-Invariants-of-Joyce-Song
excerpt_separator: <!--more-->
date: 2025-01-19
---
This is a basic and quick introduction of the theory of generalized Donaldson-Thomas invariants of strict Calabi-Yau $3$-folds due to Joyce-Song
in [JS11][^1]. We work over $\mathbb C$, although these also work over any algebraically closed field of characteristic zero.

<!--more-->

## 0. Review of Donaldson-Thomas Invariants of Calabi-Yau $3$-folds

> **Definition 0.1.** A **Calabi-Yau manifold** is a smooth projective variety $X$ over $\mathbb C$ such that $K\_X\cong\mathscr O\_X$.
> A **strict Calabi-Yau manifold** is a Calabi-Yau manifold $X$ such that $H^i(X,\mathscr O\_X)=0$ for any $0<i<\dim X$.

Then we fix a Calabi-Yau $3$-fold $X$ with a very ample line bundle $\mathscr O\_X(1)$ and a Gieseker stability condition $(\tau,G,\leq)$. Consider the moduli stack of semistable sheaves $\mathcal M^{\alpha\text{-ss}}(\tau)$ for some $\alpha\in K^{\text{num}}(\text{coh}(X))$. Then it is a proper Artin stack
with a projective good moduli space $ M^{\alpha\text{-ss}}(\tau)$. They contain open locus of stable objects $\mathcal M^{\alpha\text{-st}}(\tau)\subset\mathcal M^{\alpha\text{-ss}}(\tau)$ and $M^{\alpha\text{-st}}(\tau)\subset M^{\alpha\text{-ss}}(\tau)$ which need not be proper.

We can show that there is a perfect obstruction theory of $\mathcal M^{\alpha\text{-ss}}(\tau)$ (and hence $\mathcal M^{\alpha\text{-st}}(\tau)$) comes from their derived enhancement. This is a general fact:

> **Theorem 0.2.** Let $X$ be a smooth projective variety of dimension $n$. Then the natural derived moduli stack $\mathbb R\underline{Coh}(X)$ has cotangent complex \\[\mathbb L\_{\mathbb R\underline{Coh}(X)}\cong(\mathbb R\mathscr Hom\_{\pi}(\mathbb F,\mathbb F)[1])^{\vee}\cong\mathbb R\mathscr Hom\_{\pi}(\mathbb F,\mathbb F\otimes\omega\_X)[n-1]\\]
> where $\pi:\mathbb R\underline{Coh}(X)\times X\to\mathbb R\underline{Coh}(X)$ and universal sheaf $\mathbb F$ which induce an obstruction theory $\mathbb L\_{\mathbb R\underline{Coh}(X)}|_{\underline{Coh}(X)}\to\mathbb L\_{\underline{Coh}(X)}$.

Hence by this fact, we know that for the Calabi-Yau $3$-fold $X$, $\mathcal M^{\alpha\text{-ss}}(\tau)$ (and hence $\mathcal M^{\alpha\text{-st}}(\tau)$) has
a perfect obstruction theory. But by the theory of Behrend–Fantechi or general virtual pullbacks (see [virtual-blog](https://dvlxlwz.github.io//Blogs/2025-01-14-A-Brief-Introduction-to-the-Virtual-Intersection-Theory) for the introduction), the virtual classes can not construct over a general Artin stack which is not Deligne-Mumfold. However, the good moduli space $\mathcal M^{\alpha\text{-st}}(\tau)\to M^{\alpha\text{-st}}(\tau)$ is actually a $B\mathbb G_m$-gerbe and we can descend the obstruction theory of $\mathcal M^{\alpha\text{-st}}(\tau)$ to $M^{\alpha\text{-st}}(\tau)$, up to some twist (but the $\mathbb R\mathscr Hom(\mathbb F,\mathbb F)$ does not change after the twist). Hence by the theory of Behrend–Fantechi, we get a virtual class 
\\[[M^{\alpha\text{-st}}(\tau)]^{\text{vir}}\in\text{CH}_0(M^{\alpha\text{-st}}(\tau)).\\]

> **Definition 0.3.** For a Calabi-Yau $3$-fold $X$ such that $M^{\alpha\text{-ss}}(\tau)=M^{\alpha\text{-st}}(\tau)$, the **Donnaldson-Thomas invariants** is defined by \\[\text{DT}^{\alpha}(\tau):=\int\_{[M^{\alpha\text{-st}}(\tau)]^{\text{vir}}}1\in\mathbb Z.\\]

The goal of generalized Donaldson-Thomas invariants is to define the DT invariant for any $\alpha$ even $M^{\alpha\text{-ss}}(\tau)\neq M^{\alpha\text{-st}}(\tau)$.
The idea comes from another description of DT invariants of Calabi-Yau $3$-fold $X$ such that $M^{\alpha\text{-ss}}(\tau)=M^{\alpha\text{-st}}(\tau)$.

This description follows from a function, we call it the Behrend function:

> **Definition 0.4.** Let $X$ a finite type $\mathbb C$-scheme. Suppose $X\subset M$ is an embedding of $X$ as a closed subscheme of a smooth scheme $M$. Let $C_XM$ be the normal cone with projection $\pi: C\_XM\to X$. Define the **distinguished cycle** is \\[\mathfrak c\_{X/M}=\sum\_{C'}(-1)^{\dim\pi(C')}\mathrm{mult}(C')\pi(C')\in Z_*(X)\\]
> where the sum is over all irreducible components $C'$ of $C\_XM$. One can show that this determined by $X$ uniquely, so we let $\mathfrak c\_{X}=\mathfrak c\_{X/M}$.
>
> Write $\text{CF}\_{\mathbb Z}(X)$ for the group of $\mathbb Z$-valued constructible functions on $X$. The **local Euler obstruction** is a group isomorphism $\text{Eu}:Z_*(X)\to\text{CF}\_{\mathbb Z}(X)$ defined as: if $V$ is a prime cycle on $X$, then \\[\text{Eu}:V\mapsto\left(x\mapsto\int\_{\mu^{-1}(x)}c(\tilde{T})\cap s(\mu^{-1}(x),\tilde{V})\right)\\]
> where $\mu:\tilde{V}\to V$ be the Nash blowup of $V$ with dual of universal quotient bundle $\tilde{T}$. Finally, we define the **Behrend function** as
> \\[\nu_X:=\text{Eu}(\mathfrak c\_{X})\in\text{CF}(X).\\]

> **Small Remark.** For the Nash blowup we refer to see Example 4.2.9 in [2022-12-12-blogs](https://dvlxlwz.github.io//Blogs/2022-12-12-Some-Gaps-and-Examples-in-Intersection-Theory-by-Fulton-I) and the refs in it.

Then we have the following fact:

> **Theorem 0.5.** (Behrend) Let $M$ be a proper $\mathbb C$-scheme with a symmetric perfect obstruction theory, then 
> \\[\int\_{[M]^{\text{vir}}}1=\chi(X,\nu\_X):=\sum\_{k\in\mathbb Z}k\chi(\nu\_X^{-1}(k)).\\]

> **Remark 0.6.** Here although we do not prove this theorem, we can give some idea of the reason why this result is true.
> Here we focus on the case that consider the Calabi-Yau $3$-fold $X$ and $M:=M^{\alpha\text{-ss}}(\tau)=M^{\alpha\text{-st}}(\tau)$.
> By the works of derived symplectic geometry in [BBJ19][^2], the moduli space $M$ is known to be locally written as critical loci of some function. That is for each point $p\in M$, there is an open neighborhood $p\in U$ such that $U\cong\mathrm{Crit}(w)$ where $Y$ is a smooth scheme and $w$ is a regular function on it.
> So we need to consider the geometry of critical locus.
>
> Let $U$ be a complex manifold with a holomorphic function $f:U\to\mathbb C$. Then we can show that
> \\[\nu\_{\mathrm{Crit}(f)}(x)=(-1)^{\dim U}(1-\text{MF}_f(x)),\quad x\in\mathrm{Crit}(f).\\]
> Then as the virtual locus is just the perturb the section locally to give a nice zero locus, here Behrend function is also given by some perturbing, that is, the Milnor fibres. Of course, as a generalization of Milnor fibres, we can using vanishing cycle to give another description. As in [JS11][^1] Theorem 4.9, we have
> \\[\chi\_{U\_0}(\phi\_f(\underline{\mathbb Q}[n-1]))(x)=\nu\_{\mathrm{Crit}(f)}(x),\quad x\in\mathrm{Crit}(f)\\]
> where $\phi\_f$ be the vanishing-cycle functor.

However, when $M^{\alpha\text{-ss}}(\tau)\neq M^{\alpha\text{-st}}(\tau)$, then locally $M^{\alpha\text{-ss}}(\tau)$ is not a critical locus. But it is for moduli stack $\mathcal M^{\alpha\text{-ss}}(\tau)$! So we need to consider the Behrend function on Artin stacks. But  it is not obvious how to take
its weighted Euler characteristics. For example, let us take $\alpha$ with Hilbert polynomial $P = (2, 0, 0, 0)$ so that the only semistable sheaf is $\mathscr O\_X^{\oplus 2}$. Then $\mathcal M^{\alpha\text{-ss}}(\tau)\cong B\text{GL}\_2(\mathbb C)$. Their euler number can not defined $1/(\chi(\text{GL}\_2(\mathbb C)))$
or its $\mathbb C^*$-rigidification $1/(\chi(\text{PGL}\_2(\mathbb C)))$
as $\chi(\text{GL}\_2(\mathbb C))=\chi(\text{PGL}\_2(\mathbb C))=0$.

An issue caused here is that, for a strictly semistable sheaf $E$, the dimension of the maximal torus of $\text{Aut}(E)$ is greater than one. A crucial idea in Joyce  is that, by taking the **logarithm** of the moduli stack $\mathcal M^{\alpha\text{-ss}}(\tau)$, we can regard it as a **virtual**
stack whose stabilizer groups have one-dimensional maximal torus. Then by getting
rid of the one-dimensional maximal torus and integrating over the Behrend function,
the desired DT invariant (called generalized DT invariant) is defined.


## 1. Constructible Functions and Stack Functions

Here are some basic definitions we need in the whole theory.

### 1.1. Constructible Functions

> **Definition 1.1.** Let $\mathbb{K}$ be an algebraically closed field of characteristic zero, and $\mathfrak{F}$ an Artin $\mathbb{K}$-stack. We call $C \subseteq \mathfrak{F}(\mathbb{K})$ constructible if $C = \bigcup_{i \in I} \mathfrak{F}_i(\mathbb{K})$, where $\{\mathfrak{F}_i : i \in I\}$ is a finite collection of finite type Artin $\mathbb{K}$-substacks $\mathfrak{F}_i$ of $\mathfrak{F}$. We call $S \subseteq \mathfrak{F}(\mathbb{K})$ locally constructible if $S \cap C$ is constructible for all constructible $C \subseteq \mathfrak{F}(\mathbb{K})$.

A function $f : \mathfrak{F}(\mathbb{K}) \to \mathbb{Q}$ is called constructible if $f(\mathfrak{F}(\mathbb{K}))$ is finite and $f^{-1}(c)$ is a constructible set in $\mathfrak{F}(\mathbb{K})$ for each $c \in f(\mathfrak{F}(\mathbb{K})) \setminus \{0\}$. A function $f : \mathfrak{F}(\mathbb{K}) \to \mathbb{Q}$ is called locally constructible if $f \cdot \delta_C$ is constructible for all constructible $C \subseteq \mathfrak{F}(\mathbb{K})$, where $\delta_C$ is the characteristic function of $C$. Write $\text{CF}(\mathfrak{F})$ and $\text{LCF}(\mathfrak{F})$ for the $\mathbb{Q}$-vector spaces of $\mathbb{Q}$-valued constructible and locally constructible functions on $\mathfrak{F}$.

### 1.2. Stack Functions


## 2. Ringle-Hall Algebra and Its Applications


## 3. Generalized Donaldson-Thomas Invariants


## 4. BPS Invariants and Integrality



![placeholder](/MyBlogs/my_pics/2023-01-19-1.png){: .align-center}

$\blacksquare$


<html>
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width">
  <script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
  <script id="MathJax-script" async
          src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js">
  </script>
</head>
<body>
<p>
\begin{align*}
&\mathrm{length}_{\mathscr{O}}(\mathscr{O}/(a_1g_2-a_2g_1,fa_1,fa_2))\\
&=\mathrm{length}_{\mathscr{O}}(\mathscr{O}/(a_1,a_2))+\mathrm{length}_{\mathscr{O}}(\mathscr{O}/(f,a_1g_2-a_2g_1)).
\end{align*}
</p>
</body>
</html>



[^1]: [JS11] Dominic Joyce and Yinan Song. A theory of generalized Donaldson-Thomas invariants. Amer. Math. Soc. 2011. See also [arXiv:0810.5645](https://arxiv.org/abs/0810.5645).

[^2]: [BBJ19] Brav, C., Bussi, V., Joyce, D.: A Darboux theorem for derived schemes with shifted symplectic structure. J. Amer. Math. Soc. 32, 399–443 (2019)


