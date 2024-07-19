---
layout: exercises
title: Integration by Parts  - Exercises
dept: math
course: calculus-II
unit: unit2
deptDisplay: Math
courseDisplay: Calculus II
unitDisplay: Unit 2
---
<ol>

<li> <div class="exercise">  Evaluate the integral
$$\begin{equation}\int x^2\sin 3x \d x \end{equation}$$

<div class="answerBox"> 
 <button onclick="myFunction('answer5')" class="answerButton">Show Answer</button> 
 <div  id='answer5' class="answer" >
To solve this problem, we note that the function which we want to differentiate is the \(x^2\). The sine does not become more complicated if it's integrated, but the \(x^2\) becomes simpler if differentiated. We will have to integrate by parts twice. Thus, 
$$\begin{align}
\int x^2\sin 3x \d x ={}& -x^2\frac{\cos 3x}{3} + \frac{2}{3}\int x\cos 3x \d x \\
={}& -\frac{x^2}{3}\cos 3x + \frac{2x}{9}\sin 3x - \frac{2}{9}\int \sin 3x \d x \\
={}& -\frac{x^2}{3}\cos 3x + \frac{2x}{9}\sin 3x + \frac{2}{27}\cos 3x + C
\end{align}$$

</div> 
 </div>

</div> </li>
<li> <div class="exercise">  Evaluate the integral
$$\begin{equation}\int x^3 e^{-x} \d x \end{equation}$$

<div class="answerBox"> 
 <button onclick="myFunction('answer18')" class="answerButton">Show Answer</button> 
 <div  id='answer18' class="answer" >
To solve this problem, we note that the function we want to differentiate is the \(x^2\). The exponential does not become more complicated if it's integrated, but the \(x^3\) becomes simpler if differentiated. We will have to integrate by parts three times. Thus, 
$$\begin{align}
\int x^3 e^{-x} \d x ={}& -x^3 e^{-x} + \int 3x^2 e^{-x} \d x \\
={}& -x^3 e^{-x} - 3x^2 e^{-x} + \int 6x e^{-x} \d x \\
={}& -x^3 e^{-x} -3x^2 e^{-x} - 6x e^{-x} + \int 6 e^{-x} \d x \\
={}& -(x^3 + 3x^2 + 6x + 6)e^{-x} + C
\end{align}$$
</div> 
 </div>


</div> </li>
<li> <div class="exercise"> [\(**\)] Evaluate the integral
$$\begin{equation}\int^\pi_0 e^{\cos t}\sin(2t) \d t\end{equation}$$

<div class="answerBox"> 
 <button onclick="myFunction('answer32')" class="answerButton">Show Answer</button> 
 <div  id='answer32' class="answer" >
First we will find the antiderivative. Let \(u = \cos t\), and \(\d u = -\sin t \d t\).
$$\begin{align}
\int e^{\cos t}\sin(2t) \d t ={}& \int e^{\cos t} 2\sin t \cos t \d t \\
={}& -2\int e^u u \d u\\
={}& -2 (u-1)e^u + C\\
={}& 2(1-\cos t)e^{\cos t} + C
\end{align}$$
Now evaluating at the bounds of integration, we have 
$$\begin{equation}\int^\pi_0 e^{\cos t}\sin(2t) \d t = 2(1-\cos \pi) e^{\cos \pi} - 0 = \frac{4}{e}\end{equation}$$
</div> 
 </div>


</div> </li>
<li> <div class="exercise"> [\(**\)] Evaluate the integral
$$\begin{equation}\int\cos\left(\sqrt{x}\right) \d x\end{equation}$$

<div class="answerBox"> 
 <button onclick="myFunction('answer48')" class="answerButton">Show Answer</button> 
 <div  id='answer48' class="answer" >
First make the substitution \(u = \sqrt{x}\), and \(2u \d u = \d x\):
$$\begin{equation}\int\cos\left(\sqrt{x}\right) \d x = \int\cos(u) 2u \d u\end{equation}$$
Now integrating by parts, we have
$$\begin{equation} \int\cos(u) 2u \d u = 2\left(u\sin u - \int\sin u \d u\right)\end{equation}$$
Thus the final answer in terms of \(u\) is
$$\begin{equation}2u\sin u + 2\cos u +C\end{equation}$$
Then putting back in terms of \(x\),
$$\begin{equation}\int\cos\left(\sqrt{x}\right) \d x = 2\sqrt{x}\sin\left(\sqrt{x}\right) + 2\cos\left(\sqrt{x}\right) + C\end{equation}$$
</div> 
 </div>


</div> </li>
<li> <div class="exercise"> [\(**\)]Evaluate the integral
$$\begin{equation}\int \cos\left(\log x\right) \d x\end{equation}$$

<div class="answerBox"> 
 <button onclick="myFunction('answer63')" class="answerButton">Show Answer</button> 
 <div  id='answer63' class="answer" >
First, let \(\log x = u\). Then \(\d u = \d x/x = e^{-u} \d x\). Thus \(\d x = e^u \d u\). We can then transform the integral as
$$\begin{equation}\int \cos\left(\log x\right) \d x = \int \cos u e^u \d u\end{equation}$$
We then integrate by parts twice, both times integrating the exponential, and differentiating the trigonometric function. Note that we would get the same result had we instead differentiated the exponential, and integrated the trigonometric function. 
$$\begin{equation}\int e^u \cos u \d u = e^u\cos u + e^u \sin u - \int e^u\cos u \d u\end{equation}$$
Rearranging, we have
$$\begin{equation}2\int e^u \cos u \d u = e^u(\cos u + \sin u)\end{equation}$$
Then solving for the integral, we have
$$\begin{equation}\int e^u\cos u \d u = \frac{e^u}{2}(\cos u + \sin u)\end{equation}$$
Now plugging back in the original variables, we have
$$\begin{equation}\int \cos\left(\log x\right) \d x = \frac{x}{2}(\cos(\log x) + \sin(\log x)) + C\end{equation}$$

</div> 
 </div>


</div> </li>
<li> <div class="exercise"> [\(***\)] Evaluate the integral
$$\begin{equation}\int x\arctan x \d x \end{equation}$$

<div class="answerBox"> 
 <button onclick="myFunction('answer81')" class="answerButton">Show Answer</button> 
 <div  id='answer81' class="answer" >
First we need to compute
$$\begin{equation}\int\arctan x \d x\end{equation}$$
The way to do this is to integrate by parts, letting \(u' = 1\), and \(v = \arctan x\). Then we have
$$\begin{equation}\int\arctan x \d x = x\arctan x - \int\frac{x}{x^2+1}\d x\end{equation}$$
This then evaluates to 
$$\begin{equation}\int\arctan x \d x = x\arctan x - \frac{1}{2}\log(1+x^2)\end{equation}$$
Now we return to the original integral. We will have to integrate by parts. Let \(x = u'\), and \(\arctan x = v\). Then we have
$$\begin{align}
\int x\arctan x \d x ={}& \frac{x^2}{2}\arctan x - \frac{1}{2}\int \frac{x^2}{1+x^2}\d x \\
={}& \frac{x^2}{2}\arctan x - \frac{1}{2}\int\frac{x^2+1}{1+x^2} - \frac{1}{1+x^2} \d x\\
={}& \frac{x^2}{2}\arctan x - \frac{x}{2} + \frac{\arctan x}{2} + C
\end{align}$$
Thus we have
$$\begin{equation}\int x\arctan x \d x =\frac{x^2}{2}\arctan x - \frac{x}{2} + \frac{\arctan x}{2} + C \end{equation}$$
</div> 
 </div>


</div> </li>
<li> <div class="exercise"> [\(**\)] Find the value of the integral. $$\begin{equation}\int^e_1 \log x \d x\end{equation}$$

<div class="answerBox"> 
 <button onclick="myFunction('answer101')" class="answerButton">Show Answer</button> 
 <div  id='answer101' class="answer" >
$$\begin{align}
\int_1^e \log x\d x  ={}& \left. \left( x\log x - x \right) \right|_1^e \\
={}& e\log e - e - (1\log 1 - 1) \\
={}& e - e + 1 \\
={}& 1
\end{align}$$
$$\begin{equation}\int_1^e \log x\d x  = 1\end{equation}$$

</div> 
 </div>


</div> </li>
<li> <div class="exercise"> [\(**\)] Evaluate the integral. $$\begin{equation}\int (\sin x)(\sin 3x) \d x\end{equation}$$

<div class="answerBox"> 
 <button onclick="myFunction('answer115')" class="answerButton">Show Answer</button> 
 <div  id='answer115' class="answer" >
We will have to integrate this by parts twice:
$$\begin{align}
\int (\sin x)(\sin 3x)\d x ={}&  - \cos x\sin 3x + 3\int \cos x\cos 3x\d x \\
={}&  - \cos x\sin 3x + 3\left( \sin x\cos 3x + 3\int \sin x\sin 3x\d x \right)\\
={}&  - \cos x\sin 3x + 3\sin x\cos 3x + 9\int {\sin x\sin 3x\d x} 
\end{align}$$
Rearranging:
$$\begin{equation} - 8\int \sin x\sin 3x\d x =  - \cos x\sin 3x + 3\sin x\cos 3x\end{equation}$$
$$\begin{equation}\int {\sin x\sin 3x\d x}  = \frac{1}{8}\cos x\sin 3x - \frac{3}{8}\sin x\cos 3x + C\end{equation}$$
</div> 
 </div>


</div> </li>
<li> <div class="exercise"> [\(***\)] Evaluate the integral. $$\begin{equation}\int x\arcsin x \d x\end{equation}$$

<div class="answerBox"> 
 <button onclick="myFunction('answer130')" class="answerButton">Show Answer</button> 
 <div  id='answer130' class="answer" >
We will need to integrate by parts. Let \(u = x\), and \(v' = \arcsin x\). First we need to find \(v(x)\). For this integral, integrate by parts, with the two functions being \(1\) and \(\arcsin x\). 
$$\begin{align}
v(x) = \int \arcsin x\d x  = x\arcsin x + \sqrt{1 - x^2}
\end{align}$$
$$\begin{align}
\int x\arcsin x\d x  ={}& x\left( x\arcsin x + \sqrt{1 - x^2} \right) - \int\left( x\arcsin x + \sqrt{1 -x^2} \right)\d x\\
={}& x^2\arcsin x + x\sqrt{1 - x^2}  - \int x\arcsin x\d x - \int {\sqrt{1 - x^2} \d x} \\
\end{align}$$
Rearranging, 
$$\begin{equation}
2\int x\arcsin x\d x = x^2\arcsin x + x\sqrt{1 - x^2}  - \int {\sqrt{1 - x^2} \d x} 
\end{equation}$$
Now we need to find the antiderivative of \(\sqrt{1-x^2}\). To do this, let \(x = \sin z\), and \(\d x = \cos z \d z\). 
$$\begin{align}
\int \sqrt{1 - x^2} \d x  ={}& \int \cos z^2\d z \\
={}& \frac{1}{2}\int 1 + \cos 2z\d z \\
={}& \frac{z}{2} +\frac{\sin 2z}{4} \\
={}& \frac{z}{2} + \frac{\sin z\cos z}{2}\\
={}& \frac{\arcsin x}{2} + \frac{x\sqrt{1-x^2}}{2} 
\end{align}$$
$$\begin{align}
2\int {x\arcsin x\d x}  = x^2\arcsin x + x\sqrt{1 - x^2}  -\left(  \frac{\arcsin x}{2} + \frac{x\sqrt{1-x^2}}{2}\right)\\
2\int {x\arcsin x\d x}  = x^2\arcsin x + \frac{x\sqrt{1 - x^2}}{2} - \frac{\arcsin x}{2} + C
\end{align}$$
Thus the final answer is 
$$\begin{equation}
\int {x\arcsin x\d x}  = \frac{x^2\arcsin x}{2} + \frac{x\sqrt{1 - x^2}}{4} - \frac{\arcsin x}{4} + C
\end{equation}$$
</div> 
 </div>


</div> </li>
<li> <div class="exercise">  Evaluate the integral.
$$\begin{equation}\int e^{-3x}\sin (2x) \d x\end{equation}$$

<div class="answerBox"> 
 <button onclick="myFunction('answer165')" class="answerButton">Show Answer</button> 
 <div  id='answer165' class="answer" >
In this one, we will need to integrate by parts twice. Let's integrate the exponential and differentiate the sine.
 
$$\begin{equation}\int e^{-3x}\sin (2x) \d x = -\frac{1}{3}e^{-3x}\sin 2x + \frac{2}{3}\int e^{-3x}\cos 2x \d x \end{equation}$$

Applying integration by parts again by differentiating the cosine and integrating the exponential, 

$$\begin{align}
\int e^{-3x}\sin (2x) \d x ={}& -\frac{1}{3}e^{-3x}\sin 2x + \frac{2}{3}\left(-\frac{1}{3}e^{-3x}\cos 2x - \frac{2}{3}\int e^{-3x}\sin 2x \d x\right)  \\
={}& -\frac{1}{3}e^{-3x}\sin 2x - \frac{2}{9}e^{-3x}\cos 2x - \frac{4}{9}\int e^{-3x}\sin 2x \d x
\end{align}$$

Moving both integrals to the same side, 

$$\begin{align}
\left(1 + \frac{4}{9}\right)\int e^{-3x}\sin 2x \d x ={}& -\frac{1}{3}e^{-3x}\sin 2x - \frac{2}{9}e^{-3x}\cos 2x\\
\frac{13}{9}\int e^{-3x}\sin 2x \d x ={}& -\frac{1}{9}e^{-3x}(3\sin 2x + 2\cos 2x)
\end{align}$$

Lastly, isolating the integral, we get 
$$\begin{equation}\int e^{-3x}\sin 2x \d x = -\frac{1}{13}e^{-3x}(3\sin 2x + 2\cos 2x) + C\end{equation}$$
</div> 
 </div>


</div> </li>
<li> <div class="exercise">  Evaluate the integral. 
$$\begin{equation}\int e^{3x}x^2\sin x \d x\end{equation}$$

<div class="answerBox"> 
 <button onclick="myFunction('answer192')" class="answerButton">Show Answer</button> 
 <div  id='answer192' class="answer" >
Let \(e^{3x}\sin x = u'(x)\). We will have to use integration by parts multiple times, first to get rid of the \(x^2\) term, then to integrate the remaining exponential and sine.

Let \(U'(x)  =  u(x).\)

$$\begin{align}
\int x^2 u' \d x ={}& x^2 u - 2\int xu \d x  \\
={}& x^2u - 2\left( xU - \int U \d x \right)\\
\end{align}$$

First, we need to find \(u(x)\), with \(u'(x)\) defined as above. 

$$\begin{align}
u(x) ={}& \int u'(x) \d x \\
={}& \int e^{3x}\sin x \d x \\
={}& \frac{e^{3x}}{3}\sin x - \frac{1}{3}\int e^{3x}\cos x \d x\\
={}& \frac{e^{3x}}{3}\sin x - \frac{1}{3}\left( \frac{e^{3x}}{3} + \frac{1}{3}\int e^{3x}\sin x \d x \right)
\end{align}$$

Rearranging, 

$$\begin{equation}\frac{10}{9}\int e^{3x}\sin x \d x = \frac{e^{3x}}{9}\left( 3\sin x - \cos x\right)\end{equation}$$

which tells us that, after a simple rearrangement,

$$\begin{equation}\int e^{3x}\sin x \d x  = \frac{e^{3x}}{10}\left( 3\sin x - \cos x \right).\end{equation}$$

In order to find \(U(x)\), having already found \(u(x)\), we need to perform the same procedure as in the previous integration. This is left to the reader, as it has already been shown once. 

$$\begin{align}
U(x) ={}& \int u(x) \d x \\
={}& \frac{e^{3x}}{50}\left( 4\sin x - 3\cos x \right) 
\end{align}$$
Lastly, we need the antiderivative of \(U(x)\). That is computed in the same way as the two previous:

$$\begin{equation}\int U(x)\d x = \frac{e^{3x}}{500}(9\sin x - 13\cos x) \end{equation}$$

Plugging back into the original expression yields:

$$\begin{align}
x^2u - 2\left( xU - \int U\d x \right) ={}& x^2\left( \frac{e^{3x}}{10}\left( 3\sin x - \cos x \right) \right) - 2x\left( \frac{e^{3x}}{50}\left( 4\sin x - 3\cos x \right) \right) + \\
&+2\left( \frac{e^{3x}}{500}(9\sin x - 13\cos x)\right)\\
={}& \frac{e^{3x}}{250}\left( {25x^2(3\sin x - \cos x) - 10x(4\sin x - 3\cos x) + 9\sin x - 13\cos x} \right) + C
\end{align}$$

$$\begin{equation}
\int e^{3x}x^2\sin x \d x = \frac{e^{3x}}{250}\left( 25x^2(3\sin x - \cos x) - 10x(4\sin x - 3\cos x) + 9\sin x - 13\cos x \right) + C
\end{equation}$$

</div> 
 </div>

</div> </li></ol>


