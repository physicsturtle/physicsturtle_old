---
layout: lesson
title: Boson Fields -- definition and properties
dept: physics
course: many-body-II
unit: unit17
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 17
---
We will define the position space boson fields as the Fourier transform of the previously defined particle-hole creation/annihilation operators and derive some useful properties. The boson fields are defined as the following Fourier-type transform (this is not a typical Fourier transform; there are some additional factors)

$$$$\begin{align}
\varphihat_\alpha(x) = \sum_{q > 0} \frac{1}{\sqrt{n_q}}e^{iqx}\varphihat_{q\alpha} e^{-aq/2},\quad \varphihat^\dagger_\alpha(x) = \sum_{q>0} \frac{1}{\sqrt{n_q}}e^{-iqx} \varphihat^\dagger_{q\alpha} e^{-aq/2}
\end{align}$$$$

The commutator between these two fields are 

$$$$\begin{align}
[\varphihat_\alpha(x), \varphihat^\dagger_{\alpha'}(x')] = -\delta_{\alpha\alpha'}\log\left(1-e^{i\frac{2\pi}{L}(x-x'+ia)}\right)
\end{align}$$$$

which simplifies, in the \\(L\to\infty\\) limit, to 

$$$$\begin{align}
[\varphihat_\alpha(x), \varphihat^\dagger_{\alpha'}(x')] = -\delta_{\alpha\alpha'}\log\left(i\frac{2\pi}{L}(x'-x-ia) \right)
\end{align}$$$$

We can also compute the derivative of the commutator: 

$$\begin{align}
\partial_{x'} [\phihat_\alpha(x), \phihat_{\alpha'}(x')] =& -2\pi i\delta_{\alpha\alpha'}\delta(x'-x)
\end{align}$$



Note that the inverse Fourier transform is given by 

$$$$\begin{align}
\varphihat_{q\alpha} = \sqrt{n_q} e^{\eta q/2} \int_{-L/2}^{L/2} \varphihat_\alpha(x) e^{-iqx} \d x,\quad \varphihat^\dagger_{q\alpha} = \sqrt{n_q}e^{\eta q/2} \int_{-L/2}^{L/2} \varphihat^\dagger_\alpha(x) e^{iqx} \d x
\end{align}$$$$

The Hermitian combination of the two is simply given by \\(\phihat_\alpha(x) = \varphihat_\alpha(x) + \varphihat^\dagger_\alpha(x)\\). The factor \\(\eta\\) is an infinitesimally small mathematical regularization parameter which isn ecessary to regularize ultraviolet divergent momentum sums. It will be taken to zero from above at the end of calculations. We can interpret \\(\eta\\) as approximately the lattice spacing. 

Let's write the fermion density in the boson language. This gives us 

$$\begin{align}
\rhohat_\alpha(x) =& :\psihat^\dagger_\alpha(x) \psihat_\alpha(x): \\
=& \frac{1}{L}\sum_{kk'} e^{-ikx}e^{ik'x} :\psihat^\dagger_{k\alpha} \psihat_{k'\alpha}: \\
=& \frac{1}{L}\sum_{kq} e^{iqx} : \psihat^\dagger_{k-q,\alpha} \psihat_{k\alpha}: \\
=& \frac{1}{L}\sum_k\left(\sum_{q>0} e^{iqx} : \psihat^\dagger_{k-q,\alpha} \psihat_{k\alpha}: + \sum_{q<0} e^{iqx} : \psihat^\dagger_{k-q,\alpha} \psihat_{k\alpha}: + : \psihat^\dagger_{k\alpha} \psihat_{k\alpha}:\right) \\
=& \frac{1}{L}\sum_k\left(\sum_{q>0} e^{iqx} : \psihat^\dagger_{k-q,\alpha} \psihat_{k\alpha}: + \sum_{q>0} e^{-iqx} : \psihat^\dagger_{k+q,\alpha} \psihat_{k\alpha}: + : \psihat^\dagger_{k\alpha} \psihat_{k\alpha}:\right) \\
=& \frac{1}{L}\sum_{q>0}\left(ie^{iqx}\sqrt{n_q}\varphihat_{q\alpha} -i e^{-iqx}\sqrt{n_q}\varphihat^\dagger_{q\alpha} \right) + \frac{1}{L}\sum_k : \varphihat^\dagger_{k\alpha} \varphihat_{k\alpha}:
\end{align}$$

We note that \\(:\bhat_{q\alpha}: = \bhat_{q\alpha}\\) because the operator destroys a single particle-hole pair, and so \\(\bra{\textbf{N}}_0 \bhat_{q\alpha} \ket{\textbf{N}}_0 = 0\\). A similar argument applies to the bosonic creation operator. To proceed, we note that \\(2\pi/L = q/n_q\\). Making this substitution gives us 

$$\begin{align}
\rhohat_\alpha(x) =& \frac{1}{2\pi} \sum_{q>0}\left(ie^{iqx}\frac{q}{\sqrt{n_q}} \bhat_{q\alpha} -i e^{-iqx}\frac{q}{\sqrt{n_q}} \bhat^\dagger_{q\alpha} \right) + \frac{1}{L}\Nhat_\alpha
\end{align}$$

We then recognize the first term as (almost) the derivative of the field \\(\phihat_\alpha(x)\\). To make the identification complete, we let \\(\eta\to0\\) in the formula for \\(\phihat_\alpha\\) and get 

$$\begin{align}
\rhohat_\alpha(x) = \frac{1}{2\pi} \partial_x\phihat_\alpha(x)\big|_{\eta\to 0^+} + \frac{1}{L}\Nhat_\alpha
\end{align}$$

This is a very important formula in bosonization. It is useful for example in formulating a solution of the 1D Hubbard model (IS THIS TRUE???). 


