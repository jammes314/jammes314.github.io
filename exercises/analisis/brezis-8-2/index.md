---
layout: page
title: "Brezis 8.2"
permalink: /exercises/analisis/brezis-8-2/
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

# Brezis 8.2

Let $I=(0,1)$.

## Statement

1. Assume that $(u_n)$ is a bounded sequence in $W^{1,p}(I)$ with
$1<p\leq \infty$. Show that there exist a subsequence $(u_{n_k})$ and
some $u\in W^{1,p}(I)$ such that

$$
\|u_{n_k}-u\|_{L^\infty(I)}\to 0.
$$

Moreover,

$$
u_{n_k}'\rightharpoonup u'
\quad\text{weakly in }L^p(I)
\quad\text{if }1<p<\infty,
$$

and

$$
u_{n_k}'\stackrel{*}{\rightharpoonup}u'
\quad\text{in }\sigma(L^\infty,L^1)
\quad\text{if }p=\infty.
$$

2. Construct a bounded sequence $(u_n)$ in $W^{1,1}(I)$ that admits no
subsequence converging in $L^\infty(I)$.

## Solution

### Part 1

Assume first that $1<p\leq \infty$ and that $(u_n)$ is bounded in
$W^{1,p}(I)$. Since, in one dimension,

$$
W^{1,p}(I)\hookrightarrow C(\overline I)
$$

compactly for $1<p\leq \infty$, there exist a subsequence, still denoted
by $(u_{n_k})$, and a function $u\in C(\overline I)$ such that

$$
\|u_{n_k}-u\|_{L^\infty(I)}\to 0.
$$

Suppose first that $1<p<\infty$. Since $(u_n')$ is bounded in $L^p(I)$
and $L^p(I)$ is reflexive, there exist a further subsequence, not
relabeled, and some $g\in L^p(I)$ such that

$$
u_{n_k}'\rightharpoonup g
\quad\text{weakly in }L^p(I).
$$

For every $\varphi\in C_c^1(I)$, we have

$$
\int_I u_{n_k}\varphi'
=
-\int_I u_{n_k}'\varphi.
$$

Passing to the limit, we obtain

$$
\int_I u\varphi'
=
-\int_I g\varphi,
\qquad
\forall \varphi\in C_c^1(I).
$$

Therefore $u$ has weak derivative $g$. Hence

$$
u\in W^{1,p}(I)
\quad\text{and}\quad
u'=g.
$$

Consequently,

$$
u_{n_k}'\rightharpoonup u'
\quad\text{weakly in }L^p(I).
$$

Now suppose that $p=\infty$. Since $(u_n')$ is bounded in $L^\infty(I)$,
by Banach--Alaoglu there exist a further subsequence, not relabeled, and
some $g\in L^\infty(I)$ such that

$$
u_{n_k}'\stackrel{*}{\rightharpoonup}g
\quad\text{in }\sigma(L^\infty,L^1).
$$

Again, for every $\varphi\in C_c^1(I)$,

$$
\int_I u_{n_k}\varphi'
=
-\int_I u_{n_k}'\varphi.
$$

Passing to the limit gives

$$
\int_I u\varphi'
=
-\int_I g\varphi,
\qquad
\forall \varphi\in C_c^1(I).
$$

Thus $u'=g$ in the weak sense. Since $g\in L^\infty(I)$, we obtain

$$
u\in W^{1,\infty}(I),
$$

and therefore

$$
u_{n_k}'\stackrel{*}{\rightharpoonup}u'
\quad\text{in }\sigma(L^\infty,L^1).
$$

This proves the first part.

### Part 2

For $n\geq 2$, define

$$
u_n(x)=
\begin{cases}
0,
& 0<x\leq \dfrac12,\\[6pt]
n\left(x-\dfrac12\right),
& \dfrac12<x<\dfrac12+\dfrac1n,\\[6pt]
1,
& \dfrac12+\dfrac1n\leq x<1.
\end{cases}
$$

Then $u_n\in W^{1,1}(I)$ and

$$
u_n'(x)=
\begin{cases}
n,
& \dfrac12<x<\dfrac12+\dfrac1n,\\[6pt]
0,
& \text{otherwise},
\end{cases}
$$

for almost every $x\in I$. Hence

$$
\|u_n\|_{L^1(I)}\leq 1
$$

and

$$
\|u_n'\|_{L^1(I)}
=
\int_{1/2}^{1/2+1/n} n\,dx
=
1.
$$

Therefore

$$
\|u_n\|_{W^{1,1}(I)}
=
\|u_n\|_{L^1(I)}+
\|u_n'\|_{L^1(I)}
\leq 2,
$$

so $(u_n)$ is bounded in $W^{1,1}(I)$.

We claim that $(u_n)$ has no subsequence converging in $L^\infty(I)$. Let
$(u_{n_k})$ be any subsequence. Since $n_k\to\infty$, for every fixed $k$
we can choose $j>k$ such that

$$
n_j>2n_k.
$$

Consider the interval

$$
E_{j,k}
=
\left(\frac12+\frac1{n_j},\frac12+\frac1{2n_k}\right).
$$

This interval has positive measure. If $x\in E_{j,k}$, then

$$
u_{n_j}(x)=1
$$

and

$$
0\leq u_{n_k}(x)
=
n_k\left(x-\frac12\right)
\leq
\frac12.
$$

Hence

$$
|u_{n_j}(x)-u_{n_k}(x)|\geq \frac12
\qquad\text{for every }x\in E_{j,k}.
$$

Therefore

$$
\|u_{n_j}-u_{n_k}\|_{L^\infty(I)}\geq \frac12.
$$

So no subsequence of $(u_n)$ can be Cauchy in $L^\infty(I)$. In
particular, no subsequence can converge in $L^\infty(I)$.
