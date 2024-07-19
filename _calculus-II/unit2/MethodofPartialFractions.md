---
layout: lesson
title: Method of Partial Fractions 
dept: math
course: calculus-II
unit: unit2
deptDisplay: Math
courseDisplay: Calculus II
unitDisplay: Unit 2
---

In this section, we study integrals of the form

$$\int \frac{p(x)}{q(x)} \d x,$$

where both \\(p\\) and \\(q\\) are polynomial functions. In solving these problems we do a partial fraction decomposition, which splits the integrand into a sum of simple terms. For example, a rational function and its partial fraction decomposition is

$$\frac{1}{(x+1)(x+2)} = \frac{1}{x+1} - \frac{1}{x+2}.$$

The decomposed function is much easier to integrate, but how would we actually calculate this? That is the goal of this lesson.

We only apply partial fraction decomposition if the degree of the numerator is strictly less than the degree of the denominator. The degree of a polynomial is its highest power. For example, the degree of \\(x^3 - 2x + 5\\) is 3 because of the \\(x^3\\) term. 

<ol>
<li> If the degree of \(p\) is greater than or equal to the degree of \(q\), apply polynomial long division first, then partial fractions.
</li>
<li> If the degree of \(p\) is less than the degree of \(q\), proceed directly to partial fractions. 
</li></ol>

Please refer to a secondary school text for review of polynomial long division. There are four forms that we can tackle with partial fraction decomposition. 

### Case 1: Distinct Linear Factors


<div class="example">
<b>Example:</b>
 Decompose the function
 
$$\begin{equation}
\frac{1}{(x+1)(x+3)}
\end{equation}$$
in a partial fractions decomposition.


<b>Solution:</b> We write
$$\begin{equation}
\frac{1}{(x+1)(x+3)} = \frac{A}{x+1} + \frac{B}{x+3}
\end{equation}$$
where \(A\) and \(B\) are coefficients to be found. There are two methods to find \(A\) and \(B\), and I will illustrate both here.


<b>Method 1:</b> Multiply both sides by \((x+1)(x+3)\), so that we get 
$$\begin{equation}
1 = A(x+3) + B(x+1) = (A+B)x + (3A + B)
\end{equation}$$
Since this is supposed to be an identity (meaning that the equation works for every value of \(x\)), we match coefficients to get
$$\begin{equation}
A+B = 0,\qquad 3A + B = 1.
\end{equation}$$
There are no \(x\) terms on the left hand side, which is why we got \(A+B =0\), and the constant terms need to match too. If we solve this system of equations, we find that \(A = 1/2\) and \(B = -1/2\).


<b>Method 2:</b> Multiply both sides by \((x+1)(x+3)\), so that we get 
$$\begin{equation}
1 = A(x+3) + B(x+1)
\end{equation}$$
Since this is supposed to be an identity (meaning that the equation works for every value of \(x\)), it is true in particular for \(x = -1\). Plugging in \(x = -1\) to both sides gives us \(1 = A(-1+3)\), so \(A = 1/2\). The equation is also true for \(x = -3\). Plugging in \(x = -3\) to both sides gives us \(1 = B(-3 + 1)\), so \(B = -1/2\).

Thus both methods give the same result so the decomposition is

$$\begin{equation}
\frac{1}{(x+1)(x+3)} = \frac{1}{2}\frac{1}{x+1} - \frac{1}{2}\frac{1}{x+3}.
\end{equation}$$

</div>

<div class="example">
<b>Example:</b>
Decompose the function
$$\begin{equation}
\frac{x-2}{(2x+1)(x+3)}
\end{equation}$$
in a partial fractions decomposition.


<b>Solution:</b> We write
$$\begin{equation}
\frac{x-2}{(2x+1)(x+3)} = \frac{A}{2x+1} + \frac{B}{x+3}
\end{equation}$$
where \(A\) and \(B\) are coefficients to be found. There are two methods to find \(A\) and \(B\), and I will illustrate both here.


<b>Method 1:</b> Multiply both sides by \((2x+1)(x+3)\), so that we get 
$$\begin{equation}
x-2 = A(x+3) + B(2x+1) = (A+2B)x + (3A + B)
\end{equation}$$
Since this is supposed to be an identity (meaning that the equation works for every value of \(x\)), we match coefficients to get
$$\begin{equation}
A+2B = 1,\qquad 3A + B = -2.
\end{equation}$$
If we solve this system of equations, we find that \(A = -1\) and \(B = 1\).


<b>Method 2:</b> Multiply both sides by \((2x+1)(x+3)\), so that we get 
$$\begin{equation}
x-2 = A(x+3) + B(2x+1).
\end{equation}$$
Since this is supposed to be an identity (meaning that the equation works for every value of \(x\)), it is true in particular for \(x = -1/2\). Plugging in \(x = -1/2\) to both sides gives us \(-5/2 = A(-1/2+3)\), so \(A = -1\). The equation is also true for \(x = -3\). Plugging in \(x = -3\) to both sides gives us \(-5 = B(-6 + 1)\), so \(B = 1\).

Thus both methods give the same result so the decomposition is

$$\begin{equation}
\frac{x-2}{(2x+1)(x+3)} = -\frac{1}{2x+1} + \frac{1}{x+3}.
\end{equation}$$

</div>


### Case 2: Unfactorable Quadratic

<div class="example">
<b>Example:</b> Decompose the function
$$\begin{equation}
\frac{1}{(x^2+2x+7)(x-1)}
\end{equation}$$
in a partial fractions decomposition.


<b>Solution:</b>
 The first thing we notice is that we cannot factor \(x^2+2x+7\) into linear factors! This means that the decomposition will take the form
$$\begin{equation}
\frac{1}{(x^2+2x+7)(x-1)} = \frac{Ax+B}{x^2+2x+7} + \frac{C}{x-1},
\end{equation}$$
where \(A\), \(B\), and \(C\) are coefficients to be found. In general, method 2 from the previous two examples doesn't work here because we can't plug in a value of \(x\) that makes terms disappear (because the quadratic is unfactorable). This means that we must solve the system of equations. 

Multiply both sides by \((x^2+2x+7)(x-1)\), so that we get 
$$\begin{equation}
1 = (Ax+B)(x-1) + C(x^2+2x+7) = (A+C)x^2 + (B-A + 2C)x + (7C - B)
\end{equation}$$
Since this is supposed to be an identity (meaning that the equation works for every value of \(x\)), we match coefficients to get
$$\begin{equation}
A+C = 0,\qquad B - A + 2C = 0,\qquad 7C - B = 1.
\end{equation}$$
If we solve this system of equations, we find that \(A = -1/10\), \(B = -3/10\), and \(C = 1/10\). 

Thus the partial fraction decomposition is 
$$\begin{equation}
\frac{1}{(x^2+2x+7)(x-1)} = \frac{1}{10}\frac{-x-3}{x^2+2x+7} + \frac{1}{10}\frac{1}{x-1}.
\end{equation}$$

The observant among you may have noticed that it is possible to apply method 2 to the \(x-1\) factor to find \(C\), which is true! However, one would still have to solve the system of equations as in method 1 to find \(A\) and \(B\).

</div>

### Case 3: Repeated Linear Factors


<div class="example">
<b>Example:</b>
Decompose the function
$$\begin{equation}
\frac{x}{(x-2)^2(x+3)}
\end{equation}$$
in a partial fractions decomposition.


<b>Solution:</b>
 The form that we need to use this time is 
$$\begin{equation}
\frac{x}{(x-2)^2(x+3)} = \frac{A}{x-2} + \frac{B}{(x-2)^2} + \frac{C}{x+3}.
\end{equation}$$

The first step is, you guessed it, to multiply both sides by \((x-2)^2(x+3)\). This gives us 

$$\begin{equation}
x = A(x-2)(x+3) + B(x+3) + C(x-2)^2.
\end{equation}$$

Note that if we apply method 2 to this problem it only allows us to find \(B\) and \(C\), but not \(A\). One could take this approach, and then find \(A\) by matching coefficients. I will use method 1 here and expand out the factors to get 

$$\begin{equation}
x = (A+C)x^2 + (A+B - 4C)x + (-6A + 3B + 4C)
\end{equation}$$

This gives us three equations:
$$\begin{equation}
A+C = 0,\qquad A+ B - 4C = 1, \qquad -6A + 3B + 4C = 0.
\end{equation}$$

Solving these equations, we get 

$$\begin{equation}
A = \frac{3}{25},\qquad B = \frac{2}{5},\qquad C = -\frac{3}{25}.
\end{equation}$$

Thus the partial fraction decomposition is 

$$\begin{equation}
\frac{x}{(x-2)^2(x+3)} = \frac{3}{25(x-2)} + \frac{2}{5(x-2)^2} - \frac{3}{25(x+3)}.
\end{equation}$$


</div>

### Case 4: Repeated quadratic factors:


<div class="example">
<b>Example:</b>Decompose the function
$$\begin{equation}
\frac{x^2+3}{(x^2+2x+7)^2(x+1)}
\end{equation}$$
in a partial fractions decomposition.


<b>Solution:</b> The form that we need to use this time is 

$$\begin{equation}
\frac{x^2+3}{(x^2+2x+7)^2(x+1)} = \frac{Ax+B}{x^2+2x+7} + \frac{Cx+D}{(x^2+2x+7)^2} + \frac{E}{x+1}.
\end{equation}$$

If we multiply both sides by \((x^2+2x+7)^2(x+1)\) and expand out, we get 

$$\begin{equation}
x^2+3 = (A+E)x^4 + (3A+B+4E)x^3 + (9A+3B+C+18E)x^2 + (7A + 9B + C + \d x + 28E)x+(7B+D+49E)
\end{equation}$$

If we solve this system of equations, we get 

$$\begin{equation}
A = -\frac{1}{9},\quad B = -\frac{1}{9},\quad C = \frac{1}{3},\quad D = -\frac{5}{3},\quad E = \frac{1}{9}.
\end{equation}$$

Thus the partial fraction decomposition is 

$$\begin{equation}
\frac{x^2+3}{(x^2+2x+7)^2(x+1)}  = \frac{1}{9}\frac {-x-1}{x^{2}+2x+7} + \frac{1}{3}\frac{x-5}{( {x}^{2}+2x+7)^2} + \frac{1}{9}\frac{1}{x+1}
\end{equation}$$


</div>


### Integration of the Above Examples

Now, armed with the power of partial fractions, let's integrate some functions! We will integrate the 5 examples we've done here. 

<div class="example">
<b>Example:</b> 
Evaluate the integral
$$\begin{equation}
\int\frac{1}{(x+1)(x+3)}\d x
\end{equation}$$


<b>Solution:</b>
We apply the partial fractions decomposition from example 1. This gives us 
$$\begin{equation}
\int\left( \frac{1}{2}\frac{1}{x+1} - \frac{1}{2}\frac{1}{x+3}\right)\d x
\end{equation}$$

This is easily integrated to give 

$$\begin{equation}
\int\frac{1}{(x+1)(x+3)}\d x = \frac{1}{2}\log|x+1| - \frac{1}{2}\log|x+3|
\end{equation}$$

Simplifying, we get 

$$\begin{equation}
\int\frac{1}{(x+1)(x+3)}\d x = \frac{1}{2}\log\left|\frac{x+1}{x+3}\right| + C.
\end{equation}$$

</div>

<div class="example">
<b>Example:</b>
Evaluate the integral
$$\begin{equation}
\int\frac{x-2}{(2x+1)(x+3)}\d x
\end{equation}$$


<b>Solution:</b> We apply the partial fractions decomposition from example 2. This gives us 
$$\begin{equation}
\int\left(\frac{x-2}{(2x+1)(x+3)}\right)\d x = \int\left(-\frac{1}{2x+1} + \frac{1}{x+3}\right)\d x
\end{equation}$$

This is easily integrated to give 

$$\begin{equation}
\int\frac{1}{(x+1)(x+3)}\d x = -\frac{1}{2}\log|2x+1| + \log|x+3|
\end{equation}$$

Simplifying, we get 

$$\begin{equation}
\int\frac{1}{(x+1)(x+3)}\d x = \frac{1}{2}\log\left|\frac{(x+3)^2}{2x+1}\right| + C.
\end{equation}$$

</div>

<div class="example">
<b>Example:</b>
Evaluate the integral
$$\begin{equation}
\int\frac{1}{(x^2+2x+7)(x-1)}\d x
\end{equation}$$


<b>Solution:</b> We apply the partial fractions decomposition from example 3. This gives us 
$$\begin{equation}
\int \frac{1}{(x^2+2x+7)(x-1)}\d x = \int\left(\frac{1}{10}\frac{-x-3}{x^2+2x+7} + \frac{1}{10}\frac{1}{x-1}\right)\d x
\end{equation}$$

The second term is easily integrated, but what about the first term? For the first term, we need to break it up to make 

$$\begin{equation}
\int\frac{x+3}{x^2+2x+7}\d x = \int \frac{x+1}{x^2+2x+7}\d x + 2\int \frac{1}{x^2+2x+7}\d x
\end{equation}$$

The first term is ready to be integrated as a logarithm by making the \(u\)-substitution \(u = x^2+2x+7\), and the second one can be integrated as an arctangent after we complete the square. This gives us 

$$\begin{align}
\int\frac{x+3}{x^2+2x+7}\d x ={}& \frac{1}{2}\log(x^2+2x+7)+ 2\int \frac{1}{(x+1)^2+6}\d x \\
={}& \frac{1}{2}\log(x^2+2x+7)+ \frac{2}{\sqrt{6}}\arctan\left(\frac{x+1}{\sqrt{6}}\right)
\end{align}$$

Now putting it all together, we get 

$$\begin{equation}
\int\frac{1}{(x^2+2x+7)(x-1)}\d x = \frac{1}{20}\log(x^2+2x+7) + \frac{1}{5\sqrt{6}}\arctan\left(\frac{x+1}{\sqrt{6}}\right) + \frac{1}{10}\log|x-1|
\end{equation}$$


</div>

<div class="example">
<b>Example:</b>
Evaluate the integral
$$\begin{equation}
\int\frac{x}{(x-2)^2(x+3)}\d x
\end{equation}$$


<b>Solution:</b> We apply the partial fractions decomposition from example 4. This gives us 
$$\begin{equation}
\int \frac{1}{(x^2+2x+7)(x-1)}\d x = \int\left(\frac{3}{25(x-2)} + \frac{2}{5(x-2)^2} - \frac{3}{25(x+3)}\right)\d x
\end{equation}$$

All the terms in this are easily integrated, and we get 

$$\begin{equation}
\int\frac{x}{(x-2)^2(x+3)}\d x = \frac{3}{25}\log|x-2| - \frac{2}{5}\frac{1}{x-2} - \frac{3}{25}\log|x+3|
\end{equation}$$

Simplifying, the final answer becomes

$$\begin{equation}
\int\frac{x}{(x-2)^2(x+3)}\d x = \frac{3}{25}\log\left|\frac{x-2}{x+3}\right| - \frac{2}{5}\frac{1}{x-2} + C
\end{equation}$$


</div>


<div class="example">
<b>Example:</b>
Evaluate the integral
$$\begin{equation}
\int\frac{x^2+3}{(x^2+2x+7)^2(x+1)}\d x
\end{equation}$$


<b>Solution:</b> We apply the partial fractions decomposition from example 4. This gives us 
$$\begin{equation}
\int \frac{x^2+3}{(x^2+2x+7)^2(x+1)}\d x = \int\left( \frac{1}{9}\frac {-x-1}{x^{2}+2x+7} + \frac{1}{3}\frac{x-5}{( {x}^{2}+2x+ 7)^2} + \frac{1}{9}\frac{1}{x+1}\right)\d x
\end{equation}$$

The last term is easily integrated, and the first term can be integrated by a \(u\) substitution \(u = x^2+2x+7\). These are 

$$\begin{align}
\int \frac{x^2+3}{(x^2+2x+7)^2(x+1)}\d x ={}& -\frac{1}{18}\log(x^2+2x+7) + \int\frac{1}{3}\frac{x-5}{( {x}^{2}+2x+ 7)^2} + \frac{1}{9}\log|x+1|\\
={}& \frac{1}{18}\log\frac{|x+1|^2}{x^2+2x+7} + \int\frac{1}{3}\frac{x-5}{( {x}^{2}+2x+ 7)^2}
\end{align}$$

but what about the remaining integral?

For the remaining integral, we split it up

$$\begin{equation}
\int \frac{x-5}{(x^2+2x+7)^2}\d x = \int \frac{x+1}{(x^2 + 2x+7)^2}\d x - 6\int \frac{1}{(x^2+2x+7)^2}\d x 
\end{equation}$$

The first of these two terms can be done with a \(u\) substitution: let \(u = x^2+2x+7\). For the second term, we use a trigonometric substitution after completing the square. The substitution is \(\sqrt{6}\tan\theta = x+1\). This gives us 

$$\begin{align}
\int \frac{x-5}{(x^2+2x+7)^2}\d x ={}& \int \frac{x+1}{(x^2 + 2x+7)^2}\d x - 6\int \frac{1}{(x^2+2x+7)^2}\d x \\
={}& -\frac{1}{2(x^2+2x+7)} - 6\int \frac{\sqrt{6}\sec^2\theta d\theta}{6^2\sec^4\theta} \\
={}& -\frac{1}{2(x^2+2x+7)} - \frac{1}{\sqrt{6}}\int \cos^2\theta d\theta\\
={}& -\frac{1}{2(x^2+2x+7)} - \frac{1}{2\sqrt{6}}\left(\theta + \frac{\sin 2\theta}{2}\right)\\
={}& \frac{-1}{2}\frac{1}{x^2+2x+7} - \frac{1}{2\sqrt{6}}\arctan\left(\frac{x+1}{\sqrt{6}}\right) -\frac{1}{2}\frac{x+1}{x^2+2x+7} \\
={}& -\frac{1}{2\sqrt{6}}\arctan\left(\frac{x+1}{\sqrt{6}}\right) -\frac{1}{2}\frac{x+2}{x^2+2x+7}
\end{align}$$

where we have used our knowledge of trigonometric integrals to calculate \(\int\cos^2\theta d\theta\). Finally, the answer is 

$$\begin{equation}
\int\frac{x^2+3}{(x^2+2x+7)^2(x+1)}\d x = \frac{1}{18}\log\frac{|x+1|^2}{x^2+2x+7}  -\frac{1}{6\sqrt{6}}\arctan\left(\frac{x+1}{\sqrt{6}}\right) -\frac{1}{6}\frac{x+2}{x^2+2x+7}
\end{equation}$$


</div>




### Further Examples

There are various integrals which, through some kind of substitution, can be turned into rational functions. 

<div class="example">
<b>Example:</b>
Evaluate the integral 
$$\begin{equation}
\int \csc \theta d\theta
\end{equation}$$


<b>Solution:</b> We first manipulate the integrand to make it possible to use partial fractions.
$$\begin{align}
\int \csc \theta d\theta ={}& \int \frac{1}{\sin \theta}d\theta \\
={}& \int \frac{\sin \theta }{\sin^2\theta}d\theta \\
={}& \int \frac{\sin \theta}{1-\cos^2\theta }d\theta 
\end{align}$$
Let \(\cos \theta  = u\), and \(du = -\sin \theta d\theta\). This transforms the integral in to
$$\begin{align}
\int \frac{\sin \theta}{1-\cos^2\theta }d\theta  ={}& -\int \frac{du}{1-u^2} \\
={}& -\frac{1}{2}\int\left( \frac{1}{1 + u} + \frac{1}{1 - u} \right)du \\
={}& -\frac{1}{2}\log \left| \frac{1 + u}{1 - u} \right| \\
={}& -\frac{1}{2}\log \left| \frac{1 + \cos \theta }{1 - \cos \theta } \right| \\ 
={}& -\frac{1}{2}\log \left| \frac{1 + \cos \theta }{1 - \cos \theta }\left( \frac{1 + \cos \theta }{1 + \cos \theta } \right) \right| \\
={}& -\frac{1}{2}\log \left| \frac{(1 + \cos \theta )^2}{\sin^2\theta } \right|\\
={}& -\log \left| \frac{1+\cos \theta }{\sin \theta } \right|\\
={}& -\log \left| {\csc \theta  + \cot \theta } \right|
\end{align}$$

Thus

$$\begin{equation}
\int {\csc \theta d\theta }  = -\log \left| {\csc \theta  + \cot \theta } \right|
\end{equation}$$

</div>


