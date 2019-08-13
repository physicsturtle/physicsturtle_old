---
layout: exercises
title: Trigonometric Substitution - Exercises
dept: math
unit: unit2
course: calculus-II
deptDisplay: Math
unitDisplay: Unit 2
courseDisplay: Calculus II
---




<ol>
<li><div class="exercise"> Evaluate the integral. \[\int\frac{dx}{(9+x^2)^2}\]

<div class="answerBox">
<button onclick="myFunction('answer1')" class="answerButton">Show Answer</button>
<div  id="answer1" class="answer" >
We recognize this as the form of a trigonometric substitution integral, so let $x = 3\tan z$, and $dx = 3\sec^2zdz$.
\begin{eqnarray*}
\int \frac{3\sec^2zdz}{(9 + 9\tan^2z)^2} &=& \frac{1}{27}\int \frac{1}{\sec^2z}dz \\
& =& \frac{1}{27}\int \cos^2zdz \\
&=& \frac{1}{54}\int 1 + \cos 2zdz \\
&=& \frac{1}{54}\left( z + \frac{\sin 2z}{2} \right) \\
&=& \frac{1}{54}\left( \arctan \left( \frac{x}{3}\right) + \sin z\cos z \right)\\
&=& \frac{1}{54}\left( \arctan \left( \frac{x}{3} \right) + \sin z\cos z\right) \\
&=& \frac{1}{54}\left( \arctan \left( \frac{x}{3} \right) + \frac{3x}{x^2 + 9} \right) + C\\
\end{eqnarray*}
The final answer is then
\[\int \frac{dx}{(9 + x^2)^2}  = \frac{1}{54}\arctan \left( \frac{x}{3} \right) + \frac{x}{18(x^2 + 9)} + C\]
</div>
</div>
</div>
</li>


<li><div class="exercise"> Evaluate the integral
\[\int x\sqrt{1-x^4} dx\]

<div class="answerBox">
<button onclick="myFunction('answer2')" class="answerButton">Show Answer</button>
<div  id="answer2" class="answer" >
Let $x^2 = \sin\theta$, and $2xdx = \cos\theta d\theta$. Then the integral becomes
\begin{eqnarray*}
\int x\sqrt{1-x^4} dx &=& \frac{1}{2}\int \sqrt{1-\sin^2\theta}\cos\theta d\theta\\
&=&\frac{1}{2}\int \cos^2\theta d\theta \\
&=& \frac{1}{2}\int\frac{1+\cos 2\theta}{2} d\theta\\
&=& \frac{\theta}{4} + \frac{\sin 2\theta}{8} + C\\
&=& \frac{\theta}{4} + \frac{\sin\theta\cos\theta}{4} + C
\end{eqnarray*}
Now plugging back in the original variables we have
\[\int x\sqrt{1-x^4} dx = \frac{\arcsin(x^2)}{4} + \frac{x^2\sqrt{1-x^4}}{4} + C\]
</div>
</div>
</div>
</li>



<li><div class="exercise"> Evaluate the integral. 
\[\int \frac{(16-9x^2)^{3/2}}{x^6} dx\]

<div class="answerBox">
<button onclick="myFunction('answer3')" class="answerButton">Show Answer</button>
<div  id="answer3" class="answer" >
Let $x = \frac{4}{3}\sin \theta$, so $dx = \frac{4}{3}\cos \theta d\theta$. Thus the integral becomes
\begin{eqnarray*}
\int \frac{(16 - 9x^2)^{3/2}}{x^6} dx &=& \int \frac{64\cos^3\theta}{\frac{4^6}{3^6}\sin^6\theta}\frac{4}{3}\cos \theta d\theta \\
&=& \frac{3^5}{2^4}\int \cot ^4\theta \csc^2\theta d\theta \\
\end{eqnarray*}
Now we make a second substitution. Let $\cot \theta = u$, so $du =  - \csc^2\theta d\theta$. Then we have the greatly simplified integral
\begin{eqnarray*}
\frac{3^5}{2^4}\int \cot ^4\theta \csc^2\theta d\theta&=&  - \frac{3^5}{2^4}\int u^4du \\
&=&  - \frac{3^5}{2^4}\frac{u^5}{5} + C\\
&=&  - \frac{3^5}{2^4}\frac{\cot^5\theta }{5} + C \\
&=&  - \frac{3^5}{2^4}\frac{1}{5}\left( \frac{\sqrt{16 - 9x^2}}{3x} \right)^5 + C \\
&=&  - \frac{1}{80}\frac{(16 - 9x^2)^{5/2}}{x^5} + C\\
\end{eqnarray*}
This leaves us with the final answer
\[\int \frac{(16 - 9x^2)^{3/2}}{x^6}dx =  - \frac{1}{80}\frac{(16 - 9x^2)^{5/2}}{x^5} + C\]
</div>
</div>
</div>
</li>




<li><div class="exercise"> Evaluate the integral. The attached table may be useful.
\[\int^{\pi/2}_0 \frac{\cos\theta}{\sqrt{1+\sin^2\theta}} d\theta\]

<div class="answerBox">
<button onclick="myFunction('answer4')" class="answerButton">Show Answer</button>
<div  id="answer4" class="answer" >
Let $\sin\theta = u$, and $du = \cos\theta d\theta$. Then we have the integral
\[\int^{\pi/2}_0 \frac{\cos\theta}{\sqrt{1+\sin^2\theta}} d\theta = \int_0^1 \frac{du}{\sqrt{1+u^2}}\]
Let $u = \tan\varphi$, $du = \sec^2\varphi d\varphi$. Then the integral is now
\[\int_0^1 \frac{du}{\sqrt{1+u^2}} = \int_0^{\pi/4} \sec \varphi d\varphi\]
By the secant example, we have
\[\int_0^{\pi/4} \sec \varphi d\varphi = \left.\left(\log|\sec\varphi + \tan\varphi|\right)\right|^{\pi/4}_0\]
</div>
</div>
</div>
</li>




<li><div class="exercise"> Evaluate the integral. The attached table may be useful. \[\int\frac{dx}{x\sqrt{9+4x^2}}\]

<div class="answerBox">
<button onclick="myFunction('answer5')" class="answerButton">Show Answer</button>
<div  id="answer5" class="answer" >
To evaluate this integral we recognize it as the form of a trigonometric substitution. Let $x = \frac{3}{2}\tan z$, and $dx = \frac{3}{2}\sec^2z dz$. Note that we will have to evaluate the integral of $\csc$ along the way for this problem. You may use the attached table, but we will show the steps to evaluate the $\csc$ integral regardless.
\begin{eqnarray*}
\int \frac{\sec^2z}{\tan z\sqrt{9 + 9\tan^2z}}dz  &=& \frac{1}{3}\int\frac{\sec z}{\tan z}dz \\
&=& \frac{1}{3}\int \frac{1}{\sin z}dz \\
&=& \frac{1}{3}\int \frac{\sin z}{\sin^2z}dz  = \frac{1}{3}\int \frac{\sin z}{1 - \cos^2z}dz 
\end{eqnarray*}
Now we have to set this up for a partial fraction decomposition:
Let $\cos z = u$, and $du =  - \sin zdz$
\begin{eqnarray*}
- \frac{1}{3}\int \frac{1}{1 - u^2} du &=&  - \frac{1}{6}\int \frac{1}{1+u} + \frac{1}{1-u}du \\
&=& \frac{-1}{6}\log \left| \frac{1 + u}{1 - u} \right| \\
&=& \frac{1}{6}\log \left| \frac{1 - u}{1 + u} \right| \\
&=& \frac{1}{6}\log \left| \frac{1 - \cos z}{1 + \cos z} \right| \\
&=& \frac{1}{6}\log \left| \frac{1 - \cos z}{1 + \cos z}\left( \frac{1 - \cos z}{1 - \cos z} \right) \right|\\
&=& \frac{1}{6}\log \left| \frac{(1 - \cos z)^2}{\sin^2z} \right|\\
&=& \frac{1}{3}\log \left| \frac{1 - \cos z}{\sin z} \right|\\
&=& \frac{1}{3}\log \left| \csc z - \cot z \right| + C \\
&=& \frac{1}{3}\log \left| \frac{\sqrt{9 + 4x^2}  - 3}{x} \right| + C\\
\end{eqnarray*}
Thus our final answer is
\[\int \frac{dx}{x\sqrt{9 + 4x^2}}  = \frac{1}{3}\log \left| \frac{\sqrt{9 + 4x^2}  - 3}{x} \right| + C\]
</div>
</div>
</div>
</li>




<li><div class="exercise">Evaluate the integral. The attached table may be useful. \[\int \frac{x^2}{\sqrt{x^2-16}} dx\]

<div class="answerBox">
<button onclick="myFunction('answer6')" class="answerButton">Show Answer</button>
<div  id="answer6" class="answer" >
Let $x = 4\sec \theta$, so $dx = 4\sec \theta \tan \theta d\theta$. Then the integral is transformed to
\[\int \frac{x^2}{\sqrt{x^2-16}} dx = 16\int \sec^3\theta d\theta \]
Need to evaluate integral of $\sec^3x$:
\[\int \sec^3\theta d\theta  = \int \sec \theta \sec^2\theta d\theta \]
We will integrate this by parts:
Let $\sec \theta  = u$, so $\sec ^2\theta  = v'$ and  $u' = \sec \theta \tan \theta$, $v = \tan \theta$.
\begin{eqnarray*}
\int \sec \theta \sec^2\theta d\theta  &=& \sec \theta \tan \theta  - \int \tan^2\theta \sec \theta d\theta \\
&=& \sec \theta \tan \theta  - \int (\sec^2\theta  - 1)\sec \theta d\theta  \\
&=& \sec \theta \tan \theta  - \int \sec^3\theta d\theta  + \int \sec \theta d\theta \\
\end{eqnarray*}
Now we move the integral of $\sec^3$ to the other side.
\begin{eqnarray*}
2\int \sec^3\theta d\theta  &=& \sec \theta \tan \theta  + \int\sec \theta d\theta  \\
&=& \sec \theta \tan \theta  + \log \left| \sec \theta  + \tan \theta  \right| \\
\end{eqnarray*}
Now dividing through by 2, 
\[\int \sec^3\theta d\theta = \frac{1}{2}\left( \sec \theta \tan \theta  + \log \left| \sec \theta  + \tan \theta  \right| \right) + C\]
Finally, multiplying by 16 to make it just like the original integral from the beginning of the solution, 
\begin{eqnarray*}
16\int \sec^3\theta d\theta  &=& 8\sec \theta \tan \theta  + 8\log \left| \sec \theta  + \tan \theta \right|\\
&=&\frac{1}{2}x\sqrt{x^2 - 16}  + 8\log \left| x + \sqrt{x^2 - 16} \right| + C\\
\end{eqnarray*}
\[\int \frac{x^2}{\sqrt{x^2 - 16}}dx  = \frac{1}{2}x\sqrt{x^2 - 16}  + 8\log \left| x + \sqrt{x^2 - 16}\right| + C\]
</div>
</div>
</div>
</li>




<li><div class="exercise"> Evaluate the integral \[\int \frac{\sqrt{9-4x^2}}{x} dx\]

<div class="answerBox">
<button onclick="myFunction('answer7')" class="answerButton">Show Answer</button>
<div  id="answer7" class="answer" >
Let $x = \frac{3}{2}\sin z$ and $dx = \frac{3}{2}\cos zdz$
\begin{eqnarray*}
\int \frac{\sqrt{9 - 4x^2}}{x}dx  &=& \int \frac{\cos z\sqrt{9 - 9\sin^2z}}{\sin z}dz  \\
&=& 3\int \frac{\cos z\sqrt{1 - \sin^2z}}{\sin z}dz \\
&=& 3\int \frac{\cos^2z}{\sin z}dz  \\
&=& 3\int \csc z - \sin zdz  \\
&=&  - 3\log \left| \csc z + \cot z \right| + 3\cos z + C\\
&=&  - 3\log \left|\frac{3}{2x} + \frac{\sqrt{9 - 4x^2}}{2x} \right| + \sqrt{9 - 4x^2}  + C\\
&=& \sqrt{9 - 4x^2}  - 3\log \left| \frac{3}{x} + \frac{\sqrt{9 - 4x^2}}{x} \right| + C
\end{eqnarray*}
</div>
</div>
</div>
</li>




<li><div class="exercise">Evaluate the integral. \[\int \frac{dx}{(4x^2-24x+27)^{3/2}}\]

<div class="answerBox">
<button onclick="myFunction('answer8')" class="answerButton">Show Answer</button>
<div  id="answer8" class="answer" >
\[\int \frac{dx}{(4x^2 - 24x + 27)^{3/2}}  = \int \frac{dx}{(4(x - 3)^2 - 9)^{3/2}}\]
Let $2(x - 3) = 3\sec z$ and $2dx = 3\sec z\tan z dz$. 
\begin{eqnarray*}
\int \frac{dx}{(4x^2 - 24x + 27)^{3/2}}  &=& \frac{3}{2}\int \frac{\sec z\tan zdz}{\left( 9\sec^2z - 9\right)^{3/2}}\\
&=& \frac{1}{18}\int \frac{\sec z\tan z}{\tan^3z}dz \\
&=& \frac{1}{18}\int \frac{\sec z}{\tan^2z}dz  \\
&=& \frac{1}{18}\int \cot z\csc zdz  = \frac{1}{18}( - \csc z) + C\\
&=& \frac{ -1}{18\sin z} + C \\
&=& \frac{2(3 - x)}{18\sqrt{4x^2 - 24x + 27}} + C\\
\end{eqnarray*}
The final answer is then
\[\int \frac{dx}{(4x^2 - 24x + 27)^{3/2}}  = \frac{3 - x}{9\sqrt{4x^2 - 24x + 27}} + C\]
</div>
</div>
</div>
</li>

</ol>
