---
layout: lesson
title: Klein Factors
dept: physics
course: many-body-II
unit: unit17
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 17
---
We have to finally define the Klein factors \\(\Fhat^\dagger_\alpha\\) and \\(\Fhat_\alpha\\). These are able to connect the various \\(\textbf{N}\\)-particle Hilbert spaces by raising or lowering the total number of fermions by one. It is not possible for any combination of bosonic operators to this, which is why they are necessary. An additional upside to defining these is that they ensure the different flavours of fermionic operators anticommute, even when expressed in terms of bosonic operators. The Klein factors are defined to have the property of commuting with the bosonic operators

$$[\varphihat_{q\alpha}, \Fhat^\dagger_{\alpha'}] = [\varphihat^\dagger_{q\alpha}, \Fhat^\dagger_{\alpha'}] = [\varphihat_{q\alpha},\Fhat_{\alpha'}] = [\varphihat^\dagger_{q\alpha}, \Fhat_{\alpha'}] = 0$$

At this stage, one aspect isn't totally clear. The basis states in the Fock space are labelled by the occupation of a particular flavour and also momentum. The Klein factor seems to indicate only a flavour that is created/annihilated. If we have a ground state \\(\ket{\textbf{N}}_0\\) with no particle-hole excitations, then there is a very sensical way in which the Klein factor should act. It should add an electron to the lowest empty \\(\alpha\\)-level of \\(\ket{\textbf{N}}_0\\). Similarly, for the annihilation Klein factor, it should remove the electron from the highest occupied level of \\(\ket{\textbf{N}}_0\\). That is, 

$$\begin{align}
\Fhat_\alpha^\dagger\ket{\textbf{N}}_0 =& \psihat^\dagger_{N_\alpha+1,\alpha} \ket{N_1,\dots,N_\alpha,\dots,N_M}_0 \\ 
=& \hat{T}_\alpha \ket{N_1,\dots,N_\alpha+1,\dots,N_M}_0 \\
\Fhat_\alpha \ket{\textbf{N}}_0 =& \psihat_{N_\alpha,\alpha} \ket{N_1,\dots,N_\alpha,\dots,N_M}_0 \\
=& \hat{T}_\alpha \ket{N_1,\dots,N_\alpha-1,\dots,N_M}_0
\end{align}$$

Here, \\(\hat{T}\\) is a phase factor which accounts for the fact that the creation/annihilation operator must pass through numerous other operators before it can join its friends of the same flavour. Thus

$$$$\begin{align}
\hat{T}_\alpha = (-1)^{\sum_{\bar{\alpha}=1}^{\alpha-1}\hat{N}_\alpha}
\end{align}$$$$

<div class="example">
<b>Example:</b>
SHOW HOW THE KLEIN FACTOR ACTS ON THE N PARTICLE GROUND STATE

</div>

We can now use this information to define how the Klein factor should act on a general state. Since a general state can be written as 

$$\ket{\textbf{N}} = f(\varphi^\dagger)\ket{\textbf{N}}_0$$

and we already established that the Klein factor should commute with the bosonic operator, then we can act on \\(\ket{\textbf{N}}\\) with a creation/annihilation Klein factor (let's pick the creation one; the annihilation computation is identical)

$$\begin{align}
\Fhat^\dagger_\alpha\ket{\textbf{N}} =& \Fhat_\alpha f(\varphihat^\dagger)\ket{\textbf{N}}_0 \\
=& f(\varphihat^\dagger) \Fhat_\alpha \ket{\textbf{N}}_0 \\
=& f(\varphihat^\dagger) \hat{T}_\alpha \ket{N_1,\dots,N_\alpha+1,\dots,N_M}_0 \\
\end{align}$$

The phase factor \\(\hat{T}_\alpha\\) is necessary because, 

Consider a state \\(\ket{\textbf{N}}\\), where \\(\textbf{N} = (N_1,\dots,N_\alpha,\dots, N_M)\\), where \\(M\\) is the total number of flavours. Recall that \\(N_\alpha\\) indicates the number of particles of flavour \\(\alpha\\) (relative to the Fermi sea) there are in the state. The Klein factor will create one more particle of 




To write the Klein factors explicitly, we define the following notation:

$$$$\begin{align}
\ket{\textbf{N}; \{m_q\}} = \prod_{q>0} \frac{(\bhat^\dagger_q)^{m_q}}{\sqrt{m_q!}} \ket{\textbf{N}}_0
\end{align}$$$$

where \\(m_q\geq 0\\) are some numbers specifying how many bosonic quanta of momentum \\(q\\) have been excited. IS THERE A CONSTRAINT ON \\(m_q\\)?

<div class="example">
<b>Example:</b>


</div>


