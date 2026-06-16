---

layout: default
title: "Brezis Lemma 9.6"
permalink: /exercises/analisis/brezis-9-6/
------------------------------------------

# Brezis Lemma 9.6

In this exercise we prove an estimate for difference quotients in the half-space.

Let

$$
\Omega=\mathbb{R}^{N}_{+}
=========================

\left{
x=(x',x_N)\in\mathbb{R}^{N}: x_N>0
\right}.
$$

The boundary of $\Omega$ is

$$
\Gamma=\partial\Omega
=====================

\left{
x=(x',x_N)\in\mathbb{R}^{N}: x_N=0
\right}.
$$

We say that $h$ is parallel to $\Gamma$, and we write $h\parallel \Gamma$, if

$$
h=(h',0)\in\mathbb{R}^{N-1}\times{0}.
$$

For $h\neq 0$, define the difference quotient

$$
D_hu(x)
=======

# \frac{\tau_hu(x)-u(x)}{|h|}

\frac{u(x+h)-u(x)}{|h|}.
$$

The goal is to prove that

$$
|D_hu|*{L^2(\Omega)}
\leq
|\nabla u|*{L^2(\Omega)}
$$

for every $u\in H^1(\Omega)$ and every $h\parallel\Gamma$.

## Statement

Let

$$
\Omega=\mathbb{R}^{N}_{+}.
$$

If

$$
h\parallel \Gamma,
\qquad
h\neq 0,
\qquad
u\in H^1(\Omega),
$$

then

$$
|D_hu|*{L^2(\Omega)}
\leq
|\nabla u|*{L^2(\Omega)}.
$$

## Proof

We first prove the result for smooth functions.

Assume that

$$
u\in C_c^1(\mathbb{R}^N).
$$

Fix

$$
x\in\Omega.
$$

Since

$$
h\parallel\Gamma,
$$

the vector $h$ has no component in the $x_N$-direction. Therefore,

$$
x+th\in\Omega
\qquad
\text{for every }t\in[0,1].
$$

Now define

$$
g(t)=u(x+th),
\qquad
t\in[0,1].
$$

By the chain rule,

$$
g'(t)=h\cdot\nabla u(x+th).
$$

Using the fundamental theorem of calculus, we obtain

$$
u(x+h)-u(x)
===========

# g(1)-g(0)

\int_0^1 h\cdot\nabla u(x+th),dt.
$$

Dividing by $|h|$, we get

$$
D_hu(x)
=======

# \frac{u(x+h)-u(x)}{|h|}

\int_0^1
\frac{h}{|h|}\cdot\nabla u(x+th),dt.
$$

Hence,

$$
|D_hu(x)|
\leq
\int_0^1 |\nabla u(x+th)|,dt.
$$

Squaring both sides gives

$$
|D_hu(x)|^2
\leq
\left(
\int_0^1 |\nabla u(x+th)|,dt
\right)^2.
$$

By Cauchy's inequality on $[0,1]$,

$$
\left(
\int_0^1 |\nabla u(x+th)|,dt
\right)^2
\leq
\int_0^1 |\nabla u(x+th)|^2,dt.
$$

Therefore,

$$
|D_hu(x)|^2
\leq
\int_0^1 |\nabla u(x+th)|^2,dt.
$$

Integrating over $\Omega$, we obtain

$$
\int_{\Omega}|D_hu(x)|^2,dx
\leq
\int_{\Omega}
\int_0^1 |\nabla u(x+th)|^2,dt,dx.
$$

By Fubini's theorem,

$$
\int_{\Omega}|D_hu(x)|^2,dx
\leq
\int_0^1
\int_{\Omega} |\nabla u(x+th)|^2,dx,dt.
$$

For fixed $t\in[0,1]$, make the change of variables

$$
y=x+th.
$$

Since $h\parallel\Gamma$, translation by $th$ maps $\Omega$ onto itself. Hence,

$$
\int_{\Omega} |\nabla u(x+th)|^2,dx
===================================

\int_{\Omega} |\nabla u(y)|^2,dy.
$$

Thus,

$$
\int_{\Omega}|D_hu(x)|^2,dx
\leq
\int_0^1
\int_{\Omega} |\nabla u(y)|^2,dy,dt.
$$

Since the inner integral does not depend on $t$, we have

$$
\int_{\Omega}|D_hu(x)|^2,dx
\leq
\int_{\Omega}|\nabla u(y)|^2,dy.
$$

Therefore,

$$
|D_hu|*{L^2(\Omega)}^2
\leq
|\nabla u|*{L^2(\Omega)}^2.
$$

Taking square roots, we obtain

$$
|D_hu|*{L^2(\Omega)}
\leq
|\nabla u|*{L^2(\Omega)}.
$$

This proves the estimate for smooth functions.

Now let

$$
u\in H^1(\Omega).
$$

Choose a sequence

$$
u_n\in C_c^1(\mathbb{R}^N)
$$

such that

$$
u_n\to u
\qquad
\text{in }H^1(\Omega).
$$

From the smooth case, we know that

$$
|D_hu_n|*{L^2(\Omega)}
\leq
|\nabla u_n|*{L^2(\Omega)}
\qquad
\text{for every }n.
$$

We now pass to the limit.

Since

$$
D_hu_n-D_hu
===========

D_h(u_n-u),
$$

we have

$$
|D_hu_n-D_hu|_{L^2(\Omega)}
===========================

|D_h(u_n-u)|_{L^2(\Omega)}.
$$

Using the definition of $D_h$,

$$
|D_h(u_n-u)|_{L^2(\Omega)}
==========================

\frac{1}{|h|}
|\tau_h(u_n-u)-(u_n-u)|_{L^2(\Omega)}.
$$

By the triangle inequality,

$$
|D_h(u_n-u)|*{L^2(\Omega)}
\leq
\frac{1}{|h|}
\left(
|\tau_h(u_n-u)|*{L^2(\Omega)}
+
|u_n-u|_{L^2(\Omega)}
\right).
$$

Since translation by $h$ in a tangential direction preserves the $L^2$-norm on $\Omega$,

$$
|\tau_h(u_n-u)|_{L^2(\Omega)}
=============================

|u_n-u|_{L^2(\Omega)}.
$$

Therefore,

$$
|D_hu_n-D_hu|*{L^2(\Omega)}
\leq
\frac{2}{|h|}
|u_n-u|*{L^2(\Omega)}.
$$

Since

$$
u_n\to u
\qquad
\text{in }H^1(\Omega),
$$

we also have

$$
u_n\to u
\qquad
\text{in }L^2(\Omega).
$$

Hence,

$$
D_hu_n\to D_hu
\qquad
\text{in }L^2(\Omega).
$$

Also,

$$
\nabla u_n\to\nabla u
\qquad
\text{in }L^2(\Omega).
$$

Passing to the limit in

$$
|D_hu_n|*{L^2(\Omega)}
\leq
|\nabla u_n|*{L^2(\Omega)},
$$

we obtain

$$
|D_hu|*{L^2(\Omega)}
\leq
|\nabla u|*{L^2(\Omega)}.
$$

Therefore,

$$
\boxed{
|D_hu|*{L^2(\Omega)}
\leq
|\nabla u|*{L^2(\Omega)}
}
$$

for every $u\in H^1(\Omega)$ and every $h\parallel\Gamma$.

This completes the proof.

## Key idea

The condition

$$
h\parallel\Gamma
$$

means that $h$ is tangential to the boundary of the half-space. Therefore, if

$$
x\in\Omega,
$$

then the whole segment

$$
x+th,
\qquad
t\in[0,1],
$$

remains inside $\Omega$.

This is the reason why we can apply the fundamental theorem of calculus along the segment $x+th$ without leaving the domain.

The estimate

$$
|D_hu|*{L^2(\Omega)}
\leq
|\nabla u|*{L^2(\Omega)}
$$

says that the tangential difference quotient of $u$ is controlled by the weak gradient of $u$.
