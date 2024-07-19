---
layout: lesson
title: Integration by Parts 
dept: math
course: calculus-II
unit: unit2
deptDisplay: Math
courseDisplay: Calculus II
unitDisplay: Unit 2
---

In the last section, we discussed \\(u\\)-substitution, which was the inverse of the chain rule. In this section, we will discuss integration by parts, which is the inverse of the product rule. The product rule from differential calculus says that 

$$\begin{equation}(f(x)g(x))' = f'(x)g(x) + f(x)g'(x).\end{equation}$$

If we integrate both sides, then we get

$$\begin{equation}f(x)g(x) = \int f'(x) g(x) \d x + \int f(x)g'(x) \d x.\end{equation}$$

Rearranging terms, we get the integration by parts formula.

<div class="result">
<b>Result:</b>
The integration by parts formula is given by the following:

$$\begin{equation}\int f'(x)g(x) \d x= f(x)g(x) - \int f(x)g'(x) \d x.\end{equation}$$


</div>

This formula should be used in the following way. Note that we have the product of two functions, \\(f'(x)\\) and \\(g(x)\\), in the original integral. In the second integral, we will have to integrate \\(f(x)g'(x)\\). If we identify one of our functions as \\(g\\), then we will end up differentiating it, and the remaining part \\(f'(x)\\) must be integrated. We thus want to pick \\(f'(x)\\) to be the function which does not get more complicated when integrated, and \\(g(x)\\) as a function which gets simpler when differentiated. This will be seen in the following examples.

Note that it is not always the case that we have an integral for which \\(f'(x)\\) doesn't get more complicated when integrated. In these situations, using integration by parts is not recommended! There are some interesting cases which can still be solved by integration by parts even if they don't fall under the description in the previous paragraph, and I will show examples of those as well. 


<div class="example">
<b>Example:</b>
Evaluate the integral

$$\begin{equation}\int x e^x \d x.\end{equation}$$


<b>Solution:</b> According to the notation above, we set \(f'(x) = e^x\) and \(g(x) = x\). This is because we will differentiate \(g\), whose derivative is just 1, and integrate \(f'\), whose antiderivative is just itself. Thus, 

$$\begin{equation}\int x e^x \d x  = xe^x - \int 1 e^x \d x = x e^x - e^x\end{equation}$$

In summary,

$$\begin{equation}\int x e^x \d x = (x-1)e^x + C.\end{equation}$$


</div>

<div class="example">
<b>Example:</b>
Evaluate the integral 

$$\begin{equation}\int x^2 \cos 2x \d x.\end{equation}$$


<b>Solution:</b> According ot the notation above, we set \(f'(x) = \cos 2x\) and \(g(x) = x^2\). This is because we will differentiate \(g\), whose derivative is \(2x\), which is simpler than before, and integrate \(f'\), whose antiderivative is just a sine, which is not more complicated than a cosine. Thus,

$$\begin{equation}\int x^2 \cos 2x \d x = \frac{x^2}{2}\sin 2x - \int x\sin 2x \d x\end{equation}$$

Unfortunately, the resulting integral is still not one of the ones that we already know! In fact, we need to use integration by parts a second time. Note that we used a \(u\) substitution with \(u = 2x\) in order to integrate \(\cos 2x\). The mechanics of \(u\)-substitutions are described in the previous lesson.

$$\begin{equation}
\int x^2 \cos 2x \d x = \frac{x^2}{2}\sin 2x - \left(\frac{x}{2}\cos 2x - \frac{1}{2}\int -\cos 2x \d x \right)
\end{equation}$$

Now, we can easily integrate the last integral! Evaluating the last integral gives us the final answer

$$\begin{equation}
\int x^2 \cos 2x \d x = \frac{x^2}{2}\sin 2x + \frac{x}{2}\cos 2x - \frac{1}{4}\sin 2x + C
\end{equation}$$

</div>

<div class="example">
<b>Example:</b>
Evaluate the integral 

$$\begin{equation}\int x^3 e^{x^2} \d x.\end{equation}$$


<b>Solution:</b> To evaluate this integral, we first need to make a \(u\)-substitution. Let \(u = x^2\), so that our integral becomes 

$$\begin{equation}\int x^3 e^{x^2} \d x = \frac{1}{2}\int u e^{u} \d u,\end{equation}$$

where one power of \(x\) was cancelled out by the \(u\) substitution and the resulting \(x^2\) was substituted by \(u = x^2\). Now, this is in the form of an integration by parts problem with the variable \(u\). If we integrate it by parts, we find that 

$$\begin{equation} \frac{1}{2}\int u e^{u} \d u = \frac{1}{2}ue^u - \frac{1}{2}\int e^u \d u = \frac{1}{2}(u-1)e^u,\end{equation}$$

If we substitute back in our original expression \(u = x^2\), then we get our final answer

$$\begin{equation}\int x^3 e^{x^2} \d x = \frac{1}{2}(x^2 - 1)e^{x^2} + C.\end{equation}$$


</div>

<div class="example">
<b>Example:</b>
Evaluate the integral

$$\begin{equation}\int e^{2x}\cos x \d x \end{equation}$$


<b>Solution:</b> This is a more complicated example than what we have seen so far because it is not obvious what we need to integrate and what we need to differentiate! To solve this problem, we simply need to pick something to differentiate and something to integrate. Let's differentiate the cosine and integrate the exponential. The first step is 

$$\begin{align}
\int e^{2x}\cos x \d x ={}& \frac{1}{2}e^{2x}\cos x - \int e^{2x}(-\sin x) \d x\\
={}& \frac{1}{2}e^{2x}\cos x + \frac{1}{2}\int e^{2x}\sin x \d x\\
\end{align}$$

It doesn't look like we've made the problem any simpler. In fact, it looks just as difficult as before! We will continue by doing integration by parts again. We integrate the exponential and differentiate the sine. 
$$\begin{equation}\int e^{2x}\cos x \d x = \frac{1}{2}e^{2x}\cos x + \frac{1}{4}e^{2x}\sin x -  \frac{1}{4}\int e^{2x}\cos x \d x\end{equation}$$
Again, it doesn't look like the problem is any simpler. However, we are in fact almost done. Observe that the integral on the left hand side is the same as the integral on the right hand side! If we move them both to the same side, then we get 

$$\begin{align}
\left(1 + \frac{1}{4}\right)\int e^{2x}\cos x \d x ={}& \frac{1}{2}e^{2x}\cos x + \frac{1}{4}e^{2x}\sin x \\
\frac{5}{4}\int e^{2x}\cos x \d x ={}& \frac{1}{4}e^{2x}(2\cos x + \sin x)
\end{align}$$

Thus, dividing both sides by the constant we find the final result 

$$\begin{equation}\int e^{2x}\cos x \d x = \frac{1}{5}e^{2x}(2\cos x + \sin x) + C\end{equation}$$


</div>

<div class="example">
<b>Example:</b>
Evaluate the integral

$$\begin{equation}\int \log x \d x \end{equation}$$


<b>Solution:</b> To solve this problem, we have to introduce an extra 1 inside the integral, which of course doesn't actually change anything. 

$$\begin{equation}\int \log x \d x = \int 1\log x \d x\end{equation}$$

If we integrate the \(1\) and differentiate the logarithm, then we find that 

$$\begin{align}
\int 1\log x \d x ={}& x\log x - \int x\frac{1}{x} \d x \\
={}& x\log x - \int 1 \d x 
\end{align}$$

The integral of 1 is simply \(x\), so we get our final answer 

$$\begin{equation}\int \log x \d x = x\log x - x + C\end{equation}$$

</div>

<div class="example">
<b>Example:</b>
Evaluate the integral
$$\begin{equation}\int \arcsin x \d x \end{equation}$$

<b>Solution:</b> We proceed just like in the last example by introducing a 1. 

$$\begin{equation}\int \arcsin x \d x  = \int 1\arcsin x \d x \end{equation}$$

We integrate the 1 and differentiate the arcsine. 

$$\begin{equation}\int 1\arcsin x \d x = x\arcsin x - \int \frac{x}{\sqrt{1-x^2}} \d x\end{equation}$$

The resulting integral can be done with a \(u\)-substitution. Letting \(u = 1-x^2\), we leave the details to the reader and find 

$$\begin{equation}\int \arcsin x \d x = x\arcsin x + \sqrt{1-x^2} + C\end{equation}$$


</div>


