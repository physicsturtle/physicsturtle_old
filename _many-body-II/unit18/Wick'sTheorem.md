---
layout: lesson
title: Wick's Theorem
dept: physics
course: many-body-II
unit: unit18
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 18
---
Wick's theorem, as we have typically seen it, applies to expanding the correlator of numerous creation/annihilation operators into a sum of products of 2-point correlators. Wick's theorem also comes in other flavours however. The flavour that we will use here is the following. If \\(\Ahat_1,\dots,\Ahat_n\\) are (linear combinations of) creation and annihilation operators, then 

$$\begin{align} 
\Ahat_1\dots \Ahat_n =& : \Ahat_1\dots \Ahat_n:\\
&+ :\wick{\c2{\Ahat_1}\c2{\Ahat_2}\Ahat_3\dots \Ahat_n}: + \dots + : \wick{\c2{\Ahat_1}\dots\c2{\Ahat_{n-1}}A_n}: + :\wick{\c2{\Ahat_1}\dots\c2{\Ahat_n}}: \\
&+:\wick{\c2{\Ahat_1}\c2{\Ahat_2}\c2{\Ahat_3}\c2{\Ahat_4}\dots \Ahat_n}: + \dots.
\end{align}$$ 


Here \\(:\cdot :\\) denotes the normal ordering of operators, and \\(\wick{\c2{\Ahat_i} \c2{\Ahat_j}} = \langle \Ahat_i \Ahat_j \rangle\\). The expectation value is taken with respect to either the bosonic vacuum (in the case of bosonic operators), or the Fermi sea (in the case of fermionic operators) CHECK IF THIS IS RIGHT!!!.  



We need to make some comments on Wick's theorem in CFT. One of the things we assume whenever dealing with operators is that things occur inside both of a time-ordering symbol and also inside expectation values. Under expectation values, Wick's theorem applies. It is therefore confusing to suppress this symbol and perform Wick contractions when there are no expectation value symbols around! 

NOTE: If \\(z - z' \ll \beta v_F/\pi\\), then \\(\mathcal{G}(z;z') \sim \frac{1}{2\pi(z-z')}\\).

<div class="example">
<b>Example:</b>
Consider the current operator \\(\Jhat(z) = 2\pi:\psihat^\dagger(z) \psihat(z):\\). Compute the product \\(\Jhat(z+\epsilon) \Jhat(z)\\). 

To do this, let us apply Wick's theorem to the following quantity: 

$$\begin{align}
\psihat^\dagger(z_1)\psihat(z_1)\psihat^\dagger(z_2) \psihat(z_2) =& :\psihat^\dagger(z_1)\psihat(z_1)\psihat^\dagger(z_2) \psihat(z_2): \\
&+ :\wick{\c2{\psihat^\dagger}(z_1) \c2{\psihat}(z_1)} \psihat^\dagger(z_2) \psihat(z_2): + :\psihat^\dagger(z_1)\psihat(z_1) \wick{\c2{\psihat}^\dagger(z_2) \c2{\psihat}(z_2)}: \\
&+ :\wick{\c2{\psihat}^\dagger(z_1)\psihat(z_1)\psihat^\dagger(z_2) \c2{\psihat}(z_2)}: + :\psihat^\dagger(z_1) \wick{\c2{\psihat}(z_1) \c2{\psihat}^\dagger(z_2)} \psihat(z_2): \\
&+ : \wick{\c2{\psihat}^\dagger(z_1) \c2{\psihat}(z_1) \c2{\psihat}^\dagger(z_2) \c2{\psihat}(z_2)}: + :\wick{\c3{\psihat}^\dagger(z_1)\c2{\psihat}(z_1) \c2{\psihat}^\dagger(z_2) \c3{\psihat}(z_2)}:
\end{align}$$

The 1st normal ordered term goes to zero by fermionic statistics in the limit \\(z_1\to z_2\\). Also taking the contractions out of the normal order, we find

$$\begin{align}
\psihat^\dagger(z_1)\psihat(z_1)\psihat^\dagger(z_2) \psihat(z_2) =& \wick{\c2{\psihat^\dagger}(z_1) \c2{\psihat}(z_1)} : \psihat^\dagger(z_2) \psihat(z_2): + :\psihat^\dagger(z_1)\psihat(z_1) : \wick{\c2{\psihat}^\dagger(z_2) \c2{\psihat}(z_2)} \\
&+ \wick{\c2{\psihat}^\dagger(z_1)\c2{\psihat}(z_2)} :\psihat(z_1)\psihat^\dagger(z_2) : + \wick{\c2{\psihat}(z_1) \c2{\psihat}^\dagger(z_2)} :\psihat^\dagger(z_1)  \psihat(z_2): \\
&+  \wick{\c2{\psihat}^\dagger(z_1) \c2{\psihat}(z_1)} \wick{\c2{\psihat}^\dagger(z_2) \c2{\psihat}(z_2)} + \wick{\c2{\psihat}^\dagger(z_1) \c2{\psihat}(z_2)} \wick{\c2{\psihat}(z_1) \c2{\psihat}^\dagger(z_2) }
\end{align}$$

Now combining some terms, we get 

$$\begin{align}
\psihat^\dagger(z_1)\psihat(z_1)\psihat^\dagger(z_2) \psihat(z_2) =& \wick{\c2{\psihat^\dagger}(z_1) \c2{\psihat}(z_1)} \left(: \psihat^\dagger(z_2) \psihat(z_2): + \wick{\c2{\psihat}^\dagger(z_2) \c2{\psihat}(z_2)}  \right) \\
&+ :\psihat^\dagger(z_1)\psihat(z_1) : \wick{\c2{\psihat}^\dagger(z_2) \c2{\psihat}(z_2)} + \wick{\c2{\psihat}^\dagger(z_1)\c2{\psihat}(z_2)} :\psihat(z_1)\psihat^\dagger(z_2) : \\
&+ \wick{\c2{\psihat}(z_1) \c2{\psihat}^\dagger(z_2)} :\psihat^\dagger(z_1)  \psihat(z_2):  + \wick{\c2{\psihat}^\dagger(z_1) \c2{\psihat}(z_2)} \wick{\c2{\psihat}(z_1) \c2{\psihat}^\dagger(z_2) }
\end{align}$$

Now replacing some of the Wick contractions with the Green function, \\(\mathcal{G}(z_1;z_2) = -\bra{0} \psihat(z_1) \psihat^\dagger(z_2) \ket{0} = \bra{0} \psihat^\dagger(z_2) \psihat(z_1)  \ket{0} = \frac{1}{2\pi z_{21}}\\) (where \\(z_{21} = z_2 - z_1\\)) we get 

$$\begin{align}
\psihat^\dagger(z_1)\psihat(z_1)\psihat^\dagger(z_2) \psihat(z_2) =& \wick{\c2{\psihat^\dagger}(z_1) \c2{\psihat}(z_1)} \psihat^\dagger(z_2) \psihat(z_2) \\
&+ :\psihat^\dagger(z_1)\psihat(z_1) : \wick{\c2{\psihat}^\dagger(z_2) \c2{\psihat}(z_2)} + \frac{1}{z_{12}}:\psihat(z_1)\psihat^\dagger(z_2) : \\
&+ \frac{-1}{2\pi z_{21}} :\psihat^\dagger(z_1)  \psihat(z_2):  + \frac{1}{2\pi z_{12}}\frac{-1}{2\pi z_{21}}
\end{align}$$

Now moving the left hand side to the right hand side and combining it with the first term, we get 

$$\begin{align}
0 =& \left(\wick{\c2{\psihat^\dagger}(z_1) \c2{\psihat}(z_1)}  - \psihat^\dagger(z_1) \psihat(z_1) \right) \psihat^\dagger(z_2) \psihat(z_2) \\
&+ :\psihat^\dagger(z_1)\psihat(z_1) : \wick{\c2{\psihat}^\dagger(z_2) \c2{\psihat}(z_2)} + \frac{1}{2\pi z_{12}}:\psihat(z_1)\psihat^\dagger(z_2) : + \frac{1}{2\pi z_{12}} :\psihat^\dagger(z_1)  \psihat(z_2):  + \frac{1}{4\pi^2 z_{12}^2}
\end{align}$$

Now,  replacing the bracketed term with the normal ordered product, we get

$$\begin{align}
0 =& -:\psihat^\dagger(z_1) \psihat(z_1): \psihat^\dagger(z_2) \psihat(z_2) \\
&+ :\psihat^\dagger(z_1)\psihat(z_1) : \wick{\c2{\psihat}^\dagger(z_2) \c2{\psihat}(z_2)} + \frac{1}{2\pi z_{12}}\left(:\psihat(z_1)\psihat^\dagger(z_2) : +  :\psihat^\dagger(z_1)  \psihat(z_2):\right)  + \frac{1}{4\pi^2 z_{12}^2}
\end{align}$$

Lastly, combining the final two terms and moving to the left hand side, we get 

$$\begin{align}
:\psihat^\dagger(z_1) \psihat(z_1):\left( \psihat^\dagger(z_2) \psihat(z_2) - \wick{\c2{\psihat}^\dagger(z_2) \c2{\psihat}(z_2)}\right) =& \frac{1}{2\pi z_{12}}\left(:\psihat(z_1)\psihat^\dagger(z_2) : +  :\psihat^\dagger(z_1)  \psihat(z_2):\right)  + \frac{1}{4\pi^2 z_{12}^2}
\end{align}$$

Finally, writing \\(\Jhat(z) = 2\pi:\psihat^\dagger(z)\psihat(z):\\), we find 

$$\begin{align}
\Jhat(z_1) \Jhat(z_2) =& \frac{2\pi}{z_{12}}\left(:\psihat(z_1)\psihat^\dagger(z_2) : +  :\psihat^\dagger(z_1)  \psihat(z_2):\right)  + \frac{1}{z_{12}^2}
\end{align}$$

This expression can actually be written in a more useful way if we take the limit \\(z_1 \to z_2 = z\\). For this, we set \\(z_1 = z_2 + \epsilon\\). 

$$\begin{align}
\lim_{\epsilon \to 0} \left(\Jhat(z + \epsilon) \Jhat(z) - \frac{1}{ \epsilon^2}\right) =& 2\pi\lim_{\epsilon \to 0}\frac{1}{\epsilon}\left(:\psihat(z + \epsilon)\psihat^\dagger(z ) : +  :\psihat^\dagger(z + \epsilon)  \psihat(z):\right) \\
=& 2\pi \lim_{\epsilon \to 0}\frac{1}{\epsilon}\left(:\psihat^\dagger(z + \epsilon)  \psihat(z): - : \psihat^\dagger(z)\psihat(z + \epsilon) : \right) \\
=& 2\pi \left(:\partial_z\psihat^\dagger(z)\psihat(z): - : \psihat^\dagger(z)\partial_z\psihat(z) :\right) + O(\epsilon)
\end{align}$$

where the \\(O(1)\\) term cancels out between the two.


</div>

Now, we rewrite our Hamiltonian as 

$$\begin{align}
\Hhat_0 =& iv_F\int_{-\ell/2}^{\ell/2}\psihat^\dagger(x) \frac{\d}{\d x}\psihat(x) \d x \\
=&  \frac{iv_F}{2}\int_{-\ell/2}^{\ell/2} \left(\psihat^\dagger(x) \frac{\d}{\d x}\psihat(x) - \frac{\d}{\d x}\psihat^\dagger(x)  \psihat(x)\right)\d x \\
\end{align}$$

Then, the current density squared can be written as (using \\(\partial f/\partial x = i\partial f/\partial z\\); because \\(f\\) is independent of \\(z^{*}\\))

$$\begin{align}
\lim_{\epsilon \to 0} \left(\Jhat(z + \epsilon) \Jhat(z) - \frac{1}{\epsilon^2}\right) =& 2\pi i\left(\psihat^\dagger(x) \partial_x \psihat - (\partial_x\psihat^\dagger)\psihat\right)
\end{align}$$

Plugging this in to the Hamiltonian, we get 

$$\begin{align}
\Hhat_0 =& \frac{v_F}{4\pi} \int_{-\ell/2}^{\ell/2} \Jhat(x)^2 \d x \\
\end{align}$$

We have successfully bosonized our Hamiltonian! This is a bosonic current. It satisfies the following commutation relation.

<div class="example">
<b>Example:</b>
The commutator can be calculated in the following way:

$$\begin{align}
[\Jhat(x), \Jhat(y)] =& [\psihat^\dagger(x) \psihat(x), \psihat^\dagger(y) \psihat(y)] \\
=& \psihat^\dagger(x) \psihat(x) \psihat^\dagger(y) \psihat(y) - \psihat^\dagger(y) \psihat(y)\psihat^\dagger(x) \psihat(x)
\end{align}$$

We already have the Wick expansion of the first term:

$$\begin{align}
\psihat^\dagger(x)\psihat(x)\psihat^\dagger(y) \psihat(y) =& :\psihat^\dagger(x)\psihat(x)\psihat^\dagger(y) \psihat(y): \\
&+ :\wick{\c2{\psihat^\dagger}(x) \c2{\psihat}(x)} \psihat^\dagger(y) \psihat(y): + :\psihat^\dagger(x)\psihat(x) \wick{\c2{\psihat}^\dagger(y) \c2{\psihat}(y)}: \\
&+ :\wick{\c2{\psihat}^\dagger(x)\psihat(x)\psihat^\dagger(y) \c2{\psihat}(y)}: + :\psihat^\dagger(x) \wick{\c2{\psihat}(x) \c2{\psihat}^\dagger(y)} \psihat(y): \\
&+ : \wick{\c2{\psihat}^\dagger(x) \c2{\psihat}(x) \c2{\psihat}^\dagger(y) \c2{\psihat}(y)}: + :\wick{\c3{\psihat}^\dagger(x)\c2{\psihat}(x) \c2{\psihat}^\dagger(y) \c3{\psihat}(y)}:
\end{align}$$

and the second term of the commutator is obtained simply by swapping \\(x\\) and \\(y\\). In the commutator, we must assume that everything lives under a time ordering symbol. However, \\(\Jhat(x)\\) and \\(\Jhat(y)\\) do not depend on time! To ensure that they have the correct order, in the commutator we write it as (setting \\(z = \tau + ix\\) and defining \\(\delta\\) as the time component)

$$[\Jhat(x),\Jhat(y)] = \lim_{\delta \to 0}\left(\Jhat(x - i\delta)\Jhat(y) - \Jhat(y-i\delta)\Jhat(x) \right)$$

Now, with this we plug in the Wick expansions. We see that the first term of the Wick expansion is the same for both terms in the commutator. The disconnected terms also clearly cancel out. Lastly we consider the terms 

$$\begin{align}
\frac{[\Jhat(x),\Jhat(y)]}{4\pi^2} =& :\wick{\c2{\psihat}^\dagger(x-i\delta)\psihat(x-i\delta)\psihat^\dagger(y) \c2{\psihat}(y)}: + :\psihat^\dagger(x-i\delta) \wick{\c2{\psihat}(x-i\delta) \c2{\psihat}^\dagger(y)} \psihat(y): \\
& + :\wick{\c3{\psihat}^\dagger(x-i\delta)\c2{\psihat}(x-i\delta) \c2{\psihat}^\dagger(y) \c3{\psihat}(y)}: \\
& -:\wick{\c2{\psihat}^\dagger(y-i\delta)\psihat(y-i\delta)\psihat^\dagger(x) \c2{\psihat}(x)}: - :\psihat^\dagger(y-i\delta) \wick{\c2{\psihat}(y-i\delta) \c2{\psihat}^\dagger(x)} \psihat(x): \\
&- :\wick{\c3{\psihat}^\dagger(y-i\delta)\c2{\psihat}(y-i\delta) \c2{\psihat}^\dagger(x) \c3{\psihat}(x)}:
\end{align}$$

Now inserting the appropriate Green functions, we find 

$$\begin{align}
\frac{[\Jhat(x),\Jhat(y)]}{4\pi^2} =& \frac{1}{2\pi(\delta + ix - iy)} :\psihat(x-i\delta)\psihat^\dagger(y): - \frac{1}{2\pi(iy - ix - \delta)}:\psihat^\dagger(x-i\delta)\psihat(y): \\
& -\frac{1}{2\pi(\delta + iy - ix)} :\psihat(y-i\delta) \psihat^\dagger(x): + \frac{1}{2\pi(ix - \delta - iy)} :\psihat^\dagger(y-i\delta)\psihat(x): \\
&+ \frac{1}{2\pi(\delta + ix - iy)} \frac{-1}{2\pi(iy - ix - \delta)} - \frac{1}{2\pi(\delta + iy - ix)} \frac{-1}{2\pi(ix - iy - \delta)}
\end{align}$$

Now using the identity 

$$\frac{1}{a \pm i\eta} = \mathcal{P}\frac{1}{a}  \mp i\pi\delta(a)$$

we find (we can also set \\(\delta \to 0\\) inside the operators because the role of \\(\delta\\) has been used up in finding the propagators)

$$\begin{align}
\frac{[\Jhat(x),\Jhat(y)]}{4\pi^2} =& \frac{1}{2\pi}\left(\frac{-i}{x-y} + \pi\delta(x-y)\right) \left(:\psihat(x)\psihat^\dagger(y): + :\psihat^\dagger(x)\psihat(y):\right) \\
& -\frac{1}{2\pi}\left(\frac{i}{x-y} + \pi\delta(x-y)\right) \left(:\psihat(y) \psihat^\dagger(x): + :\psihat^\dagger(y)\psihat(x): \right) \\
&- \frac{1}{4\pi^2(x-y-i\delta)^2} + \frac{1}{4\pi^2(x-i+i\delta)^2}
\end{align}$$

The first two lines cancel out, and we are left with the last two lines. We extract a derivative to get 

$$\begin{align}
[\Jhat(x),\Jhat(y)] =& \frac{\d}{\d x}\left(\frac{1}{x-y-i\delta} - \frac{1}{x-y+i\delta}\right) \\
=& \frac{\d}{\d x}\left(\frac{1}{x-y} + i\pi\delta(x-y) - [\frac{1}{x-y} - i\pi\delta(x-y)]\right) \\
=& 2\pi i \frac{\d}{\d x}\delta(x-y)
\end{align}$$

This result (the RHS) is called a ``Schwinger term, or a chiral \\(U(1)\\) anomaly".


</div>

To show how this is related to a bosonic theory, let us consider the theory

$$\L = \frac{1}{2}\left(\frac{\partial\phi}{\partial t}\right)^2 - \frac{1}{2}\left(\frac{\partial\phi}{\partial x}\right)^2$$

The canonical momentum is \\(\pi = \dot{\phi}\\), and the resulting canonical commutation relation is \\([\phihat(x),\pihat(y)] = i\delta(x-y)\\). We decompose this into left and right moving parts. This is done by looking at the Euler-Lagrange equation, which is 

$$\partial_t\frac{\partial \L}{\partial(\partial_t\phi)} + \partial_x\frac{\partial\L}{\partial(\partial_x\phi)} = 0 = (\partial^2_t - \partial^2_x)\phi$$

We split up the differential operator into two parts:

$$(\partial_t+\partial_x)(\partial_t-\partial_x)\phi = 0$$

This is a wave equation in 1 dimension, and we recall that the two linearly independent solutions are the left moving and right moving parts. These are 

$$\phi(x,t) = \phi_L(x,+t) + \phi_R(x-t)$$

whereby \\((\partial_t-\partial_x)\phi_L = 0\\), and \\((\partial_t+\partial_x)\phi_R = 0\\). The Hamiltonian is given by 

$$\mathcal{H} = \frac{1}{2}\left(\frac{\partial\phi}{\partial t}\right)^2 + \frac{1}{2}\left(\frac{\partial\phi}{\partial x}\right)^2$$

Substituting \\(\partial_{\pm} = \partial_t \pm \partial_x\\) into this Hamiltonian gives us two decoupled Hamiltonians:

$$\begin{align}
\mathcal{H} =& \frac{1}{2}\left[\frac{1}{2}(\partial_+ + \partial_-)\phi\right]^2 + \frac{1}{2}\left[\frac{1}{2}(\partial_+ - \partial_-)\phi\right]^2 \\
=& \frac{1}{4}(\partial_+\phi)^2 + \frac{1}{4}(\partial_-\phi)^2 \\
=& \frac{1}{4}(\partial_-\phi_R)^2 + \frac{1}{4}(\partial_+\phi_L)^2
\end{align}$$

Note that \\(\partial_t\phi_R(x)\\) is simply an alternative notation for \\(\pi_R(x)\\). Consider the Hamiltonian density for the left-moving bosonic field only. Then, if we compute 

$$\begin{align}
[\partial_+\phihat_L(x), \partial_+\phihat_L(y)] =& [\pihat(x) + \partial_x\phihat(x), \pihat(y) + \partial_y\phihat(y)] \\
=& [\pihat(x),\partial_y\phihat(y)] + [\partial_x\phihat(x), \pihat(y)] \\
=& -\partial_y[\phihat(y),\pihat(x)] + \partial_x[\phihat(x),\pihat(y)] \\
=& -\partial_y i\delta(y-x) + \partial_x i\delta(x-y) \\
=& 2i\frac{\d}{\d x}\delta(x-y)
\end{align}$$

We see that this is almost the same result as the fermionic currents. Therefore, making the identification \\(\Jhat_L(x) = \sqrt{\pi}\partial_+\phihat_L(x)\\). This identification is possible because the commutation relations and Hamiltonian are the same. Thus the operators are the same with appropriate boundary conditions. To determine what these boundary conditions are, we should compute the spectra of the two different cases. In the fermionic case, let's choose boundary conditions 

$$\psi(\ell/2) = -\psi(-\ell/2), \quad k_n = \frac{2\pi}{\ell}\left(n + \frac{1}{2}\right),\quad n\in \ZZ$$

The dispersion relation is given by \\(E = -v_F k\\), so the minimum energy state of charge \\(Q\\) (relative to the ground state) has \\(Q\\) extra electrons on top of the Fermi sea. They will be populated starting with the smallest value of \\(k\\). We find 

$$E(Q) = \frac{2v_F\pi}{\ell} \sum_{n=0}^{Q-1} \left(n + \frac{1}{2}\right) = \frac{v_F\pi}{\ell}Q^2$$

Now, what happens if we have particle-hole excitations on top of the charge \\(Q\\) ground state we just found? Well, if we move \\(n_m\\) electrons by \\(m\\) levels (move them all together), then \\(n_{m-1}\\) electrons by \\(m-1\\) levels, etc, then the energy is 

$$E = \frac{2\pi v_F}{\ell}\left(\frac{1}{2}Q^2 + \sum_{m=1}^\infty n_m m\right)$$

Now, let's consider the bosonic spectrum. If we use periodic boundary conditions, then we have that 

