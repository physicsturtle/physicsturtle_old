---
layout: lesson
title: 1 loop RG in $D = 2,3$
dept: physics
course: many-body-II
unit: unit25
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 25
---
``Tadpole diagram" contribute a \\((\omega,k,\theta)\\) independent term to self-energy 

corresponds to a shift in chemical potential

$$$$\begin{align}\delta S = \delta\mu\int\bar{\psi}\psi\end{align}$$$$

would shift density

we add a counter-term to \\(\mu\\) to keep density of interest

This is not important at this stage, but will come up again when we consider interaction energy of excited state

Renormalization of interactions

we get same 3 diagrams as in \\(\D=1\\). 

insert diagrams here

Note:we set \\(\omega = 0\\) amd \\(k=0\\) on all external lines, in order toe calculate renormalization of marginal couplings only, so all \\(|\textbf{k}_i| = k_F\\)

2 types of choices for directions of \\(\textbf{k}_i\\)

\\(F\\) or \\(V\\) interactions

Renormalization of \\(F\\): choose \\(\textbf{K}_1 = \textbf{K}_3\\), \\(\textbf{K}_2 = \textbf{K}_4\\) (up to a rotation of \\(\textbf{K}_3\\), \\(\textbf{K}_4\\) around \\(\textbf{K}_1 + \textbf{K}_2\\) by \\(\phi_{12;34}\\) in \\(\D=3\\)).

Recall that internal momenta (\\(\textbf{K}\\) and \\(\textbf{K} + \textbf{K}_1 - \textbf{K}_3\\) in ZS diagram) must be in \\(>\\) momentum region, \\(\Lambda - d\Lambda < |k| <\Lambda\\) where \\(K = k_F + k\\).

In particular, \\(k \not=0\\).

In most ccases, these diagrams are proportional to \\(d\Lambda^2\\), so \\(\beta\\) function vanishes. (defined by \\(\lim_{d\Lambda\to 0}\frac{dF}{d\Lambda}\\))

Consider for example ZS': \\(\textbf{K}_1 - \textbf{K}_4 = \textbf{K}_1 - \textbf{K}_2\\) is generally a large momentum of \\(O(k_F)\\).

SEe diagram!

The same story for BCS diagram since \\(\textbf{K}_1 + \textbf{K}_2\\) is generally large for \\(F\\) term. 

What about ZS?

In \\(\D=2\\), \\(\textbf{K}_1 = \textbf{K}_3\\) for \\(F\\) term so we don't get \\((d\Lambda)^2\\) suppression.

However, it gives zero for anothe reason. This is the same as in \\(\D=1\\).

$$$$\begin{align}\int_{-\infty}^\infty \frac{d\omega}{(i\omega - vk)^2} = 0\end{align}$$$$

Here it is importnat htat \\(k\not=0\\)

even if we gave \\(|\textbf{K}_1-\textbf{K}_3|\\) as a small value much less than \\(\Lambda\\), \\(|\textbf{K} + \textbf{K}_1 - \textbf{K}_3| - k_F\\) will have same sign as \\(|\textbf{K}| - k_F\\) so \\(\omega\\) integral vanishes.

In \\(\D=3\\), generally \\(|\textbf{K}_1 - \textbf{K}_3|\\) is again large, so we get \\((d\Lambda)^2\\) factor so

$$$$\begin{align}\Lambda\frac{dF}{d\Lambda}(Z_{13},\phi_{12;34} = 0 to O(F^2))\end{align}$$$$

Renormalization of \\(V\\):

Same diagrams, but now \\(\textbf{K}_1 + \textbf{K}_2 = 0\\)

\\(|\textbf{K}_1 - \textbf{K}_3|\\) and \\(|\textbf{K}_! - \textbf{K}_4|\\) are generally large in this case, giving \\((d\Lambda)^2\\) factor in ZS, ZS'

but BCS diagram given no \\(d\Lambda\\) factor since internal momenta are \\(\textbf{K}\\) and \\(-\textbf{K}\\)

Furthermore, \\(\omega\\) integral is nonzero.

$$$$\begin{align}\int_{-\infty}^\infty\frac{d\omega}{(i\omega - vk)(-i\omega - vk)} = \int_{-\infty}^\infty\frac{d\omega}{\omega^2 + v^2k^2} = \frac{\pi}{v|k|}\end{align}$$$$

like in \\(\D=1\\) but there is no second diagram to cancel it! Letting \\(\hat{\Omega}\\) be the direction of internal momentum \\(\textbf{K}\\), we get \\(V(\hat{\Omega}_1\cdot\hat{\Omega})\\) at lower interaction vertex and \\(V(\hat{\Omega}\cdot\hat{\Omega}_3)\\) at upper vertex.

$$$$\begin{align}\Lambda\frac{d}{d\Lambda}V(\theta_1 - \theta_3) = \frac{1}{8\pi^2}\int_0^{2\pi}V(\theta_1 - \theta)V(\theta - \theta_3)\frac{d\theta}{2\pi}\end{align}$$$$

in \\(\D=2\\), or proprtional to

$$$$\begin{align}\int V(\hat{\Omega}_1\cdot\hat{\Omega})V(\hat{\Omega}\cdot\hat{\Omega}_3)d^2\hat{\Omega}\end{align}$$$$

in \\(D=3\\). Expanding in circular (or spherical) harmonics, \\(V(\theta) = \sum_\ell e^{-i\ell\theta}V_\ell\\), so

$$$$\begin{align}\Lambda\frac{dV_\ell}{d\Lambda} = \frac{V_\ell^2}{4\pi}\end{align}$$$$

like RG for Kondo coupling - marginally relevant if \\(V_\ell < 0\\) corresponding to attractive interactions. \\(V_\ell\\) becomes large, even if initially small, at an exponentially small energy scale, \\(\Delta\sim De^{-4\pi/V_\ell}\\)

Otherwise, it renormalizes to 0. In general, some \\(V_\ell\\) might be positive, some negative.

Angular momenetum channel for which \\(V\\) gets large gives symmetry of copper pair wave function in BCS theory. \\(s\\)-wave, \\(p\\)-wave, \\(d\\)-wave etc.

Actually, a mroe careful analysis, keeping effects of higher orderin \\(\L/k_F\\), shows that \\(V_\ell\\) at very large \\(\ell\\) always become 

$$$$\begin{align}\Lambda\frac{dV_\ell}{d\Lambda} = \frac{V_\ell^2}{4\pi}\end{align}$$$$

\\(C\\) \\(V(\theta = \pi)^2/\ell^4\\), \\(C\\) dependso n \\(K_F/\Lambda\\) attractice and eventually renormalize to infinity.

THis is Kohn-Luttinger instability. But, in cases where this happens for large \\(\ell\\), corresponding \\(\Delta\\) is extremely small, and there is a large range of energies much less than \\(E_F\\) where we may ignore \\(V\\) and use Fermi liquid theory

Some metals show no sign of superconductivity down to lowest measured temperature

most metals that do exhibit superconductivity have \\(\Delta \sim T_C \leq 30 K\\) and Fermi liquid theory seems to apply for \\(T_c \ll E \ll E_F\\). 

Also true of \\(He^3\\) \\(E_F = 5K\\) \\(T_C = 1mK\\). 

High \\(T_c\\) cuprates appear ot be an exception - \\(E_F small\\), \\(T_K\\) large.

Superconductivity in most metals is believed to be due to electron-phonon interaction, which we have not discussed. 

This typically leads to \\(s\\)-wave superconductivity - below energy scale \\(\omega_\D\\). We could use this electron-only approach with \\(V_0\\) attractive.

