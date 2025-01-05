---
layout: exercises
title: Propagator as a Path Integral  - Exercises
dept: physics
course: qm-V
unit: unit3
deptDisplay: Physics
courseDisplay: Quantum Mechanics V
unitDisplay: Unit 3
---
<ol>
<li> <div class="exercise">  <ol type="a">
<li> Calculate the classical action for a particle of mass \(m\) moving in a harmonic potential well \(V(x) = \frac{1}{2}m\omega^2 x^2\), where the particle starts at \(x_a\) and ends at \(x_b\).
</li>
<li> Expand a general trajectory between \(x_a\) and \(x_b\) as 
\(\)x(t) = x_\text{cl}(t) + x_q(t)\(\)

where \(x_\text{cl}\) is classical solution found in part (a), and \(x_q(t_a) = x_q(t_b) = 0\).
</li></ol>

<div class="answerBox"> 
 <button onclick="myFunction('answer9')" class="answerButton">Show Answer</button> 
 <div  id='answer9' class="answer" >

</div> 
 </div>


</div> </li>
<li> <div class="exercise">  Prove the following mathematical lemma:

\(\)\lim_{n\to\infty} \prod_{k=1}^n \left(1 + \frac{1}{n}f\left(\frac{k}{n}\right)\right) = e^{\int_0^1 f(x) \d x}\(\)

<div class="answerBox"> 
 <button onclick="myFunction('answer18')" class="answerButton">Show Answer</button> 
 <div  id='answer18' class="answer" >
Let's define 

\(\)P_n(f) = \prod_{k=1}^n \left(1 + \frac{1}{n}f\left(\frac{k}{n}\right)\right)\(\)

Then, if we take the logarithm of both sides, then 

\(\)\log P_n(f) = \sum_{n=1}^n \log\left(1 + \frac{1}{n}f\left(\frac{k}{n}\right)\right)\(\)

We have that the following inequality holds:

\(\)0 \leq x - \log(x+1) = \int_1^{x+1} \frac{t-1}{t} \d t \leq \frac{x^2}{2} = \int_1^{x+1} (t-1) \d t \(\)

Then, let's let \(x = \frac{1}{n}f\left(\frac{k}{n}\right)\). Then, we get 

\(\)0 \leq \frac{1}{n}f\left(\frac{k}{n}\right) - \log\left(1 + \frac{1}{n}f\left(\frac{k}{n}\right)\right) \leq \frac{1}{2n^2}f\left(\frac{k}{n}\right)^2\(\)

Now, let's sum both sides over \(k\). We get 

\(\)0 \leq \sum_{k=1}^n \frac{1}{n}f\left(\frac{k}{n}\right) - P_n(f) \leq \frac{1}{2n}\sum_{k=1}^n \frac{1}{n} f\left(\frac{k}{n}\right)^2\(\)

Let's now take the limit of the entire inequality, and get 

\(\)0 \leq \int_0^1 f(x) \d x - \lim_{n\to\infty} \log P_n(f) \leq \lim_{n\to\infty} \frac{1}{2n} \int_0^1 f(x)^2 \d x\(\)

Thus, we have that 

\(\)0 \leq \int_0^1 f(x) \d x - \lim_{n\to\infty} \log P_n(f) \leq 0\(\)

Thus we can conclude that 

\(\) \lim_{n\to\infty} \log P_n(f)  = \int_0^1 f(x) \d x\(\)

Exponentiating both sides gives us the result we were looking for.

</div> 
 </div>



 
    
  </div> </li></ol>

