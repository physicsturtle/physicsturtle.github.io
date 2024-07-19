---
layout: page
title: Chain Rule
course: test
unit: unit1
permalink: /test/chain-rule
---

Suppose we are interested in differentiating the function 

$$f(x) = u(v(x))$$

This is a nested function. The rule for differentiating this kind of function is known as the *chain rule*. It is more difficult to derive than the product and quotient rules, and is:

<div class = "result"> Chain Rule:
$$f'(x) = u'(v(x))v'(x)$$ </div>

<button onclick="myFunction('answer1')" class="answerButton">Show Derivation</button>
<div  id="answer1" class="answer">
We will now derive the *chain rule*, which tell us the  For this, we use the definition of the derivative. Define $\Delta v = v(x+h) - v(x)$. 

$$\begin{eqnarray}
\lim_{h \to 0} \frac{f(x+h) - f(x)}{h} &=& \lim_{h\to 0}\frac{u(v(x+h)) - u(v(x))}{h}\\
&=& \lim_{h\to 0}\frac{u(v(x+h)) - u(v(x))}{h}\underbrace{\lim_{\Delta v \to 0}\frac{v(x+h) - v(x)}{v(x+h) - v(x)}}_{=1}\\
&=& \lim_{h\to 0} \lim_{\Delta v \to 0} \frac{u(v(x+h)) - u(v(x))}{v(x+h) - v(x)}\frac{v(x+h) - v(x)}{h}\\
&=&  \lim_{\Delta v \to 0} \frac{u(v(x+h)) - u(v(x))}{v(x+h) - v(x)}\lim_{h\to 0}\frac{v(x+h) - v(x)}{h}\\
f'(x) &=& u'(v(x))v'(x)
\end{eqnarray}$$
</div> 





