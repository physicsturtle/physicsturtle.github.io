---
layout: exercises
title: Dirac Delta Function  - Exercises
dept: math
course: green_functions
unit: unit1
deptDisplay: Math
courseDisplay: Green functions
unitDisplay: Unit 1
---
<ol>
<li> <div class="exercise">  Suppose \(f(x)\) is continuous at \(x_0\). Using the two defining properties of the delta function, prove the sifting property

$$\begin{equation}\int_{-\infty}^\infty f(x) \delta(x-x_0) \d x = f(x_0).\end{equation}$$

<div class="answerBox"> 
 <button onclick="myFunction('answer5')" class="answerButton">Show Answer</button> 
 <div  id='answer5' class="answer" >
Since \(\delta(x) = 0\) for all \(x\neq 0\). Thus we can write

$$\begin{equation}\int_{-\infty}^\infty f(x) \delta(x-x_0) \d x = \int_{-\infty}^\infty f(x+x_0)\delta(x) \d x = \int_{-\epsilon}^\epsilon f(x+x_0) \delta(x) \d x.\end{equation}$$

for any \(\epsilon > 0\).

</div> 
 </div>

</div> </li>
<li> <div class="exercise">  Construct a delta sequence out of functions of the form 

$$\begin{equation}
f_\epsilon(x) = \frac{C\epsilon}{x^2+\epsilon^2}
\end{equation}$$

as \(\epsilon \to 0\). Also determine the constant \(C\) as you go.

<div class="answerBox"> 
 <button onclick="myFunction('answer22')" class="answerButton">Show Answer</button> 
 <div  id='answer22' class="answer" >


We find 

\(\)\lim_{\epsilon\to 0} f_\epsilon(x) = C\pi\delta(x)\(\)
</div> 
 </div>

</div> </li>
<li> <div class="exercise">  By introducing a regularization factor \(e^{-\epsilon|n|}\) on the left hand side, prove the identity

$$\begin{equation}
\sum_{n\in\ZZ} e^{inx} = 2\pi\sum_{\bar{n}\in\ZZ} \delta(x-2\pi\bar{n})
\end{equation}$$

<div class="answerBox"> 
 <button onclick="myFunction('answer36')" class="answerButton">Show Answer</button> 
 <div  id='answer36' class="answer" >
The first thing we do is evaluate

$$\begin{align}
f_\epsilon(x) ={}& \sum_{n\in \ZZ} e^{inx} e^{-\epsilon|n|} \\
={}& \frac{1}{1-e^{ix-\epsilon}} + \frac{1}{1-e^{-ix-\epsilon}}-1\\
={}& \frac{\sinh \epsilon}{\cosh\epsilon - \cos x}
\end{align}$$

We note that, if \(x\neq 2\pi n\) for integer \(n\), then 

\(\)\lim_{\epsilon\to 0} f_\epsilon(x) = 0\(\)

Now, the question is what happens at \(x = 2\pi n\)? Well, we integrate the function \(f_\epsilon(x)\) over the interval \((2\pi n -\delta , 2\pi n + \delta)\). Since the function is periodic, we might as well do this around \(x=0\); the same result occurs around any point. 

$$\begin{align}
\int_{-\delta}^\delta f_\epsilon(x) \d x ={}& 2\arctan\left(\tan\left(\frac{x}{2}\right)\sqrt{\frac{\cosh\epsilon+1}{\cosh\epsilon-1}}\right)\bigg|_{-\delta}^\delta \\
\sim{}& 4\arctan\left(\frac{\sqrt{2}}{\epsilon}\tan\left(\frac{\delta}{2}\right)\right) \\
\sim{}& 2\pi
\end{align}$$

This tells us that, in the neighbourhood of \(x=0\), we have that \(\lim_{\epsilon\to 0} f_\epsilon(x) = 2\pi\delta(x)\). If we then include the periodicity of \(f\), we find that 

$$\begin{equation}
f(x) = \lim_{\epsilon\to 0} f_\epsilon(x) = 2\pi\sum_{\bar{n}\in \ZZ} \delta(x - 2\pi \bar{n})
\end{equation}$$

Thus, we have proven the result.

</div> 
 </div> 

</div> </li>
<li> <div class="exercise">  Consider the function \(f_a(x) = \frac{1}{4a\cosh^2(x/2a)}\). 

<ol type="a">
<li> Develop a Taylor expansion for small \(a\) as \(a \to 0^+\). Do this up to second order in \(a\). 
<ol type="i">
<li> Compute \(\lim_{a\to 0^+} \partial_a f_a(x)\).
</li>
<li> Compute \(\lim_{a\to 0^+} \partial^2_a f_a(x)\).
</li>
<li> What does this give us for the Taylor expansion?
</li></ol>
</li>
<li> Can you guess the expansion for arbitrary orders of \(a\)?
</li>
<li> Does your guess for the Taylor expansion converge? Should it converge, or not?
</li></ol>
This problem underlies the so-called <i>Sommerfeld expansion</i> in statistical physics, which is useful to compute low-temperature properties of weakly interacting fermion systems.

<div class="answerBox"> 
 <button onclick="myFunction('answer81')" class="answerButton">Show Answer</button> 
 <div  id='answer81' class="answer" >
<ol type="a">
<li> We see right away that, as \(a\to 0^+\), \(f_a(x) \to \delta(x)\), by the result of an earlier exercise. 
<ol type="i">
<li> Since we want to expand for small \(a\), we need to compute derivatives with respect to \(a\). In particular, we have that 

$$\begin{align}
\partial_a f_a(x) ={}& -\frac{1}{4a^2\cosh^2(x/2a)} + \frac{x\sinh(x/2a)}{4a^3\cosh^3(x/2a)} \\
={}& -\frac{1}{a}\left(\frac{1}{4a\cosh^2(x/2a)}\right) - \frac{x}{a}\left(-\frac{\sinh(x/2a)}{4a^2\cosh^3(x/2a)}\right)
\end{align}$$

We note that we can rewrite this derivative in a very convenient way by observing that 

\(\)\partial_x f_a(x) = -\frac{\sinh(x/2a)}{4a^2\cosh^3(x/2a)}\(\)

Thus we have 

$$\begin{align}
\partial_a f_a(x) ={}& -\frac{1}{4a^2\cosh^2(x/2a)} + \frac{x\sinh(x/2a)}{4a^3\cosh^3(x/2a)} \\
={}& -\frac{1}{a}f_a(x) - \frac{x}{a}\partial_x f_a(x)
\end{align}$$

In order to understand the behaviour of \(\partial_a f_a(x)\) as \(a\to 0\), we integrate it against a test function. We find that 

$$\begin{align}
\int_{-\infty}^\infty \phi(x) \partial_a f_a(x) \d x ={}& \int_{-\infty}^\infty \left(-\frac{1}{a}f_a(x) - \frac{x}{a}\partial_x f_a(x)\right) \phi(x) \d x \\
={}& -\frac{1}{a}\int_{-\infty}^\infty f_a(x) \phi(x) \d x - \frac{1}{a}\int_{-\infty}^\infty x \partial_x f_a(x) \phi(x) \d x \\ 
={}& -\frac{1}{a}\int_{-\infty}^\infty f_a(x) \phi(x) \d x - \frac{1}{a}\left(x\phi(x) f_a(x)\right)\bigg|_{-\infty}^\infty + \frac{1}{a}\int_{-\infty}^\infty \partial_x(x\phi(x)) f_a(x) \d x \\
={}& -\frac{1}{a}\int_{-\infty}^\infty f_a(x) \phi(x) \d x + \frac{1}{a}\int_{-\infty}^\infty (x\phi'(x) + \phi(x)) f_a(x) \d x \\
={}& \frac{1}{a}\int_{-\infty}^\infty x \phi'(x) f_a(x) \d x
\end{align}$$

If the test function \(\phi(x)\) is odd, then this is automatically zero. But, what if the test function is even? Well, then we need to take the limit as \(a\to 0^+\). The denominator obviously goes to zero, which is not good! However, we note that the numerator goes to zero as well. Which goes to zero faster? Let's consider setting \(x/a = y\), so then 

$$\begin{align}
\lim_{a\to 0^+} \frac{1}{a}\int_{-\infty}^\infty x \phi'(x) f_a(x) \d x ={}& \lim_{a\to 0^+} \frac{1}{a}\int_{-\infty}^\infty x \phi'(x) \frac{1}{4a\cosh^2(x/2a)} \d x \\
={}& \lim_{a\to 0^+} \frac{1}{a} \int_{-\infty}^\infty ay \phi'(ay) \frac{1}{4a\cosh^2(y/2)} a \d y \\
={}& \lim_{a\to0^+} \int_{-\infty}^\infty \frac{y\phi'(ay)}{4\cosh^2(y/2)} \d y
\end{align}$$

 Since the integrand is analytic, we can take the limit inside, and get 

$$\begin{align}
\lim_{a\to 0^+} \frac{1}{a}\int_{-\infty}^\infty x \phi'(x) f_a(x) \d x ={}& \int_{-\infty}^\infty \frac{y\phi'(0)}{4\cosh^2(y/2)} \d y \\
={}& 0
\end{align}$$

In the last step, we get 0 because the integrand is odd. 

</li>
<li> We have that the second derivative is given by 

$$\begin{align}
\partial_a^2 f_a(x) ={}& \frac{1}{a^2} f_a(x) - \frac{1}{a}\partial_a f_a(x) + \frac{x}{a^2}\partial_x f_a(x) - \frac{x}{a}\partial_x \partial_a f(x) \\
={}& \frac{1}{a^2} f_a(x) + \frac{1}{a}\left(\frac{1}{a} f_a(x) + \frac{x}{a}\partial_x f_a(x)\right) + \frac{x}{a^2}\partial_x f_a(x) + \frac{x}{a}\partial_x \left(\frac{1}{a} f_a(x) + \frac{x}{a}\partial_x f_a(x)\right) \\
={}& \frac{2}{a^2}f_a(x) + \frac{4x}{a^2}\partial_x f_a(x) + \frac{x^2}{a^2}\partial_x^2 f_a(x)
\end{align}$$ 

Next, to understand the nature of this function, we integrate it against a test function. This gives us 

$$\begin{align}
\int_{-\infty}^\infty \phi(x) \partial_a^2 f_a(x) \d x ={}& \int_{-\infty}^\infty\left(\frac{2}{a^2}f_a(x) + \frac{4x}{a^2}\partial_x f_a(x) + \frac{x^2}{a^2}\partial_x^2 f_a(x)\right) \phi(x) \d x \\
={}& \frac{1}{a^2}\int_{-\infty}^\infty\left(2f_a(x)\phi(x) - 4f_a(x)(x\phi(x))' + f_a(x)(x^2\phi(x))"\right) \d x \\
={}& \frac{1}{a^2}\int_{-\infty}^\infty\left(2\phi(x) - 4(x\phi(x))' + (x^2\phi(x))"\right) \frac{1}{4a\cosh^2(x/2a)} \d x \\
={}& \frac{1}{a^2}\int_{-\infty}^\infty \frac{2\phi(x) - 4(x\phi'(x) + \phi(x)) + (x^2\phi"(x) + 4x\phi'(x) + 2\phi(x))}{4a\cosh^2(x/2a)} \d x \\
={}& \frac{1}{a^2}\int_{-\infty}^\infty \frac{x^2\phi"(x)}{4a\cosh^2(x/2a)} \d x 
\end{align}$$

We make the same variable substitution \(x/a = y\), and get 

$$\begin{align}
\int_{-\infty}^\infty \phi(x) \partial_a^2 f_a(x) \d x ={}& \int_{-\infty}^\infty \frac{y^2\phi"(ay)}{4\cosh^2(y/2)} \d y
\end{align}$$

Now taking the limit as \(a\to 0\), we get 

$$\begin{align}
\lim_{a\to 0^+} \int_{-\infty}^\infty \phi(x) \partial_a^2 f_a(x) \d x ={}& \int_{-\infty}^\infty \frac{y^2\phi"(0)}{4\cosh^2(y/2)} \d y \\
={}& \phi"(0)2\int_{-\infty}^\infty \frac{z^2 \d z}{\cosh^2(z)} 
\end{align}$$

Then we use the common integration result 

$$\begin{equation}
\int_{-\infty}^\infty \frac{z^2 \d z}{\cosh^2(z)} = \frac{\pi^2}{6}
\end{equation}$$

which gives us 

$$\begin{align}
\lim_{a\to 0^+} \int_{-\infty}^\infty \phi(x) \partial_a^2 f_a(x) \d x ={}& \phi"(0)\frac{\pi^2}{3} \\
={}& \frac{\pi^2}{3} \int_{-\infty}^\infty \delta"(x) \phi(x) \d x
\end{align}$$

From this, we conclude that 

$$\begin{equation}
\lim_{a\to 0^+} \partial_a^2 f_a(x) = \frac{\pi^2}{3}\delta"(x)
\end{equation}$$

</li>
<li> We have seen that 

$$\begin{align}
\lim_{a\to 0^+} f_a(x) ={}& \delta(x) \\
\lim_{a\to 0^+} \partial_a f_a(x) ={}& 0 \\
\lim_{a\to 0^+} \partial_a^2 f_a(x) ={}& \frac{\pi^2}{3}\delta"(x)
\end{align}$$

Now using the Taylor expansion below

$$\begin{align}
f_a(x) = \sum_{n=0}^\infty \frac{a^n}{n!}\left(\frac{\partial^n}{\partial a^n} f_a(x)\right)\bigg|_{a\to0^+}
\end{align}$$

we have that, as \(a\to 0^+\), 

$$\begin{equation}
f_a(x) \approx \delta(x) + \frac{\pi^2a^2}{6}\delta"(x)
\end{equation}$$
 
</li></ol>

 
 
</li></ol>
</div> 
 </div>


</div> </li></ol>

