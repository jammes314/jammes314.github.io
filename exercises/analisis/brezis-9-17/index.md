---
layout: page
title: " Lema 9.6"
permalink: /exercises/analisis/brezis-9-6/
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


En este post se transcribe y ordena el detalle del argumento de cocientes de diferencias tangenciales en el semiespacio. La idea central es probar primero la estimación para funciones suaves y luego pasar al límite por densidad en $H^1(\Omega)$.

## Contexto

Sea

$$
\Omega=\mathbb{R}^N_+
=
\{x=(x',x_N)\in\mathbb{R}^N: x_N>0\},
$$

y sea

$$
\Gamma=\partial\Omega=\{x_N=0\}.
$$

Diremos que $h\parallel \Gamma$ si

$$
h=(h',0)\in \mathbb{R}^{N-1}\times\{0\}.
$$

En particular, si $x\in\Omega$ y $t\in[0,1]$, entonces

$$
x+th\in\Omega.
$$

Esto ocurre porque $h$ no cambia la coordenada $x_N$.

Definimos la traslación

$$
\tau_h u(x)=u(x+h)
$$

y el cociente de diferencias

$$
D_hu(x)=\frac{\tau_hu(x)-u(x)}{|h|}
=
\frac{u(x+h)-u(x)}{|h|},
\qquad h\neq 0.
$$

## Lema

Si $u\in H^1(\Omega)$ y $h\parallel\Gamma$, entonces

$$
\|D_hu\|_{L^2(\Omega)}
\le
\|\nabla u\|_{L^2(\Omega)}.
$$

## Demostración

Primero probamos la desigualdad para una función suave. Supongamos que

$$
v\in C_c^1(\overline{\Omega}).
$$

Fijemos $x\in\Omega$ y tomemos $h\parallel \Gamma$. Como la traslación es paralela a la frontera, tenemos

$$
x+th\in\Omega,
\qquad 0\le t\le 1.
$$

Definimos

$$
g(t)=v(x+th),
\qquad t\in[0,1].
$$

Entonces, por la regla de la cadena,

$$
g'(t)=h\cdot \nabla v(x+th).
$$

Por el teorema fundamental del cálculo,

$$
v(x+h)-v(x)
= g(1)-g(0)
= \int_0^1 h\cdot \nabla v(x+th)\,dt.
$$

Dividiendo entre $|h|$, obtenemos

$$
D_hv(x)
=
\int_0^1 \frac{h}{|h|}\cdot \nabla v(x+th)\,dt.
$$

Por la desigualdad de Cauchy--Schwarz en $\mathbb{R}^N$,

$$
|D_hv(x)|
\le
\int_0^1 |\nabla v(x+th)|\,dt.
$$

Elevando al cuadrado y usando Cauchy--Schwarz en la variable $t$, se tiene

$$
|D_hv(x)|^2
\le
\left(\int_0^1 |\nabla v(x+th)|\,dt\right)^2
\le
\int_0^1 |\nabla v(x+th)|^2\,dt.
$$

Ahora integramos en $\Omega$:

$$
\int_\Omega |D_hv(x)|^2\,dx
\le
\int_\Omega\int_0^1 |\nabla v(x+th)|^2\,dt\,dx.
$$

Por Fubini,

$$
\int_\Omega |D_hv(x)|^2\,dx
\le
\int_0^1\int_\Omega |\nabla v(x+th)|^2\,dx\,dt.
$$

En la integral interna hacemos el cambio de variable

$$
y=x+th.
$$

Como $h\parallel\Gamma$, la traslación $x\mapsto x+th$ preserva el semiespacio $\Omega$. Además, el jacobiano del cambio de variable es igual a $1$. Por tanto,

$$
\int_\Omega |\nabla v(x+th)|^2\,dx
=
\int_\Omega |\nabla v(y)|^2\,dy.
$$

Así,

$$
\int_\Omega |D_hv(x)|^2\,dx
\le
\int_0^1\int_\Omega |\nabla v(y)|^2\,dy\,dt.
$$

Como la integral en $y$ no depende de $t$,

$$
\int_\Omega |D_hv(x)|^2\,dx
\le
\int_\Omega |\nabla v(y)|^2\,dy.
$$

Por lo tanto,

$$
\|D_hv\|_{L^2(\Omega)}^2
\le
\|\nabla v\|_{L^2(\Omega)}^2,
$$

es decir,

$$
\|D_hv\|_{L^2(\Omega)}
\le
\|\nabla v\|_{L^2(\Omega)}.
\tag{1}
$$

Ahora pasamos al caso general. Sea

$$
u\in H^1(\Omega).
$$

Tomamos una sucesión

$$
u_n\in C_c^1(\overline{\Omega})
$$

tal que

$$
u_n\to u
\qquad\text{en }H^1(\Omega).
$$

Por la parte anterior, para todo $n$,

$$
\|D_hu_n\|_{L^2(\Omega)}
\le
\|\nabla u_n\|_{L^2(\Omega)}.
\tag{2}
$$

Necesitamos justificar que se puede pasar al límite en esta desigualdad. Para ello observamos que

$$
D_hu_n-D_hu
= D_h(u_n-u).
$$

Entonces

$$
\|D_hu_n-D_hu\|_{L^2(\Omega)}
=\|D_h(u_n-u)\|_{L^2(\Omega)}.
$$

Usando la definición de $D_h$, tenemos

$$
\|D_h(u_n-u)\|_{L^2(\Omega)}
=
\frac{1}{|h|}
\|\tau_h(u_n-u)-(u_n-u)\|_{L^2(\Omega)}.
$$

Por la desigualdad triangular,

$$
\|D_h(u_n-u)\|_{L^2(\Omega)}
\le
\frac{1}{|h|}
\left(
\|\tau_h(u_n-u)\|_{L^2(\Omega)}
+
\|u_n-u\|_{L^2(\Omega)}
\right).
$$

Como $h\parallel\Gamma$, la traslación preserva $\Omega$, y entonces

$$
\|\tau_h(u_n-u)\|_{L^2(\Omega)}
=
\|u_n-u\|_{L^2(\Omega)}.
$$

Por tanto,

$$
\|D_hu_n-D_hu\|_{L^2(\Omega)}
\le
\frac{2}{|h|}
\|u_n-u\|_{L^2(\Omega)}.
$$

Como $u_n\to u$ en $H^1(\Omega)$, en particular

$$
u_n\to u
\qquad\text{en }L^2(\Omega).
$$

Así,

$$
D_hu_n\to D_hu
\qquad\text{en }L^2(\Omega).
$$

Además, como $u_n\to u$ en $H^1(\Omega)$, también se tiene

$$
\nabla u_n\to \nabla u
\qquad\text{en }L^2(\Omega).
$$

Finalmente, pasando al límite en (2), obtenemos

$$
\|D_hu\|_{L^2(\Omega)}
\le
\|\nabla u\|_{L^2(\Omega)}.
$$

Esto concluye la demostración.

$$
\square
$$

## Comentario clave

La condición $h\parallel\Gamma$ es esencial en este argumento porque garantiza que la traslación $x\mapsto x+th$ no saca los puntos de $\Omega$. Por eso podemos hacer el cambio de variable $y=x+th$ sin cambiar el dominio de integración.
