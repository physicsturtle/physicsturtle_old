---
layout: lesson
title: Definition of the Derivative
dept: math
course: calculus-I
unit: unit3
deptDisplay: Math
courseDisplay: Calculus I
unitDisplay: Unit 3
---

\question[$**$] Suppose $f(x)$ is differentiable at $x = a$. Find the value of the limit in terms of $f'(a)$:
\[\lim_{x\to a}\frac{f(x) - f(a)}{\sqrt{x} - \sqrt{a}}\]

\begin{solution}[60 mm]
First, notice that the limit is very similar to the definition of the derivative.\\ Multiply both numerator and denominator by $\sqrt{x}+\sqrt{a}$ to obtain the form of the definition of the derivative.\\
\begin{eqnarray*}
\lim_{x\to a}\frac{f(x) - f(a)}{\sqrt{x} - \sqrt{a}} \cdot \frac{\sqrt{x}+\sqrt{a}}{\sqrt{x}+\sqrt{a}} &=& \lim_{x\to a}\frac{f(x) - f(a)}{x - a} \cdot (\sqrt{x}+\sqrt{a})\\
\end{eqnarray*}
Next, use the property of the limits to separate the limit into two.
\begin{eqnarray*}
\lim_{x\to a}\frac{f(x) - f(a)}{x - a} \cdot (\sqrt{x}+\sqrt{a}) &=& \lim_{x\to a}\frac{f(x) - f(a)}{x - a} \cdot \lim_{x\to a}(\sqrt{x}+\sqrt{a})\\
&=& f'(a) \cdot \lim_{x\to a}(\sqrt{x}+\sqrt{a})\\
&=& f'(a) \cdot 2\sqrt{a}\\
\end{eqnarray*}
\end{solution}


\question[$**$] Compute the derivative of $\displaystyle{y = \sqrt{5x + 1}}$ using the definition of the derivative. 
\begin{solution}[140 mm]
\begin{eqnarray*}
y' &=& \lim_{h \to 0} \frac{\sqrt{5(x+h) + 1} - \sqrt{5x + 1}}{h}\\
&=& \lim_{h \to 0} \frac{(\sqrt{5(x+h) + 1} - \sqrt{5x + 1})(\sqrt{5(x+h) + 1} + \sqrt{5x + 1})}{h(\sqrt{5(x+h) + 1} + \sqrt{5x + 1})}\\
&=& \lim_{h \to 0} \frac{5x + 5h + 1 - 5x - 1}{h(\sqrt{5(x+h) + 1} + \sqrt{5x + 1})}\\
&=& \lim_{h \to 0} \frac{5h}{h(\sqrt{5(x+h) + 1} + \sqrt{5x + 1})}\\
&=& \lim _{h \to 0} \frac{5}{\sqrt{5(x+h) + 1} + \sqrt{5x + 1}}\\
&=& \frac{5}{2 \sqrt{5x+1}}
\end{eqnarray*}
\end{solution}

\question[$***$] Compute $f'(x)$ using the definition of the derivative if $\displaystyle{f(x)=\frac{\sqrt{x+1}}{x}}$. 
\begin{solution}[150 mm]
\begin{eqnarray*}
f'(x) &=& \lim_{h \to 0} \frac{f(x+h)-f(x)}{h}\\
&=&\lim_{h \to 0} \frac{\frac{\sqrt{x+h+1}}{x+h} - \frac{\sqrt{x+1}}{x}}{h}\\
&=&\lim_{h \to 0} \frac{x\sqrt{x+h+1} - (x+h)\sqrt{x+1}}{xh(x+h)}\\
&=&\lim_{h \to 0}  \frac{x\sqrt{x+h+1} - (x+h)\sqrt{x+1}}{xh(x+h)} \cdot \frac{x\sqrt{x+h+1} + (x+h)\sqrt{x+1}}{x\sqrt{x+h+1} + (x+h)\sqrt{x+1}}\\
&=&\lim_{h \to 0} \frac{x^2(x+h+1)-(x+h)^2(x+1)}{xh(x+h)(x\sqrt{x+h+1} + (x+h)\sqrt{x+1})}\\
&=&\lim_{h \to 0}  \frac{x^3+x^2h+x^2-(x^2+2xh+h^2)(x+1)}{xh(x+h)(x\sqrt{x+h+1} + (x+h)\sqrt{x+1})}\\
&=&\lim_{h \to 0} \frac{x^3+x^2h+x^2-(x^3+2x^2h+xh^2+x^2+2xh+h^2)}{xh(x+h)(x\sqrt{x+h+1} - (x+h)\sqrt{x+1})} \\
&=&\lim_{h \to 0}  \frac{-x^2h-xh^2-2xh-h^2}{xh(x+h)(x\sqrt{x+h+1} + (x+h)\sqrt{x+1})}\\
&=&\lim_{h \to 0}  \frac{-x^2-xh-2x-h}{x(x+h)(x\sqrt{x+h+1} + (x+h)\sqrt{x+1})}\\
&=& \frac{-x^2-2x}{x^2(x\sqrt{x+1} + x\sqrt{x+1})}\\
&=& \frac{-x-2}{x(x\sqrt{x+1} + x\sqrt{x+1})}\\
f'(x) &=& \frac{-x-2}{2x^2\sqrt{x+1}}\\
\end{eqnarray*}

\end{solution}


\question[$**$] For the given function $f(x)$, determine if 
\begin{enumerate}[(a)]
\item $f(x)$ is continuous at $x = 2$, and 
\item if $f(x)$ is differentiable at $x = 2$. 
\end{enumerate}
\[f(x) = \frac{|x-2|-7}{x+4}\]

\begin{solution}[190 mm]
A function is continuous if \[f(a)=\lim_{x\to a}f(x)\]
We can rewrite $f(x)$ in piecewise notation as
\begin{displaymath}
f(x) = \left \{
\begin{array}{lr}
\frac{x-9}{x+4}& , x \geq 2 \\
\frac{-5-x}{x+4} &, x < 2
\end{array}
\right.
\end{displaymath}
\begin{enumerate}[(i)]
\item Right hand side limit:
\begin{eqnarray*}
\lim_{x\to2^+}f(x)&=&\lim_{x\to2^+}\frac{x-9}{x+4}\\
&=&\frac{-7}{6}
\end{eqnarray*}
\item Left hand side limit:
\begin{eqnarray*}
\lim_{x\to2^-}f(x)&=&\lim_{x\to2^-}\frac{-5-x}{x+4}\\
&=&\frac{-7}{6}
\end{eqnarray*}
\end{enumerate}
The lateral limits are equal to each other and to $f(2)$, therefore $f(x)$ is continuous at $x = 2$

A function is differentiable if $\displaystyle{\lim_{x\to a}\frac{f(x)-f(a)}{x-a}}$ exists and $f$ is continuous at $a$. We already know that $f$ is continuous at $x = a$. Here, $a=2$ and $\displaystyle{f(2)=\frac{-7}{6}}$
\begin{enumerate}[(i)]
\item Differentiability from the right:
\begin{eqnarray*}
\lim_{x\to2^+}\frac{\frac{x-9}{x+4}-(-\frac{7}{6})}{x-2^+}&=& \lim_{x\to2^+}\frac{\frac{6}{6}\cdot\frac{x-9}{x+4}+\frac{x+4}{x+4}\cdot\frac{7}{6}}{x-2}\\
&=&\lim_{x\to2^+}\frac{\frac{6x-54}{6x+24}+\frac{7x+28}{6x+24}}{x-2}\\
&=&\lim_{x\to2^+}\frac{\frac{13x-26}{6x+24}}{x-2}\\
&=&\lim_{x\to2^+}\frac{13x-26}{(6x+24)(x-2)}\\
&=&\lim_{x\to2^+}\frac{13(x-2)}{(6x+24)(x-2)}\\
&=&\lim_{x\to2^+}\frac{13}{6x+24}\\
&=&\frac{13}{36}
\end{eqnarray*}
\item Differentiability from the left:
\begin{eqnarray*}
\lim_{x\to2^-}\frac{\frac{-5-x}{x+4}-(-\frac{7}{6})}{x-2}
&=& \lim_{x\to2^-}\frac{\frac{6}{6}\cdot\frac{-5-x}{x+4}+\frac{x+4}{x+4}\cdot\frac{7}{6}}{x-2}\\
&=&\lim_{x\to2^-}\frac{\frac{-30-6x}{6x+24}+\frac{7x+28}{6x+24}}{x-2} \\
&=&\lim_{x\to2^-}\frac{\frac{x-2}{6x+24}}{x-2}\\
&=&\lim_{x\to2^-}\frac{1}{6x+24}\\
&=&\frac{1}{36}
\end{eqnarray*}
\end{enumerate}
Since \[\frac{13}{36} \not=\frac{1}{36} \] the slopes are unequal and the function is not differentiable at $x = 2$.

\end{solution}
