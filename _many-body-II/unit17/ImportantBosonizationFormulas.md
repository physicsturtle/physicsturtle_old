---
layout: lesson
title: Important Bosonization Formulas
dept: physics
course: many-body-II
unit: unit17
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 17
---

Another important formula is the normal ordering of the exponential of the boson field. This gives us 

$$\begin{align}
:e^{ir\phihat_\alpha(x)}: =& \sum_{n=0}^\infty \frac{(ir)^n}{n!} :(\phihat_\alpha(x))^n: \\
=& \sum_{n=0}^\infty \frac{(ir)^n}{n!} :(\varphihat^\dagger_\alpha(x) + \varphihat_\alpha(x))^n: \\
=& \sum_{n=0}^\infty \frac{(ir)^n}{n!} \sum_{m=0}^n \binom{n}{m} (\varphihat^\dagger_\alpha(x))^m( \varphihat_\alpha(x))^{n-m}  \\
\end{align}$$

where we can use the binomial theorem because the fields are normal ordered; everything commutes in the normal ordered product. Next, we swap the order of summation to get 

$$\begin{align}
:e^{ir\phihat_\alpha(x)}: =& \sum_{m=0}^\infty\sum_{n =m}^\infty \frac{(ir)^m (ir)^{n-m}}{m!(n-m)!} (\varphihat^\dagger_\alpha(x))^m( \varphihat_\alpha(x))^{n-m}  \\
=& \sum_{m=0}^\infty \frac{ir)^m}{m!} (\varphihat^\dagger_\alpha(x))^m \sum_{n=m}^\infty \frac{(ir)^{n-m}}{(n-m)!} (\varphihat_\alpha(x))^{n-m} \\
=& \sum_{m=0}^\infty \frac{ir)^m}{m!} (\varphihat^\dagger_\alpha(x))^m \sum_{n=0}^\infty \frac{(ir)^{n}}{(n)!} (\varphihat_\alpha(x))^{n} \\
=& e^{ir\varphihat^\dagger_\alpha(x)} e^{ir\varphihat_\alpha(x)} 
\end{align}$$

We can combine the two exponentials again, using the fact that the commutator \\([\varphihat_\alpha(x), \varphihat^\dagger_{\alpha'}(x')] = - \delta_{\alpha\alpha'}\log\left(\frac{2\pi}{L}(i(x'-x) + a)\right)\\), which gives 

$$\begin{align}
:e^{ir\phihat_\alpha(x)}: =& e^{ir(\varphihat^\dagger_\alpha(x) + \varphihat_\alpha(x))} e^{(ir)^2[\varphihat^\dagger_\alpha(x), \varphihat_{\alpha}(x)]/2} \\
=&  e^{ir(\varphihat^\dagger_\alpha(x) + \varphihat_\alpha(x))} e^{-\frac{r^2}{2}\log\frac{2\pi a}{L}} \\
=& e^{ir\phihat_\alpha(x)} \left(\frac{L}{2\pi a}\right)^{r^2/2}
\end{align}$$

We can also derive another expression for products of exponentials at different points. This derivation is simply 

$$\begin{align}
:e^{ir\phihat_\alpha(x)} e^{ir'\phihat_\alpha(y)}: =& :\sum_{n=0}^\infty \frac{(ir)^n}{n!}(\phihat_\alpha(x))^n \sum_{m=0}^\infty \frac{(ir')^m}{m!} (\phihat_\alpha(y))^m: \\
=& \sum_{n,m=0}^\infty \frac{(ir)^n(ir')^m}{n!m!} :(\varphihat^\dagger_\alpha(x) + \varphihat_\alpha(x))^n(\varphihat^\dagger_\alpha(y) + \varphihat_\alpha(y))^m: \\
=& \sum_{n,m=0}^\infty \frac{(ir)^n(ir')^m}{n!m!}\sum_{k=0}^n \sum_{\ell=0}^m \binom{n}{k} \binom{m}{\ell} (\varphihat^\dagger_\alpha(x))^k (\varphihat^\dagger_\alpha(y))^\ell (\varphihat_\alpha(y))^{m-\ell} (\varphihat_\alpha(x))^{n-k} \\
=& \sum_{n,m,k,\ell=0}^\infty \frac{(ir)^n(ir')^m (ir)^k (ir')^\ell}{n!m!k!\ell!} (\varphihat^\dagger_\alpha(x))^k (\varphihat^\dagger_\alpha(y))^\ell (\varphihat_\alpha(y))^m (\varphihat_\alpha(x))^n \\
=& e^{ir\varphihat^\dagger_\alpha(x)} e^{ir'\varphihat^\dagger_\alpha(y)} e^{ir' \varphihat_\alpha(y)} e^{ir\varphihat_\alpha(x)}
\end{align}$$

Next, we combine the middle two fields in the same way as above to get 

$$\begin{align}
:e^{ir\phihat_\alpha(x)} e^{ir'\phihat_\alpha(y)}: =& \left(\frac{L}{2\pi a}\right)^{r^{\prime 2}/2} e^{ir\varphihat^\dagger_\alpha(x)} e^{ir'\phihat_\alpha(y)} e^{ir\varphihat_\alpha(x)}
\end{align}$$

Now, we use the fact that \\(e^A e^B = e^B e^A e^{[A,B]}\\), which holds in the case where \\(C=[A,B]\\) satisfies \\([A,C]=[B,C]=0\\), to find that 

$$\begin{align}
:e^{ir\phihat_\alpha(x)} e^{ir'\phihat_\alpha(y)}: =& \left(\frac{L}{2\pi a}\right)^{r^{\prime 2}/2} e^{ir\varphihat^\dagger_\alpha(x)} e^{ir\varphihat_\alpha(x)} e^{ir'\phihat_\alpha(y)} e^{-rr'[\phihat_\alpha(y), \varphihat_\alpha(x)]} \\
=& \left(\frac{L}{2\pi a}\right)^{r^{\prime 2}/2} e^{ir\varphihat^\dagger_\alpha(x)} e^{ir\varphihat_\alpha(x)} e^{ir'\phihat_\alpha(y)} e^{-rr'[\varphihat^\dagger_\alpha(y), \varphihat_\alpha(x)]} \\
=& \left(\frac{L}{2\pi a}\right)^{r^{\prime 2}/2} e^{ir\varphihat^\dagger_\alpha(x)} e^{ir\varphihat_\alpha(x)} e^{ir'\phihat_\alpha(y)} e^{-rr'\log\left(\frac{2\pi}{L}(i(y-x) + a)\right)} \\
=& \left(\frac{L}{2\pi a}\right)^{r^{\prime 2}/2} e^{ir\varphihat^\dagger_\alpha(x)} e^{ir\varphihat_\alpha(x)} e^{ir'\phihat_\alpha(y)} \left(\frac{L}{2\pi(i(y-x) + a)}\right)^{rr'}
\end{align}$$

Now we combine the first two terms to find 

$$\begin{align}
:e^{ir\phihat_\alpha(x)} e^{ir'\phihat_\alpha(y)}: =& \left(\frac{L}{2\pi a}\right)^{(r^{\prime 2}+r^2)/2} \left(\frac{L}{2\pi(i(y-x) + a)}\right)^{rr'} e^{ir\phihat_\alpha(x)} e^{ir'\phihat_\alpha(y)} 
\end{align}$$

We can invert the relation to find a useful formula for the product of two exponentials of bosonic fields: 

$$\begin{align}
e^{ir\phihat_\alpha(x)} e^{ir'\phihat_\alpha(y)} =& \left(\frac{L}{2\pi a}\right)^{-(r^{\prime 2}+r^2)/2} \left(\frac{L}{2\pi(i(y-x) + a)}\right)^{-rr'}  :e^{ir\phihat_\alpha(x)} e^{ir'\phihat_\alpha(y)}:
\end{align}$$

<div class="result">
<b>Result:</b>
The following expressions for exponentials are very useful: 

$$\begin{align}
e^{ir\phihat_\alpha(x)} =&  \left(\frac{L}{2\pi a}\right)^{-r^2/2} :e^{ir\phihat_\alpha(x)}:\\
e^{ir\phihat_\alpha(x)} e^{ir'\phihat_\alpha(y)} =& \left(\frac{L}{2\pi a}\right)^{-(r^{\prime 2}+r^2)/2} \left(\frac{L}{2\pi(i(y-x) + a)}\right)^{-rr'}  :e^{ir\phihat_\alpha(x)} e^{ir'\phihat_\alpha(y)}:
\end{align}$$

These are useful because everything commutes inside the (bosonic) normal ordering! 


</div>

We now are interested in computing some famous bosonization formulas. In the following, we assume \\(y-x = \epsilon\\), where \\(\epsilon\\) is very small, but still \\(\epsilon \gg a\\). Thus, we should take the limit \\(a\to 0\\) first, and then the limit \\(\epsilon\to 0\\). 

$$\begin{align}
\psihat^\dagger_\alpha(x) \psihat_\alpha(x) =& \lim_{\epsilon\to 0} \lim_{a\to 0} \psihat^\dagger_\alpha(x) \psihat_\alpha(x+\epsilon) \\
=& \lim_{\epsilon\to 0} \lim_{a\to 0} \frac{1}{2\pi a} e^{i\phihat_\alpha(x)} e^{-i\phihat_\alpha(x+\epsilon)} \\
=& \lim_{\epsilon\to 0} \lim_{a\to 0} \frac{1}{2\pi a} \left(\frac{L}{2\pi a}\right)^{-1} \left(\frac{L}{2\pi(i(y-x) + a)}\right)^1 :e^{i\phihat_\alpha(x)} e^{-i\phihat_\alpha(x+\epsilon)}: \\
=& \lim_{\epsilon\to 0} \lim_{a\to 0} \frac{1}{2\pi a} \left(\frac{L}{2\pi a}\right)^{-1} \left(\frac{L}{2\pi(i\epsilon + a)}\right)^1 :e^{i\phihat_\alpha(x)} e^{-i\phihat_\alpha(x+\epsilon)}: \\
=& \lim_{\epsilon\to 0} \lim_{a\to 0} \frac{1}{2\pi(i\epsilon + a)} :e^{i\phihat_\alpha(x)-i\phihat_\alpha(x+\epsilon)}: \\
=& \lim_{\epsilon\to 0} \frac{1}{2\pi i\epsilon} :e^{-i\epsilon\partial_x\phihat_\alpha(x) - i\epsilon^2\partial^2_x \phihat_\alpha(x)/2 + \cdots }: \\
=& \lim_{\epsilon\to 0} \frac{1}{2\pi i\epsilon} :\left(-i\epsilon\partial_x\phihat_\alpha(x) + O(\epsilon^2)  \right) \\
=& \lim_{\epsilon\to 0} \frac{1}{2\pi i} :\left(-i\partial_x\phihat_\alpha(x) + O(\epsilon)  \right) \\
=& -\frac{1}{2\pi} \partial_x\phihat_\alpha(x) \\
\end{align}$$

Now, we consider the fermion term which appears in the kinetic part. 

$$\begin{align}
\psihat^\dagger_\alpha(x)\partial_x\psihat_\alpha(x) =& \lim_{\epsilon\to 0} \lim_{a\to 0} \partial_y\left[ \psihat^\dagger_\alpha(x) \psihat_\alpha(y)\right] \bigg|_{y=x+\epsilon} \\
=& \lim_{\epsilon\to 0}\lim_{a\to 0} \frac{1}{2\pi a} \left(\frac{L}{2\pi a}\right)^{-1}\partial_y\left[ \left(\frac{L}{2\pi(i(y-x)+a)}\right)^1 :e^{i\phihat_\alpha(x)} e^{-i\phihat_\alpha(y)}: \right] \bigg|_{y=x+\epsilon} \\
=& \lim_{\epsilon\to 0} \frac{1}{L} \partial_y\left[ \frac{L}{2\pi i(y-x)} :e^{i\phihat_\alpha(x)} e^{-i\phihat_\alpha(y)}: \right] \bigg|_{y=x+\epsilon} \\
=& \lim_{\epsilon\to 0} \left[ -\frac{1}{2\pi i(y-x)^2}  :e^{i\phihat_\alpha(x)} e^{-i\phihat_\alpha(y)}:  + \frac{1}{2\pi i(y-x)} \partial_y :e^{i\phihat_\alpha(x)} e^{-i\phihat_\alpha(y)}: \right] \bigg|_{y=x+\epsilon}
\end{align}$$

We then plug in \\(\epsilon\\), and replace the derivative with respect to \\(y\\) with one instead with respect to \\(\epsilon\\). Since the \\(\psi\\) have the same functional dependence on \\(y\\) as they do on \\(\epsilon\\), this is ok. Thus, doing the Taylor expansion gives 

$$\begin{align}
\psihat^\dagger_\alpha(x)\partial_x\psihat_\alpha(x) =& \lim_{\epsilon\to 0} \left[ -\frac{1}{2\pi i\epsilon^2} :\left(1 - i\epsilon\partial_x \phihat_\alpha(x) - i\frac{\epsilon^2}{2}\partial^2_x \phihat_\alpha(x) - \frac{\epsilon^2}{2}(\partial_x\phihat_\alpha)^2 + O(\epsilon^3) \right): \right. \\
&+ \left. \frac{1}{2\pi i\epsilon}  \partial_\epsilon :\left(1 - i\epsilon\partial_x \phihat_\alpha(x) - i\frac{\epsilon^2}{2}\partial^2_x \phihat_\alpha(x) - \frac{\epsilon^2}{2}(\partial_x\phihat_\alpha)^2 + O(\epsilon^3) \right): \right] \\
=& \lim_{\epsilon\to 0} \left[ -\frac{1}{2\pi i\epsilon^2} :\left(- i\epsilon\partial_x \phihat_\alpha(x) - i\frac{\epsilon^2}{2}\partial^2_x \phihat_\alpha(x) - \frac{\epsilon^2}{2}(\partial_x\phihat_\alpha)^2 + O(\epsilon^3) \right): \right. \\
&+ \left. \frac{1}{2\pi i\epsilon}  \partial_\epsilon :\left(- i\epsilon\partial_x \phihat_\alpha(x) - i\frac{\epsilon^2}{2}\partial^2_x \phihat_\alpha(x) - \frac{\epsilon^2}{2}(\partial_x\phihat_\alpha)^2 + O(\epsilon^3) \right): \right] \\
=& \lim_{\epsilon\to 0} \frac{1}{2\pi i\epsilon} \left[ -:\left(- i\partial_x \phihat_\alpha(x) - i\frac{\epsilon}{2}\partial^2_x \phihat_\alpha(x) - \frac{\epsilon}{2}(\partial_x\phihat_\alpha)^2 + O(\epsilon^2) \right): \right. \\
&+ \left. :\left(- i\partial_x \phihat_\alpha(x) - i\epsilon\partial^2_x \phihat_\alpha(x) - \epsilon(\partial_x\phihat_\alpha)^2 + O(\epsilon^2) \right): \right] \\
=& \lim_{\epsilon\to 0} \frac{1}{2\pi i\epsilon} \left[ -:\left( - i\frac{\epsilon}{2}\partial^2_x \phihat_\alpha(x) - \frac{\epsilon}{2}(\partial_x\phihat_\alpha)^2 + O(\epsilon^2) \right): \right. \\
&+ \left. :\left(- i\epsilon\partial^2_x \phihat_\alpha(x) - \epsilon(\partial_x\phihat_\alpha)^2 + O(\epsilon^2) \right): \right] \\
=& \frac{1}{2\pi i} \left[ :\left(i\frac{1}{2}\partial^2_x \phihat_\alpha(x) + \frac{1}{2}(\partial_x\phihat_\alpha)^2 \right): - :\left(i\partial^2_x \phihat_\alpha(x) + (\partial_x\phihat_\alpha)^2\right): \right] \\
=& - \frac{1}{2\pi i} :\left(i\frac{1}{2}\partial^2_x \phihat_\alpha(x) + \frac{1}{2}(\partial_x\phihat_\alpha)^2 \right): \\
\end{align}$$

Thus we find 

$$\begin{align}
\psihat^\dagger_\alpha(x)\partial_x\psihat_\alpha(x) =&\frac{1}{4\pi } :\left( i(\partial_x\phihat_\alpha)^2 - \partial^2_x \phihat_\alpha(x) \right):
\end{align}$$

<div class="result">
<b>Result:</b>
The famous bosonization formulas are given by (in the thermodynamic limit)

$$\begin{align}
\psihat_\alpha(x) =& \frac{1}{\sqrt{2\pi a}} \Fhat_\alpha  e^{-i\phihat_\alpha(x)} \\
\psihat^\dagger_\alpha(x) \psihat_\alpha(x) =& -\frac{1}{2\pi} \partial_x \phihat_\alpha(x) \\
\psihat^\dagger_\alpha(x)\partial_x\psihat_\alpha(x) =&\frac{1}{4\pi } :\left( i(\partial_x\phihat_\alpha)^2 - \partial^2_x \phihat_\alpha(x) \right):
\end{align}$$

Note that the latter term of the kinetic expression disappears when the entire thing is put under an integral due to periodicity of the derivative of the bosonic field.


</div>


