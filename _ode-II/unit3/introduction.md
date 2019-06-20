---
layout: lesson
title: Introduction
course: ode-II
unit: unit3
---

The Fourier transform is ubiquitous throughout mathematics, physics, and engineering. In this section, we will study how it can be used to find integral representations of solutions to certain ODEs, thus making them easier to solve. For example, the Airy equation $y'' = xy$ which we solved by series methods earlier can also have its solution be represented by an integral! In this section, we will introduce the idea of the Fourier transform and some definitions. 

This section will require the reader to know the calculus of complex variables. 

<div class="definition">
Let $f : \mathbb{R}\to\mathbb{C}$ be a function which decays sufficiently rapidly at infinity such that the integral
$$\mathcal{F}(f)(k) = \frac{1}{\sqrt{2\pi}}\int_{-\infty}^\infty e^{-ikx} f(x) dx $$
converges. Then $\hat{f}(k) = \mathcal{F}(f)(k)$ is called the <i>Fourier transform</i> of $f$.
</div>

Conceptually, this should be thought of as a continuous analogue of Fourier series. In the study of Fourier series, we found two ways of representing a $2L$-periodic function by a Fourier series. One was with sines and cosines, but the other was with complex exponentials. The representation in terms of complex exponentials is 

$$f(x) = \sum_{n=-\infty}^\infty c_n e^{in\pi x/L} ,$$

where the coefficients $c_n$ are given by 

$$c_n = \frac{1}{L}\int_{-L}^L f(x) \e^{-in\pi x/L} dx.$$

Our interpretation for the coefficients $c_n$ was that they represent the *amount* of the frequency $k_n = n\pi/L$ that the function $f$ contained. We note that the bigger $L$ gets, the finer spaced the $k_n$ values are; we can allow for higher frequencies. Allowing for higher frequencies allows us to expand functions with *less* periodicity, by which we mean functions with longer periods. If we consider making the period infinitely long, it would mean that $k_n$ can take on any real value, instead of just integers multiplied by $\pi/L$. We are thus led to consider the *continuous variable* $k$, which would give us something like 

$$c_k = \frac{1}{L}\int_{-L}^L f(x) \e^{-ikx} dx.$$

We can see that this formula for $c_k$ coincides with $\hat{f}(k) = \mathcal{F}(f)(k)$. Thus this leads naturally to our interpretation for the Fourier transform of a function. The Fourier transform $\hat{f}(k)$ of a function $f(x)$ is, as before, the amount of frequency $k$ contained in the original function $f$. 

There are certain functions whose Fourier transforms will be frequently used. These will be collected in a table. To understand where these come from, we will start by calculating some elementary examples. 

### Exercises

<ol>
<li> <div> Sketch all of the points such that \(y = 1\). </div>

<button onclick="myFunction('answer2')" class="answerButton">Show Answer</button>
<div  id="answer2" class="answer">
This is a plane that is parallel to the \(xz\) plane. 
</div> </li>
<li> <div> Sketch all of the points such that \(y = 1\). </div>

<button onclick="myFunction('answer2')" class="answerButton">Show Answer</button>
<div  id="answer2" class="answer">
This is a plane that is parallel to the \(xz\) plane. 
</div> </li>
</ol>
