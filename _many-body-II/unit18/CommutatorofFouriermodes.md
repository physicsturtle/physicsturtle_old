---
layout: lesson
title: Commutator of Fourier modes
dept: physics
course: many-body-II
unit: unit18
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 18
---

In this section, we will calculate the commutator of Fourier modes. We will include the implicit time-ordering symbol. We want to calculate
 
 $$T_\tau[\Ahat_k,\Bhat_{k'}] = \frac{1}{(2\pi)^2} \int_0^\ell \int_0^\ell T_\tau\left(A(\tau - ix) B(-iy) - B(\tau - iy) A(-ix)\right) e^{-ikx} e^{-ik'y} \d x \d y $$
 
If we assume these are bosonic operators and that they have an operator product expansion of the form 

$$\Ahat(z_1^{*})\Bhat(z_2^{*}) = \frac{\Chat(z_2^{*})}{z_{12}^{*2}} + \frac{\Dhat(z_2^{*})}{z_{12}^{*}} + O(1)$$
 
This also implies that 

$$\Bhat(z_2^{*})\Ahat(z_1^{*}) = \frac{\Chat(z_2^{*})}{z_{12}^{*2}} + \frac{\Dhat(z_2^{*})}{z_{12}^{*}} + O(1)$$
 
 Subsequently, we have that 
 
 $$\begin{align}
T_\tau [A(\tau - ix) B(-iy) - B(\tau - iy) A(-ix) ] =& 
\end{align}$$

Consider the integral

$$\begin{align}
\oint_{-iy} A(z) \d z =& \int_1 A(z) \d z + \int_2 A(z) \d z + \int_3 A(z) \d z + \int_4 A(z) \d z \\
=& \int_\ell^0 (-i)\Ahat(\tau - ix) \d x + \int_{\tau}^{-\tau}A(\tau')\d\tau' + \int_0^\ell (-i)\Ahat(-\tau - ix) \d x + \int_{-\tau}^\tau \Ahat(\tau' - i\ell) \d \tau'
\end{align}$$

Now, consider the following 

$$\begin{align}
\oint_{-iy} T_\tau[\Ahat(z)\Bhat(-iy)] \d z =& \int_1 T_\tau[\Ahat(z)\Bhat(-iy)] \d z + \int_2 T_\tau[\Ahat(z)\Bhat(-iy)] \d z + \int_3 T_\tau[\Ahat(z)\Bhat(-iy)]  \d z + \int_4 T_\tau[\Ahat(z)\Bhat(-iy)]  \d z \\
=& \int_\ell^0 (-i)T_\tau[\Ahat(\tau - ix)\Bhat(-iy)] \d x + \int_{\tau}^{-\tau}T_\tau[A(\tau')\Bhat(-iy)] \d\tau' \\
&+ \int_0^\ell (-i)T_\tau[\Ahat(-\tau - ix)\Bhat(-iy)] \d x + \int_{-\tau}^\tau T_\tau[\Ahat(\tau' - i\ell)\Bhat(-iy)] \d \tau' \\
=& \int_\ell^0 (-i)\Ahat(\tau - ix)\Bhat(-iy) \d x + \int_{\tau}^{-\tau}T_\tau[A(\tau')\Bhat(-iy)] \d\tau' \\
&+ \int_0^\ell (-i)\Bhat(-iy)\Ahat(-\tau - ix) \d x + \int_{-\tau}^\tau T_\tau[\Ahat(\tau' - i\ell)\Bhat(-iy)] \d \tau' \\
=& i\int_0^\ell \left( \Ahat(\tau - ix)\Bhat(-iy) - \Bhat(-iy)\Ahat(-\tau - ix)\right) \d x \\
&+\int_{-\tau}^\tau \left( T_\tau[\Ahat(\tau' - i\ell)\Bhat(-iy)] - T_\tau[\Ahat(\tau')\Bhat(-iy)] \right)\d \tau'
\end{align}$$

From this, we conclude that 

$$\begin{align}
i\int_0^\ell \left( \Ahat(\tau - ix)\Bhat(-iy) - \Bhat(-iy)\Ahat(-\tau - ix)\right) \d x =& \oint_{-iy} T_\tau[\Ahat(z)\Bhat(-iy)] \d z \\
&-  \int_{-\tau}^\tau \left( T_\tau[\Ahat(\tau' - i\ell)\Bhat(-iy)] - T_\tau[\Ahat(\tau')\Bhat(-iy)] \right)\d \tau'
\end{align}$$

Now, we take the limit as \\(\tau \to 0\\) on both sides. Since the integrand is bounded for the second integral on the right, and the interval shrinks to 0, we can remove it. Thus, 

$$\begin{align}
i\int_0^\ell \left( \Ahat(\tau - ix)\Bhat(-iy) - \Bhat(-iy)\Ahat(-\tau - ix)\right) \d x =& \oint_{-iy} T_\tau[\Ahat(z)\Bhat(-iy)] \d z
\end{align}$$

Now, we replace this in the formula for the commutator of the Fourier components: 

$$$$\begin{align}
T_\tau[\Ahat_k,\Bhat_{k'}] = \frac{1}{(2\pi)^2} \int_0^\ell \oint_{-iy} T_\tau[\Ahat(z)\Bhat(-iy)] e^{kz} \d ze^{-ik'y} \d y 
\end{align}$$$$
 
Now, we use the OPE for the fields \\(\Ahat\\) and \\(\Bhat\\) to get 

$$$$\begin{align}
T_\tau[\Ahat_k,\Bhat_{k'}] = \frac{1}{(2\pi)^2} \int_0^\ell \frac{1}{i} \oint_{-iy} \left(\frac{\Chat(-iy)}{(z+iy)^2} + \frac{\Dhat(-iy)}{z+iy}\right) e^{kz} \d ze^{-ik'y} \d y 
\end{align}$$$$

Now evaluating the contour integral, we find that 

$$\begin{align}
T_\tau[\Ahat_k,\Bhat_{k'}] =& \frac{1}{(2\pi)^2} \int_0^\ell \frac{1}{i} \oint_{-iy} \left(2\pi i k e^{-iky}\Chat(-iy) + 2\pi i\Dhat(-iy)e^{-iky} \right) e^{-ik'y} \d y \\
=& \frac{1}{2\pi} \int_0^\ell \left(k\Chat(-iy) + \Dhat(-iy) \right) e^{-iky} e^{-ik'y} \d y \\
=& k\Chat_{k+k'} + \Dhat_{k+k'}
\end{align}$$

We therefore have the result 

$$[\Ahat_k, \Bhat_{k'}] = k\Chat_{k+k'} + \Dhat_{k+k'}.$$

Note that with \\(k_n = 2\pi n/L\\), this allows us to instead write 

$$[\Ahat_m, \Bhat_n] =\frac{2\pi m}{\ell} \Chat_{m+n} + \Dhat_{m+n}.$$


