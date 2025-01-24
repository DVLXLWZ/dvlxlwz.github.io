---
title: "A Brief Introduction to the Virtual Intersection Theory"
collection: Blogs
permalink: /Blogs/2025-01-14-A-Brief-Introduction-to-the-Virtual-Intersection-Theory
excerpt_separator: <!--more-->
date: 2025-01-14
---
This is a basic and quick introduction of the virtual intersection theory introduced by [BF97][^2] and [Man12][^4] and give some more properties of these theories.
<!--more-->

## 0. Background and History

The virtual intersection theory comes from the goal to define the modern enumerative invariants. The most fundamental philosophy in the area of enumerative geometry is that, we need to consider the intersection theory 
in the moduli space of the objects you want to consider.
We have seen this in the problems of classical enumerative geometry:

> **Example 0.1.** For example, for a general cubic 3-fold $X$, the Fano scheme $F(X)$ (Hilbert scheme of lines) consist of several isolated
reduced points. So what we count is 
\\[N=\int_{[F(X)]}1=27,\\] 
where $[F(X)]$ is the fundamental class of $F(X)$.

But note also that the most of the modern enumerative geometry come from the physics, especially the string theory. Recall that in the world of string theory, general relativity and quantum mechanics are unified at a cost:
\\[\mathsf{SpaceTime}=\bb R^3\times\bb R^1\times X\\]
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
the fundamental class $[\mathcal M]$ does not exists. So we need to find some (virtual) class $[\mathcal M]^{\vir}$ which can be used in the intersection
theory and counting some objects we want.

The most basic model of these given in the Chapter
14.1 in [Ful98][^5]:
> **Example 0.2.**
Let $Y$ be a algebraic scheme over some field $k$ of pure dimension $n$ and a vector bundle $E$ of rank $e$ over it.
For any section $s:Y\to E$ of bundle $E$, let $Z(s)$ be the zero locus of this section which forms the following fiber product:
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
\[\begin{tikzcd}
	{Z(s)} && Y \\
	Y && E
	\arrow[from=1-1, to=1-3]
	\arrow["i"', from=1-1, to=2-1]
	\arrow["\ulcorner"{anchor=center, pos=0.125}, draw=none, from=1-1, to=2-3]
	\arrow["s"', hook, from=1-3, to=2-3]
	\arrow["0", hook, from=2-1, to=2-3]
\end{tikzcd}\]
 </p>
</body>
</html>

Then we define 
\\[c_{\mathrm{loc}}(E,s):=0^![Y]=0^*(C_{Z(s)/Y})\in\CH_{n-e}(Z(s))\\] 
be the **localized Chern class** of $E,s$.






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



[^1]: [Beh97] K. Behrend. Gromov–witten invariants in algebraic geometry. Invent. Math., 127:601–617, 1997.

[^2]: [BF97] K. Behrend and B. Fantechi. The intrinsic normal cone. Invent. Math., 128:45–88, 1997.

[^3]: [LT96] Jun Li and Gang Tian. Virtual moduli cycles and gromov–witten invariants of algebraic varieties. J.
Amer. Math. Soc., 11:119–174, 1996

[^4]: [Man12] Cristina Manolache. Virtual pull-backs. J. Algebraic Geom., 21:201–245, 2012.

[^5]: [Ful98] William Fulton. Intersection Theory. Springer New York, 1998.



