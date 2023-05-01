---
layout: lesson
title: $\D=3$ case spherical fermi surface. 
dept: physics
course: many-body-II
unit: unit24
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 24
---
Again conditions \\(\textbf{K}_1 + \textbf{K}_2 = \textbf{K}_3 + \textbf{K}_4\\) and \\(|\textbf{K}_i| = K_F\\) are very restrictive. \\(F\\) type term can be more general.

\\(\theta_{34} = \theta_{12}\\) as before but \\(\textbf{K}_3\\) and \\(\textbf{K}_4\\) could be rigidly rotated about axis of \\(\textbf{K}_1 + \textbf{K}_2\\) by an angle \\(\phi\\) as shown (refer to figure)

\\(\phi = \phi_{12;34}\\) is angle between plane of \\(\textbf{K}_1,\textbf{K}_2\\) and plane of \\(\textbf{K}_3\\), \\(\textbf{K}_4\\). Coupling function \\(F\\) can now depend on \\(Z_{12} = \hat{\Omega}_1 \cdot\hat{\Omega}_2 = \cos\theta_{12}\\) (angle between \\(\textbf{K}_1\\), \\(\textbf{K}_2\\) and \\(\phi_{12,34}\\)). \\(F = F(Z_{12}, \phi_{12;34})\\). 

Other possibility \\(\textbf{K}_1 = -\textbf{K}_2\\); \\(\textbf{K}_3 = -\textbf{K}_4\\) is essentially unchanged.

\\(V\\) can depend on angle between \\(\textbf{K}_1\\) and \\(\textbf{K}_3\\) only: \\(V(Z_{13})\\) , \\(Z_{13} = \hat{\Omega}_1\cdot\hat{\Omega}_3 = \cos\theta_{13}\\)

we can again calculate \\(F\\) and \\(V\\) for cubic lattice tight binding model in limit of small \\(K_F\\) so Fermi surface is approximately spherical.

$$$$\begin{align}u(\hat{\Omega}_1,\hat{\Omega}_2,\hat{\Omega}_3,\hat{\Omega}_4) = u_0(\hat{\Omega}_1 - \hat{\Omega}_2)\cdot(\hat{\Omega}_3 - \hat{\Omega}_4)\end{align}$$$$

as before. \\(F\\) terms: \\(|\hat{\Omega}_1 - \hat{\Omega}_2| = |\hat{\Omega}_3 - \hat{\Omega}_4|\\), 

$$$$\begin{align}(\hat{\Omega}_1 - \hat{\Omega}_2)\cdot(\hat{\Omega}_3 - \hat{\Omega}_4) = (\hat{\Omega}_1 - \hat{\Omega}_2)^2\cos\phi_{12;34} = 2(1-Z_{12})\cos\phi_{12;34}\end{align}$$$$

\\(F\propto (1-Z_{12})\cos\phi_{12;34}\\)

\\(V\\) term: \\(\hat{\Omega}_1 = -\hat{\Omega}_2\\), \\(\hat{\Omega}_3 = -\hat{\Omega}_4\\). 

$$$$\begin{align}(\hat{\Omega}_1 - \hat{\Omega}_2)\cdot(\hat{\Omega}_3 - \hat{\Omega}_4) = 4\hat{\Omega}_1\cdot\hat{\Omega}_3 = 4Z_{13}\end{align}$$$$

as before \\(V\propto Z_{13}\\). 

An important calculation that we can do with this effective Hamiltonian is the decay rate (at \\(T=0\\)) for a particle of momentum \\(\textbf{K}_1\\), slightly above the Fermi surface to decay into 2 particles and a hole.

Let hole have momentum \\(\textbf{K}_2\\), particles have momentua \\(\textbf{K}_3\\) and \\(\textbf{K}_4\\), 

\\(|k_2|\\), \\(k_3\\), \\(k_4\\) \\(< k_1\\) by energy conservation. \\(Vk_1 = V(-k_2) + V k_3 + Vk_4\\) (\\(k_2 < 0\\), \\(k_{3.4}>0\\))

so we can do calculation using our low energy effective Hamiltonian. Let's assume \\(V = 0\\) for now, as it is for a Fermi liquid

We calculate \\(1/\tau\\) - decay rate to second order in \\(F\\) using Fermi's golden rule.

$$$$\begin{align}\frac{1}{\tau} = 2\pi \sum_f |\bra{f}H_\text{int}\ket{i}|^2\delta(E_f - E_i)\end{align}$$$$

This was probably first step in Landau's develop of Fermi liquid theory.

Restricted phase space at low \\(\epsilon_1\\) makes \\(1/\tau\propto \epsilon_1^2\\) so particle becomes infinitely long lived as \\(\epsilon_1\to 0\\) like a non-interacting electron.

$$$$\begin{align}\frac{1}{\tau} = 2\pi \frac{1}{2!}\int F(\theta\phi)^2 \frac{d^3k_2 d^3k_3 d^3k_4}{(2\pi)^9 k_F^4}\delta^{(3)}(\textbf{K}_1 + \textbf{K}_2 - \textbf{K}_3 - \textbf{K}_4)\delta(\epsilon_1 + \epsilon_2 - \epsilon_3 - \epsilon_4)\end{align}$$$$

Note: this process is equivalent to an actual particle of momentum \\(\textbf{K}_1\\) colliding with a particle inside Fermi sea, of momentum \\(\textbf{K}_2\\), with final 2 particles, above Fermi sea, at \\(\textbf{K}_3\\) and \\(\textbf{K}_4\\). 

We must have \\(K_2 < K_F\\), \\(K_3\\), \\(K_4 > K_F\\) at \\(T = 0\\) (to lowest order in interaction) due to ``Pauli blocking"

\\(1/\alpha!\\) factor arises due to 2 final particles being identical. 

\\(1/k_F^4\\) due to the way we defined interactions in terms of fields rescaled by \\(k_F\\). 

We are ignoring spin here, but result is very similar including it. If we do \\(\textbf{K}_4\\) integral, we get

$$$$\begin{align}\frac{1}{\tau} = \frac{1}{(2\pi)^8}\frac{1}{2!}\frac{1}{k_F^4}\int F(\theta,\phi)^2\delta(\epsilon_1 + \epsilon_2 - \epsilon_3 -\epsilon_4) d^3k_2 d^3k_3\end{align}$$$$

\\(\theta\\) is angle between \\(\textbf{K}_1\\) (initial particle) and \\(\textbf{K}_2\\) (hole) \\(\phi = \phi_{12;34}\\)

