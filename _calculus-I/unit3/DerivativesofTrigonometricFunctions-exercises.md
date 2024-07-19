---
layout: exercises
title: Derivatives of Trigonometric Functions  - Exercises
dept: math
course: calculus-I
unit: unit3
deptDisplay: Math
courseDisplay: Calculus I
unitDisplay: Unit 3
---
<ol>
<li> <div class="exercise">  Suppose \(f(x)\) is defined as 
$$\begin{equation}f(x) = \lim_{t \to x}\frac{\sec t - \sec x}{t - x}\end{equation}$$
Compute \(f'(\pi/4)\).

<div class="answerBox"> 
 <button onclick="myFunction('answer5')" class="answerButton">Show Answer</button> 
 <div  id='answer5' class="answer" >
First, notice that the limit resembles the definition of the derivative of the\\ form $$\begin{equation}\lim_{t\to a} \frac{g(t)-g(a)}{t-a}\end{equation}$$ where \(g(t)=\sec(t)\) and \(a=x\).\\\\
Then, write out the limit in the form of a derivative.\\
$$\begin{align}
\lim_{t \to x}\frac{\sec t - \sec x}{t - x} ={}& \frac{\d}{\d t}(\sec(t))\quad for \quad g'(x)\\
={}& \sec(t)\tan(t)\\
={}& \sec(x)\tan(x)\\
\end{align}$$
Now that we have \(f(x)=g'(x)\), we take another derivative using the product rule to find \(f'(\frac{\pi}{4})\).
$$\begin{align}
\frac{\d}{\d x}(f(x)) = \frac{\d}{\d x}(\sec(x)\tan(x)) ={}& (\sec(x)\tan(x))\tan(x)+\sec^2(x)\sec(x)\\
={}& \sec(x)\tan^2(x) + \sec^3(x)\\
={}& \frac{\sin^2(x)}{\cos^3(x)}+\frac{1}{\cos^3(x)}\\
={}& \frac{(\frac{1}{\sqrt{2}})^2}{(\frac{1}{\sqrt{2}})^3}+\frac{1}{(\frac{1}{\sqrt{2}})^3}\\
={}& \sqrt{2}+2\sqrt{2}\\
={}& 3\sqrt{2}\\
\end{align}$$
</div> 
 </div>

</div> </li>
<li> <div class="exercise">  Evaluate the limit $$\begin{equation}\lim_{x\to-\pi/4}\frac{\tan x + 1}{x + \pi/4}\end{equation}$$.

<div class="answerBox"> 
 <button onclick="myFunction('answer26')" class="answerButton">Show Answer</button> 
 <div  id='answer26' class="answer" >
We will present two different but correct solutions here:
<ol>[(i)]
<li>  First, we notice that the limit resembles the definition of the derivative of the form 
$$\begin{equation}\lim_{x\to a}\frac{f(x)-f(a)}{x-a}\end{equation}$$ where \(f(x)=\tan(x)\) and \(a=-\frac{\pi}{4}\).\\
Then, write out the limit in the form of a derivative.\\
$$\begin{align}
\lim_{x\to-\pi/4}\frac{\tan x + 1}{x + \pi/4} ={}& \frac{\d}{\d x}(\tan(x)) \quad \text{for} \quad f'\left(-\frac{\pi}{4}\right)\\
={}& \sec^2(x)\\
={}& \sec^2(-\frac{\pi}{4})\\
={}& \frac{1}{\cos^2(-\frac{\pi}{4})}\\
={}& \frac{1}{(\frac{1}{\sqrt{2}})^2}\\
={}& 2\\
\end{align}$$

</li>
<li> Alternatively:\\
Substitute out the denominator using \(h=x + \frac{\pi}{4}\).\\
$$\begin{align}
\lim_{x\to-\pi/4}\frac{\tan x + 1}{x + \frac{\pi}{4}} ={}& \lim_{h\to0}\frac{\tan (h-\frac{\pi}{4}) + 1}{h}\\
\end{align}$$
Next, use the trigonometric identity \(\tan(A-B) = \frac{\tan(A)-\tan(B)}{1+\tan(A)\tan(B)}.\)\\
$$\begin{align}
\lim_{h\to0}\frac{\tan (h-\frac{\pi}{4}) + 1}{h} ={}& \lim_{h\to0}\frac{\frac{\tan(h)-\tan(\frac{\pi}{4})}{1+\tan(h)\tan(\frac{\pi}{4})} + 1}{h}\\
={}& \lim_{h\to0}\frac{\frac{\tan(h)-(1)}{1+\tan(h)(1)} + 1}{h}\\
={}& \lim_{h\to0}\frac{\frac{\tan(h)-1}{1+\tan(h)} + 1}{h}\\
={}& \lim_{h\to0}\frac{\tan(h)-1 + 1+\tan(h)}{h(1+\tan(h))}\\
={}& \lim_{h\to0}\frac{2\tan(h)}{h(1+\tan(h))}\\
={}& \lim_{h\to0}\frac{2(\frac{\sin(h)}{\cos(h)})}{h(1+\tan(h))}\cdot\frac{\cos(h)}{\cos(h)}\\
={}& \lim_{h\to0}\frac{2\sin(h)}{h(\cos(h)+\sin(h))}\\
={}& \lim_{h\to0}\frac{\sin(h)}{h}\cdot\frac{2}{\cos(h)+\sin(h)}\\
\end{align}$$
It is well-known that \(\displaystyle\lim_{h\to0}\frac{\sin(h)}{h}\) equals to 1, thus
$$\begin{align}
={}& 1\cdot\frac{2}{1+0}\\
={}& 2
\end{align}$$
</li></ol>
</div> 
 </div>
	
</div> </li></ol>



