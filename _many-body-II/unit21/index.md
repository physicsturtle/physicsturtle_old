---
layout: lesson
title: Lecture March 15
dept: physics
course: many-body-II
unit: unit21
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 21
---
Now compare Green functions, commutators, and Hamiltonians of free boson and free fermion models (we will extend to interacting fermion model later)

We will also show that we can identify \\(\phi^\dagger_L\phi_L\sim \partial_+\phi\\), and \\(\phi^\dagger_R\phi_R\sim \partial_-\phi\\).

Mode expansion: [for other approaches to derivative bosonization, see Mahan or Haldane, phys rev lett 47, 1840, 1981]

$$$$\begin{align}\psi_R(x) = \int_{-\Lambda}^\Lambda\phi_R(k) e^{ikx}\frac{dk}{2\pi} = \int_0^\Lambda(a_k e^{ikx}+ b_k^\dagger e^{-ikx})\frac{dk}{2\pi}\end{align}$$$$

where \\(a_k =\psi_R(k)\\) and \\(b_k^\dagger = \psi_R(-k)\\), \\(k > 0\\)

insert picture here

\\(b^\dagger_k \psi(-k)\\) creates a hole at wave vector \\(k_F - k\\) \\((k>0)\\)

positron in particle physics

Note:

$$$$\begin{align}\{a_k,a_{k'}^\dagger\} = \{b_k,b_{k'}^\dagger\} = 2\pi\delta(k-k')\end{align}$$$$

\\(\{\psi_R(x),\psi_R^\dagger(y)\} = \delta_\Lambda(x-y)\\)

where \\(\delta_{\Lambda}\\) is a dirac \\(\delta\\) function broadened by \\(1/\Lambda\\).

\\(a_k(t) = e^{-ikt}a_k\\) so

$$$$\begin{align}\psi_R(t,x) = \int_0^\Lambda(a_k e^{-ik(t-x)}+b_k^\dagger e^{ik(t-x)})\frac{dk}{2\pi}\end{align}$$$$

similarly, 

$$$$\begin{align}\psi_L(t,x) = \int_{-\Lambda}^0 (a_k e^{ik(t+x)} + b_k^\dagger e^{-ik(t+x)})\frac{dk}{2\pi}\end{align}$$$$

Fermionic green function (time correlation function):

$$$$\begin{align}\bra{0}\psi^\dagger_R(t,x)\psi_R(0,0)\ket{0} = \int_0^\Lambda e^{-ik(t-x)}\frac{dk}{2\pi}\end{align}$$$$

\\(a_k\\) on left.

Note:

\\(a_k\ket{0} = b_k\ket{0} = 0\\), \\(\bra{0}a_{k'}^\dagger a_k\ket{0} = 2\pi\delta(k-k')\\)

Convenient again to replace cutoff \\(\Lambda\\) by convergence factor \\(e^{-\eta k}\\), \\(\eta\sim 1/\Lambda\\). 

$$$$\begin{align}\bra{0}\psi_R^\dagger(t,x)\psi_R(0,0)\ket{0} = \int_0^\infty e^{-ik(t-x-i\eta)}\frac{dk}{2\pi} = \frac{1}{2\pi i(t-x-i\eta)} = \bra{0}\psi_R(t,x)\psi_R^\dagger(0,0)\ket{0}\end{align}$$$$

Get similar results using \\(\Lambda\\) cut-off for \\(\Lambda|t-x|\gg 1\\) but this is more convenient.

Similarly, 

$$$$\begin{align}\bra{0}\psi_L^\dagger(t,x)\psi_L(0,0)\ket{0} = \frac{1}{2\pi i(t+x-i\eta)} = \bra{0}\psi_L(t,x)\psi^\dagger_L(0,0)\ket{0}\end{align}$$$$

Just like \\(x\to -x\\) 

Consider normal ordered operators where we move all creation operators to the left of the nanihilation operators. 

$$$$\begin{align}J_R(t,x) = \psi_R^\dagger(t,x)\psi_R(t,x) = \psi_R^\dagger\psi_R - \bra{0}\psi_R^\dagger\psi_R\ket{0}\end{align}$$$$

Then 

$$\begin{align}
\bra{0}J_R(t,x)J_R(0,0)\ket{0} =& \bra{0}:\psi_R^\dagger(t,x)\psi_R(t,x): : \psi_R^\dagger(0,0)\psi_R(0,0):\ket{0}\\
=& \bra{0}\psi^\dagger_R(t,x)\psi_R(0,0)\ket{0}\bra{0}\psi_R(t,x)\psi_R^\dagger(0,0)\ket{0}\\
=& -\left(\frac{1}{2\pi(t-x-i\eta)}\right)^2 \\
=& \frac{1}{4\pi}\bra{0}\partial_i\phi(t,x)\partial_-\phi(0,0)\ket{0}
\end{align}$$

First hint of bosonization! 

Gould we identify \\(j_F = :\phi_R^\dagger\phi_R:\\) with \\(\frac{1}{\sqrt{4\pi}}\partial_-\phi\\)?

Actually, the free boson Hamiltonian is quadratic in \\(\partial_{\p}m\phi\\), 

$$$$\begin{align}H = \frac{1}{2}(\partial_t \phi)^2 + \frac{1}{2}(\partial_x\phi)^2 = \frac{1}{4}(\partial_-\phi)^2 + \frac{1}{4}(\partial_+\phi)^2 = H_R + H_L\end{align}$$$$

Free fermion Hamilonian is

$$$$\begin{align}H = -i\psi_R^\dagger\partial_x\psi_R + i\psi^\dagger_L\partial_x\psi_L \stackrel{?}{=} \pi J_L^2 + \pi J_L^2\end{align}$$$$

Amazingly, this is true and is the key to bosonization. Naively, \\(J_R(x)^2\sim \psi^\dagger_R(x)\psi_R^\dagger(x)\psi_R(x)\psi_R(x)\\) is zero due to Fermi statistics, \\(\psi_R(x)^2= 0\\).

But we need to be careful about operator order. This is very singular so let's consider 

$$$$\begin{align}\lim_{\epsilon\to 0}J_R(x)J_R(x+\epsilon)\end{align}$$$$

this seems natural in a CMP context where \\(\epsilon\\) could be a lattice constant, 

$$$$\begin{align}
J_R(x)J_R(x+\epsilon) = :\psi_R^\dagger(x)\psi_R(x)::\psi^\dagger_R(x+\epsilon)\psi_R(x+\epsilon):
\end{align}$$$$

Let's write this as 

$$$$\begin{align}
:\psi^\dagger_R(x)\psi_R(x)\psi^\dagger_R(x+\epsilon)\psi_R(x+\epsilon): + \text{corrections}
\end{align}$$$$

Corrections arise from bringing creation operator part of \\(\psi^\dagger_R(x+\epsilon)\\) to left of annihilation operator part of \\(\psi_R(x)\\), then bginging creation operator part of \\(\psi^\dagger_R(x+\epsilon)\\) to left of annihilation operator part of \\(\psi_R(x)\\), then bringing creation operator part of \\(\psi_R(x+\epsilon)\\) to left of annihilation operator part of \\(\psi^\dagger_R(x)\\).

The completely normal ordered product vanishes as \\(\epsilon\to 0\\). Because creation operators are next to creation operators and annihilation operators are next to annihilation operators.

The correction from bringing creation part of \\(\psi^\dagger_R(x+\epsilon)\\) to left of annihilation part of \\(\psi_R(x)\\) is \\(\bra{0}\psi_R(x)\psi^\dagger_R(x+\epsilon)\ket{0}\\). 

$$$$\begin{align}
x:\psi^\dagger_R(x)\psi_R(x+\epsilon):
\end{align}$$$$

altogether, we have

$$\begin{align}
J_R(x)J_R(x+\epsilon) =& :\psi^\dagger_R(x)\psi_R(x)\psi^\dagger_R(x+\epsilon)\psi_R(x+\epsilon): + :\psi^\dagger_R(x)\psi_R(x+\epsilon):\bra{0}\psi_R(x)\psi^\dagger_R(x+\epsilon)\ket{0} \\
&+ :\psi^\dagger_R(x+\epsilon)\psi_R(x):\bra{0}\psi_R(x+\epsilon)\psi^\dagger_R(x)\ket{0} + \bra{0}\psi^\dagger_R(x)\psi_R(x+\epsilon)\ket{0}\bra{0}\psi_R(x)\psi^\dagger_R(x+\epsilon)\ket{0}
\end{align}$$

Note no minus signs due to order written, 

$$$$\begin{align}J_R(x)J_R(x+\epsilon) = :J_R J_R:\frac{1}{2\pi i\epsilon}(:\psi^\dagger_R(x)\psi_R(x+\epsilon): - :\psi^\dagger_R(x+\epsilon)\psi_R(x):) - \left(\frac{1}{2\pi\epsilon}\right)^2\end{align}$$$$

as \\(\epsilon\to 0\\) we got a derivative. 

$$$$\begin{align}\lim_{\epsilon\to 0}[J_R(x))J_R(x+\epsilon) + \left(\frac{1}{2\pi\epsilon}\right)^2 = \frac{1}{2\pi i}\left(:\psi^\dagger_R \frac{d}{dx}\psi_R: - :\frac{d}{dx}\psi^\dagger_R \psi_R:\right)]\end{align}$$$$

so \\(H_R = \pi J_R^2\\) as needed (up to \\(c\\)-number)

Similarly, $$$$\begin{align}J_L(x)J_L(x+\epsilon) = :J_L(x)J_L(x+\epsilon): - \frac{1}{2\pi i}(:\psi^\dagger_L\psi_L(x+\epsilon): - :\psi^\dagger(x+\epsilon)\psi_L(x):) - \left(\frac{1}{2\pi\epsilon}\right)^2\end{align}$$$$

Extra minus sign became 

$$$$\begin{align}\bra{0}\psi_L(x)\psi^\dagger_L(x+\epsilon)\ket{0} = -\frac{1}{2\pi i\epsilon} = -\bra{0}\psi_R(x)\psi^\dagger_R(x+\epsilon)\ket{0}\end{align}$$$$

so

$$$$\begin{align}\lim_{\epsilon\to 0}[J_L(x)J_L(x+\epsilon) + \left(\frac{1}{2\pi\epsilon}\right)^2] = \frac{1}{\pi}H_L\end{align}$$$$

$$$$\begin{align}H_L = \pi J_L^2\end{align}$$$$

(drop \\(c\\) numbers ) consistent with \\(J_R = \frac{1}{\sqrt{4\pi}}\partial_i\phi\\), \\(J_L = -\frac{1}{\sqrt{4\pi}}\partial_+\phi\\). The sign convention is arbitrary - just fixes the sign of \\(\phi_R\\) and \\(\phi_L\\)

commutators of these sets of operators also correspond \\([J_R(x), J_R(y)]\\) (at equal times) is clearly zero except at \\(x\to y\\). We can use our previous expression in normal ordered quantities - no contribution from operator parts:

$$\begin{align}
[J_R(x), J_R(y)] =& \bra{0}[J_R(x),J_R(y)]\ket{0} \\
=& -\left(\frac{1}{2\pi(x-y+i\eta)}\right)^2 + \left(\frac{1}{2\pi(y-x+i\eta)}\right)^2
\end{align}$$

Note: only in term distinguishes 2 terms - as I showed last lecture, this is 

$$\begin{align}
\frac{d}{dx}\left(\frac{1}{(2\pi)^2(x-y+i\eta)} - \frac{1}{(2\pi)^2(x-y-i\eta)}\right) = -\frac{i}{2\pi}\frac{d}{dx}\delta(x-y)
\end{align}$$

This is 

$$$$\begin{align}
\frac{1}{4\pi}[\partial_-\phi(x),\partial_-\phi(y)]
\end{align}$$$$

so \\(J_R(x)\\) and \\(\frac{1}{\sqrt{4\pi}}\partial_-\phi(x)\\)

Have same commutator and same (quantie...?) Hamiltonian. 

Therefore, the models are equivalent, i.e. commutation relations determine mode expansion - both are harmonic oscillator models - particle-hold pair \\(\leftrightarrow\\) boson 

\\(J_R(x)\\), \\(J_L(x)\\) are charge densities of left and right movers. 

$$$$\begin{align}
\int J_R(x)dx = \int_0^\Lambda(a^\dagger_k a_k - b^\dagger_k b_k)\frac{dk}{2\pi}
\end{align}$$$$

$$$$\begin{align}
\int J_L(x) dx = \int_{-\Lambda}^0(a^\dagger_k a_k - b^\dagger_k b_k)\frac{dk}{2\pi}
\end{align}$$$$

\\(\rho = J_L + J_R\\) is the charge density, and \\(J = J_R - J_L\\) is the current density. REcall that we are workign in units where \\(v_F = 1\\).

ALl excitations travel at the same speed, so charge and density are simply relded?

very importantly, we can extend bosonization ?? to express \\(\psi_R(x)\\), \\(\psi_L(x)\\) in terms of \\(\phi_R(x)\\), \\(\phi_L(x)\\)

We can determine correct expression by considering commutator 

$$\begin{align}
[J_R(x),\psi_R(y)] =& [\psi^\dagger_R(x)\psi_R(x),\psi_R(y)]\\
=& \{\psi_R(y),\psi^\dagger_R(x)\}\psi_R(x) \\
=& -\delta(x-y)\psi_R(x)
\end{align}$$

can we find an operator, written in terms of \\(\phi_R(y)\\), which has this commutator with 

$$$$\begin{align}
\frac{1}{\sqrt{4\pi}}\partial_-\phi_R(x)?
\end{align}$$$$

To find it, consider commutator

$$\begin{align}
[\partial_-\phi_R(x),\phi_R(y)] =& [\partial_-\phi_R(x),\phi_R(y) + \phi_L(y)] \\
=& [\partial_r\phi-\partial_x\phi,\phi] \\
=& -i\delta(x-y)
\end{align}$$

can we think of some function \\(f(\phi_R)\\) so

$$$$\begin{align}\frac{1}{\sqrt{4\pi}}[\partial_-\phi_R(x),f(\phi_R(y))] = -\delta(x-y)f[\phi_R(x)]?\end{align}$$$$

$$\begin{align}
\frac{1}{\sqrt{4\pi}}[\partial_-\phi_R(x),\exp(-i\sqrt{4\pi}\phi_R(y))] =& \frac{1}{\sqrt{4\pi}}\sum_{n=0}^\infty \frac{(-i\sqrt{4\pi})^n}{n!}[\partial_-\phi_R(x),(\phi_R(y))^n] \\
=& -i\frac{\delta(x-y)}{\sqrt{4\pi}}\sum_{n=1}^\infty \frac{(-i\sqrt{4\pi})^2}{n!}n[\phi_R(y)]^{n-1} \\
=& -\delta(x-y)\exp(-i\sqrt{4\pi}\phi_R(x))
\end{align}$$

so we conclude that

$$$$\begin{align}\phi_R(x)\propto e^{-i\sqrt{4\pi}\phi_R(x)}\end{align}$$$$

constant of proportionality not yet determined. Let's check Green function

$$$$\begin{align}\left<e^{i\sqrt{4\pi}\phi_R(t,x)}e^{-i\sqrt{4\pi}\phi_R(0,0)}\right>\end{align}$$$$

$$$$\begin{align}\alpha\propto \left<\phi^\dagger_R(t,x)\phi_R(0,0)\right> = \frac{1}{2\pi i(t-x-i\eta)}\end{align}$$$$

a convenient way ot calculating this is to just calculate

$$$$\begin{align}\left<e^{i\beta\phi(t,x)}e^{-i\beta\phi(0,0)}\right>\end{align}$$$$

for arbitrary \\(\beta\\). Then observe it must factorize:

$$$$\begin{align}\propto \left<e^{i\beta\phi_R(t,x)}e^{-i\beta\phi_R(0,0)}\right>\left<e^{i\beta\phi_L(t,x)}e^{-i\beta\phi_L(0,0)}\right> = F(t-x) F(t+x)\end{align}$$$$

We can then extract \\(F(t-x)\\). Just do calculation for imaginrary time

$$$$\begin{align}\left<e^{i\beta\phi(\tau,x)}e^{-i\beta\phi(0,0)}\right> = \frac{1}{Z}\int e^{-\frac{1}{2}\int(\left(\frac{d\phi}{d\tau}\right)^2 + \left(\frac{d\phi}{dx}\right)^2 + i\beta\phi(\tau,x) - i\beta\phi(0,0))d^2x}\D\phi\end{align}$$$$

where \\(Z = \int e^{-S_0}\D\phi\\). More generally, consider

$$$$\begin{align}\left<e^{i\int \phi(\tau,x)f(\tau,x)d^2x}\right> = \left< e^{i\int \tilde{\phi}(\omega,k)\tilde{f}(-\omega-k)\frac{d\omega dk}{(2\pi)^2}}\right>\end{align}$$$$

for arbitrary function \\(f(\tau,x)\\), where \\(\tilde{\phi}\\), \\(\tilde{f}\\), are Fourier transforms. 

$$$$\begin{align}S = \frac{1}{2}\int |\tilde{\phi}(\omega,k)|^2(\omega^2 + k^2)\frac{d\omega dk}{(2\pi)^2}\end{align}$$$$

gen an independence gaussian integral for each Fourier mode, use

$$$$\begin{align}
\frac{\int e^{-ax^2/2 + ibx}dx}{\int e^{-ax^2/2}dx} = e^{-b^2/2a}
\end{align}$$$$

\section{Lecture March 20}

$$\begin{align}
\left<e^{i\int \tilde{\phi}\tilde{f}\frac{d\omega dk}{(2\pi)^2}}\right> =& e^{-\frac{1}{2}\int \frac{|\tilde{f}(\omega,k)|^2}{\omega^2+k^2}\frac{dkd\omega}{(2\pi)^2}} \\
=& \exp(-\frac{1}{2}\int f(\tau,x)G(\tau-\tau',x-x')f(\tau',x')d\tau dx d\tau' dx')
\end{align}$$

where \\(G(\tau,x) = \int \frac{e^{i(\omega\tau + kx)}}{\omega^2+k^2} \frac{d\omega dk}{(2\pi)^2}\\)

This is the Green function for \\(\phi\\) that we calculated last lecture. This can be doing \\(\omega\\) integral by contour method. 

$$$$\begin{align}G(\tau,x) = \frac{1}{4\pi}\int e^{-|k||\tau|+ikx}\frac{dk}{|k|}\end{align}$$$$

as we saw before, this is infrared divergent, but we will see that only \\(G(\tau,x) - G(0,0)\\) is needed. To calculate

$$$$\begin{align}\left<e^{i\beta(\phi(\tau,x)-\phi(0,0))}\right>\end{align}$$$$

we choose

$$$$\begin{align}
f(\tau',x') = \beta(\delta(\tau'-\tau)\delta(x'-x)-\delta(\tau')\delta(x'))
\end{align}$$$$

so 

$$\begin{align}
\left<e^{i\beta(\phi(\tau,x) - \phi(0,0))}\right> =& e^{\beta^2(G(\tau,x) - G(0,0))} \\
=& e^{-\beta^2\log(\Delta^2(\tau^2+x^2))/4\pi}
\end{align}$$

for \\(\Lambda^2(\tau^2+x^2)\gg 1\\), \\(\Lambda\\) is the cutoff. So

$$$$\begin{align}\left<e^{i\beta\phi_R(\tau,x)} e^{-i\beta\phi(\tau,x)}\right> = \left(\frac{1}{\Lambda(\tau-ix)}\right)^{\beta^2/4\pi}\end{align}$$$$

we had \\(\beta = \sqrt{4\pi}\\), so it simplifies. This is the correct answer, and becomes

$$$$\begin{align}\frac{1}{i\Lambda(t-x)}\end{align}$$$$

for real time. Similarly, 

$$$$\begin{align}\psi_L\propto e^{i\sqrt{4\pi}\phi_L}\end{align}$$$$

Note opposite sign in exponent due to sign change for current. 

$$$$\begin{align}T_L = \frac{1}{\sqrt{4\pi}}\partial_+\phi\end{align}$$$$

could these formulas be considered with anticommutation relations for Fermion fields? Check

$$$$\begin{align}\{\psi_R(x),\psi_R(y)\} = 0\end{align}$$$$

with 

$$$$\begin{align}\psi_R(x)\propto e^{-i\sqrt{4\pi}\phi_R(x)}\end{align}$$$$

what is 

$$$$\begin{align}[\phi_R(x),\phi_R(y)]?\end{align}$$$$

it must be zero when \\(x=y\\), but not zero in general since we showed

$$\begin{align}
\partial_-\phi(t,x),\partial_-\phi(t,y)] =& -2i\frac{d}{dx}\delta(x-y) \\
=& 4[\partial_x\phi_R,\partial_y\phi_R]
\end{align}$$

where 

$$$$\begin{align}
[\phi_R(x),\partial_y\phi_R(y)] = -\frac{i}{2}\delta(x-y)
\end{align}$$$$

so 

$$$$\begin{align}
[\phi_R(x),\phi_R(y)] = \frac{i}{4}\sgn(x-y)
\end{align}$$$$

thus

$$$$\begin{align}\psi_R(x)\psi_R(y) \not= \psi_R(y)\psi_R(x)\end{align}$$$$

instead, we get a minus sign! check on HW 5. Now all interactions to fermion model, 

$$$$\begin{align}H_\text{int} = u\int J_L(x)J_R(x)dx\end{align}$$$$

which is the only exactly maginarl term. Bosonize:

$$$$\begin{align}H = \frac{1}{2}(\partial_+\phi)^2 + \frac{1}{4}(\partial_-\phi)^2 - \frac{4}{4\pi}\partial_+\partial_-\phi\end{align}$$$$

still quadratic in \\(\phi\\). Not worrying about effects of higher order in \\(u\\) Lagrangian is

$$\begin{align}
\L =& \frac{1}{2}[(\partial_t\phi)^2 - (\partial_x\phi)^2] + \frac{u}{4\pi}[(\partial_t\phi)^2 - (\partial_x\phi)^2] \\
=& \frac{1}{2}\left(1+\frac{u}{2\pi}\right)[(\partial_t\phi)^2 - (\partial_x\phi)^2]
\end{align}$$

We may restore standard form of \\(\L\\) by rescaling \\(\phi\\). Let \\(\tilde{\phi} = \sqrt{1+\frac{u}{2\pi}}\phi\\). 

$$$$\begin{align}\L = \frac{1}{2}[(\partial_t\tilde{\phi})^2 - (\partial_x\tilde{\phi})^2]\end{align}$$$$

Let \\(\tilde{\phi} = e^{-\gamma}\phi\\), \\(\gamma\\) is a smooth function of \\(u\\), \\(\gamma = -u/4\pi + O(u^2)\\). 

This method doesn't determine \\(\gamma(u)\\) exactly - depends on irrelevant operator effects - but \\(\gamma(u)\\) is known exactly for nearest neighbour tight binding model from Bethe ansatz solution

To preserve commutation relations \\(\tilde{\pi} = e^\gamma \pi\\).

Rescaling affects bosonization identities - this giving nontrivial green functions in fermion theory. TO get \\(\phi_{R/L}\\) in terms of \\(\tilde{\phi}\\), we just write \\(\phi_{R/L}\\) in terms of \\((\phi,\pi)\\)

$$$$\begin{align}\partial_x\phi_R = -\frac{1}{2}(\partial t - \partial_x)\phi = -\frac{1}{2}(\pi - \partial_x\phi)\end{align}$$$$

$$$$\begin{align}\phi_R(x) = -\frac{1}{2}\int_{-\infty}^x \pi(x')dx' + \frac{1}{2}\phi(x)\end{align}$$$$

similarly, 

$$$$\begin{align}
\phi_L(x) = \frac{1}{2}\int_{-\infty}^x\pi(x')dx' + \frac{1}{2}\phi(x)
\end{align}$$$$

$$$$\begin{align}
\phi_{R/L} = \mp\frac{1}{2}e^{-\gamma}\int_{-\infty}^x\tilde{\pi}(x')dx' + \frac{1}{2}e^\gamma \tilde{\phi}
\end{align}$$$$

Rewrite in terms of \\(\tilde{\phi}_R\\), \\(\tilde{\phi}_L\\), so \\(\tilde{\phi} = \tilde{\phi}_R + \tilde{\phi}_L\\)

$$$$\begin{align}\phi_{R/L} = \mp \frac{1}{2}e^{-\gamma}(-\tilde{\phi}_R + \tilde{\phi}_L) + \frac{1}{2}e^\gamma(\tilde{\phi}_R + \tilde{\phi}_L)\end{align}$$$$

$$$$\begin{align}
\begin{pmatrix}
	\phi_R \\ \phi_L
\end{pmatrix} = \begin{pmatrix}
	\cosh\gamma & \sinh\gamma \\ \sinh\gamma & \sinh\gamma 
\end{pmatrix} \begin{pmatrix}
	\tilde{\phi}_R \\ \tilde{\phi}_L
\end{pmatrix}
\end{align}$$$$

This preserves commutation relations 

$$$$\begin{align}[\phi_R(x)\,\phi_R(y)] = -[\phi_L(x),\phi_L(y)] = \frac{i}{4}\sgn(x-y)\end{align}$$$$

$$$$\begin{align}\phi_R\propto e^{-i\sqrt{4\pi}[\tilde{\phi}_R \cosh\gamma + \tilde{\phi}_L\sinh\gamma]} \end{align}$$$$

\\(\tilde{\phi}_R,\tilde{\phi}_L\\) are just free boson fields with normal green functions. 

$$\begin{align}
\left<\psi_R^\dagger(t,x) \psi_R(0,0)\right> \propto & \left<e^{i\sqrt{4\pi}\cosh\gamma\tilde{\phi}_R(t,x)} e^{-i\sqrt{4\pi}\cosh\gamma\tilde{\phi}_R(0,0)}\right>\left<e^{i\sqrt{4\pi}\sinh\gamma\tilde{\phi}_L(t,x)}e^{-i\sqrt{4\pi}\sinh\gamma\tilde{\phi}_L(0,0)}\right> \\
\propto & \left(\frac{1}{t-x-i\eta}\right)^{\cosh^2\gamma}\left(\frac{1}{t+x-i\eta}\right)^{\sinh^2\gamma}
\end{align}$$

Fourier transform to get spectral density. Check that at \\(\gamma = 1\\) (free Fermion), 

$$$$\begin{align}G(\omega,k)\propto \int_{-\infty}^\infty \int_{-\infty}^\infty \frac{e^{i(\omega t + kx)}}{t-x-i\eta}dxdt\end{align}$$$$

let \\(t_{\p}m = t\pm x\\). 

$$$$\begin{align}G(\omega,k) \propto \int_{-\infty}^\infty \int_{-\infty}^\infty \frac{e^{i(t_-(\omega-k)/2 + t_+(\omega+k)/2)}}{t - i\eta} dt_+ dt_- \propto \delta(\omega + k)\theta(\omega - k) = \delta(\omega + k)\theta(\omega) \quad(since k < 0)\end{align}$$$$

\\(\psi_R(k)\\) creates a hole with momentum \\(k < 0\\) and energy \\(|k| = -k\\). 

insert figure here

Fermi liquid theory result - spectral function has a pole at \\(\omega = \epsilon(k)\\) at \\(T\to 0\\), \\(\epsilon(k) \to 0\\).

Note: \\(t_-\\) integral has a simple pole at \\(t_- = i\eta\\). 

Close the contour in the upper half plane for \\(\omega_- > 0\\). At \\(\gamma\not=0\\), \\(t_{\p}m\\) integrals have branch cuts;

$$$$\begin{align}\int \frac{e^{it_-(\omega-k)/2}}{(t_--i\eta)^{\cosh^2\gamma}}dt_i\propto \theta(\omega-k)(\omega-k)^{(\cosh^2\gamma - 1)}\end{align}$$$$

so

$$$$\begin{align}G(\omega,k)\propto \frac{\theta(\omega+k)\theta(\omega-k)(\omega-k)^{(\cosh^2\gamma - 1)}}{(\omega+k)^{1-\sinh^2\gamma}}\end{align}$$$$

Pole is replaced by power law singularity;

$$$$\begin{align}
\propto \frac{1}{(\omega+k)^\eta},\qquad \eta - 1-\sin^2\gamma = 1-\left(\frac{u}{4\pi}\right)^2
\end{align}$$$$

This is a non-fermi liquid because of no pole at \\(T = \epsilon = 0\\). This has experimental consequence for density of states measured in tunneling experiments among other things.

\section{RG for Interacting Fermions in \\(d = 2\\) and \\(d = 3\\)}
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

