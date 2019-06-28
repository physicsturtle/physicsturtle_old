---
layout: lesson
title: Quotient Rule
dept: math
course: calculus-I
unit: unit3
deptDisplay: Math
courseDisplay: Calculus I
unitDisplay: Unit 3
---

In this section, we will derive the quotient rule. 

$$\begin{eqnarray*}
\frac{d}{dx}\frac{f(x)}{g(x)} = \lim_{h\to 0} \frac{\frac{f(x+h)}{g(x+h)} - \frac{f(x)}{g(x)}}{h}\\
&=& \lim_{h\to 0} \frac{f(x+h)g(x) - f(x)g(x+h)}{g(x+h)g(x)h}\\
&=& \lim_{h\to 0}\frac{f(x+h)g(x) - f(x) g(x) + f(x)g(x) - f(x)g(x+h)}{f(x+h)g(x)h}\\
&=& \frac{g(x)\lim_{h\to 0}\frac{f(x+h)-f(x)}{h} - f(x)\lim_{h\to 0}\frac{g(x+h) - g(x)}{h}}{\lim_{h\to 0}g(x)g(x+h)}\\
&=& \frac{f'(x)g(x) - f(x)g'(x)}{g(x)^2}
\end{equarray*}$$
