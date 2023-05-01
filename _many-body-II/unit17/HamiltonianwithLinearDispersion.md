---
layout: lesson
title: Hamiltonian with Linear Dispersion
dept: physics
course: many-body-II
unit: unit17
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 17
---
We start by deriving a Hamiltonian with a linear dispersion. The first step is to consider a free fermion tight-binding model:

$$H_0 = -t\sum_{\langle i,j \rangle} (\chat^\dagger_{i\sigma} \chat_{j\sigma} + \hc) - \mu\sum_{i\sigma} \chat^\dagger_{i\sigma} \chat_{i\sigma}$$

After applying the Fourier transforms (here \\(k\\) runs over the first Brillouin zone)

$$\chat_{i\sigma} = \frac{1}{\sqrt{N}}\sum_k e^{ikx} \chat_{k\sigma}, \quad \chat^\dagger_{i\sigma} = \frac{1}{\sqrt{N}}\sum_k e^{-ikx} \chat^\dagger_{k\sigma}$$

then the Hamiltonian can be rewritten as 

$$H_0 = \sum_{k\sigma} \xi_k \chat^\dagger_{k\sigma} \chat_{k\sigma}$$

where \\(\xi_k = -2t\cos(ka) - \mu\\). The low-energy excitations occur around \\(k\\) for which \\(\xi_k \approx 0\\). If we set \\(\mu = 0\\) (half-filling), then \\(\xi_k = 0\\) at \\(k = \pm k_F\\), where \\(k_F = \pi/2a\\). We linearize the dispersion around these two points and write:

$$\begin{align}
\xi^\pm_k =& \xi_{\pm k_F} + (k\mp k_F)(\partial_k\xi_k)(\pm k_F) \\
=& \pm 2at(k\mp k_F)
\end{align}$$

We define \\(\textbf{v}_F = \frac{1}{\hbar}(\nabla_k\xi_k)(k_F) = 2at\\) (we set \\(\hbar = 1\\)), which here gives us 

$$\begin{align}
\xi^\pm_k =& \pm v_F(k\mp k_F) 
\end{align}$$

Although we initially started with the sums over \\(k\\) being over the first Brillouin zone, we instead let \\(k\\) now be unbounded, and also define left and right movers. The left movers have dispersion \\(\xi^-_k\\), and the right movers have dispersion \\(\xi^+_k\\). Thus the Hamiltonian becomes 

$$\begin{align}
H_0 =& \sum_{k\sigma}v_F \left((k-k_F)\chat^\dagger_{kR\sigma} \chat_{kR\sigma} - (k+k_F)\chat^\dagger_{kL\sigma} \chat_{kL\sigma}\right) \\
=& v_F\sum_{k\sigma} \left(k\chat^\dagger_{k-k_F,R\sigma} \chat_{k-k_FR\sigma} - k\chat^\dagger_{k+k_F,L\sigma} \chat_{k+k_F,L\sigma}\right)
\end{align}$$

Now, we redefine the operators \\(\chat_{k-k_F,R\sigma} = \psihat_{kR\sigma}\\) and \\(\chat_{k+k_F,L\sigma} = \psihat_{kL\sigma}\\) to get the Hamiltonian 

$$\begin{align}
H_0 =& v_F\sum_{k\sigma} \left(k\psihat^\dagger_{kR\sigma} \psihat_{kR\sigma} - k\psihat^\dagger_{kL\sigma} \psihat_{kL\sigma}\right)
\end{align}$$

We emphasize again that the sums over \\(k\\) are over \\(k=-\infty\\) to \\(\infty\\). This means that we have taken the continuum limit. 



















We consider the free fermion Hamiltonian

$$H = \sum_{\alpha=1}^M iv_F\int_{-L/2}^{L/2} :\psihat^\dagger_\alpha(x) \partial_x \psihat_\alpha(x): \d x$$

