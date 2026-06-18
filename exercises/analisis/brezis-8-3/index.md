---
layout: page
title: "Brezis 8.3"
permalink: /exercises/analisis/brezis-8-3/
---

<script>
window.MathJax = {
  tex: {
    inlineMath: [['$', '$'], ['\\(', '\\)']],
    displayMath: [['$$', '$$'], ['\\[', '\\]']],
    processEscapes: true
  }
};
</script>

<script defer src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>

# Brezis 8.3

## Helly's selection theorem

Let $(u_n)$ be a bounded sequence in $W^{1,1}(I)$, where
$I=(0,1)$. The goal is to show that there exists a subsequence
$(u_{n_k})$ such that $(u_{n_k}(x))$ converges for every $x\in(0,1)$.

## Statement

1. Show that we may always assume, in addition, that $u_n$ is
nondecreasing on $[0,1]$.

2. Prove that there exist a subsequence $(u_{n_k})$ and a measurable set
$E\subset [0,1]$ with $|E|=0$ such that $u_{n_k}(x)$ converges to a limit,
denoted by $u(x)$, for every $x\in [0,1]\setminus E$.

3. Show that $u$ is nondecreasing on $[0,1]\setminus E$ and deduce that
there exist a countable set $D\subset(0,1)$ and a nondecreasing function
$\overline u:(0,1)\to\mathbb R$ such that $\overline u$ is continuous at
every $x\in(0,1)\setminus D$ and

$$
\overline u(x)=u(x)
\qquad
\text{for every }x\in(0,1)\setminus E.
$$

4.  Prove that

$$
u_{n_k}(x)\to \overline u(x)
\qquad
\text{for every }x\in(0,1)\setminus D.
$$

5. Conclude that one can extract a subsequence of $(u_n)$ that converges
for every $x\in(0,1)$.

## Solution

We work with the absolutely continuous representatives of the functions in
$W^{1,1}(I)$.

### Part 1

Assume first that the theorem is already known for bounded nondecreasing
sequences in $W^{1,1}(I)$. We show that this is enough to prove the general
case.

Let $(u_n)$ be bounded in $W^{1,1}(I)$. Define

$$
v_n(x)=\int_0^x |u_n'(t)|\,dt.
$$

Then $v_n\in W^{1,1}(I)$ and

$$
v_n'(x)=|u_n'(x)|\geq 0
\qquad\text{for a.e. }x\in I.
$$

Hence $(v_n)$ is nondecreasing. Moreover,

$$
\|v_n'\|_{L^1(I)}=\|u_n'\|_{L^1(I)}
$$

and

$$
\|v_n\|_{L^1(I)}\leq \|v_n\|_{L^\infty(I)}
\leq \|u_n'\|_{L^1(I)}.
$$

Thus $(v_n)$ is bounded in $W^{1,1}(I)$.

Now define

$$
w_n=v_n-u_n.
$$

Then $w_n\in W^{1,1}(I)$ and

$$
w_n'=v_n'-u_n'=|u_n'|-u_n'\geq 0
\qquad\text{a.e. in }I.
$$

Therefore $(w_n)$ is also nondecreasing. Also, since both $(v_n)$ and
$(u_n)$ are bounded in $W^{1,1}(I)$, the sequence $(w_n)$ is bounded in
$W^{1,1}(I)$.

By the theorem for nondecreasing sequences, there exists a subsequence
$(v_{n_k})$ converging pointwise in $(0,1)$. Applying the same result to
$(w_{n_k})$, we can extract a further subsequence, not relabeled, such
that $(w_{n_k})$ also converges pointwise in $(0,1)$.

Since

$$
u_{n_k}=v_{n_k}-w_{n_k},
$$

the sequence $(u_{n_k})$ converges pointwise in $(0,1)$. Therefore it is
enough to prove the result under the additional assumption that each $u_n$
is nondecreasing.

From now on, assume that $(u_n)$ is bounded in $W^{1,1}(I)$ and that each
$u_n$ is nondecreasing.

### Part 2

Since $(u_n)$ is bounded in $W^{1,1}(I)$, and since the embedding

$$
W^{1,1}(I)\hookrightarrow L^1(I)
$$

is compact, there exist a subsequence $(u_{n_k})$ and a function
$u\in L^1(I)$ such that

$$
u_{n_k}\to u
\qquad\text{strongly in }L^1(I).
$$

From strong convergence in $L^1(I)$, we can extract a further subsequence,
still denoted by $(u_{n_k})$, such that

$$
u_{n_k}(x)\to u(x)
$$

for almost every $x\in I$. Therefore there exists a measurable set
$E\subset [0,1]$ with $|E|=0$ such that

$$
u_{n_k}(x)\to u(x)
\qquad
\text{for every }x\in [0,1]\setminus E.
$$

### Part 3

Let $x,y\in [0,1]\setminus E$ with $x<y$. Since each $u_{n_k}$ is
nondecreasing, we have

$$
u_{n_k}(x)\leq u_{n_k}(y)
\qquad\text{for every }k.
$$

Passing to the limit gives

$$
u(x)\leq u(y).
$$

Hence $u$ is nondecreasing on $[0,1]\setminus E$.

Since $E$ has measure zero, the set $[0,1]\setminus E$ is dense in
$[0,1]$. Define $\overline u:(0,1)\to\mathbb R$ by

$$
\overline u(x)
=
\sup\{u(t):t\leq x,\ t\in [0,1]\setminus E\}.
$$

This supremum is finite because $(u_n)$ is bounded in $W^{1,1}(I)$, and
therefore the functions $u_n$ are uniformly bounded in $L^\infty(I)$.
Consequently, the limit function $u$ is bounded on $[0,1]\setminus E$.

We claim that $\overline u$ is nondecreasing. Indeed, if $x<y$, then

$$
\{t\in [0,1]\setminus E:t\leq x\}
\subset
\{t\in [0,1]\setminus E:t\leq y\},
$$

and therefore

$$
\overline u(x)\leq \overline u(y).
$$

Also, if $x\in [0,1]\setminus E$, then, since $u$ is nondecreasing on
$[0,1]\setminus E$,

$$
\overline u(x)=u(x).
$$

We now use the standard fact that every monotone function has at most
countably many discontinuities. Hence there exists a countable set
$D\subset(0,1)$ such that $\overline u$ is continuous at every
$x\in(0,1)\setminus D$.

Thus we have constructed a nondecreasing function
$\overline u:(0,1)\to\mathbb R$, continuous outside a countable set, and
such that

$$
\overline u(x)=u(x)
\qquad
\text{for every }x\in(0,1)\setminus E.
$$

### Part 4

Let $x\in(0,1)\setminus D$. We prove that

$$
u_{n_k}(x)\to \overline u(x).
$$

Let $\varepsilon>0$. Since $\overline u$ is continuous at $x$, there
exists $\delta>0$ such that, if $|t-x|<\delta$, then

$$
|\overline u(t)-\overline u(x)|<\varepsilon.
$$

Choose

$$
t^-<x<t^+
$$

with

$$
t^-,t^+\in [0,1]\setminus E
$$

and

$$
t^-,t^+\in (x-\delta,x+\delta).
$$

This is possible because $[0,1]\setminus E$ is dense in $[0,1]$.

Since each $u_{n_k}$ is nondecreasing, we have

$$
u_{n_k}(t^-)
\leq
u_{n_k}(x)
\leq
u_{n_k}(t^+)
\qquad\text{for every }k.
$$

Passing to the limit inferior and superior gives

$$
u(t^-)
\leq
\liminf_{k\to\infty}u_{n_k}(x)
\leq
\limsup_{k\to\infty}u_{n_k}(x)
\leq
u(t^+).
$$

Since $t^-,t^+\notin E$, we know that

$$
u(t^-)=\overline u(t^-),
\qquad
u(t^+)=\overline u(t^+).
$$

Therefore,

$$
\overline u(t^-)
\leq
\liminf_{k\to\infty}u_{n_k}(x)
\leq
\limsup_{k\to\infty}u_{n_k}(x)
\leq
\overline u(t^+).
$$

By the choice of $t^-$ and $t^+$,

$$
\overline u(x)-\varepsilon
<
\overline u(t^-)
\leq
\overline u(t^+)
<
\overline u(x)+\varepsilon.
$$

Hence

$$
\overline u(x)-\varepsilon
\leq
\liminf_{k\to\infty}u_{n_k}(x)
\leq
\limsup_{k\to\infty}u_{n_k}(x)
\leq
\overline u(x)+\varepsilon.
$$

Since $\varepsilon>0$ was arbitrary, we conclude that

$$
\lim_{k\to\infty}u_{n_k}(x)=\overline u(x).
$$

Thus

$$
u_{n_k}(x)\to \overline u(x)
\qquad
\text{for every }x\in(0,1)\setminus D.
$$

### Part 5

It remains to obtain convergence at the points of $D$. Since $D$ is
countable, write

$$
D=\{d_1,d_2,d_3,\dots\}.
$$

The sequence $(u_{n_k})$ is bounded in $W^{1,1}(I)$, hence it is bounded
in $L^\infty(I)$. Therefore, for each fixed $d_j\in D$, the numerical
sequence

$$
(u_{n_k}(d_j))_{k\in\mathbb N}
$$

is bounded in $\mathbb R$.

We now apply a diagonal argument. First choose a subsequence that converges
at $d_1$. From that subsequence choose a further subsequence that converges
at $d_2$. Continuing in this way, and then taking the diagonal subsequence,
we obtain a subsequence, still denoted by $(u_{n_k})$, such that

$$
u_{n_k}(d_j)
$$

converges for every $j\in\mathbb N$.

This subsequence still converges at every point of $(0,1)\setminus D$, by
Part 4. Therefore it converges at every point of $(0,1)$.

This proves Helly's selection theorem.
