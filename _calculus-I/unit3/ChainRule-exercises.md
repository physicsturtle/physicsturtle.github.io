---
layout: exercises
title: Chain Rule  - Exercises
dept: math
course: calculus-I
unit: unit3
deptDisplay: Math
courseDisplay: Calculus I
unitDisplay: Unit 3
---
<ol>
<li> <div class="exercise">  Evaluate the limit 
$$\begin{equation}
\lim_{x\to e}\frac{\log x - 1}{x - e}.
\end{equation}$$

<div class="answerBox"> 
 <button onclick="myFunction('answer6')" class="answerButton">Show Answer</button> 
 <div  id='answer6' class="answer" >
First, we notice that the limit is similar to the definition of the derivative of the form 

$$\begin{equation}
\lim_{x\to a}\frac{f(x)-f(a)}{x-a}
\end{equation}$$ 

where \(f(x)=\log(x)\) and \(a=e\).\\
Then, write out the limit in the form of a derivative.\\
$$\begin{align}
\lim_{x\to e}\frac{\log x - 1}{x - e} ={}& \frac{\d}{\d x}(\log(x))\bigg|_{x=e}\\
={}& \frac{1}{x} \bigg|_{x=e} \\
={}& \frac{1}{e}\\
\end{align}$$
</div> 
 </div>

</div> </li>
<li> <div class="exercise">  Find the equation of the line tangent to \(f(x) = e^{x + \log (\sin x)}\) at the point \( x = \pi/2\). 

<div class="answerBox"> 
 <button onclick="myFunction('answer24')" class="answerButton">Show Answer</button> 
 <div  id='answer24' class="answer" >
Equation of a tangent line: \(y-y_1=m(x-x_1)\)
First we find \(f(\pi/2)\):

$$\begin{align}
f\left(\frac{\pi}{2}\right)={}&e^{\frac{\pi}{2}+\log(\sin \frac{\pi}{2})}\\
={}& e^\frac{\pi}{2}\cdot e^{\log(\sin \frac{\pi}{2})}\\
={}& e^\frac{\pi}{2}\cdot\sin\frac{\pi}{2}\\
={}& e^\frac{\pi}{2}
\end{align}$$

The point through which the tangent line passes is therefore \((\frac{\pi}{2},e^\frac{\pi}{2})\). So the equation of the tangent so far is \(y-e^\frac{\pi}{2}=m(x-\frac{\pi}{2})\). Now we must find \(m=f'(\frac{\pi}{2})\).
We can rewrite the function \(f\) as
$$\begin{equation}
f(x) = e^{x+{\log}(\sin x)}=e^x\cdot e^{\log(\sin x)} = e^x \sin x
\end{equation}$$
Now it is easy to differentiate \(f\) by using the product rule.

$$\begin{align}
f'(x) ={}& (e^x\cdot\sin x)'\\
={}& e^x\cdot\sin (x) + e^x\cdot\cos(x)\\
={}& e^x(\sin x +\cos x)
\end{align}$$

Now evaluating at \(x = \pi/2\):

$$\begin{equation}
f'\left(\frac{\pi}{2}\right)=e^\frac{\pi}{2}(1+0)=e^\frac{\pi}{2}=m
\end{equation}$$

Thus the equation of the tangent line is 

$$\begin{equation}
y-e^\frac{\pi}{2}=e^\frac{\pi}{2}\left(x-\frac{\pi}{2}\right) 
\end{equation}$$

Finally rearranging \(y\) on one side:

$$\begin{equation}
y=e^\frac{\pi}{2}\left(x-\frac{\pi}{2}\right)+e^\frac{\pi}{2}
\end{equation}$$
</div> 
 </div>


</div> </li>
<li> <div class="exercise">  Differentiate the following function:
$$\begin{equation}
y = \left( \frac{x}{1+x} \right) ^5
\end{equation}$$\\
\\
<div class="answerBox"> 
 <button onclick="myFunction('answer73')" class="answerButton">Show Answer</button> 
 <div  id='answer73' class="answer" >
We have to use the chain rule, but the inner function requires the quotient rule. We first differentiate the inner function with the quotient rule:
$$\begin{align}
\left[\frac{x}{1+x}\right]' ={}& \frac{(1)(1+x)-(x)(1)}{(1+x)^2} \\
={}& \frac{1+x-x}{(1+x)^2} \\
={}& \frac{1}{(1+x)^2}
\end{align}$$

Now we apply the chain rule on the entire function \(y\):
$$\begin{align}
\left[ \left( \frac{x}{1+x} \right)^5\right]' ={}& 5\left(\frac{x}{1+x}\right)^4 \cdot \frac{1}{(1+x)^2} \\
={}& \frac{5x^4}{(1+x)^4}\cdot \frac{1}{(1+x)^2}\\
={}& \frac{5x^4}{(1+x)^6}
\end{align}$$



</div> 
 </div>


</div> </li>
<li> <div class="exercise">  Differentiate the following function:  $$\begin{equation}y = (x-1)\sqrt{x^2-2x+2}\end{equation}$$

<div class="answerBox"> 
 <button onclick="myFunction('answer95')" class="answerButton">Show Answer</button> 
 <div  id='answer95' class="answer" >
First, use chain rule to find \([\sqrt{x^2-2x+2}]'\) then use product rule to find the derivative of the entire thing.
$$\begin{align}
[\sqrt{x^2-2x+2}]' ={}& \frac{1}{2\sqrt{x^2-2x+2}}\cdot (2x-2) \\
={}& \frac{2(x-1)}{2\sqrt{x^2-2x+2}} \\
={}& \frac{x-1}{\sqrt{x^2-2x+2}}
\end{align}$$

Now product rule:
$$\begin{align}
(1)(\sqrt{x^2-2x+2})+(x-1)\left(\frac{x-1}{\sqrt{x^2-2x+2}}\right) ={}& \frac{x^2-2x+2}{\sqrt{x^2-2x+2}}+\frac{x^2-2x+1}{\sqrt{x^2-2x+2}} \\
={}& \frac{2x^2-4x+3}{\sqrt{x^2-2x+2}}
\end{align}$$

</div> 
 </div>

</div> </li>
<li> <div class="exercise">  Compute a linear approximation to \(z = z(w)\) at the point \(w =0\) if 
$$\begin{equation}
z = \frac{w}{\sqrt{1-w^2}}
\end{equation}$$

<div class="answerBox"> 
 <button onclick="myFunction('answer116')" class="answerButton">Show Answer</button> 
 <div  id='answer116' class="answer" >
First compute the derivative: 
$$\begin{equation}
\frac{dz}{dw} = \frac{1}{(1-w^2)^{3/2}}
\end{equation}$$
Evaluating 
$$\begin{equation}
z'(0) = 1
\end{equation}$$
Now the linear approximation is 
$$\begin{align}
L(w) ={}& z(0) + z'(0)w\\
={}& 0 + w\\
={}& w
\end{align}$$
</div> 
 </div>

</div> </li>
<li> <div class="exercise">  Differentiate the following function:  $$\begin{equation}y = \left( \frac{x^3 - 1}{2x^3 + 1} \right) ^4\end{equation}$$
<div class="answerBox"> 
 <button onclick="myFunction('answer134')" class="answerButton">Show Answer</button> 
 <div  id='answer134' class="answer" >
Use chain rule on the whole thing, but to do so, the derivative of the inner function must be found with the quotient rule. Starting with the quotient rule:
$$\begin{align}
\left[\frac{x^3-1}{2x^3+1}\right]' ={}& \frac{(3x^2)(2x^3+1)-(x^3-1)(6x^2)}{(2x^3+1)^2} \\
={}& \frac{9x^2}{(2x^3+1)^2}
\end{align}$$

Chain rule on the whole thing:
$$\begin{align}
\left[\left( \frac{x^3 - 1}{2x^3 + 1} \right) ^4\right]'  ={}& 4\left(\frac{x^3-1}{2x^3+1}\right)^3\cdot \frac{9x^2}{(2x^3+1)^2}\\
={}& \frac{36x^2(x^3-1)^3}{(2x^3+1)^5}
\end{align}$$
</div> 
 </div>

</div> </li>
<li> <div class="exercise">  Differentiate the following function:   \(y = (x^2+3)^4(2x^3 - 5)^3\)

<div class="answerBox"> 
 <button onclick="myFunction('answer150')" class="answerButton">Show Answer</button> 
 <div  id='answer150' class="answer" >
Use chain rule to find \([(x^2+3)^4]'\) and \([(2x^3-5)^3]'\), then use product rule to put it all together.
First the derivative of the first factor
$$\begin{equation} [(x^2+3)^4]' = 4(x^2+3)^3 \cdot 2x = 8x(x^2+3)^3 \end{equation}$$
Then find the derivative of the second factor
$$\begin{equation} [(2x^3-5)^3]' = 3(2x^3-5)^2 \cdot 6x^2 = 18x^2(2x^3-5)^2 \end{equation}$$
Now applying the product rule to the whole thing:
$$\begin{equation} y'=18x^2(2x^3-5)^2(x^2+3)^4+8x(x^2+3)^3(2x^3-5)^3\end{equation}$$

</div> 
 </div>


</div> </li>
<li> <div class="exercise">  Differentiate the following function. $$\begin{equation}y = \frac{\sqrt{x+\sqrt{x+\sqrt{x}}}}{\log x}\end{equation}$$
<div class="answerBox"> 
 <button onclick="myFunction('answer163')" class="answerButton">Show Answer</button> 
 <div  id='answer163' class="answer" >
$$\begin{equation}
y' = \frac{\frac{1}{2\sqrt{x+\sqrt{x+\sqrt{x}}}}\cdot\left(1+\frac{1}{2\sqrt{x+\sqrt{x}}}\cdot \left(1+\frac{1}{2\sqrt{x}}\right)\right)\log x - \frac{1}{x}\sqrt{x+\sqrt{x+\sqrt{x}}}}{(\log x)^2}
\end{equation}$$
</div> 
 </div>



</div> </li>
<li> <div class="exercise">  Differentiate the following function. $$\begin{equation}
f(\theta) = \frac{\tan 2 \theta}{1 - \cot 2\theta}
\end{equation}$$

<div class="answerBox"> 
 <button onclick="myFunction('answer175')" class="answerButton">Show Answer</button> 
 <div  id='answer175' class="answer" >
$$\begin{equation}
f'(\theta) = \frac{2\sec^2(2\theta)(1-\cot(2\theta)) - \tan(2\theta)2(\csc^2(2\theta))}{(1-\cot(2\theta))^2}
\end{equation}$$
</div> 
 </div>

</div> </li></ol>


