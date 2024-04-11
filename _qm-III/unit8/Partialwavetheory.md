---
layout: lesson
title: Partial wave theory 
dept: physics
course: qm-III
unit: unit8
deptDisplay: Physics
courseDisplay: Quantum Mechanics III
unitDisplay: Unit 8
---
Partial wave theory is concerned with decomposing the scattering wave functions into different angular momentum modes. For a spherically symmetric potential, the different angular momentum modes will all scatter independently, so we can look at each one separately. For a spherically symmetric potential, we start by rewriting the Schrödinger equation as a 1 dimensional problem with an effective potential \\(V_\text{eff}\\). The Schrödinger equation for this situation is given by 

$$\begin{equation}
-\frac{\hbar^2}{2m}\nabla^2 \psi + V(\x)\psi = E\psi
\end{equation}$$

We assume that \\(V(\x) = V(r)\\) is spherically symmetric. Then, writing the Laplacian as 

$$\begin{equation}
\nabla^2 = \frac{1}{r^2}\frac{\partial}{\partial r}\left(r^2\frac{\partial}{\partial r}\right) + \frac{1}{r^2\sin\theta} \frac{\partial}{\partial\theta}\left(\sin\theta\frac{\partial}{\partial\theta}\right) + \frac{1}{r^2\sin^2\theta} \frac{\partial^2}{\partial \varphi^2}
\end{equation}$$

We note that this can be related to the angular momentum operator because 

$$\begin{equation}
\mathbf{L}^2 = -\hbar^2\left(\frac{1}{\sin\theta}\frac{\partial}{\partial\theta}\left(\sin\theta\frac{\partial}{\partial\theta}\right) + \frac{1}{\sin^2\theta}\frac{\partial^2}{\partial\varphi^2}\right)
\end{equation}$$

so that the Laplacian is 

$$\begin{equation}
\nabla^2 = \frac{1}{r^2}\frac{\partial}{\partial r}\left(r^2\frac{\partial}{\partial r}\right) - \frac{1}{\hbar^2r^2}\mathbf{L}^2
\end{equation}$$

Then we can rewrite the Schrödinger equation as 

$$\begin{equation}
-\frac{\hbar^2}{2mr^2}\frac{\partial}{\partial r}\left(r^2\frac{\partial}{\partial r}\right)\psi + \frac{1}{2mr^2}\mathbf{L}^2\psi + V(r)\psi = E\psi
\end{equation}$$

Now, let us separate variables by setting \\(\psi(r,\theta,\varphi) = R(r)Y^m_\ell(\theta,\varphi)\\). Doing this, we get 

$$\begin{align}
-\frac{\hbar^2}{2mr^2}\frac{\partial}{\partial r}\left(r^2\frac{\partial R}{\partial r}\right)Y^m_\ell + \frac{R}{2mr^2}\mathbf{L}^2Y^m_\ell + V(r)RY^m_\ell ={}& ERY^m_\ell \\
-\frac{\hbar^2}{2mr^2}\frac{\partial}{\partial r}\left(r^2\frac{\partial R}{\partial r}\right)Y^m_\ell + \frac{R\hbar^2\ell(\ell+1)}{2mr^2}Y^m_\ell + V(r)RY^m_\ell ={}& ERY^m_\ell 
\end{align}$$

Now, we can divide both sides by \\(Y^m_\ell\\), to get 

$$\begin{align}
-\frac{\hbar^2}{2mr^2}\frac{\partial}{\partial r}\left(r^2\frac{\partial R}{\partial r}\right) + \left[\frac{\hbar^2\ell(\ell+1)}{2mr^2} + V(r)\right]R ={}& ER
\end{align}$$

This allows us to define the effective potential

$$\begin{equation}
V_\text{eff}(r) = \frac{\hbar^2\ell(\ell+1)}{2mr^2} + V(r)
\end{equation}$$

$$\begin{align}
-\frac{\hbar^2}{2mr^2}\frac{\partial}{\partial r}\left(r^2\frac{\partial R}{\partial r}\right) + V_\text{eff}(r)R ={}& ER
\end{align}$$

Now, to simplify the equation, we set \\(R(r) = \frac{1}{r}u(r)\\), which gives us 

$$\begin{align}
r^2\frac{\partial R}{\partial r} ={}& r^2\left(-\frac{1}{r^2}u + \frac{1}{r}\frac{\partial u}{\partial r}\right) \\
={}& -u + r\frac{\partial u}{\partial r}
\end{align}$$

and taking one further derivative, we find 

$$\begin{align}
\frac{\partial}{\partial r}\left(r^2\frac{\partial R}{\partial r}\right) ={}& \frac{\partial}{\partial r}\left(-u + r\frac{\partial u}{\partial r}\right)\\
={}& -\frac{\partial u}{\partial r} + \frac{\partial u}{\partial r} + r\frac{\partial^2 u}{\partial r^2}\\
={}& r\frac{\partial^2 u}{\partial r^2}
\end{align}$$

Thus, we find that 

$$\begin{align}
-\frac{\hbar^2}{2mr}\frac{\partial^2 u}{\partial r^2} + V_\text{eff}(r)\frac{u}{r} ={}& E\frac{u}{r} \\
-\frac{\hbar^2}{2m}\frac{\partial^2 u}{\partial r^2} + V_\text{eff}(r) u ={}& E u
\end{align}$$

We rearrange one more time to get 

$$\begin{align}
\frac{\partial^2 u}{\partial r^2} + \left(\frac{2m E}{\hbar^2} - \frac{2m V_\text{eff}(r)}{\hbar^2} \right)u ={}& 0
\end{align}$$

and then we let \\(k^2 = 2mE/\hbar^2\\), and label our eigenfunctions by \\(u_{k\ell}\\)

$$\begin{align}
\frac{\partial^2 u_{k\ell}}{\partial r^2} + \left(k^2 - \frac{2m V_\text{eff}(r)}{\hbar^2} \right)u_{k\ell} ={}& 0
\end{align}$$

Now, in the limit \\(r\to\infty\\), we will find a simplified Schrödinger equation and solve for \\(u\\) in this limit. This will give us the scattering wave function. Now, let us take the limit \\(r\to\infty\\), which gives us \\(V_\text{eff}(r) \to 0\\). Then, we solve for the approximate solution \\(\tilde{u}\\) to get 

$$\begin{align}
\frac{\partial^2 \tilde{u}_{k\ell}}{\partial r^2} + k^2\tilde{u}_{k\ell} ={}& 0
\end{align}$$

The solution to this is 

$$\begin{equation}
\tilde{u}_{k\ell} = Ae^{ikr} + Be^{-ikr}
\end{equation}$$


Now, keeping \\(r\\) dependence of the centrifugal term but removing the \\(V(r)\\) term, let's compute the wave function in the intermediate region. If we return to the original representation (\\(R\\) equation instead of \\(u\\) equation), then the equation is 

$$\begin{equation}
-\frac{\hbar^2}{2mr^2}\frac{\partial}{\partial r}\left(r^2\frac{\partial R}{\partial r}\right) + \frac{\hbar^2\ell(\ell+1)}{2mr^2}R = ER
\end{equation}$$

Then, expanding this out and defining \\(k^2 = 2mE/\hbar^2\\), we have that 

$$\begin{equation}
-\frac{1}{r^2}\frac{\partial}{\partial r}\left(r^2\frac{\partial R}{\partial r}\right) + \frac{\ell(\ell+1)}{r^2}R = k^2R
\end{equation}$$

Rearranging, we get 

$$\begin{equation}
r^2R" + 2rR' + (k^2r^2 - \ell(\ell+1))R = 0
\end{equation}$$

The solution to this is simply \\(R = j_\ell(kr)\\) and \\(y_\ell(kr)\\). These are the spherical Bessel functions of the first and second kind, respectively. The spherical bessel function of the second kind is sometimes called a Neumann function. These functions can somewhat be intuited by looking at their asymptotic forms: 

$$\begin{equation}
j_\ell(kr) \sim \frac{1}{kr}\sin\left(kr - \frac{\ell\pi}{2}\right),\qquad y_\ell(kr) = -\frac{1}{kr}\cos\left(kr - \frac{\ell\pi}{2}\right)
\end{equation}$$

Thus, it makes sense to define the <i>Hankel functions</i>, which define incoming and outgoing waves by \\(h^{(1)}_\ell(kr) = j_\ell(kr) + iy_\ell(kr)\\). These are analogous to writing \\(e^{ikr} = \cos(kr) + i\sin(kr)\\), which works because the sine and cosine are each superpositions of incoming and outgoing waves, so we can recover only the outgoing component. Then, we can write the radial solution in terms of incoming and outoging waves. We pick only the outgoing ones, and therefore get \\(R(kr) = h^{(1)}_\ell(kr)\\). The outgoing wave function is then given by 

$$\begin{equation}
\psi = \sum_{\ell,m} c_{\ell,m} h^{(1)}_\ell(kr) Y^m_\ell(\theta,\varphi)
\end{equation}$$

We note that, because the scattering is symmetric about the \\(z\\) axis, that it should be independent of \\(\varphi\\). Then, we can assume that \\(m=0\\). If we assume this, then

$$\begin{equation}
Y^0_\ell(\theta,\varphi) = \sqrt{\frac{2\ell+1}{4\pi}} P_\ell(\cos\theta)
\end{equation}$$

and plugging this in, we define \\(c_{\ell,0} = i^{\ell+1}k\sqrt{4\pi(2\ell+1)}a_\ell\\). Then, the outgoing wave function is given by 

$$\begin{equation}
\psi = k\sum_{\ell=0}^\infty i^{\ell+1}(2\ell+1)a_\ell h^{(1)}_\ell(kr) P_\ell(\cos\theta)
\end{equation}$$

The total wave function is then given by 

$$\begin{equation}
\psi = A\left(e^{ikz} + k\sum_{\ell=0}^\infty i^{\ell+1}(2\ell+1)a_\ell h^{(1)}_\ell(kr) P_\ell(\cos\theta)\right)
\end{equation}$$

Note that the Hankel function has the asymptotic form 

$$\begin{equation}
h^{(1)}_\ell(kr) \sim (-i)^{\ell+1}\frac{e^{ikr}}{r},\qquad kr\gg 1
\end{equation}$$

which gives the outgoing wave to be 

$$\begin{equation}
\psi = f(\theta) \frac{e^{ikr}}{r}, \qquad f(\theta) = \sum_{\ell=0}^\infty a_\ell (2\ell+1)P_\ell(\cos\theta)
\end{equation}$$

Thus, the total ingoing and outgoing wave function in the radiation zone is 

$$\begin{equation}
\psi = A\left(e^{ikz} + f(\theta)\frac{e^{ikr}}{r}\right)
\end{equation}$$

Now, returning to the full wave function, we note that we have done things in terms of plane waves and also spherical waves. Then, we can use Rayleigh's formula which we proved last week:

$$\begin{equation}
e^{ikz} = \sum_{\ell=0}^\infty i^\ell (2\ell+1)j_\ell(kr) P_\ell(\cos\theta)
\end{equation}$$

and thus find the wave function to be 

$$\begin{equation}
\psi = A\sum_{\ell=0}^\infty i^\ell(2\ell+1)\left[j_\ell(kr) + ika_\ell h^{(1)}_\ell(kr)\right]P_\ell(\cos\theta)
\end{equation}$$

The coefficient \\(a_\ell\\) is called a partial wave amplitude. 

<div class="example">
<b>Example:</b>
Compute the partial wave amplitudes for the potential 

$$\begin{equation}
V(r) = \begin{cases}
\infty & r \leq a \\
0 & r > a
\end{cases}
\end{equation}$$

<b>Solution:</b> The boundary condition for this is \(\psi(a,\theta)\). Thus, if we take the wave function

$$\begin{equation}
\psi(a,\theta) = \sum_{\ell=0}^\infty i^\ell(2\ell+1)\left[j_\ell(ka) + ika_\ell h^{(1)}_\ell(ka)\right] P_\ell(\cos\theta) = 0
\end{equation}$$

Since this should hold for all \(\ell\), we have that 

$$\begin{equation}
j_\ell(ka) + ika_\ell h^{(1)}_\ell(ka) = 0 \rightarrow a_\ell = \frac{ij_\ell(ja)}{kh^{(1)}_\ell(ka)}
\end{equation}$$

The scattering cross section is given by the following (this was derived in class). A quick reminder is the following. We have \(\d N = I\d\sigma\). Since 

$$\begin{equation}
I = \frac{\#\text{particles}}{\text{unit area} \times \text{unit time}}
\end{equation}$$

and we have that \([\mathbf{J}] = 1/\text{m}^2\text{s}\) (particles per unit area per second), we have that simply \(I = \mathbf{J}_\text{inc}\cdot\zhat\). We also have that the number of particles passing through an outgoing area is given by 

$$\begin{equation}
\d N = \frac{\#\text{particles}}{\text{unit time}}
\end{equation}$$

Thus to get this, we need to take the outgoing probability current and multiply by the area that it is going through to get 

$$\begin{equation}
\d N = \mathbf{J}_\text{out}\cdot\hat{r} (r^2\d\Omega)
\end{equation}$$

Thus, computing each of these for \(\psi_\text{inc} = Ae^{ikz}\), and \(\psi_\text{out} = A\frac{e^{ikr}}{r}f(\theta)\), we have that \(I = \frac{\hbar}{m}\|A\|^2 k\zhat\), and also 

$$\begin{equation}
\mathbf{J}_\text{out} = \frac{\hbar\|A\|^2}{m}\frac{\|f(\theta)\|^2}{r^2} \nabla(kr) = \frac{\hbar\|A\|^2}{m}\frac{\|f(\theta)\|^2}{r^2}\hat{r} k
\end{equation}$$

which gives us 

$$\begin{equation}
\d N = \frac{\hbar}{m}\|A\|^2\|f(\theta)\|^2k\d\Omega
\end{equation}$$

and combining these two to get 

$$\begin{equation}
\frac{\hbar\|A\|^2}{m}\|f(\theta)\|^2 k \d\Omega = \frac{\hbar}{m}\|A\|^2 k \d\sigma
\end{equation}$$

we find that the <i>differential scattering cross section</i> is

$$\begin{equation}
D(\theta) = \|f(\theta)\|^2 = \frac{\d\sigma}{\d\Omega}
\end{equation}$$

where 

$$\begin{equation}
f(\theta) = \sum_{\ell=0}^\infty (2\ell+1)a_\ell P_\ell(\cos\theta)
\end{equation}$$

so that 

$$\begin{align}
\sigma {}&= \int\sum_{\ell\ell'} (2\ell+1)(2\ell'+1)a_\ell a_{\ell'}^* P_\ell(\cos\theta) P_{\ell'}(\cos\theta) \d\Omega \\
={}& \int_0^\pi \int_0^{2\pi} \sum_{\ell\ell'} (2\ell+1)(2\ell'+1)a_\ell a_{\ell'}^* P_\ell(\cos\theta) P_{\ell'}(\cos\theta) \sin\theta\d\varphi\d\theta\\
={}& 2\pi \int_{-1}^1  \sum_{\ell\ell'} (2\ell+1)(2\ell'+1)a_\ell a_{\ell'}^* P_\ell(x) P_{\ell'}(x) x\d x
\end{align}$$

Using the orthogonality relation 

$$\begin{equation}
\int_{-1}^1 P_\ell(x) P_{\ell'}(x) \d x = \frac{2}{2\ell+1} \delta_{\ell\ell'}
\end{equation}$$

we find 

$$\begin{align}
\sigma ={}& 2\pi \int_{-1}^1  \sum_{\ell\ell'} (2\ell+1)(2\ell'+1)a_\ell a_{\ell'}^* \frac{2\delta_{\ell\ell'}}{2\ell+1} \\
={}& 4\pi \sum_{\ell} (2\ell+1)\|a_\ell\|^2 \\
={}& 4\pi \sum_{\ell=0}^\infty (2\ell+1)\left\|\frac{j_\ell(ka)}{kh^{(1)}_\ell(kr)}\right\|^2
\end{align}$$

To get some intuition for this, let's consider the limit \(ka \ll 1\) (the low energy limit) so that the series will converge quickly. This allows us to use the asymptotic forms 

$$\begin{equation}
j_\ell(z) \sim \frac{z^\ell 2^\ell \ell!}{(2\ell+1)(2\ell)!},\qquad y_\ell(z) \sim -\frac{(2\ell)!}{z^{\ell+1}2^\ell \ell!},\qquad z\to 0
\end{equation}$$

which means that 

$$\begin{align}
\sigma ={}& \frac{4\pi}{k^2} \sum_{\ell=0}^\infty (2\ell+1)\left\|\frac{j_\ell(ka)}{j_\ell(ka) + iy_\ell(ka)}\right\|^2 \\
={}& \frac{4\pi}{k^2} \sum_{\ell=0}^\infty (2\ell+1)\left\|\frac{j_\ell(ka)}{y_\ell(ka)}\right\|^2 \\
={}& \frac{4\pi}{k^2} \sum_{\ell=0}^\infty (2\ell+1)\left\|\frac{z^{2\ell+1}(\ell!)^2 2^{2\ell}}{(2\ell+1)(2\ell)!^2}\right\|^2 \\
={}& \frac{4\pi}{k^2} \sum_{\ell=0}^\infty \frac{(ka)^{4\ell+2}}{2\ell+1} \left(\frac{\ell! 2^\ell}{(2\ell)!}\right)^4 \\
={}& 4\pi a^2
\end{align}$$

which is 4 times the classical cross section of a sphere of radius \(a\). 


</div>


<ol>
<li> <div class="exercise">  Define the three-dimensional probability current by

$$\begin{equation}
<b>J</b> = \frac{i\hbar}{2m}(\Psi\nabla\Psi^* - \Psi^*\nabla\Psi)
\end{equation}$$

<ol type="a">
<li> Show that \(<b>J</b>\) satisfies the continuity equation

$$\begin{equation}
\nabla\cdot<b>J</b> = -\frac{\partial}{\partial t}\|\Psi\|^2
\end{equation}$$

which expresses local conservation of probability. It follows that 

$$\begin{equation}
\oint_{\partial \V} <b>J</b>\cdot\d<b>A</b> = -\frac{\d}{\d t}\int_{\V} \|\Psi\|^2 \d^3\x
\end{equation}$$

where \(\V\) is a (fixed) volume and \(\partial \V\) is its boundary surface. In words: the flow of probability out through the surface is equal to the decrease in probability of finding the particle in the volume. 

</li>
<li> Find \(<b>J</b>\) for hydrogen in the state \(n=2\), \(\ell = 1\), \(m = 1\). 

</li>
<li> If we interpret \(m<b>J</b>\) as the flow of mass, the angular momentum is 

$$\begin{equation}
<b>L</b> = m\int (\r\times<b>J</b>)\d^3\x
\end{equation}$$
</li></ol>

<div class="answerBox"> 
 <button onclick="myFunction('answer326')" class="answerButton">Show Answer</button> 
 <div  id='answer326' class="answer" >
<ol type="a">
<li> The divergence of \(<b>J</b>\) is 

$$\begin{equation}
\nabla\cdot<b>J</b> = \frac{i\hbar}{2m}(\Psi\nabla^2\Psi^* - \Psi^*\nabla^2\Psi)
\end{equation}$$

The time derivative of \(\|\Psi\|^2\) is 

$$\begin{align}
\frac{\partial}{\partial t}\|\Psi\|^2 =& \left(\frac{\partial}{\partial t}\Psi\right)\Psi^* + \Psi\frac{\partial}{\partial t}\Psi^* \\
=& \frac{1}{i\hbar}\left(-\frac{\hbar^2\nabla^2\Psi}{2m} + V\Psi\right)\Psi^* + \Psi\frac{1}{-i\hbar}\left(-\frac{\hbar^2\nabla^2\Psi^*}{2m} + V\Psi^*\right) \\
=& \frac{i\hbar}{2m} (\nabla^2\Psi)\Psi^* - \frac{i\hbar}{2m}   \Psi(\nabla^2\Psi^*) \\
=& \frac{i\hbar}{2m}((\nabla^2\Psi)\Psi^* - \Psi(\nabla^2\Psi))
\end{align}$$

Clearly, this is the negative of \(\nabla\cdot<b>J</b>\). 

</li>
<li> Let us find the probability current for the state

$$\begin{equation}
\psi_{211}(\x,t) = -\frac{r\sin\theta}{8\sqrt{\pi a^5}}e^{-r/2a}e^{i\varphi}e^{-iE_2t/\hbar}
\end{equation}$$

We need the following formula for the gradient in spherical coordinates:

$$\begin{equation}
\nabla = \ehat_r \frac{\partial}{\partial r} + \ehat_\theta \frac{1}{r} \frac{\partial}{\partial \theta} + \ehat_\varphi \frac{1}{r\sin\theta} \frac{\partial}{\partial \varphi}
\end{equation}$$

Then, we take the derivative:

$$\begin{align}
\nabla\psi_{211} =& -\frac{e^{-iE_2t/\hbar}}{8\sqrt{\pi a^5}}\left[\left(e^{-2r/a} - \frac{r}{2a}e^{-2r/a}\right)\sin\theta e^{-i\varphi} \ehat_r + \frac{\cos\theta r}{r} e^{-r/2a} e^{-i\varphi} \ehat_\theta - \frac{ire^{-r/2a}\sin\theta}{r\sin\theta} e^{-i\varphi} \ehat_\varphi\right] \\
=& -\frac{e^{-iE_2t/\hbar}}{8\sqrt{\pi a^5}}\left[\left(1 - \frac{r}{2a}\right)\sin\theta \ehat_r + \cos\theta \ehat_\theta - i\ehat_\varphi\right] e^{-r/2a}e^{-i\varphi} \\
\end{align}$$

Thus, the quantities 

$$\begin{align}
\psi_{211}\nabla\psi_{211}^* =& -\frac{1}{64\pi a^5}\left[\left(1- \frac{r}{2a}\right)\sin\theta \ehat_r + \cos\theta \ehat_\theta - i\ehat_\varphi\right]\left(-r\sin\theta e^{-r/a}\right) \\
=& \frac{1}{64\pi a^5}\left[\left(1- \frac{r}{2a}\right)\sin\theta \ehat_r + \cos\theta \ehat_\theta - i\ehat_\varphi\right]r\sin\theta e^{-r/a}
\end{align}$$

Computing the difference \(\psi_{211}\nabla\psi^*_{211} - (\nabla\psi_{211})\psi^*_{211}\) removes the real part, and we get 

$$\begin{align}
\psi_{211}\nabla\psi^*_{211} - (\nabla\psi_{211})\psi^*_{211} =& \frac{1}{64\pi a^5}\left[ - 2i \ehat_\varphi\right]r\sin\theta e^{-r/a} \\
=& \frac{-i}{32\pi a^5}r\sin\theta e^{-r/a} \ehat_\varphi 
\end{align}$$

Finally, we find 

$$\begin{equation}
<b>J</b> = \frac{\hbar}{64m\pi a^5}r\sin\theta e^{-r/a} \ehat_\varphi
\end{equation}$$

We interpret this as a current going around the \(z\) axis, which makes since \(L_z = \hbar\) for this state. 

</li>
<li> The angular momentum is then found by computing 

$$\begin{equation}
<b>L</b> = m\int(<b>r</b>\times<b>J</b>)\d^3\x
\end{equation}$$

The position vector is \(<b>r</b> = r\ehat_r\), so computing \(\ehat_r\times\ehat_\varphi = -\ehat_\theta\), so we find (using \(\ehat_\theta = \cos\theta\cos\varphi\ehat_x + \cos\theta\sin\varphi\ehat_y -\sin\theta \ehat_z\))

$$\begin{align}
<b>L</b> =& -m\int \frac{\hbar}{64m\pi a^5}r^2\sin\theta e^{-r/a} \ehat_\theta \d^3\x \\
=& \frac{\hbar m}{64m\pi a^5}\int r^2\sin\theta e^{-r/a} \sin\theta \ehat_z \d^3\x \\
=& \frac{\hbar m}{64m\pi a^5} \int_0^\infty \int_0^\pi \int_0^{2\pi} r^2\sin\theta e^{-r/a} \sin\theta r^2\sin\theta \d\varphi \d\theta \d r \ehat_z\\
=& \frac{\hbar m}{64m\pi a^5} 2\pi \int_0^\infty r^4e^{-r/a} \d r \int_0^\pi \sin^3\theta \d\theta \ehat_z\\
=& \frac{\hbar m}{64m\pi a^5} 2\pi a^5 4! \frac{4}{3} \ehat_z\\
=& \hbar \ehat_z
\end{align}$$

This makes perfect sense! 

</li></ol>
</div> 
 </div>

</div> </li>
<li> <div class="exercise">  We will often have an incoming particle. In quantum mechanics, an incoming particle is written as a plane wave. When the wave scatters off of some potential (big black dot), then we need to consider the different scattered components in terms of spherical waves. It is very inconvenient to describe the incoming wave in terms of a plane wave, but the outgoing wave in terms of a spherical wave. Thus, we need to <i>express the incoming plane wave in terms of spherical waves</i>. 

<figure class="center">
<p><img src="figures/incoming_plane_wave.pdf" alt="Function" class="center" style="width:151.42px;height:113.784px;"> </p><p><img src="figures/outgoing_spherical_wave.pdf" alt="Function" class="center" style="width:142.43px;height:114.382px;"> </p></figure>


Remark: First, what is a <i>spherical wave</i>? Well, we remind ourselves that a <i>plane wave</i> is a solution of the wave equation in Cartesian coordinates. A spherical wave is a solution of the wave equation in spherical coordinates. However, we know that these equations are actually the same, and the only difference is the coordinate system used to represent the solutions. Therefore, there should be a way to convert between the two. That is what we will discuss in this problem. Let us first review a couple things. We recall that:


We need to review the spherical harmonics first. 

<ul>
<li> The spherical harmonics are defined by 

$$\begin{equation}
Y^m_\ell(\theta,\varphi) = Ne^{im\varphi} P^m_\ell(\cos\theta)
\end{equation}$$

where \(N\) is a normalization constant and \(P^m_\ell\) are the associated Legendre polynomials. These polynomials are defined by 

$$\begin{equation}
P^m_\ell(u) = (-1)^m(1-u^2)^{m/2}\frac{\d^m}{\d u^m}P_\ell(u)
\end{equation}$$

where \(P_\ell(u)\) are the ordinary Legendre polynomials. However, if we are looking for azimuthally symmetric solutions (which we are), then there should be no \(\varphi\) dependence. Thus, \(m = 0\). Thus, we do not need to worry about the associated Legendre polynomials, and we will only consider the ordinary ones. Now let us remind ourselves about the ordinary Legendre polynomials.

</li>
<li> The Legendre polynomials are a system of complete and orthogonal polynomials on the interval \(x\in [-1,1]\). They are defined by

$$\begin{equation}
P_\ell(x) = \frac{1}{2^\ell \ell!} \frac{\d^\ell}{\d x^\ell}(x^2-1)^\ell
\end{equation}$$

They satisfy the following: 

$$\begin{equation}
\int_{-1}^1 P_m(x) P_n(x) \d x = \frac{2}{2n+1}\delta_{mn}
\end{equation}$$

Any (sufficiently nice) function \(f(x)\) can be expanded as 

$$\begin{equation}
f(x) = \sum_{\ell=0}^\infty a_\ell P_\ell(x),\qquad a_\ell = \frac{2\ell+1}{2}\int_{-1}^1 f(x) P_\ell(x) \d x
\end{equation}$$

Note: to find the coefficients \(a_\ell\), multiply the first equation by \(P_m(x)\) on both sides and then integrate, using the orthogonality relation.
</li>
<li> So far, we have just reviewed the angular solutions in spherical coordinates. What about the radial solutions? Well, in 3D, the radial solutions are related to something called ``spherical Bessel functions". The spherical Bessel functions are defined by 

$$\begin{equation}
j_\ell(x) = (-1)^\ell x^\ell \left(\frac{1}{x}\frac{\d}{\d x}\right)^\ell \frac{\sin x}{x}
\end{equation}$$

so the first few spherical Bessel functions are given by 

$$\begin{align}
j_0(x) ={}& \frac{\sin x}{x} \\
j_1(x) ={}& \frac{\sin x}{x^2} - \frac{\cos x}{x} \\
j_2(x) ={}& \left(\frac{3}{x^3} - \frac{1}{x}\right)\sin x - \frac{3}{x^2}\cos x
\end{align}$$

If we want to motivate where these come from, let us also recall that the spherical Bessel functions come from the wave equation (which includes the Laplacian) in 3 dimensions. We recall that the wave equation is 

$$\begin{equation}
\frac{\partial^2 \psi}{\partial t^2} = c^2 \nabla^2 \psi
\end{equation}$$

Then, the 

$$\begin{equation}
\nabla^2 \Psi = \left[\frac{1}{r^2}\frac{\partial}{\partial r}\left(r^2\frac{\partial}{\partial r}\right) + \frac{1}{r^2\sin\theta}\frac{\partial}{\partial\theta}\left(\sin\theta\frac{\partial}{\partial\theta}\right) + \frac{1}{r^2\sin^2\theta}\frac{\partial}{\partial\varphi^2}\right]\Psi
\end{equation}$$

To analyze the radial part of this, write that assume that \(\Psi = \psi(r,t)Y^m_\ell(\theta,\varphi)\), and then we have that 

$$\begin{equation}
Y^m_\ell\frac{\partial^2 \psi}{\partial t^2} = c^2\left[\frac{1}{r^2}\frac{\partial}{\partial r}\left(r^2\frac{\partial}{\partial r}\right) \psi - \frac{1}{r^2}\ell(\ell+1)\psi\right]Y^m_\ell
\end{equation}$$

Then letting \(\psi = R(r)T(t)\), we would have 

$$\begin{equation}
\frac{T"}{T} = \frac{c^2}{r^2R}\frac{\partial}{\partial r}\left(r^2\frac{\partial R}{\partial r}\right) - \frac{\ell(\ell+1)}{r^2} = -\omega^2 = -c^2k^2
\end{equation}$$

Then, this gives us 

$$\begin{equation}
\frac{1}{r^2R}\frac{\partial}{\partial r}\left(r^2\frac{\partial R}{\partial r}\right) - \frac{\ell(\ell+1)}{r^2} = -k^2
\end{equation}$$

Then letting \(\alpha = kr\), this changes to 

$$\begin{equation}
\frac{1}{\alpha^2 R}\frac{\partial}{\partial \alpha }\left(\alpha^2\frac{\partial R}{\partial \alpha}\right) - \frac{\ell(\ell+1)}{\alpha^2} = -1
\end{equation}$$

We can rearrange this to 

$$\begin{equation}
\alpha^2 \frac{\partial^2 R}{\partial\alpha^2} + 2\alpha\frac{\partial R}{\partial \alpha} + (\alpha^2 - \ell(\ell+1))R= 0
\end{equation}$$

This is the spherical Bessel function, with \(R = j_\ell(\alpha) = j_\ell(kr)\). Now that we know where the spherical Bessel functions came from, and we have some motivation for us to express the plane waves in terms of these radially symmetric functions.

</li></ul>

</div> </li>
<li> <div class="exercise">  Prove that 

$$\begin{equation}
e^{ikz} = \sum_{\ell=0}^\infty i^\ell (2\ell+1)j_\ell(kr) P_\ell(\cos\theta)
\end{equation}$$

<div class="answerBox"> 
 <button onclick="myFunction('answer546')" class="answerButton">Show Answer</button> 
 <div  id='answer546' class="answer" >
In order to prove this, we have a function \(e^{ikz} = e^{ikr\cos\theta}\). Defining \(u = \cos\theta\), we want to use the above result to find the coefficients \(a_\ell\) in 

$$\begin{equation}
e^{ikru} = \sum_{\ell=0}^\infty a_\ell(kr)P_\ell(u)
\end{equation}$$
 
To find the coefficients, we compute 

$$\begin{equation}
a_\ell(kr) = \frac{2\ell+1}{2}\int_{-1}^1 e^{ikru}P_\ell(u) \d u
\end{equation}$$

Now, plugging in the form of \(P_\ell(u)\), we get 

$$\begin{align}
a_\ell(kr) ={}& \frac{2\ell+1}{2}\int_{-1}^1 e^{ikru} \frac{1}{2^\ell \ell!}\frac{\d^\ell}{\d u^\ell}(u^2-1)^\ell \d u \\
={}& \frac{2\ell+1}{2^{\ell+1}\ell!}\int_{-1}^1 e^{ikru}\frac{\d^\ell}{\d u^\ell}(u^2-1)^\ell \d u
\end{align}$$

We need to integrate by parts \(\ell\) times. If we do this, then we get 

$$\begin{align}
a_\ell(kr) ={}& \frac{2\ell+1}{2^{\ell+1}\ell!}\int_{-1}^1 (-1)^\ell \frac{\d^\ell}{\d u^\ell}(e^{ikru}) (u^2-1)^\ell \d u \\
={}& \frac{2\ell+1}{2^{\ell+1}\ell!} (-ikr)^\ell \int_{-1}^1 e^{ikru} (u^2-1)^\ell \d u
\end{align}$$

If we define \(\alpha = kr\), then we want to find the relationship between this integral and the spherical Bessel function

$$\begin{align}
\int_{-1}^1 e^{i\alpha u} (u^2-1)^n \d u
\end{align}$$

Well, let's calculate 

$$\begin{align}
\frac{1}{\alpha}\frac{\partial}{\partial\alpha}\int_{-1}^1 e^{i\alpha u} \d u ={}& \frac{1}{\alpha}\int_{-1}^1 e^{i\alpha u} iu \d u \\
={}& \frac{1}{2\alpha}\int_{-1}^1 e^{i\alpha u} i (u^2-1)'\d u \\
={}& \frac{i}{2\alpha}e^{i\alpha u}(u^2-1)\bigg|_{-1}^1 - \frac{i}{2\alpha} \int_{-1}^1 i\alpha e^{i\alpha u}(u^2-1)\d u \\
={}& \frac{1}{2} \int_{-1}^1 e^{i\alpha u}(u^2-1)\d u
\end{align}$$

If we generalize this, then we can find that 

$$\begin{align}
\frac{1}{\alpha}\frac{\partial}{\partial\alpha} \int_{-1}^1 e^{i\alpha u} (u^2-1)^n \d u ={}& \frac{1}{\alpha} \int_{-1}^1 iu e^{i\alpha u} (u^2-1)^n \d u \\
={}& \frac{1}{2\alpha(n+1)} \int_{-1}^1 ie^{i\alpha u} [(u^2-1)^{n+1}]' \d u \\
={}& \frac{i}{2\alpha(n+1)} e^{i\alpha u}(u^2-1)^{n+1}\bigg|_{-1}^1 - \frac{i}{2\alpha(n+1)}\int_{-1}^1 i\alpha e^{i\alpha u}(u^2-1)^{n+1} \d u \\
={}& \frac{1}{2(n+1)}\int_{-1}^1 e^{i\alpha u}(u^2-1)^{n+1} \d u 
\end{align}$$

We see now that we pick up a factor of \(1/2\) and \(1/(n+1)\) when we differentiate (and also divide by \(\alpha\)) \(\int_{-1}^1 e^{i\alpha u} (u^2-1)^n \d u\). Thus, if we want to differentiate (and divide by \(\alpha\))

\(\)\int_{-1}^1 e^{i\alpha u} \d u\(\)

\(\ell\) times, then we get 

$$\begin{equation}
\left(\frac{1}{\alpha}\frac{\partial}{\partial\alpha}\right)^\ell \int_{-1}^1 e^{i\alpha u} \d u = \frac{1}{2^\ell\ell!} \int_{-1}^1 e^{i\alpha u}(u^2-1)^\ell \d u
\end{equation}$$

Thus, we can use 

$$\begin{align}
a_\ell(kr) ={}& \frac{2\ell+1}{2^{\ell+1}\ell!} (-ikr)^\ell \int_{-1}^1 e^{ikru} (u^2-1)^\ell \d u \\
={}& \frac{2\ell+1}{2}(-i\alpha)^\ell \left(\frac{1}{\alpha}\frac{\partial}{\partial\alpha}\right)^\ell \int_{-1}^1 e^{i\alpha u} \d u \\
={}& \frac{2\ell+1}{2}(-i\alpha)^\ell \left(\frac{1}{\alpha}\frac{\partial}{\partial\alpha}\right)^\ell \frac{1}{i\alpha}e^{i\alpha u}\bigg|_{-1}^1 \\
={}& \frac{2\ell+1}{2}(-i\alpha)^\ell \left(\frac{1}{\alpha}\frac{\partial}{\partial\alpha}\right)^\ell \frac{1}{i\alpha}(e^{i\alpha} - e^{-i\alpha}) \\
={}& (2\ell+1)(-i\alpha)^\ell \left(\frac{1}{\alpha}\frac{\partial}{\partial\alpha}\right)^\ell \frac{\sin\alpha}{\alpha}\\
={}& (2\ell+1)i^\ell j_\ell(\alpha)
\end{align}$$

Finally plugging back in \(\alpha = kr\), we get 

$$\begin{align}
a_\ell(kr) ={}& (2\ell+1)i^\ell j_\ell(kr)
\end{align}$$

Thus, we find that 

$$\begin{align}
e^{ikru} ={}& \sum_{\ell=0}^\infty a_\ell(kr)P_\ell(u) \\
={}& \sum_{\ell=0}^\infty (2\ell+1)i^\ell j_\ell(\alpha)P_\ell(u) 
\end{align}$$

and finally substituting back in \(u = \cos\theta\), we get 

$$\begin{align}
e^{ikz} = e^{ikr\cos\theta} ={}& \sum_{\ell=0}^\infty (2\ell+1)i^\ell j_\ell(\alpha)P_\ell(\cos\theta) 
\end{align}$$

</div> 
 </div>

</div> </li></ol>


\subsection{Partial Wave phase shifts} %ready

In this tutorial, we will develop a couple of technical results that will be useful in the development of partial wave theory. The partial wave expansion applies when we are in the intermediate region where we can approximate the potential as \\(V \approx 0\\), and we then want to connect the solution to the scattering region where the potential is nonzero. This is done by matching boundary conditions. 



Let us recall the wave function from the previous section on partial waves, which consists of the incoming and outgoing waves:

$$\begin{equation}
\psi = A\sum_{\ell=0}^\infty i^\ell(2\ell+1)(j_\ell(kr) + ika_\ell h^{(1)}_\ell(kr)) P_\ell(\cos\theta)
\end{equation}$$

Since each angular momentum \\(\ell\\) scatters independently, the amplitude of  each must be conserved, by conservation of probability. Let's show that, if we have a wave function written as 

$$\begin{equation}
\psi = A\sum_{\ell=0}^\infty i^\ell (2\ell+1)(b_\ell h^{(1)}_\ell(kr) + c_\ell h^{(2)}_\ell(kr))P_\ell(\cos\theta),
\end{equation}$$

that we require \\(\|b_\ell\|^2 = \|c_\ell\|^2\\). This is the conservation of probability for an incoming wave function component of angular momentum \\(\ell\\) scattering into an outgoing wave function component of angular momentum \\(\ell\\) must conserve the amplitude since each component scatters independently (no mixing between different \\(\ell\\)). 

The continuity equation is 

$$\begin{equation}
\frac{\partial}{\partial t}\|\psi\|^2 + \nabla\cdot\mathbf{J} = 0
\end{equation}$$

The time-dependent version of the above wave function is 

$$\begin{equation}
\psi(r,\theta,t) = \sum_{\ell=0}^\infty i^\ell (2\ell+1)(b_\ell h^{(1)}_\ell(kr) + c_\ell h^{(2)}_\ell(kr)) P_\ell(\cos\theta) e^{-iE_kt/\hbar}
\end{equation}$$

because all of the states with the same \\(k\\) are degenerate. Thus, \\(\rho = \|\psi\|^2\\) is time independent so \\(\partial_t\rho = 0\\). For the probability current part, we have then that 

$$\begin{equation}
\int \nabla\cdot\mathbf{J} = 0 = \oint \mathbf{J}\cdot \d\mathbf{A}
\end{equation}$$

Thus, let us calculate the above integral. 

$$\begin{align}
\oint \mathbf{J}\cdot \d\mathbf{A} ={}& \frac{i\hbar}{2m}\int_0^\pi \int_0^{2\pi} (\psi \nabla\psi^* - \psi^*\nabla\psi) r^2 \hat{r} \sin\theta \d\varphi\d\theta \\
={}& \frac{2\pi i\hbar}{2m}\int_0^\pi (\psi \partial_r\psi^* - \text{c.c}) r^2 \sin\theta \d\theta
\end{align}$$

where c.c. means complex conjugate. Now, plugging in the wave function, we get 

$$\begin{align}
\oint \mathbf{J}\cdot \d\mathbf{A} ={}& \frac{\pi i\hbar}{m}\int_0^\pi \left[\sum_{\ell=0}^\infty \sum_{\ell'=0}^\infty i^\ell (2\ell+1) (b_\ell h^{(1)}_\ell(kr) + c_\ell h^{(2)}_\ell(kr))P_\ell(\cos\theta) \right.\\
&\times \left. (-i)^{\ell'} (2\ell'+1)(b_\ell^* \partial_r h^{(2)}_\ell(kr) + c_\ell^* \partial_r h^{(1)}_\ell(kr)) P_{\ell'}(\cos\theta) - \text{c.c}\right] r^2 \sin\theta \d\theta
\end{align}$$

If we then use the identity 

$$\begin{equation}
\int_0^\pi P_\ell(\cos\theta) P_{\ell'}(\cos\theta) \sin\theta \d\theta = \frac{2\delta_{\ell\ell'}}{2\ell+1}
\end{equation}$$

then we find 

$$\begin{align}
\oint \mathbf{J}\cdot \d\mathbf{A} ={}& \frac{\pi i\hbar }{m} \left[\sum_{\ell\ell'} \frac{2\delta_{\ell\ell'}r^2}{2\ell+1} i^\ell (2\ell+1) (b_\ell h^{(1)}_\ell(kr) + c_\ell h^{(2)}_\ell(kr)) (-i)^{\ell'} (2\ell'+1)(b_\ell^* \partial_r h^{(2)}_\ell(kr) + c_\ell^* \partial_r h^{(1)}_\ell(kr)) - \text{c.c}\right] \\
={}& \frac{2\pi i\hbar r^2}{m} \left[\sum_{\ell} (2\ell+1) (b_\ell h^{(1)}_\ell(kr) + c_\ell h^{(2)}_\ell(kr))(b_\ell^* \partial_r h^{(2)}_\ell(kr) + c_\ell^* \partial_r h^{(1)}_\ell(kr)) - \text{c.c}\right] \\
={}& \frac{2\pi i\hbar r^2}{m} \left[\sum_{\ell} (2\ell+1) (\|b_\ell\|^2 h^{(1)}_\ell(kr) \partial_r h^{(2)}_\ell(kr) + c_\ell b_\ell^* h^{(2)}_\ell(kr) \partial_r h^{(2)}_\ell(kr) \right. \\
&\left. + b_\ell c_\ell^* h^{(1)}_\ell(kr) \partial_r h^{(1)}_\ell(kr) + \|c_\ell\|^2 h^{(2)}_\ell(kr) \partial_r h^{(1)}_\ell(kr))- \text{c.c}\right] 
\end{align}$$

We see that \\(c_\ell b_\ell^* h^{(2)}_\ell \partial_r h^{(2)}_\ell(kr) + b_\ell c_\ell^* h^{(1)}_\ell(kr) \partial_r h^{(1)}_\ell(kr)\\) is real, so when we subtract off the complex conjugate we get zero. Thus, we find 

$$\begin{align}
\oint \mathbf{J}\cdot \d\mathbf{A} ={}& \frac{2\pi i\hbar r^2}{m} \left[\sum_{\ell} (2\ell+1) (\|b_\ell\|^2 h^{(1)}_\ell(kr) \partial_r h^{(2)}_\ell(kr) + \|c_\ell\|^2 h^{(2)}_\ell(kr) \partial_r h^{(1)}_\ell(kr))- \text{c.c}\right] \\
={}& \frac{2\pi i\hbar r^2}{m} \sum_{\ell} (2\ell+1) (\|b_\ell\|^2 - \|c_\ell\|^2)(h^{(1)}_\ell(kr) \partial_r h^{(2)}_\ell - h^{(2)}_\ell(kr) \partial_r h^{(1)}_\ell(kr)) 
\end{align}$$

It is sufficient to note that the term \\(h^{(1)}_\ell(kr) \partial_r h^{(2)}_\ell - h^{(2)}_\ell(kr) \partial_r h^{(1)}_\ell(kr) \neq 0\\) to conclude that \\(\|b_\ell\|^2 - \|c_\ell\|^2 = 0\\). Note that if we want to be more specific, we can show that 

$$\begin{equation}
h^{(1)}_\ell(kr) \partial_r h^{(2)}_\ell - h^{(2)}_\ell(kr) \partial_r h^{(1)}_\ell(kr) = -\frac{2i}{kr^2}
\end{equation}$$

We can simplify the term with the \\(r\\) in it because it is the Wronskian, using the familiar theorem from Sturm-Liouville theory: if 

$$\begin{equation}
(py')' - qy + \lambda \sigma y = 0
\end{equation}$$

Then the Wronskian is given by

$$\begin{equation}
W(x) = \frac{c}{p(x)}.
\end{equation}$$

If we plug in some specific value of \\(r\\), then we find the above result (the constant \\(c = -2i/k\\)). Thus, we have that 

$$\begin{align}
\oint \mathbf{J}\cdot \d\mathbf{A} ={}& \frac{4\pi\hbar}{m} \sum_{\ell=0}^\infty (2\ell+1) (\|b_\ell\|^2 - \|c_\ell\|^2)
\end{align}$$

Now, it may be a bit more clear that we should set \\(\|b_\ell\| = \|c_\ell\|\\).

Now, what are the consequences of this condition on the following wave function:

$$\begin{equation}
\psi = A\sum_{\ell=0}^\infty i^\ell (2\ell+1)(j_\ell(kr) + ika_\ell h^{(1)}_\ell(kr))P_\ell(\cos\theta)?
\end{equation}$$

Let's show that that we have partial wave phase shifts \\(\delta_\ell\\), and find their relationship to \\(a_\ell\\). 



If we return to our original wave function, we have that 

$$\begin{equation}
\psi = A\sum_{\ell=0}^\infty i^\ell(2\ell+1)(j_\ell(kr) + ika_\ell h^{(1)}_\ell(kr)) P_\ell(\cos\theta)
\end{equation}$$

and since \\(j_\ell(kr) = \frac{1}{2}(h^{(1)}_\ell(kr) + h^{(2)}_\ell(kr))\\), then we get 

$$\begin{equation}
\psi = A\sum_{\ell=0}^\infty i^\ell(2\ell+1)\left[\left(\frac{1}{2} + ika_\ell \right)h^{(1)}_\ell(kr) + \frac{1}{2}h^{(2)}_\ell(kr)\right] P_\ell(\cos\theta)
\end{equation}$$

Since we have that the magnitudes of the coefficients must be equal, they must differ only by a phase. Therefore, we set 

$$\begin{equation}
\frac{1}{2} + ika_\ell = \frac{1}{2}e^{2i\delta_\ell},\qquad a_\ell = \frac{1}{2ik}(e^{2i\delta_\ell} - 1) = \frac{1}{k}e^{i\delta_\ell}\sin(\delta_\ell)
\end{equation}$$

and the solution is then written as 

$$\begin{equation}
\psi = A\sum_{\ell=0}^\infty i^\ell\frac{(2\ell+1)}{2}\left[e^{2i\delta} h^{(1)}_\ell(kr) + h^{(2)}_\ell(kr)\right] P_\ell(\cos\theta)
\end{equation}$$

so the outgoing wave is phase-shifted by \\(2\delta\\) in comparison to the incoming wave. The 2 in the exponent is a mere convention; we think of the incoming wave as being shifted by \\(\delta\\), and then shifted again on the way out. 


Next, let's relate the scattering phase shifts can be related to the scattering cross section. The scattering cross section can be rewritten as 

$$\begin{align}
\sigma ={}& 4\pi \sum_{\ell =0 }^\infty (2\ell+1) \|a_\ell\|^2 \\
={}& 4\pi \sum_{\ell =0 }^\infty (2\ell+1) \bigg\|\frac{1}{k}e^{i\delta_\ell}\sin\delta_\ell\bigg\|^2 \\ 
={}& \frac{4\pi}{k^2} \sum_{\ell =0 }^\infty (2\ell+1)\sin^2\delta_\ell
\end{align}$$

Thus, if we have the partial wave phase shifts, we can calculate the scattering cross section. 




<div class="example">
<b>Example:</b>
Consider the problem from last week, with the 3D infinite spherical barrier. In this case, the potential was 

$$\begin{equation}
V(r) = \begin{cases} \infty & r < a \\ 0 & r \geq a \end{cases}
\end{equation}$$

so the wave function for \(r < a\) was zero. For this problem

<ol type="a">
<li> Compute the partial wave phase shifts \(\delta_\ell\)
</li>
<li> Compute the partial wave shift for the case \(ka \ll 1\)
</li></ol>

<b>Solution:</b>
<ol type="a">
<li> The partial wave shifts can be gotten from the partial wave amplitudes, which we calculated last time to be 

$$\begin{equation}
a_\ell = \frac{ij_\ell(ka)}{kh^{(1)}_\ell(ka)}
\end{equation}$$

Then, the partial wave phase shifts are 

$$\begin{align}
e^{2i\delta_\ell} ={}& 1 + 2ika_\ell \\
={}& 1 - \frac{2j_\ell(ka)}{h^{(1)}_\ell(ka)} \\
={}& \frac{h^{(1)}_\ell(ka) - 2j_\ell(ka)}{h^{(1)}_\ell(ka)} \\
={}& \frac{j_\ell(ka) + iy_\ell(ka) - 2j_\ell(ka)}{h^{(1)}_\ell(ka)} \\
={}& -\frac{h^{(2)}_\ell(ka)}{h^{(1)}_\ell(ka)} 
\end{align}$$

Thus, we have that 

$$\begin{equation}
2\delta_\ell = \pi - 2\Arg(h^{(1)}_\ell(ka))
\end{equation}$$

so the phase shift is 

$$\begin{equation}
\delta_\ell = \frac{\pi}{2} - \Arg h^{(1)}_\ell(kr) = \frac{\pi}{2} - \arctan \left(\frac{y_\ell(ka)}{j_\ell(ka)}\right)
\end{equation}$$

</li>
<li> The phase shift is given by plugging in the low-energy forms 

$$\begin{equation}
j_\ell(z) \sim \frac{z^\ell 2^\ell \ell!}{(2\ell)!},\qquad y_\ell(z) \sim -\frac{(2\ell+1)!}{z^{\ell+1}2^\ell \ell!}
\end{equation}$$

$$\begin{align}
\delta_\ell ={}& \frac{\pi}{2} - \arctan\left(-\frac{(2\ell+1)!(2\ell)! }{(ka)^{2\ell+1}2^{2\ell} \ell!^2}\right) \\
={}&\frac{\pi}{2} + \arctan\left(\frac{(2\ell+1)!(2\ell)! }{(ka)^{2\ell+1}2^{2\ell} \ell!^2}\right) \\
={}&\pi - \arctan\left(\frac{(ka)^{2\ell+1}2^{2\ell} \ell!^2}{(2\ell+1)!(2\ell)! }\right) \\
={}&\pi - \frac{(ka)^{2\ell+1}2^{2\ell} \ell!^2}{(2\ell+1)!(2\ell)!}
\end{align}$$

Where we have taken the first term in the Taylor series for \((ka)\ll 1\) in the last step. This gives us \(\delta_\ell = \pi - (ka)^{2\ell+1}2^{2\ell} \ell!^2/(2\ell+1)!(2\ell)!\).
</li></ol>

</div>


<div class="example">
<b>Example:</b>
Let us now consider a 3D spherical well potential

$$\begin{equation}
V(r) = \begin{cases} - V_0 & r < a \\ 0 & r \geq a \end{cases}
\end{equation}$$

<ol type="a">
<li> Compute the partial wave phase shifts for each \(\ell\).
</li>
<li> Compute the phase shift \(\delta_0\) for \(\ell = 0\). 
</li>
<li> In the low-energy limit \(ka\ll 1\), compute the scattering cross section. Do this by taking only the \(\ell=0\) term. 
</li></ol>

<b>Solution:</b>
<ol type="a">
<li> The Schrödinger equation is given by 

$$\begin{equation}
-\frac{\hbar^2}{2mr^2}\frac{\partial}{\partial r}\left(r^2\frac{\partial R}{\partial r}\right) + V_\text{eff}(r)R = ER
\end{equation}$$

where 

$$\begin{equation}
V_\text{eff}(r) = V(r) + \frac{\hbar^2\ell(\ell+1)}{2mr^2}
\end{equation}$$

In the region \(r > a\), we have that the wave function is the typical form 

$$\begin{equation}
\psi_\text{out} = A\sum_{\ell=0}^\infty i^\ell \frac{(2\ell+1)}{2}(h^{(1)}_\ell(kr) e^{2i\delta_\ell} + h^{(2)}_\ell(kr))P_\ell(\cos\theta)
\end{equation}$$

and in the region \(r < a\), we have 

$$\begin{equation}
\psi_\text{in} = B\sum_{\ell=0}^\infty  i^\ell (2\ell+1) c_\ell j_\ell(k_0 r) P_\ell(\cos\theta)
\end{equation}$$

Note that the \(i^\ell(2\ell+1)\) is not strictly necessary, but we include it for convenience. Then, we have that the wave function should be continuous at \(r = a\), and its derivative should also be continuous there. Thus, we have that the continuity condition is

$$\begin{equation}
\frac{A}{2}[h^{(1)}_\ell(ka) e^{2i\delta_\ell} + h^{(2)}_\ell(ka)] = Bc_\ell j_\ell(k_0 a)
\end{equation}$$

and the 

$$\begin{equation}
\frac{Ak}{2}[h^{(1)\prime}_\ell(ka) e^{2i\delta_\ell} + h^{(2)\prime}_\ell(ka)] = Bk_0c_\ell j_\ell'(k_0 a)
\end{equation}$$

If we solve for the phase shift by dividing these two equations, we find that 

$$\begin{equation}
\frac{k[h^{(1)\prime}_\ell(ka) e^{2i\delta_\ell} + h^{(2)\prime}_\ell(ka)]}{h^{(1)}_\ell(ka) e^{2i\delta_\ell} + h^{(2)}_\ell(ka)} = k_0 \frac{j'_\ell(k_0a)}{j_\ell(k_0a)}
\end{equation}$$

Then, we can rearrange a little to get 

$$\begin{align}
kj_\ell(k_0a)[h^{(1)\prime}_\ell(ka) e^{2i\delta_\ell} + h^{(2)\prime}_\ell(ka)] ={}& k_0 j'_\ell(k_0a)[h^{(1)}_\ell(ka) e^{2i\delta_\ell} + h^{(2)}_\ell(ka)] \\
kj_\ell(k_0a)h^{(1)\prime}_\ell(ka) e^{2i\delta_\ell} + kj_\ell(k_0a) h^{(2)\prime}_\ell(ka) ={}& k_0 j'_\ell(k_0a)h^{(1)}_\ell(ka) e^{2i\delta_\ell} + k_0 j'_\ell(k_0a) h^{(2)}_\ell(ka) 
\end{align}$$

Then rearranging, we find 

$$\begin{equation}
e^{2i\delta_\ell}[kj_\ell(k_0a)h^{(1)\prime}_\ell(ka) - k_0 j'_\ell(k_0a)h^{(1)}_\ell(ka) ] = k_0 j'_\ell(k_0a) h^{(2)}_\ell(ka) - kj_\ell(k_0a) h^{(2)\prime}_\ell(ka)
\end{equation}$$

and finally solving for 

$$\begin{equation}
e^{2i\delta_\ell} = \frac{k_0 j'_\ell(k_0a) h^{(2)}_\ell(ka) - kj_\ell(k_0a) h^{(2)\prime}_\ell(ka)}{kj_\ell(k_0a)h^{(1)\prime}_\ell(ka) - k_0 j'_\ell(k_0a)h^{(1)}_\ell(ka) }
\end{equation}$$

As a sanity check, we can let \(V_0\to-\infty\), which means that, defining \(\kappa = \sqrt{2m(-E-V_0)}/\hbar\), the Bessel functions get replaced by modified Bessel functions so 

$$\begin{align}
e^{2i\delta_\ell} ={}& \frac{k_0 i'_\ell(\kappa_0a) h^{(2)}_\ell(ka) - ki_\ell(\kappa a) h^{(2)\prime}_\ell(ka)}{ki_\ell(\kappa_0a)h^{(1)\prime}_\ell(ka) - k_0 i'_\ell(\kappa a)h^{(1)}_\ell(ka) } \\
={}& 1 + \frac{\kappa i'_\ell(\kappa a) h^{(2)}_\ell(ka) - ki_\ell(\kappa a) h^{(2)\prime}_\ell(ka)}{ki_\ell(\kappa a)h^{(1)\prime}_\ell(ka) - \kappa i'_\ell(\kappa a)h^{(1)}_\ell(ka) } - 1 \\
={}& 1 + \frac{\kappa i'_\ell(\kappa a) h^{(2)}_\ell(ka) - ki_\ell(\kappa a) h^{(2)\prime}_\ell(ka) - ki_\ell(\kappa a)h^{(1)\prime}_\ell(ka) + \kappa i'_\ell(\kappa a)h^{(1)}_\ell(ka) }{ki_\ell(\kappa a)h^{(1)\prime}_\ell(ka) - \kappa i'_\ell(\kappa a)h^{(1)}_\ell(ka) } \\
={}& 1 + \frac{2\kappa i'_\ell(\kappa a) j_\ell(ka) - 2ki_\ell(\kappa a) j'_\ell(ka)}{ki_\ell(\kappa a)h^{(1)\prime}_\ell(ka) - \kappa i'_\ell(\kappa a)h^{(1)}_\ell(ka) }
\end{align}$$

Since the asymptotic form is \(i_\ell(z) \sim e^z/2z\), we have that \(i'_\ell(z) \sim e^2/2z\) and thus 

$$\begin{align}
e^{2i\delta_\ell} ={}& 1 + \frac{2\kappa i'_\ell(\kappa a) j_\ell(ka) - 2ki_\ell(\kappa a) j'_\ell(ka)}{ki_\ell(\kappa a)h^{(1)\prime}_\ell(ka) - \kappa i'_\ell(\kappa a)h^{(1)}_\ell(ka)} \\
={}& 1 + 2\frac{\kappa j_\ell(ka) - k j'_\ell(ka)}{kh^{(1)\prime}_\ell(ka) - \kappa h^{(1)}_\ell(ka)} \\
={}& 1 - 2\frac{\kappa j_\ell(ka)}{\kappa h^{(1)}_\ell(ka)} \\
={}& 1 - \frac{2j_\ell(ka)}{h^{(1)}_\ell(ka)}
\end{align}$$

which agrees for \(a_\ell = ij_\ell(ka)/kh^{(1)}_\ell(ka)\). Thus we have confidence that our answer is correct.

</li>
<li> For the result from the previous part 

$$\begin{align}
e^{2i\delta_\ell} ={}& -\frac{kj_\ell(k_0a) h^{(2)\prime}_\ell(ka) - k_0 j'_\ell(k_0a) h^{(2)}_\ell(ka)}{kj_\ell(k_0a)h^{(1)\prime}_\ell(ka) - k_0 j'_\ell(k_0a)h^{(1)}_\ell(ka)} 
\end{align}$$

we can observe that the denominator is the complex conjugate of the numerator. This makes sense because the magnitudes of the numerator and denominator must be equal! Letting 

$$\begin{equation}
z = kj_\ell(k_0a)h^{(1)\prime}_\ell(ka) - k_0 j'_\ell(k_0a)h^{(1)}_\ell(ka) = \|z\|e^{i\varphi}
\end{equation}$$

where \(\varphi = \Arg(z)\). Then, we have that 

$$\begin{equation}
e^{2i\delta_\ell} = e^{i\pi} \frac{z^*}{z} = e^{i\pi} e^{-2i\varphi}
\end{equation}$$

so that 

$$\begin{align}
\delta_\ell ={}& \frac{\pi}{2} - \varphi \\
={}& \frac{\pi}{2} - \Arg[kj_\ell(k_0a)h^{(1)\prime}_\ell(ka) - k_0 j'_\ell(k_0a)h^{(1)}_\ell(ka)] 
\end{align}$$

Now, let us consider the case \(\ell=0\). Then, we plug in the functions 

$$\begin{equation}
j_0(z) = \frac{\sin z}{z},\qquad h^{(1)}_0(z) = -i \frac{e^{iz}}{z}
\end{equation}$$

This gives us 

$$\begin{align}
\delta_\ell ={}& \frac{\pi}{2} - \Arg\left[k \frac{\sin(k_0 a)}{k_0 a}\left(i\frac{e^{ika}}{(ka)^2} + \frac{e^{ika}}{ka}\right) + ik_0\left(-\frac{\sin(k_0 a)}{(k_0a)^2} + \frac{\cos(k_0 a)}{k_0 a}\right) \frac{e^{ika}}{ka}\right] \\
={}& \frac{\pi}{2} - \Arg\left[k \sin(k_0 a)\left(i\frac{1}{(ka)} + 1\right) + ik_0\left(-\frac{\sin(k_0 a)}{(k_0a)} + \cos(k_0 a)\right) \right] - ka \\
={}& \frac{\pi}{2} - \Arg\left[\sin(k_0 a)\left(i\frac{1}{a} + k\right) + i\left(-\frac{\sin(k_0 a)}{a} + k_0\cos(k_0 a)\right) \right] - ka \\
={}& \frac{\pi}{2} - \Arg\left[\sin(k_0 a)k + ik_0\cos(k_0 a)\right] - ka \\
={}& \frac{\pi}{2} - \Arg\left[ik_0\left(\cos(k_0 a) - i\frac{k}{k_0}\sin(k_0 a)\right)\right] - ka \\
={}& - \Arg\left[\left(\cos(k_0 a) - i\frac{k}{k_0}\sin(k_0 a)\right)\right] - ka \\
={}& - \arctan\left(-\frac{k}{k_0}\tan(k_0 a)\right) - ka \\
={}& \arctan\left(\frac{k}{k_0}\tan(k_0 a)\right) - ka
\end{align}$$

</li>
<li> The phase shift from the previous section is given by 

$$\begin{align}
\delta_0 = \arctan\left(\frac{k}{k_0}\tan(k_0 a)\right) - ka
\end{align}$$

and in the low-energy limit, we can rewrite this as

$$\begin{align}
\delta_0 ={}& \arctan\left(\frac{ka}{k_0a}\tan(k_0 a)\right) - ka \\
={}& \frac{ka}{k_0a}\tan(k_0 a) - ka \\
={}& ka\left(\frac{\tan(k_0 a)}{k_0a} - 1\right)
\end{align}$$

The first term in the scattering cross section series is then given by 

$$\begin{align}
\sigma ={}& \frac{4\pi}{k^2}\sin^2\delta_0 \\
={}& \frac{4\pi}{k^2}\sin^2\left[ka\left(\frac{\tan(k_0 a)}{k_0a} - 1\right)\right] \\
={}& \frac{4\pi}{k^2}\left[ka\left(\frac{\tan(k_0 a)}{k_0a} - 1\right)\right]^2 \\
={}& 4\pi a^2 \left(\frac{\tan(k_0 a)}{k_0a} - 1\right)^2
\end{align}$$

For the case \(k_0 a\to 0\), the scattering cross section goes to zero which makes sense because

$$\begin{equation}
k_0 = \sqrt{\frac{2m(E+V_0)}{\hbar^2}}
\end{equation}$$

and we already assumed \(E\approx 0\), so \(k_0 = \sqrt{2mV_0}/\hbar\), and as \(k_0\to 0\), this occurs when \(V_0\to 0\), so there is no potential at all. If instead \(k_0 a = n\pi\), then (returning to the previous formula) we have \(\delta_0 \sim 0\) as well, and the scattering cross section goes to zero, even when the potential is nonzero. This is called the <i>Ramsauer-Townsend effect</i>. It makes sense because, setting \(k_0 = 2\pi/\lambda\), we have that \(\lambda = 2a/n\), and the wave length is commensurate with the spherical well.

On the other hand, if \(k_0 a\to \pi/2\), then the scattering cross section diverges! This makes sense because when \(k_0a = \pi/2\), the first bound state appears (at zero energy!). Then, \(\delta_0\to 1\) and \(\sigma = 4\pi/k^2\), and \(k\) is very large! The incoming particle resonates strongly with the bound state, causing the cross section to be very large. 

Note that the origin of the bound state can be found by looking at 

$$\begin{equation}
\kappa = -k_0\cot(k_0 a)
\end{equation}$$

where \(\kappa = \sqrt{-2mE}/\hbar\), and \(k_0 = \sqrt{2m(E+V_0)}/\hbar\). We can rewrite this equation as (defining \(w_0 = \sqrt{2mV_0}a/\hbar\) and \(w = k_0 a\))

$$\begin{align}
-\cot(k_0 a) ={}& \frac{\kappa}{k_0} \\
-\cot(w) ={}& \frac{\kappa a}{w} \\
={}& \frac{1}{w}\frac{a\sqrt{-2mEa^2}}{\hbar} \\
={}& \frac{1}{w}\frac{a\sqrt{-2m(E+V_0) + 2mV_0}}{\hbar} \\
={}& \frac{1}{w}\sqrt{-a^2\frac{2m(E+V_0)}{\hbar^2} + \frac{2mV_0a^2}{\hbar^2}} \\
={}& \frac{1}{w}\sqrt{-w^2 + w_0^2} \\
={}& \sqrt{\frac{w_0^2}{w^2} - 1}
\end{align}$$

The first solution occurs at \(w = \pi/2\) when \(w_0 = \pi/2\). If \(w_0 < \pi/2\), there are no solutions. This is when we get the energy resonance! Since \(w = k_0 a = \pi/2\), this corresponds to the behaviour we found above.
</li></ol>

</div>

