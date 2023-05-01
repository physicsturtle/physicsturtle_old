---
layout: lesson
title: Effective Action of the Kondo Model
dept: physics
course: many-body-II
unit: unit13
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 13
---
In typical experiments, \\(J\nu\ll 1\\), so we can use perturbation theory, inspired by the RG.

We integrate out momentum components \\(\bar{\psi}_{\k,\omega,\sigma}\\), \\(\psi_{\k,\omega,\sigma}\\) with large \\(\epsilon_{\k}\\) and calculate the effective Hamiltonian and action. For small \\(J\nu\\), changes are initially small, but as width of remaining energy band goes to zero, they start to blow up. At small cutoff \\(\Lambda\\) we can linearize the dispersion relation at the Fermi surface

$$$$\begin{align}
\epsilon(\k) \sim v_F (k - k_F),
\end{align}$$$$

and the model becomes approximately equivalent to a relativistic model, as we will discuss. Note that we do not integrate out \\(\textbf{S}\\) in weak coupling RG, but rather only some momentum components \\(\chat_{\k\omega\sigma}\\). In a sense, we do integrate out \\(\textbf{S}\\) in strong coupling RG, to be discussed later. It is possible to write a path integral representation of spin using spin coherent states, but this isn't really necessary or useful, so we will use a hybrid approach: path integral for fermions, but quantum trace for spin \\(\textbf{S}\\). Our operators act on the tensor product of the Fermionic Fock space with \\(\chat^2\\), where the latter describes the spin of the impurity. This tells us that the appropriate resolution of identity here is

$$$$\begin{align}
\1 = \left(\prod_{\alpha,\k} e^{-\bar{\psi}_\alpha(\k)\psi_\alpha(\k)}\ket{\psi_\alpha(\k)}\bra{\bar{\psi}_\alpha(\k)}d\bar{\psi}_\alpha(\k)d\psi_\alpha(\k)\right)\otimes\sum_\sigma\ket{\sigma}\bra{\sigma},\end{align}$$$$

where \\(\sigma = \uparrow,\downarrow\\) labels impurity spin states. We insert the identity \\(\1\\) in between the product of the \\(N\\) time slices of the Hamiltonian. This gets rid of the fermion operators, but spin operators remain. Thus the partition function becomes

$$$$\begin{align}
Z = \sum_\sigma\bra{\sigma}\prod_{i=N}^1 \exp\left(\sum_{\k,\alpha}\bar{\psi}_{\k}(\tau_i)(\psi_{\k}(\tau_i) - \psi_{\k}(\tau_{i-1})) -\epsilon H(\bar{\psi}(\tau_{i+1}),\psi(\tau_i),\textbf{S})\right)[d\bar{\psi}(\tau_n),d\psi(\tau_n)]\ket{\sigma}
\end{align}$$$$

Note: We reexponentiated \\(1-\epsilon H\\) factors but did not replace product of exponentials by exponential of sum. This wouldn't be legitimate because psin operators don't commute with each other. We can take care of this by giving spin operators an imaginary time label \\(\textbf{S}(\tau_i)\\) and writing

$$$$\begin{align}
Z = \tr_S T\int \exp\left(-\int_0^\beta \left(\sum_{\k,\sigma}\bar{\psi}_{\k,\sigma}\frac{d\psi_{\k,\sigma}}{d\tau} + H(\bar{\psi}(\tau)\psi(\tau),\textbf{S})\right)d\tau \right) \D\bar{\psi}(\k)\D\psi(\k)
\end{align}$$$$

where we suppressed \\(\k\\), at labels on \\(\psi_\alpha(\k,\tau)\\). \\(T\\) is the time ordering symbol for spin operators only, latest on the left. The trace over conduction electrons has already been performed, hence the path integral, and we leave the trace over the impurity spin separate. We denote the argument of the exponential by \\(S\\), the effective action:

$$$$\begin{align}
S = \int_0^\beta \left(\sum_{\k,\sigma}\bar{\psi}_{\k,\tau,\sigma}\partial_\tau \psi_{\k,\tau,\sigma} + H(\bar{\psi}(\tau)\psi(\tau),\textbf{S})\right) d\tau,
\end{align}$$$$

and split this effective action into two parts. There is the free part, \\(S_0\\), and the interacting part, 

$$$$\begin{align}
S_0 = \int_0^\beta\left(\sum_{\k,\sigma}\bar{\psi}_{\k,\sigma}\frac{d\psi_{\k,\sigma}}{d\tau} + \sum_{\k,\sigma} \epsilon(\k)\bar{\psi}_{\k,\sigma}(\tau)\psi_{\k,\sigma}(\tau)\right) d\tau 
\end{align}$$$$

$$$$\begin{align}
S_\text{int} = \frac{J}{N_s}\sum_{\k,\k',\alpha,\beta} \int_0^\beta \bar{\psi}_{\k,\alpha}(\tau)\boldsymbol{\sigma}_{\alpha\beta}\psi_{\k,\beta}(\tau)\textbf{S}(\tau) d\tau 
\end{align}$$$$

Only with time ordering can we replace the product of exponentials by exponential of sum (see notes on many-body physics for this). Note: spin operators don't actually depend on time but we must order them by time. 

$$$$\begin{align}
T_\tau [\hat{S}^x(\tau_1)\hat{S}^x(\tau_2)] = (\hat{S}^x)^2 = \frac{1}{4}I
\end{align}$$$$

$$$$\begin{align}
T_\tau [\hat{S}^x(\tau_1)\hat{S}^y(\tau_1)] = \begin{cases}
\hat{S}^x \hat{S}^y = \frac{i}{2}\hat{S}^z, & \tau_1 > \tau_2 \\
\hat{S}^y \hat{S}^x = -\frac{i}{2}\hat{S}^z, &\tau_1 < \tau_2
\end{cases}
\end{align}$$$$

We use bosonic sign convention for time ordering for spin operators. The general form of the time ordering relation is given by

$$$$\begin{align}
T_\tau[\hat{S}^a(\tau_1)\hat{S}^b(\tau_2)] = \frac{1}{4}\delta^{ab}I + \sgn(\tau_1-\tau_2)\frac{i}{2}\epsilon^{abc}\hat{S}^c.
\end{align}$$$$

We will Taylor expand \\(\Hhat_\text{int}\\) term in exponential to do perturbation theory in \\(J\nu\\). We must time order \\(\hat{S}^a\\) in each term. Note that, in interaction picture, \\(\textbf{S}(\tau) = \textbf{S}\\) since \\(\Hhat_0\\) is independent of \\(\textbf{S}\\). We now calculate renormalization of \\(S_\text{eff}\\) by integrating out modes from Fermi surface. Following Shankar, let \\(\psi_>\\), \\(\bar{\psi}_>\\), represent modes with large \\(|\epsilon_{\k}|\\) and \\(\psi_<\\), \\(\bar{\psi}_<\\) modes with small \\(|\epsilon_{\k}|\\).  In general, we will have an initial cut off \\(D\\) and a reduced cut off \\(D'\\) such that

$$$$\begin{align} \label{eq:slow_fast_fields}
\psi(\k) = \begin{cases} 
\psi_>(\k), & D' < |\epsilon_{\k}| < D \\
\psi_<(\k), & |\epsilon_{\k}| < D'.
\end{cases}
\end{align}$$$$

This also means that we can split up the path integral so that \\(\D\psi(\k)\\) is split up into the product over states satisfying the first of the conditions in \eqref{eq:slow_fast_fields}.

$$$$\begin{align}
\int \D\bar{\psi}\D\psi = \int \D\bar{\psi}_< \D\psi_< \D\bar{\psi}_> \D\psi_>.
\end{align}$$$$

where we recall that \\(\D \psi_<\\) is interpreted as 

$$\D \psi_< = \prod_{\k,\sigma}^{|\epsilon(\k)| < D'} d\psi(\k,\sigma)$$

We will actually perform the integral over \\(\D\psi_>\\) and \\(\D\bar{\psi}_>\\) and interpret result as a renormalized \\(S_\text{eff}(\bar{\psi}_<,\psi_<)\\). Let's see how to rewrite the partition function

$$\begin{align}
Z = \int e^{-S} \D \bar{\psi} \D \psi
\end{align}$$

$$$$\begin{align}
S_0 = \int_0^\beta \sum_{\k,\sigma}\bar{\psi}_{\k,\sigma}(\tau) \left(\frac{d}{d\tau}+\epsilon(\k)\right)\psi_{\k,\sigma}(\tau) d\tau  = S_{0>} + S_{0<}.
\end{align}$$$$

and the sums over \\(\k\\) in \\(S_{0>}\\) and \\(S_{0<}\\) are over the ranges of \\(\k\\) specified above. The interaction term is given by 

$$$$\begin{align}
S_\text{int} = \frac{J}{N}\int_0^\beta  \sum_{\k,\k',\alpha,\beta}\bar{\psi}_{\k\alpha}(\tau) \boldsymbol{\sigma}_{\alpha\beta}\psi_{\k,\beta}(\tau) \cdot\textbf{S}(\tau) d\tau 
\end{align}$$$$

also has cross-terms. The partition function becomes 

$$\begin{align}
Z =& \int e^{-S_0 - S_\text{int}} \D \bar{\psi} \D \psi \\
=& \int e^{S_{0>} - S_{0<} - S_\text{int}} \D \bar{\psi}_> \D\psi_> \D \bar{\psi}_< \D \psi_< \\
=& \int e^{-S_{0<}} \left(\int e^{-S_{0>}} e^{-S_\text{int}} \D\bar{\psi}_> \D \psi_>\right) \D\bar{\psi}_< \D\psi_< \\
=& Z_{0>} \int e^{-S_{0<}} \left(\frac{1}{Z_{0>}}\int e^{-S_{0>}} e^{-S_\text{int}} \D\bar{\psi}_> \D \psi_>\right) \D\bar{\psi}_< \D\psi_< \\
=& Z_{0>} \int e^{-S_{0<}} \left< e^{-S_\text{int}} \right>_{0>} \D\bar{\psi}_< \D\psi_< \\
=& Z_{0>} \int \exp\left(-S_{0<} + \sum_{n=1}^\infty \frac{(-1)^n}{n!} \left<S^n_\text{int}\right>_{0>,c} \right) \D\bar{\psi}_< \D\psi_< \label{eq:slow_partition_function}
\end{align}$$

where we define 

$$\left<A\right>_{0>} = \frac{1}{Z_{0>}} \int e^{S_{0>}} A \D \bar{\psi}_> \D \psi_>$$

and \\(Z_{0>}\\) is just the partition function with the fast fields. The equation \eqref{eq:slow_partition_function} is of the form of a typical partition function, so we therefore define an effective action

$$$$\begin{align} \label{eq:slow_effective_action}
S_\text{eff} = S_{0<} + \sum_{n=1}^\infty \frac{(-1)^{n-1}}{n!} \left<S^n_\text{int}\right>_{0>,c}
\end{align}$$$$ 

\subsubsection{Renormalization at Zeroth Order}
We will analyze the effective action Eq. \eqref{eq:slow_effective_action}. The first term is simply \\(S_{0<}\\). 




It can be seen that expanding to 1st order in \\(S_\text{int}\\) gives no renormalization of \\(S_\text{eff}\\), using \\(\tr\boldsymbol{\sigma} = 0\\).

We will work at \\(T = 0\\), \\(\beta\to\infty\\).

It is convenient to let \\(\tau\\) integral run from \\(-\beta/2\\) to \\(\beta/2\\), using periodicity, so it runs from \\(-\infty\\) to \\(\infty\\) at \\(\beta\to\infty\\). 

For the Kondo model, it is convenient to work in time-domain, not frequency.

Second order expansion of \\(e^{+S_\text{int}}\\) is

$$$$\begin{align}\frac{1}{2}\left(\frac{J}{V}\right)^2\int_{-\infty}^\infty d\tau_1 d\tau_2\sum_{\k_1,\k_1',\k_2,\k_2'}T[\bar{\psi}(\k_1,\tau_1)\frac{\boldsymbol{\sigma}}{2}\psi(\k_1',\tau_1)\cdot\textbf{S}(\tau_1)\bar{\psi}(\k_2,\tau_2)\frac{\boldsymbol{\sigma}}{2}\psi(\k_2',\tau_2)\cdot\textbf{S}(\tau_2)]\end{align}$$$$

If all 4 wave vectors are in \\(<\\) range, we don't need to both expanding.

If we leave all in \\(>\\) range, integral just gives a constant, independent of \\(\psi_<\\), \\(\bar{\psi}_<\\) - shifts ground state energy.

Interesting case has either \\(\k_1'\\),\\(\k_2\\), \\(\epsilon\\) \\(>\\) or \\(\k_1\\),\\(\k_2'\\), \\(\epsilon\\) \\(>\\) (only)

Then we do Grassmann integrals

$$$$\begin{align}\left<\psi_\beta(\k_1',\tau_1)\bar{\psi}_\gamma(\k_2,\tau_2)\right> \end{align}$$$$

or

$$$$\begin{align}\left<\bar{\psi}_\alpha(\k_1,\tau_1)\psi_\delta(\k_2',\tau_2)\right>\end{align}$$$$

These are simply Matsubara Green functions at \\(\beta\to\infty\\) which gives

$$$$\begin{align}\left<\psi(\k,\tau_1)\bar{\psi}(\k,\tau_2)\right> = (\theta(\tau_1-\tau_2)\left<\chat_{\k} \chat^\dagger_{\k}\right> - \theta(\tau_2 - \tau_1)\left<\chat_{\k}^\dagger \chat_{\k}\right>)e^{(\tau_2 - \tau_1)\epsilon_{\k}} = (\theta(\tau_1 - \tau_2)\theta(+\epsilon_{\k}) - \theta(\tau_2 - \tau_1)\theta(-\epsilon_{\k}))e^{(\tau_2 - \tau_1)\epsilon_{\k}}\end{align}$$$$

Note: exponent is always less than 0, so we can replace by \\(e^{-|\tau_2 - \tau_1||\epsilon_{\k}|}\\).

The term with \\(\k_1\\), \\(\k_2\\),\\(\epsilon\\) \\(>\\) gives

$$$$\begin{align}\frac{1}{2}\left(\frac{J}{V}\right)^2\sum_{\k_1,\k'_2,\epsilon <,a,b}\int d\tau_1 d\tau_2 \bar{\psi}(\k_1,\tau_1)\frac{\sigma^a}{2}\frac{\sigma^b}{2}\psi(\k_2',\tau_2)T[S^a(\tau_1)S^b(\tau_2)][\theta(\tau_1-\tau_2)\theta(\epsilon_{\k}) - \theta(\tau_2 - \tau_1)\theta(-\epsilon_{\k})]\exp((\tau_2 - \tau_1)\epsilon_{\k})\end{align}$$$$

Here, we used the fact that 

$$$$\begin{align}\left<\psi_\beta(\k_1,\tau_1)\bar{\psi}_\gamma(\k_2,\tau_2)\right> \propto\delta_{\beta\gamma}\end{align}$$$$

so that

$$$$\begin{align}\sum \bar{\psi}_\alpha \sigma^a_{\alpha\beta}\delta_{\beta\gamma}\sigma^b_{\gamma\delta}\psi_\delta = \bar{\psi}\sigma^a\sigma^b\psi\end{align}$$$$

Now consider second term with \\(\k_1\\),\\(\k_2'\\) \\(\epsilon\\) \\(>\\)

We can anticommute remaining

$$$$\begin{align}\psi(\k_1',\tau_1)\bar{\psi}(\k_2,\tau_2)\end{align}$$$$

into order \\(\bar{\psi}\psi\\) at cost of a minus sign.

If we relabel integration and summation variables, \\(\tau_1\leftrightarrow \tau_2\\) and \\(\k_2\leftrightarrow \k_1\\), \\(\k_2'\leftrightarrow \k_1'\\), \\(a\leftrightarrow b\\), we get an identical expression except the order of \\(S^a(\tau_1)\\) and \\(S^b(\tau_2)\\) switches.

i.e.

$$$$\begin{align}\sum\int\bar{\psi}(\tau_2)\sigma^b\sigma^a\psi(\tau_1) T S^a(\tau_1)S^b(\tau_2)\to \sum\int \bar{\psi}(\tau_1)\sigma^a\sigma^b\psi(\tau_2)T S^b(\tau_2) S^a(\tau_1)\end{align}$$$$

Now, adding the two terms together gives a factor of 

$$$$\begin{align}T[S^a(\tau_1),S^b(\tau_2)] = \sgn(\tau_1 - \tau_2)i\epsilon^{abc}S^c\end{align}$$$$

Note: Only nonzero because \\(S^a\\) and \\(S^b\\) don't commute. We can now simplify trace over spin indices on fermions using

$$$$\begin{align}\sum_{a,b}\epsilon^{abc}\sigma^a \sigma^b = 2i\sigma^c\end{align}$$$$

Second order term becomes

$$$$\begin{align}-\left(\frac{J}{V}\right)^2\int_{-\infty}^\infty d\tau_1 d\tau_2 \sum_{\k\k'\epsilon<}\bar{\psi}(\k,\tau_1)\frac{\boldsymbol{\sigma}}{2}\psi(\k,\tau_2)\cdot\textbf{S}\end{align}$$$$

$$$$\begin{align}\frac{1}{2}\sum_{\k_2\epsilon >}(\theta(\tau_1 - \tau_2)\theta(\epsilon_{\k_2})-\theta(\tau_2-\tau_1)\theta(-\epsilon_{\k_2}))e^{(\tau_2 - \tau_1)\epsilon_{\k_2}}\sgn(\tau_1-\tau_2)\end{align}$$$$

Minus sign from \\(i^2\\).

This looks like a \\(O(J^2)\\) correction to \\(J\\). However, it is a retarded interaction involving \\(\bar{\psi}(\tau_1)\\), \\(\psi(\tau_2)\\) at different times

$$$$\begin{align}\int \bar{\psi}(\tau_1)\psi(\tau_2)\delta(\tau_1-\tau_2) d\tau_1 d\tau_2 \end{align}$$$$

We will Taylor expand

$$$$\begin{align}\psi(\tau_2) = \psi(\tau_1) + (\tau_2 - \tau_1)\frac{d\psi}{d\tau} + \cdots \end{align}$$$$

and integrate over \\(\tau_2\\) term by term. 

In this way, we generate a series of terms in \\(S_\text{eff}\\) which are instantaneous but involve time derivatives of \\(\psi\\). Keep only non-derivative term for now. Other ones, as we will see, correspond to irrelevant operators. Let \\(\tau_2 - \tau_1 = \tau\\). Then, the second term becomes

$$$$\begin{align}-\left(\frac{J}{V}\right)^2\int d\tau \sum_{\k,\k',\epsilon,<}\bar{\psi}(\k,\tau)\frac{\boldsymbol{\sigma}}{2}\psi(\k',\tau)\cdot\textbf{S}\frac{1}{2}\int d\tau'\sum_{\k_2\epsilon>}(\theta(-\tau')\theta(\epsilon_{\k_2})-\theta(+\tau')\theta(-\epsilon_{\k_2}))\sgn(-\tau')\exp(\tau'\epsilon_{\k_2})\end{align}$$$$

Integral over \\(d\tau'\\) gives

$$$$\begin{align}\theta(\epsilon)\int_{-\infty}^0 e^{\tau\epsilon}d\tau' + \theta(-\epsilon)\int_0^\infty d\tau' e^{\tau'\epsilon} = \frac{\theta(\epsilon)}{\epsilon} + \frac{\theta(-\epsilon)}{-\epsilon} = \frac{1}{|\epsilon|}\end{align}$$$$

Leaving

$$$$\begin{align}\frac{-J^2}{V}\sum_{\k,\k',\epsilon<}\int d\tau \bar{\psi}(\k,\tau)\frac{\boldsymbol{\sigma}}{2}\psi(\k',\tau)\cdot\textbf{S}\frac{1}{2}\frac{1}{V}\sum_{\k_2\epsilon>}\frac{1}{|\epsilon_{\k_2}|}\end{align}$$$$

We reexponentiate

$$$$\begin{align}
e^{\delta S_\text{int}} = 1+\delta S_\text{int}
\end{align}$$$$

where

$$$$\begin{align}
\delta S_\text{int} = -\int \delta H_\text{int}d\tau 
\end{align}$$$$

correction to \\(S_\text{int}\\) has form of a correction to Kondo coupling.

$$$$\begin{align}\delta J = J^2 \frac{1}{V}\frac{1}{2}\sum_{\k_2\epsilon>}\frac{1}{|\epsilon_{\k_2}|}\end{align}$$$$


Take \\(V\to\infty\\). 

$$$$\begin{align}\delta J = \frac{J^2}{2}\int \frac{1}{|\epsilon_{\k}|}\frac{d^3\k}{(2\pi)^3} = \frac{J^2}{2}\int \frac{\nu(\epsilon)}{|\epsilon|}d\epsilon\end{align}$$$$

where \\(\nu(\epsilon)\\) is the density of states. The integral is over \\(\D' < \epsilon < \D\\) and \\(-\D < \epsilon < -\D'\\) corresponding to region of \\(>\\) modes as \\(\D'\\) is reduced towards 0 (\\(\ll \epsilon_F\\))

\\(\delta J\\) diverges since \\(\nu(\epsilon)\\) can be approximate by \\(\nu(\epsilon_F) = \nu\\).

\\(\delta J \sim J^2 \nu\log \D/\D'\\)

and diverges as \\(\D'\to 0\\). 

Note that \\(\log \D\\) term is just an estimate. it becomes correct if \\(\D'\\) is also much smaller than \\(E_F\\) - otherwise there is a finite correction term.

The RG is usually performed in infinitesimal steps (more powerful that way)

We consider an infinitesimal reduction \\(\D' = \D - \delta \D\\), \\(\delta \D \ll \D\\) and we consider infinitesimal change in \\(S_\text{Eff}\\)

When the running cut off is near \\(\D\\), the change in coupling constants depends on their values at \\(\D\\)

In previous calculation, we interpret \\(J\\) as \\(J(\D)\\) - running coupling constant when cut-off is \\(\D\\).

$$$$\begin{align}\log \frac{\D}{\D'} = \log\frac{\D}{\D-\delta \D} \sim \frac{\delta \D}{\D}\end{align}$$$$

$$$$\begin{align}\delta J = J^2(\D) \nu \frac{\delta \D}{\D}\end{align}$$$$

$$$$\begin{align}\D\frac{dJ}{d\D} = 0\nu J^2(\D)\end{align}$$$$ 

because the change in \\(\D\\) is \\(-\delta \D\\), or

$$$$\begin{align}\frac{dJ}{d\log \D} = -\nu J^2\end{align}$$$$

If we define dimensionless Kondo coupling \\(\lambda = J\nu\\), so that

$$$$\begin{align}\frac{d\lambda}{d\log \D} = -\lambda^2\end{align}$$$$

This verifies that, as expected, \\(J\nu\\) is appropriate definition of dimensionless coupling constant. 

More generally, if 

$$$$\begin{align}\frac{d\lambda}{d\log \D} = \beta(\lambda)\end{align}$$$$

then \\(\beta(\lambda)\\) is called the \\(\beta\\) function. \\(\beta = -\lambda^2\\) is the lowest order perturbative calculation.

We will refer to \\(d\lambda/d\log \D = \beta(\lambda)\\) as the RG equation. A fundamental part of the RG equation is easily solved.

Let \\(\lambda_0\\) be \\(\lambda(\D_0)\\) for some relatively high energy cutoff \\(\D_0\\) and express \\(\lambda(\D)\\) at lower cutoff \\(\D\\) in terms of \\(\lambda_0\\) and \\(\D_0\\). 

$$$$\begin{align}\int_{\lambda_0}^\lambda \frac{d\lambda}{\lambda^2} = \int_\D^{\D_0} d(\log \D)\end{align}$$$$

Thus, integrating this, 

$$$$\begin{align}\frac{1}{\lambda_0} - \frac{1}{\lambda} = \log\frac{\D_0}{\D}\end{align}$$$$

Thus, 

$$$$\begin{align}\lambda(\D) = \frac{\lambda_0}{1-\lambda_0\log \D_0/\D} = \lambda_0 + \lambda_0^2\log \D_0/\D + \lambda_0^3 \log^2 \D_0/\D+\cdots\end{align}$$$$

Note that our strictly perturbative calculation gave only first two terms, by writing the RG equation we get complete series. This corresponds to summing a series of diagrams 

(Feynman diagrams here)

There are other diagrams residue. These ones which give higher order terms in \\(\beta\\) function. 

$$$$\begin{align}\lambda = \lambda_0 + \lambda_0^2 \log\frac{\D}{\D'} + \lambda^3\log^2\frac{\D}{\D'} - \frac{1}{2}\lambda_0^3\log\frac{\D}{\D'}\end{align}$$$$

Lowest order \\(\beta\\) function corresponds to ``leading log" approximation

$$$$\begin{align}\lambda_0^n\log^{n-1}\frac{\D}{\D'}\end{align}$$$$

$$$$\begin{align}\lambda_0^3\log\frac{\D}{\D'}\end{align}$$$$

gives \\(O(\lambda^3)\\) term in \\(\beta\\) function. 

$$$$\begin{align}\frac{d\lambda}{d\log \D} = -\lambda_0^2 - 2\lambda_0^3 \log\frac{\D}{\D'} + \frac{1}{2}\lambda_0^3 = -(\lambda_0 + \lambda_0^2\log\frac{\D}{\D'})^2 + \frac{1}{2}\lambda_0^3 = -\lambda^2 + \frac{1}{2}\lambda^3\end{align}$$$$

\\(\beta(\lambda) = -\lambda^2 + \frac{1}{2}\lambda^3 + O(\lambda^4)\\)

If we knew \\(\beta(\lambda)\\) exactly, we could determine \\(\lambda(\D)\\) at any scale \\(\D\\) (ignoring irrelevant operators), but we don't. 

Our lowest order result is only valid over range of \\(\D\\) where \\(\lambda(\D)\ll 1\\), we can ignore higher order corrections in \\(\beta\\) function.

\\(\lambda > 0\\) (AF), \\(\lambda < 0\\) (F) are very different.

If \\(\lambda_0 < 0\\), 

$$$$\begin{align}\lambda(\D) = \frac{\lambda_0}{1-\lambda_0\log \frac{\D_0}{\D}} = \frac{\lambda_0}{1 + |\lambda_0|\log\frac{\D_0}{\D}}\end{align}$$$$

Keeps getting smaller as \\(\D\\) is reduced. So if base coupling \\(\lambda_0\\) is small and negative, higher order terms in \\(\beta\\) function never become important, and we see that \\(\lambda(\D)\to 0\\) as \\(\D\to 0\\), \\(\lambda(\D)\sim -\frac{1}{\log \D_0/\D}\\)

On the other hand, if \\(\lambda_0 > 0\\), as appears to be the case experimentally for must types of impurities and metals, then \\(\lambda(\D)\\) grows as \\(\D\\) is reduced, and we always eventually leat to a cutoff scale \\(\D\\) where higher order terms become important. 

Note: Knowing the cubic term doesn't help very much usually, because at low enough \\(\D\\) that it is important, \\(\lambda(\D) \sim 1\\), quartic and higher terms are also important. 

Basic idea of RG improved perturbation theory is to calculate some physical quantity, e.g. resistivity, to lowest order in \\(\lambda\\), then replace \\(\lambda\\) by its renormalized value at the energy scale \\(E\\) that characterizes the quantity we are trying to calculate.

This corresponds to summing up an infinite series of corrections to lowest order calculation in leading order log approximation.

We will return to some fine points about this later.

For F case, this is a very powerful technique, even though perturbation theory is apparently breaking down:

$$$$\begin{align}\lambda_0 + \lambda_0^2 \log\frac{\D_0}{\D} + \lambda_0^3\log^2\frac{\D_0}{\D} + \cdots\end{align}$$$$

we sum series to get a small quantity

$$$$\begin{align}\frac{\lambda_0}{1+|\lambda_0|\log\frac{\D_0}{\D}}\to 0\end{align}$$$$

also useful for \\(\lambda > 0\\) but less so.

Now we can only use RG improved perturbation theory above energy scale where \\(\lambda(\epsilon) \sim 1\\). 

This energy scale is called the Kondo temperature, \\(T_K\\) (setting \\(k_B = 1\\)).

Using 

$$$$\begin{align}\lambda(E) = \frac{\lambda_0}{1-\lambda_0\log\frac{\D_0}{\D}}\end{align}$$$$

we can estimate \\(T_K\\), using \\(\lambda(T_K)\sim 1\\). 

$$$$\begin{align}1\sim \frac{\lambda_0}{1-\lambda_0\log\frac{\D_0}{T_K}}= \frac{1}{\frac{1}{\lambda_0} - \log\frac{\D_0}{T_K}}\end{align}$$$$

Thus, 

$$$$\begin{align}\frac{1}{\lambda_0}\sim\log\frac{D_0}{T_K}\end{align}$$$$

so that

$$$$\begin{align}T_K\sim D_0 e^{-1/\lambda_0}\end{align}$$$$

up to a factor of \\(O(1)\\). 

In this rough estimate, we could take \\(D_0\\) to be the original band width of \\(E_F\\) and \\(\lambda_0\\) to be the original ``bare" Kondo coupling, proportional to \\(E_F\\), 

$$$$\begin{align}T_K\sim E_F\exp(-\frac{1}{J\nu})\end{align}$$$$

exponentially small compared to \\(E_F\\). Like \\(\Lambda\\)-QCD - strong interaction coupling constant also grows with lowering \\(E\\). 

RG improved perturbation theory is valid for \\(E\gg T_K\\), but at \\(E\sim T_K\\) we enter strong coupling regime where perturbation theory completely fails, even when improved by RG. 

It is convenient to write

$$$$\begin{align}\lambda(E) \approx \frac{1}{\log E/T_K}\end{align}$$$$

for \\(E\gg T_K\\)

elementates bare coupling and replaces it by \\(T_K\\).

RG improved perturbation theory cna be applied y resistivity as we will now show.

Lowest order \\(R(T)\propto n_\text{imp}\lambda_0^2\\) where \\(n_\text{int}\\) is the impurity concentration. Note: this is just contribution to \\(R(T)\\) from scattering off of magnetic impurities - must be added to other contributions.

Now, if we RG-improve calculation, we get

$$$$\begin{align}R(T)\propto n_\text{imp}/\log^2(T/T_K)\end{align}$$$$ for $T\gg T_K$

This fits experimental data (and numerical calculations of Kondo model) well at \\(T\gg T_K\\)

Note: we cannot use this result as \\(T\to T_K\\) where it predicts \\(R\to\infty\\). We will return to question of what happens at lower \\(T\\), but first \\(g_1\\) through calculation of \\(R(T)\\) to second order in \\(J\\) in some detail - opportunity to learn some other techniques of CMP. See Henson chapter 2, Marder 11.1, A\& M chap 13. 

The plan is to calculate correction to electron Green function

$$$$\begin{align}G_\text{ret}(\k,\omega) = \frac{1}{\omega -\epsilon_{\k} + \frac{i}{2\tau}}\end{align}$$$$

this proadents single-electron pole 

(insert graph of retarded green function here)

Width = \\(1/\tau\\), \\(\tau\\) is time electron spends in a state of momentum \\(\k\\) before scattering (off an impurity)

We can insert this result in Boltzmann equation result for resistivity

$$$$\begin{align}\sigma = \frac{1}{R} = \frac{2e^2}{3}v_J^2 \nu \tau\end{align}$$$$

where \\(\nu\\) is the density of states at the Fermi surface. 

Boltzmann equation approach makes it clear that scattering rate at energies \\(|G_{\k}|\lesssim T\\) contribute to resistivity at temperatures \\(T\\). 

Using free electron dispersion relation, this reduces to 

\\(\frac{1}{R} = ne^2 T/m\\), which is the classical Drude formula.

Most rigorous derivation of the formula is from Kubo formula - can express retarded Green function for current operator in terms of green function for electron operator in this case

$$$$\begin{align}\sigma^{ab} = e^2\int \tau(\epsilon_{\k})v_{\k}^a v_{\k}^b(-\frac{\partial f}{\partial\epsilon})_{\epsilon_{\k}}\frac{d^3\k}{4\pi^3}\end{align}$$$$

for isotropic dispersion relation, we can replace \\(v^a_{\k} v^b_{\k} = \frac{1}{3}\delta^{ab}v^2_{\k}\\) inside integral 


