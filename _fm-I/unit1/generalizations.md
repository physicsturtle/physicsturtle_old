---
layout: lesson
dept: physics
title: Generalizations
course: cm-III
unit: unit1
deptDisplay: Physics
courseDisplay: Classical Mechanics III
unitDisplay: Unit 1
---

Next, we will discuss what happens when there are 2 or more dependent variables; the number of independent variables, 1, remains the same.

### Multiple Dependent Variables
Here, we concern ourselves with finding stationary points of functionals of the form
$$S[x,y] = \int_{t_!}^{t_2} \L(t,x,y,\dot{x},\dot{y}) dt.$$

In order to derive the Euler-Lagrange equation, we need to consider multiple variations, 

$$\begin{cases}
x(t) = x_*(t) + \epsilon\eta_1(t),
y(t) = y_*(t) + \epsilon\eta_2(t).
\end{cases}$$

where we have the same parameter $\epsilon$ for both variations but potentially different functions $\eta_1$ and $\eta_2$. We again impose the condition
$$\frac{dS}{d\epsilon}\bigg|_{\epsilon = 0} = 0,$$

and look at what the Euler-Lagrange equation becomes. This derivation is very similar to the one from the single variable case and it is left to the exercises. The result is actually two Euler-Lagrange equations, 

$$\frac{\partial\L}{\partial x} = \frac{d}{dt}\frac{\partial\L}{\partial\dot{x}},\qquad \frac{\partial \L}{\partial y } = \frac{d}{dt}\frac{\partial\L}{\partial\dot{y}}.$$

In general this result can be generalized:

<div class="result">
<b>Result:</b> Suppose we have a functional of $n$ dependent variables, $q_1,q_2,\dots,q_n$. 
$$S[q_1,q_2,\dots, q_n] = \int_{t_1}^{t_2}\L(t,q_1,q_2,\dots,q_n,\dot{q}_1,\dot{q}_2,\dots,\dot{q}_n) dt$$

Then for each variable, we have the Euler-Lagrange equation

$$\frac{\partial\L}{\partial q_i} = \frac{d}{dt}\frac{\partial \L}{\partial \dot{q}_i},\qquad i = 1,2,\dots,n$$
</div>

### Constrained Systems
We also consider constrained optimization. By this, we mean that we aim to optimize the functional

$$S[x] = \int_{t_1}^{t_2}\L(t,x,\dot{x}) dt,$$

where the function $x$ must satisfy the requirement 

$$C = \int_{t_1}^{t_2}\mathcal{M}(t,x,\dot{x}) dt,$$

where $C$ is a constant. This should remind you of Lagrange multipliers. The method of Lagrange multipliers is exactly what we will use here. Recall that in multivariable calculus, if we aimed to optimize a function $f$ of $n$ variables $f(x_1,x_2,\dots,x_n)$ subject to $m$ constraints $g_1(x_1,x_2,\dots,x_n) = c_1, g_2(x_1,x_2,\dots,x_n)= c_2,\dots,g_m(x_1,x_2,\dots,x_n)=c_m$ where $m < n$, then we solve $m+n$ equations 

$$\begin{cases}
\nabla(f+\lambda_1 g_1 + \lambda_2 g_2 + \cdots + \lambda_m g_m) = 0\\
g_1(x_1,x_2,\dots,x_n) = c_1 \\
g_2(x_1,x_2,\dots,x_n) = c_2 \\
\vdots \\
g_m(x_1,x_2,\dots,x_n) = c_m 
\end{cases}$$

In the calculus of variations, we consider the exact same thing. Here, we consider the functional

$$S[x] + \lambda C[x] = \int_{t_1}^{t_2}\left(\L(t,x,\dot{x}) + \lambda \mathcal{M}(t,x,\dot{x})\right) dt$$

and then plug the resulting combined Lagrangian $\L(t,x,\dot{x}) + \lambda \mathcal{M}(t,x,\dot{x})$ into the Euler-Lagrange equation. This will have two constants of integration, along with the Lagrange multiplier, which makes for two equations in three unknowns. The constraint provides the third equation for the third unknown. To derive the Euler-Lagrange equation for this system, we first note that making a variation $x = x_\* + \epsilon\eta$ will disrupt the constraint! If we aim to minimize $S$ with a one parameter family of variations, then it cannot be true that $C$ is maintained constant as $\epsilon$ is varied. Thus, we must introduce a two parameter family 

$$x = x_* + \epsilon_1 \eta_1 + \epsilon_2 \eta_2$$

so that the values of $\epsilon_1$ and $\epsilon_2$ can work together to keep $C$ constant. We consider plugging $x$ into combined functional 

$$J(\epsilon_1,\epsilon_2) = S[x_* + \epsilon_1 \eta_1 + \epsilon_2 \eta_2] + \lambda C[x_* + \epsilon_1 \eta_1 + \epsilon_2 \eta_2],$$ 

and then impose the conditions 

$$\frac{\partial J}{\partial\epsilon_1}\bigg|_{\epsilon_1 = \epsilon_2 = 0} ,\qquad \frac{\partial J}{\partial\epsilon_2}\bigg|_{\epsilon_1 = \epsilon_2 = 0}.$$

Now, we differentiate both sides with respect to $\epsilon_i$, where $i = 1,2$. Note that differentiating with respect to either $\epsilon_1$ or $\epsilon_2$ will give us analogous expressions.

$$\frac{\partial J}{\partial\epsilon_i} = \int_{t_1}^{t_2} $$










