---
layout: lesson
title: Taylor Series*
dept: math
course: calculus-III
unit: unit3
deptDisplay: Math
courseDisplay: Calculus III
unitDisplay: Unit 3
---

In single variable calculus, we used Taylor series to approximate differentiable functions. An identical thing can be done for functions of multiple variables, but it is a little bit more complicated. Recall that for an infinitely differentiable function in one variable, its Taylor series about a point \\(a\\) is 


$$ f(x) = \sum_{n = 0}^\infty \frac{f^{(n)}(a)(x-a)^n}{n!}$$

### Taylor Series in Two Variables
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

### Relationship with Single Variable Series

You might be wondering, would there be a difference between the series of \\(f(x,y) = \sin(xy)\\) when it is expanded in the method of above, versus treating \\(xy\\) as a single variable, and expanding it in the single variable sense? The answer is no. They will be exactly the same. Let us show that now. 

**Exercise** Expand the function \\(f(x,y) = \sin(xy)\\) about the origin in the above sense, and in the single variable sense. Show that they match.

<button onclick="myFunction('answer')" class="answerButton">Show Answer</button>

<div  id="answer" class="answer">
We recall the formula for the Taylor series of sine to be 
$$\sin(x) = \sum_{n=0}^\infty (-1)^n\frac{x^{2n+1}}{(2n+1)!}$$

Thus replacing \(x\) by \(xy\), we get 
$$\sin(xy) = \sum_{n=0}^\infty (-1)^n\frac{(xy)^{2n+1}}{(2n+1)!}$$

Now for the multivariable perspective. We want to compute the coefficients \(c_{mn}\). The coefficients are 

$$c_{mn} = \frac{1}{m!n!}\left(\frac{\partial^m\partial^nf}{\partial x^m\partial y^n}\right)(0,0)$$

and we know that for the sine function, after an even number of derivatives, if it is evaluated at \((0,0)\), it will be zero. If it is \(4k+1\) derivatives, for some integer \(k\), then it will be a positive cosine, and be \(+1\). If it is \(4k+3\) derivatives, for some integer \(k\), then it will be a negative cosine, and be \(-1\). In summary, 

$$c_{mn} = \frac{1}{m!n!}\left\{\begin{array}{cc}
0, & m+n = 4k \\
1, & m + n = 4k+1 \\
0, & m+n = 4k+2 \\
-1,& m+n = 4k+3
\end{array} \right. $$

Now let's consider two cases. For fixed even \(n\) and for fixed odd \(n\). 

$$f(x,y) = \sum_{n=0}^\infty\sum_{m=0}^\infty c_{mn}x^m y^n $$

Case 1: Suppose \(n\) is even. Then if \(m\) is also even, \(c_{mn} = 0\). If not, \(c_{mn} = \)







</div>

### Multi-index Notation

It is possible to make the formula for the Taylor Series in two variables more compact by introducing a new notation. This is known as the multi-index notation, and is very useful in expressing forulas involving derivatives in many variables, and also in combinatorics. It will also allow us to trivially create formulas for Taylor Series for functions in greater than two variables.




### Exercises

<ol>
<li> <div> Sketch all of the points such that \(y = 1\). </div>

<button onclick="myFunction('answer2')" class="answerButton">Show Answer</button>
<div  id="answer2" class="answer">
This is a plane that is parallel to the \(xz\) plane. 
</div> </li>
<li> <div> Sketch all of the points such that \(y = 1\). </div>

<button onclick="myFunction('answer2')" class="answerButton">Show Answer</button>
<div  id="answer2" class="answer">
This is a plane that is parallel to the \(xz\) plane. 
</div> </li>
</ol>
