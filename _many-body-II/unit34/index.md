---
layout: lesson
title: Renormalization Group for Interaction Fermions: 2 dimensions
dept: physics
course: many-body-II
unit: unit34
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 34
---
Consider a free electron gas in \\(d = 2\\). The dispersion relation is \\(\epsilon_{\K} = \frac{\K^2}{2m}\\). Then, the reduced dispersion with chemical potential is \\(\xi_{\K} = \epsilon_{\K} - \mu\\) can be linearized around the Fermi level. This allows us to rewrite \\(\xi_{\k} = vk\\). Here, \\(k = |\K| - K_F\\). The Hamiltonian is given by (where \\(\{\psihat(\x),\psihat^\dagger(\y)\} = \delta(\x-\y)\\))

$$\Hhat = \int \psihat^\dagger(\x) \left(-\frac{\nabla^2}{2m} - \mu\right)\psihat(\x) \d \x = \int \xi_{\K} \psihat^\dagger(\K) \psihat(\K) \frac{\d^d\K}{(2\pi)^d} $$

where \\(\xi_{\K} = \K^2/2m - \mu\\), and we used the Fourier transform

$$\psihat(\x) = \int e^{i\K\cdot\x} \psihat(\K) \frac{\d^d\K}{(2\pi)^d}.$$

Let us briefly discuss the spectrum of this Hamiltonian. The energy levels are 

$$\xi_{\K} = \frac{\K^2}{2m} - \mu$$

This tells us that the ground state has all states for which \\(\xi_{\K} < 0\\). The set \\(\xi_{\K} = 0\\) constitutes the Fermi surface, and the low-energy excitations can be found by linearizing the dispersion about the points \\(\K\\) satisfying \\(\xi_{\K} = 0\\). This first gives us the value of the Fermi wave vector \\(K_F = \sqrt{2m\mu}\\). We note that there are infinitely many points on the Fermi surface, each labelled by an angle \\(\theta\in[0,2\pi)\\). However, since the dispersion relation is independent of \\(\theta\\), we will just Taylor expand about the magnitude of \\(K = K_F\\). To do this, we set \\(K = K_F +k\\), where \\(k\\) is the displacement from the Fermi surface in the radial direction. Then, 

$$\xi_{K} = \frac{K^2}{2m} - \mu = \frac{(2K_F+k)k}{2m}$$

If we are interested in low-energy physics, then \\(k \ll K_F\\), so we get 

$$\xi_{K} \approx \frac{K_F}{m}k = v_Fk$$

where \\(v_F = K_F/m\\). This linearization of the dispersion relation will make our lives much simpler. The low-energy Hamiltonian can also be written by separating the angular dependence from the radial dependence (because the dispersion doesn't depend on angle). Here, we define a cutoff \\(\Lambda\\), where \\(|k| < \Lambda \ll K_F\\). This low-energy Hamiltonian is then given by

$$\Hhat = \int_{-\Lambda}^\Lambda \int_0^{2\pi} \xi_{k} \psihat^\dagger(k,\theta) \psihat(k,\theta) \frac{K_F\d\theta \d k}{(2\pi)^2} $$

As a final step, we absorb \\(K_F\\) into our fields, giving us therefore 

$$\Hhat = \int_{-\Lambda}^\Lambda \int_0^{2\pi} \xi_{k} \psihat^\dagger(k,\theta) \psihat(k,\theta) \frac{\d\theta \d k}{(2\pi)^2} $$

We are finally ready to set up the Grassmann action. Doing this for the free part, we find

$$S_0 = \int_0^\beta \int_{-\Lambda}^\Lambda\int_0^{2\pi} \bar{\psi}_{k\theta\tau} (\partial_\tau + \xi_{k}) \psi_{k\theta\tau}\frac{\d\theta\d k}{(2\pi)^2} \d\tau$$

Next, we use the following Fourier transforms to Matsubara space, which hold in the following form at zero temperature:

$$\psi_{k\tau} = \int \psi_{k\omega} e^{-i\omega\tau} \frac{\d\omega}{2\pi}$$

This gives us the following action:

$$S_0 = \iint  \bar{\psi}_{k\theta\omega} (-i\omega+ v_Fk) \psi_{k\theta\omega} \frac{\d\omega}{2\pi} \frac{\d\theta\d k}{(2\pi)^2}$$

We want to perform a renormalization group analysis on this. To do this, we want to eliminate the high-energy modes. The high-energy modes, as we have seen, have large \\(k\\). Note that we do not impose a cutoff restriction for the Matsubara frequencies. We could do this, and obtain the same results (CHECK), but we can justify this choice here because a large \\(\omega\\) does not get suppressed in the action unlike it did in the Hertz-Millis theory. In the Hertz-Millis theory, we had a real action, and large \\(\omega\\) would increase the energy by a lot. For a Grassmann action, large \\(\omega\\) is not suppressed. 

The RG transformation will scale \\(k\\) and \\(\omega\\) the same way, according to \\(k' = sk\\), \\(\omega' = s\omega\\). Performing this transformation on the free action, we find 

$$\begin{align}
S_0 =& \iint  \bar{\psi}_{k\theta\omega} \left(-i\frac{\omega'}{b} + v_F\frac{k'}{b}\right) \psi_{k\theta\omega} \frac{\d\omega'}{b2\pi} \frac{\d\theta\d k'}{b(2\pi)^2} \\
=& \iint  \frac{1}{b^{3/2}}\bar{\psi}\left(\frac{k'}{b},\theta,\frac{\omega'}{b}\right) \left(-i\omega' + v_Fk'\right) \frac{1}{b^{3/2}}\psi\left(\frac{k'}{b},\theta,\frac{\omega'}{b}\right) \frac{\d\omega'}{2\pi} \frac{\d\theta\d k'}{(2\pi)^2}
\end{align}$$

This gives us \\(\psi'(k',\theta,\omega') = s^{-3/2}\psi\left(\frac{k'}{s},\theta,\frac{\omega'}{s}\right)\\), so that the action is invariant:

$$\begin{align}
S_0 =& \iint \bar{\psi}'\left(k',\theta,\omega'\right) \left(-i\omega' + v_Fk'\right) \psi\left(k',\theta, \omega'\right) \frac{\d\omega'}{2\pi} \frac{\d\theta\d k'}{(2\pi)^2}
\end{align}$$

Now, we introduce an extremely generic quartic action which preserves translation invariance in time and space. The consequence of this is delta functions for both momenta and Matsubara frequencies. 

$$\begin{align}
S_\text{int} =& \frac{1}{4}\int \bar{\psi}_{\K_4\omega_4} \bar{\psi}_{\K_3,\omega_3} \psi_{\K_2\omega_2} \psi_{\K_1\omega_1} u(\{\K_i,\omega_i\}) (2\pi)^3 \delta^{(2)}(\K_4+\K_3-\K_2-\K_1)\delta(\omega_4+\omega_3-\omega_2-\omega_1) \prod_{i=1}^4 \frac{\d^2\k_1}{(2\pi)^2} \frac{\d\omega_i}{2\pi}
\end{align}$$

where \\(u(\{\K_i,\omega_i\}) = u(\K_4,\omega_4,\K_3,\omega_3,\K_2,\omega_2,\K_1,\omega_1)\\). Evaluating the integral over 4, we find 

$$S_\text{int} = \frac{1}{4}\int \bar{\psi}_{\k_4\omega_4} \bar{\psi}_{\k_3,\omega_3} \psi_{\k_2\omega_2} \psi_{\k_1\omega_1} u(\{\k_i,\omega_i\}) \prod_{i=1}^3 \frac{\d^2\k_i}{(2\pi)^2} \frac{\d\omega_i}{2\pi} $$

wher \\(\K_4 = \K_1 + \K_2 - \K_3\\), and \\(\omega_4 = \omega_1 + \omega_2 - \omega_3\\). Now, if we restrict our fields to lie within the low-energy subspace, then we have that \\(|k_1|, |k_2|, |k_3| < \Lambda\\). Note however that this does not guarantee that \\(|k_4| < \Lambda\\). For this, we need to introduce a constraining \\(\theta\\)-function. There are no constraints on the Matsubara frequencies because we don't have a cutoff for them.

The interaction we can write as 

$$S_\text{int} = \frac{1}{4}\int \bar{\psi}(4)\bar{\psi}(3)\psi(2)\psi(1) \delta(4+3-2-1) u(4,3,2,1) \frac{\d^3 k_1}{(2\pi)^3} \frac{\d^3 k_2}{(2\pi)^3} \frac{\d^3 k_3}{(2\pi)^3} \frac{\d^3 k_4}{(2\pi)^3}$$

Since the low-energy physics is in the neighbournood of the Fermi usrface of distance \\(\Lambda\\), we define \\(\K = |\K|(\cos\theta,\sin\theta)\\) and the distance \\(k = |\K|-K_F\\). Then, \\(|k| < \Lambda\\). The momentum conservation gives us 

$$\K_4 = \K_1 + \K_2 - \K_3$$

we find that \\(k_4 = |\K_1 + \K_2 - \K_3| - K_F\\). Note however that the field \\(\bar{\psi}(4)\\) may have a momentum much farther than \\(\Lambda\\) away from the Fermi surface. In particular, if \\(\K_1 = K_F\ehat_1\\), \\(\K_2 = K_F\ehat_1\\), and \\(\K_3 = -K_F\ehat_1\\), then \\(|\K_4|\\) could be \\(3K_F\\). This is clearly a problem! We must therefore introduce a theta function \\(\theta(\Lambda - |k_4|)\\), which ensures that the fourth momentum stays within \\(\Lambda\\) of the Fermi surface. Thus, 

$$S_\text{int} = \frac{1}{4} \int_{-\Lambda}^\Lambda \int_{-\Lambda}^\Lambda \int_{-\Lambda}^\Lambda \bar{\psi}(4)\bar{\psi}(3)\psi(2)\psi(1) \theta(\Lambda - |k_4|) u(4,3,2,1) \frac{\d^3 k_1}{(2\pi)^3} \frac{\d^3 k_2}{(2\pi)^3} \frac{\d^3 k_3}{(2\pi)^3} $$

In the RG procedure, we would split up into slow and fast fields, and then integrate over fast fields. Let's just look at how the term with all slow fields would rescale back to the original.

$$S_\text{int}^< = \frac{1}{4} \int_{-\Lambda/b}^{\Lambda/b} \int_{-\Lambda/b}^{\Lambda/b} \int_{-\Lambda/b}^{\Lambda/b} \bar{\psi}(4)\bar{\psi}(3)\psi(2)\psi(1) \theta(\Lambda/b - |k_4|) u(4,3,2,1) \frac{\d^3 k_1}{(2\pi)^3} \frac{\d^3 k_2}{(2\pi)^3} \frac{\d^3 k_3}{(2\pi)^3} $$

Then, we use the RG transformation \\(k' = bk\\) and \\(\omega' = b\omega\\), which gives us that 

$$S_\text{int}^< = \frac{1}{4} \int_{-\Lambda}^{\Lambda} \int_{-\Lambda}^{\Lambda} \int_{-\Lambda}^{\Lambda} \bar{\psi}(4'/b)\bar{\psi}(3'/b)\psi(2'/b)\psi(1'/b) \theta(\Lambda/b - |k_4|) u(4,3,2,1) \frac{\d^3 k_1'}{b^2(2\pi)^3} \frac{\d^3 k_2'}{b^2(2\pi)^3} \frac{\d^3 k_3'}{b^2(2\pi)^3} $$

We note that the measure being scaled by only \\(1/b^2\\) instead of \\(1/b^3\\) is a consequence of the low-energy excitations being nearby the Fermi surface, instead of being near \\(K = 0\\), and the fact that if we map \\(k' = bk\\), then \\(k = |\K| - K_F\\)....COME UP WITH A JUSTIFICATION

What happens with the \\(\theta\\)-function? Well, let's rewrite \\(k_4\\). We had that 

$$\begin{align}
k_4 =& |\K_1 + \K_2 - \K_3| - K_F \\
=& |K_F(\nhat_1 + \nhat_2 - \nhat_3) + k_1\nhat_1 + k_2\nhat_2 - k_3\nhat_3| - K_F
\end{align}$$

Thus, when we make the variable substitutions \\(k' = bk\\), we get that 

$$\frac{k_4'}{b} = \left|K_F(\nhat_1 + \nhat_2 - \nhat_3) + \frac{k_1'\nhat_1 + k_2'\nhat_2 - k_3'\nhat_3}{b}\right| - K_F$$

which we can rewrite as 

$$k_4' = \left|bK_F(\nhat_1 + \nhat_2 - \nhat_3) + k_1'\nhat_1 + k_2'\nhat_2 - k_3'\nhat_3\right| - bK_F$$

Therefore, the \\(\theta\\)-function becomes 

$$\theta(\Lambda/b - |k_4|) = \theta(\Lambda - |k_4'|)$$

HOWEVER, the \\(k_4'\\) does not have the same form as \\(k_4\\) did. This is because \\(K_F \mapsto bK_F\\). Therefore, there is no way to say how the coupling \\(u\\) transforms if the integration measure does not return to its original form. To resolve this issue, we instead use a soft cutoff, replacing \\(\theta(\Lambda - |k_4|) \mapsto e^{-|k_4|/\Lambda}\\). Thus, the high-energy modes are exponentially suppressed, but not entirely eliminated. Defining \\(\Omegahat = \Omegahat_1 + \Omegahat_2 - \Omegahat_3\\), and replacing the \\(\theta\\) function with its exponential counterpart, we find that 

$$\begin{align}
S_\text{int}^< =& \int_{-\Lambda}^{\Lambda} \int_{-\Lambda}^{\Lambda} \int_{-\Lambda}^{\Lambda} \bar{\psi}(4'/b)\bar{\psi}(3'/b)\psi(2'/b)\psi(1'/b) e^{-|k_4'|/\Lambda} u(4,3,2,1) \frac{\d^3 k_1'}{b^2(2\pi)^3} \frac{\d^3 k_2'}{b^2(2\pi)^3} \frac{\d^3 k_3'}{b^2(2\pi)^3} \\
=& \int_{-\Lambda}^{\Lambda} \int_{-\Lambda}^{\Lambda} \int_{-\Lambda}^{\Lambda} b^{3/2}\bar{\psi}'(4')b^{3/2}\bar{\psi}'(3')b^{3/2}\psi'(2')b^{3/2}\psi'(1') e^{-||bK_F\Omegahat| - bK_F|/\Lambda} u(4,3,2,1) \frac{\d^3 k_1'}{b^2(2\pi)^3} \frac{\d^3 k_2'}{b^2(2\pi)^3} \frac{\d^3 k_3'}{b^2(2\pi)^3} \\
=& \int_{-\Lambda}^{\Lambda} \int_{-\Lambda}^{\Lambda} \int_{-\Lambda}^{\Lambda} \bar{\psi}'(4') \bar{\psi}'(3') \psi'(2') \psi'(1')  e^{-||\Omegahat| - 1|bK_F/\Lambda} u(4,3,2,1) \frac{\d^3 k_1'}{(2\pi)^3} \frac{\d^3 k_2'}{(2\pi)^3} \frac{\d^3 k_3'}{(2\pi)^3} \\
=& \int_{-\Lambda}^{\Lambda} \int_{-\Lambda}^{\Lambda} \int_{-\Lambda}^{\Lambda} \bar{\psi}'(4') \bar{\psi}'(3') \psi'(2') \psi'(1') e^{-||\Omegahat| - 1|K_F/\Lambda} e^{-||\Omegahat| - 1|(b-1)K_F/\Lambda} u(4,3,2,1) \frac{\d^3 k_1'}{(2\pi)^3} \frac{\d^3 k_2'}{(2\pi)^3} \frac{\d^3 k_3'}{(2\pi)^3}
\end{align}$$

For the last step, we just modify this so that it looks like the original factor. Thus, we see that 

$$u'(4',3',2',1') = e^{-||\Nhat| - 1|(b-1)K_F/\Lambda} u\left(\frac{4'}{b},\frac{3'}{b},\frac{2'}{b},\frac{1'}{b}\right)$$

We see that this is irrelevant, unless a special condition is satisfied. The only couplings which survive the exponential suppression as \\(b\to 1\\) are those for which \\(|\nhat| = 1\\). To make that true, we require that 

$$|\nhat_1 + \nhat_2 - \nhat_3| = 1$$

For this, we have three options:

<ul>
<li> \\(\nhat_1 = \nhat_3\\)
</li> 
 <li> \\(\nhat_2 = \nhat_3\\)
</li> 
 <li> \\(\nhat_1 = -\nhat_2\\).
\end{itemize}

For angles obeying one of the three conditions, we can forget about the exponential suppression factor, and conclude that 

$$u'(4',3',2',1') = u\left(\frac{4'}{b},\frac{3'}{b},\frac{2'}{b},\frac{1'}{b}\right)$$

Let's expand this in a Taylor series for small \\(k\\) and \\(\omega\\). This is possible only if the function is nonsingular. Note that this is not generically true, because we could have e.g. the Coulomb interaction. However, if we consider a screened Coulomb interaction, then there is no problem. Such a singular interaction is a general property of integrating out a gapless degree of freedom like the photon. This will give us a bunch of coupling constants:

$$u = u_0 + ku_1 + k^2u_2 + \cdots$$

and we see that \\(u_0\\) is marginal, and the rest are irrelevant. Therefore, we can ignore the dependence of \\(u\\) on \\(k\\) and \\(\omega\\). However, it is still posisble to for \\(u\\) to depend on the angles! However, since interactions with \\(k\\) in them are irrelevant, we may as well evaluate \\(u_0\\) on the Fermi circle. In this case, we have 

$$u_0 = u(\theta_1,\theta_2,\theta_3,\theta_4)$$

and for cases 1 and 2, we have either \\(\theta_1 = \theta_3\\) or \\(\theta_2 = \theta_3\\). However, since \\(u\\) is antisymmetric under exchange of \\(\theta_1\\) and \\(\theta_2\\), including that permutation gives us no new information. We can therefore set \\(\theta_1 = \theta_3\\) and \\(\theta_2 = \theta_4\\). Thus 

$$u_0 = F(\theta_1,\theta_2) = F(\theta_1-\theta_2)$$

where the last step is due to rotational invariance. This is one of the couplings that we will have. The other coupling function can be found by setting \\(\theta_1 + \theta_2 = 0\\). Then we also have \\(\theta_3 + \theta_4 = 0\\), and that there is a coupling function \\(V(\theta_1 - \theta_3) = V(\theta)\\). Both \\(F\\) and \\(V\\) are marginal at tree level. Before moving to the one-loop analysis, we need to perform some simplifying steps. We recall that \\(|\Nhat| = 1\\) was required for the interaction to have even a hope of relevancy. This constraint has important consequences on the magnitudes of the momenta. We recall that 

$$K_1\nhat_1 + K_2 \nhat_2 \equiv K_3 \nhat_3 + K_4 \nhat_4$$

For the first case, we have that \\(\nhat_1 = \nhat_3\\), so that 

$$\nhat_1(K_1 - K_3) \equiv \nhat_2(K_4 - K_2),\qquad \nhat_1(k_1 - k_3) \equiv \nhat_2(k_4 - k_2)$$

If we don't want the only scattering events to be those between parallel-ly travelling electrons, we can require that \\(k_1 = k_3\\) and \\(k_2 = k_4\\). Similarly, for the case \\(\nhat_1 + \nhat_2 = 0\\), we get that \\(k_1 = -k_2\\) and \\(k_3 = -k_4\\).

The conclusion here is that both of these couplings \\(F\\) and \\(V\\) are marginal at tree level. Let us now move on to the one-loop analysis. To facilitate this analysis, we must simplify the action. The interaction that we have will be given by the sum of two terms:

$$u(4,3,2,1) = F(\theta_1-\theta_2)(2\pi)^2\delta(\theta_1-\theta_3)\delta(k_1-k_3) + V(\theta_1-\theta_3)(2\pi)^2\delta(\theta_1+\theta_2)\delta(k_1+k_2)$$

Plugging this in, we get (we drop the \\(e^{-|k_4|/\Lambda}\\) term because it doesn't change under the RG)

$$\begin{align}
S_\text{int} =& \frac{1}{4} \int \bar{\psi}(k_2,\theta_2,\omega_2 + \Omega)\bar{\psi}(k_1,\theta_1,\omega_1 - \Omega)\psi(k_2,\theta_2,\omega_2)\psi(k_1,\theta_1,\omega_1) F(\theta_1-\theta_2) \frac{\d k_1 \d k_2 \d \theta_1 \d\theta_2 \d\omega_1\d\omega_2\d\Omega }{(2\pi)^7} \\
&+\frac{1}{4} \int \bar{\psi}(-k_3,-\theta_3,-\omega_3 + \Omega)\bar{\psi}(k_3,\theta_3,\omega_3)\psi(-k_1,-\theta_1,-\omega_1+\Omega) \psi(k_1,\theta_1,\omega_1)  V(\theta_1-\theta_3) \frac{\d k_1 \d k_3 \d \theta_1 \d\theta_3 \d\omega_1 \d\omega_3 \d\Omega}{(2\pi)^7}
\end{align}$$

There are two kinds of vertices here, each of which may get renormalized! Let us now compute the renormalization at 1 loop order. The partition function for the theory is 

$$\begin{align}
Z =& \int e^{-S_0^< - S_0^> - S_\text{int}^< - S_\text{int}^>} \D\bar{\psi}_> \D\psi_> \D\bar{\psi}_< \D\psi_< \\
=& \int e^{-S_0^< - S_\text{int}^<} \left(\int e^{-S_0^> - S_\text{int}^>} \D\bar{\psi}_> \D\psi_>\right)\D\bar{\psi}_< \D\psi_< \\
=& Z_0^> \int e^{-S_0^< - S_\text{int}^<} \langle e^{ - S_\text{int}^>} \rangle_{0>} \D\bar{\psi}_< \D\psi_<
\end{align}$$

We now perform a cumulant expansion on the expectation value. This gives us 

$$\langle e^{ - S_\text{int}^>} \rangle_{0>} = \exp\left[-\langle S_\text{int}^> \rangle_{0>} + \frac{1}{2}\left(\langle (S_\text{int}^>)^2 \rangle_{0>} - \langle S_\text{int}^>\rangle^2_{0>}\right) + \cdots \right]$$

The first order term gives the marginal result for the interaction that we already saw, but it may renormalize the kinetic term (show this?). The interaction term is renormalized at second order. To see this, we compute the connected diagrams which look like the \\(F\\) and \\(V\\) vertices. These are going to be 

\includegraphics[scale = 0.5]{RG_diagrams}

For the renormalization of \\(F\\), the zero sound diagram has the form 

$$\delta F = \int \frac{1}{i\omega - \xi_{\K}} \frac{1}{i\omega - \xi_{\K}} \frac{\d\omega}{2\pi}$$

This is zero because both of the poles are in the same half plane, and we therefore can close in the other half plane and get 0.

The zero sound' diagram has the form

$$\delta F = \int \frac{1}{i\omega - \xi_{\K}} \frac{1}{i\omega - \xi_{\K+\Q}} \frac{\d\omega}{2\pi} \frac{\d\theta}{2\pi} \frac{\d k}{2\pi} $$

The integral over \\(k\\) has width \\(\ell\Lambda\\), however not every angle will give us a particle-hole diagram. In fact, we require that the angular integral goes over the angle \\(\d\Lambda/K_F\\). Therefore, we get \\(\d\Lambda^2 = \ell^2\Lambda^2\\). This will go to zero when we take the limit \\(\ell \to 0\\). 

The BCS diagram also experiences this same thing, and goes to zero.

For the renormalization of \\(V\\), the zero sound and zero sound' diagrams both go to zero. 

Let us now compute the renormalization of \\(V\\) carefully. It is the \\(V\\) vertices which contribute to this diagram. Let us compute 

$$\begin{align}
\langle (S_\text{int}^>)^2\rangle_{0>} =& \frac{2}{16}\int \langle \bar{\psi}_<(-k_3,-\theta_3,-\omega_3 + \Omega)\bar{\psi}_<(k_3,\theta_3,\omega_3)\psi_>(-k_1,-\theta_1,-\omega_1+\Omega) \psi_>(k_1,\theta_1,\omega_1)  V(\theta_1-\theta_3) \frac{\d k_1 \d k_3 \d \theta_1 \d\theta_3 \d\omega_1 \d\omega_3 \d\Omega}{(2\pi)^7} \\
&\times\int \bar{\psi}_>(-k_3',-\theta_3',-\omega_3' + \Omega')\bar{\psi}_>(k_3',\theta_3',\omega_3')\psi_<(-k_1',-\theta_1',-\omega_1'+\Omega') \psi_<(k_1',\theta_1',\omega_1')  V(\theta_1'-\theta_3') \frac{\d k_1' \d k_3' \d \theta_1' \d\theta_3' \d\omega_1' \d\omega_3' \d\Omega'}{(2\pi)^7} \langle
\end{align}$$

We note that there are 4 ways to produce this because there are 2 ways to pick the fast fields for each of the two vertices. We now apply Wick's theorem to the fast fields: 

$$\begin{align}
&\langle \psi_>(-k_1,-\theta_1,-\omega_1+\Omega) \psi_>(k_1,\theta_1,\omega_1) \bar{\psi}_>(-k_3',-\theta_3',-\omega_3' + \Omega')\bar{\psi}_>(k_3',\theta_3',\omega_3')\rangle_{0>} \\
=& \langle \bar{\psi}_>(-k_3',-\theta_3',-\omega_3'+\Omega')\psi_>(k_1,\theta_1,\omega_1) \rangle_{0>} \langle \bar{\psi}_>(k_3',\theta_3',\omega_3') \psi_>(-k_1,-\theta_1,-\omega_1+\Omega) \rangle_{0>} \\
&- \langle \bar{\psi}_>(-k_3',-\theta_3',-\omega_3' + \Omega') \psi_>(-k_1,-\theta_1,-\omega_1+\Omega)  \rangle_{0>} \langle \bar{\psi}_>(k_3',\theta_3',\omega_3')\rangle_{0>} \psi_>(k_1,\theta_1,\omega_1) \rangle_{0>} \\
=& \frac{(2\pi)^3 \delta(\theta_1+\theta_3') \delta(k_1+k_3') \delta(\omega_1 + \omega_3'-\Omega')}{i\omega_1 - \xi_{\K_1}} \frac{2\pi)^3 \delta(\theta_1+\theta_3') \delta(k_1+k_3') \delta(\omega_1 + \omega_3'-\Omega)}{i\omega_3' - \xi_{-\K_1}} \\
&- \frac{(2\pi)^3 \delta(k_1-k_3') \delta(\theta_1 - \theta_3') \delta(\omega_3' - \Omega' - \omega_1 + \Omega)}{-i\omega_1+i\Omega - \xi_{-\K_1}} \frac{(2\pi)^3 \delta(k_1-k_3')\delta(\theta_1-\theta_3')\delta(\omega_1 - \omega_3')}{i\omega_1 - \xi_{\K_1}} \\
=& \frac{(2\pi)^3 \delta(\theta_1+\theta_3') \delta(k_1+k_3') \delta(\Omega-\Omega')}{i\omega_1 - \xi_{\K_1}} \frac{(2\pi)^3 \delta(\theta=0) \delta(k=0) \delta(\omega_1 + \omega_3'-\Omega)}{i\Omega - i\omega_1 - \xi_{\K_1}} \\
&- \frac{(2\pi)^3 \delta(k_1-k_3') \delta(\theta_1 - \theta_3') \delta(\Omega - \Omega')}{-i\omega_1+i\Omega - \xi_{\K_1}} \frac{(2\pi)^3 \delta(k=0)\delta(\theta=0)\delta(\omega_1 - \omega_3')}{i\omega_1 - \xi_{\K_1}} \\
=& \frac{(2\pi)^6\delta(\Omega-\Omega')}{i\omega_1 - \xi_{\K_1}}\frac{\delta(k=0)\delta(\theta=0)}{-i\omega_1 + i\Omega - \xi_{-\K_1}} [\delta(k_1+k_3') \delta(\theta_1+\theta_3')\delta(\omega_1+\omega_3'-\Omega) - \delta(k_1-k_3') \delta(\theta_1-\theta_3') \delta(\omega_1-\omega_3')]
\end{align}$$

Now, we can compute 

$$\begin{align}
\langle (S_\text{int}^>)^2\rangle_{0>} =& \frac{1}{8}\int \bar{\psi}_<(-k_3,-\theta_3,-\omega_3 + \Omega)\bar{\psi}_<(k_3,\theta_3,\omega_3) V(\theta_1-\theta_3) \psi_<(-k_1',-\theta_1',-\omega_1'+\Omega') \psi_<(k_1',\theta_1',\omega_1')  V(\theta_1'-\theta_3')\\
&\times\frac{(2\pi)^6\delta(\Omega-\Omega')}{i\omega_1 - \xi_{\K_1}}\frac{\delta(k=0)\delta(\theta=0)}{-i\omega_1 + i\Omega - \xi_{-\K_1}} [\delta(k_1+k_3') \delta(\theta_1+\theta_3')\delta(\omega_1+\omega_3'-\Omega) - \delta(k_1-k_3') \delta(\theta_1-\theta_3') \delta(\omega_1-\omega_3')] \\
&\times \frac{\d k_1 \d k_3 \d \theta_1 \d\theta_3 \d\omega_1 \d\omega_3 \d\Omega}{(2\pi)^7} \frac{\d k_1' \d k_3' \d \theta_1' \d\theta_3' \d\omega_1' \d\omega_3' \d\Omega'}{(2\pi)^7} \\
=&\frac{1}{8}\int \bar{\psi}_<(-k_3,-\theta_3,-\omega_3 + \Omega)\bar{\psi}_<(k_3,\theta_3,\omega_3)  \psi_<(-k_1',-\theta_1',-\omega_1'+\Omega) \psi_<(k_1',\theta_1',\omega_1')\\
&\times\frac{(2\pi)^6}{i\omega_1 - \xi_{\K_1}}\frac{\delta(k=0)\delta(\theta=0)}{-i\omega_1 + i\Omega - \xi_{-\K_1}} V(\theta_1-\theta_3) V(\theta_1'-\theta_3')[\delta(\theta_1+\theta_3') -  \delta(\theta_1-\theta_3')] \\
&\times \frac{\d k_1 \d k_3 \d \theta_1 \d\theta_3 \d\omega_1 \d\omega_3 \d\Omega}{(2\pi)^7} \frac{\d k_1'\d \theta_1' \d\theta_3' \d\omega_1'}{(2\pi)^7} \\
=&\frac{1}{8}\int \bar{\psi}_<(-k_3,-\theta_3,-\omega_3 + \Omega)\bar{\psi}_<(k_3,\theta_3,\omega_3)  \psi_<(-k_1',-\theta_1',-\omega_1'+\Omega) \psi_<(k_1',\theta_1',\omega_1')\\
&\times\frac{(2\pi)^6}{i\omega_1 - \xi_{\K_1}}\frac{\delta(k=0)\delta(\theta=0)}{-i\omega_1 + i\Omega - \xi_{-\K_1}} V(\theta_1-\theta_3) [V(\theta_1' + \theta_1) - V(\theta_1' - \theta_1)] \\
&\times \frac{\d k_1 \d k_3 \d \theta_1 \d\theta_3 \d\omega_1 \d\omega_3 \d\Omega}{(2\pi)^7} \frac{\d k_1'\d \theta_1' \d\omega_1'}{(2\pi)^7}
\end{align}$$

We can do a change of variables for the first \\(V\\) term and get 

$$\begin{align}
\langle (S_\text{int}^>)^2\rangle_{0>} =&\frac{1}{8}\int \bar{\psi}_<(-k_3,-\theta_3,-\omega_3 + \Omega)\bar{\psi}_<(k_3,\theta_3,\omega_3) \\
&\times V(\theta_1-\theta_3) [V(-\theta_1' + \theta_1)\psi_<(k_1',\theta_1',\omega_1') \psi_<(-k_1',-\theta_1',-\omega_1'+\Omega) - V(\theta_1' - \theta_1)\psi_<(-k_1',-\theta_1',-\omega_1'+\Omega) \psi_<(k_1',\theta_1',\omega_1')] \\
&\times \frac{(2\pi)^6}{i\omega_1 - \xi_{\K_1}}\frac{\delta(k=0)\delta(\theta=0)}{-i\omega_1 + i\Omega - \xi_{-\K_1}}  \frac{\d k_1 \d k_3 \d \theta_1 \d\theta_3 \d\omega_1 \d\omega_3 \d\Omega}{(2\pi)^7} \frac{\d k_1'\d \theta_1' \d\omega_1'}{(2\pi)^7}
\end{align}$$

This gives 2 times the thing, and we get UP TO A MINUS SIGN???

$$\begin{align}
\langle (S_\text{int}^>)^2\rangle_{0>} =&- \frac{1}{4}\int \bar{\psi}_<(-k_3,-\theta_3,-\omega_3 + \Omega)\bar{\psi}_<(k_3,\theta_3,\omega_3)\psi_<(-k_1',-\theta_1',-\omega_1'+\Omega) \psi_<(k_1',\theta_1',\omega_1') \\
&\times \left( \int V(\theta_1-\theta_3)V(\theta_1' - \theta_1)\frac{(2\pi)^2}{i\omega_1 - \xi_{\K_1}}\frac{\delta(k=0)\delta(\theta=0)}{-i\omega_1 + i\Omega - \xi_{-\K_1}} \frac{\d\theta_1}{2\pi} \frac{\d\omega_1}{2\pi} \frac{\d k_1}{2\pi} \right) \frac{\d k_3 \d\theta_3 \d\omega_3 \d\Omega}{(2\pi)^4} \frac{\d k_1'\d \theta_1' \d\omega_1'}{(2\pi)^3} 
\end{align}$$

Then setting \\(\delta(\theta = 0)2\pi = 1\\) and also \\(\delta(k=0)2\pi = \V = 1\\) the volume, we get 

$$\begin{align}
\langle (S_\text{int}^>)^2\rangle_{0>} =&- \frac{1}{4}\int \bar{\psi}_<(-k_3,-\theta_3,-\omega_3 + \Omega)\bar{\psi}_<(k_3,\theta_3,\omega_3)\psi_<(-k_1',-\theta_1',-\omega_1'+\Omega) \psi_<(k_1',\theta_1',\omega_1') \\
&\times \left( \int \frac{V(\theta_1-\theta_3)}{i\omega_1 - \xi_{\K_1}}\frac{V(\theta_1' - \theta_1)}{-i\omega_1 + i\Omega - \xi_{-\K_1}} \frac{\d\theta_1}{2\pi} \frac{\d\omega_1}{2\pi} \frac{\d k_1}{2\pi} \right) \frac{\d k_3 \d\theta_3 \d\omega_3 \d\Omega}{(2\pi)^4} \frac{\d k_1'\d \theta_1' \d\omega_1'}{(2\pi)^3} 
\end{align}$$

We define (setting \\(\Omega = 0\\))

$$\begin{align}
\Pi =& \frac{1}{2} \int \frac{V(\theta_1-\theta_3)}{i\omega_1 - \xi_{\K_1}}\frac{V(\theta_1' - \theta_1)}{-i\omega_1 - \xi_{\K_1}} \frac{\d\theta_1}{2\pi} \frac{\d\omega_1}{2\pi} \frac{\d k_1}{2\pi} \\
=& \frac{1}{2}\int \frac{V(\theta_1-\theta_3)V(\theta_1' - \theta_1)}{\omega_1^2 + \xi_{\K_1}^2} \frac{\d\theta_1}{2\pi} \frac{\d\omega_1}{2\pi} \frac{\d k_1}{2\pi} \\
=& \frac{1}{2}\int \frac{V(\theta_1-\theta_3)V(\theta_1' - \theta_1)}{2|\xi_{\K_1}|} \frac{\d\theta_1}{2\pi} \frac{\d k_1}{2\pi} \\
=& \frac{1}{2}\int \frac{V(\theta_1-\theta_3)V(\theta_1' - \theta_1)}{2}2\ell\Lambda \frac{\d\theta_1}{2\pi} \frac{1}{2\pi} \\
=& \frac{1}{8\pi^2}\int V(\theta_1 - \theta_3)V(\theta_1'-\theta_1) \d\theta_1
\end{align}$$

Finally, we have that the 

$$-V(\theta_1-\theta_3) \mapsto -V'(\theta_1-\theta_3) = - V(\theta_1-\theta_3) + \Pi $$

\section{Appendix}
Since \\(V' = V(b) = V(1+\ell) = V + \ell \frac{\d V}{\d\ell}\\), we find 

$$\frac{\d V}{\d \ell} = - \Pi = -\frac{1}{8\pi^2}\int V(\theta-\theta_3)V(\theta_1-\theta)\d\theta$$

Then, we can write in terms of a Fourier transform:

$$V(\theta) = \sum_m e^{im\theta} v_m$$

which gives the flow equation

$$\frac{\d v_m}{\d\ell} = -\frac{v_m^2}{4\pi}$$

We see that the couplings always flow to smaller values. If \\(v_m > 0\\), then it flows to zero. If \\(v_m < 0\\), it flower to minus infinity. This is the BCS instability! Thus we have two results. The result for \\(F\\) is that there is a renormalization of the band structure, but that the interaction is marginal. 

