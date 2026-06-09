---
layout: page
title: "Brezis 8.1"
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

<script defer src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-chtml.js"></script>

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

$$
\text{We prove first that }
u\in W^{1,p}(\mathbb{R})
\quad
\forall p\in\left[\frac{1}{\alpha},+\infty\right].
$$

$$
u\in W^{1,p}(\mathbb{R})
\iff
u\in L^p(\mathbb{R})
\quad\text{and}\quad
u'\in L^p(\mathbb{R}).
$$

1. The case (p=\infty)

$$
u(x)=
\frac{1}{(1+x^2)^{\frac{\alpha}{2}}\log(2+x^2)}.
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

\frac{1}{(1+x^2)^{\frac{\alpha}{2}}\log(2+x^2)}
\le
\frac{1}{\log 2}.
$$

Therefore,

$$
u\in L^\infty(\mathbb{R}).
$$

2. The case (\frac{1}{\alpha}\le p<+\infty)

Since (u) is continuous, it is enough to study its behavior as (|x|\to+\infty).

For large (|x|),

$$
1+x^2\sim x^2,
\qquad
(1+x^2)^{-\frac{\alpha}{2}}\sim |x|^{-\alpha},
$$

and

$$
\log(2+x^2)\sim \log(x^2)=2\log |x|.
$$

Hence,

$$
|u(x)|^p
\sim
\frac{1}{|x|^{\alpha p}(\log |x|)^p}.
$$

Thus, we study

$$
\int_R^{+\infty}
\frac{1}{x^{\alpha p}(\log x)^p},dx.
$$

If

$$
p>\frac{1}{\alpha},
$$

then

$$
\alpha p>1,
$$

and therefore

$$
\int_R^{+\infty}
\frac{1}{x^{\alpha p}(\log x)^p},dx
\le
\int_R^{+\infty}
\frac{1}{x^{\alpha p}},dx
<+\infty.
$$

Now suppose

$$
p=\frac{1}{\alpha}.
$$

Then

$$
\alpha p=1,
$$

and we need to study

$$
\int_R^{+\infty}
\frac{1}{x(\log x)^p},dx.
$$

Using the change of variables

$$
v=\log x,
\qquad
dv=\frac{1}{x},dx,
$$

we obtain

\int_{\log R}^{+\infty}
\frac{1}{v^p},dv.
$$

Since

$$
0<\alpha<1,
\qquad
p=\frac{1}{\alpha}>1,
$$

we have

$$
\int_{\log R}^{+\infty}
\frac{1}{v^p},dv
<+\infty.
$$

Therefore,

$$
u\in L^p(\mathbb{R})
\quad
\forall p\in\left[\frac{1}{\alpha},+\infty\right].
$$

3. Integrability of the derivative

We compute

(1+x^2)^{-\frac{\alpha}{2}}
\left(\log(2+x^2)\right)^{-1}.
$$

Then

(1+x^2)^{-\frac{\alpha}{2}}
\frac{2x}{(2+x^2)(\log(2+x^2))^2}.
\end{aligned}
$$

Factoring (u(x)), we get

\frac{2x}{(2+x^2)\log(2+x^2)}
\right).
$$

Define

\frac{-\alpha x}{1+x^2}

\frac{2x}{(2+x^2)\log(2+x^2)}.
$$

Then

$$
u'(x)=u(x)h(x).
$$

Moreover,

$$
\frac{-\alpha x}{1+x^2}\to 0
\quad
\text{as }
|x|\to+\infty,
$$

and

$$
\frac{2x}{(2+x^2)\log(2+x^2)}\to 0
\quad
\text{as }
|x|\to+\infty.
$$

Hence (h) is continuous and bounded on (\mathbb{R}). Therefore,

$$
h\in L^\infty(\mathbb{R}).
$$

Thus,

|uh|_p
\le
|u|p|h|\infty
<+\infty.
$$

Therefore,

$$
u'\in L^p(\mathbb{R}).
$$

Consequently,

$$
u\in W^{1,p}(\mathbb{R})
\quad
\forall p\in\left[\frac{1}{\alpha},+\infty\right].
$$

4. Non-integrability for (q<\frac{1}{\alpha})

Let

$$
1\le q<\frac{1}{\alpha}.
$$

For large (x),

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

Choose (\gamma) such that

$$
\beta<\gamma<1.
$$

Let

$$
\varepsilon=\gamma-\beta>0.
$$

For (x) large enough,

$$
(\log x)^q\le x^\varepsilon.
$$

Therefore,

x^\gamma.
$$

Thus,

$$
\frac{1}{x^\beta(\log x)^q}
\ge
\frac{1}{x^\gamma}.
$$

But

+\infty,
\qquad
\gamma<1.
$$

Therefore,

+\infty.
$$

Hence,

$$
u\notin L^q(\mathbb{R})
\quad
\forall q\in\left[1,\frac{1}{\alpha}\right).
$$

This proves the result.

