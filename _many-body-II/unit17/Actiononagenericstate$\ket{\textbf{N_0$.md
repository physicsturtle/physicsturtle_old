---
layout: lesson
title: Action on a generic state $\ket{\textbf{N_0$ 
dept: physics
course: many-body-II
unit: unit17
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 17
---
We now establish the bosonic coherent states. The commutation relations for the boson and fermion operators are 

$$$$\begin{align}
[\varphihat_{q\alpha'}, \psihat_{\alpha}(x)] = \delta_{\alpha\alpha'}a_q(x) \psihat_\alpha,\quad [\varphihat^\dagger_{q\alpha'}, \psihat_\alpha(x)] = \delta_{\alpha\alpha'}a_q(x) \psihat_\alpha(x)
\end{align}$$$$

whereby \\(a_q(x) = -\frac{i}{\sqrt{n_q}}e^{-iqx}\\). This tells us that, since the state \\(\ket{\textbf{N}}_0\\) (which we recall has \\(\textbf{N}\\)-many particles, but no particle-hole excitations) satisfies \\(\bhat_{q\alpha}\ket{\textbf{N}}_0 = 0\\), we have that 

$$\begin{align}
\bhat_{q\alpha'}\psihat_\alpha(x)\ket{\textbf{N}}_0 =& (\psihat_\alpha(x)\bhat_{q\alpha'} + \delta_{\alpha\alpha'}a_q(x)\psihat_\alpha(x))\ket{\textbf{N}}_0 \\
=& \delta_{\alpha\alpha'}a_q(x)\psihat_\alpha(x)\ket{\textbf{N}}_0
\end{align}$$

This tells us that the state \\(\psihat_\alpha(x)\ket{\textbf{N}}_0\\) is a coherent state of the \\(\varphihat_{q\alpha}\\) operator; it is however still annihilated by \\(\varphihat_{q\alpha'}\\). We recall that any bosonic coherent state can be written as 

$$$$\begin{align}
\psihat_\alpha(x)\ket{\textbf{N}}_0 \propto e^{\sum_q a_q(x) \varphihat^\dagger_{q\alpha}} \Fhat_\alpha \ket{\textbf{N}}_0
\end{align}$$$$

which is equivalently 

$$$$\begin{align}
\psihat_\alpha(x)\ket{\textbf{N}}_0 \propto e^{-i\varphi^\dagger_\alpha(x)} \Fhat_\alpha \ket{\textbf{N}}_0
\end{align}$$$$

We introduce the Klein factor because \\(\psihat_\alpha(x)\\) removes one \\(\alpha\\)-particle, but there is still a proportionality constant which must be worked out. In order to work out the constant, we write an equality.

$$$$\begin{align}
\psihat_\alpha(x)\ket{\textbf{N}}_0 = e^{-i\varphi^\dagger_\alpha(x)} \Fhat_\alpha \hat{\lambda}_\alpha(x) \ket{\textbf{N}}_0
\end{align}$$$$

Then, we bring ourselves back into the same particle number sector by acting with \\(\Fhat^\dagger_\alpha\\) and then take the expectation value in the state \\(\ket{\textbf{N}}_0\\) to get 

$$$$\begin{align}
\bra{\textbf{N}}_0 \Fhat^\dagger_\alpha\psihat_\alpha(x)\ket{\textbf{N}}_0 = \bra{\textbf{N}}_0 \Fhat^\dagger_\alpha e^{-i\varphi^\dagger_\alpha(x)} \Fhat_\alpha \hat{\lambda}_\alpha(x) \ket{\textbf{N}}_0
\end{align}$$$$

We evaluate this in two different ways. First, we note that the Klein factors on the RHS cancel out because they commute with \\(e^{-i\varphihat^\dagger_\alpha(x)}\\), and \\(\Fhat^\dagger_\alpha \Fhat_\alpha = 1\\), so we find 

$$$$\begin{align}
\bra{\textbf{N}}_0 \Fhat^\dagger_\alpha\psihat_\alpha(x)\ket{\textbf{N}}_0 = \bra{\textbf{N}}_0 e^{-i\varphihat^\dagger_\alpha(x)} \hat{\lambda}_\alpha(x) \ket{\textbf{N}}_0
\end{align}$$$$

The expression simplifies again since \\(\varphihat_\alpha(x)\ket{\textbf{N}}_0 = 0\\) so we also have \\(\bra{\textbf{N}}_0 \varphihat^\dagger_\alpha(x) = 0\\). Thus, 

$$$$\begin{align}
\bra{\textbf{N}}_0 \Fhat^\dagger_\alpha\psihat_\alpha(x)\ket{\textbf{N}}_0 = \bra{\textbf{N}}_0\hat{\lambda}_\alpha(x) \ket{\textbf{N}}_0 = \lambda_\alpha(x)
\end{align}$$$$

We now work out the quantity in a different way. The other way is by using the Fourier expansion of \\(\psihat_\alpha(x)\\), which gives 

$$$$\begin{align}
\bra{\textbf{N}}_0 \Fhat^\dagger_\alpha\psihat_\alpha(x)\ket{\textbf{N}}_0 = \frac{1}{\sqrt{L}}\sum_{k=-\infty}^\infty \bra{\textbf{N}}_0 \Fhat^\dagger_\alpha e^{ikx} \psihat_{k\alpha} \ket{\textbf{N}}_0
\end{align}$$$$

Since the Klein factor is acting from the right on the bra \\(\ket{\textbf{N}}_0\\), its action is simply that of a creation operator, and we find 

$$$$\begin{align}
\bra{\textbf{N}}_0 \Fhat^\dagger_\alpha\psihat_\alpha(x)\ket{\textbf{N}}_0 = \frac{1}{\sqrt{L}}\sum_{k=-\infty}^\infty \bra{\textbf{N}}_0 \psihat^\dagger_{K\alpha} e^{ikx} \psihat_{k\alpha} \ket{\textbf{N}}_0
\end{align}$$$$

where this particular value of \\(K\\) is such that \\(K = \frac{2\pi}{L}(N_\alpha-\delta_b/2)\\). Then, we find that 

$$$$\begin{align}
\bra{\textbf{N}}_0 \Fhat^\dagger_\alpha\psihat_\alpha(x)\ket{\textbf{N}}_0 = \frac{1}{\sqrt{L}}\sum_{k=-\infty}^\infty e^{ikx} \delta_{k,K} = \frac{1}{\sqrt{L}} e^{i\frac{2\pi}{L}(N_\alpha - \delta_b/2)x}
\end{align}$$$$

Matching the two expressions, we find that 

$$$$\begin{align}
\lambda_\alpha(x) = \frac{1}{\sqrt{L}} e^{i\frac{2\pi}{L}(N_\alpha - \delta_b/2)x}
\end{align}$$$$

This means that, in operator form, we have 

$$$$\begin{align}
\hat{\lambda}_\alpha(x) = \frac{1}{\sqrt{L}} e^{i\frac{2\pi}{L}(\Nhat_\alpha - \delta_b/2)x}
\end{align}$$$$

We wish to bosonize this free fermion Hamiltonian. 


