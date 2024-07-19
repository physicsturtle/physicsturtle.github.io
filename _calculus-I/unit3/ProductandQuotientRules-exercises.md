---
layout: exercises
title: Product and Quotient Rules  - Exercises
dept: math
course: calculus-I
unit: unit3
deptDisplay: Math
courseDisplay: Calculus I
unitDisplay: Unit 3
---
<ol>
<li> <div class="exercise">  Let the function \(t\) be defined by
$$\begin{equation}
t(x) = \frac{u(x)}{\sin x}
\end{equation}$$ and suppose \(u(\pi/3) = 4\) and \(u'(\pi/3) = -1\). Find \(t'(\pi/3)\)\\

<div class="answerBox"> 
 <button onclick="myFunction('answer6')" class="answerButton">Show Answer</button> 
 <div  id='answer6' class="answer" >
Apply the quotient rule on 

$$\begin{equation}
t(x)=\frac{u(x)}{\sin x}
\end{equation}$$

This gives us 

$$\begin{align}
\frac{\d t}{\d x} ={}&\frac{(\sin x)(\frac{\d u}{\d x})-(u)(\frac{\d}{\d x}\sin x)}{(\sin x)^2}\\
={}& \frac{(\sin x)(u'(x))-(u(x))(\cos x)}{(\sin x)^2}
\end{align}$$
Now evaluating at \(x = \pi/3\):
$$\begin{align}
t'\left(\frac{\pi}{3}\right)={}&\frac{(\sin \frac{\pi}{3})(u'(\frac{\pi}{3}))-(u(\frac{\pi}{3}))(\cos \frac{\pi}{3})}{(\sin \frac{\pi}{3})^2} \\
={}& \frac{(\frac{\sqrt{3}}{2})(-1)-(4)(-1/2)}{(\frac{\sqrt{3}}{2})^2}\\
={}& \frac{-\frac{\sqrt{3}}{2}-2}{\frac{3}{4}} \\
={}& \frac{-2\sqrt{3}-8}{3}
\end{align}$$

</div> 
 </div>


</div> </li>
<li> <div class="exercise">  Find the equation of the line tangent to the graph of $$\begin{equation}f(x) = \frac{x+7}{x^2 - 2}\end{equation}$$ at \(x = 3\).

<div class="answerBox"> 
 <button onclick="myFunction('answer32')" class="answerButton">Show Answer</button> 
 <div  id='answer32' class="answer" >
First, take the derivative of \(f(x)\) using the quotient rule to find the slope at \(f'(3)\)\\
$$\begin{align}
f'(x) = \frac{\d}{\d x}(\frac{x+7}{x^2-2}) ={}& \frac{(1)(x^2-2)-(2x)(x+7)}{(x^2-2)^2}\\
={}& \frac{x^2-2-2x^2-14x}{(x^2-2)^2}\\
={}& \frac{-x^2-14x-2}{(x^2-2)^2}\\
&\Rightarrow& \frac{-(3)^2-14(3)-2}{((3)^2-2)^2} \quad \text{for} \quad f'(3)\\
={}& \frac{-9-42-2}{(9-2)^2}\\
={}& -\frac{53}{49}\\
\end{align}$$
Next, find find \(f(3)\) to get the coordinates of a point on the tangent line.
$$\begin{align}
f(3) ={}& \frac{(3)+7}{(3)^2-2}\\
={}& \frac{10}{7}\\
(x,y) ={}& \left(3,\frac{10}{7}\right)\\
\end{align}$$
Now we need to find the \(y\)-intercept by tracing back 3 units of \(x\) to \(y=0\)\\
$$\begin{align}
y-int ={}& \frac{10}{7}+\left(-\frac{53}{49}\right)\cdot(-3)\\
={}& \frac{229}{49}\\
\end{align}$$
Putting it all together, the equation of the line is \(y=\frac{229}{49}-\frac{53}{49}x\).\\
</div> 
 </div>
	
</div> </li></ol>



