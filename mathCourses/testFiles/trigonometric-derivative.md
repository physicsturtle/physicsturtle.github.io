---
layout: page
title: Trigonometric Differentiation
course: test
unit: unit1
permalink: /test/trigonometric-differentiation/
---

Suppose we are interested in differentiating the functions 

$$f(x) = \sin(x),\quad g(x) = \cos(x).$$

The derivatives of these are 



<div class = "result"> Sine and Cosine Differentation:
$$\frac{d}{dx}\sin(x) = \cos(x),\quad \frac{d}{dx}\cos(x) = -\sin(x)$$ </div>

<button onclick="myFunction('answer1')" class="answerButton">Show Derivation</button>
<div  id="answer1" class="answer">
We show the differentiation of the sine function.

$$\begin{eqnarray}
\lim_{h \to 0} \frac{f(x+h) - f(x)}{h} &=& \lim_{h\to 0}\frac{\sin(x+h) - \sin(x)}{h}\\
&=& \lim_{h\to 0}\frac{\sin(x)\cos(h) + \cos(x)\sin(h) - \sin(x)}{h}\\
&=& \lim_{h\to 0}\frac{\sin(x)(\cos(h)-1) + \cos(x)\sin(h)}{h}\\
&=& \sin(x) \underbrace{\lim_{h\to 0}\frac{\cos(h)-1}{h}}_{=0} +  \cos(x)\underbrace{\lim_{h\to 0}\frac{\sin(h)}{h}}_{=1}\\
f'(x) &=& \cos(x)
\end{eqnarray}$$
</div> 



