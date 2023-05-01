---
layout: lesson
title: Relation Between Path Integral and Canonical Quantization
dept: physics
course: many-body-II
unit: unit3
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 3
---
Here, we will compare the canonical quantization and path integral formulations of many-body physics. 

\begin{table}[ht]
\centering
\begin{tabular}{ccc}
Object & Canonical Quantization & Path Integral \\
Matsubara function \\(\mathcal{G}(\nu',\tau'; \nu,\tau)\\) & \\(-\left<T_\tau[\chat_{\nu'}(\tau')\chat^\dagger_\nu(\tau)]\right>\\) & \\(\left<c_{\nu'}(\tau')\bar{c}_\nu(\tau)\right>\\) \\
Free Hamiltonian & \\(\Hhat_0 = \sum_\nu (\epsilon_\nu-\mu) \chat^\dagger_\nu \chat_\nu\\) & \\(H_0 = \sum_\nu (\epsilon_\nu-\mu) \bar{c}_\nu c_\nu\\) \\
Free Green Function (freq) & \\(\frac{1}{i\omega - \xi_\nu}\\) &
\end{tabular}
\end{table}

In this section, we will explicitly show how the calculation of correlation functions in canonical quantization can be written in terms of a path integral calculation. The previous parts of this chapter have shown how the partition function is rewritten in terms of a path integral, but correlation functions are also very important. We start with a bosonic two-point correlation function. 

$$$$\begin{align}
\mathcal{G}(\nu',\tau';\nu.\tau) = -\left<T_\tau\left[\bhat_\nu(\tau')\bhat^\dagger_{\nu}(\tau)\right]\right>
\end{align}$$$$

For the case \\(\tau' > \tau\\), we get 
$$\begin{align}
\mathcal{G}(\nu',\tau';\nu.\tau) =& -\left<\bhat_\nu(\tau')\bhat^\dagger_{\nu}(\tau)\right> \\
=& -\frac{1}{Z}\tr\left(e^{-\beta H}\bhat_\nu(\tau')\bhat^\dagger_{\nu}(\tau)\right) \\
=& -\frac{1}{Z}\tr\left(^{-\beta\Hhat} e^{\tau'\Hhat}\bhat_{\nu'}e^{-\tau'\Hhat}e^{\tau\Hhat}\bhat^\dagger_\nu e^{-\tau\Hhat}\right) \\
=& -\frac{1}{Z}\int\bra{z_0}e^{-\beta\Hhat} e^{\tau'\Hhat}\bhat_{\nu'}e^{-\tau'\Hhat}e^{\tau\Hhat}\bhat^\dagger_\nu e^{-\tau\Hhat}\ket{z_0} \d z_0^{*}\d z_0 \\
=& -\frac{1}{Z}\int\bra{z_0}e^{-(\beta-\tau')\Hhat}\bhat_{\nu'} \ket{z_{\tau'}}\bra{z_{\tau'}} e^{-(\tau'-\tau)\Hhat}\ket{z_\tau}\bra{z_\tau} \bhat^\dagger_\nu e^{-\tau\Hhat}\ket{z_0} \d z_0^{*}\d z_0 \\
=& -\frac{1}{Z}\int\bra{z_0}e^{-\epsilon\Hhat}\ket{z_{N-1}}\bra{z_{N-1}}e^{-\epsilon\Hhat}\cdots e^{-\epsilon\Hhat} \ket{z_{\tau'+\epsilon}}\bra{z_{\tau'+\epsilon}}\bhat_{\nu'} \ket{z_{\tau'}} \\
&\times \bra{z_{\tau'}} e^{-\epsilon\Hhat}\ket{z_{\tau'-\epsilon}}\bra{z_{\tau'-\epsilon}}e^{-\epsilon\Hhat} \cdots e^{-\epsilon\Hhat}\ket{z_\tau}\bra{z_\tau} \bhat^\dagger_\nu e^{-\epsilon\Hhat}\ket{z_{\tau-\epsilon}}\bra{z_{\epsilon}}e^{-\epsilon\Hhat}\cdots e^{-\epsilon\Hhat} \ket{z_0} \\
& \times \d z_0^{*}\d z_0 \d z_\epsilon^{*} \d z_\epsilon \cdots \d z_{N-1}^{*} \d z_{N-1} \\
=& -\frac{1}{Z}\int\bra{z_0}e^{-\epsilon H[z_0^{*}.z_{N-1}]}\ket{z_{N-1}}\bra{z_{N-1}}e^{-\epsilon H[z^{*}_{N-1},z_{N-2}]}\cdots e^{-\epsilon\Hhat} \ket{z_{\tau'+\epsilon}}\bra{z_{\tau'+\epsilon}}b_{\nu'} \ket{z_{\tau'}} \\
&\times \bra{z_{\tau'}} e^{-\epsilon H[z_0,z_{N-1}]}\ket{z_{\tau'-\epsilon}}\bra{z_{\tau'-\epsilon}}e^{-\epsilon H[z_{\tau'+\epsilon},z_\tau']} \cdots \bra{z_\tau} b^{*}_\nu e^{-\epsilon\Hhat}\ket{z_{\tau-\epsilon}}\bra{z_{\epsilon}}e^{-\epsilon\Hhat}\cdots e^{-\epsilon\Hhat} \ket{z_0} \\
& \times \d z_0^{*}\d z_0 \d z_\epsilon^{*} \d z_\epsilon \cdots \d z_{N-1}^{*} \d z_{N-1}
\end{align}$$

This can be done generally for any correlators, and the final result of this section is that 

<div class="result">
<b>Result:</b>
The relationship between correlation functions in the operator language and path integral language is the following. For bosonic fields, we have

$$\left<T_\tau\left[\bhat_{\nu_1'}(\tau_1')\cdots \bhat_{\nu_n'}(\tau_n') \bhat^\dagger_{\nu_1}(\tau_1)\cdots\bhat^\dagger_{\nu_n}(\tau_n)\right]\right> = \left< b_{\nu_1'}(\tau_1')\cdots b_{\nu_N'}(\tau_N') b^{*}_{\nu_1}(\tau_1)\cdots b^{*}_{\nu_N}(\tau_N)\right>$$

and a similar result holds for fermionic fields:

$$\left<T_\tau\left[\chat_{\nu_1'}(\tau_1')\cdots \chat_{\nu_n'}(\tau_n') \chat^\dagger_{\nu_1}(\tau_1)\cdots\chat^\dagger_{\nu_n}(\tau_n)\right]\right> = \left< c_{\nu_1'}(\tau_1')\cdots c_{\nu_n'}(\tau_n') \bar{c}_{\nu_1}(\tau_1)\cdots \bar{c}_{\nu_n}(\tau_n)\right>$$

We emphasize that the operators are given in the Heisenberg picture, not the interaction picture. Of course for the complex or Grassmann fields in the bosonic and fermionic cases respectively, there is no notion of interaction or Heisenberg picture; they are simply the fields at a particular time.

</div>


