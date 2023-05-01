---
layout: lesson
title: Taking the Thermodynamic Limit
dept: physics
course: many-body-II
unit: unit16
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 16
---
For our lattice model, we want to write it in momentum space and with integrals of momentum instead of sums over momentum. This will make it easier to actually perform the renormalization group analysis later on. The thermodynamic limit, we recall, makes the Brillouin zone continuous, despite the limits of \\(-\pi/a\\) to \\(\pi/a\\) staying the same. In the thermodynamic limit, the number of lattice sites becomes infinite, so it is not as useful to use the following Fourier transform:

$$\chat_j = \frac{1}{\sqrt{N}}\sum_k e^{ikR_j} \chat_k, \quad \chat_k = \frac{1}{\sqrt{N}}\sum_j e^{-ikR_j} \chat_j$$

Here, \\(N\\) is the number of primitive unit cells in the Bravais lattice, and, as we just said, it is infinite! In order to properly deal with this, we should take the thermodynamic limit at the very end of the calculation. The kinetic term becomes 

$$H_0 = \sum_k \epsilon_k \chat^\dagger_k \chat_k$$

where \\(\epsilon_k = -2t\cos(ka)\\) is the dispersion relation. In the thermodynamic limit, we change the sum to an integral:

$$H_0 = \int_{-\pi/a}^{\pi/a} \epsilon_k \chat^\dagger_k \chat_k\frac{\V \d k}{2\pi}$$

We then define \\(\psihat_k = \sqrt{\V}\chat_k\\). Then, the Hamiltonian is rewritten as 

$$H_0 = \int_{-\pi/a}^{\pi/a} \epsilon_k \psihat^\dagger_k \psihat_k\frac{\d k}{2\pi}$$

So now, \\(\epsilon_k\\) still has units of energy, but we remember that now \\(\psi_k\\) has units of \\(\sqrt{\V}\\). In summary, we have defined a new Fourier transform by using the relations for the Fourier transform of \\(\chat_j\\) and \\(\psihat_k\\) to get:

$$\begin{align}
\chat_j =& \frac{1}{\sqrt{N}}\sum_k e^{ikR_j} \chat_k \\
=& \frac{1}{\sqrt{N}}\int_{-\pi/a}^{\pi/a} e^{ikR_j} \chat_k \frac{\V\d k}{2\pi} \\
=& \sqrt{\frac{\V}{N}} \int_{-\pi/a}^{\pi/a} e^{ikR_j} \left(\sqrt{\V}\chat_k\right) \frac{\d k}{2\pi} \\
=& \sqrt{a} \int_{-\pi/a}^{\pi/a} e^{ikR_j} \psihat_k \frac{\d k}{2\pi}
\end{align}$$





 For the interaction term, we also Fourier transform the operators to get that 

$$H_\text{int} = \frac{U}{N}\sum_{k_1,k_2,k_3,k_4}\delta_{k_1+k_2,k_3+k_4} \chat^\dagger_{k_1} \chat^\dagger_{k_2} \chat_{k_3} \chat_{k_4}$$


For \\(U=0\\), or for constructing perturbation theory in \\(U\\), we Fourier transform \\(\psi_j\\) as



where \\(k\\) runs over the first Brillouin zone, and \\(N\\) is the number of primitive unit cells in the real space lattice.

$$$$\begin{align}
\psihat_j = \sqrt{a}\int_{-\pi/a}^{\pi/a}e^{iKR_j}\psihat(K)\frac{dK}{2\pi}
\end{align}$$$$

where \\(R_j = ja\\), and \\(a\\) is the lattice spacing. In moving to the infinite size limit, we take the Brillouin zone to be the continuum. This means that the 

\\(K\\) integral over Brillouin zone only \\(\psihat(k)\\) normalized as in Shankar, 

$$$$\begin{align}
\{\psihat(K), \psihat^\dagger(K')\} = 2\pi\delta(K-K')
\end{align}$$$$

$$$$\begin{align}
\{\psihat_j, \psihat^\dagger_{j'}\} = \delta_{j,j'}
\end{align}$$$$

$$$$\begin{align}
H_ 0 =\int_{-\pi/a}^{\pi/a}\psihat^\dagger(K)\psihat(K)\epsilon(K)\frac{dK}{2\pi}
\end{align}$$$$

$$$$\begin{align}
\epsilon(K) = -2t\cos(K) - \mu
\end{align}$$$$

Insert picture here! Because we are in 1 dimension, there are only two fermi points, \\(\pm k_F\\), not a Fermi surface. The model is therefore much simpler. We will integrate out Fourier modes far from Fermi points in RG. After some initial stages of RG, the remaining states are 2 narrow bands near \\(\pm k_F\\) with width \\(\Lambda\\). Thus \\(\Lambda\\) will serve as the momentum cutoff. 

Insert picture here

Low energy (\\(|\epsilon(K)|\\) small) modes have wave vectors \\(K = k_F + k\\) (right moving) or \\(K = -k_F + k\\) (left moving). Note that left vs. right moving is defined simply by 

with \\(|k|\ll k_F\sim \pi/2a\\).

Let \\(\psi_R(k) = \psi(k_F + k)\\), \\(\psi_L(k) = \psi(-k_F + k)\\)

Right and left-moving fields

$$$$\begin{align}
\psi_j = e^{iK_F ja}\int_{-\Lambda}^\Lambda\psi_R(k)e^{ikja}\frac{dk}{2\pi} + e^{-ik_Fja}\int_{-\Lambda}^\Lambda e^{-ikja}\psi_L(k)\frac{dk}{2\pi} = e^{iK_Fja}\psi_R(ja) + e^{-iK_Fja}\psi_L(ja) 
\end{align}$$$$

\\(\psi_R(x)\\) and \\(\psi_L(x)\\) vary slowly on lattice scale. 

Note: Shankar uses nonstandard notation, \\(\psi_L(k)\to \psi_L(-k)\\) for small \\(\Lambda\\), we can linearize dispersion relation 

$$$$\begin{align}
\epsilon(k_F + k) = v_Fk,\qquad \epsilon(-k_F + k) = -v_Fk
\end{align}$$$$


