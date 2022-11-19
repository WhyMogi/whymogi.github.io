---
layout: post
title: Algebraic Groups (1)
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
\newcommand{\GL}{\mathrm{GL}}
\newcommand{\cHom}{\mathcal{H}om}
\newcommand{\Id}{\mathrm{Id}}
\newcommand{\Pic}{\mathrm{Pic}}
\newcommand{\rProj}{\underline\mathrm{Proj}\,}
\newcommand{\rank}{\mathrm{rank}\,}
\newcommand{\SL}{\mathrm{SL}}
\newcommand{\SO}{\mathrm{SO}}
\newcommand{\Sp}{\mathrm{Sp}}
\newcommand{\rSpec}{\underline\mathrm{Spec}\,}
\newcommand{\Spec}{\mathrm{Spec}\,}
\newcommand{\Sym}{\mathrm{Sym}\,}\\]

# Before Start

This post series for introducing algebraic groups. We start it with variety (not as a scheme, although it can be identified as schemes. Explicitly, affine varieties are given as).

The order of contents was followed from some lecture note that doesn't want to be disclosed. Instead, I just list references.

I assume we all know very basic definition of varieties (see \[1\] Chapter 1 or \[2\] chapter I)

# Convention

In this post, we assume field $k$ is algebraically closed.

We assume variety is **not necessarily** irreducible. If it is irreducible, I will indicate them.

# Start

## (Basic) Definitions and Examples

We list several varieties from easy things. Before start, we see some definitions that we are interested in.

### 1

An **algebraic group** is a variety $G$ with three morphism (or called regular maps) of varieties $m:G\times G\rightarrow G$, $i:G\rightarrow G$, and $e:\{\ast\} \rightarrow G$ where 

- $m$ satisfies $m(m(a,b),c)=m((a,m(b,c)))$, 
- for any $a\in G$, $b:=i(a)$ satisfies $m(a,b)=e=m(b,a)$ where (abusing notation) $e$ is the image of $e$. 

From now on, $e$ usually means the image of $e$ and called the **identity** of $G$. Also $i$ is called the **inverse** map, and $m$ is called **multiplication** of $G$.

This definition is similar to the definition groups but multiplication has (more) condition.

An **affine algebraic group** is an algebraic group which is affine. 

A complete algebraic group is called **abelian variety**.

### 2

The space $X:=\GL\_{n}$ of $n\times n$ matrix (called **general linear group**) is an algebraic group. It is identified as $\bA^{n^2}$ where $m:X\times X\rightarrow X$ is given as the usual product of matrix and $i$ is the inverse of matrix and $e$ is the identity matrix. These maps are regular maps because it is written as polynomials. 

Some note: consider determinant formula $\det$ with $n^2$ variables. (For example, if $n=2$ the formula looks like $\det(a,b,c,d)=ad-bc$.)

Then $\GL_n$ is an open subset of $\bA^{n^2}$ (complement of $\det=0$). 

The space $\bG_a=k$ is called the **additive group**. Multiplication are induced from addition of $k$. We  often write $\bG_a=\bA^1_k$ as a line.

The space $\bG_m=k^\times:=k-\\{0\\}$ is called the **multiplicative group**. Multiplication are induced from multiplication of $k$. We can view this as the open set of $\bG_a$.

### 3

The **morphism** of algebraic groups $f:G\rightarrow G'$ is a regular morphism of varieties which preserves $m$: meaning $m_{G'}(f(x),f(y))=m_G(x,y)$ for every $x,y\in G$. If the inverse of $f$ exists (there is morphism of algebraic groups where $f\circ h$ and $h\circ f$ are identites), then $f$ is an **isomorphism**.

Let $\varphi:X\rightarrow Y$ be a morphism of irreducible varieties. It is **dominant** if $\varphi(X)$ is dense in $Y$. It is **separable** if the induced field extension $k(Y)\rightarrow k(X)$ of quotient fields of $X$ and $Y$ is a separable extension.

### 4

We prove very useful statement for constructing algebraic groups.

A closed subgroup of an algebraic group is again algebraic group.

Proof is easy. Just show $m':H\times H\rightarrow H$ and $i:H\rightarrow H$ are regular maps of varieties.


### 5

From general linear group, we can construct (famous) algebraic affine group. Let $X=\Gl_n$

(**Special linear group**) $\SL_n$ is a closed subvariety of $X$ with $\det=1$.

From this example write $J_n$ as the $n\times n$ matrix where $(i,j)$-th entry of $J_n$ is a [Kronecker delta](https://en.wikipedia.org/wiki/Kronecker_delta) $\delta_{i,n+1-j}$ and given matrix $x$, $x^t$ means the [transpose](https://en.wikipedia.org/wiki/Transpose) of $x$.

(**Special orthogonal group**)  In here, we assume the characteristic of $k$ is not $2$. 

When $n$ is even, $\SO(n)$ is a closed subvariety of $x\in X$ that satisfies equation $x^tJ_{n}x=J_n$. 

When $n$ is odd, $\SO(n)$ is a closed subvariety of $x\in X$ that satisfies equation $x^tJ'_{n}x=J'_n$ where $J'n$ is a matrix of diagonal matrix where $(1,1)$-entry is $1$ and other part is $J_{n-1}$. 

(Note that equations are just a lot of polynomials so they are closed. A (easy but) hard part is to show these are groups)

(Translation of algebraic subgroups) Let $H$ is a closed algebraic subgroup of $G$. For any $x\in G$, we define $xH$ by the image of $H$ with map $\times x:G\rightarrow G$. It is an isomorphism (its inverse is $x^{-1}$). Because $H$ is closed, $xH$ is closed as well (of course it is not a group).

### 6

Back to algebraic group $G$, irreducible components and connected components are closed. We will investigate these later.

### 7

We can define group action of algebraic groups on variety $X$: if there is a regular map $\mu:G\times X\rightarrow X$ such that (1) $\mu(ab,x)=a\mu(b,x)$ and (2) $\mu(e,x)=x$ for every $a,b\in G$ and $x\in X$ ($e$ is an identity of $G$ and $ab:=m(a,b)$), then we say $X$ is a $G$-**variety** (or $G$-**space**). If the action is transitive, then $X$ is called a **homogeneous space**.

Given $G$-space $X$, we define **orbit** of $x\in X$ as
\\[G\cdot x:=\{g\cdot x\mid g\in G\\},\\]
and the **isotropy group** of $x\in X$ as
\\[G_x=\{g\in G\mid g\cdot x=x\\}.\\]

Note that $G_x$ is a closed subset of $G$ because $G_x$ can be written as the inverse image of $x$ with $\mu_x:G\times \{x\}\rightarrow X$ (restriction of $\mu$).

### 8

This is a nontrivial result. For proof, see \[3\] section 5.5. Before start, we define

We construct quotient of varieties similar to quotient of groups. In detail, given algebraic group $G$ and a closed subgroup $H$ of $G$, we want to find a homogeneous space $G/H$ of $G$ (called **quotient**) such that

- There is a morphism $\pi:G\rightarrow G/H$ (of algebraic groups) and a point $a\in G/H$ such that $G_a=H$.
- With fixed $x\in X$, $\mu(-,x):g\mapsto g\cdot x$ induces a separable morphism $G^0\rightarrow \mu(-,x)G^0$ where $G^0$ is a irreducible component of $G$ containing identity element $e\in G$.
- The fibers of $\pi$ are the cosets $gH$ for some $g\in G$.

Remark that $H$ is not necessarily normal in $G$. 

$G/H$ satisfies universal property: If there is a morphism $\pi':G\rightarrow Y$ of algebraic group such that $H\subset G_b$ for some $b\in Y$, then there is unique morphism $\theta:G/H\rightarrow Y$ such that $\theta\circ\pi=\pi'$ and $\theta(a)=b$.

In next post, we will see some concrete examples!

# Reference

I don't want to write references in formal way. To clarify, I added link.

\[1\]: Ulrich Görtz, Torsten Wedhorn, Algebraic Geometry I: Schemes With Examples and Exercises ([link](https://link.springer.com/book/10.1007/978-3-658-30733-2)).

\[2\]: James E. Humphreys, Linear Algebraic Groups ([link](https://link.springer.com/book/10.1007/978-1-4684-9443-3)).

\[3\]: T. A. Springer, Linear Algebraic Groups ([link](https://link.springer.com/book/10.1007/978-0-8176-4840-4))