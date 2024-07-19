---
layout: lesson
title: Substitution Rule 
dept: math
course: calculus-II
unit: unit2
deptDisplay: Math
courseDisplay: Calculus II
unitDisplay: Unit 2
---
In this section, we will discuss the inverse of the chain rule for differentiation. We recall that the chain rule for differentiation is given by

$$\begin{equation}
\frac{\d}{\d x}f(g(x)) = f'(g(x))g'(x).
\end{equation}$$

The way we invert the chain rule is by doing a substitution, and it is often called a "\\(u\\)-substitution". This is  because \\(u\\) is the most common letter used for such a substitution. The substitution rule says the following:

To evaluate the integral

$$\begin{equation}
\int f'(g(x))g'(x) \d x,
\end{equation}$$

make the substitution \\(u = g(x)\\). This doesn't tell us the whole story however, because we also need to express the differential \\(\d x\\) in terms of \\(u\\). To do this, we take the differential of both sides of \\(u = g(x)\\). Doing this gives \\(\d u = g'(x) \d x\\). Thus, we get

$$\begin{equation}\int \underbrace{f'(g(x))}_{f'(u)} \underbrace{g'(x) \d x}_{\d u} = \int f'(u) \d u = f(u) = f(g(x)).\end{equation}$$

It may not always be the case that the \\(g'(x)\\) is just sitting there beside the \\(\d x\\), so extra work may be necessary. This seems a little bit abstract, so we will do several examples. 

\begin{remark_wrapper}
\begin{remark}
The following formulas will be useful to have memorized while attempting these problems (for both the examples and the exercises)

$$\begin{align}
\int x^n \d x ={}& \frac{x^{n+1}}{n+1} ,\qquad (n\not=-1)\\
\int \sin x \d x ={}& -\cos x \\
\int \cos x \d x ={}& \sin x \\
\int \frac{\d x}{1+x^2} ={}& \arctan x \\
\int e^x \d x ={}& e^x \\
\int \frac{\d x}{x} ={}& \log|x| 
\end{align}$$

Armed with these formulas, you should be equipped to solve the following exercises. Also make sure that you keep your trigonometric identities in mind. Some of these integrals may seem quite complicated at first, but by using a trigonometric identity they are substantially simplified.
\end{remark}
\end{remark_wrapper}

<div class="example">
<b>Example:</b>
Calculate the following integral
$$\begin{equation}\int\cos(2x) \d x \end{equation}$$ 


<b>Solution:</b> We already know how to integrate \(\cos x\), but not \(\cos(2x)\). How can we change this into a form that we recognize? Let's make the substitution \(u = 2x\). If we make this substitution, then we also need to change the differential, which gives \(\d u = 2\d x\). This means that \(\d x = \frac{1}{2} \d u\). Thus, the integral becomes
$$\begin{equation}
\int\cos(2x) \d x = \int\cos u \frac{\d u}{2}
\end{equation}$$

If we just move the \(1/2\) out to the front, then we are integrating a normal cosine! 

$$\begin{equation}
\frac{1}{2}\int\cos u \d u = \frac{1}{2}\sin u + C
\end{equation}$$

Thus, if we substitute back in our original variable \(u = 2x\), we find that

$$\begin{equation}
\int\cos(2x) \d x = \frac{1}{2}\sin(2x) + C
\end{equation}$$


</div>

<div class="example">
<b>Example:</b>
Calculate the following integral
$$\begin{equation}
\int xe^{x^2} \d x 
\end{equation}$$


<b>Solution:</b> Here, we recognize that if we make the substitution \(u = x^2\) and \(\d u = 2x\d x\), then we can substitute in \(\d x = \frac{\d u}{2x}\). This will make the extra \(x\) cancel out! 

$$\begin{equation}
\int xe^{x^2} \d x = \int x e^{x^2} \frac{\d u}{2x} = \frac{1}{2}\int e^u \d u
\end{equation}$$

Now, we can integrate the exponential easily!

$$\begin{equation} 
\frac{1}{2}\int e^u \d u = \frac{1}{2} e^u + C
\end{equation}$$

Lastly, substituting in \(u = x^2\), we find that

$$\begin{equation}
\int xe^{x^2} \d x = \frac{1}{2} e^{x^2}
\end{equation}$$ 


</div>

You may have started to notice a theme here. If we see a function (in the previous example, \\(x^2\\)) and its derivative, or something which is a constant multiple of its derivative (in the previous example, \\(x\\) is not the derivative of \\(2x\\), but it is a constant multiple thereof), then we can do a \\(u\\)-substitution for the function (in the previous example \\(u = x^2\\)).

<div class="example">
<b>Example:</b>
Calculate the following integral
$$\begin{equation}\int \frac{\cos x}{2\sin x + 7} \d x\end{equation}$$


<b>Solution:</b> In this example, we see a function, \(2\sin x + 7\), and its derivative \(\cos x\) (not actually the derivative, but it is a constant multiple). Thus, we let \(u = 2\sin x + 7\), so that \(\d u = 2\cos x \d x \). Thus the integral becomes 
$$\begin{equation}\int \frac{\cos x}{2\sin x + 7} \d x = \frac{1}{2}\int \frac{1}{u} \d u = \frac{1}{2} \log |u| + C\end{equation}$$
Lastly, undoing the substitution by putting \(u = 2\sin x + 7\), we find that 
$$\begin{equation}\int \frac{\cos x}{2\sin x + 7} \d x = \frac{1}{2}\log|2\sin x + 7| + C.\end{equation}$$

</div>

<div class="example">
<b>Example:</b>
Calculate the following integral
$$\begin{equation}
\int\tan x \d x 
\end{equation}$$

<b>Solution:</b> We first rewrite the integral like
$$\begin{equation}
\int\tan x \d x  = \int \frac{\sin x}{\cos x} \d x
\end{equation}$$
Then, we make the substitution \(u = \cos x\), and \(\d u = -\sin x \d x\). This gives us

$$\begin{equation} 
\int \frac{\sin x}{\cos x} \d x = -\int \frac{1}{u} \d u
\end{equation}$$

This is easy to integrate, and gives us 
$$\begin{equation}
-\int \frac{1}{u} \d u = -\log|u|
\end{equation}$$
Substituting back in in terms of \(x\), 
$$\begin{equation}
\int\tan x \d x = -\log|\cos x| + C.
\end{equation}$$
Note that this can also be written (by using the laws of logarithms) as 
$$\begin{equation}
\int\tan x \d x = \log|\sec x| + C.
\end{equation}$$

</div>

<div class="example">
<b>Example:</b>
Calculate the following integral
$$\begin{equation}\int \frac{x-3}{4x^2+1}\d x\end{equation}$$


<b>Solution:</b> In this example, it is much less obvious what to do! It is not obvious because the derivative of the problem function, \(4x^2+1\), does not appear! However, if we split the integral up into two parts, this can be put in an easier form. 
$$\begin{equation}
\int \frac{x-3}{4x^2+1}\d x = \int \frac{x}{4x^2+1} \d x- \int \frac{3}{4x^2+1}
\end{equation}$$
Now let's focus on the first integral. If we let \(u = 4x^2+1\) and \(\d u = 8x \d x\), then we get 
$$\begin{equation}
\int \frac{x}{4x^2+1} \d x = \frac{1}{8}\int \frac{\d u}{u} = \frac{1}{8}\log |u|
\end{equation}$$
Plugging back in \(u = 4x^2 + 1\), we find that 
$$\begin{equation}
\int \frac{x}{4x^2+1} \d x = \frac{1}{8}\log(4x^2+1).
\end{equation}$$
Now for the second integral. In this integral, we instead make the substitution \(u = 2x\). Then, we find 
$$\begin{equation}
\int \frac{3}{4x^2+1} \d x = \frac{3}{2}\int \frac{\d u}{u^2+1} = \frac{3}{2}\arctan(u)
\end{equation}$$
where we have recognized the antiderivative of \(1/(1+u^2)\) as the arctangent. Plugging back in \(u = 2x\), we get 
$$\begin{equation}
\int \frac{3}{4x^2+1} \d x = \frac{3}{2}\arctan(2x).
\end{equation}$$
Now, we add our results together and find that 
$$\begin{equation}
\int \frac{x-3}{4x^2+1}\d x = \frac{1}{8}\log(4x^2+1) - \frac{3}{2}\arctan(2x) + C.
\end{equation}$$

</div>

<div class="example">
<b>Example:</b>
Calculate the following integral
$$\begin{equation}
\int x^3\sqrt{x^2+9}\d x
\end{equation}$$


<b>Solution:</b> In this example, it is not obvious at all what we need to do! We can make use of a clever trick. Let \(u = x^2 + 9\) and \(\d u = 2x \d x\). Then, we get that 
$$\begin{equation}
\int x^3\sqrt{x^2+9}\d x = \frac{1}{2}\int x^2\sqrt{u} \d u
\end{equation}$$

but we haven't gotten rid of all of the \(x\) terms! The way to solve this is substitute in \(x^2 = u-9\). Thus, 

$$\begin{equation}
\int x^3\sqrt{x^2+9}\d x = \frac{1}{2}\int(u-9)\sqrt{u} \d u = \frac{1}{2} \int (u^{3/2} - 9 u^{1/2}) \d u
\end{equation}$$

This is now simple integrate by using the power rule, so 

$$\begin{equation}
\frac{1}{2} \int (u^{3/2} - 9 u^{1/2}) \d u = \frac{1}{5}u^{5/2} - 3u^{3/2} + C.
\end{equation}$$

Now we substitute back in the expression \(u = x^2 + 9\) to find our final answer:

$$\begin{equation}
\int x^3\sqrt{x^2+9}\d x = \frac{1}{5}(x^2+9)^{5/2} - 3(x^2+9)^{3/2} + C
\end{equation}$$ 

</div>



