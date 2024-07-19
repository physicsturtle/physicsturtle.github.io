---
layout: exercises
title: Substitution Rule  - Exercises
dept: math
course: calculus-II
unit: unit2
deptDisplay: Math
courseDisplay: Calculus II
unitDisplay: Unit 2
---
<ol>
<li> <div class="exercise"> [\(*\)] Compute the integral
$$\begin{equation}\int 2\sin(3x) \d x\end{equation}$$

<div class="answerBox"> 
 <button onclick="myFunction('answer4')" class="answerButton">Show Answer</button> 
 <div  id='answer4' class="answer" >
We make the substitution \(u = 3x\), \(\d u = 3\d x\), which gives us 

$$\begin{equation}
\int 2\sin(3x) \d x = 2\int \sin(u) \frac{\d u}{3} 
\end{equation}$$

and we can simply evaluate this after moving the \(1/3\) to the front.

$$\begin{equation}
2\int \sin(u) \frac{\d u}{3} = \frac{2}{3}\int \sin u \d u = -\frac{2}{3}\cos u + C
\end{equation}$$

Now substituting back in \(u = 3x\), 

$$\begin{equation}
\int 2\sin(3x) \d x = -\frac{2}{3}\cos(3x) + C
\end{equation}$$

</div> 
 </div>

</div> </li>
<li> <div class="exercise"> [\(*\)] Evaluate the integral
$$\begin{equation}
\int \frac{x^2}{3}\cos(x^3) \d x
\end{equation}$$

<div class="answerBox"> 
 <button onclick="myFunction('answer30')" class="answerButton">Show Answer</button> 
 <div  id='answer30' class="answer" >
We recognize that we have the function \(x^3\), and something which is almost its derivative, \(x^2\). Thus we make the substitution \(u = x^3\), \(\d u = 3x^2\d x\). Doing this, we see that the \(x^2\) in the numerator will cancel with the \(x^2\) which is introduced in the denominator from the transformation of the differential. 

$$\begin{align}
\int \frac{x^2}{3}\cos(x^3) \d x={}& \frac{1}{3}\int x^2 \cos(u) \frac{\d u}{3x^2} \\
={}& \frac{1}{9}\int \cos u \d u \\
={}& \frac{1}{9}\sin u + C\\
={}& \frac{1}{9} \sin(x^3) + C
\end{align}$$

</div> 
 </div>

</div> </li>
<li> <div class="exercise"> [\(*\)] Evaluate the integral
$$\begin{equation}\int \cot\theta \d\theta\end{equation}$$

<div class="answerBox"> 
 <button onclick="myFunction('answer45')" class="answerButton">Show Answer</button> 
 <div  id='answer45' class="answer" >
We rewrite the integral as 
$$\begin{equation}
\int \cot\theta \d\theta = \int \frac{\cos\theta}{\sin\theta} \d\theta
\end{equation}$$

Making the substitution \(u = \sin\theta\), and \(\d u = \cos\theta \d\theta\), we have that 

$$\begin{equation}
\int \frac{\cos\theta}{\sin\theta} \d\theta = \int \frac{1}{u}{\d u}
\end{equation}$$

This can be easily integrated to get 

$$\begin{equation}
\int \frac{1}{u}{\d u} = \log |u|.
\end{equation}$$

Substituting back in, we find
$$\begin{equation}
\int \cot\theta \d\theta = \log|\sin\theta| + C.
\end{equation}$$
</div> 
 </div>

</div> </li>
<li> <div class="exercise"> [\(*\)] Compute the value of the integral. 
$$\begin{equation}\int^8_4 \frac{x}{\sqrt{x^2-15}}\d x\end{equation}$$

<div class="answerBox"> 
 <button onclick="myFunction('answer72')" class="answerButton">Show Answer</button> 
 <div  id='answer72' class="answer" >
For the integral
$$\begin{equation}\int_4^8 \frac{x}{\sqrt{x^2 - 15}}\d x\end{equation}$$
We first need to find the antiderivative 
$$\begin{equation}\int \frac{x}{\sqrt {x^2 - 15}}\d x\end{equation}$$
Make the substitution \(u = x^2 - 15\), and  \(\d u = 2x\d x\) to obtain
$$\begin{align}
\int \frac{x}{\sqrt {x^2 - 15}}\d x ={}& \frac{1}{2}\int u^{-1/2}\d u  \\
={}& \sqrt u  \\
={}& \sqrt {x^2 - 15} \\
\end{align}$$
Now evaluating the antiderivative at both end points:
$$\begin{align}
\int_4^8 \frac{x}{\sqrt {x^2 - 15}}\d x  ={}& \left. \left( \sqrt {x^2 - 15} \right) \right|_4^8 \\
={}& 7 - 1 \\
={}& 6\\
\end{align}$$
The final answer becomes
$$\begin{equation}\int_4^8 \frac{x}{\sqrt {x^2 - 15}}\d x = 6\end{equation}$$
</div> 
 </div>


</div> </li>
<li> <div class="exercise">  Evaluate the integral
$$\begin{equation}\int \frac{\cos\left(\log x\right)}{x} \d x\end{equation}$$

<div class="answerBox"> 
 <button onclick="myFunction('answer97')" class="answerButton">Show Answer</button> 
 <div  id='answer97' class="answer" >
Make the substitution \(u = \log x\) so that we get 
$$\begin{equation}\int \frac{\cos\left(\log x\right)}{x} \d x = \int \cos u du = \sin u + C\end{equation}$$
Substituting back in our original expression, we find that 
$$\begin{equation}\int \frac{\cos\left(\log x\right)}{x} \d x = \sin \log x + C\end{equation}$$
</div> 
 </div>


</div> </li>
<li> <div class="exercise">  Evaluate the integral. $$\begin{equation}\int 2e^x \sin (e^x) \d x\end{equation}$$

<div class="answerBox"> 
 <button onclick="myFunction('answer107')" class="answerButton">Show Answer</button> 
 <div  id='answer107' class="answer" >
Make the substitution \(u = e^x\) to find
$$\begin{equation}\int 2\sin u du = -2\cos u +C\end{equation}$$
Substituting back in terms of \(x\), we find 
$$\begin{equation}\int 2e^x \sin (e^x) \d x = -2\cos(e^x)\end{equation}$$
</div> 
 </div>


</div> </li>
<li> <div class="exercise"> [\(**\)] Evaluate the integral. 
$$\begin{equation}\int\frac{e^{2x}}{1+e^{4x}}\d x\end{equation}$$

<div class="answerBox"> 
 <button onclick="myFunction('answer118')" class="answerButton">Show Answer</button> 
 <div  id='answer118' class="answer" >
For the integral
$$\begin{equation}\int \frac{e^{2x}}{1 + e^{4x}}\d x \end{equation}$$
We make the substitution \(u = e^{2x}\), and \(\d u = 2e^{2x}\d x\). The integral then becomes
$$\begin{align}
\int \frac{e^{2x}}{1 + e^{4x}}\d x  ={}& \frac{1}{2}\int \frac{1}{1 + u^2} \d u \\
={}& \frac{1}{2}\arctan u + C \\
={}& \frac{1}{2}\arctan (e^{2x}) + C
\end{align}$$
The final answer is then
$$\begin{equation} \int \frac{e^{2x}}{1 + e^{4x}}\d x  = \frac{1}{2}\arctan (e^{2x}) + C\end{equation}$$
</div> 
 </div>



</div> </li>
<li> <div class="exercise"> [\(**\)] Evaluate the integral. 
$$\begin{equation}\int \frac{2x-7}{x^2+1} \d x\end{equation}$$

<div class="answerBox"> 
 <button onclick="myFunction('answer136')" class="answerButton">Show Answer</button> 
 <div  id='answer136' class="answer" >
We split the integral up into the sum of two fractions, both of which are easy to evaluate:
$$\begin{align}
\int \frac{2x - 7}{x^2 + 1}\d x ={}& \int \frac{2x}{x^2 + 1} - \frac{7}{x^2 + 1}\d x \\
={}& \log (x^2 + 1) - 7\arctan x + C
\end{align}$$
The final answer is then
$$\begin{equation}\int \frac{2x - 7}{x^2 + 1}\d x = \log (x^2 + 1) - 7\arctan x + C \end{equation}$$
</div> 
 </div>


</div> </li>
<li> <div class="exercise"> [\(**\)] Compute the value of the integral. 
$$\begin{equation}\int^9_4 \frac{1-\sqrt{x}}{1+\sqrt{x}}  \d x\end{equation}$$

<div class="answerBox"> 
 <button onclick="myFunction('answer150')" class="answerButton">Show Answer</button> 
 <div  id='answer150' class="answer" >
$$\begin{equation}
\int_4^9 \frac{1 - \sqrt{x}}{1 + \sqrt{x}}\d x 
\end{equation}$$
We first find an antiderivative.
$$\begin{align}
\int \frac{1 - \sqrt{x}}{1 + \sqrt{x}}\d x ={}& \int \frac{1 + \sqrt{x} - 2\sqrt{x}}{1 + \sqrt{x}}\d x \\
={}& \int 1 - \frac{2\sqrt{x}}{1 + \sqrt {x}} \d x \\
={}& x - 2\int \frac{\sqrt {x}}{1 + \sqrt {x}} \d x 
\end{align}$$
Consider the remaining integral
$$\begin{equation}\int \frac{\sqrt{x}}{1 + \sqrt{x} }\d x. \end{equation}$$
Make the substitution \(u = 1 + \sqrt{x}\), which gives \( \d u = \frac{{\d x}}{2\sqrt{x}}\), or, rearranging, \(\d x = 2(u - 1)\d u\). We then have the integral
$$\begin{align}
\int \frac{\sqrt{x}}{1 + \sqrt{x}}\d x ={}& \int \frac{2(u - 1)^2}{u}\d u \\
={}& 2 \int \frac{u^2 - 2u + 1}{u} \d u \\
={}& 2\int u - 2 + \frac{1}{u}\d u \\
={}& 2\left( \frac{u^2}{2} - 2u + \log u \right)  \\
={}& (1 + \sqrt{x} )^2 - 4(1 + \sqrt{x} ) + 2\log (1 + \sqrt{x} )
\end{align}$$
Then, plugging this result into equation \eqref{int3.1}:
$$\begin{align}
\int \frac{1 - \sqrt{x}}{1 + \sqrt{x}}\d x  ={}& x - 2\left[ (1 + \sqrt{x})^2- 4(1 + \sqrt{x}) + 2\log (1 + \sqrt{x} )\right] \\
={}& - x + 6 + 4\sqrt{x}  - 4\log (1 + \sqrt{x})
\end{align}$$
Now that we have the antiderivative, we can evaluate it at the two endpoints:
$$\begin{align}
 \int_4^9 \frac{1 - \sqrt{x}}{1 + \sqrt{x}}\d x  ={}& \left. \left(- x + 6 + 4\sqrt{x}  - 4\log (1 + \sqrt{x}) \right) \right|_4^9 \\
 ={}& 4\log (3/4) - 1
 \end{align}$$
</div> 
 </div>


</div> </li>
<li> <div class="exercise"> [\(**\)] Evaluate the integral. 
$$\begin{equation}\int\frac{e^x - 1}{e^x + 1} \d x\end{equation}$$

<div class="answerBox"> 
 <button onclick="myFunction('answer186')" class="answerButton">Show Answer</button> 
 <div  id='answer186' class="answer" >
$$\begin{align}
\int \frac{e^x - 1}{e^x + 1}\d x ={}&  - \int \frac{1 - e^x}{e^x + 1}\d x \\
={}&  - \int \frac{1 + e^x}{e^x + 1} - \frac{2e^x}{e^x + 1}\d x \\
={}&  - \int 1 -\frac{2e^x}{e^x + 1} \d x\\
={}&  - x + 2\int \frac{e^x}{e^x + 1} \d x \\
={}&  - x + 2\log (e^x + 1) + C \\
={}& 2\log (e^x + 1) - x + C
\end{align}$$
Thus
$$\begin{equation}
\int \frac{e^x - 1}{e^x + 1} \d x = 2\log (e^x + 1) - x + C
\end{equation}$$
</div> 
 </div>

</div> </li>
<li> <div class="exercise">  Evaluate the integral. 
$$\begin{equation}\int\frac{1}{1-\sin(x/2)}\d x\end{equation}$$

<div class="answerBox"> 
 <button onclick="myFunction('answer204')" class="answerButton">Show Answer</button> 
 <div  id='answer204' class="answer" >
We will need to multiply by the conjugate to solve this problem:
$$\begin{align}
\int \frac{1}{1-\sin (x/2)}\d x ={}& \int \frac{1 + \sin (x/2)}{1 - \sin^2(x/2)}\d x \\
={}& \int \frac{1 + \sin (x/2)}{\cos^2(x/2)}\d x \\
={}& \int \sec^2\left(\frac{x}{2}\right) + \tan\left(\frac{x}{2}\right)\sec\left(\frac{x}{2}\right)\d x \\
={}& 2\left(\tan\left(\frac{x}{2}\right)  + \sec\left(\frac{x}{2}\right)\right) + C
\end{align}$$
The final answer is then
$$\begin{equation}\int \frac{1}{1 - \sin (x/2)}\d x = 2\left(\tan\left(\frac{x}{2}\right) + \sec\left(\frac{x}{2}\right)\right) + C\end{equation}$$
</div> 
 </div>

</div> </li>
<li> <div class="exercise"> [\(***\)] Evaluate the integral. 
$$\begin{equation}\int\frac{\cos 2x}{\sin^2(2x) + 8}\d x\end{equation}$$

<div class="answerBox"> 
 <button onclick="myFunction('answer219')" class="answerButton">Show Answer</button> 
 <div  id='answer219' class="answer" >
For the integral
$$\begin{equation} \int \frac{\cos 2x}{\sin^2(2x) + 8} \d x \end{equation}$$
We make the substitution \(u = \sin 2x\), so the differential is \(\d u = 2\cos2x\,\d x\). 
$$\begin{align}
\int \frac{\cos 2x}{\sin^2 2x + 8} \d x ={}& \frac{1}{2}\int \frac{1}{u^2+ 8}\d u  \\
={}& \frac{1}{16}\int \frac{1}{\left( \frac{u}{2\sqrt{2}} \right)^2 + 1} \d u 
\end{align}$$
Now with this integral, make the substitution \(w = \frac{u}{2\sqrt{2}}\), and \(\d u = 2\sqrt 2 \d w\), to easily evaluate the integral:
$$\begin{align}
\frac{1}{16}\int \frac{1}{\left( \frac{u}{2\sqrt{2} }\right)^2 + 1} \d u ={}& \frac{\sqrt{2}}{8}\int \frac{1}{1 + w^2}\d w \\
={}& \frac{\sqrt{2}}{8}\arctan w + C \\
={}& \frac{\sqrt{2}}{8}\arctan \left(\frac{\sin 2x}{2\sqrt{2}} \right) + C
\end{align}$$
</div> 
 </div>


</div> </li>
<li> <div class="exercise"> [\(***\)] Compute the value of the integral. 
$$\begin{equation}\int^{\pi}_0 \frac{\sin x}{\cos^2x - 6\cos x + 13}\d x\end{equation}$$

<div class="answerBox"> 
 <button onclick="myFunction('answer239')" class="answerButton">Show Answer</button> 
 <div  id='answer239' class="answer" >
$$\begin{equation}\int_0^\pi \frac{\sin x}{\cos^2x - 6\cos x + 13} \d x\end{equation}$$
First we find an antiderivative by making a \(u\) substitution. For the integral
$$\begin{equation} \int \frac{\sin x}{\cos^2x - 6\cos x + 13}\d x \end{equation}$$
Make the substitution \(u = \cos x\), and \(\d u =  - \sin x\d x\). This yields the integral
$$\begin{align}
\int \frac{\sin x}{\cos^2x - 6\cos x + 13}\d x ={}&  - \int \frac{1}{u^2 - 6u + 13}\d u\\
={}&  - \int \frac{1}{(u - 3)^2 + 4}\d u \\
={}&  - \frac{1}{4}\int \frac{1}{\left( \frac{u - 3}{2} \right)^2 + 1}\d u 
\end{align}$$
Now with this integral, we make the substitution \(\frac{u - 3}{2}  = w\) and \(2\d w =  \d u\). The we have the integral
$$\begin{align}
- \frac{1}{4}\int \frac{1}{\left( \frac{u - 3}{2} \right)^2 + 1} \d u={}&  - \frac{1}{2}\int \frac{1}{1 + w^2}\d w \\
={}&  - \frac{1}{2}\arctan w 
\end{align}$$
Now substitution in the original variables:
$$\begin{equation}- \frac{1}{2}\arctan \left( \frac{\cos x - 3}{2} \right) \end{equation}$$
Now we evaluate at the endpoints:
$$\begin{equation}\left. \left(- \frac{1}{2}\arctan \left(\frac{\cos x - 3}{2} \right) \right) \right|_0^\pi  \end{equation}$$
This yields the final answer:
$$\begin{equation}\frac{1}{2}\left(\arctan 2 - \frac{\pi}{4} \right)\end{equation}$$
</div> 
 </div>


</div> </li>
<li> <div class="exercise"> [\(**\)] Evaluate the integral. $$\begin{equation}\int \frac{1}{x+x^{1/3}} \d x\end{equation}$$

<div class="answerBox"> 
 <button onclick="myFunction('answer265')" class="answerButton">Show Answer</button> 
 <div  id='answer265' class="answer" >
Let \(x = z^3\), and \(\d x = 3z^2\d z\). Making these substitutions yields
$$\begin{align}
\int \frac{1}{z^3 + z}3z^2\d z ={}& 3\int \frac{z}{z^2 + 1}\d z \\
={}& \frac{3}{2}\log (z^2 + 1)  + C  \\
={}& \frac{3}{2}\log (x^{2/3} + 1) + C\\
\end{align}$$
Thus the final answer is
$$\begin{equation} \int \frac{1}{x + x^{1/3}}\d x  = \frac{3}{2}\log (x^{2/3} + 1) + C\end{equation}$$
</div> 
 </div>




</div> </li>
<li> <div class="exercise"> [\(**\)] Evaluate the integral. $$\begin{equation}\int x^3 \sqrt{a^2-x^2} \d x\end{equation}$$

<div class="answerBox"> 
 <button onclick="myFunction('answer281')" class="answerButton">Show Answer</button> 
 <div  id='answer281' class="answer" >
Let \(u = a^2 - x^2\) and \(\d u =  - 2x\d x\).
$$\begin{align}
\int x^3\sqrt{a^2 - x^2} \d x  ={}&  - \frac{1}{2}\int x^2\sqrt{u} \d u \\
={}& \frac{1}{2}\int (u -a^2)\sqrt{u} \d u \\
 ={}& \frac{1}{2}\int u^{3/2} - a^2\sqrt{u} \d u  \\
 ={}& \frac{1}{2}\left( \frac{2}{5}u^{5/2} - \frac{2}{3}a^2u^{3/2} \right) + C\\
 ={}& \frac{1}{5}(a^2 - x^2)^{5/2} - \frac{a^2}{3}(a^2 - x^2)^{3/2} + C
\end{align}$$
</div> 
 </div>



</div> </li>
<li> <div class="exercise"> [\(***\)] Evaluate the integral. $$\begin{equation}\int \sqrt{1-\cos x} \d x\end{equation}$$

<div class="answerBox"> 
 <button onclick="myFunction('answer296')" class="answerButton">Show Answer</button> 
 <div  id='answer296' class="answer" >
Use the double angle identity
$$\begin{equation}
1 - \cos 2x = 2\sin ^2x \Rightarrow 1 - \cos x = 2\sin ^2\left( \frac{x}{2} \right)
\end{equation}$$
$$\begin{align}
\int \sqrt{1 - \cos x} \d x ={}& \int \sqrt{2\sin^2\left( \frac{x}{2} \right)} \d x\\ 
={}& \sqrt2 \int \sin \left( \frac{x}{2} \right) \d x \\
={}&  - 2\sqrt2 \cos \left( \frac{x}{2} \right) + C\\
\end{align}$$
$$\begin{equation}
\int \sqrt{1 - \cos x} \d x  =  - 2\sqrt2 \cos \left( \frac{x}{2} \right) + C
\end{equation}$$
</div> 
 </div>


</div> </li>
<li> <div class="exercise"> [\(*\)] Evaluate the integral
$$\begin{equation}\int\frac{\sqrt{1+\sqrt{x}}}{\sqrt{x}}\d x\end{equation}$$

<div class="answerBox"> 
 <button onclick="myFunction('answer315')" class="answerButton">Show Answer</button> 
 <div  id='answer315' class="answer" >
Let \(u = 1+ \sqrt{x}\), and \(2\d u = \frac{1}{\sqrt{x}} \d x\). Then the integral becomes
$$\begin{equation}\int\frac{\sqrt{1+\sqrt{x}}}{\sqrt{x}}\d x = 2\int\sqrt{u} \d u\end{equation}$$
This integral is easily evaluated
$$\begin{equation} 2\int\sqrt{u} \d u = \frac{4}{3}u^{3/2} + C \end{equation}$$
Now changing to the original variables, 
$$\begin{equation}\int\frac{\sqrt{1+\sqrt{x}}}{\sqrt{x}}\d x = \frac{4}{3}(1+\sqrt{x})^{3/2} + C\end{equation}$$
</div> 
 </div>



</div> </li>
<li> <div class="exercise"> [\(***\)] Evaluate the integral. $$\begin{equation}\int \frac{2x-3}{x^2+6x+13} \d x\end{equation}$$

<div class="answerBox"> 
 <button onclick="myFunction('answer328')" class="answerButton">Show Answer</button> 
 <div  id='answer328' class="answer" >
We will split this integral up so that part of it can be evaluated as a logarithm:
$$\begin{align}
\int \frac{2x - 3}{x^2 + 6x + 13}\d x  ={}& \int \frac{2x + 6 - 9}{x^2 + 6x + 13}\d x \\
={}& \int \frac{2x + 6}{x^2 + 6x + 13}\d x - \int \frac{9}{x^2 + 6x + 9 + 4}\d x \\
={}& \log \left| x^2 + 6x + 13 \right| - 9\int \frac{1}{(x + 3)^2 + 4}\d x \\
\end{align}$$
To evaluate the second integral, $$\begin{equation}9\int \frac{1}{(x + 3)^2+ 4}\d x\end{equation}$$
we need to make the substitution \(x + 3 = 2\tan z\), and \(\d x = 2\sec^2z\d z\). Thus
$$\begin{equation}9\int \frac{1}{(x + 3)^2+ 4}\d x =\frac{9}{2}\int 1\d z = \frac{9z}{2} = \frac{9}{2}\arctan \left( \frac{x + 3}{2}\right)\end{equation}$$
The final answer is then 
$$\begin{equation}\int \frac{2x-3}{x^2+6x+13} \d x = \log \left| {x^2 + 6x + 13} \right| - \frac{9}{2}\arctan \left( \frac{x + 3}{2} \right) + C\end{equation}$$
</div> 
 </div>



</div> </li>
<li> <div class="exercise"> [\(**\)] Evaluate the integral. $$\begin{equation}\int \csc(2x) \d x\end{equation}$$

<div class="answerBox"> 
 <button onclick="myFunction('answer346')" class="answerButton">Show Answer</button> 
 <div  id='answer346' class="answer" >
$$\begin{align}
\int \csc (2x)\d x  ={}& \int \frac{1}{\sin (2x)}\d x \\
 ={}& \int \frac{1}{2\sin (x)\cos (x)}\d x  \\
 ={}& \int \frac{\cos (x)}{2\sin (x)\cos^2(x)}\d x  \\
 ={}& \frac{1}{2} \int \frac{\sec^2(x)}{\tan (x)} \d x\\
={}&\frac{1}{2}\log \left| \tan x \right| + C\\
\end{align}$$
The final answer is then
$$\begin{equation}\int \csc (2x)\d x  = \frac{1}{2}\log \left| \tan x \right| + C\end{equation}$$
</div> 
 </div>



</div> </li>
<li> <div class="exercise"> [\(**\)] Evaluate the integral $$\begin{equation}\int \frac{2x+3}{9x^2-12x + 8} \d x\end{equation}$$

<div class="answerBox"> 
 <button onclick="myFunction('answer362')" class="answerButton">Show Answer</button> 
 <div  id='answer362' class="answer" >
$$\begin{align}
\int \frac{2x + 3}{9x^2 - 12x + 8}\d x  ={}& \frac{1}{9}\int \frac{18x + 27}{9x^2 - 12x + 8}  \d x\\
={}& \frac{1}{9}\int \left( \frac{18x - 12}{9x^2 - 12x + 8} + \frac{39}{(3x - 2)^2 + 4}\right)\d x \\
\end{align}$$
Let \( 3x - 2 = 2z\), and \(3\d x = 2\d z\). 
$$\begin{align}
\frac{1}{9}\int \left(\frac{18x - 12}{9x^2 - 12x + 8} + \frac{39}{(3x - 2)^2 + 4}\right)\d x  ={}& \frac{1}{9}\log \left| 9x^2 - 12x + 8 \right| + \frac{1}{18}\int \frac{13}{z^2 + 1}\d z \\
 ={}& \frac{1}{9}\log \left| 9x^2 - 12x + 8 \right| + \frac{13}{18}\arctan (z) + C\\
 ={}& \frac{1}{9}\log \left| 9x^2 - 12x + 8 \right| + \frac{13}{18}\arctan \left( \frac{3x - 2}{2} \right) + C
\end{align}$$
</div> 
 </div>





</div> </li></ol>


