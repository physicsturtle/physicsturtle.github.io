---
layout: lesson
title: Test functions 
dept: math
course: green_functions
unit: unit1
deptDisplay: Math
courseDisplay: Green functions
unitDisplay: Unit 1
---
We are able to give meaning to certain expressions involving delta functions. Examples are \\(x\delta(x)\\), \\(f(x)\delta'(x)\\), and \\(\delta(f(x))\\). The rigorous approach was due to Laurent Schwartz. In order to do this, one has to introduce the notion of a <i>test function</i>.

<div class="definition">
<b>Definition:</b>
A function \(\phi(x)\) is called a test function if \(\phi(x)\) is infinitely differentiable and vanishes outside some finite interval. (i.e. it has compact support)

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

Test functions are mostly useful when they are acted upon by some object. This object could be a derivative, or they could be inside an integral. We care about functions inside an integral because of the following generalization of the dot product from linear algebra. In particular, we will look at generalized functions \\(f(x)\\) (by generalized function, we also mean distribution or some expression involving Dirac delta functions) through their actions on test functions \\(\phi(x)\\) via the functional known as the <i>inner product</i>. 

<div class="definition">
<b>Definition:</b>
The <i>inner product</i> between (generalized) functions \(f\) and \(g\) is defined by

$$\begin{equation}
\left< f,\phi\right> = \int_{-\infty}^\infty f(x)\phi(x) \d x
\end{equation}$$

</div>

This definition generalizes the dot product from linear algebra. In linear algebra, if we have two vectors \\(\mathbf{u}\\) and \\(\mathbf{v}\\), then their dot product is given by 

$$\begin{equation}
\langle \mathbf{u}, \mathbf{v} \rangle = \mathbf{u}\cdot\mathbf{v} = \sum_{i=1}^d u_i v_i
\end{equation}$$

In this analogy, the discrete index \\(i\\) is replaced by the continuous index \\(x\\), and the sum over \\(i\\) is replaced by an integral over \\(x\\). In this way, we have generalized the notion of inner product to vector spaces consisting of functions.

It is now possible to reframe the Dirac delta function's sifting property in terms of the inner product. We recall that, setting \\(f(x) = \delta(x)\\), it satisfies the sifting property

$$\begin{equation}
\int_{-\infty}^\infty f(x)\phi(x) \d x = \phi(0)
\end{equation}$$

for any test function \\(\phi(x)\\). Note: Defining \\(\delta(x)\\) by the above equation allows us to show that Dirac's formal definition that \\(\delta(x) = 0\\) for \\(x\not=0\\) and \\(\int\_{-\infty}^\infty \delta(x) \d x = 1\\) holds. 

Claim 1: If this holds for all \\(\phi(x)\\) test functions, then \\(f(x) = 0\\) for \\(x\not = 0\\). 

The idea of the proof is, suppose that \\(f(x\_0) \not=0\\) for \\(x\_0\not=0\\); without loss of generality set \\(x\_0 > 0\\). Thus, 

$$\begin{equation}
\phi(0) = 0 \not= \int \phi f
\end{equation}$$

so it cannot hold. 

Claim 2: \\(\int\_{-\infty}^\infty f(x) \d x = 1\\) if \\(f(x) = 0\\) for \\(x\not=0\\). 

Thus

$$\begin{equation}
\int_{-\infty}^\infty f(x)\phi(x) \d x = \phi(0) \int_{-\infty}^\infty f(x) \d x
\end{equation}$$

holds if \\(\int\_{-\infty}^\infty f(x) \d x = 1\\). 

<div class="definition">
<b>Definition:</b>
Let \(f_k(x)\) be a sequence of functions (possibly a delta sequence). We say that \(f_k(x)\to f(x)\) as \(k\to\infty\) <i>weakly</i> if 

$$\begin{equation}
\lim_{k\to\infty}(f_k,\phi) = \left<f,\phi\right>
\end{equation}$$

for any test function \(\phi(x)\).

</div>

Recall that we defined test functions \\(\phi(x)\\) as infinitely smooth (\\(C^\infty\\)), with compact support (vanish outside some finite interval). 

Recall that we defined \\(\delta(x-x\_0)\\) via the sifting property, 

$$\begin{equation}
\int_{-\infty}^\infty \delta(x-x_0) \phi(x) \d x = \phi(x_0).
\end{equation}$$

<div class="definition">
<b>Definition:</b>
Let \(f_k(x)\) be a sequence of generalized functions. We say that 

$$\begin{equation}
f_k(x)\to f(x),\text{as}\, k\to\infty
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

<div class="result">
<b>Result:</b>
<ol>
<li> The first identity allows us to take constants out of a delta function:
$$\begin{equation}
\delta(cx) = \frac{1}{|c|}\delta(x)
\end{equation}$$
Note that this may appear slightly unintuitive, but an easy way to remember it is that the delta function \(\delta(cx)\) has units \([\delta(cx)] = 1/[cx]\). Thus to maintain this property the \(c\) should come out and go to the denominator.
</li>
<li> The next one says that the derivative of the Heaviside function \(H(x)\) is the delta function: \(H'(x) = \delta(x)\).

</li>
<li> Generally, if \(f(x)\) has multiple simple zeros, then the delta function should peak at each of these zeros. We can therefore write the expansion
$$\begin{equation}
\delta(f(x)) = \sum_{k=1}^n \frac{\delta(x-x_k)}{|f'(x_k)|}
\end{equation}$$
where \(f(x_k) = 0\) for \(k = 1,\dots, n\), and \(f'(x_k)\not=0\). Note that we can only have simple zeros.
</li>
<li> \(\delta\left(\sin\frac{\pi x}{a}\right) = \frac{|a|}{\pi}\sum_{k=-\infty}^\infty \delta(x-ka)\)
</li></ol>

</div>

The derivations of these are the following. 

<ol>
<li> To derive the first identity, we can do a direct computation. We have that the inner product is 
$$\begin{equation}
(\delta(cx),\phi(x)) = \int_{-\infty}^\infty \delta(cx)\phi(x) \d x
\end{equation}$$
Now we do a variable substitution, and let \(y = cx\) so that \(\d x = \d y/c\). If \(c > 0\), we don't have to swap the integral bounds, and if \(c < 0\) we do. We can capture both cases by introducing an absolute value.

$$\begin{equation}
\int_{-\infty}^\infty \frac{1}{|c|}\delta(y)\phi\left(\frac{y}{c}\right) dy = \frac{1}{|c|}\phi(0) = \left(\frac{1}{|c|}\delta(x),\phi(x)\right)
\end{equation}$$

thus, \(\delta(cx) = \frac{\delta(x)}{|c|}\).

</li>
<li> For the second identity, we consider the <i>Heaviside function</i>, (also called \(\theta\)-function or step function), defined by

$$\begin{equation}
\theta(x) = \begin{cases}
0 & x < 0 \\ 
1 & x \geq 0
\end{cases}
\end{equation}$$

Then,

$$\begin{equation}
\int_{-\infty}^\infty \theta'(x) \phi(x) = -\int_{-\infty}^\infty H(x) \phi'(x) = -\int_0^\infty \phi'(x) \d x = \phi(0)
\end{equation}$$

Thus, 

$$\begin{equation}
\int_{-\infty}^\infty \theta'(x) \phi(x) \d x = \int_{-\infty}^\infty \delta(x) \phi(x) \d x
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


