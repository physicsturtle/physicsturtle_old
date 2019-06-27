---
layout: page
title: Inverse Laplace Transform
course: test
unit: unit1
permalink: /test/inverse-laplace-transform/
---

The inverse Laplace transform is 

$$f(t) = \frac{1}{2\pi i}\lim_{T\to\infty}\int_{\gamma - iT}^{\gamma + iT}e^{st}F(s) ds$$

where $\Re(s) = \gamma$ is the vertical line where $\gamma$ is greater than all singularities of $F(s)$, and $F(s)$ is also bounded on the line $\Re(s) = \gamma$. In practice, this integral can be evaluated by constructing a semicircular contour going upward along the line $\Re(s) = \gamma$, then counterclockwise along the contour $s = \gamma + re^{i\theta}$ for $\theta$ from $\pi/2$ to $3\pi/2$. 



<div class="example">
<b>Example:</b> Find the inverse Laplace transform of $F(s) = 1/s$. 
<b>Solution:</b> In order to evaluate 
$$f(t) = \frac{1}{2\pi i}\lim_{T\to\infty}\int_{\gamma - iT}^{\gamma + iT} \frac{e^{st}}{s}ds,$$
we need to consider doing the integral 
$$\int_C \frac{e^{st}}{s} ds$$
where $C$ is the contour $\Re(s) = \gamma$, then counterclockwise along the contour $s = \gamma + re^{i\theta}$ for $\theta$ from $\pi/2$ to $3\pi/2$. We split the integral up into two pieces
$$\int_C \frac{e^{st}}{s} ds = \int_{\pi/2}^{3\pi/2} \frac{e^{\gamma + re^{i\varphi}}rie^{i\varphi}}{\gamma + re^{i\varphi}} d\varphi + \int_{\gamma-ir}^{\gamma+ir} \frac{e^{st}}{s} ds $$
We consider the magnitude of the first integral 
$$\begin{eqnarray*}
\left|\int_{\pi/2}^{3\pi/2} \frac{e^{\gamma + r\cos\varphi + ir\sin\varphi}rie^{i\varphi}}{\gamma + re^{i\varphi}} d\varphi\right| &\leq& \int_{\pi/2}^{3\pi/2} \left|\frac{e^{\gamma + r\cos\varphi + ir\sin\varphi}rie^{i\varphi}}{\gamma + re^{i\varphi}}\right| d\varphi \\
&=& \int_{\pi/2}^{3\pi/2} \left|\frac{e^{\gamma + r\cos\varphi}r}{\gamma + re^{i\varphi}}\right| d\varphi \\
&=& e^\gamma \int_{\pi/2}^{3\pi/2} \left|\frac{e^{r\cos\varphi}}{\gamma/r + e^{i\varphi}}\right| d\varphi \\
\end{eqnarray*}$$
As $r$ grows, the numerator goes to zero for every value of $\varphi$, so this integral goes to zero for $r\to\infty$. Thus, as $r$ goes to $\infty$, 

$$\int_C \frac{e^{st}}{s} ds = \int_{\gamma-ir}^{\gamma+ir} \frac{e^{st}}{s} ds, \qquad r\to\infty.$$

The right hand side is the integral which we actually want to calculate, and the left hand side is a contour integral around a closed contour. This closed contour encloses the only pole of the integrand, at $s = 0$. We can apply the residue theorem to evaluate this integral. The residue of the pole at $s = 0$ is $1$, so the integral is 
$$\int_C \frac{e^{st}}{s} ds = 2\pi i \Res\left(\frac{e^{st}}{s},s=0\right) = 2\pi i$$

Thus the inverse Laplace transform is 

$$f(t) = 1.$$
</div>
