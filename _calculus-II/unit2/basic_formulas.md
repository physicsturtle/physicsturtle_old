---
layout: lesson
title: Basic Formulas
dept: math
unit: unit2
course: calculus-II
deptDisplay: Math
unitDisplay: Unit 2
courseDisplay: Calculus II
---

Integration, or, the inverse operation of differentiation, is in general more difficult than differentiation. Differentiation has a very formulaic procedure; one can use the product and chain rules to differentiate any elementary function! However, when we work with integrals, the techniques are much more varied! Although all methods can be thought of in terms of reversing the chain rule or product rule, sometimes realizing what needs to be done is much more subtle. Thus, we start our discussion of the techniques of integration with the integrals that can be derived directly from a table of derivatives! 

In this section, we will discuss the basic formulas for integration, all of which should be memorized. We recall the table of derivatives, which I will write in a different form than usual so that it can be more easily inverted to make a table of integrals (aka antiderivatives). The table of derivatives is the following. 

#### Table of Derivatives:

$$\begin{eqnarray*}
\frac{d}{dx} x^{n+1} &=& (n+1) x^n \\
\frac{d}{dx} (-\cos x) &=& \sin x \\
\frac{d}{dx}\sin x &=& \cos x \\
\frac{d}{dx} \arctan x &=& \frac{1}{1+x^2} \\
\frac{d}{dx} e^x &=& e^x \\
\frac{d}{dx}\log|x| &=& \frac{1}{x} \\
\end{eqnarray*}$$

This table can be inverted to produce a table of integrals! By inverted, I mean getting rid of the differentiation sign, and adding an integral sign to the other side! The resulting table of integrals is 

#### Table of Integrals:

$$\begin{eqnarray*}
\int x^n dx &=& \frac{x^{n+1}}{n+1} ,\qquad (n\not=-1)\\
\int \sin x dx &=& -\cos x \\
\int \cos x dx &=& \sin x \\
\int \frac{dx}{1+x^2} &=& \arctan x \\
\int e^x dx &=& e^x \\
\int \frac{dx}{x} &=& \log|x| 
\end{eqnarray*}$$

In the following sections, it will frequently be necessary to reduce complicated integrals into one of the above forms. This is why it is important to commit these to memory; it will greatly speed up your computations to have certain common formulas memorized.
