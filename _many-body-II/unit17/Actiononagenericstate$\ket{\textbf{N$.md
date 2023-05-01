---
layout: lesson
title: Action on a generic state $\ket{\textbf{N$ 
dept: physics
course: many-body-II
unit: unit17
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 17
---
Now that we know how \\(\psihat_\alpha(x)\\) acts on the state \\(\ket{\textbf{N}}_0\\), we should determine how \\(\psihat_\alpha(x)\\) acts on a generic state. For this, we use the fact that a generic state \\(\ket{\textbf{N}} = f(\varphihat^\dagger)\ket{\textbf{N}}_0\\). It is clear we will need to commute \\(\psihat_\alpha(x)\\) past \\(f(\varphihat^\dagger)\\), so the following two identities are useful. 

$$\begin{align}
\psihat_\alpha(x) f(\varphihat^\dagger) = f(\varphihat^\dagger_{q\alpha'} - \delta_{\alpha\alpha'}a_q(x)) \psihat_\alpha(x) \\
f(\varphihat^\dagger_{q\alpha'} - \delta_{\alpha\alpha'} a^{*}_q(x)) = e^{-i\varphihat_\alpha(x)} f(\varphihat^\dagger) e^{i\varphihat_\alpha(x)}
\end{align}$$

Now, we act on the generic state with the fermionic annihilation operator:

$$\begin{align}
\psihat_\alpha(x)\ket{\textbf{N}} =& \psihat_\alpha(x) f(\{\varphihat^\dagger_{q\alpha'}\}) \ket{\textbf{N}}_0 \\
=& f(\{\varphihat^\dagger_{q\alpha'} - \delta_{\alpha\alpha'}a^{*}_q(x)\}) \psihat_\alpha(x) \ket{\textbf{N}}_0
\end{align}$$

Here, we used the identity above for commuting the \\(\psihat\\) past \\(f(\{\varphihat\})\\). Next, we use the action of \\(\psihat_\alpha(x)\\) on the \\(\textbf{N}\\)-particle ground state, which we derived in the previous section, as well as use the other identity to rewrite the \\(f\\) part:. This gives us 

$$$$\begin{align}
\psihat_\alpha(x)\ket{\textbf{N}} = f(\{\varphihat^\dagger_{q\alpha'} - \delta_{\alpha\alpha'}a^{*}_q(x)\}) \left(e^{-i\varphihat^\dagger_\alpha(x)} \Fhat_\alpha \hat{\lambda}_\alpha(x) \ket{\textbf{N}}_0 \right)
\end{align}$$$$

Then, since the Klein factor changes the number of particles and the \\(\hat{\lambda}\\) factor depends only on the number of fermions, we can commute both the Klein factor and \\(\hat{\lambda}\\) factor as long as they stay together and don't swap positions. Thus CHECK THAT STATEMENT

$$$$\begin{align}
\psihat_\alpha(x)\ket{\textbf{N}} = \Fhat_\alpha \hat{\lambda}_\alpha(x) f(\{\varphihat^\dagger_{q\alpha'} - \delta_{\alpha\alpha'}a^{*}_q(x)\}) e^{-i\varphihat^\dagger_\alpha(x)}  \ket{\textbf{N}}_0 
\end{align}$$$$

Furthermore, we can swap the order of the \\(e^{-i\varphihat^\dagger_\alpha(x)}\\) factor with the \\(f\\) because they deal with different flavours. 

$$$$\begin{align}
\psihat_\alpha(x)\ket{\textbf{N}} = \Fhat_\alpha \hat{\lambda}_\alpha(x) e^{-i\varphihat^\dagger_\alpha(x)}  f(\{\varphihat^\dagger_{q\alpha'} - \delta_{\alpha\alpha'}a^{*}_q(x)\}) \ket{\textbf{N}}_0
\end{align}$$$$

Next, we can use the other identity to rewrite the \\(f\\) factor as

$$$$\begin{align}
\psihat_\alpha(x)\ket{\textbf{N}} = \Fhat_\alpha \hat{\lambda}_\alpha(x) e^{-i\varphihat^\dagger_\alpha(x)}  e^{-i\varphihat_\alpha(x)} f(\varphihat^\dagger) e^{i\varphihat_\alpha(x)}\ket{\textbf{N}}_0
\end{align}$$$$

Since \\(\varphihat_\alpha(x)\ket{\textbf{N}}_0 = 0\\), we have \\(e^{i\varphihat_\alpha(x)}\ket{\textbf{N}}_0 = \ket{\textbf{N}}_0\\) and we get 

$$$$\begin{align}
\psihat_\alpha(x)\ket{\textbf{N}} = \Fhat_\alpha \hat{\lambda}_\alpha(x) e^{-i\varphihat^\dagger_\alpha(x)}  e^{-i\varphihat_\alpha(x)} f(\varphihat^\dagger) \ket{\textbf{N}}_0
\end{align}$$$$

Finally, we combine \\(f\\) back in to the state and get 

$$$$\begin{align}
\psihat_\alpha(x)\ket{\textbf{N}} = \Fhat_\alpha \hat{\lambda}_\alpha(x) e^{-i\varphihat^\dagger_\alpha(x)}  e^{-i\varphihat_\alpha(x)} \ket{\textbf{N}}
\end{align}$$$$

Therefore, we have found the action of \\(\psihat_\alpha(x)\\) acting on an arbitrary state. Thus, we write 

$$$$\begin{align}
\left( \psihat_\alpha(x) - \Fhat_\alpha \hat{\lambda}_\alpha(x) e^{-i\varphihat^\dagger_\alpha(x)}  e^{-i\varphihat_\alpha(x)}\right)\ket{\textbf{N}} = 0
\end{align}$$$$

Thus since \\(\ket{\textbf{N}}\\) is arbitrary, we find that 

$$$$\begin{align}
\psihat_\alpha(x) = \Fhat_\alpha \hat{\lambda}_\alpha(x) e^{-i\varphihat^\dagger_\alpha(x)}  e^{-i\varphihat_\alpha(x)}
\end{align}$$$$

This is the fundamental bosonization identity. Plugging in the form of \\(\lambda_\alpha(x)\\), this formula can be rewritten as 

$$$$\begin{align}
\psihat_\alpha(x) = \frac{1}{\sqrt{L}} \Fhat_\alpha e^{i\frac{2\pi}{L}(\Nhat_\alpha-\delta_b/2)x}  e^{-i\varphihat^\dagger_\alpha(x)}  e^{-i\varphihat_\alpha(x)}
\end{align}$$$$

Then, using the identity \\(e^A e^B = e^{A+B}e^{[A,B]/2}\\) (which holds when \\(C = [A,B]\\) commutes with both \\(A\\) and \\(B\\), \\([A,C] = [A,B] = 0\\)), we get 

$$\begin{align}
\psihat_\alpha(x) =& \frac{1}{\sqrt{L}} \Fhat_\alpha e^{i\frac{2\pi}{L}(\Nhat_\alpha-\delta_b/2)x}  e^{-i\phihat_\alpha(x)} e^{-\frac{1}{2}\log\frac{2\pi}{L}a} \\
=& \frac{1}{\sqrt{L}} \Fhat_\alpha e^{i\frac{2\pi}{L}(\Nhat_\alpha-\delta_b/2)x}  e^{-i\phihat_\alpha(x)} \sqrt{\frac{L}{2\pi a}} \\
=& \frac{1}{\sqrt{2\pi a}} \Fhat_\alpha e^{i\frac{2\pi}{L}(\Nhat_\alpha-\delta_b/2)x}  e^{-i\phihat_\alpha(x)} \\
=& \frac{1}{\sqrt{2\pi a}} \Fhat_\alpha  e^{-i\Phihat_\alpha(x)} \\
\end{align}$$

where \\(\phihat_\alpha(x) = \varphihat^\dagger_\alpha(x) + \varphihat_\alpha(x)\\), and \\(\Phihat_\alpha(x) = \phihat_\alpha(x) - \frac{2\pi}{L}(\Nhat_\alpha -\delta_b/2)x\\). Note that, in the thermodynamic limit \\(L\to\infty\\), \\(\Phihat_\alpha(x) = \phihat_\alpha(x)\\). 


