---
layout: lesson
title: Massless Scalar Boson
dept: physics
course: many-body-II
unit: unit19
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 19
---
Now that we have studied the massless Dirac fermion, we will study the massless scalar boson. We will observe a number of similarities between these two. This will allow us to compute correlation functions either in the boson language or fermion language. We consider the following Hamiltonian of bosonic fields:

$$$$\begin{align}
H_B = \frac{1}{2}\int\left(\Pihat^2 + (\partial_x\phihat)^2\right) \d x
\end{align}$$$$

where \\([\phihat(x),\Pihat(y)] = i\delta(x-y)\\). We then perform the standard mode expansion for the fields:

$$\begin{align}
\phihat(x) =& \int_{-\infty}^\infty \left(\phihat(k)e^{ikx} + \phihat^\dagger(k)e^{-ikx}\right)e^{-\frac{1}{2}\eta|k|} \frac{\d k}{\sqrt{2|k|}2\pi} \\
\Pihat(x) =& \int_{-\infty}^\infty \left(-i\phihat(k)e^{ikx} + i\phihat^\dagger(k)e^{-ikx}\right)e^{-\frac{1}{2}\eta|k|} \frac{|k|\d k}{\sqrt{2|k|}2\pi} 
\end{align}$$

From this, we can derive that \\([\phihat(k),\phihat^\dagger(k')] = 2\pi\delta(k-k')\\). Therefore, we can calculate that

$$$$\begin{align}
\Hhat_B = \int_{-\infty}^\infty \phihat^\dagger(k)\phihat(k)|k|\frac{\d k}{2\pi}
\end{align}$$$$

with an infinite extra term thrown out. We note that the energy of a particle with momentum \\(k\\) is \\(E = |k|\\). Thus, if \\(k > 0\\), then its velocity is positive, and if \\(k < 0\\), then its velocity is negative. The ground state can also be identified from this; since a particle of any momentum will have positive energy, the ground state has no particles in it at all. We therefore define 

$$$$\begin{align}
\phihat^\dagger(k) = \begin{cases} \phihat^\dagger_+(k), & k > 0 \\ \phihat^\dagger_-(k), & k < 0 \end{cases},\qquad \phihat(k) = \begin{cases} \phihat_+(k), & k > 0 \\ \phihat_-(k), & k < 0 \end{cases}
\end{align}$$$$

$$\begin{align}
\Hhat_B =& \int_{-\infty}^0 \phihat^\dagger(k)\phihat(k)|k|\frac{\d k}{2\pi} + \int_{0}^\infty \phihat^\dagger(k)\phihat(k)|k|\frac{\d k}{2\pi} \\
=& \int_{-\infty}^0 \phihat^\dagger_-(k)\phihat_-(k)(-k)\frac{\d k}{2\pi} + \int_{0}^\infty \phihat_+^\dagger(k)\phihat_+(k)k\frac{\d k}{2\pi} 
\end{align}$$

We then introduce the left and right movers 

$$\begin{align}
\phihat_{\p}m(x) =& \frac{1}{2}\left(\phihat(x) \mp \int_{-\infty}^x \Pihat(x')\d x'\right) \\
=& \frac{1}{2}\left( \int_{-\infty}^\infty \left(\phihat(k)e^{ikx} + \phihat^\dagger(k)e^{-ikx}\right) \frac{e^{-\frac{1}{2}\eta|k|}\d k}{\sqrt{2|k|}2\pi} \mp \int_{-\infty}^x \int_{-\infty}^\infty \left(-i\phihat(k)e^{ikx} + i\phihat^\dagger(k)e^{-ikx}\right) \frac{e^{-\frac{1}{2}\eta|k|}|k|\d k}{\sqrt{2|k|}2\pi} \d x' \right)
\end{align}$$

Then, we use the fact that 

$$$$\begin{align}
\int_{-\infty}^x e^{ikx'} \d x' = \mathcal{P}\frac{e^{ikx}}{ik} + \pi\delta(k)
\end{align}$$$$

where \\(\mathcal{P}\\) denotes the Cauchy principal value of whatever integral is evaluated after this. Thus 

$$\begin{align}
\phihat_{\p}m(x) =& \frac{1}{2}\left( \int_{-\infty}^\infty \left(\phihat(k)e^{ikx} + \phihat^\dagger(k)e^{-ikx}\right) \frac{e^{-\frac{1}{2}\eta|k|}\d k}{\sqrt{2|k|}2\pi} \mp \int_{-\infty}^\infty \left(-\phihat(k)e^{ikx'} - \phihat^\dagger(k)e^{-ikx'}\right) \frac{e^{-\frac{1}{2}\eta|k|}(|k|/k)\d k}{\sqrt{2|k|}2\pi} \right) \\
=& \frac{1}{2}\int_{-\infty}^\infty \left(1 \pm \frac{|k|}{k}\right)\left(\phihat(k)e^{ikx} + \phihat^\dagger(k)e^{-ikx}\right) \frac{e^{-\frac{1}{2}\eta|k|}\d k}{\sqrt{2|k|}2\pi} \\
=& \pm \int_0^{\pm\infty} \left(\phihat(k)e^{ikx} + \phihat^\dagger(k)e^{-ikx}\right) \frac{e^{-\frac{1}{2}\eta|k|}\d k}{\sqrt{2|k|}2\pi} \\
\end{align}$$

Now, we compute the correlation function

$$\begin{align}
G_{\p}m(x) =& \langle \phihat_{\p}m(x)\phihat_{\p}m(0) - \phihat_{\p}m(0)^2\rangle \\
=& \frac{1}{4\pi}\log\left(\frac{\eta}{\eta\mp ix}\right)
\end{align}$$

What happens then if we compute 

$$\begin{align}
G_\beta(x) =& \langle e^{i\beta\phihat(x)}e^{-i\beta\phihat(0)}\rangle
\end{align}$$

To do this, it is actually easiest to work in the framework of the path integral. For this model, the Hamiltonian density was given by 

$$$$\begin{align}
\HH = \frac{1}{2}(\Pi^2 + (\partial_x\phi)^2)
\end{align}$$$$

Using Hamilton's equations, we find that 

$$\dot{\phi} = \Pi$$

So changing this back to the Lagrangian language, we find that 

$$$$\begin{align}
\L = \frac{1}{2}(\dot{\phi}^2 - (\partial_x\phi)^2)
\end{align}$$$$

Therefore, if we set up the path integral, the real time action is given by 

$$$$\begin{align}
S_0 = \frac{1}{2}\int(\dot{\phi}^2 - (\partial_x\phi)^2)\d x \d t
\end{align}$$$$

and the imaginary time action should be 

$$\begin{align}
S_0 =& \frac{1}{2}\iint_0^\beta \left[\left(\frac{\partial\phi}{\partial\tau}\right)^2 + \left(\frac{\partial \phi}{\partial x}\right)^2\right] \d \tau\d x \\
=& \frac{1}{2}\int |\phi(k,\omega)|^2(k^2+\omega^2)\frac{\d k\d\omega}{(2\pi)^2}
\end{align}$$

where we used the Fourier transform

$$$$\begin{align}
\phi(x,\tau) = \int e^{-i\omega\tau}e^{ikx}\phi(k,\omega)\frac{\d k\d\omega}{(2\pi)^2}
\end{align}$$$$

We will derive a general formula for the correlation function

$$\begin{align}
G_\beta(x) =& \langle e^{i\int \phi(x,\tau) f(x,\tau) \d x \d\tau} \rangle \\
=& \frac{1}{\int e^{-S_0}\D\phi}\int e^{-S_0}
\end{align}$$

$$\begin{align}
\left<e^{i\int \tilde{\phi}\tilde{f}\frac{d\omega dk}{(2\pi)^2}}\right> =& e^{-\frac{1}{2}\int \frac{|\tilde{f}(\omega,k)|^2}{\omega^2+k^2}\frac{dkd\omega}{(2\pi)^2}} \\
=& \exp(-\frac{1}{2}\int f(\tau,x)G(\tau-\tau',x-x')f(\tau',x')d\tau dx d\tau' dx')
\end{align}$$

where \\(G(\tau,x) = \int \frac{e^{i(\omega\tau + kx)}}{\omega^2+k^2} \frac{d\omega dk}{(2\pi)^2}\\)

This is the Green function for \\(\phi\\) that we calculated last lecture. This can be doing \\(\omega\\) integral by contour method. 

$$$$\begin{align}
G(\tau,x) = \frac{1}{4\pi}\int e^{-|k||\tau|+ikx}\frac{dk}{|k|}
\end{align}$$$$

as we saw before, this is infrared divergent, but we will see that only \\(G(\tau,x) - G(0,0)\\) is needed. To calculate

$$$$\begin{align}\left<e^{i\beta(\phi(\tau,x)-\phi(0,0))}\right>\end{align}$$$$

we choose

$$$$\begin{align}
f(\tau',x') = \beta(\delta(\tau'-\tau)\delta(x'-x)-\delta(\tau')\delta(x'))
\end{align}$$$$

so 

$$\begin{align}
\left<e^{i\beta(\phi(\tau,x) - \phi(0,0))}\right> =& e^{\beta^2(G(\tau,x) - G(0,0))} \\
=& e^{-\beta^2\log(\Delta^2(\tau^2+x^2))/4\pi}
\end{align}$$

for \\(\Lambda^2(\tau^2+x^2)\gg 1\\), \\(\Lambda\\) is the cutoff. So

$$$$\begin{align}\left<e^{i\beta\phi_R(\tau,x)} e^{-i\beta\phi(\tau,x)}\right> = \left(\frac{1}{\Lambda(\tau-ix)}\right)^{\beta^2/4\pi}\end{align}$$$$

we had \\(\beta = \sqrt{4\pi}\\), so it simplifies. This is the correct answer, and becomes

$$$$\begin{align}\frac{1}{i\Lambda(t-x)}\end{align}$$$$

Therefore, the correlation function is given by 


