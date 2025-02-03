---
title: "Basic Theory of the Generalized Donaldson-Thomas Invariants of Joyce-Song"
collection: Blogs
permalink: /Blogs/2025-01-19-Basic-Theory-of-Generalized-Donaldson-Thomas-Invariants-of-Joyce-Song
excerpt_separator: <!--more-->
date: 2025-01-19
---
This is a basic and quick introduction of the theory of generalized Donaldson-Thomas invariants of strict Calabi-Yau $3$-folds due to Joyce-Song
in [JS11][^1]. We work over $\mathbb C$ to defined consider the generalized DT-invariants. But most of the theory before that we will work over any algebraically closed field $\mathbb K$ of characteristic zero.

<!--more-->

## 0. Review of Donaldson-Thomas Invariants of Calabi-Yau $3$-folds

> **Definition 0.1.** A **Calabi-Yau manifold** is a smooth projective variety $X$ over $\mathbb K$ such that $K\_X\cong\mathscr O\_X$.
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

> **Theorem 0.5.** (Behrend) Let $M$ be a proper $\mathbb K$-scheme with a symmetric perfect obstruction theory, then 
> \\[\int\_{[M]^{\text{vir}}}1=\chi(X,\nu\_X):=\sum\_{k\in\mathbb Z}k\chi(\nu\_X^{-1}(k)).\\]

> **Remark 0.6.** Here although we do not prove this theorem, we can give some idea of the reason why this result is true. Here we let $\mathbb K=\mathbb C$.
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

A function $f : \mathfrak{F}(\mathbb{K}) \to \mathbb{Q}$ is called **constructible** if $f(\mathfrak{F}(\mathbb{K}))$ is finite and $f^{-1}(c)$ is a constructible set in $\mathfrak{F}(\mathbb{K})$ for each $c \in f(\mathfrak{F}(\mathbb{K})) \setminus \{0\}$. A function $f : \mathfrak{F}(\mathbb{K}) \to \mathbb{Q}$ is called **locally constructible** if $f \cdot \delta_C$ is constructible for all constructible $C \subseteq \mathfrak{F}(\mathbb{K})$, where $\delta_C$ is the characteristic function of $C$. Write $\text{CF}(\mathfrak{F})$ and $\text{LCF}(\mathfrak{F})$ for the $\mathbb{Q}$-vector spaces of $\mathbb{Q}$-valued constructible and locally constructible functions on $\mathfrak{F}$.、

> **Definition 1.2.** Let $\mathbb{K}$ have characteristic zero, and $\mathfrak{F}$ be an Artin $\mathbb{K}$-stack with affine geometric stabilizers and $C \subseteq \mathfrak{F}(\mathbb{K})$ be constructible. Then we define the **naïve Euler characteristic** $\chi^{\text{na}}(C)$ of $C$ to be some $\chi(Y)$ for some algebraic scheme $Y$ on $\mathbb K$ with $C\cong Y(\mathbb K)$ by some Weil cohomology theory (we will omit this). It is called **naïve** as it takes no account of stabilizer groups. For $f \in \text{CF}(\mathfrak{F})$, define $\chi^{\text{na}}(\mathfrak{F}, f)$ in $\mathbb{Q}$ by
\\[\chi^{\text{na}}(\mathfrak{F}, f) = \sum_{c \in f (\mathfrak{F}(\mathbb{K})) \setminus \{0\}} c \chi^{\text{na}} (f^{-1}(c)).\\]
>
> Let $\mathfrak{F}, \mathfrak{G}$ be Artin $\mathbb{K}$-stacks with affine geometric stabilizers, and $\phi : \mathfrak{F} \to \mathfrak{G}$ a 1-morphism. For $f \in \text{CF}(\mathfrak{F})$, define $\text{CF}^na(\phi)f : \mathfrak{G}(\mathbb{K}) \to \mathbb{Q}$ by
\\[
\text{CF}^{\text{na}}(\phi)f(y) = \chi^{\text{na}}(\mathfrak{F}, f \cdot \delta\_{\phi^{-1}(y)}) \quad \text{for } y \in \mathfrak{G}(\mathbb{K}),
\\]
where $\delta\_{\phi^{-1}(y)}$ is the characteristic function of $\phi^{-1}(\{y\}) \subseteq \mathfrak{G}(\mathbb{K})$ on $\mathfrak{G}(\mathbb{K})$. Then $\text{CF}^{\text{na}}(\phi) : \text{CF}(\mathfrak{F}) \to \text{CF}(\mathfrak{G})$ is a $\mathbb{Q}$-linear map called the **naïve pushforward**.
>
> Now suppose $\phi$ is representable. Then for any $x \in \mathfrak{F}(\mathbb{K})$ we have an injective morphism $\phi\_\* : \text{Iso}\_{\mathfrak{F}}(x) \to \text{Iso}\_{\mathfrak{G}}(\phi\_\*(x))$ of affine algebraic $\mathbb{K}$-groups. The image $\phi\_\*(\text{Iso}\_{\mathfrak{F}}(x))$ is an affine algebraic $\mathbb{K}$-group closed in $\text{Iso}\_{\mathfrak{G}}(\phi\_\*(x))$, so the quotient $\text{Iso}\_{\mathfrak{G}}(\phi\_\*(x))/(\phi\_\*(\text{Iso}\_{\mathfrak{F}}(x)))$ exists as a quasiprojective $\mathbb{K}$-variety. Define a function $m\_\phi : \mathfrak{F}(\mathbb{K}) \to \mathbb{Z}$ by $m\_\phi(x) = \chi(\text{Iso}\_{\mathfrak{G}}(\phi\_\*(x))/(\phi\_\*(\text{Iso}\_{\mathfrak{F}}(x))) )$ for $x \in \mathfrak{F}(\mathbb{K})$. For $f \in \text{CF}(\mathfrak{F})$, define $\text{CF}^{stk}(\phi)f : \mathfrak{G}(\mathbb{K}) \to \mathbb{Q}$ by
\\[
\text{CF}^{stk}(\phi)f(y) = \chi^{\text{na}}(\mathfrak{F}, m\_\phi \cdot f \cdot \delta\_{\phi^{-1}(y)}) \quad \text{for } y \in \mathfrak{G}(\mathbb{K}).
\\]
>
> An alternative definition is
\\[
\text{CF}^{stk}(\phi)f(y) = \chi(\mathfrak{F} \times\_{\phi, \mathfrak{G}, y}\text{Spec}\, \mathbb{K}, \pi\_{\mathfrak{F}}^{\*}(f)) \quad \text{for } y \in \mathfrak{G}(\mathbb{K}),
\\]
where $\mathfrak{F} \times\_{\phi, \mathfrak{G}, y}\text{Spec}\, \mathbb{K}$ is a $\mathbb{K}$-scheme (or algebraic space) as $\phi$ is representable, and $\chi(\cdots)$ is the Euler characteristic of this $\mathbb{K}$-scheme weighted by $\pi\_{\mathfrak{F}}^{\*}(f)$. These two definitions are equivalent as the projection $\pi\_1 : \mathfrak{F} \times\_{\phi, \mathfrak{G}, y}\text{Spec}\, \mathbb{K} \to \mathfrak{F}$ induces a map on $\mathbb{K}$-points $(\pi\_1)\_\* : (\mathfrak{F} \times\_{\phi, \mathfrak{G}, y}\text{Spec}\, \mathbb{K})(\mathbb{K}) \to \phi\_{\*}^{-1}(y) \subset \mathfrak{F}(\mathbb{K})$, and the fibre of $(\pi\_1)\_\*$ over $x \in \phi\_{\*}^{-1}(y)$ is $(\text{Iso}\_{\mathfrak{G}}(\phi\_\*(x))/(\phi\_\*(\text{Iso}\_{\mathfrak{F}}(x))))(\mathbb{K})$, with Euler characteristic $m\_\phi(x)$. Then $\text{CF}^{stk}(\phi) : \text{CF}(\mathfrak{F}) \to \text{CF}(\mathfrak{G})$ is a $\mathbb{Q}$-linear map called the **stack pushforward**. If $\mathfrak{F}, \mathfrak{G}$ are $\mathbb{K}$-schemes then $\text{CF}^na(\phi), \text{CF}^{stk}(\phi)$ coincide, and we write them both as $\text{CF}(\phi) : \text{CF}(\mathfrak{F}) \to \text{CF}(\mathfrak{G})$.
>
> Let $\theta : \mathfrak{F} \to \mathfrak{G}$ be a finite type 1-morphism. If $C \subseteq \mathfrak{G}(\mathbb{K})$ is constructible then so is $\theta\_{、*}^{-1}(C) \subseteq \mathfrak{F}(\mathbb{K})$. It follows that if $f \in \text{CF}(\mathfrak{G})$ then $f \circ \theta\_\*$ lies in $\text{CF}(\mathfrak{F})$. Define the **pullback** $\theta^{\*} : \text{CF}(\mathfrak{G}) \to \text{CF}(\mathfrak{F})$ by $\theta^{\*}(f) = f \circ \theta\_\*$. It is a linear map.

There are several functorial and commutative properties of these pullback pushforward we will omit these. We refer Theorem 2.4 in [JS11][^1].

### 1.2. Stack Functions

> **Definition 1.3.** Let $\mathbb{K}$ be an algebraically closed field, and $\mathfrak{F}$ be an Artin $\mathbb{K}$-stack with affine geometric stabilizers. Consider pairs $(\mathfrak{R}, \rho)$, where $\mathfrak{R}$ is a finite type Artin $\mathbb{K}$-stack with affine geometric stabilizers and $\rho : \mathfrak{R} \to \mathfrak{F}$ is a 1-morphism. We call two pairs $(\mathfrak{R}, \rho)$, $(\mathfrak{R}' , \rho')$ **equivalent** if there exists a 1-isomorphism $\iota : \mathfrak{R} \to \mathfrak{R}'$ such that $\rho' \circ \iota$ and $\rho$ are 2-isomorphic 1-morphisms $\mathfrak{R} \to \mathfrak{F}$. Write $[(\mathfrak{R}, \rho)]$ for the equivalence class of $(\mathfrak{R}, \rho)$. If $(\mathfrak{R}, \rho)$ is such a pair and $\mathfrak{S}$ is a closed $\mathbb{K}$-substack of $\mathfrak{R}$ then $(\mathfrak{S}, \rho\|\_{\mathfrak{S}})$, $(\mathfrak{R}\setminus \mathfrak{S}, \rho\|\_{\mathfrak{R}\setminus \mathfrak{S}})$ are pairs of the same kind.
>
> Define $\underline{\mathrm{SF}}(\mathfrak{F})$ to be the $\mathbb{Q}$-vector space generated by equivalence classes $[(\mathfrak{R}, \rho)]$ as above, with for each closed $\mathbb{K}$-substack $\mathfrak{S}$ of $\mathfrak{R}$ a relation
>
> \\[
[(\mathfrak{R}, \rho)] = [(\mathfrak{S}, \rho\|\_{\mathfrak{S}})] + [(\mathfrak{R}\setminus \mathfrak{S}, \rho\|\_{\mathfrak{R}\setminus \mathfrak{S}})].
\\]
>
> Define $\mathrm{SF}(\mathfrak{F})$ to be the $\mathbb{Q}$-vector space generated by $[(\mathfrak{R}, \rho)]$ with $\rho$ representable, with the same relations above. Then $\mathrm{SF}(\mathfrak{F}) \subseteq \underline{\mathrm{SF}}(\mathfrak{F})$.

> **Small Remark:** Elements of $\mathrm{SF}(\mathfrak{F})$ will be called **stack functions**. We write stack functions either as letters $f, g, \ldots$, or explicitly as sums $\sum\_{i=1}^m c\_i[(\mathfrak{R}\_i, \rho\_i)]$. If $[(\mathfrak{R}, \rho)]$ is a generator of $\mathrm{SF}(\mathfrak{F})$ and $\mathfrak{R}^{\mathrm{red}}$ is the reduced substack of $\mathfrak{R}$ then $\mathfrak{R}^{\mathrm{red}}$ is a closed substack of $\mathfrak{R}$ and the complement $\mathfrak{R} \setminus \mathfrak{R}^{\mathrm{red}}$ is empty. Hence 
>
> \\[
[(\mathfrak{R}, \rho)] = [(\mathfrak{R}^{\mathrm{red}}, \rho|\_{\mathfrak{R}^{\mathrm{red}}})].
\\]
>
> Thus, the relations (2.5) destroy all information on nilpotence in the stack structure of $\mathfrak{R}$. 

We now can relate $\mathrm{CF}(\mathfrak{F})$ and $\mathrm{SF}(\mathfrak{F})$:

> **Definition 1.4.**  Let $\mathfrak{F}$ be an Artin $\mathbb{K}$-stack with affine geometric stabilizers, and $C \subseteq \mathfrak{F}(\mathbb{K})$ be constructible. Then $C = \prod\_{i=1}^n \mathfrak{R}\_i(\mathbb{K})$, for $\mathfrak{R}\_1, \ldots, \mathfrak{R}\_n$ finite type $\mathbb{K}$-substacks of $\mathfrak{F}$. Let $\rho\_i : \mathfrak{R}\_i \to \mathfrak{F}$ be the inclusion 1-morphism. Then $[(\mathfrak{R}\_i, \rho\_i)] \in \mathrm{SF}(\mathfrak{F})$. Define $\delta\_C = \sum\_{i=1}^n [(\mathfrak{R}\_i, \rho\_i)] \in \mathrm{SF}(\mathfrak{F})$. We think of this stack function as the analogue of the characteristic function $\delta\_C \in \mathrm{CF}(\mathfrak{F})$ of $C$. When $\mathbb{K}$ has characteristic zero, define a $\mathbb{Q}$-linear map $\iota\_{\mathfrak{F}} : \mathrm{CF}(\mathfrak{F}) \to \mathrm{SF}(\mathfrak{F})$ by $\iota\_{\mathfrak{F}}(f) = \sum\_{0 \neq c \in f (\mathfrak{F}(\mathbb{K}))} c \cdot \delta\_{f^{-1}(c)}$. Define $\mathbb{Q}$-linear $\pi\_{\mathfrak{F}}^{\mathrm{stk}} : \mathrm{SF}(\mathfrak{F}) \to \mathrm{CF}(\mathfrak{F})$ by
>
> \\[
\pi\_{\mathfrak{F}}^{\mathrm{stk}} (\sum\_{i=1}^n c\_i [(\mathfrak{R}\_i, \rho\_i)]) = \sum\_{i=1}^n c\_i \mathrm{CF}\_{\rho\_i}^{\mathrm{stk}} (\rho\_i) \mathbf{1}\_{\mathfrak{R}\_i},
\\]
>
> where $\mathbf{1}\_{\mathfrak{R}\_i}$ is the function in $\mathrm{CF}(\mathfrak{R}\_i)$. Then we can show that $\pi\_{\mathfrak{F}}^{\mathrm{stk}} \circ \iota\_{\mathfrak{F}}$ is the identity on $\mathrm{CF}(\mathfrak{F})$. Thus, $\iota\_{\mathfrak{F}}$ is injective and $\pi\_{\mathfrak{F}}^{\mathrm{stk}}$ is surjective. In general $\iota\_{\mathfrak{F}}$ is far from surjective, and $\underline{\mathrm{SF}}, \mathrm{SF}(\mathfrak{F})$ are much larger than $\mathrm{CF}(\mathfrak{F})$.

Some operators:

> **Definition 1.5**. Define **multiplication** ‘.’ on $\underline{\mathrm{SF}}(\mathfrak{F})$ by
>
> \\[
[(\mathfrak{R}, \rho)] \cdot [(\mathfrak{S}, \sigma)] = [(\mathfrak{R} \times\_{\rho, \mathfrak{F}, \sigma} \mathfrak{S}, \rho \circ \pi\_{\mathfrak{R}})].
\\]
>
> This extends to a $\mathbb{Q}$-bilinear product $\underline{\mathrm{SF}}(\mathfrak{F}) \times \underline{\mathrm{SF}}(\mathfrak{F}) \to\underline{\mathrm{SF}}(\mathfrak{F})$ which is commutative and associative, and $\mathrm{SF}(\mathfrak{F})$ is closed under ‘.’. Let $\phi : \mathfrak{F} \to \mathfrak{G}$ be a $1$-morphism of Artin $\mathbb{K}$-stacks with affine geometric stabilizers. Define the **pushforward** $\phi^{\*} : \underline{\mathrm{SF}}(\mathfrak{F}) \to \underline{\mathrm{SF}}(\mathfrak{G})$ by
>
> \\[
\phi^{\*} : \sum\_{i=1}^m c\_i[(\mathfrak{R}\_i, \rho\_i)] \mapsto \sum\_{i=1}^m c\_i[(\mathfrak{R}\_i, \phi \circ \rho\_i)].
\\]
>
> If $\phi$ is representable then $\phi^{\*}$ maps $\mathrm{SF}(\mathfrak{F}) \to \mathrm{SF}(\mathfrak{G})$. For $\phi$ of finite type, define **pullbacks** $\phi^{\*} :\underline{\mathrm{SF}}(\mathfrak{G}) \to\underline{\mathrm{SF}}(\mathfrak{F})$, $\phi^{\*} : \mathrm{SF}(\mathfrak{G}) \to \mathrm{SF}(\mathfrak{F})$ by
>
> \\[
\phi^{\*} : \sum\_{i=1}^m c\_i[(\mathfrak{R}\_i, \rho\_i)] \mapsto \sum\_{i=1}^m c\_i[(\mathfrak{R}\_i \times\_{\rho\_i, \mathfrak{G}, \phi} \mathfrak{F}, \pi\_{\mathfrak{F}})].
\\]
>
> The **tensor product** $\otimes :\underline{\mathrm{SF}}(\mathfrak{F}) \times\underline{\mathrm{SF}}(\mathfrak{G}) \to\underline{\mathrm{SF}}(\mathfrak{F} \times \mathfrak{G})$ or $\mathrm{SF}(\mathfrak{F}) \times \mathrm{SF}(\mathfrak{G}) \to \mathrm{SF}(\mathfrak{F} \times \mathfrak{G})$ is
>
> \\[
(\sum\_{i=1}^m c\_i[(\mathfrak{R}\_i, \rho\_i)]) \otimes (\sum\_{j=1}^n d\_j[(\mathfrak{G}\_j, \sigma\_j)]) = \sum\_{i,j} c\_i d\_j[(\mathfrak{R}\_i \times \mathfrak{G}\_j, \rho\_i \times \sigma\_j)].
\\]

There are several functorial and commutative properties of these pullback pushforward we will omit these. We refer Theorem 2.8, 2.9 in [JS11][^1].


### 1.3. Projections of Virtual Ranks

As we have seen, aiming to define the generalized DT-invariants we need to find a **logarithm** of the moduli stack $\mathcal M^{\alpha\text{-ss}}(\tau)$, we can regard it as a **virtual** stack whose stabilizer groups have one-dimensional maximal torus. Here we will introduce a projection which will maps the stack functions to the stack functions with some fixed *virtual* rank of stabilizer groups.

In general, a projection $\Pi^{\mu}$ of stack functions is associated to a weight function:

> **Definition 1.6.** A **weight function** $\mu$ is a map
>
> \\[
\mu : \{ \mathbb{K} \text{-groups } \mathbb{G}\_m^{k} \times K, \, k \geq 0, \, K \text{ finite abelian}, \, \text{up to isomorphism} \} \longrightarrow \mathbb{Q}.
\\]

In our idea, if $\mathfrak{R}$ has abelian stabilizer groups, then $\Pi^\mu([(\mathfrak{R}, \rho)])$ simply weights each point $r$ of $\mathfrak{R}$ by $\mu(\text{Isos}\_\mathfrak{R}(r))$. But if $\mathfrak{R}$ has nonabelian stabilizer groups, then $\Pi^\mu([(\mathfrak{R}, \rho)])$ replaces each point $r$ with stabilizer group $G$ by a $\mathbb{Q}$-linear combination of points with stabilizer groups $C\_G(\{t\})$ for $t \in T^G$, where $T^G$ is the maximal torus and the $\mathbb{Q}$-coefficients depend on the values of $\mu$ on subgroups of $T^G$:

> **Definition 1.7.** For any Artin $\mathbb{K}$-stack $\mathfrak{F}$ with affine geometric stabilizers, we will define linear maps $\Pi^\mu : \mathrm{SF}(\mathfrak{F}) \to \mathrm{SF}(\mathfrak{F})$ and $\Pi^\mu : \mathrm{SF}(\mathfrak{F}) \to \mathrm{SF}(\mathfrak{F})$. Now $\mathrm{SF}(\mathfrak{F})$ is generated by $[(\mathfrak{R}, \rho)]$ with $\mathfrak{R}$ 1-isomorphic to a quotient $[X/G]$, for $X$ a quasiprojective $\mathbb{K}$-variety and $G$ a special algebraic $\mathbb{K}$-group, with maximal torus $T^G$.
>
> Let $\mathcal{S}(T^G)$ be the set of subsets of $T^G$ defined by Boolean operations upon closed $\mathbb{K}$-subgroups $L$ of $T^G$. Given a weight function $\mu$ as above, define a measure $d\mu : \mathcal{S}(T^G) \to \mathbb{Q}$ to be additive upon disjoint unions of sets in $\mathcal{S}(T^G)$, and to satisfy $d\mu(L) = \mu(L)$ for all algebraic $\mathbb{K}$-subgroups $L$ of $T^G$. Define
>
>\\[
\Pi^\mu ([(\mathfrak{R}, \rho)]) =
\int\_{t \in T^G}\frac{\|\{w \in W(G, T^G) : w \cdot t = t\}\|}{\|W(G,T^G)\|}\left[ ([X^{(t)} / C\_G((t))], \rho \circ l^{(t)}) \right]d\mu.
\\]
>
> Here $X^{(t)}$ is the subvariety of $X$ fixed by $t$, and $l^{(t)} : [X^{(t)} / C\_G((t))] \to [X/G]$ is the obvious 1-morphism of Artin stacks.
>
> We can show that $\Pi^\mu ([(\mathfrak{R}, \rho)])$ is indeoendent of $X,G,T^G$ and $\mathfrak R\cong[X/G]$.

Now $\Pi^{\mu}$ commute with pushforward and $\Pi^{\mu}\Pi^{\gamma}=\Pi^{\mu\gamma}$.

For our special case, we define $\Pi^{\text{vir}}_n:=\Pi^{\mu\_n}$ where $\mu\_n([H])=1$ if rank of $H$ is $1$ and $0$ otherwise.

### 1.4. Stack Function Spaces Twisted by Euler Characteristics

Let $\mathcal{Q}(G,T^{G})$ is a set of closed subgroups $Q$ of $T^G$ such that $Q=T^G\cap C(C_G(Q))$. We call $G$ is **very special** if 
$Q,C_G(Q)$ are special for $Q\in\mathcal{Q}(G,T^{G})$. One can show that $\text{CL}_k(\mathbb K)$ is very special.

> **Definition 1.8.** Let $\mathfrak{F}$ be an Artin $\mathbb{K}$-stack with affine geometric stabilizers. Consider pairs $(\mathfrak{R},\rho)$, where $\mathfrak{R}$ is a finite type Artin $\mathbb{K}$-stack with affine geometric stabilizers and $\rho:\mathfrak{R}\rightarrow\mathfrak{F}$ is a 1-morphism, with equivalence of pairs as in Definition 2.5. Define $\underline{\widehat{\mathrm{SF}}}(\mathfrak{F},\chi,\mathbb{Q})$ to be the $\mathbb{Q}$-vector space generated by equivalence classes $[(\mathfrak{R},\rho)]$ as above, with the following relations:
>
> - (i) Given $[(\mathfrak{R},\rho)]$ as above and $\mathfrak{S}$ a closed $\mathbb{K}$-substack of $\mathfrak{R}$ we have $[(\mathfrak{R},\rho)]=[(\mathfrak{S},\rho\|\_{\mathfrak{S}})]+[(\mathfrak{R} \setminus\mathfrak{S},\rho\|\_{\mathfrak{R}\setminus\mathfrak{S}})]$, as in (2.5).
>
> - (ii) Let $\mathfrak{R}$ be a finite type Artin $\mathbb{K}$-stack with affine geometric stabilizers, $U$ a quasiprojective $\mathbb{K}$-variety, $\pi\_{\mathfrak{R}}:\mathfrak{R}\times U\rightarrow\mathfrak{R}$ the natural projection, and $\rho:\mathfrak{R}\rightarrow\mathfrak{F}$ a 1-morphism. Then $[(\mathfrak{R}\times U,\rho\circ\pi\_{\mathfrak{R}})]=\chi([U])[(\mathfrak{R},\rho)]$. Here $\chi(U)\in\mathbb{Z}$ is the Euler characteristic of $U$. It is a _motivic invariant_ of $\mathbb{K}$-schemes, that is, $\chi(U)=\chi(V)+\chi(U\setminus V)$ for $V\subset U$ closed.
>
> - (iii) Given $[(\mathfrak{R},\rho)]$ as above and a 1-isomorphism $\mathfrak{R}\cong[X/G]$ for $X$ a quasiprojective $\mathbb{K}$-variety and $G$ a very special algebraic $\mathbb{K}$-group acting on $X$ with maximal torus $T^{G}$, we have
>  \\[[(\mathfrak{R},\rho)]=\sum\_{Q\in\mathcal{Q}(G,T^{G})}F(G,T^{G},Q)\bigl{[}([X/Q], \rho\circ t^{\mathbb{Q}})\bigr{]},\\]
> where $t^{\mathbb{Q}}:[X/Q]\rightarrow\mathfrak{R}\cong[X/G]$ is the natural projection 1-morphism.
>
Here $F(G,T^{G},Q)\in\mathbb{Q}$ are a system of rational coefficients with a complicated definition  which we will not repeat.
>
Similarly, define $\widehat{\mathrm{SF}}(\mathfrak{F},\chi,\mathbb{Q})$ to be the $\mathbb{Q}$-vector space generated by $[(\mathfrak{R},\rho)]$ with $\rho$ representable, and relations (i)-(iii) as above. Then $\widehat{\mathrm{SF}}(\mathfrak{F},\chi,\mathbb{Q})\subset\underline{\widehat{\mathrm{SF}}}( \mathfrak{F},\chi,\mathbb{Q})$. Define projections $\Pi\_{\mathfrak{F}}^{\chi,\mathbb{Q}}:\underline{\widehat{\mathrm{SF}}}(\mathfrak{F}) \to\underline{\widehat{\mathrm{SF}}}(\mathfrak{F},\chi,\mathbb{Q})$ and $\widehat{\mathrm{SF}}(\mathfrak{F})\rightarrow\widehat{\mathrm{SF}}(\mathfrak{F}, \chi,\mathbb{Q})$ by $\Pi\_{\mathfrak{F}}^{\chi,\mathbb{Q}}:\sum\_{i\in I}c\_{i}[(\mathfrak{R}\_{i},\rho\_{i })]\mapsto\sum\_{i\in I}c\_{i}[(\mathfrak{R}\_{i},\rho\_{i})]$.
>
> Define _multiplication '._', _pushforwards_ $\phi\_{\*}$, _pullbacks_ $\phi^{\*}$, and _tensor products_ $\otimes$ on the spaces $\widehat{\mathrm{SF}},\underline{\widehat{\mathrm{SF}}}(\*,\chi,\mathbb{Q})$ as in Definition 2.7, and _projections_ $\Pi\_{n}^{vi}$.

An important structure result:

> **Proposition 1.9.**  $\widehat{\mathrm{SF}},\underline{\widehat{\mathrm{SF}}}(\mathfrak{F},\chi, \mathbb{Q})$ are spanned over $\mathbb{Q}$ by elements $[(U \times [\operatorname{Spec} \mathbb{K}/T], \rho)]$, for $U$ a quasiprojective $\mathbb{K}$-variety and $T$ an algebraic $\mathbb{K}$-group isomorphic to $\mathbb{G}\_m^k \times K$ for $k \geq 0$ and $K$ finite abelian.
>
> Suppose $\sum\_{i \in I} c\_i [(U\_i \times [\operatorname{Spec} \mathbb{K}/T\_i], \rho\_i)] = 0$ in $\underline{\widehat{\mathrm{SF}}}(\mathfrak{F}, \chi, \mathbb{Q})$ or $\widehat{\mathrm{SF}}(\mathfrak{F}, \chi, \mathbb{Q})$, where $I$ is finite set, $c\_i \in \mathbb{Q}$, $U\_i$ is a quasiprojective $\mathbb{K}$-variety, and $T\_i$ is an algebraic $\mathbb{K}$-group isomorphic to $\mathbb{G}\_m^{k\_i} \times K\_i$ for $k\_i \geq 0$ and $K\_i$ finite abelian, with $T\_i \neq T\_j$ for $i \neq j$. Then $c\_j [(U\_j \times [\operatorname{Spec} \mathbb{K}/T\_j], \rho\_j)] = 0$ for all $j \in I$.

Note that in this representation, the operators $\Pi\_n^{\mathrm{vi}}$ are easy to define: we have
$\Pi\_n^{\mathrm{vi}} ([(U \times [\operatorname{Spec} \mathbb{K}/T], \rho)]) = [(U \times [\operatorname{Spec} \mathbb{K}/T], \rho)]$
if $\text{dim } T = n$ and $\Pi\_n^{\mathrm{vi}} ([(U \times [\operatorname{Spec} \mathbb{K}/T], \rho)]) =0$ otherwise.

This proposition says that a general element $[(\mathfrak{R}, \rho)]$ of $\widehat{\mathrm{SF}},\underline{\widehat{\mathrm{SF}}}(\mathfrak{F}, \chi, \mathbb{Q})$, whose stabilizer groups $\mathrm{Iso}\_{\mathfrak{R}}(x)$ for $x \in \mathfrak{R}(\mathbb{K})$ are arbitrary affine algebraic $\mathbb{K}$-groups, may be written as a $\mathbb{Q}$-linear combination of elements $[(U \times [\operatorname{Spec} \mathbb{K}/T], \rho)]$ whose stabilizer groups $T$ are of the form $\mathbb{G}\_m^k \times K$ for $k \geq 0$ and $K$ finite abelian. That is, by working in $\widehat{\mathrm{SF}},\underline{\widehat{\mathrm{SF}}}(\mathfrak{F}, \chi, \mathbb{Q})$, we can treat all stabilizer groups as if they are abelian. Furthermore, although $\widehat{\mathrm{SF}},\underline{\widehat{\mathrm{SF}}}(\mathfrak{F}, \chi, \mathbb{Q})$ forget information about nonabelian stabilizer groups, they do remember the difference between abelian stabilizer groups of the form $\mathbb{G}\_m^k \times K$ for finite $K$.

## 2. Ringle-Hall Algebra and Its Applications

Here we will focus on and assume our abelian category $\mathcal A$ and $K(\mathcal A)$ which is a quotient of G-group $K_0(\mathcal A)$ with some expected properties (see Assumption 3.2 in [JS11][^1]).
Note that these properties holds for $\mathrm{Coh}(X)$ of smooth projective variety $X$ with $K(\mathrm{Coh}(X))=K^{\text{num}}(\mathrm{Coh}(X))$;
the caetgory of reps of quiver with relations.

We will use the following notation:

- Define the ‘positive cone’ $C(\mathcal A)$ in $K(\mathcal A)$ to be
\\[
C(\mathcal A) = \{[E] \in K(\mathcal A) : 0 \not\equiv E \in\mathcal A\} \subset K(\mathcal A).
\\]

- Write $\mathfrak{M}\_{\mathcal A}$ for the moduli stack of objects in $\mathcal A$. It is an Artin $\mathbb{K}$-stack, locally of finite type. Elements of $\mathfrak{M}\_{\mathcal A}(\mathbb{K})$ correspond to isomorphism classes $[E]$ of objects $E$ in $\mathcal A$, and the stabilizer group $\text{Iso}\_{\mathfrak{M}\_{\mathcal A}}([E])$ in $\mathfrak{M}\_{\mathcal A}$ is isomorphic as an algebraic $\mathbb{K}$-group to the automorphism group $\text{Aut}(E)$.

- For $\alpha \in C(A)$, write $\mathfrak{M}\_{\mathcal A}^\alpha$ for the substack of objects $E \in {\mathcal A}$ in class $\alpha$ in $K(\mathcal A)$. It is an open and closed $\mathbb{K}$-substack of $\mathfrak{M}\_{\mathcal A}$.

- Write $\mathfrak{Exact}\_{\mathcal A}$ for the moduli stack of short exact sequences $0 \to E\_1 \to E\_2 \to E\_3 \to 0$ in $A$. It is an Artin $\mathbb{K}$-stack, locally of finite type.

- For $j = 1, 2, 3$ write $\pi\_j : \mathfrak{Exact}\_{\mathcal A} \to \mathfrak{M}\_{\mathcal A}$ for the 1-morphism of Artin stacks projecting $0 \to E\_1 \to E\_2 \to E\_3 \to 0$ to $E\_j$. Then $\pi\_2$ is _representable_, and $\pi\_1 \times \pi\_3 : \mathfrak{Exact}\_{\mathcal A} \to \mathfrak{M}\_{\mathcal A} \times \mathfrak{M}\_{\mathcal A}$ is of _finite type_.


> **Definition 2.1.** Define bilinear operations $\*$ on the stack function spaces $\underline{\text{SF}}, \text{SF}(\mathfrak{M}\_{\mathcal A})$ and $\underline{\widehat{\text{SF}}}, \widehat{\text{SF}}(\mathfrak{M}\_{\mathcal A}, \chi, \mathbb{Q})$ by
>
>\\[
f * g = (\pi\_2)\_\*((\pi\_1 \times \pi\_3)^\*(f \otimes g)),
\\]
>
> using pushforwards, pullbacks and tensor products we defined. They are well-defined as $\pi\_2$ is representable, and $\pi\_1 \times \pi\_3$ is of finite type. We can sbhow that this $\*$ is associative, and makes $\underline{\text{SF}}, \text{SF}(\mathfrak{M}\_{\mathcal A})$ and $\underline{\widehat{\text{SF}}}, \widehat{\text{SF}}(\mathfrak{M}\_{\mathcal A}, \chi, \mathbb{Q})$ into noncommutative $\mathbb{Q}$-algebras, with identity $\bar{\delta}\_{[0]}$, where $[0] \in \mathfrak{M}\_{\mathcal A}$ is the zero object. We call them **Ringel-Hall algebras**. The natural inclusions and projections $\Pi\_{\mathfrak{M}\_{\mathcal A}}^{\chi,\mathbb{Q}}$ between these spaces are algebra morphisms.

> **Definition 2.2.** Suppose $[(\mathfrak{R}, \rho)]$ is a generator of $\text{SF}(\mathfrak{M}\_{\mathcal A})$. Let $r \in \mathfrak{R}(\mathbb{K})$ with $\rho\_\*(r) = [E] \in \mathfrak{M}\_{\mathcal A}(\mathbb{K})$\. Then $\rho$ induces an injective morphism of stabilizer $\mathbb{K}$-groups $\rho\_\* : \text{Iso}\_{\mathfrak{R}}(r) \rightarrow \text{Iso}\_{\mathfrak{M}\_A}([E]) \cong \text{Aut}(E)$ as $\rho$ is representable this is injective. Hence induces an isomorphism of $\text{Iso}\_{\mathfrak{R}}(r)$ with a $\mathbb{K}$-subgroup of $\text{Aut}(E)$. Now $\text{Aut}(E) = \text{End}(E)^{\times}$ is the $\mathbb{K}$-group of invertible elements in a finite-dimensional $\mathbb{K}$-algebra $\text{End}(E) = \text{Hom}(E, E)$. We say that $[(\mathfrak{R}, \rho)]$ has **algebra stabilizers** if whenever $r \in \mathfrak{R}(\mathbb{K})$ with $\rho\_\*(r) = [E]$, the $\mathbb{K}$-subgroup $\rho\_\*(\text{Iso}\_{\mathfrak{R}}(r))$ in $\text{Aut}(E)$ is the $\mathbb{K}$-group $A^{\times}$ of invertible elements in a $\mathbb{K}$-subalgebra $A$ in $\text{End}(E)$.
>
> Write $\text{SF}\_{\text{al}}(\mathfrak{M}\_{\mathcal A}), \widehat{\text{SF}}\_{\text{al}}(\mathfrak{M}\_{\mathcal A}, \chi, \mathbb{Q})$ for the subspaces spanned over $\mathbb{Q}$ by $[(\mathfrak{R}, \rho)]$ with algebra stabilizers. These are subalgebras of Ringel-Hall algebras and one can show that they are closed under $\Pi^{\text{vir}}_{n}$. We define $\text{SF}\_{\text{al}}^{\text{ind}}(\mathfrak{M}\_{\mathcal A}), \widehat{\text{SF}}\_{\text{al}}^{\text{ind}}(\mathfrak{M}\_{\mathcal A}, \chi, \mathbb{Q})$ to be the subspaces consist of $f$ with $\Pi\_1^i(f) = f$.
>
> We can show that $\text{SF}\_{\text{al}}^{\text{ind}}(\mathfrak{M}\_{\mathcal A}), \widehat{\text{SF}}\_{\text{al}}^{\text{ind}}(\mathfrak{M}\_{\mathcal A}, \chi, \mathbb{Q})$ are closed under the Lie bracket $[f, g] = f \* g - g \* f$. Thus, these are Lie subalgebras. The projection $\Pi\_{\mathfrak{M}\_{\mathcal A}}^{\chi,\mathbb Q}:\text{SF}\_{\text{al}}^{\text{ind}}(\mathfrak{M}\_{\mathcal A}) \to\widehat{\text{SF}}\_{\text{al}}^{\text{ind}}(\mathfrak{M}\_{\mathcal A}, \chi, \mathbb{Q})$ is a Lie algebra morphism.

So our $\text{SF}\_{\text{al}}^{\text{ind}}(\mathfrak{M}\_{\mathcal A}), \widehat{\text{SF}}\_{\text{al}}^{\text{ind}}(\mathfrak{M}\_{\mathcal A}, \chi, \mathbb{Q})$ are stack functions with **virtual rank $1$**! Using the local structure result before, we can show:

> **Proposition 2.3.** $\widehat{\text{SF}}\_{\text{al}}(\mathfrak{M}\_{\mathcal A}, \chi, \mathbb{Q})$ is spanned over $\mathbb{Q}$ by elements of the form $[(U \times [\text{Spec } \mathbb{K}/\mathbb{G}\_{m}^{k}], \rho)]$ with algebra stabilizers, for $U$ a quasiprojective $\mathbb{K}$-variety and $k \geq 0$. Also $\widehat{\text{SF}}\_{\text{al}}^{\text{ind}}(\mathfrak{M}\_{\mathcal A}, \chi, \mathbb{Q})$ is spanned over $\mathbb{Q}$ by $[(U \times [\text{Spec} \mathbb{K}/\mathbb{G}\_{m}^{k}], \rho)]$ with algebra stabilizers, for $U$ a quasiprojective $\mathbb{K}$-variety.

Finally we will taking the **logarithm** of the moduli stack of semistable objects and  we can regard it as a virtual stack whose stabilizer groups have one-dimensional maximal torus, that is, lies in $\text{SF}\_{\text{al}}^{\text{ind}}(\mathfrak{M}\_{\mathcal A})$. 

Now let $\mathbb K, A, K(A)$ be abelian categories with K-group, and $(\tau, T, \leq)$ be a permissible (that is, $A$ is $\tau$-Artinian and the moduli stack of $\alpha$-semistable objects is of finite type for $\alpha\in C(A)$) weak stability condition on $A$. Let $\mathfrak M^{\alpha\text{-ss}}\_{A}(\tau),\mathfrak M^{\alpha\text{-st}}\_{A}(\tau)$ be the moduli stack of semistable, stable objects.

> **Definition 2.4.** Define stack functions $\delta\_{\text{ss}}^{\alpha}(\tau) = \delta\_{\mathfrak{M}^{\alpha\text{-ss}}(\tau)}$ in $\text{SF}\_{\text{al}}(\mathfrak{M}\_A)$ for $\alpha \in C(A)$. We define elements $\bar{\epsilon}^{\alpha}(\tau)$ in $\text{SF}\_{\text{al}}(\mathfrak{M}\_A)$ by
>
> \\[
\bar{\epsilon}^{\alpha}(\tau) =
\sum\_{n \geq 1, \, \alpha\_1, \ldots, \alpha\_n \in C(A): \, \alpha\_1 + \cdots + \alpha\_n = \alpha, \, \tau(\alpha\_i) = \tau(\alpha), \, \text{all } i}
\frac{(-1)^{n-1}}{n} \delta\_{\text{ss}}^{\alpha\_1}(\tau) \* \delta\_{\text{ss}}^{\alpha\_2}(\tau) \* \cdots \* \delta\_{\text{ss}}^{\alpha\_n}(\tau),
\\]
>
> where $\*$ is the Ringel-Hall multiplication in $\text{SF}\_{\text{al}}(\mathfrak{M}\_A)$. Then we can prove that
>
> \\[
\delta\_{\text{ss}}^{\alpha}(\tau) =
\sum\_{n \geq 1, \, \alpha\_1, \ldots, \alpha\_n \in C(A): \, \alpha\_1 + \cdots + \alpha\_n = \alpha, \, \tau(\alpha\_i) = \tau(\alpha), \, \text{all } i}
\frac{1}{n!} \bar{\epsilon}^{\alpha\_1}(\tau) \* \bar{\epsilon}^{\alpha\_2}(\tau) \* \cdots \* \bar{\epsilon}^{\alpha\_n}(\tau).
\\]
>
> There are only finitely many nonzero terms above, because as the family of $\tau$-semistable sheaves in class $\alpha$ is bounded, there are only finitely ways to write $\alpha = \alpha\_1 + \cdots + \alpha\_n$ with $\tau$-semistable sheaves in class $\alpha\_i$ for all $i$.

> **Small Remark.** Here is a way to interpret these informally in terms of **log and exp**: working in a completed version, so that appropriate classes of infinite sums make sense, for fixed $t \in T$ we have
>
> \\[
\sum\_{\alpha \in C(A): \tau(\alpha) = t} \tilde{\epsilon}^\alpha(\tau) = \log \left[ \bar{\delta}\_0 + \sum\_{\alpha \in C(A): \tau(\alpha) = t} \bar{\delta}\_\text{ss}^\alpha(\tau) \right],
\\]
>
> and
> 
> \\[
\bar{\delta}\_0 + \sum\_{\alpha \in C(A): \tau(\alpha) = t} \bar{\delta}\_\text{ss}^\alpha(\tau) = \exp \left[ \sum\_{\alpha \in C(A): \tau(\alpha) = t} \tilde{\epsilon}^\alpha(\tau) \right],
\\]
>
> where $\bar{\delta}\_0$ is the identity 1 in $\widetilde{\text{SF}}\_{\text{al}}(\mathfrak{M}\_A)$. For $\alpha \in C(A)$ and $t = \tau(\alpha)$, using the power series $\log(1 + x) = \sum\_{n \geq 1} \frac{(-1)^{n-1}}{n} x^n$ and $\exp(x) = 1 + \sum\_{n \geq 1} \frac{1}{n!} x^n$ we see that (3.4)-(3.5) are the restrictions of (3.6)-(3.7) to $\mathfrak{M}\_A^\alpha$. This makes clear why (3.4) and (3.5) are inverse, since log and exp are inverse. Thus, knowing the $\tilde{\epsilon}^\alpha(\tau)$ is equivalent to knowing the $\bar{\delta}\_\text{ss}^\alpha(\tau)$.
>
> If $\mathfrak{M}\_\text{ss}^\alpha(\tau) = \mathfrak{M}\_\text{st}^\alpha(\tau)$ then $\tilde{\epsilon}^\alpha(\tau) = \bar{\delta}\_\text{ss}^\alpha(\tau)$. The difference between $\tilde{\epsilon}^\alpha(\tau)$ and $\bar{\delta}\_\text{ss}^\alpha(\tau)$ is that $\tilde{\epsilon}^\alpha(\tau)$ 'counts' strictly semistable sheaves in a special, complicated way.

Here is an **important and highly nontrivial property** of the $\tilde{\epsilon}^\alpha(\tau)$, which does not hold for $\delta\_{\text{ss}}^{\alpha}(\tau)$,
that tell us that taking the **logarithm** of the moduli stack of semistable objects and  we can regard it as a virtual stack whose stabilizer groups have one-dimensional maximal torus:

> **Theorem 2.5.** We have $\bar{\epsilon}^{\alpha}(\tau)\in\text{SF}\_{\text{al}}^{\text{ind}}(\mathfrak{M}\_A)\subset\text{SF}\_{\text{al}}(\mathfrak{M}\_A)$.

Using these, we can define the generalized Donaldson-Thomas invariants.

## 3. Generalized Donaldson-Thomas Invariants

Let $X$ be a **strict** projective Calabi-Yau $3$-fold over $\mathbb C$. Let $\mathfrak M:=\underline{Coh}(X)$ be the moduli stack of coherent sheaves
and $\mathcal M^{\alpha\text{-ss}}(\tau)$ be the stack of semistable objects for some $\alpha\in K^{\text{num}}(\text{coh}(X))$ with a projective good moduli space $ M^{\alpha\text{-ss}}(\tau)$. They contain open locus of stable objects $\mathcal M^{\alpha\text{-st}}(\tau)\subset\mathcal M^{\alpha\text{-ss}}(\tau)$ and $M^{\alpha\text{-st}}(\tau)\subset M^{\alpha\text{-ss}}(\tau)$ which need not be proper.

### 3.1. Generalized DT-Invariants

We will define a **global Behrend function of $\mathfrak M$** first:

> **Theorem 3.1.** Let $X$ be a Calabi-Yau 3-fold over $\mathbb{C}$, and $\mathfrak{M}$ the moduli stack of coherent sheaves on $X$. The **Behrend function** $\nu\_{\mathfrak{M}} : \mathfrak{M}(\mathbb{C}) \to \mathbb{Z}$ is a natural locally constructible function on $\mathfrak{M}$. For all $E\_1, E\_2 \in \operatorname{coh}(X)$, it satisfies:  
> \\[
\nu\_{\mathfrak{M}}(E\_1 \oplus E\_2) = (-1)^{\bar{X}([E\_1],[E\_2])} \nu\_{\mathfrak{M}}(E\_1) \nu\_{\mathfrak{M}}(E\_2),
\\] 
> and 
> \\[
\int\_{[\lambda] \in \mathbb{P}(Ext^1(E\_2,E\_1))} \nu\_{\mathfrak{M}}(F) \, d\chi - \int\_{[\bar{\lambda}] \in \mathbb{P}(Ext^1(E\_1,E\_2))} \nu\_{\mathfrak{M}}(\tilde{F}) \, d\chi \\
= (\dim Ext^1(E\_2, E\_1) - \dim Ext^1(E\_1, E\_2)) \nu\_{\mathfrak{M}}(E\_1 \oplus E\_2).
\\] 
>
> Here the correspondence between $[\lambda] \in \mathbb{P}(Ext^1(E\_2,E\_1))$ and $F \in \operatorname{coh}(X)$ is that $[\lambda] \in \mathbb{P}(Ext^1(E\_2,E\_1))$ lifts to some $0 \neq \lambda \in Ext^1(E\_2,E\_1)$, which corresponds to a short exact sequence $0 \to E\_1 \to F \to E\_2 \to 0$ in $\operatorname{coh}(X)$ in the usual way. The function $[\lambda] \mapsto \nu\_{\mathfrak{M}}(F)$ is a constructible function $\mathbb{P}(Ext^1(E\_2,E\_1)) \to \mathbb{Z}$, and the integrals are integrals of constructible functions using the Euler characteristic as measure.

Here they uses gauge theory and transcendental complex analytic geometry methods.

> **Definition 3.2.** Define a Lie algebra $\tilde{L}(X)$ to be the $\mathbb{Q}$-vector space with basis of symbols $\tilde{\lambda}^{\alpha}$ for $\alpha \in K^{\text{num}}(\text{coh}(X))$, with Lie bracket
> \\[
[\tilde{\lambda}^{\alpha}, \tilde{\lambda}^{\beta}] = (-1)^{\bar{\chi}(\alpha, \beta)} \bar{\chi}(\alpha, \beta) \tilde{\lambda}^{\alpha + \beta},
\\]
>
 As $\bar{\chi}$ is antisymmetric, this satisfies the Jacobi identity, and makes $\tilde{L}(X)$ into an infinite-dimensional Lie algebra over $\mathbb{Q}$.
>
> Define a $\mathbb{Q}$-linear map $\tilde{\Psi}^{\chi,\mathbb{Q}}:\widehat{\text{SF}}\_{\text{al}}^{ind}(\mathfrak{M}, \chi, \mathbb{Q})\to \tilde{L}(X)$ by
> \\[
\tilde{\Psi}^{\chi,\mathbb{Q}}(f) = \sum\_{\alpha \in K^{\text{num}}(\text{coh}(X))} \gamma^{\alpha} \tilde{\lambda}^{\alpha},
\\]
> where $\gamma^{\alpha} \in \mathbb{Q}$ is defined as follows. Write $f|\_{\mathfrak{M}^{\alpha}}=\sum\_{i=1}^n\delta_i[(U_i\times[\text{Spec}\mathbb C/\mathbb G\_m],\rho_i)]$ where $\delta_i\in\mathbb Q$ and $U_i$ is a quasiprojective variety, and set
> \\[
\gamma^{\alpha} = \sum\_{i=1}^{n} \delta\_i \chi(U\_i, \rho\_i^* (\nu\_{\mathfrak{M}})),
\\]
>
> where $\rho\_i^* (\nu\_{\mathfrak{M}})$ is the pullback of the Behrend function $\nu\_{\mathfrak{M}}$ to a constructible function on $U\_i \times [\text{Spec }\mathbb C / \mathbb{G}\_m]$, or equivalently on $U\_i$, and $\chi(U\_i, \rho\_i^* (\nu\_{\mathfrak{M}}))$ is the Euler characteristic of $U\_i$ weighted by $\rho\_i^* (\nu\_{\mathfrak{M}})$. Define $\tilde{\Psi} : \text{SF}\_{\text{al}}^{ind}(\mathfrak{M}) \rightarrow \tilde{L}(X)$ by $\tilde{\Psi} = \tilde{\Psi} ^{\chi,\mathbb{Q}} \circ{\Pi}\_{\mathfrak{M}}^{\chi,\mathbb{Q}}$.
>
> Here is an alternative way to write $\tilde{\Psi}^{\chi,\mathbb{Q}}$, $\tilde{\Psi}$ using constructible functions. Define a $\mathbb{Q}$-linear map $\Pi\_{\text{CF}} :\widehat{\text{SF}}\_{\text{al}}^{ind}(\mathfrak{M}, \chi, \mathbb{Q}) \rightarrow \text{CF}(\mathfrak{M})$ by
> \\[
\Pi\_{\text{CF}} : \sum\_{i=1}^{n} \delta\_i [(U\_i \times [\text{Spec } C / \mathbb{G}\_m], \rho\_i)] \mapsto \sum\_{i=1}^{n} \delta\_i \text{CF}^{\text{na}}(\rho\_i)(1\_{U\_i}).
\\]
> Then we have
> \\[
\tilde{\Psi}^{\chi,\mathbb{Q}}(f) = \sum\_{\alpha \in K^{\text{num}}(\text{coh}(X))} \chi^{\text{na}} (\mathfrak{M}^{\alpha}, (\Pi\_{\text{CF}}(f) \cdot \nu\_{\mathfrak{M}})|\_{\mathfrak{M}^{\alpha}}) \tilde{\lambda}^{\alpha},
\\]
> and
> \\[
\tilde{\Psi}(f) = \sum\_{\alpha \in K^{\text{num}}(\text{coh}(X))} \chi^{\text{na}} (\mathfrak{M}^{\alpha}, (\Pi\_{\text{CF}} \circ \tilde{\Pi}\_{\mathfrak{M}}^{\chi,\mathbb{Q}}(f) \cdot \nu\_{\mathfrak{M}})|\_{\mathfrak{M}^{\alpha}}) \tilde{\lambda}^{\alpha}.
\\]

> **Theorem 3.3.** Maps $\tilde{\Psi} : \text{SF}\_{\text{al}}^{ind}(\mathfrak{M}) \rightarrow \tilde{L}(X)$ and
> $\tilde{\Psi}^{\chi,\mathbb{Q}}:\widehat{\text{SF}}\_{\text{al}}^{ind}(\mathfrak{M}, \chi, \mathbb{Q})\to \tilde{L}(X)$ are Lie algebra morphisms.

> **Definition 3.4.** Let $X$ be a strict projective Calabi-Yau 3-fold over $\mathbb{C}$, let $\mathscr O\_X(1)$ be a very ample line bundle on $X$, and let $(\tau, G, \leq)$ be Gieseker stability and $(\mu, M, \leq)$ be $\mu$-stability on $\text{coh}(X)$ w.r.t. $\mathscr O\_X(1)$. We define **generalized Donaldson-Thomas invariants** $\bar{\text{DT}}^\alpha(\tau) \in \mathbb{Q}$ and $\bar{\text{DT}}^\alpha(\mu) \in \mathbb{Q}$ for all $\alpha \in C(\text{coh}(X))$ by
>
> \\[
\tilde{\Psi}(\bar{\epsilon}^{\alpha}(\tau)) = -\bar{\text{DT}}^\alpha(\tau)\tilde{\lambda}^{\alpha} \quad \text{and} \quad 
\tilde{\Psi}(\bar{\epsilon}^{\alpha}(\mu)) = -\bar{\text{DT}}^\alpha(\mu)\tilde{\lambda}^{\alpha}.
\\]
>
> We can also have an alternative expression as above and we will omit this.

These are **invariants** since the following theorem:

> **Theorem 3.5.** Using the expression of generalized DT invariants by the Joyce-Song stable pair invariants (see section 5.4 in [JS11][^1]) and the fact that the Chern character maps $K^{\text{num}}(\text{Coh}(X))$ into a subgroup(a lattice) of $H^{2*}(X,\mathbb Q)$ which force $K^{\text{num}}(\text{Coh}(X))$ depends only on the underlying topological space of $X$ (see section 4.5 in [JS11][^1]), we can show that the **generalized Donaldson-Thomas invariants** $\bar{\text{DT}}^\alpha(\tau) \in \mathbb{Q}$ are unchanged under continuous deformations of complex structures.

### 3.2. Compare with Usually DT-Invariants

Now we compare this and the ordinary DT-invariants above.

> **Theorem 3.6.** If $\mathcal M^{\alpha\text{-ss}}(\tau)=\mathcal M^{\alpha\text{-st}}(\tau)$, then
> \\[\bar{\text{DT}}^\alpha(\tau)={\text{DT}}^\alpha(\tau):=\int\_{[M^{\alpha\text{-st}}(\tau)]^{\text{vir}}}1\in\mathbb Z.\\]
>
>> *Proof.* In this case we have $\bar{\epsilon}^{\alpha}(\tau)=\delta^{\alpha}\_{\text{ss}}(\tau)=[(\mathcal M^{\alpha\text{-st}}(\tau),\iota)]$.
>> Let $\pi:\mathcal M^{\alpha\text{-st}}(\tau)\to M^{\alpha\text{-st}}(\tau)$ be the good moduli space and then we have
>> \\[\bar{\text{DT}}^\alpha(\tau)=-\chi^{\text{na}}(\mathcal M^{\alpha\text{-st}}(\tau),\nu_{\mathcal M^{\alpha\text{-st}}(\tau)})\\]
>> as the definition and that $\chi$ is a motivic invariants and $\pi$ is a $B\mathbb G_m$-gerbe. Then
>> \\[-\chi^{\text{na}}(\mathcal M^{\alpha\text{-st}}(\tau),\nu\_{\mathcal M^{\alpha\text{-st}}(\tau)})
=\chi^{\text{na}}(\mathcal M^{\alpha\text{-st}}(\tau),\pi^*\nu\_{M^{\alpha\text{-st}}(\tau)})
=\chi^{\text{na}}(M^{\alpha\text{-st}}(\tau),\nu\_{M^{\alpha\text{-st}}(\tau)}).\\]
>> Hence \\[\bar{\text{DT}}^\alpha(\tau)={\text{DT}}^\alpha(\tau):=\int\_{[M^{\alpha\text{-st}}(\tau)]^{\text{vir}}}1 \\]
>> by Behrend's result.

### 3.3. Where We Use the "Strict"?

There are two places we use $H^1(X,\mathscr O\_X)=0$:

- In the proof of **Theorem 3.1** about the global stacky Behrend function, we use a fact that $\mathfrak M$ is locally isomorphjic to the moduli stack of vector bundles. The proof of this fact uses the Seidel-Thomas twists by $\mathscr O\_X(-n)$. We need $\mathscr O\_X(-n)$ is a spherical object, that is, if $H^1(X,\mathscr O\_X)=0$.
- In the proof of **Theorem 3.5.**, we use the fact that the Chern character maps $K^{\text{num}}(\text{Coh}(X))$ into a subgroup of $H^{2*}(X,\mathbb Q)$ which force $K^{\text{num}}(\text{Coh}(X))$ depends only on the underlying topological space of $X$. This is right for $H^1(X,\mathscr O\_X)=0$.


## 4. BPS Invariants and the Integrality

Note that by a direct calculation (as section 6.1 in [JS11][^1]), we find that given a rigid $\tau$-stable sheaf $E$ in class $\alpha$, the sheaves $mE$ contribute $1/m^2$ to $\bar{\text{DT}}^{m\alpha}(\tau) for all $m\geq 1$. Therefore we may guess that the generalized DT-invariants comes from some another invariants of integral value with weights of form $1/m^2$.




[^1]: [JS11] Dominic Joyce and Yinan Song. A theory of generalized Donaldson-Thomas invariants. Amer. Math. Soc. 2011. See also [arXiv:0810.5645](https://arxiv.org/abs/0810.5645).

[^2]: [BBJ19] Brav, C., Bussi, V., Joyce, D.: A Darboux theorem for derived schemes with shifted symplectic structure. J. Amer. Math. Soc. 32, 399–443 (2019)


