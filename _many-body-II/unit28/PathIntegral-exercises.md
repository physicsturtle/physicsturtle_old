---
layout: lesson
title: Path Integral - Exercises
dept: physics
course: many-body-II
unit: unit28
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 28
---
<ol>
\question Evaluate the integral
$$I_{S,m} = \int_0^1 x^{S+m}(1-x)^{S-m}\d x$$

by using the following generating function:

$$f_S(z) = \sum_{n=0}^{2S} \binom{2S}{n} I_{S,n-S} z^n.$$

\begin{solution}
$$\begin{align}
f_S(z) =& \sum_{n=0}^{2S} \binom{2S}{n} z^n \int_0^1 x^n(1-x)^{2S-n}\d x \\
=& \int_0^1 \sum_{n=0}^{2S} \binom{2S}{n} (zx)^n(1-x)^{2S-n}\d x \\
=& \int_0^1 (zx+1-x)^{2S} \d x \\
=& \frac{[1+(z-1)x]^{2S+1}}{(z-1)(2S+1)}\big|_0^1 \\
=& \frac{1}{2S+1}\frac{z^{2S+1}-1}{z-1} 
\end{align}$$

We can therefore expand \\(f_S(z)\\) as 

$$f_S(z) = \frac{1}{2S+1}\left(1 + z + \cdots z^{2S}\right).$$

Thus, with the original representation of \\(f_S(z)\\) being 

$$f_S(z) = \binom{2S}{0} I_{S,-S} + \binom{2S}{1} I_{S,1-S}z + \cdots \binom{2S}{S+m} I_{S,m} z^{S+m} + \cdots + \binom{2S}{2S}I_{S,S} z^{2S}$$

we find that, matching coefficients of \\(f_S(z)\\), that 

$$\binom{2S}{S+m}I_{S,m} = \frac{1}{2S+1}$$

and finally solving for \\(I_{S,m}\\) gives us 

$$I_{S,m} = \frac{(S+m)!(S-m)!}{(2S+1)!}$$

\end{solution}

\question Verify that 

$$\bra{\Omega}\ket{\Omega'} = e^{iS(\chi'-\chi)}\left(\frac{1 + \boldsymbol{\Omega}\cdot\boldsymbol{\Omega}'}{2}\right)^S\exp\left(2Si\arctan\left[\tan\left(\frac{\varphi'-\varphi}{2}\right)\frac{\cos(\frac{1}{2}(\theta+\theta'))}{\cos(\frac{1}{2}(\theta-\theta'))}\right]\right) $$

\begin{solution}
We proceed with a direct computation. Doing this, we get 

$$\begin{align}
\bra{\Omega}\ket{\Omega'} =& e^{iS(\chi'-\chi)}\sum_{mm'} \frac{\cos^{S+m}(\frac{\theta}{2})\sin^{S+m}(\frac{\theta}{2})\cos^{S+m'}(\frac{\theta'}{2})\sin^{S-m'}(\frac{\theta'}{2})e^{i(\varphi'm'-\varphi m)}(2S)!}{\sqrt{(S+m)!}\sqrt{(S-m)!}\sqrt{(S+m')!}\sqrt{(S-m')!}} \bra{S.m}\ket{S,m'} \\
=& e^{iS(\chi'-\chi)}\sum_{mm'} \frac{\cos^{S+m}(\frac{\theta}{2})\sin^{S+m}(\frac{\theta}{2})\cos^{S+m'}(\frac{\theta'}{2})\sin^{S-m'}(\frac{\theta'}{2})e^{i(\varphi'm'-\varphi m)}(2S)!}{\sqrt{(S+m)!}\sqrt{(S-m)!}\sqrt{(S+m')!}\sqrt{(S-m')!}} \delta_{mm'} \\
=& e^{iS(\chi'-\chi)}\sum_{m=-S}^S \frac{\cos^{S+m}(\frac{\theta}{2})\sin^{S+m}(\frac{\theta}{2})\cos^{S+m}(\frac{\theta'}{2})\sin^{S-m}(\frac{\theta'}{2})e^{i(\varphi'-\varphi) m}(2S)!}{(S+m)!(S-m)!} \\
=& e^{iS(\chi'-\chi)}\left[\cos\left(\frac{\theta}{2}\right)\sin\left(\frac{\theta}{2}\right)\cos\left(\frac{\theta'}{2}\right)\sin\left(\frac{\theta'}{2}\right)\right]^S \sum_{m=-S}^S (2S)!\frac{\cot^m(\frac{\theta}{2})\cot^m(\frac{\theta'}{2})e^{i(\varphi'-\varphi)m}}{(S+m)!(S-m)!}
\end{align}$$

We can apply the binomial theorem to evaluate the sum over \\(m\\); 

$$\sum_{m=-S}^S x^m \binom{2S}{S-m} = \frac{(1+x)^{2S}}{x^S}$$

Thus this simplifies to 

$$\begin{align}
\bra{\Omega}\ket{\Omega'} =& e^{iS(\chi'-\chi)}\left[\cos\left(\frac{\theta}{2}\right)\sin\left(\frac{\theta}{2}\right)\cos\left(\frac{\theta'}{2}\right)\sin\left(\frac{\theta'}{2}\right)\right]^S \frac{(1+\cot(\frac{\theta}{2})\cot(\frac{\theta'}{2})e^{i(\varphi'-\varphi)})^{2S}}{(\cot(\frac{\theta}{2})\cot(\frac{\theta'}{2})e^{i(\varphi'-\varphi)})^S} \\
=& e^{iS(\chi'-\chi)}\left[\sin\left(\frac{\theta}{2}\right)\sin\left(\frac{\theta'}{2}\right)\right]^{2S} \left(1+\cot(\frac{\theta}{2})\cot(\frac{\theta'}{2})e^{i(\varphi'-\varphi)}\right)^{2S} e^{-i(\varphi'-\varphi)S}\\
=& e^{iS(\chi'-\chi)}\left[\sin\left(\frac{\theta}{2}\right)\sin\left(\frac{\theta'}{2}\right)e^{-i(\varphi'-\varphi)/2}+\cos(\frac{\theta}{2})\cos(\frac{\theta'}{2})e^{i(\varphi'-\varphi)/2}\right]^{2S}
\end{align}$$

We now write out the complex exponentials inside the brackets in terms of sines and cosines to get

$$\begin{align}
\bra{\Omega}\ket{\Omega'} =& e^{iS(\chi'-\chi)}\left[\left(\sin\left(\frac{\theta}{2}\right)\sin\left(\frac{\theta'}{2}\right)+\cos(\frac{\theta}{2})\cos(\frac{\theta'}{2})\right)\cos\left(\frac{\varphi'-\varphi}{2}\right) \right. \\
&\left. + i\left(\cos(\frac{\theta}{2})\cos(\frac{\theta'}{2})-\sin\left(\frac{\theta}{2}\right)\sin\left(\frac{\theta'}{2}\right)\right)\sin\left(\frac{\varphi'-\varphi}{2}\right)\right]^{2S} \\
=& e^{iS(\chi'-\chi)}\left[\cos\left(\frac{\theta-\theta'}{2}\right)\cos\left(\frac{\varphi'-\varphi}{2}\right) + i\cos\left(\frac{\theta+\theta'}{2}\right)\sin\left(\frac{\varphi'-\varphi}{2}\right)\right]^{2S}
\end{align}$$

We now wish to write the interior or the brackets in terms of a complex exponential:

$$\begin{align}
\alpha =& \cos\left(\frac{\theta-\theta'}{2}\right)\cos\left(\frac{\varphi'-\varphi}{2}\right) + i\cos\left(\frac{\theta+\theta'}{2}\right)\sin\left(\frac{\varphi'-\varphi}{2}\right) \\
=& |\alpha|e^{i\arg(\alpha)}
\end{align}$$

We find that 

$$\begin{align}
|\alpha| =& \sqrt{\cos^2\left(\frac{\varphi'-\varphi}{2}\right)\cos^2\left(\frac{\theta'-\theta}{2}\right) + \sin^2\left(\frac{\varphi'-\varphi}{2}\right)\cos^2\left(\frac{\theta+\theta'}{2}\right)}\\
=& \sqrt{\frac{1+\cos^2(\frac{\varphi'-\varphi}{2})\cos(\theta'-\theta) + \sin^2(\frac{\varphi'-\varphi}{2})\cos(\theta+\theta')}{2}} \\
=& \sqrt{\frac{1+\cos\theta\cos\theta' + \cos(\varphi'-\varphi)\sin\theta\sin\theta'}{2}}
\end{align}$$

We recognize:

$$\begin{align}
\boldsymbol{\Omega}\cdot\boldsymbol{\Omega'} =& (\sin\theta\cos\varphi,\sin\theta\sin\varphi,\cos\theta)\cdot(\sin\theta'\cos\varphi',\sin\theta'\sin\varphi',\cos\theta') \\
=&\cos\theta\cos\theta' + \cos(\varphi'-\varphi)\sin\theta\sin\theta'
\end{align}$$

which tells us that 

$$\begin{align}
|\alpha| =& \sqrt{\cos^2\left(\frac{\varphi'-\varphi}{2}\right)\cos^2\left(\frac{\theta'-\theta}{2}\right) + \sin^2\left(\frac{\varphi'-\varphi}{2}\right)\cos^2\left(\frac{\theta+\theta'}{2}\right)}\\
=& \sqrt{\frac{1+\cos^2(\frac{\varphi'-\varphi}{2})\cos(\theta'-\theta) + \sin^2(\frac{\varphi'-\varphi}{2})\cos(\theta+\theta')}{2}} \\
=& \sqrt{\frac{1+\boldsymbol{\Omega}\cdot\boldsymbol{\Omega}'}{2}}
\end{align}$$

Now we compute the argument of the complex number. This gives us 

$$\begin{align}
\arg(\alpha) =& \tan\left(\frac{\varphi'-\varphi}{2}\right)\frac{\cos(\frac{1}{2}(\theta+\theta'))}{\cos(\frac{1}{2}(\theta-\theta'))}
\end{align}$$

This tells us that 

$$\begin{align}
\bra{\Omega}\ket{\Omega'} =& e^{iS(\chi'-\chi)}\left(\frac{1 + \boldsymbol{\Omega}\cdot\boldsymbol{\Omega}'}{2}\right)^S\exp\left(2Si\arctan\left[\tan\left(\frac{\varphi'-\varphi}{2}\right)\frac{\cos(\frac{1}{2}(\theta+\theta'))}{\cos(\frac{1}{2}(\theta-\theta'))}\right]\right) 
\end{align}$$

We can simplify this expression a little bit by defining 

$$\psi = \chi - \chi' + 2\arctan\left[\tan\left(\frac{\varphi-\varphi'}{2}\right)\frac{\cos(\frac{1}{2}(\theta+\theta'))}{\cos(\frac{1}{2}(\theta-\theta'))}\right]$$

so that the overlap between coherent states can be rewritten as 

$$\begin{align}
\bra{\Omega}\ket{\Omega'} =& \left(\frac{1 + \boldsymbol{\Omega}\cdot\boldsymbol{\Omega}'}{2}\right)^Se^{-iS\psi} 
\end{align}$$

Note that this means the coherent states are not orthogonal; clearly this matrix element is not zero.

\end{solution}

\question Verify that 

$$\bra{\Omega}(\hat{S}_x,\hat{S}_y,\hat{S}_z)\ket{\Omega} = S(\cos\varphi\sin\theta,\sin\varphi\sin\theta,\cos\theta)$$

\begin{solution}
We will start with the \\(z\\) component. Doing this, we find 

$$\begin{align}
\bra{\Omega}\hat{S}^z\ket{\Omega} =& 
\end{align}$$

\end{solution}

\question Compute \\(\bra{\Omega}(\hat{S}_x,\hat{S}_y,\hat{S}_z)\ket{\Omega'}\\). 

\begin{solution}

\end{solution}


\end{questions}


\subsection{Path Integral}

We now need to construct the path integral for the partition function of a spin system, for example the Heisenberg model. We consider a Hamiltonian 


<ol>
\question
\end{questions}

