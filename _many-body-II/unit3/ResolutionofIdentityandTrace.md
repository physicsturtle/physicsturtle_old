---
layout: lesson
title: Resolution of Identity and Trace
dept: physics
course: many-body-II
unit: unit3
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 3
---
Without reference to Grassmann numbers or even operators, we can write the identity operator for a system which has two possible states: empty and occupied. The identity then is written as 

$$$$\begin{align}
\1 = \ket{0}\bra{0} + \ket{1}\bra{1}. 
\end{align}$$$$

Our goal is to write this resolution of identity in terms of an analogous expression to REFERENCE EQN HERE the bosonic case. This will be useful for formulating the path integral later. 

<div class="result">
<b>Result:</b>
The resolution of identity for a Hilbert space consisting of a single state, either occupied or unoccupied, is

$$$$\begin{align}
\1 = \int \ket{\psi}\bra{\bar{\psi}}e^{-\bar{\psi}\psi}\d\bar{\psi}\d\psi.
\end{align}$$$$

</div>

<div class="proof">
<b>Proof:</b>
To prove this, we simply evaluate the exponential. We simply Taylor expand, and then write the coherent states as the expansion in terms of \\(\ket{0}\\) and \\(\ket{1}\\).
 
$$\begin{align}
\int \ket{\psi}\bra{\bar{\psi}}e^{-\bar{\psi}\psi}\d\bar{\psi}\d\psi =& \int(\ket{0} - \psi\ket{1})(\bra{0} - \bra{1}\bar{\psi})(1-\bar{\psi}\psi)\d\bar{\psi}\d\psi \\
=& -\ket{0}\bra{0}\int \bar{\psi}\psi \d\bar{\psi} \d\psi + \ket{1}\bra{1}\int \psi\bar{\psi} \d\bar{\psi} \d\psi \\
=& \ket{0}\bra{0} + \ket{1}\bra{1} \\
=& \1
\end{align}$$
as desired.

</div>

So formal integrals over Grassmann numbers make a perfectly valid resolution of the identity operator. 

\begin{remark_wrapper}
\begin{remark}
You may be confused why our Hilbert space is only two dimensional, consisting of an empty and a singly occupied state. At first, this seems reasonable, as these are the only two possible occupation numbers! However, I recall that when I first learned this, I had trouble recognizing how this is related to something like a fermion in an infinite square well; there are infinitely many states in the infinite square well! To formulate the infinite square well in terms of what we've done here, we would take each of the wave functions

$$$$\begin{align}
\psi_n(x) = \sqrt{\frac{2}{L}}\sin\left(\frac{n\pi x}{L}\right),
\end{align}$$$$

and say that it could hold a fermion or not hold a fermion. Since each occupiable state could either contain a fermion or not, and we have infinitely many occupiable states, this becomes a problem of undetermined many particles. If we truly wanted to understand the ....Since, in the infinite square well problem, we say that we only have one particle, we would .....

\end{remark}
\end{remark_wrapper}

The other useful identity in the bosonic case was expressing the trace as an integral. We can do the same in the fermionic case here via the following result. 

<div class="result">
<b>Result:</b>

$$$$\begin{align}
\tr\Omega = \int\bra{-\bar{\psi}}\Omega\ket{\psi}e^{-\bar{\psi}\psi}\d\bar{\psi}\d\psi
\end{align}$$$$

Note the minus sign. 

</div>


<div class="proof">
<b>Proof:</b>
We prove this by 
$$\begin{align}
\int\bra{-\bar{\psi}}\Omega\ket{\psi}e^{-\bar{\psi}\psi}d\bar{\psi}d\psi =& \int(\bra{0}+\bra{1}\bar{\psi})\Omega(\ket{0}-\psi\ket{1})e^{-\bar{\psi}\psi}d\bar{\psi}d\psi\\
=& \bra{0}\Omega\ket{0}\int e^{-\bar{\psi}\psi}d\bar{\psi}d\psi - \bra{1}\Omega\ket{1}\int\bar{\psi}\psi e^{-\bar{\psi}\psi}d\bar{\psi}d\psi\\
=& \bra{0}\Omega\ket{0}\int-\bar{\psi}\psi d\bar{\psi}d\psi - \bra{1}\Omega\ket{1}\int \bar{\psi}\psi d\bar{\psi}d\psi\\
=& \bra{0}\Omega\ket{0} + \bra{1}\Omega\ket{1}\\
=& \tr\Omega
\end{align}$$

</div>

