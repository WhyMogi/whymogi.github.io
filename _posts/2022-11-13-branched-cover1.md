---
layout: post
title: Cover (1)
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
\newcommand{\cHom}{\mathcal{H}om}
\newcommand{\Id}{\text{Id}}
\newcommand{\Pic}{\mathrm{Pic}}
\newcommand{\rank}{\mathrm{rank}\,}
\newcommand{\rProj}{\underline\mathrm{Proj}\,}
\newcommand{\rSpec}{\underline\mathrm{Spec}\,}
\newcommand{\Spec}{\mathrm{Spec}\,}
\newcommand{\Sym}{\mathrm{Sym}\,}\\]

# Before start

This post was made for the proof of heading 3.3 of this [post](/_posts/2022-11-11-k3-surfaces1.md). See convention, definitions from there.

# Start

## Definition

### 1

Let $f:X\rightarrow Y$ be a morphism of scheme. The support of $\Omega_f$ is called the **ramification locus** and the image of ramification locus is called the **branch locus**.

When $\Omega_f=0$ and $f$ is locally of finite type, we say $f$ is **unramified**.

### 2

Let $\cA$ be a locally free sheaf of finite rank on locally ringed space $(X,O_X)$. The **total space** of $\cA$ is given as 

\\[\rSpec(\Sym \cA^\vee)=\rSpec(O_X\oplus \cA^\vee \oplus (\cA^\vee)^{\otimes 2}\oplus \cdots).\\]


### 3

Let $X$ be an integral scheme and $D$ be an cartier divisor. Then we have a canonical map $O_X(-D)\rightarrow O_X$. After tensoring $O(D)$ to this morphism, we have a map $O_X\rightarrow O_X(D)$. Define canonical section $s_D$ of $D$ as the image of $1\in \Gamma(X,O_X)$.

When $D$ is effective, the zero set of $s_D$ is same as the Weil divisor corresponding to $D$. Note that the corresponding Weil divisor is same as the support of $D$ which is same as the zero set of $s_D$.

## $n$-fold cover.

### 1

Consider this situation. Let $X$ be a smooth projective variety and $\cL$ be a invertible sheaf on $X$. Pick $0\neq s\in \Gamma(X,\cL^n)$ and define $D$ as the zero locus of $s$.

We want to find a map $f:Y\righarrow X$ that the branch locus is precisely $D$ and *looks like* $n$ *cover*.

![picture1](/assets/1113_1.jpg)

The setting of $Y\rightarrow X$ is not that difficult. Let $t$ be the canonical section of $\pi^*\cL$ Set $Y$ by the closed subscheme of total space $X'$ of $\cL$ cut out by equation $t^n-\pi^*(s)$ where $\pi:X'\rightarrow X$ is a canonical map and $\pi^*(s)$ is defined as follows. $s$ induces a morphism $s:O_X\rightarrow \cL^n$ (by multiplication). Then we have a map $\pi^*(s):O\_{X'}\rightarrow \pi^*\cL^n$. Then $\pi^\*(s)\in \Gamma(X,\pi^\*(\cL^n))$ is the image of $1\in O_{X'}$.