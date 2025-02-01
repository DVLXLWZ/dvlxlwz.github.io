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
\\]
>
> \\[
\int\_{t \in T^G} |\{w \in W(G, T^G) : w \cdot t = t\}| \left[ ([X^{(t)} / C\_G((t))], \rho \circ l^{(t)}) \right] d\mu.
\\]
>
> Here $X^{(t)}$ is the subvariety of $X$ fixed by $t$, and $l^{(t)} : [X^{(t)} / C\_G((t))] \to [X/G]$ is the obvious 1-morphism of Artin stacks.


### 1.4. Stack Function Spaces Twisted by Euler Characteristics


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


