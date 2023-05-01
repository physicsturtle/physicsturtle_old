---
layout: lesson
title: Resolution of Identity and Trace
dept: physics
course: many-body-II
unit: unit2
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 2
---
Then, the resolution of the identity can be written as

$$$$\begin{align}
I = \sum_{n=0}^\infty \frac{1}{n!}(a^\dagger)^n\ket{0}\bra{0}a^n.
\end{align}$$$$

Another useful representation of the resolution of identity is in terms of coherent states, which we recall are eigenstates of the annihilation operator. The coherent state for the annihilation operator \\(a\\) is given by

$$$$\begin{align}
\ket{z} \propto e^{za^\dagger}\ket{0}.
\end{align}$$$$

The set of coherent states (for \\(z\in\CC\\)) is another complete set of states. It is actually an overcomplete set and not orthogonal, but that doesn't matter. Let's normalize \\(\ket{z}\\) to fix the proportionality constant. 

$$\begin{align}
\bra{0}e^{z^{*}a}e^{za^\dagger}\ket{0} =& \sum_{n=0}^\infty\bra{0}a^n(a^\dagger)^n\ket{0}\\
=& \sum_{n=0}^\infty \frac{|z|^{2n}}{n!} = e^{|z|^2}
\end{align}$$

Thus we want the coherent state to be

$$$$\begin{align}
\ket{z} = e^{-|z|^2/2}e^{za^\dagger}\ket{0}.
\end{align}$$$$

Note that it is also possible to express the coherent state as 

$$$$\begin{align}
\ket{z} = e^{-|z|^2/2}\sum_{n=0}^\infty \frac{z^n}{\sqrt{n!}}\ket{n}
\end{align}$$$$

Now, we consider the following expression, which we expect will be related to the resolution of identity. We set it to be proportional to the identity, and will prove that fact momentarily:

$$$$\begin{align}
\1 \propto \int \ket{z}\bra{z}\d z \d z^{*},
\end{align}$$$$

where the integration over \\(z\\) and \\(z^{*}\\) is meant to be interpreted as an integration over the entire complex plane; this is not a contour integral. To the best of my knowledge, there is no rigorous definition of \\(\int \d z^{*} \d z\\), and it must be defined in terms of integrals over real variables. The reason for this is because, to integrate over a complex variable, one needs to pick a path in the complex plane; here, we are actually doing an area integral over the entire complex plane. Namely, we define:

$$$$\begin{align}
\int \d z^{*} \d z := \int_{-\infty}^\infty \d\Re z \int_{-\infty}^\infty \d\Im z = \int_0^\infty \int_0^{2\pi} r\d\theta \d r.
\end{align}$$$$

Let's now show that the above expression is indeed (almost) the identity. We plug in our expression for the coherent state: 

$$\begin{align}
\int \ket{z}\bra{z}\d z \d z^{*} =& \int e^{-|z|^2}\sum_{n=0}^\infty \sum_{m=0}^\infty \frac{z^n}{n!}\frac{(z^{*})^m}{m!}(a^\dagger)^n\ket{0}\bra{0}a^m dz^{*} dz
\end{align}$$

To simplify the integral, we note that 

$$$$\begin{align}
\int e^{-|z|^2}z^n(z^{*})^mdzdz^{*} = 0,\quad n\not=m
\end{align}$$$$

This fact is due to rotational invariance. If one writes \\(z = |z|e^{i\theta}\\), then part of the integrand is \\(z^n (z^{*})^m = |z|^{n+m}e^{i\theta(n-m)}\\). Since we are integrating over the entire complex plane, one could make the substitution \\(z = we^{i\phi}\\). If this substitution is made, then one can show that the integral must be zero for \\(n\not= m\\). This is because the integral is proportional to \\(\int_0^{2\pi}e^{i(n-m)\theta}d\theta\\). Discarding this case, we now look at when \\(n=m\\). For the case \\(n=m\\), we find

$$\begin{align}
\int e^{-|z|^2}|z|^{2n} dzdz^{*} =& \int_0^{2\pi}\int_0^\infty e^{-r^2}r^{2n} r\d r\d\theta \\
=& 2\pi  \int_0^\infty e^{-r^2}r^{2n+1}dr\\
=& \pi\int_0^\infty e^{-u}u^n du\\
=& \pi n!
\end{align}$$

Thus in summary

$$$$\begin{align}
\int e^{-|z|^2}(z^{*})^m z^n \d z \d z^{*} = \pi n! \delta_{mn}
\end{align}$$$$

Thus, we plug this integration result into the above expression to give us

$$\begin{align}
\int \ket{z}\bra{z}dz dz^{*} =& \sum_{n=0}^\infty \frac{\pi n!}{(n!)^2} (a^\dagger)^n\ket{0}\bra{0}a^n\\
=& \pi \sum_{n=0}^\infty \frac{(a^\dagger)^n}{\sqrt{n!}}\ket{0}\bra{0}\frac{a^n}{\sqrt{n!}}\\
=& \pi \sum_{n=0}^\infty \ket{n}\bra{n}\\
=& \pi \1
\end{align}$$

Thus, we find the resolution of the identity in terms of bosonic coherent states:

$$$$\begin{align}
\1 = \int \ket{z}\bra{z} \frac{\d z^{*} \d z}{\pi}.
\end{align}$$$$

Similarly, we can do the same with the trace of a particular operator. Let us do this now for the trace operator. The claim is that the trace of an operator \\(A\\) is given by 

$$$$\begin{align}
\tr(A) = \int \bra{z}A \ket{z}\frac{\d z^{*} \d z}{\pi}.
\end{align}$$$$

<div class="proof">
<b>Proof:</b>
To prove this assertion, we proceed via a direct computation: 

$$\begin{align}
\tr(A) =& \sum_{m,n=0}^\infty \int e^{-|z|^2} \bra{m} \frac{(z^{*})^m}{\sqrt{m!}} A \frac{z^n}{\sqrt{n!}}\ket{n} \frac{\d z \d z^{*}}{\pi} \\
=&\sum_{m,n=0}^\infty \frac{\bra{m}A\ket{n}}{\sqrt{m!n!}} \frac{1}{\pi}\int e^{-|z|^2}(z^{*})^mz^n \d z \d z^{*}
\end{align}$$

Substituting in the value of the integral which we evaluated above, we find that 

$$\begin{align}
\tr(A) =&\sum_{m,n=0}^\infty \frac{\bra{m}A\ket{n}}{\sqrt{m!n!}} \frac{1}{\pi}\pi n!\delta_{mn} \\
=& \sum_{n=0}^\infty \bra{n}A \ket{n}
\end{align}$$

Thus the formula is verified

</div>


