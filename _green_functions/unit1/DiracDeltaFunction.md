---
layout: lesson
title: Dirac Delta Function 
dept: math
course: green_functions
unit: unit1
deptDisplay: Math
courseDisplay: Green functions
unitDisplay: Unit 1
---
The Dirac delta function \\(\delta(x)\\) is a function which is extremely sharply peaked at \\(x = 0\\). Strictly speaking, it is not a function at all, but rather a distribution. We will not delve into the theory of distributions in these notes, but rather treat it as a function that has some unusual properties.

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

There are other properties of the delta function that we will find useful.

<u>Sifting Property</u>
If \\(f(x)\\) is a continuous function for \\(x \in[x_1,x_2]\\), and if \\(x_0\in(x_1,x_2)\\), then

$$\begin{equation}
\int_{x_1}^{x_2}f(x)\delta(x-x_0) \d x = f(x_0).
\end{equation}$$

There is another definition of the Dirac delta function. 

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

A delta sequence looks like in the following plot:

<figure class="center">
<p><img src="figures/gaussian_delta_sequence.pdf" alt="Function" class="center" style="width:125.64px;height:114.149px;"> </p><figcaption class="center">A delta sequence constructed out of Gaussian functions, \(f_k = \sqrt{\frac{k</figcaption>{\pi</figcaption></figcaption>e^{-kx^2</figcaption>\), where we have plotted \(k=1,2,3,4,5\).</figcaption>
</figure>

There are many examples of delta sequences. 

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

<div class="example">
<b>Example:</b>
Find \(M\) such that the following sequence of functions is a delta sequence as \(\epsilon\to 0\).
$$\begin{equation}
f_k(x) = \frac{M}{\epsilon}\sech^2\frac{x}{\epsilon}
\end{equation}$$

<b>Solution:</b>

(\(M = 1/2\)).


</div>

We are able to give meaning to certain expressions involving delta functions. Examples are \\(x\delta(x)\\), \\(f(x)\delta'(x)\\), and \\(\delta(f(x))\\). 

The rigorous approach was due to Laurent Schwartz. 

<div class="definition">
<b>Definition:</b>
A function \(\phi(x)\) is called a test function if \(\phi(x)\) is infinitely differentiable and vanishes outside some finite interval. (i.e., it has compact support)

</div>

<div class="example">
<b>Example:</b>
An example of a test function is 

$$\begin{equation}
\phi(x) = \begin{cases}
	\exp\left(-\frac{a^2}{a^2-x^2}\right) & |x| < a\\ 0 & |x| \geq a
\end{cases}
\end{equation}$$

</div>

We will look at generalized functions \\(f(x)\\) (such as expressions involving delta functions) only through their actions on test functions \\(\phi(x)\\) via the functional

$$\begin{equation}
\left< f,\phi\right> = \int_{-\infty}^\infty f(x)\phi(x) \d x
\end{equation}$$

The delta function \\(f(x) = \delta(x)\\) is defined by the sifting property such that

$$\begin{equation}
\int_{-\infty}^\infty f(x)\phi(x) \d x = \phi(0)
\end{equation}$$

for any test function \\(\phi(x)\\). 

Note: Defining \\(\delta(x)\\) by the above equation allows us to show that Dirac's formal definition that \\(\delta(x) = 0\\) for \\(x\not=0\\) and \\(\int_{-\infty}^\infty \delta(x) \d x = 1\\) holds. 

Claim 1: If this holds for all \\(\phi(x)\\) test functions, then \\(f(x) = 0\\) for \\(x\not = 0\\). 

The idea of the proof is, suppose that \\(f(x_0) \not=0\\) for \\(x_0\not=0\\); without loss of generality set \\(x_0 > 0\\). Thus, 

$$\begin{equation}
\phi(0) = 0 \not= \int \phi f
\end{equation}$$

so it cannot hold. 

Claim 2: \\(\int_{-\infty}^\infty f(x) \d x = 1\\) if \\(f(x) = 0\\) for \\(x\not=0\\). 

Thus

$$\begin{equation}
\int_{-\infty}^\infty f(x)\phi(x) \d x = \phi(0) \int_{-\infty}^\infty f(x) \d x
\end{equation}$$

holds if \\(\int_{-\infty}^\infty f(x) \d x = 1\\). 

<div class="definition">
<b>Definition:</b>
Let \(f_k(x)\) be a sequence of functions (possibly a delta sequence). We say that \(f_k(x)\to f(x)\) as \(k\to\infty\) <i>weakly</i> if 

$$\begin{equation}
\lim_{k\to\infty}(f_k,\phi) = \left<f,\phi\right>
\end{equation}$$

for any test function \(\phi(x)\).

</div>

Recall that we defined test functions \\(\phi(x)\\) as infinitely smooth (\\(C^\infty\\)), with compact support (vanish outside some finite interval). 

Recall that we defined \\(\delta(x-x_0)\\) via the sifting property, 

$$\begin{equation}
\inf_{-\infty}^\infty \delta(x-x_0) \phi(x) \d x = \phi(x_0).
\end{equation}$$

<div class="definition">
<b>Definition:</b>
Let \(f_k(x)\) be a sequence of generalized functions. We say that 

$$\begin{equation}
f_k(x)\to f(x),\text{as} k\to\infty
\end{equation}$$

weakly, if 

$$\begin{equation}
\lim_{k\to\infty}(f_k,\phi) = (f,\phi)
\end{equation}$$

for all \(\phi\)


</div>

<div class="example">
<b>Example:</b>
Illustration of weak convergence for a delta sequence. Let 

$$\begin{equation}
f_k(x) = \begin{cases}
	k & |x| < 1/2k \\ 0 & |x| \geq 1/2k
\end{cases}
\end{equation}$$

Non rigorously, last class, we wrote \(\lim_{k\to\infty}f_k(x) = \delta(x)\).

A better way is via weak convergence. Let \(\phi(x)\) be any test function. Then, 

$$\begin{equation}
\left< f_k,\phi\right> = \int_{-\infty}^\infty f_k(x)\phi(x) \d x = k\int_{-1/2k}^{1/2k}\phi(x) \d x 
\end{equation}$$

By the mean value theory for integrals, we can rewrite this as

$$\begin{equation}
\left<f_k,\phi \right> = k\phi(\bar{x})\left(\frac{1}{2k} - \frac{-1}{2k}\right) = \phi(\bar{x})
\end{equation}$$

Let \(k\to\infty\), and \(\bar{x}\), so that

$$\begin{equation}
\lim_{k\to\infty} \left< f_k,\phi \right> = \phi(0) = \int_{-\infty}^\infty \phi(x) \delta(x) \d x
\end{equation}$$

so \(f_k\to\delta\) weakly. 

</div>

We can this derive the following identities using the test function idea

<ol>
<li> 
$$\begin{equation}
\delta(cx) = \frac{1}{|c|}\delta(x)
\end{equation}$$
	
</li>
<li> \(\delta(x) = H'(x)\) where \(H\) is the Heaviside function.

</li>
<li> 
$$\begin{equation}
\delta(f(x)) = \sum_{k=1}^n \frac{\delta(x-x_k)}{|f'(x_k)|}
\end{equation}$$
where \(f(x_k) = 0\) for \(k = 1,\dots, n\), and \(f'(x_k)\not=0\). Note that we can only have simple zeros.
</li>
<li> \(\delta\left(\sin\frac{\pi x}{a}\right) = \frac{|a|}{\pi}\sum_{k=-\infty}^\infty \delta(x-ka)\)
</li></ol>

The derivations of these are the following. 

<ol>
	<li> $$\begin{equation}
	(\delta(cx),\phi(x)) = \int_{-\infty}^\infty \delta(cx)\phi(x) \d x
	\end{equation}$$
	let \(y = cx\) so that \(\d x = dy/c\). If \(c > 0\), we don't have to swap the integral bounds, and if \(c < 0\) we do. We can capture both cases by introducing an absolute value. 
	$$\begin{equation}
	\int_{-\infty}^\infty \frac{1}{|c|}\delta(y)\phi\left(\frac{y}{c}\right) dy = \frac{1}{|c|}\phi(0) = \left(\frac{1}{|c|}\delta(x),\phi(x)\right)
	\end{equation}$$
	
	thus, \(\delta(cx) = \frac{\delta(x)}{|c|}\).
</li>
<li> For the second identity, we consider 
$$\begin{equation}H(x) = \begin{cases}
0 & x < 0 \\ 
1 & x \geq 0
\end{cases}
\end{equation}$$
	Then, 
	
$$\begin{equation}
\int_{-\infty}^\infty H'(x) \phi(x) = -\int_{-\infty}^\infty H(x) \phi'(x) = -\int_0^\infty \phi'(x) \d x = \phi(0)
\end{equation}$$
	
Thus, 
	
$$\begin{equation}
\int_{-\infty}^\infty H'(x) \phi(x) \d x = \int_{-\infty}^\infty \delta(x) \phi(x) \d x
\end{equation}$$

</li>
<li> For this one, we let \(f(x_k) = 0\), for \(k = 1,\dots,n\), and \(f'(x_k)\not=0\). Choose \(a_k,b_k\) such that \(a_k < x_k < b_k\), and \(f(x)\) is monotonic on \([a_k,b_k]\). Then, 
$$\begin{equation}
(\delta(f(x)),\phi(x)) = \sum_{k=1}^n \int_{a_k}^{b_k}\delta(f(x))\phi(x) \d x
\end{equation}$$
	
On each subinterval, since monotonicity holds, let \(\sigma = f(x)\) so that
	
$$\begin{equation}
\frac{\d x}{d\sigma} = \frac{1}{f'(x)}
\end{equation}$$
	
Thus, when \(\sigma = 0\), \(x = x_k\). Thus, 
	
$$\begin{align}
\left<\phi(x),\delta(f(x))\right> ={}& \sum_{k=1}^n \int_{f(a_k)}^{f(b_k)} \frac{\phi(x(\sigma))}{f'(x(\sigma))}\delta(\sigma) d\sigma \\
={}& \sum_{k=1}^n \frac{\phi(x(0))}{|f'(x(0))|} \\
={}& \sum_{k=1}^n \frac{\phi(x_k)}{|f'(x_k)|} \\
={}& \int_{-\infty}^\infty \sum_{k=1}^n \frac{\delta(x-x_k)}{|f'(x_k)|}\phi(x) \d x
\end{align}$$
	</li>
<li> Lastly, let's prove the expansion of the sine identity. For thiso one, we apply the previous result with \(f(x) = \sin(\pi x/a)\). Thus \(f(x_k) = 0\) for \(x_k = ak\), where \(k\in \ZZ\). Thus \(f'(x_k) = \frac{\pi}{a}\cos\left(\frac{\pi x_k}{a}\right) = (-1)^k\frac{\pi}{a}\). Using the previous result, we find that
	$$\begin{equation}
	\delta\left(\sin\frac{\pi x}{a}\right) = \frac{|a|}{\pi}\sum_{k=-\infty}^\infty \delta(x-ak)
	\end{equation}$$
</li></ol>


