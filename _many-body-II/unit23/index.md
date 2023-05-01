---
layout: lesson
title: RG for Interacting Fermions in $d = 2$ and $d = 3$
dept: physics
course: many-body-II
unit: unit23
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 23
---
In this final section, we will treat interacting fermions in 2 or 3 spatial dimensions. This will lead us to an RG treatment of Fermi liquid theory. In contrast to the RG approach that you have probably studied in a statistical field theory course, complications here arise due to the Fermi surface. 

We will begin with the simplest case: \\(d=2\\), and circular Fermi surface. We will also consider \textit{spinless fermions}. The dispersion (minus chemical potential) for the spherical Fermi surface in 2 spatial dimensions is given by

$$$$\begin{align}
\xi(\textbf{K}) = \frac{\hbar^2 \K^2}{2m} - \mu
\end{align}$$$$

and so the Hamiltonian is given by 

$$$$\begin{align}
\Hhat = \sum_{\k} \xi_{\k} \chat^\dagger_{\k}\chat_{\k} + \frac{1}{N}\sum_{\k_1\k_2\k_3\k_4}U(\k_1,\k_2,\k_3,\k_4) \chat^\dagger_{\k_1}\chat^\dagger_{\k_2} \chat_{\k_3}\chat_{\k_4}\delta_{\k_1+\k_2,\k_3+\k_4}
\end{align}$$$$

We then define the noninteracting and interacting parts as 

$$$$\begin{align}
\Hhat_0 = \sum_{\k} \xi_{\k} \chat^\dagger_{\k}\chat_{\k}, \quad H_\text{int} = \frac{1}{N}\sum_{\k_1\k_2\k_3\k_4}U(\k_1,\k_2,\k_3,\k_4) \chat^\dagger_{\k_1}\chat^\dagger_{\k_2} \chat_{\k_3}\chat_{\k_4}\delta_{\k_1+\k_2,\k_3+\k_4}
\end{align}$$$$

We note that the special case of \\(U(\k_1,\k_2,\k_3,\k_4) = U\\) is the Hubbard model with on-site repulsion only. We now move to the thermodynamic limit by changing sums over \\(\k\\) to integrals over \\(\k\\). Then the noninteracting part becomes 

$$$$\begin{align}
\Hhat_0 = \V\int\xi_{\k} \chat^\dagger_{\k} \chat_{\k} \frac{\d^d\k}{(2\pi)^d}
\end{align}$$$$

For the interacting part, the delta function becomes \\(\delta_{\k_1+\k_2,\k_3+\k_4} \to \frac{(2\pi)^d}{\V}\delta^{(d)}(\k_1+\k_2-\k_3-\k_4)\\)

$$\begin{align}
\Hhat_\text{int} =& \frac{1}{N}\int U(\k_1,\k_2,\k_3)\chat^\dagger_{\k_1}\chat^\dagger_{\k_2} \chat_{\k_3}\chat_{\k_4} \frac{(2\pi)^d}{\V}\delta^{(d)}(\k_1+\k_2-\k_3-\k_4) \frac{\V\d^d\k_1}{(2\pi)^d} \frac{\V\d^d\k_2}{(2\pi)^d} \frac{\V\d^d\k_3}{(2\pi)^d} \frac{\V\d^d\k_4}{(2\pi)^d} \\
=& \frac{1}{N}\int U(\k_1,\k_2,\k_3)\chat^\dagger_{\k_1}\chat^\dagger_{\k_2} \chat_{\k_3}\chat_{\k_4} (2\pi)^d\delta^{(d)}(\k_1+\k_2-\k_3-\k_4) \frac{\V\d^d\k_1}{(2\pi)^d} \frac{\V\d^d\k_2}{(2\pi)^d} \frac{\V\d^d\k_3}{(2\pi)^d} \frac{\d^d\k_4}{(2\pi)^d} \\
=& \V^2v\int U(\k_1,\k_2,\k_3)\chat^\dagger_{\k_1}\chat^\dagger_{\k_2} \chat_{\k_3}\chat_{\k_4} (2\pi)^d\delta^{(d)}(\k_1+\k_2-\k_3-\k_4) \frac{\d^d\k_1}{(2\pi)^d} \frac{\d^d\k_2}{(2\pi)^d} \frac{\d^d\k_3}{(2\pi)^d} \frac{\d^d\k_4}{(2\pi)^d} \\
\end{align}$$

where \\(v = \V/N\\) is the volume of a primitive unit cell of the real space lattice. We now rescale these creation and annihilation operators, and also the coupling by sending 

$$\psihat_{\k} = \sqrt{\V}\chat_{\k},\quad \psihat^\dagger_{\k} = \sqrt{\V}\chat^\dagger_{\k},\quad u = vU.$$

Thus the Hamiltonian terms become 

$$\begin{align}
\Hhat_0 =& \int\xi_{\k} \psihat^\dagger_{\k} \psihat_{\k} \frac{\d^d\k}{(2\pi)^d} \\
\Hhat_\text{int} =& \int u(\k_1,\k_2,\k_3,\k_4)\psihat^\dagger_{\k_1}\psihat^\dagger_{\k_2} \psihat_{\k_3}\psihat_{\k_4} (2\pi)^d\delta^{(d)}(\k_1+\k_2-\k_3-\k_4) \frac{\d^d\k_1}{(2\pi)^d} \frac{\d^d\k_2}{(2\pi)^d} \frac{\d^d\k_3}{(2\pi)^d} \frac{\d^d\k_4}{(2\pi)^d}
\end{align}$$

The low energy states of this theory will have a small \\(\k\\) relative to the Fermi surface. We then take each of our \\(\k\\) vectors above and redefine it \\(\k \mapsto \k + \k_F\\). This means that we are now measuring \\(\k\\) with respect to the Fermi surface, and, to look at the low-energy theory, we neglect all \\(\k\\) which satisfy \\(|\k| > \Lambda\\), where \\(\Lambda\\) is a high-energy momentum cutoff; the only remaining states are within \\(\Lambda\\) of the Fermi surface. We therefore split up each \\(\k\\) into its magnitude and direction components. Thus \\(\k = k(\cos\theta,\sin\theta)\\) in 2 dimensions (which is the focus of this section). We can therefore also label each of our states by a magnitude of a wave vector and a direction. 

%Here, we treat \\(\K\\) as the wavevector of the electron, and then we will measure deviations from the Fermi wavevector \\(\k_F\\) as \\(\k = \K-\k_F\\). After initial stages of RG, we have only a narrow band of states remaining around Fermi ``surface" i.e. Fermi circle of radius \\(k_F\\). The only remaining states are within \\(\Lambda\\) of the Fermi surface. That is, if we define \\(\k = \K-\k_F\\), obeying \\(-\Lambda < |\k| < \Lambda\\). \\(\epsilon = v_F k\\) (drop \\(F\\) subscript).

The free effective action is therefore (now specializing to 2 dimensions)

$$\begin{align}
S_0 =& \int_0^\beta\int \bar{\psi}_{\k\tau}(\partial_\tau + \xi_{\k})\psi_{\k\tau} \frac{\d^2\k}{(2\pi)^2} \d\tau \\
=& \frac{1}{\beta}\sum_{i\omega} \int_{-\Lambda}^\Lambda \int_0^{2\pi} \bar{\psi}_{k\theta,i\omega}(-i\omega + \xi_{\k})\psi_{k\theta,i\omega} \frac{\d\theta}{2\pi}\frac{\d k}{2\pi}
\end{align}$$

where we used the Fourier transforms 

$$$$\begin{align}
\psi_{\k\tau} = \frac{1}{\beta}\sum_{i\omega} e^{-i\omega\tau} \psi_{\k,i\omega}, \quad \bar{\psi}_{\k\tau} = \frac{1}{\beta}\sum_{i\omega} e^{i\omega\tau} \bar{\psi}_{\k,i\omega}
\end{align}$$$$

Lastly, we change the Matsubara sum to an integral and linearize the dispersion relation (this works since we are close to the Fermi surface) and find

$$\begin{align}
S_0 =& \int_{-\infty}^\infty \int_{-\Lambda}^\Lambda \int_0^{2\pi} \bar{\psi}_{k\theta\omega}(-i\omega + v_Fk)\psi_{k\theta\omega} \frac{\d\theta}{2\pi}\frac{\d k}{2\pi}\frac{\d\omega}{2\pi}
\end{align}$$

where \\(v_F\\) is the Fermi velocity. This noninteracting action is invariant under the same RG transformation as in \\(d=1\\). Namely, the transformation

CONTINUE CHECKING HERE! NEED TO WRITE THE RG TRANSFORMATION IN SOME SENSIBLE WAY

$$$$\begin{align}
\begin{cases}
\Lambda \to \Lambda/s \\
k \to \tilde{k}/s \\
\omega \to 
\end{cases}
\end{align}$$$$

\\(\Lambda\to\Lambda/s\\) to \\(k = \tilde{k}/s\\), \\(|\tilde{k}| <\Lambda\\), \\(\omega = \tilde{\omega}/s\\), \\(\tilde = s^{3/2}\psi'\\). 

This resembles an infinite number of 1-dimensional relativistic fermion fields labelled by angle \\(\theta\\) on Fermi surface. 

Note: this looks like nothing like a relativistic fermion model in \\(d=2\\).

We only get that in special cases like graphene with unusual dispersion relation.

Instead this is like a complicated 1D relativistic model.

General quartic interaction term in low energy Hamiltonian (only keeping states near Fermi circle)

Can be written

$$$$\begin{align}
\delta S_4 = \frac{1}{(2!)^2}\int_{k\omega\theta} \bar{\psi}(4)\bar{\psi}(3)\psi(2)\si(1)u(4,3,2,1)
\end{align}$$$$

where \\(\psi(1) = \psi(\omega_1,k_1,\theta_1)\\), etc. And, after eliminating \\(\int \d\omega_4 \d k_4\\) integral with energy and momentum conserving delta function, 

$$$$\begin{align}\int_{k\omega\theta} = \prod_{i=1}^3 \int_{-\infty}^\infty\int_{-\Lambda}^\Lambda \int_0^{2\pi}\theta(\Lambda - |k_4|) \frac{d\theta_i}{2\pi} \frac{dk_i}{2\pi} \frac{d\omega_i}{2\pi}\end{align}$$$$

here \\(k_4 = |\textbf{K}_1 + \textbf{K}_2 - \textbf{K}_3| - k_F\\). 

i.e. \\(\int dk_4\\) is only restricted to \\(|k_4| < \Lambda\\), so \\(\delta(\textbf{K}_1 + \textbf{K}_2 - \textbf{K}_3 - \textbf{K}_4)\\) is only nonzero when \\(|\textbf{K}_1 + \textbf{K}_2 - \textbf{K}_3|\\) is in the narrow range 

\section{Lecture March 22}
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

