---
layout: lesson
title: Bosonic Fock Space
dept: physics
course: many-body-II
unit: unit17
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 17
---
The reason why bosonizing is possible is that for 1 dimensional fermionic theories, the Fock space \\(\mathcal{F}\\) which is spanned by \\(\chat_{k\alpha}\\) can be organized as a direct sum

$$$$\begin{align}
\mathcal{F} = \bigoplus_\textbf{N} \mathcal{H}_\textbf{N}
\end{align}$$$$

Here, \\(\textbf{N}\\) is a vector which contains the number of particle-hole excitations. Note that, to define excitation, it has to be an excitation \textit{on top of} a particular ground state. We will define this ground state momentarily, and note that the class of Hamiltonians we will consider must satisfying that the to-be-defined ground state is indeed the ground state of the noninteracting part of the Hamiltonian. Now, this vector \\(\textbf{N}\\) has \\(M\\) components, one for each flavour of fermion. 

<div class="example">
<b>Example:</b>
Suppose we have a system of spin up and spin down fermions. Then, if the vector \\(\textbf{N} = (N_\uparrow,N_\downarrow) = (1,2)\\), then this means that the corresponding Hilbert space \\(\HH_\textbf{N}\\) contains all the states which have 1 spin-up fermion and 2 spin-down fermions above the Fermi level, as well as 

</div>

Note that we are staying in a fixed particle sector of the Hilbert space; there are always the same number of fermions. This is effectively working in the canonical ensemble. We will transition to the grand canonical ensemble later when we introduce Klein factors. Now we define the ground state of the system.

\begin{definition_wrapper}
\begin{definition}
Let \\(\ket{0}_0\\) be the state defined by 

$$$$\begin{align}
\begin{cases} 
\psihat_{k\alpha}\ket{0}_0 = 0 & k > 0 \\
\psihat^\dagger_{k\alpha}\ket{0}_0 = 0 & k \leq 0 
\end{cases}
\end{align}$$$$

This means the so-defined ground state has no particles with \\(k>0\\), and is full for the particles with \\(k\leq 0\\). To be clear, this is not truly an ``empty" state, but is rather a Fermi sea. Furthermore, note that this Fermi sea ground state is the ground state of a noninteracting Hamiltonian, not an interacting one. 

We note that the same property is shared by all flavours of electron. In practice, the definition of the state may have different properties for different flavours of electrons. In this case, everything is essentially composed of right-movers. 
\end{definition}
\end{definition_wrapper}

We can now define normal ordering \textit{with respect to} this vacuum state. This is defined as

$$$$\begin{align}
:ABC\dots: = ABC\dots - \bra{0}_0 ABC\dots \ket{0}_0,
\end{align}$$$$
%
where \\(A,B,C\dots\\) are either creation/annihilation operators. Armed with the normal ordering notation, we can then define the number operator, which measures the number of electrons with a particular flavour with respect to \\(\ket{0}_0\\). This operator is given by 

$$\begin{align}
\hat{N}_\alpha =& \sum_{k=-\infty}^\infty :\psihat^\dagger_{k\alpha} \psihat_{k\alpha}: \\
=& \sum_{k=-\infty}^\infty \left(\psihat^\dagger_{k\alpha} \psihat_{k\alpha} - \bra{0}_0 \psihat^\dagger_{k\alpha} \psihat_{k\alpha} \ket{0}_0\right).
\end{align}$$
%
Using this operator, we can define the set of all states which have the same number of \\(\alpha\\)-type electrons in them, where \\(\textbf{N} = (N_1,\dots,N_M) \in \ZZ^M\\). We call this the \\(\textbf{N}\\)-particle Hilbert space \\(H_\textbf{N}\\). This Hilbert space contains infinitely many states, each with different particle hole configurations. We emphasize that this Hilbert space can have any number of particles (again measured with respect to the vacuum \\(\ket{0}_0\\)).

We then are led to define \\(\ket{\textbf{N}}_0\\) to be the specific \\(\textbf{N}\\)-particle state in \\(H_\textbf{N}\\) which has no particle-hole excitations. What we mean by ``no particle-hole excitations" is that there are no missing wave vectors. We fill all consecutive wave vectors up until a certain number of states have been filled. Although we haven't specified a Hamiltonian, we are calling this the lowest-energy state in \\(H_\textbf{N}\\), and call it the \\(\textbf{N}\\)-particle ground state. We define it in a particular way so that no ambiguities in the phase arise:

$$\ket{\textbf{N}}_0 = (\hat{C}_1)^{N_1}(\hat{C}_2)^{N_2}\cdots (\hat{C}_M)^{N_M}\ket{0}_0$$

where the operators \\((\hat{C}_\alpha)^{N_\alpha}\\) are given by (note that the \\(N_\alpha\\) superscript is NOT an exponent)

$$$$\begin{align}
(\hat{C}_\alpha)^{N_\alpha} = \begin{cases} \psihat^\dagger_{N_\alpha \alpha} \psihat^\dagger_{(N_\alpha-1)\alpha} \cdots \psihat^\dagger_{1\alpha} & N_\alpha > 0 \\
1 & N_\alpha = 0 \\
\psihat_{(N_\alpha+1)\alpha} \psihat_{(N_\alpha+2)\alpha} \cdots \psihat_{0\alpha} & N_\alpha < 0
\end{cases}
\end{align}$$$$
%
Here, we have \\(\psihat_{n\alpha} = \psi_{k\alpha}\\), where \\(k = \frac{2\pi}{N}(n - \frac{\delta_b}{2})\\). This means that, if \\(N_\alpha > 0\\), \\((\hat{C}_\alpha)^{N_\alpha}\\) fills up all the positive momenta up until \\(k = \frac{2\pi}{L}(N_\alpha-\delta_b/2)\\). Similarly, if \\(N_\alpha < 0\\), then \\((\hat{C}_\alpha)^{N_\alpha}\\) removes all particles starting from zero momenta, and then going to more and more negative momenta until reaching \\(k = \frac{2\pi}{L}(N_\alpha+1-\delta_b/2)\\). 

<div class="example">
<b>Example:</b>
Consider a single flavour of electrons. Sketch the following states schematically:
<ol type="a">
</li> 
 <li> \\(\ket{0}_0\\)
</li> 
 <li> \\(\ket{4}_0\\)
</li> 
 <li> \\(\ket{-3}_0\\)
\end{parts}


</div>

Now, we want to build the bosonic particle-hole operators. We want to note that, since the states in the \\(\textbf{N}\\)-particle Hilbert space all have the same number of particles, they can be regarded as particle-hole excitations built on the ground state \\(\ket{\textbf{N}}_0\\). We define the bosonic creation and annihilation operators (for \\(q > 0\\)) as

$$\varphihat^\dagger_{q\alpha} := -\frac{i}{\sqrt{n_q}}\sum_{k=-\infty}^\infty \psihat^\dagger_{k+q,\alpha} \psihat_{k\alpha},\quad \varphihat_{q\alpha} := \frac{i}{\sqrt{n_q}}\sum_{k=-\infty}^\infty \psihat^\dagger_{k-q,\alpha} \psihat_{k\alpha}$$

where \\(q = 2\pi n_q/L\\) and \\(n_q\in \ZZ^+\\) is positive. Let's quickly discuss these operators. We see that \\(\bhat^\dagger_{q\alpha}\\) creates a superposition of states, each of which has an electron removed and placed \\(q\\) higher. 

Therefore, if we have a state \\(\ket{\textbf{N}}\\), the state \\(\varphihat^\dagger_{q\alpha}\ket{\textbf{N}}\\) has additional particle-hole excitations compared to \\(\ket{\textbf{N}}\\), and therefore consists of a linear combinations of a bunch of different states in \\(H_\textbf{N}\\). Each term in the linear combination has \\(q\\) units of momentum more than \\(\textbf{N}\\). Thus, we can think of \\(\varphihat^\dagger_{q\alpha}\\) and \\(\varphihat_{q\alpha}\\) as momentum raising/lowering operators. The commutation relations can be derived to be 

$$$$\begin{align}
[\varphihat_{q\alpha},\varphihat_{q'\alpha'}] = [\varphihat^\dagger_{q\alpha}, \varphihat^\dagger_{q'\alpha'}] = 0,\quad [\hat{N}_{q\alpha},\varphihat_{q'\alpha'}] = [\hat{N}_{q\alpha},\varphihat^\dagger_{q'\alpha'}] = 0,\quad [\varphihat_{q\alpha},\varphihat^\dagger_{q'\alpha'}] = \delta_{\alpha\alpha'}\delta_{qq'}
\end{align}$$$$

We now note that, since the state \\(\ket{\textbf{N}}_0\\) has no particle-hole excitations the particle-hole pair annihilation operator \\(\bhat_{q\alpha}\\) should annihilate it:

$$\varphihat_{q\alpha} \ket{\textbf{N}}_0 = 0$$

We then can define the boson normal ordering with respect to this ground state as 

$$:ABC\dots: = ABC\dots - \bra{\textbf{N}}_0ABC\dots \ket{\textbf{N}}_0$$

where \\(A,B,C,\dots\\) are either \\(\varphihat_{q\alpha}\\) or \\(\varphihat^\dagger_{q\alpha}\\). Note that we are fortunate in that hte boson-normal ordered expression is also fermion normal ordered which can be noted by setting \\(\textbf{N} = 0\\) in the above equation. Similarly, if a product of boson operators is fermion normal-ordered, then it will also be boson normal ordered.

It should be clear that we can create a state \\(\ket{\textbf{N}}\\) with any number of particle-hole pairs in it (with starting \\(\textbf{N}\\) particles) from using fermion creation/annihilation operators acting on \\(\ket{\textbf{N}}_0\\) via \\(\ket{\textbf{N}} = \bar{f}(\psihat^\dagger_{k\alpha}\psihat_{k'\alpha})\ket{\textbf{N}}_0\\). It is actually possible to do this in terms of the boson operators as well \\(\ket{\textbf{N}} = f(\varphihat^\dagger)\ket{\textbf{N}}_0\\). This is not an intuitive statement because the operator \\(\psihat^\dagger\\) contains an infinite sum of fermion creation/annihilation operators. This is actually a very nontrivial statement because the boson operators are infinite sums of pairs of fermion operators. 

<div class="proof">
<b>Proof:</b>


</div>


