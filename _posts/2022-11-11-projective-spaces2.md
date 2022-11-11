---
layout: post
title: Projective spaces (2)
tags: 
- AG
---
\\[\newcommand{\bA}{\mathbb{A}}
\newcommand{\bR}{\mathbb{R}}
\newcommand{\bC}{\mathbb{C}}
\newcommand{\bD}{\mathbb{D}}
\newcommand{\bF}{\mathbb{F}}
\newcommand{\bG}{\mathbb{G}}
\newcommand{\bH}{\mathbb{H}}
\newcommand{\bN}{\mathbb{N}}
\newcommand{\bP}{\mathbb{P}}
\newcommand{\bQ}{\mathbb{Q}}
\newcommand{\bT}{\mathbb{T}}
\newcommand{\bU}{\mathbb{U}}
\newcommand{\bZ}{\mathbb{Z}}
\newcommand{\cA}{\mathcal{A}}
\newcommand{\cB}{\mathcal{B}}
\newcommand{\cC}{\mathcal{C}}
\newcommand{\cD}{\mathcal{D}}
\newcommand{\cE}{\mathcal{E}}
\newcommand{\cF}{\mathcal{F}}
\newcommand{\cG}{\mathcal{G}}
\newcommand{\cH}{\mathcal{H}}
\newcommand{\cHom}{\mathcal{H}om}
\newcommand{\cI}{\mathcal{I}}
\newcommand{\cJ}{\mathcal{J}}
\newcommand{\cK}{\mathcal{K}}
\newcommand{\cL}{\mathcal{L}}
\newcommand{\cM}{\mathcal{M}}
\newcommand{\cN}{\mathcal{N}}
\newcommand{\cP}{\mathcal{P}}
\newcommand{\cT}{\mathcal{T}}
\newcommand{\cU}{\mathcal{U}}
\newcommand{\cX}{\mathcal{X}}
\newcommand{\fa}{\mathfrak{a}}
\newcommand{\fd}{\mathfrak{d}}
\newcommand{\fm}{\mathfrak{m}}
\newcommand{\fn}{\mathfrak{n}}
\newcommand{\fp}{\mathfrak{p}}
\newcommand{\fq}{\mathfrak{q}}
\newcommand{\Bl}{\text{Bl}}
\newcommand{\Id}{\text{Id}}
\newcommand{\rProj}{\underline\mathrm{Proj}\,}
\newcommand{\Spec}{\mathrm{Spec}\,}
\newcommand{\Proj}{\mathrm{Proj}\,}\\]

# This post is not complete.

# Before start

It is a continuous from post [projective space (2)](2022-11-11-projective-spaces1.md)

See conventions from there.

In here, I try to focus on listing statements instead of long proof.

## Some facts from Cohomology

### 1
(See \[1\] chapter III.1 and 2 for complete discussion)

Reamrk that given scheme $(X,O_X)$, the $n$-th cohomological group $H^n(X,-)$ is the $n$-th derived functor of $\Gamma(X,-)$. In here we collect several results (collected from \[1\] Chapter III.2.). In here we first assume $X$ is just a topological spaces.

1. When $X$ is noetherian of dimension $n$ and $\cF$ is an sheaf of abelian groups on $X$, $H^i(X,\cF)=0$ for every $i>n$.

2. Let $\{\cF_k\}_k$ be a direct system of abelian sheaves. Then 
$$\varinjlim H^i(X,\cF_k)= H^i(X, \varinjlim \cF_k).$$ 

3. Let $i:Y\rightarrow X$ be the inclusion. Then $H^i(Y,\cF)=H^i(X,i_*\cF)$.

### 2

(See \[1\] chapter III.3 for complete discussion)

We develope cohomology into scheme. Definition is not changed but we have more good situations. The followings are equivalent (\[1\] Theorem III.3.7.).

- $X$ is affine
- $H^i(X,\cF)=0$ for every quasi-coherent sheaves $\cF$ on $X$ and every $i>0$.
- $H^1(X,\cJ)=0$ for every coherent ideal sheaf $\cJ\subset O_X$.

### 3

When scheme $X$ is noetherian separated scheme, we have another description of cohomology of sheaves. It is called [Čech cohomology](https://en.wikipedia.org/wiki/%C4%8Cech_cohomology). Please see the site or \[1\] chapter III.4. (definition involves too much index)

We have very useful theorem (see \[1\] Theorem III.4.5): If $\cF$ is a quasi coherent sheaf on $X$, then we have an isomorphism
\\[\check{H}^p(\cU,\cF)\cong H^p(X,\cF)\\]
where the $\check{H}^p(\cU,-)$ means the $p$-th Čech cohomology.

Čech cohomology is easy to compute (in my opinion). Here is some example. Let $X=\bP^1_k$ be a scheme with sheaf of differential $\cF$ on $X$.


# To be filled later!

# Reference

I don't want to write references in formal way. To clarify, I added link.

\[1\]: R. Hartshonre, Algebraic Geometry ([link](https://link.springer.com/book/10.1007/978-1-4757-3849-0)).

\[2\]: Ulrich Görtz, Torsten Wedhorn, Algebraic Geometry I: Schemes With Examples and Exercises ([link](https://link.springer.com/book/10.1007/978-3-658-30733-2)).