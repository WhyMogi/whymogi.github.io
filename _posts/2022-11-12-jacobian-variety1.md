---
layout: post
title: Jacobian variety (1)
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
\newcommand{\DivCl}{\mathrm{DivCl}}
\newcommand{\cHom}{\mathcal{H}om}
\newcommand{\Id}{\text{Id}}
\newcommand{\Jac}{\mathrm{Jac}}
\newcommand{\Pic}{\mathrm{Pic}}
\newcommand{\Pic0}{\mathrm{Pic}^0\,}
\newcommand{\rank}{\mathrm{rank}\,}
\newcommand{\rProj}{\underline\mathrm{Proj}\,}
\newcommand{\Spec}{\mathrm{Spec}\,}\\]

# To be filled later. It is a draft. I don't know what to put.

# Before Start

This is a short note of Jacobian variety. I followed \[1\].

# Convention

Usually $k$ means a field (not necessarily algebraically closed).

**Variety** over $k$ means a separated, geometrically integral scheme of finite type over $k$.

In here we assume $X$ is **projective** variety (closed variety contained in some projective space $\bP^n_k$)

Divisors means Weil divisors. If it is Cartier, then I will indicate it.

# Start

## Some definitions (Review)

### 1

Let $C$ be a curve. If we have a divisor 
\\[D:=\sum_i n_i\cdot p_i\\]
where $p_i$ is a point of $C$, then the degree of $D$ is defined as 
\\[\deg(D):=\sum_i n_i.\\]

We develope it in Cartier divisor. Given Cartier divisor $D=\\{(U_i,f_i)\\}$, the associated divisor is

\\[\sum_{x\in X} m_x(D)\cdot x\\]

where $m_x$ is the order of $(f_i)_x\in O_{X,x}$ (note that it is well defined). Thus we can define the order of Cartier divisor as  

\\[\deg(D):=\sum_x m_x.\\]

### 2

Let $C$ be a curve. Define $\Pic0 (C)$ by the subgroup of $\Pic(C)$ of divisor classes of degree $0$. In general, given abelian variety $A$ we define $\Pic0 (A)$ be the set of classes of invertible sheaves $\cL$ where $\lambda_\cL=0$. 

The map $\lambda_\cL$ is defined as follows:
\\[\lambda_\cL:A(k)\rightarrow \Pic(A),\quad a\mapsto t_a^*\cL\otimes \cL^{-1}\\]
where $A(k)$ is a $k$-valued point of $A$ and  $t_a:A\rightarrow A$ is given by the composition
\\[A\rightarrow A\times A\xrightarrow{m} A,\quad x\mapsto (x,a)\mapsto xa\\]
where $m:A\times A\rightarrow A$ is a multiplication of abelian variety $A$.

Note that $\lambda_\cL$ is a homomorphism (see \[1\] I.5.5,I.5.6).

## Definition (Jacobian variety)

### 1

Let $C$ be a nonsingular projective curve over field $k$ and $T$ be a nonsingular variety. Define
\\[P^0_C(T):=\Pic0 (C\times T)/q^*\Pic^0(T)\\] 
where $q:C\times T\rightarrow T$ is a projection.

If $C(k)\neq\emptyset$, then  $P^0_C$ is represented by an abelian variety $J$. We call $J$ the **Jacobian variety** of $C$ (or write it as $\Jac(C)$).



# Reference

I don't want to write references in formal way. To clarify, I added link.

\[1\]: J. S. Milne, Abelian Varieties ([link](https://www.jmilne.org/math/CourseNotes/AV.pdf)).