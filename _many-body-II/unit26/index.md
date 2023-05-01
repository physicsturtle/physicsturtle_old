---
layout: lesson
title: Lecture March 29
dept: physics
course: many-body-II
unit: unit26
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 26
---
Higher order \\(\beta\\) function. Most higher order diagrams have \\((d\Lambda)^2\\) factors for same reason as above. nly exceptions are ?? bubble. 

Bubbles for \\(F\\) all vanish in RG calculation due to 

$$$$\begin{align}\int_{-\infty}^\infty \frac{d\omega}{(i\omega - vk)^2} = 0\end{align}$$$$

Bubbles for \\(V\\) are non-vanishing. but they don't correspond to higher order terms in the \\(\beta\\) function - just the series that gives the leading ??

$$$$\begin{align}V_\ell(\Lambda) = \frac{V_\ell^0}{1+V_\ell^0\log(\Lambda_0/\Lambda)/4\pi} = \sum_{n=0}^\infty (-1)^n \left(\frac{V_\ell^0}{4\pi}\log\frac{\Lambda_0}{\Lambda}\right)^n\end{align}$$$$

So, we have exact \\(\beta\\) function in narrow band limit, \\(\Lambda \ll k_F\\)

Landau's fermi liquid theory corresponds to ?? the effects of the marginal \\(F\\) term and ignoring the \\(V\\) term.

Expected to be a good approximation over energy range where \\(V_\ell(\Lambda)\\)'s are small

In fact, ``forward-scattering" part of \\(F(Z_{12},\phi_{12;34})\\) - \\(F(Z_{12},0)\\) is much more important than \\(\phi_{12;34}\not=0\\) part. 

One way of seeing this is to calculate as Landau did, energy to add a low energy quasi particle to system when some are already present. 

i.e. interaction energy between low energy quasi particles

A convenient and elegant way to doing this is to calculate the self-energy of a quasi particle in the presence of a non-spherical Fermi surface which is deformed slightly due to the presence of particles and holes. 

i.e. \\(k_F\\) becomes a function of direction on the Fermi sphere. 

Let \\(k_F(\hat{\Omega}) = k_F + \sigma(\hat{\Omega})\\) following Shnkar.

We can make this the ground state by making the chemical potential direction-dependent on the Fermi surface - assume \\(|r(\hat{\Omega})| < \Lambda\\). Quadratic term is \\(\Hhat - \mu\hat{N}\\) is modified so

$$$$\begin{align}H_0' - \int_{-\Lambda}^\Lambda \frac{dk}{2\pi}\int \frac{d^2\hat{\Omega}}{4\pi}\psi^\dagger(V'(k-r(\hat{\Omega})) - \mu)\psi\end{align}$$$$

Note: \\(V'\\) is as renormalized velocity - it picks up a renormalization during reduction of cutoff to a small vaule. Doesn't renormalize in narrow band theory.

\\(\mu\\) is the chemical potential already present to keep Fermi surface at \\(k_F\\) in the presence of interacting term, proportional to \\(F\\). 

Using the \\(F\\) interaction, we can calculate the self-energy as a functio of \\(r(\hat{\Omega})\\)

To \\(O(F)\\) it comes from the ``tadpole diagram"

$$$$\begin{align}\int\bar{\psi}(4)\bar{\psi}(3)\psi(2)\psi(1) F(Z_{12},\phi_{12;34})\end{align}$$$$

\\(\left<\bar{\psi}(3)\psi(1)\right>\\) is only nonzero when \\(\textbf{K}_3 = \textbf{K}_1\\) so \\(\phi_{12;34} = 0\\) recall that, in general \\(\textbf{K}_3\\) is rotated from \\(\textbf{K}_1\\) nby angle \\(\phi_{12;34}\\) around \\(\textbf{K}_1 + \textbf{K}_2\\) axis. 

$$$$\begin{align}\epsilon'(k\hat{\Omega}) = V'(k - r(\hat{\Omega})) - \int F(\hat{\Omega}\cdot\hat{\Omega}',0)\frac{d\omega' dk'}{(2\pi)^4}\left(\frac{1}{i\omega' - v(k' - r\hat{\Omega})} - \frac{1}{i\omega - vk'}\right)\end{align}$$$$ 

second term is \\(O(F)\\) shifts in chemical potential, necessary so correction vanishes when \\(r =0\\). Ntoe that \\(k'\\) integral goes from

$$$$\begin{align}\int_{-\Lambda}^\Lambda\end{align}$$$$

not 

$$$$\begin{align}\int_{\Lambda - d\Lambda}^\Lambda + \int_{-\Lambda}^{-\Lambda + d\Lambda}\end{align}$$$$



$$$$\begin{align}
\int_{-\infty}^\infty (\frac{1}{i\omega' - v(k' - r(\hat{\Omega}))} - \frac{1}{i\omega - vk'}) = vr(\hat{\Omega}')\int_{-\infty}^\infty \frac{d\omega'/2\pi}{(i\omega' - v(k' - r(\hat{\Omega})))(i\omega - vk')}
\end{align}$$$$

This is only nonzero if \\(k'\\) and \\(k' - r(\hat{\Omega})\\) have opposite sign.

Because \\(k'\\) integral runs from \\(-\Lambda\\) to \\(\Lambda\\) and \\(|r(\hat{\Omega}')| < \Lambda\\) there will be a nonzero result after integrating over \\(k'\\).

\\(\omega\\) integral = \\(-\sgn(r(\hat{\Omega}'))\\) when \\(k'\\), \\(k'-r\\) have opposite sign.

e.g. if \\(r > 0\\), nonzero for \\(0 < k' < r\\)

\\(k\\) integral gives \\(r(\hat{\Omega}')\\)

So 

$$$$\begin{align}\epsilon(\hat{\Omega}) = vk + \int F(\hat{\Omega}\cdot\hat{\Omega}') r(\hat{\Omega}') \frac{d\hat{\Omega}'}{(2\pi)^3}\end{align}$$$$

second term represents interaction of quasi particle at \\(k\\) with other quasi particles corresponding to deformation of Fermi surface \\(r(\hat{\Omega}')\\).

Note:only involves \\(F(\hat{\Omega}\cdot\hat{\Omega}';0)\\)

we dropped \\(v' r(\hat{\Omega})\\) term in order to measure \\(\epsilon\\) with respect to original Hamiltonian \\(H\\) not \\(H'\\)

We may relate \\(r(\hat{\Omega})\\) to number of particles added per unit surface area in the Fermi surfaec. 

$$$$\begin{align}N = V\int^{k_F}\frac{d^3 k}{(2\pi)^3} = \frac{V}{(2\pi)^3}\int d^2\hat{\Omega}\int_0^{k_F + r(\Omega)} k^2 dk\end{align}$$$$

\\(N-N_0 = \frac{V}{(2\pi)^3}k_F^2\int d^2\Omega r(\hat{\Omega}) = \int d^2\Omega \delta r(\hat{\Omega})\\)

\\(\delta n(\hat{\Omega}) = \frac{V}{(2\pi)^3}k_F^2 r(\hat{\Omega})\\)

using this we can express energy in terms of the \\(\delta n\\)'s. GOing back to discrete sums over \\(\k\\) at finite volume, we can then write

$$$$\begin{align}E(\delta n) = \sum_{\textbf{K}}v' k\delta n(\textbf{K}) + \frac{1}{2V}\sum_{\textbf{K},\textbf{K}'}\delta n(\textbf{K}) \bar{F}(\hat{\Omega}\cdot\hat{\Omega}')\delta n(\textbf{K}')\end{align}$$$$

where \\(\bar{F}(\hat{\Omega}\cdot\hat{\Omega}')\propto F(\hat{\Omega}\cdot\hat{\Omega}',0)\\), \\(k - K - K_F\\). 

$$$$\begin{align}\delta n(\textbf{K}) = 0 or 1\end{align}$$$$ for $k>k_F$, and $0$ or $-1$ for $k < k_F$. 

THis is how Landau introduced \\(F\\) function, only depending on \\(\hat{\Omega}\cdot\hat{\Omega}'\\), not \\(\phi\\) which is 0. 

\\(F\\) for \\(\phi \not=0\\) doesn't appear in \\(E(\delta n)\\). 

Equivalently, 

$$$$\begin{align}\frac{E(r(\hat{\Omega}))}{V} = \frac{k_F^3}{(2\pi)^3}(v\int r^2(\hat{\Omega})\frac{d^2\hat{\Omega}}{4\pi} + \frac{1}{2}\int d\hat{\Omega}d\hat{\Omega}' r(\Omega) F(\hat{\Omega}\cdot\hat{\Omega}')r(\Omega'))\end{align}$$$$

Like deformation energy for a membrane!

Quadratic in \\(r(\hat{\Omega}) = k_F(\hat{\Omega}) - k_F\\) 

It appears we have only evaluated self energy to lienar order in \\(F\\) from (insert diagram here)

But actually this is exact result in narrow band limit. The technical reason is that, to maintain the desired Fermi sruface deformation \\(r(\hat{\Omega})\\) we must add an \\(O(F)\\) ``counter term" to \\(H'\\), 

$$$$\begin{align}\int \psi^\dagger(\Omega,\Lambda)\psi(\Omega\Lambda)\frac{dk d\Omega}{(2\pi)^3}\cdot \int \frac{d\Omega'}{(2\pi)^3}F(\hat{\Omega}'\cdot\hat{\Omega})r(\Omega')\end{align}$$$$

represent by (straight line diagram)

Only higher order terms in self energy in anrrow band limit are (isnert diagrams here)

and they all cancel each other. 

Landau (1956) becan his theory of Fermi liquids by observing that \\(1/\tau \propto \epsilon^2\\) (at \\(T = 0\\)) so low energy quasi particles are free-electron-like (with some renormalized fermi velocity \\(v'\\)) and we can parametrize low energy states in terms of their number \\(\delta n(\textbf{K})\\).

He then just proposed that teh energy of a state with \\(\delta n(\textbf{K})\\) particles added with momentum \\(\textbf{K}\\) should have the form of ??

I.e. there should be a pairwise interaction. 

He realized that \\(\bar{F}(\hat{\Omega}\cdot\hat{\Omega}')\\) was the forward scattering amplitude, at least for weak interactions.

In a later paper (1959), he realized that \\(\bar{F}\\) should actually be given by a certain infinite sum of Feynman diagrams ``the vertex part" in AGD - this was more or less equivalent to RG viewpoint. 

A varieety of low energy properties of Fermi liquids can be calculated in terms of \\(V'\\) and \\(F(\hat{\Omega}\cdot\hat{\Omega}')\\); zero sound, first sound, compressibility, specific hea,t magnetic properties 

We will see someo f these in student lectures.

A simple and famous result reslates \\(v'\\) to \\(F\\) - so \\(v'\\) is not really an independent parameter. Relation ship is a result of galilean invariance, i.e. that no bossing the velocities of all particle by \\(\delta\textbf{b} = \delta\p /m\\) (change of refernece frame) just changes the energy by exactly \\(\p\cdot\delta\p/m\\) where \\(m\\) is the bare fermion mass.

This is exact for a system like He3 with no lattice - no preferred reference frame.

This symmetry determines \\(v'/v\\) in terms of \\(F\\).

We conveniently write \\(v' = k_F/m^{*}\\) (and \\(v = k_F/m\\)), so, equivalently, \\(m^{*}/m\\) is determined by \\(F\\).

TO derive relationship consider an excited state with 1 quasi particle sitting infinitesimally above the Fermi surface in \\(\hat{z}\\) direciton. Now boost in \\(z\\) direction by \\(\delta p\\). 

The total momentum of the state before boost is \\(p = k_F\hat{z}\\), so \\(\delta E = \delta p k_F/m\\) (galilean invariance)

Alternatively, we can calculate \\(\delta E\\) using Fermi liquid Hamiltonian in terms of \\(V^{*}\\) and \\(F\\).

Kinetic energy term gives a contribution \\(\delta p v^{*} = \delta p k_F/m^{*}\\). 

There is another contirbution from interaction term \\(F\\). the boost distorts the Fermi surface.

New Fermi surface is described by 

$$$$\begin{align}|\textbf{K} - \delta p\hat{z}| < k_F\end{align}$$$$

$$$$\begin{align}K^2 - 2\delta p Kz < k_F^2\end{align}$$$$

\\(K < K_F + \delta p \cos\theta\\) 

so \\(r(\hat{\Omega}) = \delta p \cos\theta = \delta p z\\) from previous calculation, change in interaction energy is

$$$$\begin{align}\int F(\hat{\Omega}\cdot\hat{z})\delta p z \frac{d^2\Omega}{(2\pi)^3} = \delta p \int_{-1}^1 \frac{dz}{4\pi^2}F(z)z\end{align}$$$$

\\(F(\hat{\Omega}\cdot\hat{\Omega}')\\) is written as \\(2\pi^2 k_F\Phi(\hat{\Omega}\cdot\hat{\Omega}')/,^{*} = 2\pi^2 v^{*} \Phi(\hat{\Omega}\cdot\hat{\Omega}')\\)

where \\(\Phi\\) is dimensionless and \\(v^{*}\\) is a common factor in both terms in \\(H\\). Expanding in spherical Harmonic (legendre polynomials), 

$$$$\begin{align}\Phi(z) = \sum_\ell \Phi_\ell P_\ell(z) = \int_{-1}^1 dz \Phi_\ell(z)z = 2\delta \ell_! (2/3)\end{align}$$$$ 

because \\(P_1(z) = z\\). Given \\(1/m = 1/m^{*} + \Phi_1/3m^{*}\\) or 

$$$$\begin{align}\frac{m^{*}}{m} = 1 + \frac{1}{3}\Phi_1\end{align}$$$$

so \\(\Phi_1\\) is completely determined by \\(m^{*}/m = v/v^{*}\\)

or vice versa - reduces by 1, number of free parameters in Fermi liquid theory.

Answers ot questions.

$$$$\begin{align}\frac{1}{\tau}\propto \epsilon^2\log\frac{cE_F}{\epsilon}\end{align}$$$$

in \\(\D=2\\), where \\(c\\) is a constant of order 1. It goes to zero only slightly slower than in \\(\D=3\\) 

GEineral form of RG equations in any model 

$$$$\begin{align}\Lambda \frac{d\lambda_i}{d\Lambda} = f(\lambda_1,\lambda_2,\dots,\Lambda)\end{align}$$$$

i.e. there could be dependence on ?? cutoff \\(\Lambda\\) as well as in the values of coupling constants at the cutoff. 

In many simple and important situations there is no explicit dependence on \\(\Lambda\\). 

Often, there is some initial dependence which goes away as \\(\Lambda\\) is reduced - true of all examples discussed in course.


\section{Spin Models}
We will take a small diversion to spin models. Although this course is primarily concerned with interacting fermions and bosons, we will consider spin models only to the extent that they will be useful for coupling to conduction electrons in the Kondo lattice model. For a more thorough treatment of spin models, we also have a quantum magnetism course. 

