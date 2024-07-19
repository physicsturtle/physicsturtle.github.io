---
layout: page
title: Product Rule
course: test
unit: unit1
permalink: /test/product-rule/
---

Suppose we are interested in differentiating the function 

$$f(x) = u(x)v(x).$$

We have already learned that the derivative of a sum of functions, $f(x) = u(x) + v(x)$ is $f'(x) = u'(x) + v'(x)$. However, it is not the case that if $f(x) = u(x)v(x)$, then $\cancel{f'(x) = u'(x)v'(x)}$. The correct formula for the derivative of a product of functions is:

<div class = "result"> Product Rule:
$$f'(x) = u(x)v'(x) + u'(x)v(x)$$ </div>

<button onclick="myFunction('answer1')" class="answerButton">Show Derivation</button>
<div  id="answer1" class="answer">
We will now derive the *product rule*, which tell us the  For this, we use the definition of the derivative. 

$$\begin{eqnarray}
\lim_{h \to 0} \frac{f(x+h) - f(x)}{h} &=& \lim_{h\to 0} \frac{u(x+h)v(x+h) - u(x)v(x)}{h}\\
&=& \lim_{h\to 0} \frac{u(x+h)v(x+h) + u(x+h)v(x) - u(x+h)v(x) - u(x)v(x)}{h}\\
&=& \lim_{h\to 0} \frac{u(x+h)(v(x+h) -v(x)) + (u(x+h)-u(x))v(x)}{h}\\
&=& \lim_{h\to 0} \frac{u(x+h)(v(x+h) -v(x))}{h} + \lim_{h\to 0}\frac{(u(x+h)-u(x))v(x)}{h}\\
&=& \lim_{h\to 0}u(x+h)\left(\lim_{h\to 0} \frac{(v(x+h) -v(x))}{h}\right) + \left(\lim_{h\to 0}\frac{(u(x+h)-u(x))}{h}\right)v(x)\\
f'(x) &=& u(x)v'(x) + u'(x)v(x)\\
\end{eqnarray}$$
</div> 







