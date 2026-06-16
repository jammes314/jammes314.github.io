
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
u(x)=(1+x^2)^{-\frac{\alpha}{2}}\big(\log(2+x^2)\big)^{-1},
\qquad x\in\mathbb{R},
$$

where

$$
0<\alpha<1.
$$

Prove that

$$
u\in W^{1,p}(\mathbb{R})
\qquad
\text{for every }p\in\left[\frac{1}{\alpha},+\infty\right],
$$

and that

$$
u\notin L^q(\mathbb{R})
\qquad
\text{for every }q\in\left[1,\frac{1}{\alpha}\right).
$$

## Solución

We prove first that

$$
u\in W^{1,p}(\mathbb{R})
\qquad
\text{for every }p\in\left[\frac{1}{\alpha},+\infty\right].
$$

Recall that

$$
u\in W^{1,p}(\mathbb{R})
\quad
\Longleftrightarrow
\quad
u\in L^p(\mathbb{R})
\text{ and }
u'\in L^p(\mathbb{R}).
$$

## Step 1: The case p equals infinity

We have

$$
u(x)=\frac{1}{(1+x^2)^{\frac{\alpha}{2}}\log(2+x^2)}.
$$

Since

$$
(1+x^2)^{\frac{\alpha}{2}}\geq 1
$$

and

$$
\log(2+x^2)\geq \log 2,
$$

we obtain

$$
0<u(x)\leq \frac{1}{\log 2}.
$$

Therefore,

$$
u\in L^\infty(\mathbb{R}).
$$

## Step 2: The case p finite

Assume that

$$
\frac{1}{\alpha}\leq p<+\infty.
$$

Since the function is continuous, it is enough to study the behavior when

$$
|x|\to+\infty.
$$

For large values of

$$
|x|,
$$

we have

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
|u(x)|^p\sim \frac{1}{|x|^{\alpha p}(\log |x|)^p}.
$$

Thus, it is enough to study

$$
\int_R^{+\infty}\frac{1}{x^{\alpha p}(\log x)^p}\,dx.
$$

If

$$
p>\frac{1}{\alpha},
$$

then

$$
\alpha p>1.
$$

Therefore,

$$
\int_R^{+\infty}\frac{1}{x^{\alpha p}(\log x)^p}\,dx
\leq
\int_R^{+\infty}\frac{1}{x^{\alpha p}}\,dx
<+\infty.
$$

Now suppose that

$$
p=\frac{1}{\alpha}.
$$

Then

$$
\alpha p=1.
$$

So we need to study

$$
\int_R^{+\infty}\frac{1}{x(\log x)^p}\,dx.
$$

Use the change of variables

$$
s=\log x,
\qquad
ds=\frac{1}{x}\,dx.
$$

Then

$$
\int_R^{+\infty}\frac{1}{x(\log x)^p}\,dx
=
\int_{\log R}^{+\infty}\frac{1}{s^p}\,ds.
$$

Since

$$
0<\alpha<1,
$$

we have

$$
p=\frac{1}{\alpha}>1.
$$

Therefore,

$$
\int_{\log R}^{+\infty}\frac{1}{s^p}\,ds<+\infty.
$$

Hence,

$$
u\in L^p(\mathbb{R})
\qquad
\text{for every }p\in\left[\frac{1}{\alpha},+\infty\right].
$$

## Step 3: Integrability of the derivative

We compute the derivative of

$$
u(x)=(1+x^2)^{-\frac{\alpha}{2}}\big(\log(2+x^2)\big)^{-1}.
$$

By the product rule,

$$
u'(x)=
-\frac{\alpha x}{1+x^2}(1+x^2)^{-\frac{\alpha}{2}}\big(\log(2+x^2)\big)^{-1}
-
(1+x^2)^{-\frac{\alpha}{2}}\frac{2x}{(2+x^2)\big(\log(2+x^2)\big)^2}.
$$

Factoring

$$
u(x),
$$

we obtain

$$
u'(x)=u(x)\bigg(-\frac{\alpha x}{1+x^2}-\frac{2x}{(2+x^2)\log(2+x^2)}\bigg).
$$

Define

$$
h(x)=-\frac{\alpha x}{1+x^2}-\frac{2x}{(2+x^2)\log(2+x^2)}.
$$

Then

$$
u'(x)=u(x)h(x).
$$

Moreover,

$$
-\frac{\alpha x}{1+x^2}\to 0
\qquad
\text{as }|x|\to+\infty,
$$

and

$$
-\frac{2x}{(2+x^2)\log(2+x^2)}\to 0
\qquad
\text{as }|x|\to+\infty.
$$

Thus,

$$
h\in L^\infty(\mathbb{R}).
$$

Therefore, for every finite

$$
p\in\left[\frac{1}{\alpha},+\infty\right),
$$

we have

$$
\|u'\|_{L^p(\mathbb{R})}
=
\|uh\|_{L^p(\mathbb{R})}
\leq
\|h\|_{L^\infty(\mathbb{R})}\|u\|_{L^p(\mathbb{R})}
<+\infty.
$$

For

$$
p=+\infty,
$$

we also have

$$
\|u'\|_{L^\infty(\mathbb{R})}
\leq
\|h\|_{L^\infty(\mathbb{R})}\|u\|_{L^\infty(\mathbb{R})}
<+\infty.
$$

Hence,

$$
u'\in L^p(\mathbb{R})
\qquad
\text{for every }p\in\left[\frac{1}{\alpha},+\infty\right].
$$

Consequently,

$$
u\in W^{1,p}(\mathbb{R})
\qquad
\text{for every }p\in\left[\frac{1}{\alpha},+\infty\right].
$$

## Step 4: Non-integrability for q less than 1 over alpha

Let

$$
1\leq q<\frac{1}{\alpha}.
$$

For large values of

$$
x,
$$

we have

$$
u(x)\sim \frac{1}{2x^\alpha\log x}.
$$

Therefore,

$$
|u(x)|^q\sim \frac{1}{x^{\alpha q}(\log x)^q}.
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

Choose

$$
\gamma
$$

such that

$$
\beta<\gamma<1.
$$

Let

$$
\varepsilon=\gamma-\beta>0.
$$

For large enough

$$
x,
$$

we have

$$
(\log x)^q\leq x^\varepsilon.
$$

Therefore,

$$
x^\beta(\log x)^q\leq x^\beta x^\varepsilon=x^\gamma.
$$

Hence,

$$
\frac{1}{x^\beta(\log x)^q}\geq \frac{1}{x^\gamma}.
$$

Since

$$
\gamma<1,
$$

we have

$$
\int_R^{+\infty}\frac{1}{x^\gamma}\,dx=+\infty.
$$

Therefore,

$$
\int_R^{+\infty}|u(x)|^q\,dx=+\infty.
$$

Hence,

$$
u\notin L^q(\mathbb{R})
\qquad
\text{for every }q\in\left[1,\frac{1}{\alpha}\right).
$$

This proves the result.
```



