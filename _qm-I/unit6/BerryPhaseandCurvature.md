---
layout: lesson
title: Berry Phase and Curvature 
dept: physics
course: qm-I
unit: unit6
deptDisplay: Physics
courseDisplay: Quantum Mechanics I
unitDisplay: Unit 6
---
Consider an adiabatically transported parameter. The Hamiltonian is \\(\Hhat = \Hhat(\bm{\lambda}(t))\\), where \\(\bm{\lambda}\\) are parameters of the Hamiltonian. We assume that the internal frequency is much greater than teh external frequency. Goal: calculate how an eigenstate of the Hamiltonian at <i>fixed</i> poarameter varies with time. If \\(\Hhat\\) is independnet of time, then a particle starting in the \\(n\\)th eigenstate 

$$\Hhat\psi_n = E_n\psi_n$$

will stay in the \\(n\\)th eigenstate. If, on the other hand, \\(\Hhat\\) depends on time, then 

$$\Hhat(t) \psi_n(t) = E_n(t) \psi_n(t)$$

But, we still have \\(\bra{\psi_n(t)}\ket{\psi_m(t)} = \delta_{mn}\\).. Also, we still have \\(i\hbar \partial_t \psi(t) = \Hhat(t) \psi(t)\\). Thus, 

$$\psi(t) = \sum_n c_n(t) \psi_n(t) e^{i\theta_n(t)}$$

where \\(\theta_n = -\frac{1}{\hbar}\int_0^t E_n(t') \d t'\\). In the Schrödinger equation, we have that 

$$\begin{align}
i\hbar\partial_t\sum_n c_n(t) e^{i\theta_n(t)} \psi_n(t) ={}& \sum_n c_n(t) e^{i\theta_n(t)} \Hhat(t)\psi_n(t) \\
i\hbar\sum_n \dot{c}_n(t) e^{i\theta_n(t)} \psi_n(t) + i\hbar \sum_n c_n(t) e^{i\theta_n(t)} \dot{\psi}_n(t) - \hbar \sum_n \dot{\theta}_n(t) c_n(t) \psi_n(t) e^{i\theta_n(t)} ={}& \sum_n c_n(t) e^{i\theta_n(t)} E_n(t)\psi_n(t) \\
\end{align}$$

But, \\(\theta_n(t) = -\frac{1}{\hbar}\int_0^t E_n(t') \d t'\\), so \\(\dot{\theta}_n = -E_n(t)/\hbar\\). Thus, we have that 

$$\sum_n \left[\dot{c}_n(t) e^{i\theta_n(t)}\psi_n(t) + c_n(t) e^{i\theta_n(t)} \dot{\psi}_n(t)\right] = 0$$

Now, we want to solve for \\(c_n(t)\\). We can derive an ODE for these constants. To do this, we can take the inner prdouct on both sides as 

$$\sum_n \left[\dot{c}_n(t) e^{i\theta_n(t)} \bra{\psi_m(t)}\ket{\psi_n(t)} + c_n(t) e^{i\theta_n(t)} \bra{\psi_m(t)}\ket{\dot{\psi}_n(t)}\right] = 0$$

Thus, solving, we have (note that we used \\(\bra{\psi_m(t)}\ket{\psi_n(t)} = \delta_{mn}\\), 

$$\dot{c}_m(t) e^{i\theta_m(t)} = -\sum_n c_n(t) e^{i\theta_n(t)} \bra{\psi_m(t)}\ket{\dot{\psi}_n(t)}$$

and finally, 

$$\dot{c}_m(t) = -\sum_n c_n(t) e^{i(\theta_n(t) - \theta_m(t))} \bra{\psi_m(t)}\ket{\dot{\psi}_n(t)}$$

We want to find an expression for \\(\ket{\dot{\psi}_n(t)}\\). For this, let us differentiate both sides of the Schrödinger equation:

$$\dot{\Hhat}(t)\ket{\psi_n(t)} + \Hhat(t)\ket{\dot{\psi}_n(t)} = \dot{E}_n(t)\ket{\psi_n(t)} + E_n(t)\ket{\dot{\psi}_n(t)}$$

Now taking the bra \\(\bra{\psi_m(t)}\\) on both sides, we have 

$$\begin{align}
\bra{\psi_m(t)}\dot{\Hhat}(t)\ket{\psi_n(t)} + \bra{\psi_m(t)}\Hhat(t)\ket{\dot{\psi}_n(t)} ={}& \bra{\psi_m(t)}\dot{E}_n(t)\ket{\psi_n(t)} + \bra{\psi_m(t)}E_n(t)\ket{\dot{\psi}_n(t)} \\
\bra{\psi_m(t)}\dot{\Hhat}(t)\ket{\psi_n(t)} + E_m(t)\bra{\psi_m(t)}\ket{\dot{\psi}_n(t)} ={}& \dot{E}_n(t)\delta_{mn} + E_n(t)\bra{\psi_m(t)}\ket{\dot{\psi}_n(t)}
\end{align}$$

Thus, 

$$(E_n(t) - E_m(t))\bra{\psi_m(t)}\ket{\dot{\psi}_n(t)} = \bra{\psi_m(t)}\dot{\Hhat}(t)\ket{\psi_n(t)} - \dot{E}_n(t)\delta_{mn}$$

Now, we split the sum for the \\(c\\) equation

$$\begin{align}
\dot{c}_m(t) ={}& - c_m(t) \bra{\psi_m(t)}\ket{\dot{\psi}_m(t)} -\sum_{n\neq m} c_n(t) e^{i(\theta_n(t) - \theta_m(t))} \bra{\psi_m(t)}\ket{\dot{\psi}_n(t)} \\
={}& - c_m(t) \bra{\psi_m(t)}\ket{\dot{\psi}_m(t)} - \sum_{n\neq m} c_n(t) e^{i(\theta_n(t) - \theta_m(t))} \frac{\bra{\psi_m(t)}\dot{\Hhat}(t)\ket{\psi_n(t)}}{E_n(t) - E_m(t)} \\
\end{align}$$

Since we have assumed that the internal frequencies are much faster than the external frequencies, \\(\dot{\psi}_m(t)\\) has an internal frequency, but \\(\dot{\Hhat}(t)\\) has an external frequency, we drop the sum. Thus, we have 

$$\begin{align}
\dot{c}_m(t) ={}& - c_m(t) \bra{\psi_m(t)}\ket{\dot{\psi}_m(t)}
\end{align}$$

Now that the equations are decoupled, we can solve this as 

$$c_m(t) = c_m(0)\exp\left(-\int_0^t \bra{\psi_m(t)}\ket{\dot{\psi}_m(t)}\d t\right)$$

Now, substituting this back in, we find 

$$\ket{\psi}(t) = \sum_n c_n(0) e^{i\gamma_n(t)} e^{i\theta_n(t)} \ket{\psi_n(t)}$$

where we have defined 

$$\gamma_n(t) = i\int_0^t \bra{\psi_n(t')}\ket{\dot{\psi}_n(t')}\d t'$$

We can rewrite this as 

$$\gamma_n(t) = i\int_{\bm{\lambda}(0)}^{\bm{\lambda}(t)} \bra{\psi_n(\bm{\lambda})}\nabla_{\bm{\lambda}}\ket{\psi_n(\bm{\lambda})} \cdot \d \bm{\lambda}$$

Then, we define 

$$\mathbf{A}_n = -i\bra{\psi_n(\bm{\lambda})}\nabla_{\bm{\lambda}}\ket{\psi_n(\bm{\lambda})}$$

so that 

$$\gamma_n(t) = -\int_{\bm{\lambda}(0)}^{\bm{\lambda}(t)} \mathbf{A}_n(\bm{\lambda}) \cdot \d\bm{\lambda}$$

If the parameters \\(\bm{\lambda}(t)\\) depend on \\(t\\) in a way that returns after \\(t=T\\) seconds, then 

$$\gamma_n = -\oint \mathbf{A}_n(\bm{\lambda}) \cdot \d\bm{\lambda}$$












Now, we make the observation that, since the Hamiltonian depended on time only via the parameters \\(\hat{H}(t) = \hat{H}(<b>X</b>(t))\\), we can use the chain rule: 

$$\begin{equation}
\frac{\partial}{\partial t}\ket{\phi_m(t)} = \frac{\partial}{\partial t}\ket{\phi_m(<b>X</b>(t))} = \frac{\partial}{\partial<b>X</b>}\ket{\phi_m(<b>X</b>)} \cdot\frac{\d <b>X</b>}{\d t}
\end{equation}$$

Thus we rewrite the formula for the geometric phase as 

$$\begin{equation}
\gamma_m(t) = i\int_0^t \bra{\phi_m(<b>X</b>(t'))}\frac{\partial}{\partial <b>X</b>}\ket{\phi_m(<b>X</b>(t'))} \cdot \frac{\d<b>X</b>}{\d t'}\d t'
\end{equation}$$

We recognize that this can be rewritten in terms of a line integral through parameter space:

$$\begin{equation}
\gamma_m(t) = -i\int_{<b>X</b>(0)}^{<b>X</b>(t)} \bra{\phi_m(<b>X</b>)}\frac{\partial}{\partial <b>X</b>}\ket{\phi_m(<b>X</b>)} \cdot\d<b>X</b>
\end{equation}$$

Now, we finally can write 

$$\begin{equation}
\ket{\Psi(t)} = \sum_n a_n(0)e^{i(\theta_n(t) - \gamma_n(t))} \ket{\phi_n(t)}.
\end{equation}$$

So the time evolution is simply the standard one: if the system is starts out in an eigenstate \\(\ket{\phi_n(t)}\\), then it stays in that eigenstate and is modified only by a phase factor. In the special case that the parameter \\(<b>X</b>\\) goes around a closed loop, the geometric phase is instead called the Berry phase, and can be written as

$$\begin{equation}
\gamma_m = -i\oint_C \bra{\phi_m(<b>X</b>)}\frac{\partial}{\partial <b>X</b>}\ket{\phi_m(<b>X</b>)} \cdot\d<b>X</b>
\end{equation}$$

Let's now turn to a discussion of the Berry phase. We define the quantity 

$$\begin{equation}
<b>A</b>_m = -i\bra{\phi_m(<b>X</b>)}\frac{\partial}{\partial <b>X</b>}\ket{\phi_m(<b>X</b>)}
\end{equation}$$

where \\(<b>A</b>\\) is a vector field with the same number of components as \\(<b>X</b>\\). In the special case where the parameter space is 3-dimensional, then we can apply Stoke's theorem to rewrite the Berry phase as 

$$\begin{equation}
\gamma_m = \iint \nabla\times<b>A</b>_m \cdot \nhat\d S.
\end{equation}$$

This resembles the integral of a magnetic field \\(<b>B</b> = \nabla\times<b>A</b>\\) over a closed surface, which is interpreted as the flux! Of course, this vector field has, in general, nothing to do with an actual magnetic field; the similarity is purely mathematical. We call the quantity \\(<b>A</b>\\) the <i>Berry connection</i> and \\(<b>B</b>\\) the <i>Berry curvature</i>. There is an interpretation of the field \\(<b>A</b>\\) as a connection in the differential geometric sense, and we will discuss that in an aside section later.

<div class="example">
<b>Example:</b>
In this example, we will actually compute the Berry phase and Berry curvature for a 2-level system. The system is a single electron immersed in a time-dependent magnetic field \(<b>B</b>\). Note that it is mere coincidence that there is an actual magnetic field in this problem; normally the vector potential and magnetic field which are abstractly discussed in the context of topological physics are merely analogous to the ones in electromagnetism. The Hamiltonian for this system is given by 

$$\begin{equation}
\hat{H} = -\bm{\mu}\cdot<b>B</b>(t)
\end{equation}$$

where \(\bm{\mu} = \gamma<b>S</b>\), and \(<b>S</b> = \frac{\hbar}{2}(\sigma^x,\sigma^y,\sigma^z)\), where \(\sigma^i\) are the ordinary Pauli matrices. The magnetic field is given by \(<b>B</b>(t) = B_0(\sin\theta\cos\varphi, \sin\theta\sin\varphi, \cos\theta)\). Therefore the Hamiltonian is 

$$\begin{equation}
\hat{H} = \frac{\omega_1\hbar}{2}\begin{pmatrix} \cos\theta & \sin\theta e^{-i\varphi} \\ \sin\theta e^{i\varphi} & -\cos \theta \end{pmatrix}
\end{equation}$$

where \(\omega_1 = eB/m\) is the cyclotron frequency. The eigenvalues of the Hamiltonian are, surprisingly, time independent and are \(E_\pm = \pm \hbar\omega_1/2\). The corresponding eigenvectors of this Hamiltonian can be calculated as 

$$\begin{equation}
\ket{\chi_+} = \begin{pmatrix}\cos(\theta/2)  \\ \sin(\theta/2) e^{i\varphi} \end{pmatrix} ,\qquad \ket{\chi_-}  = \begin{pmatrix} \sin(\theta/2)e^{-i\varphi} \\ -\cos(\theta/2) \end{pmatrix}
\end{equation}$$

Now that we have the two states of the system, we can compute the gradient, which will appear in the Berry connection. This gives us 

$$\begin{align}
\nabla \ket{\chi_+} =& \frac{1}{r}\frac{\partial \ket{\chi_+}}{\partial\theta} \hat{e}_\theta + \frac{1}{r \sin\theta}\frac{\partial \ket{\chi_+}}{\partial\varphi}\hat{e}_\varphi \\
=& \frac{1}{2r}\begin{pmatrix} -\sin(\theta/2) \\ \cos(\theta/2)e^{i\varphi} \end{pmatrix} \hat{e}_\theta + \frac{1}{r\sin\theta}\begin{pmatrix} 0 \\ i\sin(\theta/2)e^{i\varphi}\end{pmatrix} \hat{e}_\varphi 
\end{align}$$

Similarly, we can compute 

$$\begin{align}
\nabla\ket{\chi_-} = \frac{1}{2r}\begin{pmatrix} \cos(\theta/2)e^{-i\varphi} \\ \sin(\theta/2) \end{pmatrix} \hat{e}_\theta + \frac{1}{r\sin\theta} \begin{pmatrix} -i\sin(\theta/2) e^{-i\varphi} \\ 0\end{pmatrix} \hat{e}_\varphi
\end{align}$$

Therefore, we find the Berry connections for the different ``bands" to be:

$$\begin{equation}
\bra{\chi_+}\nabla\ket{\chi_+} = i\frac{\sin^2(\theta/2)}{r\sin\theta} \hat{e}_\varphi,\qquad \bra{\chi_-}\nabla\ket{\chi_-} = -i\frac{\sin^2(\theta/2)}{r\sin\theta}\hat{e}_\varphi
\end{equation}$$

so the Berry connections are 

$$\begin{equation}
<b>A</b>_\pm = \pm \frac{\sin^2(\theta/2)}{r\sin\theta}\hat{e}_\varphi
\end{equation}$$

Next, we need to compute the curl of these quantities, which gives us the Berry curvature:

$$\begin{equation}
<b>B</b>_\pm = \pm \frac{1}{2r^2}\hat{e}_r
\end{equation}$$

Lastly, we can integrate this to find the Berry phase:

$$\begin{align}
\gamma_\pm =& \int<b>B</b>_\pm \cdot \nhat\d S \\
=& \int <b>B</b>_\pm \cdot \hat{e}_r r^2\d\Omega \\
=& \frac{1}{2}\int \d\Omega \\
=& \frac{\Omega}{2}
\end{align}$$

where \(\Omega\) is the solid angle traced out by the closed trajectory in \(\theta,\varphi\) space. 



</div>


\subsection{Quantum Harmonic Oscillator I}

In this lesson, we will discuss the quantum mechanical analogue of the harmonic oscillator. In classical mechanics, we solved Newton's equation for the force \\(F(x) = -kx\\), where \\(k\\) is some spring constant. The corresponding potential energy is found by integrating up

$$\frac{dV}{dx} = -F(x),$$

which gives us the potential 

$$V(x) = \frac{1}{2}kx^2.$$

It is important that we have the potential because, in quantum mechanics, the fundamental equation is the Schrödinger equation. The Schrödinger equation does not have a force term, but rather the potential energy. This means that the appropriate (time independent) Schrödinger equation is

$$\left(-\frac{\hbar^2}{2m}\frac{d^2}{dx^2} + \frac{1}{2}kx^2\right)\psi = E\psi.$$

In quantum mechanics, there isn't an analogue of spring constant, so instead, we use the equation for the resonant frequency \\(\omega^2 = k/m\\) to substitute in for \\(k\\). This gives us the equation we actually want to solve:

Quantum Harmonic Oscillator Schrödinger Equation
For a quantum harmonic oscillator of frequency \\(\omega\\), the Schrödinger equation is
$$\left(-\frac{\hbar^2}{2m}\frac{d^2}{dx^2} + \frac{1}{2}\omega^2m x^2\right)\psi = E\psi.$$
Since the wave function should decay at infinity (we want it to be normalizable!), we set the boundary conditions simply to be
$$\lim_{x\to\pm\infty} \psi(x) = 0.$$


Now, let's actually solve this equation! There are two approaches that we will perform here. 
The first is much less elegant, but it is also more concrete; it is solving the differential equation by brute force. 

The second is defining some useful operators known as the raising and lowering operators, which allows us to simplify the differential equation substantially. 


Massaging the Differential Equation

For the brute force approach, we just need to solve the differential equation! This is however easier said than done! Before moving on to actually solving it, let's rewrite the equation in terms of a dimensionless (unitless) variable \\(\xi\\). To determine what this variable should be, rewrite the equation 

$$\left(-\frac{\hbar}{m\omega}\frac{d^2\psi}{dx^2} + \frac{\omega m}{\hbar} x^2 \psi\right) = \frac{2E}{\hbar\omega}\psi.$$

Notice that on the left hand side of the equation, we have the expression \\(\omega m x^2/\hbar\\) in the denominator of the first term, and the same expression in the numerator of the second term (I know it isn't technically in the denominator of the first term because it is \\(dx^2\\), not \\(x^2\\), but for variable changing purposes it doesn't matter). This suggests the substitution

$$\xi = \sqrt{\frac{\omega m}{\hbar}} x.$$

Making this substitution, as well as defining a modified eigenvalue \\(\lambda = 2E/m\omega\\), we get 

$$-\frac{d^2\psi}{d\xi^2} + \xi^2\psi = \lambda\psi.$$

This is now the differential equation that we want to solve. However, you have not likely seen this equation in your differential equations courses! To solve it, we need to make a substitution. This substitution makes this problem much easier, but a priori, there is no way to know what it is! There are various arguments from asymptotic analysis that one can make, but I will simply show you what the substitution is. The substitution is 

$$\psi(\xi) = u(\xi)e^{-\xi^2/2}.$$

Note that the substitution \\(\psi(\xi) = u(\xi)e^{\xi^2/2}\\) also substantially simplifies the equation, but we reject it because it doesn't decay to zero at infinity. We calculate the derivatives of our substitution to find 

$$\psi'(\xi) = (-\xi u + u')e^{-\xi^2/2},\qquad \psi"(\xi) = (-u + \xi^2 u - 2\xi u' + u")e^{-\xi^2/2}$$

Plugging in the second derivative to the equation, we find that 

$$-(-u + \xi^2 u - 2\xi u' + u")e^{-\xi^2/2} + \xi^2 u e^{-\xi^2/2} = \lambda u e^{-\xi^2/2}$$

Cancelling all factors of \\(e^{-\xi^2/2}\\) and simplifying, we get 

$$u + 2\xi u' - u" = \lambda u.$$

Lastly, gathering like terms we get

$$u" - 2\xi u' + (\lambda - 1)u =0.$$

Power Series Solution

Now, we need to solve this using a power series solution. The power series solution takes the form

$$u(\xi) = \sum_{n=0}^\infty a_n \xi^n = a_0 + a_1 \xi + a_2 \xi^2 + \cdots.$$

Substituting this into the differential equation, we get 

$$\sum_{n=2}^\infty n(n-1)a_n \xi^{n-2} -2\xi \sum_{n=1}^\infty na_n \xi^{n-1} + (\lambda-1) \sum_{n=0}^\infty a_n \xi^n = 0 $$

Next, we shift the indices of the first and second sums so that the powers of \\(\xi^n\\) all match:

$$\sum_{n=0}^\infty(n+2)(n+1)a_{n+2} \xi^{n} -2\sum_{n=1}^\infty na_{n}\xi^{n} + (\lambda-1)\sum_{n=0}^\infty a_n \xi^n = 0$$

Now we peel off the \\(n=0\\) terms from the first and third sums so that the sums all start at \\(n=1\\).

$$\sum_{n=1}^\infty\left[(n+2)(n+1)a_{n+2}-2na_{n}+(\lambda-1) a_n \right]\xi^{n}+2a_{2}+(\lambda-1) a_{0} = 0$$

This gives us that \\(a_2 = -\frac{(\lambda-1) a_{0}}{2}\\). The recurrence relation is: 

$$a_{n+2} = \frac{2n-(\lambda-1)}{(n+2)(n+1)}\cdot a_n,\qquad n\geq 2$$

Note that this also satisfies our extra condition \\(a_2 = -\frac{(\lambda-1) a_{0}}{2}\\), so we can in fact define it for \\(n\geq 0\\):

$$a_{n+2} = \frac{2n-(\lambda-1)}{(n+2)(n+1)}\cdot a_n,\qquad n\geq 0$$

This gives us two solutions. Set \\(a_0\\) and \\(a_1\\) arbitrary, then generate all further terms. Now, notice that for \\(n\\) large, the recurrence relation is like 

$$a_{n+2}\sim \frac{2}{n}a_n,\qquad n\to\infty$$

the solution to which is \\(a_{n} \sim \frac{1}{(n/2)!}\\), \\(n\to\infty\\). This generates the coefficients for the power series 

$$e^{\xi^2} = \sum_{\stackrel{n=0}{n\,\text{even}}}^\infty \frac{\xi^{n}}{(n/2)!}$$

What this means for us, is that if we allow the recurrence relation to continue forever, we will get solutions like \\(u(\xi) \sim e^{\xi^2}\\), which leads again to \\(\psi(\xi) = e^{\xi^2}e^{-\xi^2/2} = e^{\xi^2/2}\\), which goes to infinity and is non-normalizable! Our conclusion is that our recurrence relation *must terminate*. The relation terminates if 

$$2n = \lambda - 1$$

for some \\(n\\). This gives us the value for our eigenvalue \\(\lambda\\). Thus, 

$$\lambda = 1 + 2n$$

Plugging back in our previous expression for \\(\lambda = 2E/\hbar\omega\\), we finally get the energy eigenvalues for the system:

$$E = \hbar\omega\left(\frac{1}{2} + n\right),\qquad n\geq 0$$

The \\(n=0\\) case is known as the <i>zero point energy</i> of the harmonic oscillator. Let's work now on the eigenfunctions of the system. The eigenfunctions corresponding to these eigenvalues are known as the Hermite polynomials, \\(H_n(\xi)\\). If you want more information about the Hermite polynomials, consult a book on mathematical physics or special functions. 

<ol>
<li> <div class="exercise">  
</div> </li></ol>

\subsection{Quantum Harmonic Oscillator II}
For an ordinary classical harmonic oscillator, the Hamiltonian is given by

$$H = \frac{p^2}{2m} + \frac{1}{2}m\omega^2 x^2$$

where we have replaced \\(k = m\omega^2\\). In the corresponding quantum theory, we promote \\(p\\) and \\(x\\) to operators, and get that 

$$\hat{H} = \frac{\hat{p}^2}{2m} + \frac{1}{2}m\omega^2\hat{x}^2.$$

We simplify the Hamiltonian by factoring it. Note that a usual factoring (as difference of squares) is not possible because \\([\hat{x},\hat{p}]\neq =0\\). Thus, we write 

$$\begin{align}
\hat{H} =& \frac{1}{2}(\hat{p}^2+ m^2\omega^2 \hat{x}^2) \\
=& \frac{1}{2m}\left((-i\hat{p} + m\omega \hat{x})(ip+m\omega\hat{x}) - m\omega\hat{x} i\hat{p} + i\hat{p}m\omega\hat{x}\right) \\
=& \frac{1}{2m}((-i\hat{p} + m\omega\hat{x})(i\hat{p} + m\omega\hat{x}) - im\omega[\hat{x},\hat{p}]) \\
=& \frac{1}{2m}((-i\hat{p} + m\omega\hat{x})(i\hat{p} + m\omega\hat{x}) + m\omega\hbar) \\
=& \hbar\omega\left(\frac{(-i\hat{p} + m\omega\hat{x})(i\hat{p} + m\omega\hat{x})}{2\hbar\omega m} + \frac{1}{2}\right) \\
=& \hbar\omega\left(\left(\frac{-i\hat{p} + m\omega\hat{x}}{\sqrt{2\hbar\omega m}}\right)\left(\frac{i\hat{p} + m\omega\hat{x}}{\sqrt{2\hbar\omega m}}\right) + \frac{1}{2}\right)
\end{align}$$

which leads us to define 

$$\ahat^\dagger = \frac{1}{\sqrt{2\hbar m\omega}}(-i\hat{p} + m\omega\hat{x}),\qquad \ahat = \frac{1}{\sqrt{2\hbar m\omega}}(i\hat{p} + m\omega\hat{x})$$

THus, the Hamiltonian is rewritten as 

$$\hat{H} = \hbar\omega\left(\ahat^\dagger\ahat+\frac{1}{2}\right).$$

This tells us that \\(E_n = \hbar\omega(n+1/2)\\). 

We can invert the relations for the creation/annihilation operators to find that 

$$\xhat = \sqrt{\frac{\hbar}{2m\omega}}(\ahat+\ahat^\dagger),\quad \phat = i\sqrt{\frac{\hbar m\omega}{2}}(\ahat^\dagger-\ahat)$$

