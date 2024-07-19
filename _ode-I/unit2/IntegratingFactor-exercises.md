---
layout: exercises
title: Integrating Factor  - Exercises
dept: math
course: ode-I
unit: unit2
deptDisplay: Math
courseDisplay: Ordinary Differential Equations I
unitDisplay: Unit 2
---
<ol>
<li> <div class="exercise">  Solve the following differential equation for \(y= y(x)\) 

$$\begin{align}
\frac{\d y}{\d x} - \frac{2xy}{x^2+1} = 1.
\end{align}$$

<div class="answerBox"> 
 <button onclick="myFunction('answer7')" class="answerButton">Show Answer</button> 
 <div  id='answer7' class="answer" >
Find the integrating factor 

$$\begin{align}
\mu(x) ={}& e^{\int \frac{-2x}{x^2+1}\d x} \\
={}& e^{-\log(x^2+1)} \\
={}& \frac{1}{x^2+1}
\end{align}$$

Multiply both sides of the equation by the integrating factor 

$$\begin{align}
\frac{1}{x^2+1}\frac{\d y}{\d x} - \frac{2x}{(x^2+1)^2}y = \frac{1}{x^2+1} = \left(\frac{y}{1+x^2}\right)'
\end{align}$$

Integrating, \(\displaystyle{\frac{y}{x^2+1} = \arctan x + C \Rightarrow y = (x^2+1)\arctan x + C(x^2+1)}\)
</div> 
 </div>

</div> </li>
<li> <div class="exercise">  Solve the following differential equation for \(r=r(\theta)\).    

$$\begin{align}
\tan \theta \frac{\d r}{\d  \theta} - r = \tan^2 \theta
\end{align}$$

<div class="answerBox"> 
 <button onclick="myFunction('answer31')" class="answerButton">Show Answer</button> 
 <div  id='answer31' class="answer" >
Put this in the form in which we will use the integrating factor \(\mu(\theta)\). 

$$\begin{align}
r' - r\cot \theta  = \tan \theta
\end{align}$$

This tells us that the integrating factor is given by

$$\begin{align}
\mu ={}& e^{\int -\cot \theta \d \theta} \\
={}& e^{-\log \sin x} \\
={}& \csc \theta
\end{align}$$

Differential equation will become 

$$\begin{align}
r' \csc \theta -r \csc \theta \cot \theta  = \sec \theta = (r\csc \theta)'
\end{align}$$

Integrating, 

$$\begin{align}
\log(\sec \theta + \tan \theta ) +C= r \csc \theta
\end{align}$$

Thus, 

$$\begin{align}
r(\theta) = C\sin \theta + \sin \theta \log(\sec \theta + \tan \theta)
\end{align}$$

</div> 
 </div>


</div> </li>
<li> <div class="exercise">  Solve the equation.

$$\begin{align}
\frac{\d r}{\d \theta} = (r + e^{-\theta})\tan \theta
\end{align}$$

<div class="answerBox"> 
 <button onclick="myFunction('answer73')" class="answerButton">Show Answer</button> 
 <div  id='answer73' class="answer" >
We will rearrange this into the first order linear form: \(r' - r\tan \theta = e^{-\theta} \tan\theta\)

The integrating factor will be 

$$\begin{align}
\mu(x) = e^{\int -\tan \theta \d \theta} = e^{\log \cos \theta} = \cos \theta
\end{align}$$

Multiplying through by the integrating factor, we get 

$$\begin{align}
r'\cos \theta - r\sin \theta = e^{-\theta} \sin \theta = (r\cos \theta)'
\end{align}$$

Integrating, 

$$\begin{align}
r\cos \theta ={}& \int e^{-\theta}\sin \theta \d \theta = \frac{-e^{-\theta}}{2}(\cos \theta + \sin \theta)+C \\
r(\theta) ={}& \frac{-e^{-\theta}}{2}(1+\tan\theta) + C\sec \theta
\end{align}$$

</div> 
 </div>

</div> </li>
<li> <div class="exercise">  Solve the equation. \(xy' - y =x^2\sin x\)\\

<div class="answerBox"> 
 <button onclick="myFunction('answer99')" class="answerButton">Show Answer</button> 
 <div  id='answer99' class="answer" >
Rearranging into standar\d  form, \(\displaystyle{y' - \frac{y}{x} = x\sin x}\)\\
\\
The integrating factor is \(\mu(x) = e^{\int -1/x \d x} = e^{-\log x} = \frac{1}{x}\)
\\
Multiplying through, \(\displaystyle{\frac{y'}{x} - \frac{y}{x^2} = \sin x = \left( \frac{y}{x} \right)' }\)\\
\\
Integrating, \(\displaystyle{\left(\frac{y}{x}\right) = -\cos x + C}\)\\
\\
\(y(x) = -x\cos x + Cx\).\\
</div> 
 </div>

</div> </li>
<li> <div class="exercise">  Solve the equation. \(\displaystyle{x\frac{\d y}{\d x} + 2y = \frac{-\sin x}{x}}\)\\

<div class="answerBox"> 
 <button onclick="myFunction('answer113')" class="answerButton">Show Answer</button> 
 <div  id='answer113' class="answer" >
Rearange the equation into standar\d  form: \(\displaystyle{\frac{\d y}{\d x} + \frac{2}{x}y = \frac{-\sin x}{x^2}}\)\\
\\
Find the integrating factor: \(\mu(x) = e^{\int \frac{2}{x} \d x} = e^{\log x^2} = x^2\)\\
\\
Multiplying through, \(\displaystyle{x^2\frac{\d y}{\d x} + 2xy = -\sin x = (x^2y)'}\)\\
\\
Integrating, \((yx^2) = \cos x +C \Rightarrow y = x^{-2}\cos x + Cx^{-2}\)\\
</div> 
 </div>



















</div> </li></ol>


