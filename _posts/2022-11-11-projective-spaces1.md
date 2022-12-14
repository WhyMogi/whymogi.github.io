---
layout: post
title: Projective spaces (1)
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

# Before start

I just collected some useful theorems (at least to me) from scheme theory and sheaf cohomology theory. This post must be updated frquently. However, I assume we know \[1\] Chapter II.5. and definition of sheaf cohomology.

Usually I divide post within some categories (using headers), but I don't do that in this post.

# Convention

$A$ means ring (including field but for emphasizing ring), $k$ means field.

## Some facts of graded rings

We require several facts to understand $\Proj S$ for graded ring $S$. Here are some results (not proved). These are takin from \[2\] Section 13.1. Please see [here](https://en.wikipedia.org/wiki/Graded_ring) for definition of graded ring. I used $\bZ$-grading.

### 1

We add more definitions. Let $S$ be a graded ring. For integer $d>0$, define
$$S^{(d)}:=\bigoplus_{n\geq 0}  S_{nd}$$
where $n$-th degree of $S^{(d)}$ is $S_{nd}$ (it is the $nd$-th degree of $S$). 

Let $M$ be a graded $A$-module. When $f\in A_d$ is a homogeneous of degree $d>0$, we define 
\\[M_{(f)}:=\\{m/f^n\in M_f\mid m\text{ is homogeneous with } \deg m=dn\\}.\\]

In short we say $M_{(f)}$ is the subgroup of $M_f$ whose degree is zero.

Given graded ring $S$, we define ideal $S_+:=\oplus_{d\geq 1} S_d$. A homogeneous prime ideal $\fp$ of $S$ is **relevant** is $A_+\not\subset \fp$. Also we write $I_+:=\oplus_{d\geq 1} I_d$.

For $n,m\geq 1$, define $A_{++}:=\bigoplus_{d\geq n} A_{dm}$. 

### 2

We collect results. Most of them are easy to prove. Let $S$ be a graded ring. Let $\fp,\fp'$ be relevant prime ideals and $\fq$ be a prime ideal. Let $I$ be a homogeneous ideal.

1. If $\fp_+=\fp'_+$, then $\fp=\fp'$.
2. Let $I$ be properly contained in $S_+$, then $I=\fp\_+$ for some homogeneous prime ideal $\fp$ of $S$ if and only if for homogeneous elements $a,b\in S_+$, $ab\in I$ implies $a\in I$ or $b\in I$.
3. We have $(\sqrt{I})_+=(\sqrt{I}) \cap A_+$.
4. $\fq$ is relevant if and only if $\fq$ doesn't contain $A_{++}$.

### 3

(This is a review of \[1\] Chapter 2.2). The set of relevant prime ideals of $S$ is written as $\Proj S$. The closed sets (satisfying the definition of topology) are given as 
$$V_+(I):=\\{\fp\in\Proj S\mid I\subset \fp\\}$$
for homogeneous ideal $I\subset A_+$. For **homogeneous** element $f\in S_+$, define
$$D_+(f):=\Proj S -V_+(f).$$

Note that $\Proj S\subset \Spec S$. It is easy to check
$$V_(\fa)\cap \Proj S=V_+(\fa^h)$$
where $\fa^h$ is a **homogeneous ideal generated** by $\fa$ (ideal generated by homogeneous component of $\fa$. Same meaning: generated by $\fa\cap S_d$ for every $d$). Thus $\Proj S$ is a subspace of $\Spec S$.

From inclusion $S_{(f)}\rightarrow S_f$, we have a continuous map 
\\[D_+(f)\hookrightarrow D(f)\rightarrow \Spec S_{(f)}\\] where the first map is the inclusion. 

---
<span style="color: blue;">Check 1.</span>

Show that it is a homeomorphism.

---

Let $X:=\Proj S$. Define sheaf $O_X(D_+(f)):=S_{(f)}$.

---
<span style="color: blue;">Check 2.</span>

Show that it is a sheaf and $(X,O_X)$ is a scheme.

---

### 5

We usually give condition to graded ring. We assume graded ring $S$ is finitely genertated $S_0$ algebra whose generator is $S_1$. In this text, we assume this.

### 6
Given graded ring $S$, define graded ring $S^{(d)}$ by $n$-th grade of $S^{(d)}$ is $S_{nd}$ (we may consider $S=R[x_1,\cdots,x_n]$ a polynomial ring). We have an isomorphism $\Proj S=\Proj S^{(d)}$. It is given as follows.

*Proof.* Consider graded ring $S'$ defined as $nd$-th grade of $S'$ is $S_{nd}$ and otherwise $0$. With obvious reason, $\Proj S'=\Proj S^{(d)}$. We remain to prove $\Proj S'= \Proj S$. Consider inclusion $S'\rightarrow S$ preserving degree. Then we have a (well-defined) morphism $\Proj S\rightarrow \Proj S'$. Explicitly, this map sends $\fp\in \Proj S$ to $\fp\cap S'$. I claim it is bijective and left to readers.

(Injective) If $\fp,\fq\in \Proj S$, then $\fp\cap S'= \fq\cap S'$. Let $a\in \fp$, then $a^{d}\in \fp\cap S'= \fq\cap S'$ implies $a^d\in \fq$ and we get $a\in \fq$.

(Surjective) Let $\fp\in \Proj S'$. $\fp$ is obviously relevant prime ideal of $S$.

We leave details to reader. (for interactive purpose)

---
<span style="color: blue;">Check 3.</span>

Complete it is a homeomorphism (show the inverse is continuous) and ends the proof of it is an isomorphism as a scheme. (This ends the proof) $\square$

---

### 7

(Serre twisting sheaf) Among projective spaces, we are interested in $X=\bP^n_A$ (especially when $A$ is a field but we start from ring). Set $S:=A[x_0,\cdots,x_n]$. Remind that $\widetilde{S}$ is a quasi-coherent $O_X$-module sending $D_+(f)$ to $S_{(f)}$.

Remark that $S(d)$ is a graded ring whose $n$-th degree is $S_{n+d}$. 

Define quasi-coherent $O_X$-module $O_X(n):=\widetilde{S(n)}$. This is called **Serre's twisting sheaf**. In general, given quasi-coherent $O_X$-module $\cF$, $\cF(n):=\cF\otimes O_X(n)$. From definition, the global section is given as $\Gamma(X,O_X(n))=S_n$.

---
<span style="color: blue;">Check 4.</span>

Consider $A$-module homomorphism $S_n\rightarrow \Gamma(X,O_X(n))$, $a\in S_+$ is mapped to gluing of $a/1\in \Gamma(D_+(f),O_X)$ for $f\in S_1$. Show it is well defined and it is an isomorphism.

---

# Reference

I don't want to write references in formal way. To clarify, I added link.

\[1\]: R. Hartshonre, Algebraic Geometry ([link](https://link.springer.com/book/10.1007/978-1-4757-3849-0)).

\[2\]: Ulrich G??rtz, Torsten Wedhorn, Algebraic Geometry I: Schemes With Examples and Exercises ([link](https://link.springer.com/book/10.1007/978-3-658-30733-2)).