---
layout: lesson
title: Hamiltonian with Linear Dispersion - Exercises
dept: physics
course: many-body-II
unit: unit17
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 17
---
<ol>
\question Take the continuum limit of the 1-dimensional Hubbard model, whose Hamiltonian (including chemical potential) is given by 

$$H = -t\sum_{i\sigma} \chat^\dagger_{i\sigma} \chat_{i+1,\sigma} + \hc + U\sum_i \nhat_{i\uparrow} \nhat_{i\downarrow} - \mu\sum_{i\sigma} \nhat_{i\sigma}$$

\begin{solution}
One way to do this is by first Fourier transforming the entire model to momentum space. 
\end{solution}

\question Compute the commutation relations for the bosons. 
<ol type="a">
</li> 
 <li> \\([\varphihat_{q\alpha},\varphihat_{q'\alpha'}]\\)
</li> 
 <li> \\([\hat{N}_{q\alpha},\varphihat_{q'\alpha'}]\\)
</li> 
 <li> \\([\varphihat_{q\alpha},\varphihat^\dagger_{q'\alpha'}]\\)
\end{parts}

\begin{solution}
<ol type="a">
</li> 
 <li> We compute the commutator simply as 

$$\begin{align}
[\varphihat_{q\alpha},\varphihat_{q'\alpha'}] =& -\frac{1}{\sqrt{n_qn_{q'}}}\sum_{kk'}\left(\psihat^\dagger_{k-q,\alpha}\psihat_{k\alpha} \psihat^\dagger_{k'-q',\alpha'} \psihat_{k'\alpha'} - \psihat^\dagger_{k'-q',\alpha'} \psihat_{k'\alpha'} \psihat^\dagger_{k-q,\alpha} \psihat_{k\alpha}\right) \\
=& -\frac{1}{\sqrt{n_qn_{q'}}} \sum_{kk'}\left(\psihat^\dagger_{k-q,\alpha} \psihat_{k'\alpha'} \delta_{\alpha\alpha'} \delta_{k,k'-q'} - \psihat^\dagger_{k'-q',\alpha'}\psihat_{k\alpha} \delta_{\alpha\alpha'} \delta_{k',k-q}\right) \\
=& -\frac{1}{\sqrt{n_qn_{q'}}}\sum_k \left(\psihat^\dagger_{k-q'-q,\alpha} \psihat_{k\alpha} - \psihat^\dagger_{k-q-q',\alpha} \psihat_{k\alpha}\right)\delta_{\alpha\alpha'}
\end{align}$$

where the last step is clear if we swap \\(k\\) and \\(k'\\) in the second sum.

</li> 
 <li> Now, we compute directly the following commutator 

$$\begin{align}
[\hat{N}_{q\alpha},\varphihat_{q'\alpha'}] =& 
\end{align}$$

</li> 
 <li> The third commutator is more subtle. One of the subtleties is that relabelling indices is a bit slippery because of the presence of infinities. 

$$\begin{align}
[\varphihat_{q\alpha}, \varphihat^\dagger_{q'\alpha'}] =& \frac{1}{\sqrt{n_qn_{q'}}}\sum_{kk'}\left[\chat^\dagger_{k-q,\alpha} \chat_{k\alpha}, \chat^\dagger_{k'+q',\alpha'} \chat_{k'\alpha'} \right] \\
=& \frac{1}{\sqrt{n_qn_{q'}}} \sum_{kk'} \left(\chat^\dagger_{k-q,\alpha} \chat_{k'\alpha'} \delta_{\alpha\alpha'}\delta_{k,k'+q'} - \chat^\dagger_{k'+q',\alpha'} \chat_{k\alpha} \delta_{\alpha\alpha'} \delta_{k',k-q}\right) \\
=& \frac{1}{\sqrt{n_qn_{q'}}} \sum_{k} \left(\chat^\dagger_{k-q,\alpha} \chat_{k-q'\alpha} - \chat^\dagger_{k-q+q',\alpha} \chat_{k\alpha} \right) \delta_{\alpha\alpha'}
\end{align}$$

Na\"ively, it appears that a simple relabelling will make these two expressions cancel out. However, this introduces infinities. To remedy this, we will introduce normal ordered expressions:

$$\begin{align}
[\varphihat_{q\alpha}, \varphihat^\dagger_{q'\alpha'}] =& \frac{\delta_{\alpha\alpha'}}{\sqrt{n_qn_{q'}}} \sum_{k} \left(:\chat^\dagger_{k-q,\alpha} \chat_{k-q'\alpha}: - :\chat^\dagger_{k-q+q',\alpha} \chat_{k\alpha}: + \bra{0}_0\chat^\dagger_{k-q,\alpha} \chat_{k-q'\alpha}\ket{0}_0 - \bra{0}_0\chat^\dagger_{k-q+q',\alpha} \chat_{k\alpha}\ket{0}_0 \right)
\end{align}$$

Now that things are normal ordered, the first two quantities cancel out because normal orderings effectively deal with infinities. 

$$\begin{align}
[\varphihat_{q\alpha}, \varphihat^\dagger_{q'\alpha'}] =& \frac{\delta_{\alpha\alpha'}}{\sqrt{n_qn_{q'}}} \sum_{k} \left(\bra{0}_0\chat^\dagger_{k-q,\alpha} \chat_{k-q'\alpha}\ket{0}_0 - \bra{0}_0\chat^\dagger_{k-q+q',\alpha} \chat_{k\alpha}\ket{0}_0 \right)
\end{align}$$

Now, we see that, in the first term, the vacuum will be annihilated if \\(k-q' > 0\\), but in the second term the vacuum will be annihilated if \\(k > 0\\); all the positive momentum states are initially empty. We also note that we require \\(q = q'\\), and so pick up a delta function. Then, we find 

$$\begin{align}
[\varphihat_{q\alpha}, \varphihat^\dagger_{q'\alpha'}] =& \frac{\delta_{\alpha\alpha'}\delta_{qq'}}{\sqrt{n_qn_{q'}}} \left(\sum_{k=-\infty}^{n_q} \bra{0}_0\chat^\dagger_{k-q,\alpha} \chat_{k-q,\alpha}\ket{0}_0 - \sum_{k=-\infty}^0 \bra{0}_0\chat^\dagger_{k\alpha} \chat_{k\alpha}\ket{0}_0 \right) \\
=& \frac{\delta_{\alpha\alpha'}\delta_{qq'}}{n_q} \left(\sum_{k=-\infty}^{n_q} 1 - \sum_{k=-\infty}^0 1 \right) \\
=& \frac{\delta_{\alpha\alpha'}\delta_{qq'}}{n_q} n_q \\
=& \delta_{\alpha\alpha'}\delta_{qq'}
\end{align}$$

\end{parts}
\end{solution}

\question Compute the following commutators:
<ol type="a">
</li> 
 <li> \\([\bhat_{q\alpha'}, \psihat_\alpha(x)]\\)
</li> 
 <li> \\([\bhat^\dagger_{q\alpha'}, \psihat_\alpha(x)]\\)
\end{parts}

\begin{solution}
<ol type="a">
</li> 
 <li> Doing the simple computation yields
$$\begin{align}
[\bhat_{q\alpha'}, \psihat_\alpha(x)] =& -\frac{i}{\sqrt{n_q}}\sum_{kk'} \frac{1}{\sqrt{L}} e^{ikx} [\chat^\dagger_{k'-q,\alpha'}\chat_{k'\alpha'}, \chat_{k\alpha}] \\
=& -\frac{i}{\sqrt{n_q}}\sum_{kk'}\frac{1}{\sqrt{L}} \delta_{k,k'-q}\delta_{\alpha\alpha'} e^{ikx} \chat_{k'\alpha'} \\
=& -\frac{i}{\sqrt{n_q}} \delta_{\alpha\alpha'} e^{-iqx} \sqrt{\frac{2\pi}{L}}\sum_{k'} e^{ik'x} \chat_{k'\alpha'} \\
=& -\frac{i}{\sqrt{n_q}}\delta_{\alpha\alpha'} e^{-iqx}\psihat_\alpha(x)
\end{align}$$

</li> 
 <li> Again, we perform the simple computation to get 

$$\begin{align}
[\bhat^\dagger_{q\alpha'}, \psihat_\alpha(x)] =& \frac{i}{\sqrt{n_q}}\sqrt{\frac{2\pi}{L}}\sum_{kk'} e^{ikx} [\chat^\dagger_{k'+q,\alpha'} \chat_{k'\alpha'}, \chat_{k\alpha}] \\
=& -\frac{i}{\sqrt{n_q}}\sqrt{\frac{2\pi}{L}}\sum_{kk'} e^{ikx} \chat_{k'\alpha'} \delta_{k,k'+q}\delta_{\alpha\alpha'} \\
=& \frac{i}{\sqrt{n_q}}\delta_{\alpha\alpha'}e^{iqx} \sqrt{\frac{2\pi}{L}}\sum_{k'} e^{ik'x} \chat_{k'\alpha} \\
=& \frac{i}{\sqrt{n_q}}\delta_{\alpha\alpha'}e^{iqx} \psihat_\alpha(x)
\end{align}$$



\end{parts}
\end{solution}

\question Compute the commutator

$$[\varphihat_\alpha(x), \varphihat^\dagger_{\alpha'}(x')] = -\delta_{\alpha\alpha'}\log\left(i\frac{2\pi}{L}(x-x'+i\eta)\right)$$

\begin{solution}
We do this with a direct computation
$$\begin{align}
[\varphihat_\alpha(x), \varphihat^\dagger_{\alpha'}(x')] =& \sum_{q>0;q'>0} \frac{1}{\sqrt{n_qn_{q'}}} e^{iqx} e^{-iq'x'} e^{-\eta q/2}e^{-\eta q'/2} [\bhat_{q\alpha}, \bhat^\dagger_{q'\alpha'}] \\
=& \sum_{q>0;q'>0} \frac{1}{\sqrt{n_qn_{q'}}} e^{iqx} e^{-iq'x'} e^{-\eta q/2}e^{-\eta q'/2} \delta_{qq'}\delta_{\alpha\alpha'} \\
=& \delta_{\alpha\alpha'}\sum_{q>0} \frac{1}{n_q} e^{iqx} e^{-iqx'} e^{-\eta q} \\
=& \delta_{\alpha\alpha'}\sum_{q>0} \frac{1}{n_q} e^{in_q\frac{2\pi}{L}(x-x'+i\eta)} \\
=& -\delta_{\alpha\alpha'}\log\left(i\frac{2\pi}{L}(x-x'+i\eta)\right)
\end{align}$$

\end{solution}
\end{questions}

