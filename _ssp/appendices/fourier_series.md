---
layout: lesson
title: Fourier Series
dept: physics
course: ssp
unit: appendices
deptDisplay: Physics
courseDisplay: Solid State Physics
unitDisplay: Appendices
---

### One Dimensional Fourier Series

We recall from math class that if we had a (real valued) function $f(x)$ of period $L$ we could expand it in the form

$$f(x) = \frac{a_0}{2} + \sum_{n=1}^\infty a_n\cos\left(\frac{2n\pi x}{L}\right) + b_n \sin\left(\frac{2n\pi x}{L}\right)$$

and the coefficients $a_n$ and $b_n$ could be found by orthogonality. The formulas were

$$a_n = \frac{2}{L} \int_0^{L} f(x) \cos\left(\frac{2n\pi x}{L}\right) dx ,\qquad b_n = \frac{2}{L} \int_0^{L} f(x) \sin\left(\frac{2n\pi x}{L}\right) dx. $$

Instead of expanding $f(x)$ in terms of sines and cosines, one can write this in terms of complex exponentials. Using the formulas

$$\sin\theta = \frac{e^{i\theta} - e^{-i\theta}}{2i},\qquad \cos\theta = \frac{e^{i\theta} + e^{-i\theta}}{2},$$

we can rewrite the Fourier series as

$$f(x) = \frac{a_0}{2} + \sum_{n=1}^\infty a_n\left(\frac{e^{i 2n\pi x/L} + e^{-i2n\pi x/L}}{2}\right)  + b_n \left(\frac{e^{i 2n\pi x/L} - e^{-i2n\pi x/L}}{2i}\right)$$

If we collect like terms, then we get 

$$f(x) = \frac{a_0}{2} + \sum_{n=1}^\infty \frac{1}{2}(a_n - ib_n) e^{i 2n\pi x/L} + \frac{1}{2} (a_n + ib_n) e^{-i2n\pi x/L}.$$

If we notice that, although we never had $n$ negative, we could technically plug in a negative $n$ into our formula for $a_n$ and $b_n$, then we find the relations $a_n = a_{-n}$ and $b_{n} = -b_{-n}$. Thus, defining $c_n = \frac{a_n - ib_n}{2} $, we have that $c_n^* = c_{-n}$. We now rewrite the sum in terms of the coefficients $c_n$. 

$$f(x) = c_0+ \sum_{n=1}^\infty c_n e^{i 2n\pi x/L} + c_n^* e^{-i2n\pi x/L}.$$

Now, we note that we can split this into two sums. 

$$f(x) = c_0+ \sum_{n=1}^\infty c_n e^{i 2n\pi x/L} + \sum_{n=1}^\infty c_n^* e^{-i2n\pi x/L}.$$

Now, in the second sum we relabel $n$ as $-n$. 

$$f(x) = c_0+ \sum_{n=1}^\infty c_n e^{i 2n\pi x/L} + \sum_{n=-\infty}^{-1} c_{-n}^* e^{i2n\pi x/L}.$$

Replacing $c_{-n}^*$ by $c_n$, 

$$f(x) = c_0+ \sum_{n=1}^\infty c_n e^{i 2n\pi x/L} + \sum_{n=-\infty}^{-1} c_n e^{i2n\pi x/L}.$$

and we can thus write this as a single sum over $n$. 

$$f(x) = \sum_{n=-\infty}^\infty c_n e^{i 2n\pi x/L}.$$

Now, we define $k_n = 2n\pi/L$. 

$$f(x) = \sum_{n=-\infty}^\infty c_n e^{ik_n x}.$$

This is the Fourier series in terms of the complex exponential for a real valued function $f(x)$ of a single real variable with period $L$. 

We now have different formulas for the coefficients $c_n$. The formula is

$$c_n = \frac{1}{L} \int_0^L f(x) e^{-ik_n x} dx$$ 

You will prove this formula in the exercises.

### Three Dimensional Fourier Series
Now that we have written our Fourier series in terms of the complex exponential, it is easy to generalize this to higher dimensions. We consider now a function $f(\x)$, which is a function of a vector variable $\x = (x_1,x_2, x_3)$ (or $\x = (x,y,z)$ if you prefer). Suppose that $f(\x)$ is periodic in all three directions. It has period $L_1$ in the $x$ direction, $L_2$ in the $y$ direction, and $L_3$ in the $z$ direction. Thus, 

$$f(x + n_1 L_1, y + n_2 L_2, z + n_3 L_3) = f(x,y,z)$$

for any integers $n_1, n_2,n_3$. Consider the three vectors $(L_1,0,0)$, $(0,L_2,0)$, and $(0,0,L_3)$. Then, we expand $f(\x)$ in terms of functions that are periodic when translating $\x$ by any of those three vectors. Such functions are

$$e^{i\k_\textbf{n}\cdot\x}.$$

where $\k_\textbf{n}$ are the vectors

$$\k_{n_1 n_2 n_3} = \left(\frac{2n_1\pi}{L_1},\frac{2n_2 \pi}{L_2}, \frac{2n_3\pi}{L_3} \right).$$

Thus, we write the Fourier series as 

$$f(\x) = \sum_{n_1}\sum_{n_2}\sum_{n_3} c_{n_1 n_2 n_3} e^{i\k_{n_1 n_2 n_3}\cdot\x}$$

where the coefficients are given by

$$c_{n_1 n_2 n_3} = \frac{1}{L_1 L_2 L_3} \int_0^{L_1}\int_0^{L_2} \int_0^{L_3} f(\x) e^{-i k_{n_1 n_2 n_3}\cdot \x} dx dy dz $$

One can define the volume $V = L_1 L_2 L_3$ and get 

$$c_{n_1 n_2 n_3} = \frac{1}{V} \int_0^{L_1}\int_0^{L_2} \int_0^{L_3} f(\x) e^{-i k_{n_1 n_2 n_3}\cdot \x} dx dy dz $$

In the vector notation,  















