---
layout: exercises
title: Extrema - Exercises
dept: math
course: calculus-I
unit: unit4
deptDisplay: Math
courseDisplay: Calculus I
unitDisplay: Unit 4
---

\question[$*$] Find the minimum and maximum values of the function on the interval $[-2,2]$.
\[f(x) = x^3 - x^2 - 8x + 1\]

\begin{solution}[100mm]
To find the maximum and minimum values, we need to first take a derivative to find the slopes and where the slope switches from positive to negative.
\begin{eqnarray*}
\frac{d}{dx}(x^3-x^2-8x+1) &=& 3x^2-2x-8\\
&=& (3x+4)(x-2)\\
&\Rightarrow& x = {-\frac{4}{3},2}\\
\end{eqnarray*}
Then we test the endpoints and where the slope is 0 to find out which point is the maximum/minimum.
\begin{eqnarray*}
f(-2) &=& (-2)^3-(-2)^2-8(-2)+1\\
&=& -8-4+16+1\\
&=& 5\\
f(-\frac{4}{3}) &=& (-\frac{4}{3})^3-(-\frac{4}{3})^2-8(-\frac{4}{3})+1\\
&=& -\frac{64}{27}-\frac{14}{9}+\frac{32}{3}+1\\
&+& -\frac{64}{27}-\frac{42}{27}-\frac{288}{27}+\frac{27}{27}\\
&=& \frac{209}{27} \Rightarrow Maximum\\
f(2) &+& (2)^3-(2)^2-8(2)+1\\
&=& 8-4-16+1\\
&=& -11 \Rightarrow Minimum\\
\end{eqnarray*}
To confirm the solution, we can simply plug in a value between $-\frac{4}{3}\geq x \leq 2$ into $f'(x)$. I'll use $f'(0)$ for simplicity.\\
\begin{eqnarray*}
f'(0) &=& (3(0)+4)((0)-2)\\
&=& (4)(-2)\\
&=& -8 \Rightarrow Negative\\
\end{eqnarray*}
Seeing that the slope was negative hence decreasing from $-\frac{4}{3}$ to $2$, the calculated values from before are correct.
\end{solution}

\question[$*$] Find the minimum and maximum values of the function on the interval $[-1,1]$.
\[f(x) = x^5 + x + 1\]

\begin{solution}[80mm]
To find the maximum and minimum values, we need to first take a derivative to find the slopes and where the slope switches from positive to negative.
\begin{eqnarray*}
\frac{d}{dx}(x^5+x+1) &=& 5x^4+1\\
\end{eqnarray*}
We should notice that $5x^4+1$ is always positive as it's a quartic function and a positive constant. \\
From this, we can conclude that the minimum and maximum on the given interval is at $x = -1$ and $x = 1$ respectively.\\
To confirm the solution, plug in $x = -1$ and $x = 1$\\
\begin{eqnarray*}
f(-1) &=& (-1)^5+(-1)+1\\
&=& -1 \Rightarrow Minimum\\
f(1) &=& (1)^5+(1)+1\\
&=& 3 \Rightarrow Maximum\\
\end{eqnarray*}
\end{solution}

\question[$**$] Find the minimum and maximum values of the function on the interval $[-\frac{1}{2},1]$.
\[f(x) = \frac{1}{x^5 + x + 1}\]

\begin{solution}[110mm]
To find the minimum and maximum values, we take the derivative of $f(x)$ using the quotient rule to find the critical values where the slope may switch from positive to negative.\\
\begin{eqnarray*}
\frac{d}{dx}(f(x)) &=& \frac{d}{dx}(\frac{1}{x^5+x+1})\\
&=& \frac{\frac{d}{dx}(1)\cdot(x^5+x+1)-1\cdot\frac{d}{dx}(x^5+x+1)}{(x^5+x+1)^2}\\
&=& -\frac{5x^4+1}{(x^5+x+1)^2}\\
\end{eqnarray*}
Analyzing the derivative, we can deduce that the derived function is always negative because the numerator is a second degree function translated upwards and the denominator is a quintic function which is squared.\\
However, we must check the denominator of the original function to ensure it isn't 0 at any point in the domain mentioned. We can check for $x=-\frac{1}{2}$ to see if it's below 0.\\
\begin{eqnarray*}
f(-\frac{1}{2}) &=& \frac{1}{(-\frac{1}{2})^5+(-\frac{1}{2})+1}\\
&=& \frac{1}{-\frac{1}{32}-\frac{16}{32}+\frac{32}{32}}\\
&=& \frac{32}{15}\\
\end{eqnarray*}
We can see that were are no asymptotes or holes within the domain of $[-\frac{1}{2},1]$\\
Thus, the maximum is at $x=-\frac{1}{2}$ and minimum at $x=1$.
\begin{eqnarray*}
f(-\frac{1}{2}) &=& \frac{32}{15}\\
f(1) &=& \frac{1}{(1)^5+(1)+1}\\
&=& \frac{1}{3}\\
\end{eqnarray*}
\end{solution}

\question[$*$] Find the critical numbers of $r(\theta) = 3\theta - \arcsin \theta$.

\begin{solution}[80mm]
Take a derivative and set it to 0 to find the critical numbers.
\begin{eqnarray*}
\frac{d}{d\theta}(r(\theta)) &=& \frac{d}{d\theta}(3\theta-\arcsin\theta)\\
&=& 3-\frac{1}{\sqrt{1-\theta^2}}\\
\theta &=& \pm 1 \enspace for \enspace singular \enspace values\\
&\Rightarrow& Equate \enspace to \enspace 0 \enspace for \enspace critical \enspace values\\
0 &=& 3-\frac{1}{\sqrt{1-\theta^2}}\\
\frac{1}{\sqrt{1-\theta^2}} &=& 3\\
\frac{1}{3} &=& \sqrt{1-\theta^2}\\
\frac{1}{9} &=& 1-\theta^2\\
\theta^2 &=& \frac{8}{9}\\
\theta &=& \pm\frac{2\sqrt{2}}{3} \enspace for \enspace critical \enspace values\\
\end{eqnarray*}
\end{solution}

\question[$**$] Find the global maximum value of $f(x)$ using any method you can think of, you do not need to be rigorous.
\[f(x) = \frac{1}{1+|x|} + \frac{1}{1+|x-a|}\]

\begin{solution}[100mm]
First, we notice that the constituent parts that sum to the function are the smallest when the denominator is the smallest.
We can use the fact that the function behaves similarly to 1/x in terms of growth with some offset from the asymptote. 
Since a is just a constant, the denominator is minimized when the absolute values are 0, hence at $x=0 \enspace and \enspace x=a$.
At both x values, for a given constant a, the output would be equal and are global maximums.
\end{solution}


\question[$**$] For the function $f(x) = e^{-2x^2+4x+3}$, find (if they exist)
\begin{enumerate}[(i)]
\item Critical points
\item Maximum points
\item Minimum points
\item Intervals of increase
\item Intervals of decrease
\item Points of inflection
\item Intervals of concave upward
\item Intervals of concave downward
\item Sketch the function
\end{enumerate}

\begin{solution}
First we calculate the derivatives of $f$:
\[f'(x) = 4(1-x)e^{-2x^2+4x+3}\]
\[f''(x) = 4(4x^2-8x+3)e^{-2x^2+4x+3}\]
\begin{enumerate}[(i)]
\item Critical points: Setting $f'(x) = 0$, we find that $x = 1$ is a critical point of $f$. There are no points where the derivative does not exist, so $x = 1$ is the \textit{only} critical point.
\item Maximum points: Plugging $x = 1$ into $f''$ we obtain
\[f''(1) = -4e^5 < 0\]
this means that $x = 1$ is a maximum of $f$.
\item Minimum points: There are no critical points of $x$ that yield a positive second derivative, so there are no minimum points.
\item Intervals of increase: We solve the inequality $f'(x) > 0$, to find that $x < 1$ is the interval of increase.
\item Intervals of decrease: We solve the inequality $f'(x) < 0$, to find that $x > 1$ is the interval of decrease.
\item Points of inflection: We solve the equation $f''(x) = 0$: This yields $4x^2-8x+3 = 0$, so $x = 1/2, 3/2$. These are the two points of inflection.
\item Intervals of concave upward: We solve the inequality $f''(x) > 0$. This yields $x \in (-\infty,1/2)$, and $x\in(3/2,\infty)$.
\item Intervals of concave downward: We solve the inequality $f''(x) < 0$. This yields $x\in(1/2,3/2)$.
\item Sketch the function:\\
\includegraphics[scale = 0.4]{curveSketch}
\end{enumerate}


\end{solution}
