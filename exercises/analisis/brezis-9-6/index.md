---

layout: default
title: "Brezis Lemma 9.6"
permalink: /exercises/analisis/brezis-9-6/
------------------------------------------

# Brezis Lemma 9.6

In this exercise we prove an estimate for difference quotients in the half-space.

Let

$$\Omega=\mathbb{R}^{N}_{+}=\left{x=(x',x_N)\in\mathbb{R}^{N}:x_N>0\right}.$$

The boundary of this set is

$$\Gamma=\partial\Omega=\left{x=(x',x_N)\in\mathbb{R}^{N}:x_N=0\right}.$$

We say that the vector h is parallel to the boundary if

$$h\parallel\Gamma.$$

This means that

$$h=(h',0)\in\mathbb{R}^{N-1}\times{0}.$$

For h different from zero, define

$$D_hu(x)=\frac{\tau_hu(x)-u(x)}{|h|}=\frac{u(x+h)-u(x)}{|h|}.$$

We want to prove that

$$|D_hu|*{L^2(\Omega)}\leq|\nabla u|*{L^2(\Omega)}.$$

This estimate holds for every

$$u\in H^1(\Omega)$$

and every

$$h\parallel\Gamma.$$

## Statement

Let

$$\Omega=\mathbb{R}^{N}_{+}.$$

Assume that

$$h\parallel\Gamma,\qquad h\neq 0,\qquad u\in H^1(\Omega).$$

Then

$$|D_hu|*{L^2(\Omega)}\leq|\nabla u|*{L^2(\Omega)}.$$

## Proof

First, assume that u is smooth. More precisely, assume that

$$u\in C_c^1(\mathbb{R}^{N}).$$

Fix

$$x\in\Omega.$$

Since h is parallel to the boundary, h has no component in the direction of x_N. Therefore,

$$x+th\in\Omega\qquad\text{for every }t\in[0,1].$$

Define

$$g(t)=u(x+th),\qquad t\in[0,1].$$

By the chain rule,

$$g'(t)=h\cdot\nabla u(x+th).$$

By the fundamental theorem of calculus,

$$u(x+h)-u(x)=g(1)-g(0)=\int_0^1 h\cdot\nabla u(x+th),dt.$$

Dividing by the norm of h, we get

$$D_hu(x)=\frac{u(x+h)-u(x)}{|h|}=\int_0^1\frac{h}{|h|}\cdot\nabla u(x+th),dt.$$

Hence,

$$|D_hu(x)|\leq\int_0^1|\nabla u(x+th)|,dt.$$

By Cauchy's inequality,

$$|D_hu(x)|^2\leq\left(\int_0^1|\nabla u(x+th)|,dt\right)^2\leq\int_0^1|\nabla u(x+th)|^2,dt.$$

Now integrate over Omega:

$$\int_{\Omega}|D_hu(x)|^2,dx\leq\int_{\Omega}\int_0^1|\nabla u(x+th)|^2,dt,dx.$$

By Fubini's theorem,

$$\int_{\Omega}|D_hu(x)|^2,dx\leq\int_0^1\int_{\Omega}|\nabla u(x+th)|^2,dx,dt.$$

For fixed t, use the change of variables

$$y=x+th.$$

Since h is parallel to the boundary, this change of variables maps Omega onto itself. Therefore,

$$\int_{\Omega}|\nabla u(x+th)|^2,dx=\int_{\Omega}|\nabla u(y)|^2,dy.$$

Thus,

$$\int_{\Omega}|D_hu(x)|^2,dx\leq\int_0^1\int_{\Omega}|\nabla u(y)|^2,dy,dt.$$

Since the inner integral does not depend on t, we obtain

$$\int_{\Omega}|D_hu(x)|^2,dx\leq\int_{\Omega}|\nabla u(y)|^2,dy.$$

Therefore,

$$|D_hu|*{L^2(\Omega)}^2\leq|\nabla u|*{L^2(\Omega)}^2.$$

Taking square roots gives

$$|D_hu|*{L^2(\Omega)}\leq|\nabla u|*{L^2(\Omega)}.$$

This proves the result for smooth functions.

Now let

$$u\in H^1(\Omega).$$

Choose a sequence

$$u_n\in C_c^1(\mathbb{R}^{N})$$

such that

$$u_n\to u\qquad\text{in }H^1(\Omega).$$

From the smooth case, we have

$$|D_hu_n|*{L^2(\Omega)}\leq|\nabla u_n|*{L^2(\Omega)}.$$

We pass to the limit.

Since

$$D_hu_n-D_hu=D_h(u_n-u),$$

we have

$$|D_hu_n-D_hu|*{L^2(\Omega)}=|D_h(u_n-u)|*{L^2(\Omega)}.$$

Using the definition of D_h,

$$|D_h(u_n-u)|*{L^2(\Omega)}=\frac{1}{|h|}|\tau_h(u_n-u)-(u_n-u)|*{L^2(\Omega)}.$$

By the triangle inequality,

$$|D_h(u_n-u)|*{L^2(\Omega)}\leq\frac{1}{|h|}\left(|\tau_h(u_n-u)|*{L^2(\Omega)}+|u_n-u|_{L^2(\Omega)}\right).$$

Since the translation is tangential, it preserves the L^2 norm on Omega. Hence,

$$|\tau_h(u_n-u)|*{L^2(\Omega)}=|u_n-u|*{L^2(\Omega)}.$$

Therefore,

$$|D_hu_n-D_hu|*{L^2(\Omega)}\leq\frac{2}{|h|}|u_n-u|*{L^2(\Omega)}.$$

Since

$$u_n\to u\qquad\text{in }H^1(\Omega),$$

we also have

$$u_n\to u\qquad\text{in }L^2(\Omega).$$

Thus,

$$D_hu_n\to D_hu\qquad\text{in }L^2(\Omega).$$

Also,

$$\nabla u_n\to\nabla u\qquad\text{in }L^2(\Omega).$$

Passing to the limit in the inequality

$$|D_hu_n|*{L^2(\Omega)}\leq|\nabla u_n|*{L^2(\Omega)},$$

we obtain

$$|D_hu|*{L^2(\Omega)}\leq|\nabla u|*{L^2(\Omega)}.$$

Therefore,

$$\boxed{|D_hu|*{L^2(\Omega)}\leq|\nabla u|*{L^2(\Omega)}}.$$

This completes the proof.

## Key idea

The condition

$$h\parallel\Gamma$$

means that h is tangent to the boundary of the half-space.

Therefore, if

$$x\in\Omega,$$

then

$$x+th\in\Omega\qquad\text{for every }t\in[0,1].$$

So we can use the fundamental theorem of calculus along the segment from x to x+h.

The final estimate is

$$|D_hu|*{L^2(\Omega)}\leq|\nabla u|*{L^2(\Omega)}.$$

This means that the tangential difference quotient is controlled by the weak gradient.
