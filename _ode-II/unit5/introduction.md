---
layout: lesson
title: Introduction
dept: math
course: ode-II
unit: unit5
deptDisplay: Math
courseDisplay: Ordinary Differential Equations II
unitDisplay: Unit 5
---

The Fourier transform is ubiquitous throughout mathematics, physics, and engineering. In this section, we will study how it can be used to find integral representations of solutions to certain ODEs, thus making them easier to solve. For example, the Airy equation $y'' = xy$ which we solved by series methods earlier can also have its solution be represented by an integral! In this section, we will introduce the idea of the Fourier transform and some definitions. This section will require the reader to know the calculus of complex variables. 

The following definition of the Fourier transform is one of many conventions. Sometimes, the $1/\sqrt{2\pi}$ coefficient in front is not there, or the sign in the exponential is $+ikx$ instead of $-ikx$. As a physicist, this is the convention that I normally use. I will present a table of the two most commonly used conventions later.

<div class="definition">
Let $f : \mathbb{R}\to\mathbb{C}$ be a function which decays sufficiently rapidly at infinity such that the integral
$$\mathcal{F}(f)(k) = \frac{1}{\sqrt{2\pi}}\int_{-\infty}^\infty e^{-ikx} f(x) dx $$
converges. Then $\hat{f}(k) = \mathcal{F}(f)(k)$ is called the <i>Fourier transform</i> of $f$.
</div>

Conceptually, this should be thought of as a continuous analogue of Fourier series. In the study of Fourier series, we found two ways of representing a $2L$-periodic function by a Fourier series. One was with sines and cosines, but the other was with complex exponentials. The representation in terms of complex exponentials is 

$$f(x) = \sum_{n=-\infty}^\infty c_n e^{in\pi x/L} ,$$

where the coefficients $c_n$ are given by 

$$c_n = \frac{1}{L}\int_{-L}^L f(x) e^{-in\pi x/L} dx.$$

Our interpretation for the coefficients $c_n$ was that they represent the *amount* of the frequency $k_n = n\pi/L$ that the function $f$ contained. We note that the bigger $L$ gets, the finer spaced the $k_n$ values are; we can allow for higher frequencies. Allowing for higher frequencies allows us to expand functions with *less* periodicity, by which we mean functions with longer periods. If we consider making the period infinitely long, it would mean that $k_n$ can take on any real value, instead of just integers multiplied by $\pi/L$. We are thus led to consider the *continuous variable* $k$, which would give us something like 

$$c_k = \frac{1}{L}\int_{-L}^L f(x) e^{-ikx} dx.$$

We can see that this formula for $c_k$ is very similar to $\hat{f}(k) = \mathcal{F}(f)(k)$. Thus this leads naturally to our interpretation for the Fourier transform of a function. The Fourier transform $\hat{f}(k)$ of a function $f(x)$ is, as before, the amount of frequency $k$ contained in the original function $f$. 

There are certain functions whose Fourier transforms will be frequently used. These will be collected in a table. To understand where these come from, we will start by calculating some elementary examples. 

<div class="example">
<p> <b>Example:</b> Calculate the Fourier transform of the Dirac delta function $f(x) = \delta(x-x')$. The number $x'$ is a constant. </p>

<p> <b>Solution:</b> </p>
The Fourier transform is found by directly plugging in the delta function. 
$$\begin{eqnarray}
\hat{f}(k) &=& \frac{1}{\sqrt{2\pi}}\int_{-\infty}^\infty \delta(x-x')e^{-ikx} dx \\
&=& e^{-ikx'}
\end{eqnarray}$$
The integral is easily soluble because of the sifting property of the delta function. 
</div> 

<div class="example">
<p> <b>Example:</b> Calculate the Fourier transform of the Gaussian function $f(x) = e^{-ax^2)$. The (real) number $a$ is a constant. </p>

<p><b>Solution:</b></p>
In order to evaluate this integral, we will have to use Cauchy's integral theorem. 
</div>

One may then ask, what happens if someone gives me the Fourier transform of a function, and I need to find the original function? For that, we can apply the *inverse Fourier transform*.  The inverse Fourier transform is 

$$f(x) = \mathcal{F}^{-1}(\hat{f})(x) = \frac{1}{\sqrt{2\pi}}\int_{-\infty}^\infty \hat{f}(k) e^{ikx} dk$$

and it returns the function $f(x)$ given $f(x)$'s Fourier transform $\hat{f}(k)$. The inverse Fourier transform is in general just as easy (or difficult) to calculate as the forward Fourier transform. 
