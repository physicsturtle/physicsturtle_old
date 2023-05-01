---
layout: lesson
title: Conduction electron Green function for Kondo effect
dept: physics
course: many-body-II
unit: unit13
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 13
---
Calculation of Electron Green function:

We will average over positions of dilute random array of impurities - restores translation invariance and makes \\(G\\) vanish unless \\(\k = \k'\\).

This is similar to our calculation of \\(\delta\lambda\\) except that now we sum over impurity state and over all momenta in action, not just in strip \\(\D' < \epsilon_{\k} < \D\\) as for RG. 

Note: no \\(O(\lambda)\\) contribution due to \\(\tr \textbf{S} = 0\\). 

It is convenient to work in position-frequency space. 

$$$$\begin{align}\mathcal{G}_{\alpha\beta}(\r,\r',i\omega_n) = -\left<\psi_\alpha(\r,\omega_n)\bar{\psi}_\beta(\r',\omega_n)\right>\end{align}$$$$

where \\(\left<\right>\\) includes trace over impurity spin states.

$$$$\begin{align}S_\text{int} = -J\int_{-\infty}^\infty \bar{\psi}(\boldsymbol{\sigma},\tau)\frac{\boldsymbol{\sigma}}{2}\psi(\boldsymbol{\sigma},\tau)\cdot\textbf{S}(\tau)d\tau\end{align}$$$$

$$$$\begin{align}\delta\mathcal{G}_{\alpha\beta} = -\frac{J^2}{2!}\sum_{ab}\left<\psi(\bar{\psi}\frac{\sigma^a}{2}\psi)(\bar{\sigma}\frac{\sigma^b}{2}\psi)\bar{\sigma}\right>\left<S^a S^b\right>\end{align}$$$$

where \\(\left<S^a S^b\right> = \frac{1}{4}\delta^{ab}\\) no \\(T\\) dependence. 

insert feynman diagram picture.


We only need to consider a single diagram, which has a symmetry factor of 2.

We use the formula

$$$$\begin{align}\sum_{ab}(\frac{\sigma^a}{2}\frac{\sigma^b}{2})_{\alpha\beta}\frac{1}{4}\delta^{ab} = \frac{3}{16}\delta_{ab}\end{align}$$$$

Using

$$$$\begin{align}
\mathcal{G}^{(0)}(\r-\r',i\omega_n) = -\left<\psi(\r,\omega_n)\bar{\psi}(\r',\omega_n)\right>
\end{align}$$$$

we obtain

$$$$\begin{align}
\delta\mathcal{G}_{\alpha\beta}(\r,\r',i\omega_n) = \frac{3}{16}\delta_{ab}J^2\mathcal{G}^{(0)}(\boldsymbol{\sigma},i\omega_n)\mathcal{G}^{(0)}(\boldsymbol{\sigma},i\omega_n)\mathcal{G}^{(0)}(-\r',i\omega_n)
\end{align}$$$$

Frequency is conserved since no \\(\tau\\) dependence arises from impurity spin operator in this case.

$$$$\begin{align}
\mathcal{G}_{0}(\boldsymbol{\sigma},i\omega_n) = \frac{1}{V}\sum_{\k} \frac{1}{i\omega_n - \epsilon_{\k}}
\end{align}$$$$

Return to evaluating this later. It is convenient to write

$$$$\begin{align}
\delta\mathcal{G}(\r,\r',i\omega_n) = \mathcal{G}_{0}(\r,i\omega_n)T(i\omega_n)\mathcal{G}^{0}(-\r',i\omega_n)
\end{align}$$$$

suppressing \\(\delta_{\alpha\beta}\\) where 

$$$$\begin{align}
T(i\omega_n) = \frac{3}{16}J^2 \frac{1}{V}\sum_{\k} \frac{1}{i\omega_n - \omega_{\k}}
\end{align}$$$$

Note: \\(T\\) is a function of frequency only, not position (or momentum)

It is called the \\(T\\)-matrix and is a generalization of the \\(T\\) matrix in ordinary potential scattering (\\(S = I + iT\\))

Suppose impurity was not at origin, but at arbitrary location \\(\textbf{R}\\). Then

$$$$\begin{align}
\delta\mathcal{G}(\r,\r',i\omega_n) = \mathcal{G}_{0}(\r-\textbf{R},i\omega_n)T(i\omega_n)\mathcal{G}^{(0)}(\textbf{R} - \r',i\omega_n)
\end{align}$$$$

due to the diagram.

Now suppose we have many impurities at locations \\(\textbf{R}_1\\), \\(\textbf{R}_2\\), etc. Then, 

$$$$\begin{align}
H_\text{int} = J\sum_{i=1}^{N_\text{imp}}\psi^\dagger(\textbf{R}_i)\frac{\boldsymbol{\sigma}}{2}\psi(\textbf{R}_i)\cdot\textbf{S}_i
\end{align}$$$$

dominant diagrams at small \\(J\\) and small \\(n_\text{imp}\\) are (diagrams here)

$$$$\begin{align}= \mathcal{G}^{(0)}(\r-\textbf{R}_{i_1})T\mathcal{G}^{(0)}(\textbf{R}_{i_1}-\textbf{R}_{i_2})T\mathcal{G}^{(0)}(\textbf{R}_{i_2} - \textbf{R}_{i_3})T\cdots T\mathcal{G}^{(0)}(\textbf{R}_{i_n} - \r')\end{align}$$$$

where \\(n \in \NN_0\\). All \\(\mathcal{G}^{(0)}\\) and \\(T\\)'s are at same frequency, \\(i\omega_n\\). Now, sum over \\(i_1,i_2,\dots,i_n\\) from \\(1\\) to \\(N_\text{imp}\\). 

In dilute limit, we can ignore idagrams where same impurity occurs more than once in a diagram. Thus, 

$$$$\begin{align}\sum_{i_p=1}^{N_\text{imp}}\to n_\text{imp}\int d^3\textbf{R}_\textbf{p}\end{align}$$$$

Since impurity locations are random and sicne we will also be integrating over \\(\r\\) and \\(\r'\\) to get resistivity. 

The \\(m\\)th order correction is

$$$$\begin{align}[n_\text{imp}T(i\omega_n)]^n\int d^3\textbf{R}_1 \cdots d^3\textbf{R}_m\mathcal{G}^{(0)}(\r-\textbf{R}_1)\mathcal{G}^{(0)}(\textbf{R}_1-\textbf{R}_2)\cdots\mathcal{G}^{(0)}(\textbf{R}_{m-1}-\textbf{R}_m)\mathcal{G}^{(0)}(\textbf{R}_m - \r')\end{align}$$$$

Note: translation invariance is restored by averaging over impurity locations in \\(\k\\) space. 

$$$$\begin{align}\mathcal{G}(\k,\omega) = (n_\text{imp}T(i\omega_n))^m[\mathcal{G}^{(0)}(\k,i\omega_n)]^{m+1}\end{align}$$$$

sum the series:

$$\begin{align}
\mathcal{G}(\k,i\omega_n) =& \sum_{m=0}^\infty [\mathcal{G}^{(0)}(\k,i\omega_n)]^{m+1}[n_\text{imp}T(i\omega_n)]^m\\
=& \frac{G^{(0)}}{1-\mathcal{G}^{(0)}n_\text{imp}T}\\
=& \frac{1}{(\mathcal{G}^{(0)})^{-1} - n_\text{imp}T}\\
=& \frac{1}{i\omega_n - \epsilon_{\k} - n_\text{imp}T(i\omega_n)}
\end{align}$$

This has the form of a self-energy.

$$$$\begin{align}
\mathcal{G} = \frac{1}{i\omega_n - \epsilon_{\k} -\Sigma(i\omega_n,\k)}
\end{align}$$$$

where self-energy depends on \\(i\omega_n\\) only, not \\(\k\\).

$$$$\begin{align}
\Sigma(\k,i\omega_n) = n_\text{imp}T(i\omega_n)
\end{align}$$$$

we actually want retarded Green function to define \\(\tau(\omega)\\) which appears in resistivity.

Are there other diagrams?

Correcting: (insert digrams here)

still give \\(\epsilon = n_\text{imp}T(i\omega_n)\\), but give corrections to \\(T(i\omega_n)\\) of higher order in \\(\lambda\\). Diagrams like:

insert digrams here

mix different impurities. now, sums over \\(i_1,i_2 = 1,\dots N_\text{imp}\\) can't be done independently - give corrections to sum of higher order in \\(n_\text{imp}\\) (virial expansion)

we ignore them in dilute limit

finally, let's evaluate \\(T(\omega)\\) to \\(O(\tau^2)\\)

$$$$\begin{align}\tau(\omega) = \frac{3}{16}\frac{J^2}{V}\sum_{\k} \frac{1}{\omega - \epsilon_{\k} + i\eta}\end{align}$$$$ 

(retarded green function)

\\(\Re T\\) just shifts Fermi energy a bit and leads to other unimportant correction. 

\\(\Im T\\) gives scattering rate

$$$$\begin{align}\Im T = -\frac{3}{16}J^2\pi\int \delta(\omega - \epsilon_{\k})\frac{d^3\k}{(2\pi)^3} = -\frac{3}{16}J^2\pi\nu(\omega) = -\frac{3}{16}J^2\pi\nu,\qquad \omega\to 0\end{align}$$$$

$$$$\begin{align}\Im \sum = -\frac{3}{16}\nu J^2\pi n_\text{imp} = -\frac{1}{2\tau}\end{align}$$$$

Note: has the correct sign (pole of \\(G_\text{ret}\\)) in negative half-plane. 

$$$$\begin{align}\frac{1}{\tau} = \frac{3}{8}\pi J^2\nu n_\text{imp}\end{align}$$$$

Plug into Kubo formula (or Boltzmann equation result from A\& M) 

$$$$\begin{align}\rho = \frac{3}{23^2 v_F^2 \nu}\frac{1}{\tau} = \frac{9\pi}{16 e^2 v_F^2} J^2 n_\text{imp}\end{align}$$$$

Explicit calculation to \\(O(J^3)\\) gives

$$$$\begin{align}\rho = \frac{9\pi}{16 e^2 v_F^2 \nu^2}(\lambda_0^2 + 2\lambda_0^3\log\frac{\D_0}{T} + \cdots ) = \frac{9\pi}{16 e^2 v_F^2 \nu^2}(\lambda(T)^2 + \cdots)\end{align}$$$$

i.e. we get RG improved result, as we expect \\(T\\) ?? scale at which to evaluate effective coupling correction in form ??

An infinite series of diagrams correspond to RG result.

$$$$\begin{align}\rho\propto \frac{n_\text{imp}}{\log^2 T/T_K},\qquad T\gg T_K\end{align}$$$$

we must go beyond RG improved perturbation theory to study \\(T\lesssim T_K\\). 

But first return to another issue.


