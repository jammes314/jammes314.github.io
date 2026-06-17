---
layout: page
title: "Brezis 9.17"
permalink: /exercises/analisis/brezis-9-17/
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

# Brezis 9.17

We write

$$
\Gamma=\partial\Omega.
$$

Recall that, for $1\le p<\infty$,

$$
W^{1,p}(\Omega)
=
\left\{
 u\in L^p(\Omega):
 \frac{\partial u}{\partial x_i}\in L^p(\Omega),\ i=1,\dots,N
\right\},
$$

with norm

$$
\|u\|_{W^{1,p}(\Omega)}
=
\|u\|_{L^p(\Omega)}+
\sum_{i=1}^{N}\left\|\frac{\partial u}{\partial x_i}\right\|_{L^p(\Omega)}.
$$

Also,

$$
W_0^{1,p}(\Omega)
=
\overline{C_c^1(\Omega)}^{\,W^{1,p}(\Omega)}.
$$

In other words, $u\in W_0^{1,p}(\Omega)$ means that $u$ can be approximated in the $W^{1,p}$-norm by smooth functions with compact support contained in $\Omega$.

## Statement

Assume that $\Omega$ is of class $C^1$. Let

$$
u\in W^{1,p}(\Omega)\cap C(\overline{\Omega}),
\qquad
1\le p<\infty.
$$

Then the following properties are equivalent:

$$
\text{(i)}\quad u=0 \text{ on } \Gamma,
$$

and

$$
\text{(ii)}\quad u\in W_0^{1,p}(\Omega).
$$

## Proof of $(i)\Rightarrow (ii)$

Assume that

$$
u=0\quad \text{on }\Gamma.
$$

We first prove the result under the extra assumption that $\operatorname{supp}(u)$ is bounded.

Choose $G\in C^1(\mathbb{R})$ such that

$$
|G(t)|\le |t|,
$$

and

$$
G(t)=0\quad \text{if } |t|\le 1,
\qquad
G(t)=t\quad \text{if } |t|\ge 2.
$$

For each $n\in\mathbb{N}$, define

$$
 u_n=\frac1n G(nu).
$$

By the chain rule for Sobolev functions, we have

$$
 u_n\in W^{1,p}(\Omega),
$$

and

$$
\nabla u_n
=
G'(nu)\nabla u.
$$

We claim that

$$
 u_n\to u
 \quad \text{in } W^{1,p}(\Omega).
$$

Indeed, first observe that, since $|G(t)|\le |t|$,

$$
 |u_n|
=
\frac1n |G(nu)|
\le |u|.
$$

Moreover, pointwise a.e. in $\Omega$,

$$
 u_n(x)\to u(x).
$$

To see this, fix $x\in\Omega$. If $u(x)=0$, then $u_n(x)=0$. If $u(x)\neq0$, then, for $n$ large enough,

$$
 |nu(x)|\ge 2,
$$

and therefore

$$
 G(nu(x))=nu(x),
$$

so

$$
 u_n(x)=u(x).
$$

Thus, by the dominated convergence theorem,

$$
 u_n\to u
 \quad \text{in } L^p(\Omega).
$$

Now let us study the gradients. Since

$$
\nabla u_n=G'(nu)\nabla u,
$$

we have

$$
\nabla u_n\to \nabla u
\quad \text{a.e. in }\Omega.
$$

Indeed, if $u(x)\neq0$, then $G'(nu(x))=1$ for $n$ large enough. If $u(x)=0$, then we use the standard Sobolev fact that

$$
\nabla u=0
\quad \text{a.e. on }\{u=0\}.
$$

Also,

$$
|\nabla u_n|
\le
\|G'\|_{L^\infty(\mathbb{R})}|\nabla u|.
$$

Since $\nabla u\in L^p(\Omega)$, another application of dominated convergence gives

$$
 \nabla u_n\to \nabla u
 \quad \text{in } L^p(\Omega).
$$

Hence

$$
 u_n\to u
 \quad \text{in } W^{1,p}(\Omega).
$$

We now prove that each $u_n$ belongs to $W_0^{1,p}(\Omega)$. Since $G(t)=0$ for $|t|\le1$, we have

$$
\operatorname{supp}(u_n)
\subset
\left\{x\in\Omega: |u(x)|\ge \frac1n\right\}.
$$

Because $u\in C(\overline{\Omega})$ and $u=0$ on $\Gamma$, the set

$$
\left\{x\in\overline{\Omega}: |u(x)|\ge \frac1n\right\}
$$

cannot touch the boundary $\Gamma$. Since $\operatorname{supp}(u)$ is bounded, this set is a compact subset of $\Omega$.

Therefore

$$
\operatorname{supp}(u_n)\Subset \Omega.
$$

By Lemma 9.5, if a function in $W^{1,p}(\Omega)$ has compact support contained in $\Omega$, then it belongs to $W_0^{1,p}(\Omega)$. Hence

$$
 u_n\in W_0^{1,p}(\Omega)
 \quad \text{for every }n.
$$

Since $W_0^{1,p}(\Omega)$ is closed in $W^{1,p}(\Omega)$ and $u_n\to u$ in $W^{1,p}(\Omega)$, we conclude that

$$
 u\in W_0^{1,p}(\Omega).
$$

### Removing the bounded support assumption

Now suppose that $\operatorname{supp}(u)$ is not necessarily bounded.

Take $\zeta\in C_c^\infty(\mathbb{R}^N)$ such that

$$
0\le \zeta\le1,
$$

$$
\zeta(x)=1
\quad \text{if } |x|\le1,
$$

and

$$
\zeta(x)=0
\quad \text{if } |x|\ge2.
$$

For each $k\in\mathbb{N}$, define

$$
\zeta_k(x)=\zeta\left(\frac{x}{k}\right).
$$

Then

$$
\zeta_k\in C_c^\infty(\mathbb{R}^N),
$$

$$
0\le \zeta_k\le1,
$$

$$
\zeta_k(x)=1
\quad \text{if } |x|\le k,
$$

and

$$
\zeta_k(x)=0
\quad \text{if } |x|\ge 2k.
$$

Moreover, for some constant $C>0$ independent of $k$,

$$
|\nabla\zeta_k(x)|
\le
\frac{C}{k}.
$$

Set

$$
 v_k=\zeta_k u.
$$

Then $v_k\in W^{1,p}(\Omega)$, $v_k\in C(\overline{\Omega})$, $v_k=0$ on $\Gamma$, and $v_k$ has bounded support. By the previous part,

$$
 v_k\in W_0^{1,p}(\Omega)
 \quad \text{for every }k.
$$

We prove that

$$
 v_k\to u
 \quad \text{in }W^{1,p}(\Omega).
$$

First,

$$
 v_k(x)=\zeta_k(x)u(x)\to u(x)
 \quad \text{a.e. in }\Omega,
$$

and

$$
 |v_k-u|
=|\zeta_k-1|\,|u|
\le |u|.
$$

Thus, by dominated convergence,

$$
 v_k\to u
 \quad \text{in }L^p(\Omega).
$$

For the gradients,

$$
\nabla v_k
=
\zeta_k\nabla u+u\nabla\zeta_k.
$$

Therefore

$$
\|\nabla v_k-\nabla u\|_{L^p(\Omega)}
\le
\|(\zeta_k-1)\nabla u\|_{L^p(\Omega)}
+
\|u\nabla\zeta_k\|_{L^p(\Omega)}.
$$

The first term goes to zero by dominated convergence, while the second satisfies

$$
\|u\nabla\zeta_k\|_{L^p(\Omega)}
\le
\frac{C}{k}\|u\|_{L^p(\Omega)}
\to0.
$$

Hence

$$
 v_k\to u
 \quad \text{in }W^{1,p}(\Omega).
$$

Since $W_0^{1,p}(\Omega)$ is closed in $W^{1,p}(\Omega)$, we obtain

$$
 u\in W_0^{1,p}(\Omega).
$$

This proves

$$
 u=0\text{ on }\Gamma
 \quad\Longrightarrow\quad
 u\in W_0^{1,p}(\Omega).
$$

## Proof of $(ii)\Rightarrow(i)$

Assume now that

$$
 u\in W_0^{1,p}(\Omega)\cap C(\overline{\Omega}).
$$

We prove that $u=0$ on $\Gamma$.

The argument is local. Since $\Omega$ is of class $C^1$, near every point of the boundary one can flatten $\Gamma$ using a $C^1$ chart. Thus it is enough to prove the result on the model half-cube.

Write

$$
x=(x',x_N),
\qquad
x'=(x_1,\dots,x_{N-1}),
$$

and

$$
|x'|=\left(\sum_{i=1}^{N-1}x_i^2\right)^{1/2}.
$$

Define

$$
\mathbb{R}_+^N=\{x\in\mathbb{R}^N:x_N>0\},
$$

$$
Q=\{x\in\mathbb{R}^N: |x'|<1,\ |x_N|<1\},
$$

$$
Q_+=Q\cap\mathbb{R}_+^N,
$$

and

$$
Q_0=\{(x',0): |x'|<1\}.
$$

We prove the following local fact:

$$
 u\in W_0^{1,p}(Q_+)\cap C(\overline{Q_+})
 \quad\Longrightarrow\quad
 u=0\text{ on }Q_0.
$$

Since $u\in W_0^{1,p}(Q_+)$, there exists a sequence

$$
(u_n)_{n\in\mathbb{N}}
\subset C_c^1(Q_+)
$$

such that

$$
 u_n\to u
 \quad \text{in }W^{1,p}(Q_+).
$$

For $x=(x',x_N)\in Q_+$, since $u_n$ has compact support in $Q_+$, we have

$$
 u_n(x',0)=0.
$$

Thus, by the fundamental theorem of calculus,

$$
 u_n(x',x_N)
=
\int_0^{x_N}
\frac{\partial u_n}{\partial x_N}(x',t)\,dt.
$$

Therefore

$$
 |u_n(x',x_N)|
\le
\int_0^{x_N}
\left|
\frac{\partial u_n}{\partial x_N}(x',t)
\right|dt.
$$

Fix $0<\varepsilon<1$. Integrating over the strip

$$
\{(x',x_N): |x'|<1,
\ 0<x_N<\varepsilon\},
$$

we obtain

$$
\frac1\varepsilon
\int_{|x'|<1}\int_0^\varepsilon
|u_n(x',x_N)|\,dx_N\,dx'
\le
\int_{|x'|<1}\int_0^\varepsilon
\left|
\frac{\partial u_n}{\partial x_N}(x',t)
\right|dt\,dx'.
$$

Passing to the limit as $n\to\infty$, using the convergence in $W^{1,p}(Q_+)$, gives

$$
\frac1\varepsilon
\int_{|x'|<1}\int_0^\varepsilon
|u(x',x_N)|\,dx_N\,dx'
\le
\int_{|x'|<1}\int_0^\varepsilon
\left|
\frac{\partial u}{\partial x_N}(x',t)
\right|dt\,dx'.
$$

Now let $\varepsilon\to0^+$. The right-hand side converges to $0$ because $\partial u/\partial x_N\in L^p(Q_+)$, hence it is locally integrable.

On the other hand, since $u\in C(\overline{Q_+})$,

$$
\frac1\varepsilon
\int_0^\varepsilon
|u(x',x_N)|\,dx_N
\to
|u(x',0)|.
$$

Hence

$$
\int_{|x'|<1}|u(x',0)|\,dx'=0.
$$

Since $u$ is continuous on $\overline{Q_+}$, it follows that

$$
 u(x',0)=0
 \quad \text{for every } |x'|<1.
$$

Therefore

$$
 u=0
 \quad \text{on }Q_0.
$$

Returning to a general $C^1$ domain $\Omega$, for every boundary point $x_0\in\Gamma$ there is a neighborhood $U$ and a $C^1$ diffeomorphism

$$
H:Q\to U
$$

such that

$$
H(Q_+)=U\cap\Omega,
$$

and

$$
H(Q_0)=U\cap\Gamma.
$$

The local half-cube result therefore gives

$$
 u=0
 \quad \text{on }U\cap\Gamma.
$$

Since $x_0\in\Gamma$ was arbitrary, we conclude that

$$
 u=0
 \quad \text{on }\Gamma.
$$

Thus

$$
 u\in W_0^{1,p}(\Omega)
 \quad\Longrightarrow\quad
 u=0\text{ on }\Gamma.
$$

Combining the two implications, we obtain

$$
 u=0\text{ on }\Gamma
 \quad\Longleftrightarrow\quad
 u\in W_0^{1,p}(\Omega).
$$

This proves Theorem 9.17.
