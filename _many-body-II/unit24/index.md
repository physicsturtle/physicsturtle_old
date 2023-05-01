---
layout: lesson
title: Lecture March 22
dept: physics
course: many-body-II
unit: unit24
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 24
---
\\(\theta(\Lambda - k_4)\\) transforms in a complicated way under \\(\Lambda\to \Lambda/s\\), \\(k = \tilde{k}/s\\) because \\(\textbf{K}_1 + \textbf{K}_2 - \textbf{K}_3 = (K_F + k_1)\hat{\Omega}_1 + (k_F + k_2)\hat{\Omega}_2 - (k_F + k_3)\hat{\Omega}_3\\) where \\(\hat{\Omega}_i = (\cos\theta_0,\sin\theta_i)\\), \\(k_i = \tilde{k}_i/s\\).

$$$$\begin{align}\textbf{K}_i\to (K_F + \frac{\tilde{k}_i}{s})\hat{\Omega}_i\end{align}$$$$

so we do not get a simple rescaling of \\(\textbf{K}_i\\) or, therefore of \\(k_4\\). 

Fortunately, \\(\theta(\Lambda - |k_4|)\\) also implies that 

$$$$\begin{align}\int d\theta_1 d\theta_2 d\theta_3\end{align}$$$$

integrals can be greatly simplified - for most choices of these 3 angles, \\(\theta(\Lambda - |k_4|) = 0\\). 

There are 2 possibilities when \\(\Lambda \ll k_F\\).

<ul>
	<li> \\(\textbf{K}_1 = \textbf{K}_3\\), \\(\textbf{K}_2 = \textbf{K}_4\\) or \\(\textbf{K}_1 = \textbf{K}_4\\) or \\(\textbf{K}_2 = \textbf{K}_3\\). these 2 correspond to the same term in \\(S_\text{eff}\\) due to Fermi statistics. \\(\textbf{K}_1\\) and \\(\textbf{K}_2\\) are arbitrary vectors of length approximately \\(k_F\\).
	</li> 
 <li> \\(\textbf{K}_1 = - \textbf{K}_2\\), \\(\textbf{K}_3 = -\textbf{K}_4\\) , where \\(\textbf{K}_1\\) and \\(\textbf{K}_3\\) arbitrary.
\end{itemize}

$$$$\begin{align}
\delta S_F = \int \prod_{i=1}^4\frac{dk_i d\omega_i}{(2\pi)^2} (2\pi)^2 \delta(\omega_1 + \omega_2 - \omega_3 - \omega_4)\delta(k_1 + k_2 - k_3 - k_4)\int_0^{2\pi}\frac{d\theta_1}{2\pi}\int_0^{2\pi}\frac{d\theta}{2\pi}\bar{\psi}(k_4,\omega_4,\theta_1)\bar{\psi}(k_3,\omega_3,\theta_1 + \theta)\psi(k_2,\omega_2,\theta_1)\psi(k_1,\omega_1,\theta_1 + \theta) F(\theta)
\end{align}$$$$

Note: \\(F\\) only depends on \\(\theta\\) - angle between \\(\textbf{K}_1\\) and \\(\textbf{K}_2\\), not angle of \\(\textbf{K}_1\\) itself - due to rotational invariance. 

Forward scattering process - indeed find \\(k_S\\) the same 

\\(F(\theta)\\) is an arbitrary coupling function.

Infinite number of coupling constants, 

$$$$\begin{align}F(\theta) = \sum_m F_m e^{im\theta}\end{align}$$$$

could be additional terms with this angle dependence but with powers of \\(k_i\\), \\(\omega_i\\) - all irrelevant as before. 

$$$$\begin{align}\delta S = \int \prod_{i=1}^4 \frac{dk_i d\omega_i}{(2\pi)^2} (2\pi)^2\delta(\omega_1 + \omega_2 - \omega_3 - \omega_4) \delta(k_1 + k_2 - k_3 - k_4)\bar{\psi}(k_4,\omega_4,-\theta_3)\bar{\psi}(k_3,\omega_3,\theta_3)\psi(k_2,\omega_2,-\theta_1)\psi(k_1,\omega_1,\theta_1)V(\theta_1-\theta_3)\end{align}$$$$

again angle \\(\theta_1 - \theta_3\\) enters \\(V\\) - not \\(\theta_1 + \theta_3\\) - rotation \\(\theta_1\\) \\(\theta_3\\) by same angle has no effect on \\(V\\) by rotational invariance. 

A second infinite set of coupling constants

as an example, we can calculate \\(F(\theta)\\) and \\(V(\theta)\\) explicitly for nearest neighbour tight binding model at low density where Fermi surface is approximately circular. 

$$$$\begin{align}\epsilon(\k) = -2t(\cos k_x a + \cos k_y a) - \mu - 4t-\mu + ta^2\textbf{K}^2\end{align}$$$$

\\(ta^2 k_F^2 \approx 4t + \mu\\) so

$$$$\begin{align}\delta H \propto \sum_{\textbf{R},\textbf{e}}\psi^\dagger_\textbf{R}\psi_\textbf{R}\psi^\dagger_{\textbf{R} + \textbf{e}}\psi_{\textbf{R} + \textbf{e}}\end{align}$$$$

whereby \\(\textbf{R}\\) is a bravais lattice vector and \\(\textbf{e} = \pm a(1,0), \pm a(0,1)\\). 

$$$$\begin{align}\delta H \propto \sum_{\textbf{R},e} \psi^\dagger_{\textbf{R}}\psi^\dagger_{\textbf{R} + \textbf{e}}\psi_{\textbf{R}}\psi_{\textbf{R} + \textbf{e}} = \frac{1}{4}\sum_{\textbf{R},\textbf{e}}[\psi^\dagger_{\textbf{R}}\psi^\dagger_{\textbf{R} + \textbf{e}} - \psi^\dagger_{\textbf{R} + \textbf{e}}\psi^\dagger_{\textbf{R}}][\psi_{\textbf{R}}\psi_{\textbf{R} + \textbf{e}}- \psi_{\textbf{R} + \textbf{e}}\psi_{\textbf{R}}]\end{align}$$$$ 

$$$$\begin{align}\propto \int \prod_{i=1}^4 d^2 K_i \delta^2(k_! + k_2 - k_3 - k_4)\bar{\psi}^\dagger_4 \psi^\dagger_3 \psi_2 \psi_1 \sum_{\textbf{e}}(e^{-i\textbf{K}_3\cdot\textbf{e}} - e^{-i\textbf{K}_4 \cdot\textbf{e}})(e^{i\textbf{K}_2\cdot\textbf{e}}- e^{i\textbf{K}_1\cdot\textbf{e}})\end{align}$$$$

Note: antisymmetric under \\(\textbf{K}_3 \to \textbf{K}_4\\) and \\(\textbf{K}_1 \to \textbf{K}_2\\).  Thus, this is equal to 

$$$$\begin{align}=2(\cos(K_2 - K_3)a + \cos(K_1 - K_4)a - \cos(K_3 - K_1)a - \cos(K_4 - K_2)a) + x(-)y\end{align}$$$$

expand for small \\(k_F\\):

$$$$\begin{align}\propto (\textbf{K}_2 - \textbf{K}_3)^2 + (\textbf{K}_1 - \textbf{K}_4)^2 - (\textbf{K}_3 - \textbf{K}_1)^2 - (\textbf{K}_2 - \textbf{K}_4)^2 \propto \textbf{K}_2\cdot\textbf{K}_3 + \textbf{K}_1\cdot\textbf{K}_4 - \textbf{K}_3 \cdot\textbf{K}_1 - \textbf{K}_2\cdot\textbf{K}_4 = (\textbf{K}_2-\textbf{K}_1)\cdot(\textbf{K}_4 - \textbf{K}_3)\end{align}$$$$

Could have written this down by inspection because odd under \\(\textbf{K}_1 \leftrightarrow \textbf{K}_2\\) and \\(\textbf{K}_3\leftrightarrow \textbf{K}_4\\) and quadratic.

For \\(F\\) term \\(\textbf{K}_3 = \textbf{K}_1\\) and \\(\textbf{K}_4 = \textbf{K}_2\\), we have 

$$$$\begin{align}F\propto (\textbf{K}_1 - \textbf{K}_2)^2 \propto (\hat{\Omega}_1 - \hat{\Omega}_2)^2 = 2(1-\cos \theta_{12})\end{align}$$$$

\\(V\\) term: \\(\textbf{K}_1 = - \textbf{K}_2\\), \\(\textbf{K}_3 = -\textbf{K}_4\\), 

$$$$\begin{align}V\propto \textbf{K}_1\cdot\textbf{K}_3 \propto \cos\theta_{13}\end{align}$$$$

insert pictures here

