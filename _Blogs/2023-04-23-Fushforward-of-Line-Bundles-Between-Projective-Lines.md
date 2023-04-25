---
title: "Fushforward of Line Bundles Between Projective Lines"
collection: Blogs
permalink: /Blogs/2023-04-23-Fushforward-of-Line-Bundles-Between-Projective-Lines
excerpt_separator: <!--more-->
date: 2023-04-23
---
This is an interesting problem is that for any finite covering $f:\mathbb{P}^1\to \mathbb{P}^1$, how to compute $f\_* \mathscr{O}(m)$?
<!--more-->

Now we want to find out the following:

> **Question.** Let $f:\mathbb{P}^1\to\mathbb{P}^1$ be a finite morphism of degree $n$, How to compute $f\_* \mathscr{O}(m)$ when $m\geq 0$?

Actually there is a proof which the method I saw a long time ago as follows.

> **Proposition.** Let $f:\mathbb{P}^1\to \mathbb{P}^1$ be a finite map of degree $n$ and let $m\geq 0$. Then for $k\geq 0$ if we let \\[\ell(m,k)=\mathrm{coeff}\_{x^{m-nk}}(1+x+...+x^{n-1})^2,\\] then we have \\[f\_* \mathscr{O}(m)\cong\mathscr{O}(-1)^{\oplus \left(n-\sum\_{k\geq 0}\ell(m,k)\right)}\oplus\bigoplus\_{k\geq 0}\mathscr{O}(k)^{\oplus \sum\_{k\geq 0}\ell(m,k)}.\\]

*Proof.* We know that $f$ is flat automatically since modules over some Dedekind ring is flat if and only if it is torsion free (see [Tag 0AUW](https://stacks.math.columbia.edu/tag/0AUW)). Then $f\_* \mathscr{O}(m)$ is a vector bundle of rank $n$ over $\mathbb{P}^1$. By the classification of vector bundles we can let

$$f_* \mathscr{O}(m)=\bigoplus_{k\in\mathbb{Z}}\mathscr{O}(k)^{\ell(m,k)}.$$

By projection formula, we have $f\_* (\mathscr{O}(m-nk))\cong f\_* (\mathscr{O}(m))\otimes\mathscr{O}(-k)$, hence we get $\ell(m,k)=\ell(m-nk,0)$.
Taking $h^0$ at (3) we have $m+1=\sum\_{k\geq 0}(k+1)\ell(m,k)$. Hence we have
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
\sum_{m\geq 0}(m+1)x^m&=\sum_{m\geq 0}\sum_{k\geq 0}\ell(m,k)(k+1)x^m\\
  &=\sum_{m\geq 0}\sum_{k\geq 0}(k+1)x^{nk}\ell(m,k)x^{m-nk}\\
  &=\sum_{k\geq 0}(k+1)x^{nk}\sum_{m\geq 0}\ell(m,k)x^{m-nk}\\
  &=\sum_{k\geq 0}(k+1)x^{nk}\sum_{m\geq 0}\ell(m-nk,0)x^{m-nk}\\
  &=\sum_{k\geq 0}(k+1)x^{nk}\sum_{m\geq 0}\ell(m,0)x^{m}
\end{align*}
</p>
</body>
</html>
where the last equation holds because for any $j<0$ we have $\ell(j,0)=0$ by checking global sections and then $\sum\_{m\geq 0}\ell(m-nk,0)x^{m-nk}$
will be a constant when $k$ varies.

Hence by taking $m$ to be $m-nk$, hence when $k\geq 0$ we have
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
\ell(m,k)&=\mathrm{coeff}_{x^{m-nk}}\frac{\sum_{m\geq 0}(m+1)x^m}{\sum_{k\geq 0}(k+1)x^{nk}}\\
  &=\mathrm{coeff}_{x^{m-nk}}\left(\frac{1-x^n}{1-x}\right)^2\\
  &=\mathrm{coeff}_{x^{m-nk}}(1+x+...+x^{n-1})^2.
\end{align*}
</p>
</body>
</html>
Now we consider the case when $k<0$. Actually when $k\leq -2$ we get $h^1(\mathbb{P}^1,\mathscr{O}(k))>0$. Hence taking $h^1$ at (3) again we get $\ell(m,k)=0$ in this case! Hence we let

$$
\ell(m,1)=n-\sum_{k\geq 0}\ell(m,k)
$$

and we get the solution! $\blacksquare$

> Corollary. In this case we have $f\_* \mathscr{O}\cong \mathscr{O}\oplus\mathscr{O}(-1)^{\oplus(n-1)}$ and $f\_* \mathscr{O}(1)\cong \mathscr{O}^{\oplus 2}\oplus\mathscr{O}(-1)^{\oplus(n-2)}$.

Similarly you can use the same method to compute other similar cases.



