---
layout: page
title: Brezis 8.1
permalink: /exercises/analisis/brezis-8-1/
---

# Brezis 8.1

## Enunciado

Consider the function

$$
u(x)=(1+x^2)^{-\frac{\alpha}{2}}\left(\log(2+x^2)\right)^{-1},
\qquad x\in\mathbb{R},
$$

with $0<\alpha<1$. Check that

$$
u\in W^{1,p}(\mathbb{R})
\qquad
\forall p\in \left[\frac{1}{\alpha},+\infty\right],
$$

and that

$$
u\notin L^q(\mathbb{R})
\qquad
\forall q\in \left[1,\frac{1}{\alpha}\right).
$$

## Solución

We want to prove that

$$
u\in W^{1,p}(\mathbb{R})
\qquad
\forall p\in \left[\frac{1}{\alpha},+\infty\right].
$$

By definition, this means that

$$
u\in L^p(\mathbb{R})
\qquad
\text{and}
\qquad
u'\in L^p(\mathbb{R}).
$$

### 1. The case $p=\infty$

We have

$$
u(x)=\frac{1}{(1+x^2)^{\frac{\alpha}{2}}\log(2+x^2)}.
$$

Since

$$
(1+x^2)^{\frac{\alpha}{2}}\ge 1
$$

and

$$
\log(2+x^2)\ge \log 2,
$$

we get

$$
|u(x)|\le \frac{1}{\log 2}.
$$

Therefore,

$$
u\in L^\infty(\mathbb{R}).
$$

### 2. The case $\frac{1}{\alpha}\le p<+\infty$

Since $u$ is continuous, it is enough to study the behavior of $u$ at infinity.

For large $|x|$, we have

$$
1+x^2\sim x^2,
$$

and therefore

$$
(1+x^2)^{-\frac{\alpha}{2}}\sim |x|^{-\alpha}.
$$

Also,

$$
\log(2+x^2)\sim \log(x^2)=2\log |x|.
$$

Hence, for large $|x|$,

$$
|u(x)|^p\sim \frac{1}{|x|^{\alpha p}(\log |x|)^p}.
$$

Thus, it is enough to study

$$
\int_R^{+\infty}\frac{1}{x^{\alpha p}(\log x)^p},dx.
$$

If

$$
p>\frac{1}{\alpha},
$$

then

$$
\alpha p>1,
$$

so the integral converges.

Now suppose

$$
p=\frac{1}{\alpha}.
$$

Then

$$
\alpha p=1.
$$

Hence we study

$$
\int_R^{+\infty}\frac{1}{x(\log x)^p},dx.
$$

Using the change of variables

$$
v=\log x,
\qquad
dv=\frac{1}{x},dx,
$$

we obtain

$$
\int_{\log R}^{+\infty}\frac{1}{v^p},dv.
$$

Since $0<\alpha<1$, we have

$$
p=\frac{1}{\alpha}>1.
$$

Therefore, the integral converges. Hence,

$$
u\in L^p(\mathbb{R})
\qquad
\forall p\in \left[\frac{1}{\alpha},+\infty\right].
$$

### 3. Integrability of the derivative

Now we compute $u'$. Since

$$
u(x)=(1+x^2)^{-\frac{\alpha}{2}}\left(\log(2+x^2)\right)^{-1},
$$

we get

$$
u'(x)
=====

## -\alpha x(1+x^2)^{-\frac{\alpha}{2}-1}\left(\log(2+x^2)\right)^{-1}

(1+x^2)^{-\frac{\alpha}{2}}
\frac{2x}{(2+x^2)(\log(2+x^2))^2}.
$$

Factoring $u(x)$, we obtain

$$
u'(x)
=====

u(x)
\left(
\frac{-\alpha x}{1+x^2}
-----------------------

\frac{2x}{(2+x^2)\log(2+x^2)}
\right).
$$

Define

$$
h(x)
====

## \frac{-\alpha x}{1+x^2}

\frac{2x}{(2+x^2)\log(2+x^2)}.
$$

Then

$$
u'(x)=u(x)h(x).
$$

The function $h$ is continuous on $\mathbb{R}$. Moreover, as $|x|\to+\infty$,

$$
\frac{-\alpha x}{1+x^2}\to 0
$$

and

$$
\frac{2x}{(2+x^2)\log(2+x^2)}\to 0.
$$

Therefore, $h$ is bounded on $\mathbb{R}$, that is,

$$
h\in L^\infty(\mathbb{R}).
$$

Thus,

$$
|u'|_p
======

|uh|_p
\le
|u|*p|h|*\infty.
$$

Since $u\in L^p(\mathbb{R})$, we conclude that

$$
u'\in L^p(\mathbb{R}).
$$

Therefore,

$$
u\in W^{1,p}(\mathbb{R})
\qquad
\forall p\in \left[\frac{1}{\alpha},+\infty\right].
$$

---

## Non-integrability for $q<\frac{1}{\alpha}$

Now we prove that

$$
u\notin L^q(\mathbb{R})
\qquad
\forall q\in \left[1,\frac{1}{\alpha}\right).
$$

Let

$$
1\le q<\frac{1}{\alpha}.
$$

For large $x$,

$$
u(x)\sim \frac{1}{x^\alpha\log(x^2)}
====================================

\frac{1}{2x^\alpha\log x}.
$$

Hence,

$$
|u(x)|^q
\sim
\frac{1}{x^{\alpha q}(\log x)^q}.
$$

Let

$$
\beta=\alpha q.
$$

Since

$$
q<\frac{1}{\alpha},
$$

we have

$$
\beta=\alpha q<1.
$$

Choose $\gamma$ such that

$$
\beta<\gamma<1.
$$

Let

$$
\varepsilon=\gamma-\beta>0.
$$

For $x$ large enough,

$$
(\log x)^q\le x^\varepsilon.
$$

Thus,

$$
x^\beta(\log x)^q
\le
x^\beta x^\varepsilon
=====================

x^\gamma.
$$

Therefore,

$$
\frac{1}{x^\beta(\log x)^q}
\ge
\frac{1}{x^\gamma}.
$$

But

$$
\int_R^{+\infty}\frac{1}{x^\gamma},dx=+\infty
$$

because $\gamma<1$. Hence,

$$
\int_R^{+\infty}|u(x)|^q,dx=+\infty.
$$

Therefore,

$$
u\notin L^q(\mathbb{R})
\qquad
\forall q\in \left[1,\frac{1}{\alpha}\right).
$$

This proves the result.
