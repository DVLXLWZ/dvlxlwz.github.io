---
title: "Fushforward of Line Bundles Between Projective Lines"
collection: Blogs
permalink: /Blogs/2023-04-22-Fushforward-of-Line-Bundles-Between-Projective-Lines
excerpt_separator: <!--more-->
date: 2023-04-22
---
This is an interesting problem is that for any finite flat covering $f:\mathbb{P}^1\to \mathbb{P}^1$, how to compute $f\_* \mathscr{O}(m)$?
<!--more-->

Now we want to find the following:

> Let $f:\mathbb{P}^1\to \mathbb{P}^1$ be a finite flat covering of degree $n$, what is $f\_* \mathscr{O}(m)$?

Here we give a proof which the method I saw a long time ago as follows:

【Proof.】We know that $f\_* \mathscr{O}(m)$ is a vector bundle over $\mathbb{P}^1$. By the classification of vector bundles we can let

$$
f_* \mathscr{O}(m)=\bigoplus_{k\in\mathbb{Z}}\mathscr{O}(k)^{\ell(m,k)}.
$$
By projection formula, we have $f\_* (\mathscr{O}(m-nk))\cong f\_* (\mathscr{O}(m))\otimes\mathscr{O}(-k)$, hence we get $\ell(m,k)=\ell(m-nk,0)$.
Taking $h^0$ we have $m+1=\sum\_{k\geq 0}\ell(m,k)$
