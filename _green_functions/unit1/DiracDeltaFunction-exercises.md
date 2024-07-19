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

</div> </li></ol>

