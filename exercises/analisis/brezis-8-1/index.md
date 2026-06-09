---
layout: page
title: Brezis 8.1
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

We want to prove that

$$
u\in W^{1,p}(\mathbb{R})
\qquad
\forall p\in \left[\frac{1}{\alpha},+\infty\right].
$$
