---
layout: lesson
title: Dirac delta Function 
dept: math
course: green_functions
unit: unit1
deptDisplay: Math
courseDisplay: Green functions
unitDisplay: Unit 1
---
In the previous section, we discussed the notion of a matrix inverse. As we know, a matrix \\(A\\) times its inverse equals the identity \\(\sum\_j A\_{ij}(A^{-1})\_{jk} = \delta\_{ik}\\). However, matrices have a finite number of elements in them, and their indices \\(i,j\\) in \\(A\_{ij}\\) are integers. If we have an operator \\(\int \mathcal{O}(x,x')u(x')\d x' = f(x)\\), and we want to find out what \\(u\\) is, the inverse of \\(\mathcal{O}\\) is defined by the same condition, namely \\(\int \mathcal{O}(x,x')\mathcal{O}(x',x") \d x' = \delta(x-x")\\). This continuous analogue requires us to study the properties of the Dirac delta function, which is the continuous analogue of the Kronecker delta.

The Dirac delta function \\(\delta(x)\\) is a function which is extremely sharply peaked at \\(x = 0\\). Strictly speaking, it is not a function at all, but rather a distribution. We will not delve into the theory of distributions in these notes, but rather treat it as a function that has some unusual properties. The defining properties of the delta function are the following.

<div class="definition">
<b>Definition:</b>
The <i>Dirac delta function</i> is defined to satisfy the following properties:

<ol>
<li> The area under \(\delta(x)\) is 1: 
$$\begin{equation}
\int_{-\infty}^\infty \delta(x) \d x = 1
\end{equation}$$ \\
</li>
<li> The delta function is zero everywhere except at \(x = 0\): 
$$\begin{equation}
\delta(x)  = \begin{cases}
0, & x \neq 0\\
\text{undefined} & x = 0
\end{cases}
\end{equation}$$
</li></ol>

</div>

From these defining properties, one can derive the most useful property of the delta function. This most useful property is called the <i>sifting property</i>. 

<div class="result">
<b>Result:</b>
The <i>sifting property</i> of the Dirac delta function is the following. If \(f(x)\) is a continuous function for \(x \in[x_1,x_2]\), and if \(x_0\in(x_1,x_2)\), then

$$\begin{equation}
\int_{x_1}^{x_2}f(x)\delta(x-x_0) \d x = f(x_0).
\end{equation}$$

</div>

The reason it is called the sifting property is that, if we imagine a strainer, but one which only has one hole, then the water could only flow out at that one point. This is essentially what the sifting property encodes. The role of the strainer vs. a sifter is not important, but one could equally imagine sifting flour, but only having one hole in the sieve, so that the flour can only come out of one hole.

Although the above definition of the Dirac delta function certainly suffices, it is not very useful when one is interested in constructing a Dirac delta function more practically. The other definition of a Dirac delta function is given by the following. 

<div class="definition">
<b>Definition:</b>
Consider a sequence of functions \(\{f_k(x)\}\), which satisfy the properties

$$\begin{equation}
\lim_{k\to\infty}\int_{-\infty}^\infty f_k(x) \d x = 1
\end{equation}$$

and 

$$\begin{equation}
\lim_{k\to\infty,x\not= 0} f_k(x) = 0
\end{equation}$$

If the above two properties hold, then \(\{f_k(x)\}\) is called a delta sequence. 

</div>

A delta sequence can be visualized as a sequence of functions which grow increasingly sharply peaked, but also increasingly narrow. They become narrower because their value needs to be zero outside of a very small interval, but they become increasingly sharply peaked in order to maintain the property of having area 1 underneath the curve. A simple example of a delta sequence is constructed out of Gaussian functions, as shown in Fig.~\ref{fig:gaussian_delta_sequence}

<figure class="center">
<p><img src="figures/gaussian_delta_sequence.pdf" alt="Function" class="center" style="width:125.64px;height:114.149px;"> </p><figcaption class="center">A delta sequence constructed out of Gaussian functions, \(f_k = \sqrt{\frac{k</figcaption>{\pi</figcaption></figcaption>e^{-kx^2</figcaption>\), where we have plotted \(k=1,2,3,4,5\).</figcaption> \label{fig:gaussian_delta_sequence</figcaption>
</figure>

Although we have pictured a Gaussian delta sequence, there are numerous examples of function sequences which become increasingly narrow, and increasingly sharply peaked. We note that a delta sequence need not be comprised of continuous functions! Some examples are:

<div class="example">
<b>Example:</b>
The following sequences of functions are \(\delta\) sequences as \(k\to\infty\).

<ul>
<li> The box function sequence:

$$\begin{equation}
f_k(x) = \begin{cases}
k & |x| < 1/2k \\ 
0 & |x| \geq 1/2k
\end{cases}
\end{equation}$$

</li>
<li> The tent function sequence: 

$$\begin{equation}
f_k(x) = \begin{cases}
A - k|x| & |x| < 1/k \\
0 & |x| > 1/k
\end{cases}
\end{equation}$$

</li>
<li> Gaussian function sequence:

$$\begin{equation}
f_k(x) = \sqrt{\frac{k}{\pi}}e^{-kx^2}
\end{equation}$$

</li>
<li> Lorentzian function sequence:

$$\begin{equation}
f_k(x) = \frac{1}{\pi}\frac{k}{1+k^2x^2}
\end{equation}$$
</li></ul>

</div>

Sometimes, one also encounters the situation where they know a sequence of sharply peaked functions, but it is not clear exactly if the sequence approaches a delta function, or a scalar multiple of one. Consider the following example:

<div class="example">
<b>Example:</b>
Find \(M\) such that the following sequence of functions is a delta sequence as \(\epsilon\to 0\).
$$\begin{equation}
f_\epsilon(x) = \frac{M}{\epsilon}\sech^2\frac{x}{\epsilon}
\end{equation}$$


<b>Solution:</b> We already know that, for \(x\neq 0\), as \(\epsilon \to 0\) \(f_\epsilon(x) \to 0\). On the other hand, what is the area under the curve? Well, we know that 

$$\begin{align}
\int_{-\infty}^\infty f_\epsilon(x) \d x ={}& \frac{M}{\epsilon}\int_{-\infty}^\infty \sech^2\frac{x}{\epsilon} \d x \\
={}& \frac{M}{\epsilon}\int_{-\infty}^\infty \frac{1}{\cosh^2(x/\epsilon)} \d x \\
={}& M\int_{-\infty}^\infty \frac{1}{\cosh^2(x)} \d x \\
={}& M\int_{-\infty}^\infty \frac{4}{(e^x + e^{-x})^2} \d x \\
={}& M\int_{-\infty}^\infty \frac{4e^{2x}}{(1 + e^{2x})^2} \d x \\
={}& 2M\int_0^\infty \frac{1}{(1+z)^2} \d z \\
={}& 2M\frac{-1}{1+z}\bigg|_0^\infty \\
={}& 2M
\end{align}$$

where we have set \(z = e^{2x}\) to perform the integral. In order to have area 1, we set \(M = 1/2\).

</div>

