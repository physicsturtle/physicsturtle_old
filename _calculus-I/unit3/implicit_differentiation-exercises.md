---
layout: lesson
title: Implicit Differentiation - Exercises
dept: math
course: calculus-I
unit: unit3
deptDisplay: Math
courseDisplay: Calculus I
unitDisplay: Unit 3
---

\question[$**$] Given $x^2y - xy^2+x^2+y^2=0$,
\begin{enumerate}[(a)]
\item Regarding $y$ as a function of $x$, compute $\displaystyle{\frac{dy}{dx}}$. \\
\item Compute a linear approximation to this graph at the point $(1,-1).$ 
\end{enumerate}

\begin{solution}[190mm]
\begin{enumerate}[(a)]
\item
Use implicit differentiation:
Let's find the derivative of each term separately, then add them all together. First the derivative of the first summand:
\[[x^2y]' = (2x)(y)+(x^2)(y') = 2xy+y'x^2\]
Derivative of the second summand:
\[[xy^2]' = (1)(y^2)+(x)(2yy') = y^2+2xyy'\]
Derivative of the third summand:
\[[x^2]' = 2x\]
Derivative of the last summand:
\[[y^2]' = 2yy'\]
Adding all of the summands together:
\[0=2xy+x^2y'-y^2-2xyy'+2x+2yy'\]
Solving for $y'$:
\[-x^2y'+2xyy'-2yy'=2xy-y^2+2x\]
\[y'=\frac{2xy-y^2+2x}{-x^2+2xy-2y}\]
\item
We must evaluate $y'$ at the point $(1,-1)$. It is $y'(1,-1) = 1$
Then the linear approximation is \[L(x) = -1 + 1(x-1) = x-2\]
\end{enumerate}
\end{solution}

\question[$***$] Considering $y$ as a function of $x$, compute $\displaystyle{\frac{dy}{dx}}$ and $\displaystyle{\frac{d^2y}{dx^2}}$.  \[x^2 - xy + y^2 = 3\]

\begin{solution}[200mm]
Use implicit differentiation to find both the first and second derivative.

$$\frac{d}{dx}[x^2-xy+y^2]=\frac{d}{dx}[3]$$

\begin{eqnarray*}
2x-(y+xy')+2yy'&=&0\\
2x-y-xy'+2yy'&=&0\\
2x-y&=&xy'=2yy'\\
y'&=&\frac{2x-y}{x-2y}\\
\end{eqnarray*}

Now for the second derivative: Note that will have to plug the first derivative into the formula for the second derivative.
\begin{eqnarray*}
y'' &=& \frac{d}{dx}[y']\\
&=& \left[\frac{2x-y}{x-2y}\right]\\
&=& \frac{(2-y')(x-2y)-(2x-y)(1-2y')}{(x-2y)^2}\\
&=&\frac{2x-4y-xy'+2yy'-(2x-4xy'-y+2yy')}{(x-2y)^2}\\
&=&\frac{-3y+3xy'}{(x-2y)^2}\\
&=&\frac{3(xy'-y)}{(x-2y)^2}\\
&=& \frac{3\left(x\left(\frac{2x-y}{x-2y}\right)-y\right)}{(x-2y)^2}\\
&=&  \frac{3\left(x\left(\frac{2x-y}{x-2y}\right)-y\right)}{(x-2y)^2} \\
&=& \frac{3\left(\frac{x(2x-y)}{x-2y} - \frac{y(x-2y)}{x-2y}\right)}{(x-2y)^2} \\
y'' &=&\frac{6(x^2+y^2-xy)}{(x-2y)^3}
\end{eqnarray*}

\end{solution}

\question[$**$] Prove that the two curves intersect at right angles at the origin. 
\begin{enumerate}[(i)]
\item $5y - 2x + y^3 - x^2y = 0$ 
\item $2y + 5x + x^4 - x^3y^2 = 0$
\end{enumerate}

\begin{solution}[200mm]
Since plugging $(0,0)$ into both (i) and (ii) satisfies the equation, we know that both curves pass through the origin. 

\begin{enumerate}[(i)]
\item
\begin{eqnarray*}
\frac{d}{dx}[5y-2x+y^3-x^2y] &=& \frac{d}{dx}[0]\\
5y'-2+3y^2y'-(2xy+x^2y') &=& 0\\
5y'+3y^2y'-x^2y'-2-2xy &=& 0 \\
y'(5+3y^2-x^2)&=&2+2xy \\
y' &=& \frac{2+2xy}{5+3y^2-x^2} \\
\end{eqnarray*}
Evaluating at $x = 0$, we have 
\[y'(0) =\frac{2+2\cdot 0 \cdot 0}{5+3\cdot 0 -0}=\frac{2}{5}\]
\item
\begin{eqnarray*}
\frac{d}{dx}[2y+5x+x^4-x^3y^2] &=& \frac{d}{dx}[0]\\
2y'+5+4x^3-(3x^2y^2+x^3\cdot 2yy') &=& 0\\
2y'-2x^3yy'+5+4x^3-3x^2y^2 &=& 0\\
y'(2-2x^3y) &=& 3x^2y^2-5-4x^3 \\
y' &=& \frac{3x^2y^2-5-4x^3}{2-2x^3y} \\
\end{eqnarray*}
Evaluating at $x = 0$ we have \[y'(0) =\frac{-5}{2}\]
\end{enumerate}

Both equations pass through the origin and each equation's slope at the origin is the negative reciprocal of the other, therefore they are perpendicular.\\
\\
\end{solution}

\question[$**$] If $\sin y + \cos x = 1$, compute $y''$ by using implicit differentiation. 

\begin{solution}[100mm]
\begin{eqnarray*}
\frac{d}{dx}[1] &=& \frac{d}{dx}[\sin y] + \frac{d}{dx}[\cos x] \\
0 &=& \cos(y)\cdot y'-\sin(x) \\
y' &=& \frac{\sin(x)}{\cos(y)}
\end{eqnarray*}
\begin{center}\textrm{Now use the quotient rule to get the second derivative}\end{center}
\begin{eqnarray*}
y'' &=& \frac{(\sin(x))'(\cos(y))-(\sin(x))(\cos(y))'}{\cos^2(y)}\\
y'' &=& \frac{\cos(x) \cdot \cos(y) - \sin(x) \cdot (-\sin(y)\cdot y')}{\cos^2(y)}\\
y'' &=& \frac{\cos(x) \cdot \cos(y) + \sin(x)\sin(y)\cdot \frac{\sin(x)}{\cos(y)})}{\cos^2(y)}\\
y'' &=& \frac{\cos(x)}{\cos(y)} + \frac{\sin^2(x)\sin(y)}{\cos^3(y)}\\
y'' &=& \frac{\cos(x)}{\cos(y)} + \frac{\sin^2(x)\tan(y)}{\cos^2(y)}
\end{eqnarray*}
\end{solution}

\question[$***$] Regarding $y$ as a function of $x$, compute $y'$:
\[x\cos y =\sin(x+y)\]

\begin{solution}[95mm]
First, use the identity $\sin(u\pm v) = \sin(u)\cos(v) \pm \cos(u)\sin(v)$ , then use the product rule for each of the three terms.
\[x \cos(y) = \sin(x) \cos(y) + \cos(x) \sin(y)\]
Now differentiating each term. First we differentiate the left hand side:
\begin{eqnarray*}
\frac{dy}{dx}[x\cos(y)] &=& \cos(y) +x(-\sin(y) y')  \\
&=& \cos(y)-xy'\sin(y)\\
\end{eqnarray*}
Now we differentiate the first summand on the right hand side:
\begin{eqnarray*}
\frac{dy}{dx}[\sin(x)\cos(y)] &=& \cos(x)\cos(y) + \sin(x) (-\sin(y) \cdot y') \\
&=& \cos(x)\cos(y)-\sin(x)\sin(y)y'\\ 
\end{eqnarray*}
Now we differentiate the second summand on the right hand side:
\begin{eqnarray*}
\frac{dy}{dx}[\cos(x)\sin(y)] &=& -\sin(x)\sin(y) +\cos(x)(\cos(y)y')\\
&=& \cos(x)\cos(y)y' - \sin(x)\sin(y)
\end{eqnarray*}
Adding it all up
\[\cos(y)-xy'\sin(y) = \cos(x)\cos(y) - \sin(x)\sin(y)y' +\cos(x)\cos(y)y' - \sin(x)\sin(y)\]
Rearranging all of the $y'$ terms on one side:
\[\cos(y)-\cos(x)\cos(y) + \sin(x)\sin(y) = \cos(x)\cos(y)y' - \sin(x)\sin(y)y' +x\sin(y)y'\]
Finally solving for $y'$:
\[y' = \frac{\cos(y)-\cos(x)\cos(y) + \sin(x)\sin(y)}{\cos(x)\cos(y) - \sin(x)\sin(y) +x\sin(y)}\] 

\end{solution}
