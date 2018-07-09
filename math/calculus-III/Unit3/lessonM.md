---
layout: lesson
title: Taylor Series*
course: calculus-III
unit: unit3
---

In single variable calculus, we used Taylor series to approximate differentiable functions. An identical thing can be done for functions of multiple variables, but it is a little bit more complicated. Recall that for an infinitely differentiable function in one variable, its Taylor series about a point \\(a\\) is 


$$ f(x) = \sum_{n = 0}^\infty \frac{f^{(n)}(a)(x-a)^n}{n!}$$

For the case of a function of several variables, writing it in terms of a sum of power terms is more  complicated because of the possibility of *mixed terms*. For example, if we were looking at \\(f(x,y)\\), in addition to terms like \\(x,x^5,y^2\\), there would also be terms like \\(xy,xy^3\\) and so on. How can we derive the coefficients? In order to account for all of these terms, let's begin by writing an expansion for \\(f(x,y)\\) about the point \\((a,b)\\) in terms of unknown coefficients:

$$f(x,y) = \sum_{n=0}^\infty\sum_{m=0}^\infty c_{mn}(x-a)^m(y-b)^n $$

Now consider differentiating the above equation \\(i\\) times with respect to \\(x\\), and then \\(j\\) times with respect to \\(y\\):

$$\frac{\partial^i}{\partial x^i}\frac{\partial^j}{\partial y^j} f(x,y) = \sum_{n=0}^\infty\sum_{m=0}^\infty c_{mn}\frac{m!}{(m-i)!}\frac{n!}{(n-j)!}(x-a)^{m-i}(y-b)^{n-j}$$

All of the terms with \\(m < i\\), and \\(n < j\\) will be zero, so this can be rewritten as 

$$\frac{\partial^i}{\partial x^i}\frac{\partial^j}{\partial y^j} f(x,y) = \sum_{n=j}^\infty\sum_{m=i}^\infty c_{mn}\frac{m!}{(m-i)!}\frac{n!}{(n-j)!}(x-a)^{m-i}(y-b)^{n-j}$$

Then plugging in \\(x = a\\), and \\(y = b\\) to both sides, we get that all of the terms drop out except for the one with \\(m = i\\) and \\(n = j\\). Thus

$$c_{ij}i!j! = \left(\frac{\partial^i\partial^jf}{\partial x^i\partial y^j}\right)(a,b)$$

Then relabelling the indices back to \\(m\\) and \\(n\\), we get 

$$c_{mn} = \frac{1}{m!n!}\left(\frac{\partial^m\partial^nf}{\partial x^m\partial y^n}\right)(a,b)$$

With our result in hand, we can rewrite our Taylor series in its entirety: 

$$f(x,y) = \sum_{n=0}^\infty\sum_{m=0}^\infty \left(\frac{\partial^m\partial^nf}{\partial x^m\partial y^n}\right)(a,b)\frac{(x-a)^m(y-b)^n }{m!n!}$$

