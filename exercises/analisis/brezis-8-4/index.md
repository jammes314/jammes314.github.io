---
layout: page
title: "Brezis 8.4"
permalink: /exercises/analisis/brezis-8-4/
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

<style>
.exercise-post {
  max-width: 900px;
  margin: 0 auto;
  line-height: 1.7;
  font-size: 1.05rem;
}

.exercise-title {
  color: #8B0D1C;
  border-bottom: 3px solid #8B0D1C;
  padding-bottom: 0.35rem;
  margin-bottom: 1.2rem;
}

.statement-box {
  border-left: 6px solid #8B0D1C;
  background: #fff7f7;
  padding: 1rem 1.25rem;
  margin: 1.25rem 0 1.75rem 0;
}

.solution-box {
  border-left: 6px solid #0047AB;
  background: #f7faff;
  padding: 1rem 1.25rem;
  margin: 1.25rem 0;
}

.part-title {
  color: #8B0D1C;
  font-weight: 700;
  margin-top: 1.6rem;
}
</style>

<div class="exercise-post" markdown="1">

# Brezis 8.4
{: .exercise-title}

<div class="statement-box" markdown="1">

**Statement.** Fix a function $\varphi\in C_c^{\infty}(\mathbb{R})$, $\varphi\neq 0$, and set

$$
u_n(x)=\varphi(x+n).$$

Let $1\le p\le \infty$.

1. Check that $(u_n)$ is bounded in $W^{1,p}(\mathbb{R})$.

2. Prove that there exists no subsequence $(u_{n_k})$ converging strongly in $L^q(\mathbb{R})$, for any $1\le q\le \infty$.

3. Show that $u_n\rightharpoonup 0$ weakly in $W^{1,p}(\mathbb{R})$ for every $p\in(1,\infty)$.

</div>

<div class="solution-box" markdown="1">

**Solution.** Since $\varphi\in C_c^\infty(\mathbb{R})$, there exists $R>0$ such that

$$
\operatorname{supp}\varphi\subset [-R,R].
$$

Hence

$$
\operatorname{supp}u_n\subset[-n-R,-n+R].
$$

<div class="part-title" markdown="1">1. Boundedness in $W^{1,p}(\mathbb{R})$</div>

For $1\le p<\infty$, using the change of variables $y=x+n$, we get

$$
\|u_n\|_{L^p(\mathbb{R})}^p
=
\int_{\mathbb{R}} |\varphi(x+n)|^p\,dx
=
\int_{\mathbb{R}} |\varphi(y)|^p\,dy
=
\|\varphi\|_{L^p(\mathbb{R})}^p.
$$

Also,

$$
u_n'(x)=\varphi'(x+n),$$

and therefore

$$
\|u_n'\|_{L^p(\mathbb{R})}
=
\|\varphi'\|_{L^p(\mathbb{R})}.
$$

Thus

$$
\|u_n\|_{W^{1,p}(\mathbb{R})}
=
\|\varphi\|_{W^{1,p}(\mathbb{R})},
$$

so $(u_n)$ is bounded in $W^{1,p}(\mathbb{R})$.

For $p=\infty$, the same argument gives

$$
\|u_n\|_{L^\infty(\mathbb{R})}
=
\|\varphi\|_{L^\infty(\mathbb{R})},
\qquad
\|u_n'\|_{L^\infty(\mathbb{R})}
=
\|\varphi'\|_{L^\infty(\mathbb{R})}.
$$

Hence $(u_n)$ is also bounded in $W^{1,\infty}(\mathbb{R})$.

<div class="part-title" markdown="1">2. No strongly convergent subsequence in $L^q(\mathbb{R})$</div>

Let $1\le q\le\infty$. Suppose, by contradiction, that there exists a subsequence $(u_{n_k})$ which converges strongly in $L^q(\mathbb{R})$.

Then $(u_{n_k})$ must be a Cauchy sequence in $L^q(\mathbb{R})$.

However, since $n_k\to\infty$, for every $K>0$ we can choose $j,k\ge K$ such that

$$
|n_j-n_k|>2R.
$$

Thus the supports of $u_{n_j}$ and $u_{n_k}$ are disjoint.

If $1\le q<\infty$, then

$$
\|u_{n_j}-u_{n_k}\|_{L^q}^q
=
\|u_{n_j}\|_{L^q}^q+
\|u_{n_k}\|_{L^q}^q
=
2\|\varphi\|_{L^q}^q.
$$

Therefore

$$
\|u_{n_j}-u_{n_k}\|_{L^q}
=
2^{1/q}\|\varphi\|_{L^q}>0.
$$

If $q=\infty$, then, again using the disjointness of the supports,

$$
\|u_{n_j}-u_{n_k}\|_{L^\infty}
=
\|\varphi\|_{L^\infty}>0.
$$

So $(u_{n_k})$ cannot be Cauchy in $L^q(\mathbb{R})$, which is a contradiction.

Hence there exists no subsequence of $(u_n)$ converging strongly in $L^q(\mathbb{R})$, for any $1\le q\le\infty$.

<div class="part-title" markdown="1">3. Weak convergence in $W^{1,p}(\mathbb{R})$</div>

Let $p\in(1,\infty)$ and let $p'$ be the conjugate exponent of $p$, that is,

$$
\frac1p+\frac1{p'}=1.
$$

We first prove the following fact: if $f\in L^{p'}(\mathbb{R})$ and $\psi\in C_c^\infty(\mathbb{R})$, then

$$
\int_{\mathbb{R}} f(x)\psi(x+n)\,dx\to 0.
$$

Indeed, if $\operatorname{supp}\psi\subset[-R,R]$, then

$$
\operatorname{supp}\psi(x+n)\subset[-n-R,-n+R].
$$

By Hölder's inequality,

$$
\left|\int_{\mathbb{R}} f(x)\psi(x+n)\,dx\right|
\le
\|f\|_{L^{p'}([-n-R,-n+R])}\,\|\psi\|_{L^p(\mathbb{R})}.
$$

Since $f\in L^{p'}(\mathbb{R})$ and the interval $[-n-R,-n+R]$ escapes to infinity, we have

$$
\|f\|_{L^{p'}([-n-R,-n+R])}\to 0.
$$

Therefore

$$
\int_{\mathbb{R}} f(x)\psi(x+n)\,dx\to 0.
$$

Applying this with $\psi=\varphi$ gives

$$
\int_{\mathbb{R}} f(x)u_n(x)\,dx\to 0
\qquad
\forall f\in L^{p'}(\mathbb{R}).
$$

Thus

$$
u_n\rightharpoonup 0
\qquad\text{weakly in }L^p(\mathbb{R}).
$$

Applying the same argument with $\psi=\varphi'$ gives

$$
\int_{\mathbb{R}} f(x)u_n'(x)\,dx\to 0
\qquad
\forall f\in L^{p'}(\mathbb{R}),
$$

and hence

$$
u_n'\rightharpoonup 0
\qquad\text{weakly in }L^p(\mathbb{R}).
$$

Now let $F\in (W^{1,p}(\mathbb{R}))^*$. Since $W^{1,p}(\mathbb{R})$ is continuously embedded into $L^p(\mathbb{R})\times L^p(\mathbb{R})$ by

$$
v\mapsto (v,v'),
$$

every such functional can be written in the form

$$
F(v)=\int_{\mathbb{R}} f(x)v(x)\,dx+
\int_{\mathbb{R}} g(x)v'(x)\,dx,
$$

for some $f,g\in L^{p'}(\mathbb{R})$.

Therefore

$$
F(u_n)
=
\int_{\mathbb{R}} f(x)u_n(x)\,dx
+
\int_{\mathbb{R}} g(x)u_n'(x)\,dx
\to 0.
$$

Hence

$$
u_n\rightharpoonup 0
\qquad\text{weakly in }W^{1,p}(\mathbb{R}),
\qquad 1<p<\infty.
$$

</div>

</div>
