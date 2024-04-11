---
layout: lesson
title: Partial Wave phase shifts 
dept: physics
course: qm-III
unit: unit8
deptDisplay: Physics
courseDisplay: Quantum Mechanics III
unitDisplay: Unit 8
---

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

<ol>
<li> <div class="exercise">  Let us now consider the soft sphere potential

$$\begin{equation}
V(r) = \begin{cases} V_0 & r < a \\ 0 & r \geq a \end{cases}
\end{equation}$$

<ol type="a">
<li>  Consider the case \(E > V_0\) 
<ol type="i">
<li> Solve the Schrödinger equation in the scattering region for the two cases 
</li>
<li> Compute the partial wave phase shifts for each \(\ell\) in terms of Bessel functions
</li>
<li> Explicitly calculate the phase shift \(\delta_0\) for \(\ell = 0\)
</li>
<li> In the low-energy limit \(ka\ll 1\), compute the scattering cross section. Do this by taking only the \(\ell=0\) term. 
</li></ol>
</li>
<li> \(E < V_0\)
<ol type="i">
<li> Solve the Schrödinger equation in the scattering region for the two cases 
</li>
<li> Compute the partial wave phase shifts for each \(\ell\) in terms of Bessel functions
</li>
<li> Explicitly calculate the phase shift \(\delta_0\) for \(\ell = 0\)
</li>
<li> In the low-energy limit \(ka\ll 1\), compute the scattering cross section. Do this by taking only the \(\ell=0\) term. 
</li></ol>

</li>
<li> Compare the results from the two cases. 
</li></ol>

<div class="answerBox"> 
 <button onclick="myFunction('answer436')" class="answerButton">Show Answer</button> 
 <div  id='answer436' class="answer" >
<ol type="a">

<li> 
<ol type="i">
<li> We need to solve the Schrödinger equation in the interior region. Unlike in the previous case, where the scattering region had oscillating states, we only have exponentially growing or decaying states in the interior region. The Schrödinger equation is given by 

\(\)-\frac{\hbar^2}{2mr^2}\frac{\partial}{\partial r}\left(r^2\frac{\partial R}{\partial r}\right) + V_\text{eff}(r)R = ER\(\)

where 

\(\)V_\text{eff} = V(r) + \frac{\hbar^2\ell(\ell+1)}{2mr^2}\(\)

In the region \(r > a\), we have the typical wave function

\(\)\psi_\text{out} = A\sum_{\ell=0}^\infty i^\ell \frac{2\ell+1}{2}(h^{(1)}_\ell(kr) e^{2i\delta_\ell} + h^{(2)}_\ell(kr))P_\ell(\cos\theta)\(\)

whereas in the region \(r < a\), we will have an oscillatory solution because the energy is greater than the potential. In particular, the solution will have the form

\(\)\psi_\text{in} = B\sum_{\ell=0}^\infty i^\ell (2\ell+1)c_\ell j_\ell(k_0 r) P_\ell(\cos\theta)\(\)

Here, \(k_0 = \sqrt{2m(E-V_0)}/\hbar\). Since \(E > V_0\), this is an oscillatory solution. Thus, in the inner region the solution is 

$$\begin{equation}
\psi_\text{in} = B\sum_{\ell=0}^\infty  i^\ell (2\ell+1) c_\ell j_\ell(k_0 r) P_\ell(\cos\theta)
\end{equation}$$

</li>
<li> To compute the partial wave shifts, we need to stitch together the two solutions. We use continuity and continuity of the derivative, as before: 

$$\begin{equation}
e^{2i\delta_\ell} = -\frac{k_0 j'_\ell(k_0a) h^{(2)}_\ell(ka) - kj_\ell(k_0a) h^{(2)\prime}_\ell(ka)}{k_0 j'_\ell(k_0a)h^{(1)}_\ell(ka) - kj_\ell(k_0a)h^{(1)\prime}_\ell(ka) }
\end{equation}$$

</li>
<li> 

</li></ol>

</li>
<li> 

<ol type="i">
<li> In the intermediate region \(r > a\), the typical wave function is given by 

\(\)\psi_\text{out} = A\sum_{\ell=0}^\infty i^\ell \frac{2\ell+1}{2}(h^{(1)}_\ell(kr) e^{2i\delta_\ell} + h^{(2)}_\ell(kr))P_\ell(\cos\theta)\(\)

whereas in the region \(r < a\), we will have an exponentially decaying solution. For this, let us look at the radial Schrödinger equation, which has the form 

\(\)-\frac{\hbar^2}{2mr^2}\frac{\partial}{\partial r}\left( r^2\frac{\partial R}{\partial r}\right)  + \left(\frac{\hbar^2\ell(\ell+1)}{2mr^2} + \frac{\hbar^2\kappa_0^2}{2m}\right)R = 0\(\)

whose solutions are the <i>modified Bessel functions</i> \(i_\ell(\kappa_0 r)\) and \(k_\ell(\kappa_0 r)\), rather than the typical ones. These two solutions are exponentially decaying and exponentially growing at large arugment. This doesn't really matter however, and what actually matters is the behaviour as \(r\to 0\). This tells us that we need \(i^{(1)}_\ell(\kappa r)\). Therefore, the wave function is 

\(\)\psi_\text{in} = B\sum_{\ell=0}^\infty i^\ell (2\ell+1) c_\ell i^{(1)}_\ell(\kappa r) P_\ell(\cos\theta)\(\)

Here, \(\kappa_0 = \sqrt{2m(V_0-E)}/\hbar\). 

</li>
<li> Now, we need to stitch together the two solutions. This gives us that the continuity condition is 

\(\)\frac{A}{2}(h^{(1)}_\ell(kr) e^{2i\delta_\ell} + h^{(2)}_\ell(kr)) = Bc_\ell i^{(1)}_\ell(\kappa_0 a)\(\)

and the continuity of the derivative is 

\(\)\frac{Ak}{2}(h^{(1)\prime}_\ell(kr) e^{2i\delta_\ell} + h^{(2)\prime}_\ell(kr)) = B\kappa c_\ell i^{(1)\prime}_\ell(\kappa_0 a)\(\)

Dividing the two equations, we find that 

\(\)k\frac{h^{(1)\prime}_\ell(kr) e^{2i\delta_\ell} + h^{(2)\prime}_\ell(kr)}{h^{(1)}_\ell(kr) e^{2i\delta_\ell} + h^{(2)}_\ell(kr)} = \frac{\kappa_0 i^{(1)\prime}_\ell(\kappa_0 a)}{i^{(1)}_\ell(\kappa_0 a)}\(\)

Thus, we can solve for \(e^{2i\delta_\ell}\) to get

\(\)e^{2i\delta_\ell} = -\frac{\kappa_0 i^{(1)\prime}_\ell(\kappa_0 a) h^{(2)}_\ell(ka) - k i^{(1)}_\ell(\kappa_0 a) h^{(2)\prime}_\ell(ka)}{\kappa_0 h^{(1)}_\ell(ka) i^{(1)\prime}_\ell(\kappa_0 a) - k h^{(1)\prime}_\ell(ka) i^{(1)}_\ell(\kappa_0 a)}\(\)

Then, the phase shifts can be found by noting that the numerator and denominator are complex conjugates are one another. Thus, we can write 

\(\)e^{2i\delta_\ell} = e^{i\pi} e^{-2i\varphi}\(\)

where 

\(\)\varphi = \Arg(\kappa_0 h^{(1)}_\ell(ka) i^{(1)\prime}_\ell(\kappa_0 a) - k h^{(1)\prime}_\ell(ka) i^{(1)}_\ell(\kappa_0 a))\(\)

Thus, 

\(\)2\delta_\ell = \pi - 2\varphi\(\)

Thus, we find 

\(\)\delta_\ell = \frac{\pi}{2} -  \Arg(\kappa_0 h^{(1)}_\ell(ka) i^{(1)\prime}_\ell(\kappa_0 a) - k h^{(1)\prime}_\ell(ka) i^{(1)}_\ell(\kappa_0 a))\(\)


</li>
<li> Now, we substitute in \(\ell=0\). This gives us 

$$\begin{align}
\delta_0 ={}& \frac{\pi}{2} - \Arg(\kappa_0 h^{(1)}_0(ka) i^{(1)\prime}_0(\kappa_0 a) - k h^{(1)\prime}_0(ka) i^{(1)}_0(\kappa_0 a)) 
\end{align}$$

Then, using the fact that 

\(\)j_0(z) = \frac{\sin z}{z}, \quad h^{(1)}_0(z) = -i\frac{e^{iz}}{z}\(\)

we can use \(i^{(1)}_\ell(z) = i^{-\ell}j_\ell(iz)\) we get that \(i^{(1)}_0(z) = \sinh z/z\). Thus, we get that 

$$\begin{align}
\delta_0 ={}& \frac{\pi}{2} - \Arg\left[\kappa_0\left(-i\frac{e^{ika}}{ka}\right)\left(-\frac{\sinh(\kappa_0 a)}{(\kappa_0 a)^2} + \frac{\cosh(\kappa_0 a)}{\kappa_0 a}\right) - k\left(\frac{e^{ika}}{ka} + i\frac{e^{ika}}{(ka)^2}\right)\left(\frac{\sinh(\kappa_0 a)}{\kappa_0 a}\right)\right] \\
={}& \frac{\pi}{2} - \Arg\left[-i\kappa_0e^{ika}\left(-\frac{\sinh(\kappa_0 a)}{\kappa_0 a} + \cosh(\kappa_0 a)\right) - k\left(e^{ika} + i\frac{e^{ika}}{ka}\right)\sinh(\kappa_0 a)\right] \\
={}& \frac{\pi}{2} - \Arg\left[ ie^{ika}\frac{\sinh(\kappa_0 a)}{a} - i\kappa_0 e^{ika}\cosh(\kappa_0 a) - ke^{ika}\sinh(\kappa_0 a) - ik\frac{e^{ika}}{a}\sinh(\kappa_0 a)\right] \\
={}& \frac{\pi}{2} - \Arg\left[- i\kappa_0 e^{ika}\cosh(\kappa_0 a) - ke^{ika}\sinh(\kappa_0 a)\right] \\
={}& \frac{\pi}{2} - \Arg\left[-i\kappa_0\cosh(\kappa_0 a) - k\sinh(\kappa_0 a)\right] - ka \\
={}& \frac{\pi}{2} - \left[\arctan\left(\frac{\kappa_0\cosh(\kappa_0 a)}{k\sinh(\kappa_0 a)}\right) - \pi \right] - ka \\
={}& -\pi + \frac{\pi}{2} - \arctan\left(\frac{\kappa_0\cosh(\kappa_0 a)}{k\sinh(\kappa_0 a)}\right)  - ka \\
={}& -\pi + \arctan\left(\frac{k\tanh(\kappa_0 a)}{\kappa_0}\right)  - ka \\
\end{align}$$
 
We throw out the \(\pi\) because it doesn't matter for the final results since we have \(e^{2i\delta_0}\) and \(e^{2\pi i} = 1\). 

$$\begin{align}
\delta_0 ={}& \arctan\left(\frac{k \tanh(\kappa_0 a)}{\kappa_0}\right) - ka
\end{align}$$

</li>
<li> In the limit \(ka\ll 1\), we have 

$$\begin{align}
\delta_0 ={}& \arctan\left(\frac{ka \tanh(\kappa_0 a)}{\kappa_0a}\right) - ka \\
={}& \frac{ka \tanh(\kappa_0 a)}{\kappa_0a} - ka \\
={}& ka \left(\frac{\tanh(\kappa_0 a)}{\kappa_0a} - 1\right) \\
\end{align}$$

Thus the cross section is 

$$\begin{align}
\sigma ={}& \frac{4\pi}{k^2}\sin^2\left[ka \left(\frac{\tanh(\kappa_0 a)}{\kappa_0a} - 1\right) \right] \\
={}& 4\pi a^2\left(\frac{\tanh(\kappa_0 a)}{\kappa_0a} - 1\right)^2 \\
\end{align}$$


</li></ol>

</li>
<li> 
</li></ol>
</div> 
 </div>

</div> </li></ol>


\subsection{Born Approximation}

The Schrödinger equation is given by 

$$-\frac{\hbar^2\nabla^2}{2m}\psi + V\psi = E\psi$$

Letting \\(k^2 = \sqrt{2mE}/\hbar\\) as usual, and defining \\(U = 2mV/\hbar^2\\), we can rewrite this equation as 

$$(\nabla^2 + k^2)\psi = U\psi$$

We recall from math that, if we have 

$$(\nabla^2 + k^2) \psi = S$$

then we have that the particular solution to the PDE is given by

$$\psi_p(\x) = -\frac{1}{4\pi} \int \frac{e^{ik\|\x-\x'\|}}{\|\x-\x'\|} S(\x') \d\x'$$

whereas the homogeneous solution is

$$\psi_h(\x) = \psi_0(\x)$$

In our case, the function \\(S\\) itself depends on \\(\psi\\), so we don't appear to have made the problem any easier by rewriting the Schrödinger as 

$$\psi(\x) = \psi_0(\x) - \frac{1}{4\pi}\int \frac{e^{ik\|\x-\x'\|}}{\|\x-\x'\|} U(\x')\psi(\x') \d\x' $$

Now plugging in the original form of \\(U\\), we have that 

$$\psi(\x) = \psi_0(\x) - \frac{m}{2\pi\hbar^2}\int \frac{e^{ik\|\x-\x'\|}}{\|\x-\x'\|} V(\x')\psi(\x') \d\x' $$

This is an exact rewriting of the Schrödinger equation; no approximations have been made yet. The nice thing about this representation however, is that it allows us to relate everything to the scattering form 

$$\psi(\x) = A\left(e^{ikz} + \frac{e^{ikr}}{r}f(\theta)\right)$$

The incoming wave function is the homogeneous solution \\(\psi_0(\x) = Ae^{ikz}\\). The outgoing solution is the second part. In order to relate to the scattering form, we need to take \\(\|\x\|\to\infty\\) to compare with the scattering amplitude \\(f\\). Then, we have that we need an approximation of the quantity \\(\|\x-\x'\|\\), which gives us 

$$\begin{align}
\|\x-\x'\| ={}& \sqrt{\x^2 - 2\x\cdot\x' + \x^{\prime 2}} \\
={}& \|\x\| \sqrt{1 - \frac{2\x\cdot\x' - \x^{\prime 2}}{\x^2}} \\
\approx{}& \|\x\| \left(1 - \frac{\x\cdot\x'}{\x^2}\right) \\
={}& \|\x\| - \rhat \cdot \x'
\end{align}$$

where \\(\rhat = \x/\|\x\|\\). Then, we have that 

$$\psi(\x) = \psi_0(\x) - \frac{m}{2\pi\hbar^2}\int \frac{e^{ik\|\x\| -ik\rhat\cdot\x'} }{\|\x\|} V(\x')\psi(\x') \d\x' $$

Then, we let \\(k\rhat = \k\\), and since \\(r = \|\x\|\\), we can rewrite this as 

$$\begin{align}
\psi(\x) ={}& Ae^{ikz} + \frac{e^{ikr}}{r}\left(-\frac{m}{2\pi \hbar^2}\int e^{-i\k\cdot\x'} V(\x')\psi(\x') \d\x'\right) \\
={}& A\left[e^{ikz} + \frac{e^{ikr}}{r}\left(-\frac{m}{2\pi \hbar^2 A}\int e^{-i\k\cdot\x'} V(\x')\psi(\x') \d\x'\right) \right]
\end{align}$$

Thus, we see that the scattering amplitude is given by 

$$f(\theta) = -\frac{m}{2\pi \hbar^2 A}\int e^{-i\k\cdot\x'} V(\x')\psi(\x') \d\x'$$

This is an exact expression for the scattering amplitude! No approximations have been made here (the approximations made for \\(\|\x-\x'\|\\) don't count because those were made just to bring the formulas into the asymptotic limit). The issue with the above formula however is that we do not know what \\(\psi\\) itself is, so we cannot plug the results into the formula! Well, if we have a high-energy incoming particle (\\(E\\) is large compared to \\(V\\)), then the particle will not be scattered very much. In this case, then we have that \\(\psi(\x') \approx \psi_0(\x')\\). Thus, we plug in \\(\psi(\x') = Ae^{ikz}\\). Then, we have 

$$f(\theta) = -\frac{m}{2\pi \hbar^2}\int e^{ikz} e^{-i\k\cdot\x'} V(\x') \d\x'$$

Finally defining \\(\k' = k\zhat\\), we have 

$$f(\theta) = -\frac{m}{2\pi \hbar^2}\int e^{i(\k'-\k)\cdot\x'} V(\x') \d\x'$$

<div class="example">
<b>Example:</b>
Consider soft sphere scattering. The potential of a soft sphere is given by 

\(\)V(\x) = \begin{cases}
V_0 & r < a \\
0 & r > a
\end{cases}\(\)

Then, the scattering amplitude can be found by directly plugging the potential in. The scattering amplitude becomes 

$$\begin{align}
f(\theta) ={}& -\frac{m}{2\pi\hbar^2} \int e^{i(\k-\k')\cdot\x'} V_0 \d\x' \\
={}& -\frac{m}{2\pi\hbar^2}\int e^{i\|\k-\k'\|r'\cos\theta'} V_0 \sin\theta' \d\varphi'\d\theta'\d r' \\
={}& -\frac{m}{2\pi\hbar^2} \int e^{i(\k-\k')\cdot\x'} V_0 \d\x' \\
={}& -\frac{m}{2\pi\hbar^2}2\pi \int e^{i\|\k-\k'\|r'\cos\theta'} V_0 \sin\theta' \d\theta'\d r' 
\end{align}$$

Then, letting \(u = \cos\theta'\), we get 

$$\begin{align}
f(\theta) ={}& -\frac{m}{2\pi\hbar^2}2\pi \int_0^a\int_{-1}^1  e^{i\|\k-\k'\|r'u} V_0 r^{\prime 2} \d u\d r' \\
={}& -\frac{m}{2\pi\hbar^2}2\pi  V_0  \int_0^a\frac{e^{i\|\k-\k'\|r'} - e^{-i\|\k-\k'\|r'}}{i\|\k-\k'\|r'} r^{\prime 2} \d r' \\
={}& -\frac{m}{2\pi\hbar^2}4\pi  V_0  \int_0^a\frac{\sin(\|\k-\k'\|r')}{\|\k-\k'\|}r'\d r' \\
={}& -\frac{m}{2\pi\hbar^2} \frac{4\pi  V_0}{\|\k-\k'\|} \left(-\frac{a\cos(\|\k-\k'\|a)}{\|\k-\k'\|} + \frac{\sin(\|\k-\k'\|a)}{\|\k-\k'\|^2} \right)
\end{align}$$

Then, since \(\k = k\rhat\) and \(\k' = k\zhat\), we have \(\|\k-\k'\| = k\sqrt{2(1-\cos\theta) }= 2k\sin(\theta/2)\). Thus, since \(\|\k-\k'\|\) is proportional to \(k\) so then the low energy limit \(ak \ll 1\) leads us to Taylor expand the sine and cosine. This gives us 

\(\)f(\theta) = -\frac{m}{2\pi\hbar^2}V_0\left(\frac{4\pi a^3}{3}\right)\(\)

Then, the differential cross section is 

\(\)\frac{\d\sigma}{\d\Omega} = \left(\frac{2m V_0 a^3}{3\hbar^2}\right)^2\(\)

and the total cross section is 

\(\)\sigma = 4\pi\left(\frac{2m V_0 a^3}{3\hbar^2}\right)^2\(\)

We see that when \(V_0\) gets bigger, the cross section is bigger. This makes sense 


</div>

