---
layout: lesson
title: Fermionic Coherent States
dept: physics
course: many-body-II
unit: unit3
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 3
---
Using these rules, it is possible to define a fermionic coherent state. We index the fermionic coherent states not by complex numbers but by Grassmann numbers. The following state is an eigenstate of the annihilation operator, with (Grassmann number) eigenvalue \\(\psi\\).

$$$$\begin{align}
\ket{\psi} = \ket{0} - \psi\ket{1} = \ket{0} - \psi\hat{\psi}^\dagger\ket{0} = (1+\hat{\psi}^\dagger\psi)\ket{0}
\end{align}$$$$

Let us show that our state \\(\ket{\psi}\\) is indeed an eigenstate of the fermionic annihilation operator \\(\hat{\psi}\\).

<div class="proof">
<b>Proof:</b>
To show that the state \\(\ket{\psi}\\) is an eigenstate of \\(\hat{\psi}\\), let's just operate on \\(\ket{\psi}\\). I will show this in excruciating detail because Grassmann numbers are still a new concept for us.

$$\begin{align}
\hat{\psi}\ket{\psi} =& \hat{\psi}(\ket{0} - \psi\ket{1})\\
=& 0-\hat{\psi}\psi(\hat{\psi}^\dagger\ket{0})\\
=& \hat{\psi}\hat{\psi}^\dagger \psi\ket{0} \\
=& \psi \hat{\psi}\hat{\psi}^\dagger\ket{0}\\
=& \psi\ket{0} \\
=& \psi\ket{0} - \psi^2\ket{1}\\
=& \psi(\ket{0} - \psi\ket{1}) \\
=& \psi\ket{\psi}
\end{align}$$

</div>

The dual of this equation is the following:
$$$$\begin{align}
\bra{\bar{\psi}} = \bra{0} - \bra{1}\bar{\psi}.
\end{align}$$$$ 

It is a bra type coherent state. 

\begin{remark_wrapper}
\begin{remark}
\\(\bar{\psi}\\) is not the Hermitian conjugate of \\(\psi\\). There is no such thing as the Hermitian conjugate of a Grassmann number.
\end{remark}
\end{remark_wrapper}

\\(\bra{\bar{\psi}}\\) is an eigenstate of \\(\hat{\psi}^\dagger\\) with eigenvalue \\(\bar{\psi}\\), so that 

$$$$\begin{align}
\bra{\bar{\psi}}\hat{\psi}^\dagger = \bra{\bar{\psi}} \bar{\psi}.
\end{align}$$$$

check this as an exercise. Also check normalization of Fermionic coherent states, 

$$$$\begin{align}
\bra{\bar{\psi}}\ket{\psi} = (\bra{0} - \bra{1}\bar{\psi})(\ket{0} -\psi{\ket{1}) = 1 + \bar{\psi}\psi} = e^{\bar{\psi}\psi}.
\end{align}$$$$

check the sign!

We can write it in the exponential for convenience since the power series terminates. Thus \\(\ket{\psi}\\) is not unit normalized. In fact, its norm is not even a \\(c\\)-number. Note that

$$$$\begin{align}
\int \bar{\psi}\psi \d\psi \d\bar{\psi} = 1
\end{align}$$$$

$$$$\begin{align}
\int e^{-a\bar{\psi}\psi}\d\bar{\psi} \d\psi = -a\int \bar{\psi}\psi \d\bar{\psi} \d\psi = a
\end{align}$$$$

This is the opposite of a \\(c\\) number since (for positive \\(a\\)) (check this...i don't think the normalization is correct)

$$$$\begin{align}
\int e^{-a z^{*}z}dz^{*} dz = \frac{1}{a}
\end{align}$$$$


