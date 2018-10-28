---
layout: page
title: Laplace's Method
course: test
unit: unit1
permalink: /test/laplace-method/
---

Laplace's method is a technique for asymptotically evaluating integrals of the form

$$I = \int_a^b e^{zf(t)}g(t) dt$$

The main contribution to the integral is due to the exponential, which is localized about the maxima of $f$. The maxima of $f$ occur at $t_\ast$, where $f'(t_\ast) = 0$, and $f'\'(t_\ast) < 0$. Let's expand $f$ about $t_\ast$.

$$f(t) = f(t_\ast) + \underbrace{f'(t_\ast)(t-t_\ast)}_{0} + \frac{f''(t_\ast)(t-t_\ast)^2}{2} + \frac{f'''(t_\ast)(t-t_\ast)^3}{6} + \cdots$$

and also expand $g(t)$ about the same point:

$$g(t) = g(t_\ast) + g'(t_\ast)(t-t_\ast) + \frac{g''(t_\ast)(t-t_\ast)^2}{2} + \frac{g'''(t_\ast)(t-t_\ast)^3}{6} + \cdots.$$

For notational convenience, denote $f(t_\ast) = f_\ast$, and $g(t_\ast) = g_\ast$. This gives the integral

$$I \approx \int_a^b e^{zf(t)} g(t) dt = \int_a^b e^{zf_\ast + \frac{z}{2}f''_\ast(t-t_\ast)^2} (g_\ast + g'_\ast(t-t_\ast)) dt$$

Let $u^2 = \frac{z}{2}\|f_\ast'\'\|(t-t_\ast)^2$, so $ t - t_\ast = u\sqrt{\frac{2}{z\|f_\ast\'\'\|}}$ and $dt = \sqrt{\frac{2}{z\|f_\ast\'\'\|}}du$, which allows us to approximate the integral in terms of its leading order term:

$$\begin{eqnarray}
I &\approx& e^{zf_\ast}g_\ast\int_{-\infty}^\infty e^{-u^2} \sqrt{\frac{2}{z|f''_\ast|}}du \\
&=& e^{zf_\ast}g_\ast \sqrt{\frac{2}{z|f''_\ast|}} \int_{-\infty}^\infty e^{-u^2}du\\
&=& e^{zf_\ast}g_\ast \sqrt{\frac{2\pi}{z|f''_\ast|}}
\end{eqnarray}$$

from which we have Laplace's Method:

(make a box of laplace's method)



### A Degenerate Case
Suppose $g_\ast = 0$. Then the entire formula breaks down! We need to proceed to higher order approximation of $g$. This involves going back to when we first Taylor expand

$$I \approx \int_a^b e^{zf(t)} g(t) dt = \int_a^b e^{zf_\ast + \frac{z}{2}f''_\ast(t-t_\ast)^2} \left(g_\ast + g'_\ast(t-t_\ast) + g''_\ast\frac{(t-t_\ast)^2}{2} + \cdots\right) dt$$

and then keeping the linear term of $g$. We make the same substitution for $u$ as before:

$$\begin{eqnarray}
I &\approx& e^{zf_\ast }g'_\ast \int_{-\infty}^\infty e^{ -u^2}|u|\sqrt{\frac{2}{z|f''_\ast|}}du\\
&=& e^{zf_\ast }g'_\ast \sqrt{\frac{2}{z|f''_\ast|}} \int_0^\infty e^{ -u^2}(2u)du\\
&=& e^{zf_\ast }g'_\ast \sqrt{\frac{2}{z|f''_\ast|}} (-1)\left.e^{-u^2}\right|^\infty_0\\
&=& e^{zf_\ast }g'_\ast \sqrt{\frac{2}{z|f''_\ast|}}
\end{eqnarray}$$






