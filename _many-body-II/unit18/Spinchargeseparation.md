---
layout: lesson
title: Spin charge separation
dept: physics
course: many-body-II
unit: unit18
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 18
---
Consider the Hamiltonian

$$\Hhat = i\frac{v_F}{2}\int_{-\infty}^\infty \left(\psihat^\dagger_\sigma \frac{\d}{\d x}\psihat_\sigma  - \frac{\d}{\d x}\psihat^\dagger_\sigma \psihat_\sigma\right)\d x$$

One option for writing this Hamiltonian in terms of bosonic currents is that we could use the abelian bosonization construction from earlier twice: once for each flavour of fermion. However, this Hamiltonian has \\(\SU(2)\\) invariance, and we want to write the Hamiltonian in a manifestly \\(\SU(2)\\) invariant way after the introduction of the bosonic currents. For this, we define a charge current and a spin current:

$$\Jhat(x) = :\psihat_\alpha^\dagger(x) \sigma^0_{\alpha\beta} \psihat_\beta(x):,\quad \hat{\boldsymbol{J}}(x) = :\psihat_\alpha^\dagger(x) \frac{\boldsymbol{\sigma}_{\alpha\beta}}{2}\psihat_\beta(x):$$

<ol>
\question Prove the following two formulas:

<ol type="a">
</li> 
 <li> $$\hat{\boldsymbol{J}}^2 = -\frac{3}{4}:\psihat^\dagger_\alpha \psihat_\alpha \psihat^\dagger_\beta \psihat_\beta: + \frac{3i}{2}\psihat_\alpha^\dagger \frac{\d}{\d x}\psihat_\alpha + \const $$
</li> 
 <li> $$\Jhat^2 = :\psihat_\alpha^\dagger \psihat_\alpha \psihat^\dagger_\beta \psihat_\beta: + 2i\psihat_\alpha^\dagger \frac{\d}{\d x}\psihat_\alpha + \const$$
\end{parts}

\begin{solution}
<ol type="a">
</li> 
 <li> We compute 

$$\begin{align}
\Jhat(x)\Jhat(y) =& \sum_{\alpha\beta}:\psihat^\dagger_\alpha(x)\psihat_\alpha(x)::\psihat^\dagger_\beta(y)\psihat_\beta(y): \\
=& \sum_{\alpha\beta}:\psihat^\dagger_\alpha(x)\psihat_\alpha(x)\psihat^\dagger_\beta(y)\psihat_\beta(y): + \wick{\c2{\psihat}^\dagger_\alpha(x) \c2{\psihat}_\beta(y)}:\psihat_\alpha(x)\psihat^\dagger_\beta(y): \\
&+\wick{\c2{\psihat}_\alpha(x)\c2{\psihat}^\dagger_\beta(y)}:\psihat^\dagger_\alpha(x)\psihat_\beta(y): + \wick{\c3{\psihat}^\dagger_\alpha(x) \c2{\psihat}_\alpha(x)\c2{\psihat}^\dagger_\beta(y) \c3{\psihat}_\beta(y)}
\end{align}$$

The first term we will show can be cancelled out later. The final term is just a constant and can be ignored. Note that if we were instead considering the commutator \\([\Jhat(x),\Jhat(y)]\\), then we could not ignore it! The second and third terms must be considered in more detail. 

$$\begin{align}
\Jhat(x)\Jhat(y) =& \sum_{\alpha\beta}\frac{-\delta_{\alpha\beta}}{2\pi i(x-y)}\psihat^\dagger_\beta(y)\psihat_\alpha(x) + \frac{\delta_{\alpha\beta}}{2\pi i(x-y)}\psihat^\dagger_\alpha(x)\psihat_\beta(y) \\
=& \sum_{\alpha\beta}\frac{\delta_{\alpha\beta}i}{2\pi (x-y)}\left[\left(\psihat^\dagger_\alpha(x) + (y-x)</li> 
 <li>ial_x\psihat^\dagger_\alpha(x)\right)\psihat_\alpha(x) - \psihat^\dagger_\alpha(x)\left(\psihat_\alpha(x) + (y-x)</li> 
 <li>ial_x\psihat_\alpha(x)\right)\right] \\
=& \sum_{\alpha\beta}:\psihat^\dagger_\alpha(x)\psihat_\alpha(x)\psihat^\dagger_\beta(y)\psihat_\beta(y): + \frac{i}{2\pi}\sum_\alpha\left[\psihat^\dagger_\alpha(x)</li> 
 <li>ial_x\psihat_\alpha(x)-</li> 
 <li>ial_x\psihat^\dagger_\alpha(x)\psihat_\alpha(x)\right] 
\end{align}$$

where, in the last line, we restored the term we previously threw away.

</li> 
 <li> Now we compute 

$$\begin{align}
\boldsymbol{J}(x)\cdot\boldsymbol{J}(y) =& \sum_{\alpha\beta\gamma\delta}:\psihat^\dagger_\alpha(x)\frac{\boldsymbol{\sigma}_{\alpha\beta}}{2}\psihat_\beta(x)::\psihat^\dagger_\gamma(y)\frac{\boldsymbol{\sigma}_{\gamma\delta}}{2}\psihat_\delta(y): \\
=& \frac{1}{4} \sum_{\alpha\beta\gamma\delta}\boldsymbol{\sigma}_{\alpha\beta}\cdot\boldsymbol{\sigma}_{\gamma\delta} \left[  :\psihat^\dagger_\alpha(x)\psihat_\beta(x)\psihat^\dagger_\gamma(y)\psihat_\delta(y): + \wick{\c2{\psihat}^\dagger_\alpha(x)\c2{\psihat}_\delta(y) }:\psihat_\beta(x)\psihat^\dagger_\gamma(y): \right.\\
&\left.+\wick{\c2{\psihat}_\beta(x) \c2{\psihat}^\dagger_\gamma(y)} :\psihat^\dagger_\alpha(x)\psihat_\delta(y): + \wick{\c3{\psihat}^\dagger_\alpha(x)\c2{\psihat}_\beta(x)\c2{\psihat}^\dagger_\gamma(y)\c3{\psihat}_\delta(y)} \right]
\end{align}$$

The first term we will later show to cancel out, the final term is a constant that we can ignore in this case, and the second and third terms need to be treated more carefully.

$$\begin{align}
\boldsymbol{J}(x)\cdot\boldsymbol{J}(y) =& \frac{1}{4}\sum_{\alpha\beta\gamma\delta}\boldsymbol{\sigma}_{\alpha\beta}\cdot\boldsymbol{\sigma}_{\gamma\delta} \frac{\delta_{\alpha\delta}}{2\pi i(x-y)}:\psihat_\beta(x)\psihat^\dagger_\gamma(y): + \frac{\delta_{\beta\gamma}}{2\pi i(x-y)}:\psihat^\dagger_\alpha(x)\psihat_\delta(y): \\
=&\frac{1}{4}\sum_{\alpha\beta\gamma\delta}\boldsymbol{\sigma}_{\alpha\beta}\cdot\boldsymbol{\sigma}_{\gamma\delta} \frac{i}{2\pi (x-y)}\left[\delta_{\alpha\delta}:\psihat^\dagger_\gamma(y)\psihat_\beta(x): - \delta_{\beta\gamma}:\psihat^\dagger_\alpha(x)\psihat_\delta(y): \right] \\
=&\frac{1}{4}\sum_{\alpha\beta}(\sigma^\ell\sigma^\ell)_{\alpha\beta} \frac{i}{2\pi (x-y)}\left[:\psihat^\dagger_\alpha(y)\psihat_\beta(x): - :\psihat^\dagger_\alpha(x)\psihat_\beta(y): \right] \\
=&\frac{1}{4}\sum_{\alpha\beta} 3\delta_{\alpha\beta} \frac{i}{2\pi (x-y)}\left[:\psihat^\dagger_\alpha(y)\psihat_\beta(x): - :\psihat^\dagger_\alpha(x)\psihat_\beta(y): \right] \\
=&\frac{3}{4}\sum_{\alpha} \frac{i}{2\pi (x-y)}\left[:\left(\psihat^\dagger_\alpha(x) + (y-x)</li> 
 <li>ial_x\psihat_\alpha(x)\right)\psihat_\alpha(x): - :\psihat^\dagger_\alpha(x)\left(\psihat_\alpha(x) + (y-x)</li> 
 <li>ial_x\psihat_\alpha(x)\right): \right] \\
=& -\frac{3}{4}:\psihat^\dagger_\alpha(x)\psihat_\alpha(x)\psihat^\dagger_\beta(x)\psihat_\beta(x): + \frac{3}{4} \sum_{\alpha} \frac{i}{2\pi}\left[\psihat^\dagger_\alpha(x)</li> 
 <li>ial_x\psihat_\alpha(x) - </li> 
 <li>ial_x\psihat_\alpha(x)\psihat_\alpha(x) \right]
\end{align}$$

where we set \\(x = y\\) in the last line, as well as reintroduced the term we threw out earlier.

</li> 
 <li> Now, we construct a combination of these currents which cancels out the first term. To do it, we compute 

\end{parts}
\end{solution}


\question Consider the following identities which are useful for the \\(k\\)-channel Kondo problem. In this case, there are now \\(k\\) flavours of electron, and there are \\(k^2-1\\) generators of \\(\SU(k)\\). The elements of the corresponding Lie algebra are written \\(T^A\\), where \\(A = 1,\dots,k^2-1\\). They are normalized such that \\(\tr(T^AT^B) = \delta_{AB}/2\\). They also obey the completeness relation 

$$\sum_A T^A_{ab} T^A_{cd} = \frac{1}{2}\left[\delta_{ad}\delta_{bc} - \frac{1}{k}\delta_{ab}\delta_{cd}\right]$$

and also the commutation relations 

$$[T^A,T^B] = if^{ABC}T^C$$

The currents are 

$$\Jhat = \sum_{i\alpha} :\psihat_{i\alpha}^\dagger(x) \psihat_{i\alpha}(x):,\quad \hat{\boldsymbol{J}} = \sum_i \psihat^\dagger_{i\alpha} \frac{\boldsymbol{\sigma}_{\alpha\beta}}{2}\psihat_{i\beta}:, \quad \Jhat^A = \sum_\alpha \psihat_{i\alpha}^\dagger T^A_{ij} \psihat_{j\alpha}:$$

Show that the free fermion Hamiltonian density 

$$\mathcal{H} = i\sum_{i\alpha} \psihat^\dagger_{i\alpha}\frac{\d}{\d x}\psihat_{i\alpha}$$

can be written in the form

$$\mathcal{H} = \frac{1}{8\pi k}\Jhat^2 + \frac{1}{2\pi(k+2)}\hat{\boldsymbol{J}}^2 + \frac{1}{2\pi(k+2)} \Jhat^A \Jhat^A$$

\end{questions}

