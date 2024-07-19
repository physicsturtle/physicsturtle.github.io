---
layout: exercises
title: Method of Partial Fractions  - Exercises
dept: math
course: calculus-II
unit: unit2
deptDisplay: Math
courseDisplay: Calculus II
unitDisplay: Unit 2
---
<ol>
<li> <div class="exercise"> [\(*\)] Evaluate the integral. 
$$\begin{equation}
\int \frac{\d x}{x^2+7x+6}
\end{equation}$$

<div class="answerBox"> 
 <button onclick="myFunction('answer6')" class="answerButton">Show Answer</button> 
 <div  id='answer6' class="answer" >
$$\begin{align}
\int \frac{\d x}{x^2 + 7x + 6} ={}& \int \frac{\d x}{(x + 6)(x + 1)}\\
={}& \frac{1}{5}\int \frac{1}{x + 1} - \frac{1}{x + 6}\d x \\
={}& \frac{1}{5}\log \left| \frac{x + 1}{x + 6} \right| + C
\end{align}$$
</div> 
 </div>



</div> </li>
<li> <div class="exercise"> [\(**\)] Evaluate the integral. $$\begin{equation}\int \frac{x+1}{x^3 + x^2 - 6x} \d x\end{equation}$$

<div class="answerBox"> 
 <button onclick="myFunction('answer18')" class="answerButton">Show Answer</button> 
 <div  id='answer18' class="answer" >
$$\begin{align}
\int \frac{x + 1}{x^3 + x^2 - 6x}\d x  ={}& \int \frac{x + 1}{x(x + 3)(x - 2)}\d x  \\
={}& \int  - \frac{1}{6x} + \frac{3}{10(x - 2)} - \frac{2}{15(x + 3)}\d x \\
={}& - \frac{1}{6}\log \left| x \right| + \frac{3}{10}\log \left| {x - 2} \right| - \frac{2}{15}\log \left| {x + 3} \right| + C
\end{align}$$
</div> 
 </div>


</div> </li>
<li> <div class="exercise"> [\(**\)] Evaluate the integral 
$$\begin{equation}
\int\frac{e^x}{(e^x - 2)(e^{2x} + 1)} \d x
\end{equation}$$

<div class="answerBox"> 
 <button onclick="myFunction('answer32')" class="answerButton">Show Answer</button> 
 <div  id='answer32' class="answer" >
Let \(e^x = u\). Then \(\d u = e^x \d x\). The integral is then transformed to
$$\begin{equation}
\int\frac{e^x}{(e^x - 2)(e^{2x} + 1)} \d x = \int \frac{\d u}{(u-2)(u^2 +1)}
\end{equation}$$
We apply a partial fraction decomposition to this. Just looking at the integrand, 
$$\begin{equation}\frac{1}{(u-2)(u^2+1)} = \frac{1}{5(x-2)}- \frac{x}{5(x^2+1)}-\frac{2}{5(x^2+1)}\end{equation}$$
Now integrating term by term, we have
$$\begin{equation}\int \frac{\d u}{(u-2)(u^2 +1)} = \frac{1}{5}\log|u-2| - \frac{1}{10}\log(u^2+1) - \frac{2}{5}\arctan u + C\end{equation}$$ 
Now transforming back to the original variable \(x\), 
$$\begin{equation}
\int\frac{e^x}{(e^x - 2)(e^{2x} + 1)} \d x = \frac{1}{5}\log|e^x - 2| - \frac{1}{10}\log(e^{2x} + 1) - \frac{2}{5}\arctan e^x + C
\end{equation}$$
</div> 
 </div>


</div> </li>
<li> <div class="exercise"> [\(**\)] Evaluate the integral. The attached table may be useful.
$$\begin{equation}
\int^{\pi/2}_0 \frac{\cos\theta}{\sqrt{1+\sin^2\theta}} \d\theta
\end{equation}$$

<div class="answerBox"> 
 <button onclick="myFunction('answer53')" class="answerButton">Show Answer</button> 
 <div  id='answer53' class="answer" >
Let \(\sin\theta = u\), and \(\d u = \cos\theta \d\theta\). Then we have the integral
$$\begin{equation}\int^{\pi/2}_0 \frac{\cos\theta}{\sqrt{1+\sin^2\theta}} \d\theta = \int_0^1 \frac{\d u}{\sqrt{1+u^2}}\end{equation}$$
Let \(u = \tan\varphi\), \(\d u = \sec^2\varphi d\varphi\). Then the integral is now
$$\begin{equation}\int_0^1 \frac{\d u}{\sqrt{1+u^2}} = \int_0^{\pi/4} \sec \varphi d\varphi\end{equation}$$
By problem \ref{secant}, we have
$$\begin{equation}\int_0^{\pi/4} \sec \varphi d\varphi = \left.\left(\log|\sec\varphi + \tan\varphi|\right)\right|^{\pi/4}_0\end{equation}$$
This evaluates to $$\begin{equation}\int^{\pi/2}_0 \frac{\cos\theta}{\sqrt{1+\sin^2\theta}} \d\theta = \log(1+\sqrt{2})\end{equation}$$
</div> 
 </div>


</div> </li>
<li> <div class="exercise"> [\(**\)] Evaluate the integral
$$\begin{equation}\int_0^1\frac{1}{1+\sqrt[3]{x}}\d x\end{equation}$$

<div class="answerBox"> 
 <button onclick="myFunction('answer67')" class="answerButton">Show Answer</button> 
 <div  id='answer67' class="answer" >
Let \(x = u^3\). Then \(\d x = 3u^2 \d u\), and the integral becomes
$$\begin{equation}\int_0^1\frac{1}{1+\sqrt[3]{x}}\d x = \int_0^1 \frac{3u^2}{1+u} \d u\end{equation}$$
Just looking at the integrand, it can be expanded by partial fractions to obtain
$$\begin{equation}\frac{3u^2}{1+u} = 3\left(u-1+\frac{1}{u+1}\right)\end{equation}$$
Now plugging this back into the integral, 
$$\begin{equation}\int_0^1\frac{1}{1+\sqrt[3]{x}}\d x =3 \int_0^1 \left(u-1+\frac{1}{u+1}\right)\d u\end{equation}$$
This is easily evaluated as 
$$\begin{equation}\int_0^1\frac{1}{1+\sqrt[3]{x}}\d x = 3\left.\left(\frac{u^2}{2} - u + \log|u+1|\right)\right|^1_0\end{equation}$$
Finally we have
$$\begin{equation}\int_0^1\frac{1}{1+\sqrt[3]{x}}\d x = 3\log 2 - \frac{3}{2}\end{equation}$$
</div> 
 </div>



</div> </li>
<li> <div class="exercise"> [\(***\)] Evaluate the integral
$$\begin{equation}
\int \sec x \d x
\end{equation}$$

<div class="answerBox"> 
 <button onclick="myFunction('answer87')" class="answerButton">Show Answer</button> 
 <div  id='answer87' class="answer" >
We first manipulate the integrand to make it possible to use partial fractions.
$$\begin{align}
\int \sec \theta \d\theta ={}& \int \frac{1}{\cos \theta}\d\theta \\
={}& \int \frac{\cos \theta }{\cos^2\theta}\d\theta \\
={}& \int \frac{\cos \theta}{1-\sin^2\theta }\d\theta 
\end{align}$$
Let \(\sin \theta  = u\), and \(\d u = \cos \theta \d\theta\). This transforms the integral in to
$$\begin{align}
\int \frac{\cos \theta}{1-\sin^2\theta }\d\theta  ={}&\int \frac{\d u}{1 - u^2} \\
={}& \frac{1}{2}\int \frac{1}{1 + u} + \frac{1}{1 - u} \d u \\
={}& \frac{1}{2}\log \left| \frac{1 + u}{1 - u} \right| = \frac{1}{2}\log \left| \frac{1 + \sin \theta }{1 - \sin \theta } \right| \\ 
={}& \frac{1}{2}\log \left| \frac{1 + \sin \theta }{1 - \sin \theta }\left( \frac{1 + \sin \theta }{1 + \sin \theta } \right) \right| \\
={}& \frac{1}{2}\log \left| \frac{(1 + \sin \theta )^2}{\cos^2\theta } \right|\\
={}& \log \left| \frac{1+\sin \theta }{\cos \theta } \right|\\
={}& \log \left| {\sec \theta  + \tan \theta } \right| \\
\end{align}$$
 Thus
$$\begin{equation}\int {\sec \theta \d\theta }  = \log \left| {\sec \theta  + \tan \theta } \right| \end{equation}$$
</div> 
 </div>



</div> </li>
<li> <div class="exercise"> [\(**\)] Evaluate the integral. $$\begin{equation}\int \frac{x^4 - x^3 - x + 1}{x^3 - x^2} \d x\end{equation}$$

<div class="answerBox"> 
 <button onclick="myFunction('answer112')" class="answerButton">Show Answer</button> 
 <div  id='answer112' class="answer" >
$$\begin{align}
\int \frac{x^4 - x^3 - x + 1}{x^3 - x^2} \d x ={}& \int x - \frac{x - 1}{x^3 - x^2}\d x  \\
={}& \frac{1}{2}x^2 - \int \frac{x - 1}{x^2(x - 1)}\d x \\
={}& \frac{1}{2} x^2 - \int \frac{1}{x^2}\d x  \\
={}& \frac{1}{2}x^2 + \frac{1}{x} + C
\end{align}$$
</div> 
 </div>





</div> </li></ol>


