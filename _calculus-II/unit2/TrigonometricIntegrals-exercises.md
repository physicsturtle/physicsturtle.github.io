---
layout: exercises
title: Trigonometric Integrals  - Exercises
dept: math
course: calculus-II
unit: unit2
deptDisplay: Math
courseDisplay: Calculus II
unitDisplay: Unit 2
---
<ol>


<li> <div class="exercise"> [\(*\)] If \(x = 6\cos \theta\), \(y = 2\sin \theta\), compute the value of the integral. 
$$\begin{equation}\int^6_3 xy \d x\end{equation}$$

<div class="answerBox"> 
 <button onclick="myFunction('answer6')" class="answerButton">Show Answer</button> 
 <div  id='answer6' class="answer" >
For the integral $$\begin{equation}\int_3^6 xy \d x\end{equation}$$
since \(x = 6\cos \theta\) and \(y = 2\sin \theta\), we can compute \(\d x =  - 6\sin \theta \d\theta\). Since the bounds are from \(x = 3\) to \(x = 6\), the equivalent \(\theta\) that accomplish this are \(\theta = \pi/3\) to \(\theta = 0\).
$$\begin{align}
\int_{\pi /3}^0 (6\cos \theta )(2\sin \theta )(-6\sin \theta )\d\theta ={}&  - 72\int_{\pi /3}^0 \sin^2\theta \cos \theta \d\theta \\
={}& 72\left. \frac{\sin^3\theta}{3} \right|_0^{\pi /3} \\
={}& 24\left(\frac{\sqrt{3}}{2}\right)^3 \\
={}& 9\sqrt{3}
\end{align}$$
$$\begin{equation}\int_3^6 xy\d x  = 9\sqrt{3}\end{equation}$$
</div> 
 </div>



</div> </li>
<li> <div class="exercise"> [\(**\)] Evaluate the integral. 
$$\begin{equation}\int\frac{1}{1-\sin(x/2)}\d x\end{equation}$$

<div class="answerBox"> 
 <button onclick="myFunction('answer23')" class="answerButton">Show Answer</button> 
 <div  id='answer23' class="answer" >
We will need to multiply by the conjugate to solve this problem:
$$\begin{align}
\int \frac{1}{1-\sin (x/2)}\d x ={}& \int \frac{1 + \sin (x/2)}{1 - \sin^2(x/2)}\d x \\
={}& \int \frac{1 + \sin (x/2)}{\cos^2(x/2)}\d x \\
={}& \int \sec^2\left(\frac{x}{2}\right) + \tan\left(\frac{x}{2}\right)\sec\left(\frac{x}{2}\right)\d x \\
={}& 2\left(\tan\left(\frac{x}{2}\right)  + \sec\left(\frac{x}{2}\right)\right) + C
\end{align}$$
The final answer is then
$$\begin{equation}
\int \frac{1}{1 - \sin (x/2)}\d x = 2\left(\tan\left(\frac{x}{2}\right) + \sec\left(\frac{x}{2}\right)\right) + C
\end{equation}$$
</div> 
 </div>



</div> </li>
<li> <div class="exercise"> [\(**\)] Evaluate the integral. 
$$\begin{equation}\int \sin^3x\cos^2x \d x\end{equation}$$

<div class="answerBox"> 
 <button onclick="myFunction('answer42')" class="answerButton">Show Answer</button> 
 <div  id='answer42' class="answer" >
Let \(\cos x = u\), \(\d u =  - \sin x\d x\)\\
$$\begin{align}
\int \sin^3x\cos^2x\d x ={}&  - \int (1 - u^2)u^2\d u \\
={}& \int u^4 - u^2\d u \\
={}& \frac{u^5}{5} - \frac{u^3}{3} + C \\
={}& \frac{\cos^5x}{5} - \frac{\cos^3x}{3} + C
\end{align}$$
$$\begin{equation}
\int \sin^3x\cos^2x\d x = \frac{\cos^5x}{5} - \frac{\cos^3x}{3} + C
\end{equation}$$
</div> 
 </div>


</div> </li>
<li> <div class="exercise"> [\(**\)] Evaluate the integral. 
$$\begin{equation}\int \tan^4 x \sec^4 x \d x\end{equation}$$

<div class="answerBox"> 
 <button onclick="myFunction('answer59')" class="answerButton">Show Answer</button> 
 <div  id='answer59' class="answer" >
Let \(u = \tan x\), \(\d u = \sec ^2x\d x\)
$$\begin{align}
\int u^4(u^2 + 1)\d u ={}& \int u^6 + u^4\d u \\
={}& \frac{u^7}{7} + \frac{u^5}{5} + C \\
={}& \frac{\tan^7x}{7} + \frac{\tan^5x}{5} + C
\end{align}$$
$$\begin{equation}
\int \tan^4x\sec^4x\d x  = \frac{\tan^7x}{7} + \frac{\tan^5x}{5} + C
\end{equation}$$
</div> 
 </div>



</div> </li>
<li> <div class="exercise"> [\(**\)] Evaluate the integral. 
$$\begin{equation}\int \sin^4 x \d x\end{equation}$$

<div class="answerBox"> 
 <button onclick="myFunction('answer76')" class="answerButton">Show Answer</button> 
 <div  id='answer76' class="answer" >
$$\begin{align}
\int \sin^4x\d x  ={}& \int \sin^2x(1 - \cos^2x )\d x\\
={}& \int \sin^2x - \sin^2x\cos^2x\d x\\
={}& \int \sin^2x \d x - \int \sin^2x\cos^2x\d x \\
={}& \int \frac{1 - \cos 2x}{2}\d x - \int \frac{\sin^2 2x}{4}\d x \\
={}& \frac{1}{2}x - \frac{\sin 2x}{4}  - \int \frac{1 - \cos 4x}{8}\d x  \\
={}& \frac{1}{2}x - \frac{\sin 2x}{4} - \frac{1}{8}x + \frac{\sin 4x}{32} + C\\
={}& \frac{3x}{8} - \frac{\sin 2x}{4} + \frac{\sin 4x}{32} + C
\end{align}$$
$$\begin{equation}
\int \sin^4x\d x  = \frac{3x}{8} - \frac{\sin 2x}{4} + \frac{\sin 4x}{32} + C
\end{equation}$$
</div> 
 </div>



</div> </li>
<li> <div class="exercise"> [\(**\)] Evaluate the integral. 
$$\begin{equation}\int x(\cos^3(x^2) - \sin^3(x^2)) \d x\end{equation}$$

<div class="answerBox"> 
 <button onclick="myFunction('answer96')" class="answerButton">Show Answer</button> 
 <div  id='answer96' class="answer" >
Let  \(x^2 = u\), \(\d u = 2x\d x\). Then
$$\begin{align}
\int x(\cos^3(x^2) - \sin^3(x^2)) \d x ={}& \frac{1}{2}\int \cos^3u  - \sin ^3u\d u\\
={}& \frac{1}{2}\int \cos^3u\d u - \frac{1}{2}\int \sin^3u\d u  \\
={}& \frac{1}{2}\int (1 - \sin^2u)\cos u\d u  - \frac{1}{2}\int (1 - \cos^2u)\sin u\d u \\
={}& \frac{1}{2}\int \cos u - \sin^2u\cos u\d u - \frac{1}{2}\int \sin u - \cos^2u\sin u\d u \\
={}& \frac{1}{2}\sin u - \frac{1}{6}\sin^3u + \frac{1}{2}\cos u - \frac{1}{6}\cos^3u \\
={}& \frac{1}{12}\left( 6(\sin u + \cos u) - 2(\sin^3u + \cos^3u) \right)\\
={}& \frac{1}{12}\left( 6(\sin u + \cos u) - 2(\sin u + \cos u)(\sin^2u + \cos^2u - \sin u\cos u) \right)\\
={}& \frac{\sin u + \cos u}{12}\left( {6 - (2 - \sin 2u)} \right) + C \\
={}& \frac{1}{12}(\sin (x^2) + \cos (x^2))(4 + \sin (2x^2)) + C
\end{align}$$
Thus the final answer is
$$\begin{equation}
\int x(\cos^3(x^2) - \sin^3(x^2))\d x  = \frac{1}{12}(\sin (x^2) + \cos (x^2))(4 + \sin (2x^2)) + C
\end{equation}$$
</div> 
 </div>


</div> </li>
<li> <div class="exercise"> [\(**\)] Evaluate the integral
$$\begin{equation}\int x\sqrt{1-x^4} \d x\end{equation}$$

<div class="answerBox"> 
 <button onclick="myFunction('answer119')" class="answerButton">Show Answer</button> 
 <div  id='answer119' class="answer" >
Let \(x^2 = \sin\theta\), and \(2x\d x = \cos\theta \d\theta\). Then the integral becomes
$$\begin{align}
\int x\sqrt{1-x^4} \d x ={}& \frac{1}{2}\int \sqrt{1-\sin^2\theta}\cos\theta \d\theta\\
={}&\frac{1}{2}\int \cos^2\theta \d\theta \\
={}& \frac{1}{2}\int\frac{1+\cos 2\theta}{2} \d\theta\\
={}& \frac{\theta}{4} + \frac{\sin 2\theta}{8} + C\\
={}& \frac{\theta}{4} + \frac{\sin\theta\cos\theta}{4} + C
\end{align}$$
Now plugging back in the original variables we have
$$\begin{equation}\int x\sqrt{1-x^4} \d x = \frac{\arcsin(x^2)}{4} + \frac{x^2\sqrt{1-x^4}}{4} + C\end{equation}$$
</div> 
 </div>



</div> </li>
<li> <div class="exercise"> [\(**\)] Evaluate the integral. $$\begin{equation}\int \sin^3(3x) \cos^5(3x) \d x\end{equation}$$

<div class="answerBox"> 
 <button onclick="myFunction('answer136')" class="answerButton">Show Answer</button> 
 <div  id='answer136' class="answer" >
Let \(3x = u\), and \(3\d x = \d u\). 
$$\begin{align}
\int \sin^3(3x) \cos^5(3x) \d x ={}& \frac{1}{3}\int \sin^3(u)\cos^5(u)\d u \\
={}& \frac{1}{3}\int (1 - \cos^2u)\sin u\cos^5(u)\d u 
\end{align}$$
Let \( \cos u = z\), and \(\d z = -\sin u \d u\). 
$$\begin{align}
\frac{1}{3}\int (1 - \cos^2u)\sin u\cos^5(u)\d u  ={}& \frac{1}{3}\int (z^2 - 1)z^5\d z  \\
={}& \frac{1}{3}\int z^7 - z^5\d z \\
={}& \frac{1}{3}\left( \frac{z^8}{8} - \frac{z^6}{6} \right)\\\
={}& \frac{1}{3}\left( \frac{\cos^8(3x)}{8} - \frac{\cos^6(3x)}{6} \right) + C
\end{align}$$
Thus the final answer is 
$$\begin{equation}
\int \sin^3(3x) \cos^5(3x) \d x = \frac{1}{3}\left( \frac{\cos^8(3x)}{8} - \frac{\cos^6(3x)}{6} \right) + C
\end{equation}$$
</div> 
 </div>



</div> </li>
<li> <div class="exercise"> [\(**\)] Evaluate the integral. $$\begin{equation}\int\tan^5 x \d x\end{equation}$$

<div class="answerBox"> 
 <button onclick="myFunction('answer159')" class="answerButton">Show Answer</button> 
 <div  id='answer159' class="answer" >
$$\begin{align}
\int \tan^5x\d x  ={}& \int (\sec^2x - 1)\tan^3x\d x  \\
={}& \int \sec^2x\tan^3x - \tan^3x\d x\\
={}& \frac{\tan^4x}{4} - \int(\sec^2x - 1)\tan x\d x  \\
={}& \frac{\tan^4x}{4} - \int \sec^2x\tan x - \tan x\d x \\
={}& \frac{\tan^4x}{4} - \frac{\tan^2x}{2} + \log \left| \sec x \right| + C
\end{align}$$
</div> 
 </div>




</div> </li>
<li> <div class="exercise"> [\(**\)] Evaluate the integral. 
$$\begin{equation}
\int \tan^3(2x)\sec^3(2x) \d x
\end{equation}$$

<div class="answerBox"> 
 <button onclick="myFunction('answer177')" class="answerButton">Show Answer</button> 
 <div  id='answer177' class="answer" >
First, let \(2x = u\) and \(2\d x = \d u\). 
$$\begin{align}
\int \tan^3(2x)\sec^3(2x)\d x  ={}& \frac{1}{2}\int \tan^3u\sec^3u\d u   \\
 ={}& \frac{1}{2}\int (\sec^2u - 1)\sec^3u\tan u\d u\\
 \end{align}$$
 Now let \( \sec u = z\) and \(\d z = \sec u\tan u\d u\).
 $$\begin{align}
\frac{1}{2}\int (\sec^2u - 1)\sec^3u\tan u\d u  ={}& \frac{1}{2}\int (z^2- 1)z^2 \d z \\
={}& \frac{1}{2}\int z^4 - z^2 \d z\\
 ={}& \frac{1}{2}\left( \frac{z^5}{5} - \frac{z^3}{3} \right) + C \\
 ={}& \frac{1}{2}\left( \frac{\sec^5(2x)}{5} - \frac{\sec^3(2x)}{3} \right) + C
\end{align}$$
</div> 
 </div>


</div> </li></ol>


