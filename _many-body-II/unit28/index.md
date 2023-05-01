---
layout: lesson
title: Spin Coherent State Path Integrals
dept: physics
course: many-body-II
unit: unit28
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 28
---
In this section, we will understand how to construct path integrals for spin, by defining coherent states and the resolution of identity in terms of them. 

For a spin \\(S\\) object, the Hilbert space is \\(2S+1\\)-dimensional. We will describe the states of the system in terms of the eigenstates of \\(\hat{S}_z\\). Our guiding question will be how to write the propagator \\(U(t)\\) as a sum over paths. We start by constructing a spin coherent state by using an overcomplete basis. We define the basis element 

$$\ket{\Omega} = \ket{\theta,\varphi} = U[R(\Omega)]\ket{S,S}$$

where \\(\ket{S,S} = \ket{S,S_z}\\), so the \\(S_z = S\\). We define \\(\ket{\theta,\varphi} = e^{-i\hat{S}_z\varphi} e^{-i\hat{S}_y\theta} \ket{S,S}\\). It is then straightforwardly verified that 

$$\bra{\Omega}(\hat{S}_x,\hat{S}_y,\hat{S}_z)\ket{\Omega} = S(\cos\varphi\sin\theta,\sin\varphi\sin\theta,\cos\theta)$$

We also have that 

$$\begin{align}
\ket{\Omega} =& e^{iS\chi} \sum_{m=-S}^S u^{s+m}v^{s-m}\frac{\sqrt{(2S)!}}{\sqrt{(S+m)!}\sqrt{(S-m)!}} \ket{S,m} \\
=& e^{iS\chi} \sum_{m=-S}^S \frac{\cos^{S+m}(\theta/2) \sin^{S-m}(\theta/2) e^{i\varphi m}\sqrt{(2S)!}}{\sqrt{(S+m)!}\sqrt{(S-m)!}} \ket{S,m}
\end{align}$$

<div class="result">
<b>Result:</b>
Formulas for spin coherent states:

$$\1 = \frac{2S+1}{4\pi}\int \ket{\Omega}\bra{\Omega} \d\Omega$$

$$\bra{\Omega'}\ket{\Omega} = \left(\frac{1+\boldsymbol{\Omega}\cdot\boldsymbol{\Omega}'}{2}\right)^S e^{-i\psi S}$$

whereby

$$\psi = \chi-\chi' + 2\arctan\left[\tan\left(\frac{\varphi-\varphi'}{2}\right)\frac{\cos(\frac{1}{2}(\theta+\theta'))}{\cos(\frac{1}{2}(\theta-\theta'))}\right]$$

$$\tr(A) = \frac{2S+1}{4\pi} \int \bra{\Omega} A \ket{\Omega} \d\Omega$$


</div>


To find the resolution of identity, let's calculate the following quantity:

$$\begin{align}
\int\ket{\Omega}\bra{\Omega}\d\Omega =& \sum_{mm'}\int \frac{\cos^{2S+m+m'}(\theta/2) \sin^{2S-m-m'}(\theta/2) e^{i\varphi(m-m')}  (2S)!}{\sqrt{(S+m)!}\sqrt{(S-m)!}\sqrt{(S+m')!}\sqrt{(S-m')!}} \ket{S,m}\bra{S,m'} \d\Omega  \\
=& \sum_{mm'}\int_0^\pi\int_0^{2\pi} \frac{\cos^{2S+m+m'}(\theta/2) \sin^{2S-m-m'}(\theta/2) e^{i\varphi (m-m')}  (2S)!}{\sqrt{(S+m)!}\sqrt{(S-m)!}\sqrt{(S+m')!}\sqrt{(S-m')!}} \ket{S,m}\bra{S,m'} \sin\theta\d\varphi\d\theta \\
=& 2\pi \sum_{mm'}\int_0^\pi\int_0^{2\pi} \frac{\cos^{2S+m+m'}(\theta/2) \sin^{2S-m-m'}(\theta/2) \delta_{mm'} (2S)!}{\sqrt{(S+m)!}\sqrt{(S-m)!}\sqrt{(S+m')!}\sqrt{(S-m')!}} \ket{S,m}\bra{S,m'} \sin\theta\d\theta \\
=& 2\pi\sum_{m=-S}^S\int_0^\pi \cos^{2S+2m}(\theta/2) \sin^{2S-2m}(\theta/2)  \sin\theta \d\theta \frac{(2S)!}{(S+m)!(S-m)!} \ket{S,m}\bra{S,m} \\
=& 4\pi \sum_{m=-S}^S I_{S,m} \frac{(2S)!}{(S+m)!(S-m)!} \ket{S,m}\bra{S,m}
\end{align}$$

Where we defined

$$\begin{align}
I_{S,m} =& \frac{1}{2} \int_0^\pi \cos^{2S+2m}(\theta/2) \sin^{2S-2m}\sin\theta \d\theta \\
=& \int_0^\pi (\cos^2(\theta/2))^{S+m} (\sin^2(\theta/2))^{S-m} \sin\theta \d\theta \\
=& \int_0^\pi \left(\frac{1+\cos\theta}{2}\right)^{S+m} \left(\frac{1-\cos\theta}{2}\right)^{S-m} \sin\theta \d\theta \\
=& \int_0^1 x^{S+m} (1-x)^{S-m} \d x \\
=& \frac{(S-m)!(S+m)!}{(2S+1)!}
\end{align}$$

where we made the substitution \\(x=\frac{1}{2}(1+\cos\theta)\\) to rewrite the integral. The integral over \\(x\\) is evaluated in the exercises. We then plug this result into our thing for the identity, which gives 

$$\begin{align}
\int\ket{\Omega}\bra{\Omega}\d\Omega =& 4\pi\sum_{m=-S}^S\frac{1}{2S+1} \ket{S,m}\bra{S,m}
\end{align}$$

Therefore, our resolution of identity is given by

$$\1 = \sum_{m=-S}^S \ket{S,m}\bra{S,m} = \frac{2S+1}{4\pi}\int \ket{\Omega}\bra{\Omega}\d\Omega$$

The next thing we need to do is to find out what the overlap between two coherent states is. This overlap is given by 



The next thing to do is to find out what the trace is in terms of coherent states. 
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


