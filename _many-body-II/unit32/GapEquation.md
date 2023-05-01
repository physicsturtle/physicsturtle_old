---
layout: lesson
title: Gap Equation
dept: physics
course: many-body-II
unit: unit32
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 32
---

In this section, we will expand on the treatment of superconducitivity from the attractive Hubbard model that we discuss earlier. This will allow us to develop a mean-field description of the superconducting phase, and find the resulting quasiparticles. This will allow us to determine the thermodynamic properties of the phase. The mean-field Hamiltonian corresponding to the uniform order parameter introduced in the study of pairing in the Fermi Hubbard model is given by 

$$\Hhat = \sum_{\k} \xi_{\k} \chat^\dagger_{\k\sigma} \chat_{\k\sigma} + $$

which means that we can eventually rewrite the Hamiltonian as 

$$H = \sum_{\k} \begin{pmatrix} \chat^\dagger_{\k\uparrow} & \chat_{-\k\downarrow} \end{pmatrix} \begin{pmatrix} \xi_{\k} & \Delta \\ \Delta^{*} & -\xi_{\k} \end{pmatrix} \begin{pmatrix} \chat_{\k\uparrow} \\ \chat^\dagger_{-\k\downarrow} \end{pmatrix} + \sum_{\k} \xi_{\k} + \frac{N_s}{U}|\Delta|^2$$

and we diagonalize the matrix in the middle by rewriting it in terms of \\(E_{\p}m(\k) = \pm\sqrt{\xi_{\k}^2 + |\Delta|^2}\\) and 

$$u_{\k} = \sqrt{\frac{1}{2} + \frac{\xi_{\k}}{2\sqrt{\xi_{\k}^2 + |\Delta|^2}}},\quad v_{\k} = \sqrt{\frac{1}{2} - \frac{\xi_{\k}}{2\sqrt{\xi_{\k}^2 + |\Delta|^2}}}.$$

Then the matrix becomes (letting \\(\Delta = e^{i\varphi}|\Delta|\\))

$$\begin{pmatrix} \xi_{\k} & \Delta \\ \Delta^{*} & -\xi_{\k} \end{pmatrix} = \begin{pmatrix} e^{i\varphi}u_{\k} & -e^{i\varphi} v_{\k} \\ v_{\k} & u_{\k} \end{pmatrix} \begin{pmatrix} E_+(\k) & 0 \\ 0 & E_-(\k) \end{pmatrix} \begin{pmatrix} e^{-i\varphi} u_{\k} & v_{\k} \\ -e^{-i\varphi} v_{\k} & u_{\k} \end{pmatrix}$$

Thus we define new operators 

$$\gammahat_{\k} = e^{-i\varphi}u_{\k} c_{\k\uparrow} + v_{\k} \chat^\dagger_{-\k\downarrow},\quad \etahat_{\k} = -e^{-i\varphi} v_{\k} \chat_{\k\uparrow} + u_{\k} \chat^\dagger_{-\k\downarrow}$$

Thus the Hamiltonian is written as 

$$H = \sum_{\k} \left(E_+(\k)\gamma^\dagger_{\k} \gammahat_{\k} + E_-(\k) \etahat^\dagger_{\k} \etahat_{\k}\right)$$





In the mean-field solution, the order parameter is given by 

$$\Delta = -\frac{U}{\beta N_s}\left<\chat_{-\k\downarrow} \chat_{\k\uparrow}\right>$$

which we will evaluate by noting that 

$$\begin{pmatrix} \chat_{\k\uparrow} \\ \chat^\dagger_{-\k\downarrow} \end{pmatrix} = \begin{pmatrix} e^{i\varphi}u_{\k} & -e^{i\varphi} v_{\k} \\ v_{\k} & u_{\k} \end{pmatrix} \begin{pmatrix} \gammahat_{\k} \\ \etahat_{\k} \end{pmatrix}$$

Thus, 

$$\begin{align}
\left<c_{-k\downarrow} c_{k\uparrow}\right> =& e^{i\varphi}\left<(v_{\k} \bar{\gamma}_k + u_{\k} \bar{\eta}_k)(u_{\k} \gamma_k - v_{\k} \eta_k)\right> \\
=& e^{i\varphi} u_{\k} v_{\k}\left[ \left<\bar{\gamma}_k \gamma_k\right> - \left<\bar{\eta}_k \eta_k\right>\right] \\
=& e^{i\varphi} u_{\k} v_{\k}\left[ \frac{1}{ik_0 - E_+(\k)} - \frac{1}{ik_0 - E_-(\k)}\right] \\
\end{align}$$

Plugging this in to our MFT equation, 

$$\Delta = -\frac{U}{\beta N_s} \sum_k e^{i\varphi} u_{\k} v_{\k}\left[ \frac{1}{ik_0 - E_+(\k)} - \frac{1}{ik_0 - E_-(\k)}\right]$$

and after cancelling out the phase from both sides and recalling \\(e^{i\varphi}|\Delta| = \Delta\\), also summing over the Matsubara frequency, we find that

$$|\Delta| = -\frac{U}{N_s} \sum_{\k} u_{\k} v_{\k}\left[ n_F(E_+(\k) - n_F(E_-(\k))\right]$$

Now, we substitute in the forms of \\(u_{\k}\\) and \\(v_{\k}\\), so that 

$$|\Delta| = -\frac{U}{N_s} \sum_{\k} \frac{|\Delta|}{E_+(\k) - E_-(\k)}\left[ n_F(E_+(\k)) - n_F(E_-(\k))\right]$$

Now changing the sum over \\(\k\\) to an integral, 

$$\frac{1}{U} = -\frac{\V}{2N_s}\int \frac{n_F(E_+(\k)) - n_F(E_-(\k))}{\sqrt{\xi_{\k}^2 + |\Delta|^2}}\frac{\d^3\k}{(2\pi)^3}$$

Assuming that the density of states is roughly constant, and as \\(T\to 0\\), the first Fermi-Dirac function goes to zero. Thus 

$$\begin{align}
\frac{1}{U} =& \frac{\V \rho}{2N_s}\int_{-D}^D \frac{1}{\sqrt{\xi^2 + |\Delta|^2}}\d\xi \\
=& \tilde{\rho}\int_0^D \frac{1}{\sqrt{\xi^2 + |\Delta|^2}}\d\xi \\
=& \tilde{\rho}\arcsinh\left(\frac{\xi}{|\Delta|}\right)\bigg|_0^D \\
=& \tilde{\rho}\arcsinh\left(\frac{D}{|\Delta|}\right)
\end{align}$$

Since \\(D/|\Delta|\\) is large, we approximate \\(\arcsinh(x) \sim \log(2x)\\) for large \\(x\\). Thus 
and solving this tells us that 

$$\frac{1}{U} = \tilde{\rho}\log\left(\frac{2D}{|\Delta|}\right)$$

and solving this tells us that 

$$\Delta\sim 2D e^{-1/\tilde{\rho} U}$$

We can take a ratio between \\(k_BT_c\\) and \\(2\Delta\\), which will cancel out the cutoff. 

$$\begin{align}
\frac{2 \Delta(0)}{k_BT_c} =& \frac{4D e^{-1/\tilde{\rho}U}}{2D e^\gamma e^{-1/\tilde{\rho}U}/\pi} \\
=& \frac{2\pi}{e^\gamma} \\
=& 3.53
\end{align}$$

This can be measured experimentally! It is clear how to measure \\(T_c\\), and the gap can be measured by looking at the spectra of emitted electrons at \\(T\to 0\\) for a uniform wave vector. ELABORATE!

