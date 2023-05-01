---
layout: lesson
title: Massless Dirac Fermion
dept: physics
course: many-body-II
unit: unit19
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 19
---
We start by considering an example. In this example, we have spinless fermions moving in 1 dimension. The wave function has two components and is given by \\(\psi = \begin{pmatrix} \psi_+ \\ \psi_- \end{pmatrix}\\) and the Schrödinger equation is

$$$$\begin{align}
i\frac{\partial\psi}{\partial t} = \Hhat\psi
\end{align}$$$$

where the Hamiltonian is 

$$$$\begin{align}
\Hhat = \alpha\hat{p} + \beta m.
\end{align}$$$$

Here, \\(\alpha = \sigma_3\\), \\(\beta = \sigma_2\\), where \\(\sigma_i\\) are the standard Pauli matrices. We start by considering the \\(m=0\\) case. Then, 

$$$$\begin{align}
H\psi = -i\partial_x\begin{pmatrix} 1 & 0 \\ 0 & -1 \end{pmatrix}\psi
\end{align}$$$$

where \\(\psi = \begin{pmatrix} \psi_+ \\ \psi_- \end{pmatrix}\\) is a 2-component spinor. Here, we have decoupled components of \\(\psi\\) because there are two separate differential equations: one for \\(\psi_+\\) and one for \\(\psi_-\\). We call \\(\psi_+\\) a \textit{right mover} and \\(\psi_-\\) a \textit{left mover}. These are so named because the velocity \\(v = \partial E/\partial k > 0\\) for the right movers and is negative for left movers. We then second quantize the Hamiltonian to get 

$$\begin{align}
\Hhat =& \int \begin{pmatrix} \psihat^\dagger_+ & \psihat^\dagger_- \end{pmatrix} (-i\partial_x)\begin{pmatrix}1 & 0 \\ 0 & -1 \end{pmatrix} \begin{pmatrix} \psihat_+ \\ \psihat_- \end{pmatrix} \d x \\
=& \int \left(\psihat^\dagger_+(x)(-i\partial_x)\psihat_+(x) + \psihat^\dagger_-(x)(i\partial_x)\psihat_-(x) \right) \d x
\end{align}$$

To diagonalize the Hamiltonian, we introduce Fourier transforms 

$$$$\begin{align}
\psihat_{\p}m(x) = \int_{-\infty}^\infty e^{ikx} \psihat_{\p}m(k) e^{-\frac{1}{2}\eta|k|} \frac{\d k}{2\pi}, \quad \psihat^\dagger_{\p}m(x) = \int_{-\infty}^\infty e^{-ikx} \psihat^\dagger_{\p}m(k) e^{-\frac{1}{2}\eta|k|} \frac{\d k}{2\pi}
\end{align}$$$$

where \\(\eta\to 0^+\\). If we plug these representations into the Hamiltonian, using \\(\int_{-\infty}^\infty e^{i(k-k')x} \d x = 2\pi \delta(k-k')\\), we find that 

$$$$\begin{align}
\Hhat = \int_{-\infty}^\infty \psihat^\dagger_+(k)\psihat_+(k) \frac{k\d k}{2\pi} + \int_{-\infty}^\infty \psihat^\dagger_-(k) \psihat_-(k) \frac{(-k)\d k}{2\pi}
\end{align}$$$$

The Hamiltonian is now diagonal, and we can see that the right movers have energy \\(E = k\\), and the left movers have energy \\(E = -k\\). This means that we can simply find the ground state. The ground state should have all right-movers with \\(k < 0\\) be occupied states, and all the left-movers with \\(k>0\\) be occupied states. Thus

$$$$\begin{align}
\ket{\text{GS}} = \prod_{k_+<0}\prod_{k_->0} \psihat^\dagger_+(k_+)\psihat^\dagger_-(k_-)\ket{0}
\end{align}$$$$

The Heisenberg time evolution of \\(\psi_{\p}m(x)\\) is calculated by 

$$$$\begin{align}
\psihat_{\p}m(x,t) = e^{i\Hhat t}\psihat_{\p}m(x) e^{-i\Hhat t} = \psihat_{\p}m(x\mp t)
\end{align}$$$$

so the Heisenberg operator is related to the Schrödinger operator by a simple translation in time. Now, we compute the ground state correlation function. We do this in a few steps. First, 

$$$$\begin{align}
G_+(k,k') = \langle \psihat_+(k)\psihat^\dagger_+(k')\rangle = \theta(k')\langle\psihat_+(k)\psihat^\dagger_+(k')\rangle
\end{align}$$$$

The Heaviside function arises because the ground state only has right movers with negative \\(k\\). Therefore, if \\(k' < 0\\) and we act with \\(\psihat^\dagger_+(k')\\) on the ground state, we should get 0 because we cannot create a double occupation. Next, we can evaluate this by noting that 

$$$$\begin{align}
G_+(k,k') = 2\pi\theta(k')\delta(k-k')
\end{align}$$$$

The correlation function can then be computed in real space as 

$$\begin{align}
G_+(x,x') =& \langle \psi_+(x) \psi^\dagger_+(x') \rangle \\
=& \int_{-\infty}^\infty\int_{-\infty}^\infty e^{ikx}e^{-ik'x'}\langle\psihat_+(k)\psihat^\dagger_+(k')\rangle e^{-\frac{1}{2}\eta|k|}e^{-\frac{1}{2}\eta|k'|} \frac{\d k}{2\pi}\frac{\d k'}{2\pi} \\
=& \int_{-\infty}^\infty\int_{-\infty}^\infty e^{ikx}e^{-ik'x'} 2\pi\theta(k')\delta(k-k') e^{-\frac{1}{2}\eta|k|}e^{-\frac{1}{2}\eta|k'|} \frac{\d k}{2\pi}\frac{\d k'}{2\pi} \\
=& \int_{-\infty}^\infty e^{ik'(x-x')} \theta(k') e^{-\eta|k'|} \frac{\d k'}{2\pi} \\
=& \int_{0}^\infty e^{ik'(x-x')}e^{-\eta k'} \frac{\d k'}{2\pi} \\
=& \frac{1}{2\pi}\frac{i}{x-x'+i\eta}
\end{align}$$


