---
layout: lesson
title: Green Functions for Hamiltonian with Linear Dispersion - Exercises
dept: physics
course: many-body-II
unit: unit17
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 17
---
<ol>
\question Evaluate 

$$\begin{align}
\mathcal{G}_L(x,\tau;x',\tau') =& \frac{1}{L}\sum_{kk'}e^{ikx}e^{-ik'x'}\mathcal{G}_L(k,\tau;k',\tau') \\
=& -\frac{1}{L}\sum_{kk'}e^{ikx}e^{-ik'x'}(\theta(\tau-\tau')-n_F(\xi_k))e^{-(\tau-\tau')\xi_k}\delta_{kk'} \\
=& -\frac{1}{L}\sum_{k}e^{ik(x-x')}(\theta(\tau-\tau')-n_F(\xi_k))e^{-(\tau-\tau')\xi_k}
\end{align}$$

\begin{solution}
Now substituting in a left-moving \\(\xi_k = -v_Fk\\), we find 

$$\begin{align}
\mathcal{G}_L(x,\tau;x',\tau') =& -\frac{1}{L}\sum_{k}e^{k[i(x-x')+v_F(\tau-\tau')]}\left(\theta(\tau-\tau')- \frac{1}{1+e^{-\beta v_Fk}}\right)
\end{align}$$

There are 4 separate cases to consider:
<ol>[(i)]
<li> \\(\tau - \tau' > 0\\) and \\(x - x' > 0\\)
</li> 
 <li> \\(\tau - \tau' > 0\\) and \\(x - x' < 0\\)
</li> 
 <li> \\(\tau - \tau' < 0\\) and \\(x - x' > 0\\)
</li> 
 <li> \\(\tau - \tau' < 0\\) and \\(x - x' < 0\\)
\end{enumerate}

<ol type="i">
</li> 
 <li> 
We assume that \\(\tau - \tau' > 0\\) (of course we already know that \\(\tau - \tau' < \beta\\)). We also change the sum over \\(k\\) to an integral (taking the thermodynamic limit). Then, this simplifies to 

$$\begin{align}
\mathcal{G}_L(x,\tau;x',\tau') =& -\frac{1}{L}\int_{-\infty}^\infty e^{k[i(x-x')+v_F(\tau-\tau')]}\left(\frac{e^{-\beta v_Fk}}{1+e^{-\beta v_Fk}}\right) \frac{L\d k}{2\pi} \\
=& -\int_{-\infty}^\infty e^{k[i(x-x')+v_F(\tau-\tau' - \beta)]}\frac{1}{1+e^{-\beta v_Fk}} \frac{\d k}{2\pi} \\
\end{align}$$

This integral should converge as \\(k\to\infty\\) because of the numerator, and it should converge as \\(k\to-\infty\\) because of the denominator. Now, we need to consider two separate cases: \\(x - x' > 0\\) and \\(x - x' < 0\\). First we consider the \\(x - x' > 0\\) case. In this case, we should close the contour in the lower half plane. This will transform the integral to a sum over the poles of this function in the lower half-plane, which occur at \\(k = i\pi(2n+1)/v_F\beta\\), where \\(n = -1,-2,-3,\dots\\). We see that

$$\mathcal{G}_L(x,\tau;x',\tau') = -2\pi i\sum_{n=-\infty}^{-1} \Res_{k=i\pi(2n+1)/v_F\beta}  \frac{-e^{k[i(x-x')+v_F(\tau-\tau' - \beta)]}}{2\pi(1+e^{-\beta v_Fk})}, \quad x - x' > 0$$ 

The leading minus sign is because the contour goes clockwise. The residue yields 

$$\begin{align}
\Res_{k=i\pi(2n+1)/v_F\beta}  \frac{e^{k[i(x-x')+v_F(\tau-\tau' - \beta)]}}{2\pi(1+e^{-\beta v_Fk})} =& \frac{\exp\left(\frac{i\pi(2n+1)}{v_F\beta}[i(x-x') + v_F(\tau-\tau'-\beta)]\right)}{2\pi\beta v_F} \\
=& \frac{e^{i\alpha}}{2\pi\beta v_F} [e^{2i\alpha}]^n
\end{align}$$

where \\(\alpha = \frac{\pi}{v_F\beta}[i(x-x') + v_F(\tau-\tau'-\beta)]\\). Thus, we can compute a geometric series. This gives us 

$$\begin{align}
\mathcal{G}_L(x,\tau;x',\tau') =& 2\pi i\frac{e^{i\alpha}}{2\pi \beta v_F}\sum_{n=-\infty}^{-1} (e^{2i\alpha})^n, \quad x - x' > 0 \\
=& i\frac{e^{i\alpha}}{\beta v_F}\sum_{n=1}^\infty (e^{-2i\alpha})^n, \quad x - x' > 0 \\
=& i\frac{e^{i\alpha}}{\beta v_F}\left(\frac{1}{1-e^{-2i\alpha}} - 1\right), \quad x - x' > 0 \\
=& i\frac{1}{\beta v_F}\frac{1}{e^{i\alpha} - e^{-i\alpha}}, \quad x - x' > 0 \\
=& \frac{1}{2\beta v_F\sin\alpha} \quad x - x' > 0 \\
=& -\frac{1}{2\beta v_F\sin\frac{\pi}{\beta}(i(x-x') + v_F(\tau-\tau'))} \quad x - x' > 0 \\
=& -\frac{1}{2\pi} \frac{1}{\frac{\beta v_F}{\pi}\sin\frac{\pi}{\beta v_F}(z-z')} \quad x - x' > 0
\end{align}$$

</li> 
 <li> Now, we consider the case \\(\tau - \tau' > 0\\) and \\(x - x' < 0\\). Here, we close the contour in the upper-half plane. This time, there will be no leading minus sign because the contour goes counterclockwise.

$$\mathcal{G}_L(x,\tau;x',\tau') = 2\pi i\sum_{n=0}^{\infty} \Res_{k=i\pi(2n+1)/v_F\beta}  \frac{-e^{k[i(x-x')+v_F(\tau-\tau' - \beta)]}}{2\pi(1+e^{-\beta v_Fk})}, \quad x - x' < 0$$ 

The residue evaluation goes the same as before, and we find 

$$\begin{align}
\Res_{k=i\pi(2n+1)/v_F\beta}  \frac{-e^{k[i(x-x')+v_F(\tau-\tau' - \beta)]}}{2\pi(1+e^{-\beta v_Fk})} =& -\frac{e^{i\alpha}}{2\pi\beta v_F} [e^{2i\alpha}]^n
\end{align}$$

Plugging this in, we get that 

$$\begin{align}
\mathcal{G}_L(x,\tau;x',\tau') =& 2\pi i\sum_{n=0}^{\infty} -\frac{e^{i\alpha}}{2\pi\beta v_F}(e^{2i\alpha})^n, \quad x - x' < 0 \\
=& -\frac{ie^{i\alpha}}{\beta v_F} \sum_{n=0}^{\infty} (e^{2i\alpha})^n, \quad x - x' < 0 \\
=& -\frac{ie^{i\alpha}}{\beta v_F} \frac{1}{1-e^{2i\alpha}}, \quad x - x' < 0 \\
=& \frac{i}{\beta v_F} \frac{1}{e^{i\alpha}-e^{-i\alpha}}, \quad x - x' < 0 \\
=& \frac{1}{2\beta v_F} \frac{1}{\sin\alpha}, \quad x - x' < 0 \\
=& -\frac{1}{2\pi} \frac{1}{\frac{\beta v_F}{\pi}\sin\frac{\pi}{\beta v_F}(z-z')} \quad x - x' > 0
\end{align}$$

Thus we find the same result as for the \\(x - x' > 0\\) case. Now, we move on to the \\(\tau - \tau' < 0\\) case. This changes the nature of the Heaviside function.

</li> 
 <li> Now we have \\(\tau - \tau' < 0\\). Thus the Green function 

$$\begin{align}
\mathcal{G}_L(x,\tau;x',\tau') =& -\frac{1}{L}\sum_{k}e^{k[i(x-x')+v_F(\tau-\tau')]}\left(\theta(\tau-\tau')- \frac{1}{1+e^{-\beta v_Fk}}\right)
\end{align}$$

simplifies instead to 

$$\begin{align}
\mathcal{G}_L(x,\tau;x',\tau') =& \frac{1}{L}\sum_{k}e^{k[i(x-x')+v_F(\tau-\tau')]}\frac{1}{1+e^{-\beta v_Fk}}
\end{align}$$

Changing the sum to an integral, we find that 

$$\begin{align}
\mathcal{G}_L(x,\tau;x',\tau') =& \int_{-\infty}^\infty e^{k[i(x-x')+v_F(\tau-\tau')]}\frac{1}{1+e^{-\beta v_Fk}} \frac{\d k}{2\pi}
\end{align}$$

We see that if \\(k\to+\infty\\), then the numerator helps us converge, whereas if \\(k\to-\infty\\), the denominator helps us converge. Thus this sanity check works out! Next, we assume \\(x-x' > 0\\). This means we can close the contour in the lower-half plane. We find 

$$\begin{align}
\mathcal{G}_L(x,\tau;x',\tau') =& -2\pi i\sum_{n = -1}^{-\infty} \Res_{z=i\pi(2n+1)/v_F\beta} e^{k[i(x-x')+v_F(\tau-\tau')]}\frac{1}{2\pi(1+e^{-\beta v_Fk})} 
\end{align}$$

There is a leading minus sign because the contour must go clockwise. This residue gives 

$$\begin{align}
\Res_{z=i\pi(2n+1)/v_F\beta} e^{k[i(x-x')+v_F(\tau-\tau')]}\frac{1}{2\pi(1+e^{-\beta v_Fk})} =& \frac{e^{i\alpha}}{2\pi\beta v_F} e^{2ni\alpha}
\end{align}$$

where this time \\(\alpha = \frac{\pi}{v_F\beta}[i(x-x') + v_F(\tau-\tau')]\\). Now, we find that 

$$\begin{align}
\mathcal{G}_L(x,\tau;x',\tau') =& -2\pi i\sum_{n = -1}^{-\infty} \frac{e^{i\alpha}}{2\pi\beta v_F}e^{2ni\alpha} \\
=& -\frac{ie^{i\alpha}}{\beta v_F} \sum_{n=1}^\infty (e^{-2i\alpha})^n \\
=& -\frac{1}{2\beta v_F\sin\alpha} \\
=& -\frac{1}{2\pi}\frac{1}{\frac{\beta v_F}{\pi}\sin\frac{\pi}{\beta v_F}(z-z')}
\end{align}$$

</li> 
 <li> This should give us the same answer.

\end{subparts}

Therefore, the Green function is given by 

$$\begin{align}
\mathcal{G}_L(x,\tau;x',\tau') =& -\frac{1}{2\pi}\frac{1}{\frac{\beta v_F}{\pi}\sin\frac{\pi}{\beta v_F}(z-z')}
\end{align}$$

For any \\(x,x'\\) and \\(-\beta < \tau - \tau' < \beta\\).

\end{solution}

\end{questions}

