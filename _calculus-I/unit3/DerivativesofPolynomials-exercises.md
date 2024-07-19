---
layout: exercises
title: Derivatives of Polynomials  - Exercises
dept: math
course: calculus-I
unit: unit3
deptDisplay: Math
courseDisplay: Calculus I
unitDisplay: Unit 3
---
<ol>
<li> <div class="exercise">  Differentiate the following function. \(y = 2x^{1/2} + 6x^{1/3} - 2x^{3/2}\)

<div class="answerBox"> 
 <button onclick="myFunction('answer3')" class="answerButton">Show Answer</button> 
 <div  id='answer3' class="answer" >
Applying the power rule, 
$$\begin{equation}
y' = \frac{1}{\sqrt{ x}} + \frac{2}{x^{2/3}} - 3 \sqrt{x}
\end{equation}$$
</div> 
 </div>

</div> </li>
<li> <div class="exercise">  Differentiate the following function. 
$$\begin{equation}
f(x) = \frac{x^3 - 5x^2 + 2x - 9}{x^2}
\end{equation}$$

<div class="answerBox"> 
 <button onclick="myFunction('answer15')" class="answerButton">Show Answer</button> 
 <div  id='answer15' class="answer" >
Simplifying, 
$$\begin{equation}
f(x) = x - 5 + \frac{2}{x} - \frac{9}{x^2}
\end{equation}$$
Applying the power rule yields, 
$$\begin{equation}
f'(x) = 1 - \frac{2}{x^2} + \frac{18}{x^3}
\end{equation}$$
</div> 
 </div>


</div> </li>
<li> <div class="exercise">  Evaluate the limit $$\begin{equation}\lim_{x\to -4}\frac{x^{1001} + 4^{1001}}{x + 4}\end{equation}$$

<div class="answerBox"> 
 <button onclick="myFunction('answer29')" class="answerButton">Show Answer</button> 
 <div  id='answer29' class="answer" >
First, notice that the limit resembles the definition of the derivative of the form 
$$\begin{equation}
\lim_{x\to a} \frac{f(x)-f(a)}{x-a}
\end{equation}$$ 
where \(f(x)=x^{1001}\) and \(a=-4\). Then, write out the limit in the form of a derivative.

$$\begin{align}
\lim_{x\to -4}\frac{x^{1001} + 4^{1001}}{x + 4} ={}& \frac{\d}{\d x}(x^{1001}) \bigg|_{x=-4}\\
={}& 1001x^{1000} \bigg|_{x=-4} \\
={}& 1001(-4)^{1000} \\
={}& 1001 \cdot 4^{1000}
\end{align}$$
</div> 
 </div>

</div> </li></ol>



