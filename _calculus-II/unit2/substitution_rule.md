---
layout: lesson
title: Substitution Rule
dept: math
unit: unit2
course: calculus-II
deptDisplay: Math
unitDisplay: Unit 2
courseDisplay: Calculus II
---

In this section, we will discuss the inverse of the chain rule for differentiation. This substitution technique is often called $u$-substitution because that is the most common letter to use. The substitution rule says the following:

$$\int f'(g(x))g'(x) dx = f(g(x))$$

This seems a little bit abstract, so we will do several examples. 

### Examples

<div class="example">
<p><b>Example:</b> Calculate the following integral
$$\int\cos(2x) dx $$ </p>
<b>Solution:</b> We already know how to integrate $\cos x$, but not $\cos 2x$. How can we change this into a form that we recognize? Let's make the substitution $u = 2x$. If we make this substitution, then we also need to change the differential, which gives $du = 2dx$. This means that $dx = \frac{1}{2} du$. Thus, the integral becomes
$$\int\cos(2x) dx = \int\cos u \frac{du}{2}$$
If we just move the $2$ out to the front, then we are integrating a normal cosine! 
$$\frac{1}{2}\int\cos u du = \frac{1}{2}\sin u + C$$
Thus, if we substitute back in our original variable $u = 2x$, we find that

$$\int\cos(2x) dx = \frac{1}{2}\sin(2x) + C$$
</div> <br>



<div class="example">
<p><b>Example:</b> Calculate the following integral
$$\int xe^{x^2} dx $$ </p>
<b>Solution:</b> Here, we recognize that if we make the substitution $u = x^2$ and $du = 2xdx$, then we can substitute in $dx = \frac{du}{2x}$. This will make the extra $x$ cancel out! 
$$\int xe^{x^2} dx = \int x e^{x^2} \frac{du}{2x} = \frac{1}{2}\int e^u du$$
Now, we can integrate the exponential easily!
$$ \frac{1}{2}\int e^u du = \frac{1}{2} e^u + C$$
Lastly, substituting in $u = x^2$, we find that

$$\int xe^{x^2} dx = \frac{1}{2} e^{x^2}$$ 
</div> <br>

You may have started to notice a theme here. If we see a function (in the previous example, $x^2$) and its derivative (in the previous example, $x$), then we can do a $u$-substitution for the function (in the previous example $u = x^2$). Obviously $x$ is not the derivative of $x^2$, but it is a constant multiple, and this is sufficient. 

<div class="example">
<p><b>Example:</b> Calculate the following integral
$$\int \frac{\cos x}{2\sin x + 7} dx$$
</p>
<b>Solution:</b> In this example, we see a function, $2\sin x + 7$, and its derivative $\cos x$ (not actually the derivative, but it is a constant multiple). Thus, we let $u = 2\sin x + 7$, so that $du = 2\cos x dx $. Thus the integral becomes 
$$\int \frac{\cos x}{2\sin x + 7} dx = \frac{1}{2}\int \frac{1}{u} du = \frac{1}{2} \log |u| + C$$
Lastly, undoing the substitution by putting $u = 2\sin x + 7$, we find that 
$$\int \frac{\cos x}{2\sin x + 7} dx = \frac{1}{2}\log|2\sin x + 7| + C.$$
</div> <br>

<div class="example">
<p><b>Example:</b> Calculate the following integral
$$\int\tan x dx $$ </p>
<b>Solution:</b> We first rewrite the integral like
$$\int\tan x dx  = \int \frac{\sin x}{\cos x} dx$$
Then, we make the substitution $u = \cos x$, and $du = -\sin x dx$. This gives us
$$ \int \frac{\sin x}{\cos x} dx = -\int \frac{1}{u} du$$
This is easy to integrate, and gives us 
$$-\int \frac{1}{u} du = -\log|u|$$
Substituting back in in terms of $x$, 
$$\int\tan x dx = -\log|\cos x| + C.$$
Note that this can also be written (by using the laws of logarithms) as 
$$\int\tan x dx = \log|\sec x| + C.$$
</div> <br>

<div class="example">
<p><b>Example:</b> Calculate the following integral
$$\int \frac{x-3}{4x^2+1}dx$$
</p>
<b>Solution:</b> In this example, it is much less obvious what to do! It is not obvious because the derivative of the problem function, $4x^2+1$, does not appear! However, if we split the integral up into two parts, this can be put in an easier form. 
$$\int \frac{x-3}{4x^2+1}dx = \int \frac{x}{4x^2+1} dx- \int \frac{3}{4x^2+1}$$
Now let's focus on the first integral. If we let $u = 4x^2+1$ and $du = 8x dx$, then we get 
$$\int \frac{x}{4x^2+1} dx = \frac{1}{8}\int \frac{du}{u} = \frac{1}{8}\log |u|$$
Plugging back in $u = 4x^2 + 1$, we find that 
$$\int \frac{x}{4x^2+1} dx = \frac{1}{8}\log(4x^2+1).$$
Now for the second integral. In this integral, we instead make the substitution $u = 2x$. Then, we find 
$$\int \frac{3}{4x^2+1} dx = \frac{3}{2}\int \frac{du}{u^2+1} = \frac{3}{2}\arctan(u)$$
where we have recognized the antiderivative of $1/(1+u^2)$ as the arctangent. Plugging back in $u = 2x$, we get 
$$\int \frac{3}{4x^2+1} dx = \frac{3}{2}\arctan(2x).$$
Now, we add our results together and find that 
$$\int \frac{x-3}{4x^2+1}dx = \frac{1}{8}\log(4x^2+1) - \frac{3}{2}\arctan(2x) + C.$$
</div> <br>


<div class="example">
<p><b>Example:</b> Calculate the following integral
$$\int x^3\sqrt{x^2+9}dx$$
</p>
<b>Solution:</b> In this example, it is not obvious at all what we need to do! We can make use of a clever trick. Let $u = x^2 + 9$ and $du = 2x dx$. Then, we get that 
$$\int x^3\sqrt{x^2+9}dx = \frac{1}{2}\int x^2\sqrt{u} du$$
but we haven't gotten rid of all of the $x$ terms! The way to solve this is substitute in $x^2 = u-9$. Thus, 
$$\int x^3\sqrt{x^2+9}dx = \frac{1}{2}\int(u-9)\sqrt{u} du = \frac{1}{2} \int (u^{3/2} - 9 u^{1/2}) du$$
This is now simple integrate by using the power rule, so 
$$\frac{1}{2} \int (u^{3/2} - 9 u^{1/2}) du = \frac{1}{5}u^{5/2} - 3u^{3/2} + C.$$
Now we substitute back in the expression $u = x^2 + 9$ to find our final answer:
$$\int x^3\sqrt{x^2+9}dx = \frac{1}{5}(x^2+9)^{5/2} - 3(x^2+9)^{3/2} + C$$ 
</div>
