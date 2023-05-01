---
layout: lesson
title: Bosonization (constructive)
dept: physics
course: many-body-II
unit: unit17
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 17
---
The field theoretic bosonization is confusing and is in the other section. Here we will follow ``bosonization for beginners" by von Delft. Bosonization is a technique which is applicable to continuum theories. Since we usually work on the lattice however, we need to take the continuum limit of our lattice problems. One way to do this is start with the lattice problem (in a finite-sized box), with creation/annihilation operators \\(\chat_{i\sigma},\chat^\dagger_{i\sigma}\\) for electrons in a Wannier function on site \\(i\\) with spin \\(\sigma\\). Then, we Fourier transform to the basis \\(\chat_{k\sigma}, \chat^\dagger_{k\sigma}\\). Here, \\(k\\) is a discrete index because the original system was finite, and it is bounded since the original system was a lattice system. We can then take the continuum limit by continuing all functions of \\(k\\) to take any value of \\(k\\), rather than just ones in the first Brillouin zone. We can then Fourier transform back to position space, and then find a continuum theory.

Our starting point is fermionic creation/annihilation operators \\(\chat_{k\alpha}, \chat^\dagger_{k\alpha}\\). The canonical anticommutation relation between them is simply given by 

$$$$\begin{align}
\{\psihat_{k\alpha}, \psihat^\dagger_{k'\alpha'}\} = \delta_{\alpha\alpha'}\delta_{kk'}.
\end{align}$$$$

\noindent Here, \\(k\\) is an unbounded but discrete index. This is from a continuous but finite-sized system. We discretize \\(k\\) by 

$$$$\begin{align}
k = \frac{2\pi}{L}\left(n - \frac{1}{2}\delta_b\right),\quad n\in \ZZ,
\end{align}$$$$

\noindent and \\(\delta_b \in [0,2)\\) is a continuous but bounded parameter which quantifies the boundary conditions for the fermions. QUESTION: WHY ARE WE USING BLOCH'S THEOREM IF WE DON'T HAVE PROPER PERIODIC BOUNDARY CONDITIONS?? Here, \\(\alpha\\) is a flavour index, running from \\(1\\) to \\(M\\) flavours. For example, \\(M\\) may represent spin up/down, or it may represent left/right movers, or even both! It may also represent orbital/channel for the case of the Kondo effect. Note that it is important that the system size \\(L\\) be finite. If we want to send it to infinity at the end, then we may. The position space fermion fields are given by the following Fourier transform relation:

$$$$\begin{align}
\psihat_\alpha(x) = \frac{1}{\sqrt{L}}\sum_{k=-\infty}^\infty e^{ikx} \psihat_{k\alpha}, \quad \psihat_{k\alpha} = \frac{1}{\sqrt{L}}\int_{-L/2}^{L/2} e^{-ikx} \psihat_\alpha(x) \d x.
\end{align}$$$$

\noindent This gives us the following commutation relation for the position space operators:

$$\begin{align}
\{\psihat_\alpha(x), \psihat^\dagger_{\alpha'}(x') \} =& \frac{1}{L}\sum_{k,k'} e^{ikx} e^{-ik'x'} \{ \psihat_{k\alpha} ,\psihat^\dagger_{k'\alpha'}\} \\
=& \frac{1}{L}\sum_{k,k'} e^{ikx} e^{-ik'x'} \delta_{\alpha\alpha'} \delta_{kk'} \\
=& \frac{1}{L}\delta_{\alpha\alpha'}\sum_{k} e^{ik(x-x')} \\
=& \frac{1}{L}\delta_{\alpha\alpha'} e^{i\delta_b\pi(x-x')/L} 2\pi \sum_{\bar{n}\in\ZZ}\delta\left(\frac{2\pi(x-x')}{L}-2\pi\bar{n}\right) \\
=& \delta_{\alpha\alpha'} e^{i\delta_b\pi(x-x')/L} \sum_{\bar{n}\in\ZZ}\delta(x-x'-L\bar{n}) \\
=& \delta_{\alpha\alpha'} \sum_{\bar{n}\in\ZZ}\delta(x-x'-L\bar{n})e^{i\delta_b\pi\bar{n}}
\end{align}$$

\noindent Note that the definition of the position space fermion operators has a consequence in terms of the boundary condition. This gives us 

$$\begin{align}
\psihat_\alpha(x+L/2) =& \frac{1}{\sqrt{L}}\sum_{k=-\infty}^\infty e^{ik(x+L/2)} \psihat_{k\alpha} \\
=& \frac{1}{\sqrt{L}}\sum_{k=-\infty}^\infty e^{ik(x-L/2)} \psihat_{k\alpha} e^{ikL} \\
=& e^{-i\pi\delta_b}  \frac{1}{\sqrt{L}}\sum_{k=-\infty}^\infty e^{ik(x-L/2)} \psihat_{k\alpha} \\
=& e^{-i\pi\delta_b} \psihat_{\alpha}(x-L/2).
\end{align}$$

