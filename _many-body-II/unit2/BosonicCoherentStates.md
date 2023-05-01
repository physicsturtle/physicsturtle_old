---
layout: lesson
title: Bosonic Coherent States
dept: physics
course: many-body-II
unit: unit2
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 2
---
We define the bosonic coherent state the same way as for the ordinary quantum harmonic oscillator. 

The overlap between two bosonic coherent states is given by 

$$\begin{align}
\bra{b}\ket{b'} =& e^{-|b|^2/2} e^{-|b'|^2/2} \sum_{m,n=0}^\infty \frac{b^{*m} b^{\prime n}}{\sqrt{m!n!}} \bra{m}\ket{n} \\
=& e^{-|b|^2/2} e^{-|b'|^2/2} \sum_{m,n=0}^\infty \frac{b^{*m} b^{\prime n}}{\sqrt{m!n!}} \delta_{mn} \\
=& e^{-|b|^2/2} e^{-|b'|^2/2} \sum_{n=0}^\infty \frac{b^{*n} b^{\prime n}}{n!} \\
=& e^{-|b|^2/2} e^{-|b'|^2/2} e^{b^{*}b'}
\end{align}$$

Now, for the many-body coherent state, it is defined by 

$$\ket{\{b\}} = \exp\left(-\frac{1}{2}\sum_i |b_i|^2\right) \exp\left(\sum_i b_i b_i^\dagger\right)\ket{0}$$

where \\(i\\) runs over lattice sites. This means that the overlap between the many-body coherent states is 

$$\bra{\{b\}}\ket{\{b'\}} = \exp\left(-\frac{1}{2}\sum_i(|b_i|^2 + |b_i'|^2)\right) \bra{0} \left(\prod_i e^{b_i^{*} \bhat_i} e^{b_i' \bhat_i^\dagger} \right)\ket{0}$$

The product of exponentials can be written as 

$$\begin{align}
e^{b_i^{*} \bhat_i} e^{b_i' \bhat_i^\dagger} =& e^{b_i^{*} \bhat_i} e^{b_i' \bhat_i^\dagger} e^{-b_i^{*} \bhat_i} e^{b_i^{*} \bhat_i} \\
=& \sum_{k=0}^\infty \frac{(b_i^{*})^k}{k!} \underbrace{[\bhat_i, [\bhat_i,\dots,[\bhat_i, e^{b_i' \bhat_i^\dagger}],\dots]]}_{k\text{-times}} e^{b_i^{*} \bhat_i}
\end{align}$$

We can evaluate the inner commutator 

$$\begin{align}
[\bhat_i, e^{b_i' \bhat_i^\dagger}] =& \sum_{\ell=0}^\infty \frac{1}{\ell!} [\bhat_i, (b_i')^\ell (\bhat_i^\dagger)^\ell] \\
=& \sum_{\ell=0}^\infty \frac{(b_i')^\ell}{\ell!} [\bhat_i, (\bhat_i^\dagger)^\ell]
\end{align}$$

Noting that if \\(\ell = 0\\), we get 0, and if \\(\ell = 1\\), we get 1, and if \\(\ell = 2\\), we get \\(2\bhat_i^\dagger[\bhat_i, \bhat_i^\dagger] = 2\bhat_i\\), if \\(\ell = 3\\), we get \\([\bhat_i, \bhat_i^\dagger \bhat_i^\dagger \bhat_i^\dagger] = [\bhat_i, \bhat_i^\dagger \bhat_i^\dagger] \bhat_i^\dagger + \bhat_i^\dagger \bhat_i^\dagger [\bhat_i, \bhat_i^\dagger] = 3\bhat_i^\dagger \bhat_i^\dagger\\). In general, \\([\bhat_i, (\bhat_i^\dagger)^\ell] = \ell (\bhat_i^\dagger)^{\ell-1}\\). Thus, we get 

$$\begin{align}
[\bhat_i, e^{b_i' \bhat_i^\dagger}] =& \sum_{\ell=0}^\infty \frac{(b_i')^\ell}{\ell!} \ell (\bhat_i^\dagger)^{\ell-1} \\
=& \sum_{\ell=0}^\infty \frac{(b_i')^\ell}{(\ell-1)!} (\bhat_i^\dagger)^{\ell-1} \\
=& \sum_{\ell=0}^\infty \frac{(b_i')^{\ell+1}}{\ell!} (\bhat_i^\dagger)^\ell \\
=& b_i' e^{b_i' \bhat_i^\dagger}
\end{align}$$

Now plugging this in, we find that 

$$\underbrace{[\bhat_i, [\bhat_i,\dots,[\bhat_i, e^{b_i' \bhat_i^\dagger}],\dots]]}_{k\text{-times}} = (b_i')^k e^{b_i' \bhat_i^\dagger}$$

Thus, 

$$\begin{align}
e^{b_i^{*} \bhat_i} e^{b_i' \bhat_i^\dagger} =& \sum_{k=0}^\infty \frac{(b_i^{*})^k}{k!} (b_i')^k e^{b_i' \bhat_i^\dagger} e^{b_i^{*} \bhat_i} \\
=& e^{b_i^{*} b_i'} e^{b_i' \bhat_i^\dagger} e^{b_i^{*} \bhat_i} 
\end{align}$$

Therefore, we get 

$$\bra{\{b\}}\ket{\{b'\}} = \exp\left(-\frac{1}{2}\sum_i(|b_i|^2 + |b_i'|^2)\right) \bra{0} \left(\prod_i e^{b_i^{*} b_i'} e^{b_i' \bhat_i^\dagger} e^{b_i^{*} \bhat_i}  \right)\ket{0}$$

Then, the expectation of this operator in the ground state simplifies very simply to 

$$\begin{align}
\bra{\{b\}}\ket{\{b'\}} =& \exp\left(-\frac{1}{2}\sum_i(|b_i|^2 + |b_i'|^2)\right) \left(\prod_i e^{b_i^{*} b_i'} \right) \\
=& \exp\left(-\frac{1}{2}\sum_i(|b_i|^2 + |b_i'|^2)+\sum_i b_i^{*} b_i' \right)
\end{align}$$


