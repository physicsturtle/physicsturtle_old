---
layout: lesson
title: Fourier Transforms
dept: physics
course: many-body-II
unit: unit35
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 35
---
The Fourier transform is used everywhere in condensed matter physics, and there are various conventions with which it is used. Here, we will set our conventions for these notes, and give definitions for the different kinds of Fourier transforms and classify the types of functions that can be transformed. I will introduce the transforms with a more mathematical notation, but I will also write the physics notation so that you can connect the ideas.

There are 4 different Fourier transforms that we can define, and it is worthwhile to become familiar with all of them. We recall that a Fourier transform takes a function defined on real space and produces a function defined on momentum space. The possibilities here though, are that the real space could be a continuous space, or a discrete space like a lattice. Depending on whether or not this real space is finite or infinite gives us four possibilities. When we classify the functions, instead of describing the space as finite or infinite, we will consider Fourier-transforming functions which are periodic or aperiodic; periodic functions may as well take place on a finite space. This leads us to the four Fourier transforms, which take place on the following four types of functions:

<ol>
	<li> The function is defined on a continuous space, and is aperiodic,
	</li> 
 <li> The function is defined on a discrete space, and is aperiodic.
	</li> 
 <li> The function is defined on a continuous space, and is periodic,
	</li> 
 <li> The function is defined on a discrete space, and is periodic,
\end{enumerate}

Each of these four possibilities leads to different properties of the momenta that come out of the Fourier transform.

\subsubsection{Continuous Real Space, Aperiodic Function}
Here we will discuss the Fourier transform of a function \\(f : \RR \to \CC\\), which is aperiodic. This will correspond to the most familiar of the Fourier transforms. The Fourier transform of a function \\(f\\) is defined by

$$$$\begin{align}\hat{f}(k) = \int_{-\infty}^\infty e^{-ikx}f(x) dx\end{align}$$$$

which tells us that the inverse transform is given by

$$$$\begin{align}f(x) = \int_{-\infty}^\infty e^{ikx}\hat{f}(k) \frac{dk}{2\pi}\end{align}$$$$

The momentum space consists of all \\(k\in\RR\\); there can be arbitrarily big or small momenta. Thus the Fourier transform \\(\hat{f}\\) is a function \\(\hat{f} : \RR \to \CC\\). 

Physically, this would correspond to a field defined on all of space, such as the potential field generated by a point charge. 

\subsubsection{Discrete Real Space, Aperiodic Function} 
This time, we discuss the Fourier transform of a function \\(f: a\ZZ\to \CC\\), which is aperiodic. Here, \\(a\\) is some number (like a lattice parameter), and \\(a\ZZ = \{an : n\in \ZZ\}\\). The relevant Fourier transform now is

$$$$\begin{align}\hat{f}(k) = \sum_{n=-\infty}^\infty f(x_n) e^{-ik x_n}\end{align}$$$$

where \\(x_n = an\\), which tells us that the inverse transform is given by

$$$$\begin{align}f(x_n) = \int_{-\pi/a}^{\pi/a} \hat{f}(k)e^{ikx_n} \frac{dk}{2\pi}.\end{align}$$$$

So we see that now \\(k\\) is restricted to \\(k\in [-\pi/a,\pi/a]\\), so \\(\hat{f} : [-\pi/a,\pi/a] \to \CC\\). What this means is that the Fourier transform of an arbitrary function on a lattice is \textit{periodic in momentum space}, with period \\(2\pi/a\\). This is exactly the case of working in the first Brillouin zone. This is probably the most useful transform in solid state physics.

\subsubsection{Continuous Real Space, Periodic Function}
Here we will discuss the Fourier transform of a function \\(f : \RR \to \CC\\) which is periodic with period \\(L\\), so \\(f(x+L) = f(x)\\) for all \\(x\\). Recall that this is equivalent to defining \\(f : [0,L] \to \chat\\); it can be periodically extended to the real line. The relevant Fourier transform is now

$$$$\begin{align}\hat{f}(k_n) = \frac{1}{L}\int_0^{L} f(x)e^{-ik_n x} dx,\end{align}$$$$

where \\(k_n = 2\pi n/L\\). This tells us that the inverse transform is given by

$$$$\begin{align}f(x) = \sum_{n=-\infty}^\infty \hat{f}(k_n)e^{ik_n x}.\end{align}$$$$

This is the case of Fourier series that you studied in your differential equations courses. 






\subsubsection{Discrete Real Space, Periodic Function}
Lastly, we come to the functions defined on a discrete real space (lattice), which are periodic. We again look at a function \\(f : a\ZZ \to \CC\\), which satisfies \\(f(x_n+aN) = f(x_n)\\) (here, \\(x_n = an\\)). Its Fourier transform is then

$$$$\begin{align}\hat{f}(k) = \sum_{n=1}^N f(x_n) e^{-ik x_n }\end{align}$$$$

The inverse Fourier transform is thus

$$$$\begin{align}f(x_i) = \frac{1}{\sqrt{N}}\sum_{n=1}^N \hat{f}(k_n)e^{ik_n x_i}\end{align}$$$$

Thus the \\(k\\)'s take on discrete values. 


\subsection{Examples}
Now, let's work some example calculations to get familiar with the Fourier transform. 

<b>Example:</b>
\textbf{Example:} Verify that 


<b>Example:</b>
\textbf{Example:} Verify that 	

