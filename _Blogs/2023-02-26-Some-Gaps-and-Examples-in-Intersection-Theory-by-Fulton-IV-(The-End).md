---
title: "Some Gaps and Examples in Intersection Theory by Fulton IV (The End)"
collection: Blogs
permalink: /Blogs/2023-02-26-Some-Gaps-and-Examples-in-Intersection-Theory-by-Fulton-IV-(The-End)
excerpt_separator: <!--more-->
date: 2023-02-26
---
This is one of a series of blogs aiming to complete some details of the examples in this book (*Intersection Theory, 2nd edition* by William Fulton[^1]) and give some comments. This blog we consider chapter 14 to chapter 15.

<!--more-->

> Previously on these:
>
> [Some Gaps and Examples in Intersection Theory by Fulton I](https://dvlxlwz.github.io//Blogs/2022-12-12-Some-Gaps-and-Examples-in-Intersection-Theory-by-Fulton-I);
> 
> [Some Gaps and Examples in Intersection Theory by Fulton II](https://dvlxlwz.github.io//Blogs/2022-12-28-Some-Gaps-and-Examples-in-Intersection-Theory-by-Fulton-II);
> 
> [Some Gaps and Examples in Intersection Theory by Fulton III](https://dvlxlwz.github.io//Blogs/2023-01-19-Some-Gaps-and-Examples-in-Intersection-Theory-by-Fulton-III).

## Chapter 14. Degeneracy Loci and Grassmannians
### Section 14.1. Localized Top Chern Class
**Example 14.1.3.** Let $i:Z(s)\to Z(s\_2)$ and $j:Z(s\_2)\to X$, then we have 
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
j_*i_*\mathbb{Z}(s)&=c_e(E)\cap [X]=c_{e_1}(E_1)c_{e_2}(E_2)\cap [X]\\
  &=c_{e_1}(E_1)\cap j_*\mathbb{Z}(s_2)=j_*(c_{e_1}(j^*E_1)\cap\mathbb{Z}(s_2)),
\end{align*}
</p>
</body>
</html>
as we need to show that $i\_* \mathbb{Z}(s)=c\_{e\_1}(j^* E\_1)\cap\mathbb{Z}(s\_2)$, we don't know is $j\_* $ injective?

**Example 14.1.5.** (a) We have
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
\deg\mathbb{Z}(s_f)&=\int_{\{t_1,...,t_n\}}\mathbb{Z}(s_f)=\int_Xc_n(f^*T_C\otimes T_X^{\vee})\\
  &=(-1)^n\chi(X)+(-1)^{n-1}\int_Xc_1(f^*T_C)c_{n-1}(T_X)\\
  &=(-1)^n\chi(X)+(-1)^{n-1}\int_Cc_1(T_C)\cap f_*(c_{n-1}(T_X)\cap [X]).
\end{align*}
</p>
</body>
</html>
As $f\_* (c\_{n-1}(T\_X)\cap [X])$ is $1$-cycle on $C$, it must of form $n[C]$. Pick a general fiber $X\_t$ with $t\in C$, we get $n=\int\_{X\_t}c\_{n-1}(T\_X\|\_{X\_t})=\chi(X\_t)$, hence we get
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
\deg\mathbb{Z}(s_f)&=(-1)^n\chi(X)+(-1)^{n-1}\int_Cc_1(T_C)\cap f_*(c_{n-1}(T_X)\cap [X])\\
  &=(-1)^n\chi(X)+(-1)^{n-1}\chi(X_t)\int_Cc_1(T_C)\cap [C]=(-1)^n(\chi(X)-\chi(X_t)\chi(C)),
\end{align*}
</p>
</body>
</html>
and well done. $\blacksquare$

### Section 14.2. Gysin Formulas
Let $\underline{A}$ be a flag of vector bundles on $X$, i.e. $0\subsetneqq A\_1\subsetneqq\cdots\subsetneqq A\_d=A$.
Now we may want to define the flag bundle $Fl(\underline{A})$ as an $X$-scheme by a representable functor, if we define
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
Fl(\underline{A})^{???}&:(Sch/X)^{opp}\to^{???}(Sets),\\
  &(f:T\to X)\mapsto^{???} \{D_1\subset\cdots\subset D_d:\dim D_i=i,D_i\subset f^*A_i\},
\end{align*}
</p>
</body>
</html>
then as the case of the Grassmannian we may **lost the functorial-property**, so may not that case!
Note that this is **NOT the triditional flag variety, so if we use the quotient definition, we can not guarantee the inclutions of $A\_i$**! So the only way is to consider the construction in the proof of Proposition 14.2.1.

> For the **triditional flag variety**, we can define that as follows:
>
> Consider the following results taken from [GT20][^2] Proposition 8.10:
>
> *Lemma.* Let $S$ be a scheme and let $i:\mathscr{U}\to\mathscr{E}$ be a morphism of $\mathscr{O}\_S$-modules. Consider the following statements:
>
> (a) The homomorphism $i$ is injective and $\mathscr{E}/\mathscr{U}$ is locally free;
>
> (b) For any scheme-morphism $f:T\to S$ the map $f^* (i):f^* \mathscr{U}\to f^* \mathscr{E}$ is injective.
>
> If $\mathscr{U}$ is any $\mathscr{O}\_S$-module and $\mathscr{E}$ is quasi-coherent, then (a) implies (b); If $\mathscr{U}$ is of finite type and $\mathscr{E}$ finite locally free. Then (a) and (b) are equivalent. $\blacksquare$
>
> Hence we can using the quotient to give a functorial-property-well difinition of triditional flag variety:
> Given a sequence $(d\_1,...,d\_m)$ of positive integers of sum $n$ and fix a vector bundle $E$ over $X$ of rank $n$. A flag of type $(E;d\_1,...,d\_m)$ is $0=V\_0\subset V\_1\subset\cdots\subset V\_m=E$ of bundles in $X$ where $V\_j/V\_{j-1}$ is locally free of rank $d\_j$. Consider the functor $\mathrm{Flag}\_X(E;d\_1,...,d\_m):(Sch/X)^{opp}\to(Sets)$ as $(f:T\to X)\mapsto$ (type $(E;d\_1,...,d\_m)$ flags). Well done.

Over. $\blacksquare$

### Section 14.3. Determinantal Formula
**Theorem 14.3.** When we consider the *universal local case*, the birational morphism $\eta:Z(s\_{\sigma})\to\Omega(\underline{A},\sigma)$ plays an important role. To see that $\eta$ is birational, write down the elements of $\phi^{-1}(x)\cap Z(s\_{\sigma})$ for some $x\in X=\mathbb{A}^{ef}$. We find that this set will contain a single element if we remove the locus where the $\dim\ker\sigma(x)\|\_{A\_i(x)}<i$, that is, the locus where $(a\_i-i)$-minors vanishing in $\Omega(\underline{A},\sigma)$. $\blacksquare$

### Section 14.4. Thom-Porteous Formula
**Example 14.4.5.** 
Here we may assume that $C$ is a smooth curve over some $k$ as it is the same as Example 4.3.2/4.3.3.

As we get $0\to E\_d\to E\_m\to F\_t$, we may then let $m\geq 2g-1$ instead of $t\geq 2g-1$ as by Riemann-Roch theorem we have
\\[h^0(\mathscr{O}(mP\_0)\otimes\mathscr{L}\_x)=m+1-g+h^0(K\_C-mP\_0-\mathscr{L}\_x)\\]
and $\deg(K\_C-mP\_0-\mathscr{L}\_x)=2g-2-m$. But as $m=t+d$, then $t\geq 2g-1$ implies $m\geq 2g-1$.

Not that the $C$ of genus $g$ is of *general moduli* means that the point corresponding to the curve $C$ in the moduli space of genus $g$ curves $M\_g$ does not belong to denumerably many proper subvarieties. $\blacksquare$

**Example 14.4.7.**

**Example 14.4.12.** I don't know what's going on!

### Section 14.6. Grassman Bundles
**Example 14.6.2.**

**Example 14.6.4.** Why and how do we use this?

### Section 14.7. Schubert Calculus
**Example 14.7.7.** This is a standard example to use the Schubert calculus to deal with some simple algebraic geometry problems and we write this as a model.
Note that the first step is to deduce the relations of Schubert relations as Example 14.7.2.

(a) After checking the dimension of $[W\_C]$, we note that $[W\_C]=ag\_p+bg\_e$. Then by Example 14.7.1 we get
\\[a=\int\_{G\_1(\mathbb{P}^3)}[W\_C]\cap (0,3),b=\int\_{G\_1(\mathbb{P}^3)}[W\_C]\cap (1,2).\\]
Then we find that using the definiton of $(a\_0,...,a\_d)$ we get $a$ is just the apparent number $d$ of double points of $C$. Similarly, $b$ is the number of 2 points in whole $\deg C=n$ points over a general plane (by Bertini) and we get $b=\binom{n}{2}$.

(b) After analyze the geometry-meanings, we find that this is just \\[\int\_{G\_1(\mathbb{P}^3)}[W\_C]\cap[V\_{C\_1}]\cap[V\_{C\_2}]\\]
and using the relations in Example 14.7.2 and the results in Example 14.7.6.(a) we get the result.

(c) Similar as (b), we find that this is just \\[\int\_{G\_1(\mathbb{P}^3)}[W\_C]\cap[W\_{C'}]\\]
and well done. $\blacksquare$

**Example 14.7.11.** Need to think that why the hyperplane section of $G$ (in Plucker embedding) coorespond to the $n-d-1$-planes in $\mathbb{P}^n$?

**Example 14.7.12.(d).** How to compute $\int\_Xc\_1((A\_X^{\vee})^{\otimes 2}\otimes\mathscr{O}(1)\_X)^8=92$ and re-think the Example 3.2.22.

**Example 14.7.13.** This is a great result and for details of this we refer [3264EH][^3] Proposition 6.4. Here we give a sketch.

By the property of $S$, we have that the fiber of $S^{\vee}$ at $[L]\in G$ is the space of linear forms on $L$, that is $H^0(\mathscr{O}\_{P(L)}(1)$. Hence the surjection $E\_G^{\vee}\to L^{\vee}$ is the restrict of linear forms to $L$. Hence so is acting $\mathrm{Sym}^m$ to deduce the $m$-degree forms case. Now a degree $m$ hyperplane $X$ defined by a zero of section $g$ of $\mathrm{Sym}^mE^{\vee}$ which deduce a degree $m$ section $g'$ of $\mathrm{Sym}^mS^{\vee}$ by restriction. Hence the zero of $g'$ is the points $[L]$ in $G$ such that $g'\|\_{L}=0$. As $X$ is the zero of $g$, then these $L$ is the $d$-planes in $X$! $\blacksquare$

## Chapter 15. Riemann-Roch for Non-singular Varieties
### Section 15.1. Preliminaries
**Example 15.1.1.** (a) Here we show that $K\_0(\mathbb{P}^m)$ generated by $[\mathscr{O}(n)]$ for $0\leq n\leq m$. Pick any coherent sheaf $\mathscr{F}$ and then $\mathscr{F}\otimes\mathscr{O}(N)$ generated by global sections for some large $N$. Hence we get surjection $\bigoplus\_{j=1}^r\mathscr{O}(-N)\to\mathscr{F}$ as $X$ is quasicompact. Repeat this, and at some point we will get $0$. Hence $K\_0(\mathbb{P}^m)$ generated by $[\mathscr{O}(n)]$ for all $n$.

Next, we consider $\mathscr{O}(m+1)$. Let $V=\bigoplus\_j^{m+1}\mathscr{O}(-1)$ and we claim that we have exact sequence
\\[0\to\bigwedge^{m+1}V\to\bigwedge^{m}V\to\cdots\to\bigwedge^{1}V\to\bigwedge^{0}V\to 0.\\]
this can be check over level of graded modules. Let $S=k[x\_0,...,x\_m]$ and the map $V=\bigoplus\_j^{m+1}S(-1)\to S$ is multiplication by $(x\_0,...,x\_m)$ which induce the maps $\bigwedge^{j+1}V\to\bigwedge^{j}V$. We can check it is exact and we omit it here. Now after taking dual, this exact sequence give us 
\\[0\to\mathscr{O}\to\bigoplus^{m+1}\mathscr{O}(1)\to\cdots\to\bigoplus^{\binom{m+1}{j}}\mathscr{O}(j)\to\cdots\to\bigoplus^{m+1}\mathscr{O}(m)\to\mathscr{O}(m+1)\to0\\]
is exact. Repeat this and we get $K\_0(\mathbb{P}^m)$ generated by $[\mathscr{O}(n)]$ for $0\leq n\leq m$. 

(b) We may use the Exercise II.6.10.(c) in [Har77][^4]. $\blacksquare$

**Example 15.1.4.** In order to compute $\int\_{\mathbb{P}^m}\frac{e^{nx}x^{m+1}}{(1-e^{-x})^{m+1}}$, we just need to compute that after expanding to the power series of $x$, the coefficient of $x^m$ is that value. This is just the residue of $\frac{e^{nx}}{(1-e^{-x})^{m+1}}$ around $x=0$.

Now let $y=1-e^{-x}$, then 
\\[\int\_{C}\frac{e^{nx}}{(1-e^{-x})^{m+1}}dx=-\int\_{C'}\frac{1}{y^{m+1}(1-y)^n}d\log (1-y)=\int\_{C'}\frac{1}{y^{m+1}(1-y)^{n+1}}dx.\\]
Now $\frac{1}{y^{m+1}(1-y)^{n+1}}=\sum\_{i=0}^{\infty}\binom{n+i}{i}y^{i-m-1}$. Hence well done. $\blacksquare$

**Example 15.1.4.** Here thay claim that $F\_kK\_0X$ generated by $[\mathscr{O}\_V]$ for $\dim V\leq k$. WLOG we let $k=\dim X$ and $F\_kK\_0X=K\_0X$. Now let $K\subset K\_0X$ be a subgroup generated by $[\mathscr{O}\_V]$ for $\dim V\leq\dim X$ and we claim that $K=K\_0X$.
First, for any subscheme $Z\subset X$ we have $0\to\mathscr{I}\_Z\to\mathscr{O}\_X\to\mathscr{O}\_Z\to0$, then any ideal sheaf living in $K$. Next we need the following "Devissage" results:

*Lemma.* Let $X$ be a Noetherian scheme. Let $\mathscr{F}$ be a coherent sheaf on $X$. There exists a filtration 
\\[0\subset\mathscr{F}\_0\subset\cdots\subset\mathscr{F}\_m=\mathscr{F}\\]
by coherent subsheaves such that for each $j=1,...,m$ there exist an integral closed subscheme $Z\_j\subset X$ and a nonzero coherent sheaf of ideals $\mathscr{I}\_j$ such that $\mathscr{F}\_j/\mathscr{F}\_{j-1}\cong (Z\_j\to X)\_* \mathscr{I}\_j$.

*Proof.* This is a little bit complicated and we refer [Tag 01YF](https://stacks.math.columbia.edu/tag/01YF). $\blacksquare$

Now using this lemma inductively, we can get that $K=K\_0X$. 
Actually the next argument in the book giving the similar things. $\blacksquare$

### Section 15.2. Grothendieck-Riemann-Roch Theorem
**Example 15.2.10.** Now as we have $0\to\mathscr{O}\_{P(E)}\to p^* E\otimes\mathscr{O}(1)\to T\_{P(E)/X}\to0$, we have
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
\chi(P(E),\mathscr{O}_{P(E)}&=\int_{P(E)}\mathrm{td}(T_{P(E)})\\
  &=\int_{P(E)}\mathrm{td}(p^*T_X)\mathrm{td}(p^* E\otimes\mathscr{O}(1))\\
  &=\int_{X}p_*(\mathrm{td}(p^*T_X)\mathrm{td}(p^* E\otimes\mathscr{O}(1))\cap[P(E)])\\
  &=\int_{X}\mathrm{td}(T_X)p_*(\mathrm{td}(p^* E\otimes\mathscr{O}(1))\cap[P(E)])=?
\end{align*}
</p>
</body>
</html>

**Example 15.2.17.** How can we let $X$ to be the smooth projective variety?

## Chapter 16. Correspondences
### Section 16.1. Algebra of Correspondences
**Example 16.1.4.(c).** As $P$ is rational, if we let $q=P^{XY}\_X$, we have
\\[\int\_{X\times Y}\alpha\cdot[P\times Y]=\int\_{X}q\_* (\alpha\cdot q^* [P])=\int\_{X}q\_* \alpha\cap [P]=d\_1(\alpha)\\]
and well done. $\blacksquare$


## Chapter 17. Bivariant Intersection Theory


[^1]: [FulIT2nd] William Fulton. Intersection Theory, 2nd. Springer New York, NY. 1998.

[^2]: [GT20] Ulrich Görtz, Torsten Wedhorn. Algebraic Geometry I: Schemes, 2nd. Springer Spektrum Wiesbaden. 2020.

[^3]: [3264EH] David Eisenbud, Joe Harris. 3264 and All That, A Second Course in Algebraic Geometry. 2016.

[^4]: [Har77] Robin Hartshorne. Algebraic Geometry. Springer, 1977.
