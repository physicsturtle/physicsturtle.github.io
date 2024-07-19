---
layout: page
title: Power Rule
course: test
unit: unit1
permalink: /test/power-rule/
---

Suppose we are interested in differentiating the function 

$$f(x) = x^\alpha$$

where $\alpha$ is a real number. This can be derived easily for the case of $\alpha$ being a real number. That derivation will be shown here, and the derivation for other $\alpha$, such as rational or arbitrary real, will be shown in later sections, after we have developed more tools for differentiation.

<div class = "result"> Power Rule:
$$f'(x) = \alpha x^{\alpha - 1}$$ </div>

<button onclick="myFunction('answer1')" class="answerButton">Show Derivation</button>
<div  id="answer1" class="answer">
We will now derive the *power rule*, for the case of integer $\alpha = n$. For this, we use the definition of the derivative.

$$\begin{eqnarray}
\lim_{h \to 0} \frac{f(x+h) - f(x)}{h} &=& \lim_{h\to 0}\frac{(x+h)^n- x^n}{h}\\
&=& \lim_{h\to 0}\frac{ \sum_{k = 0}^n x^k h^{n-k}\binom{n}{k} - x^n}{h}\\
&=& \lim_{h\to 0}\frac{ \sum_{k = 1}^{n} x^{n-k} h^{k}\binom{n}{k}}{h}\\
&=& \lim_{h\to 0}\sum_{k = 1}^{n} x^{n-k} h^{k-1}\binom{n}{k}\\
&=& \lim_{h\to 0} x^{n-1} \binom{n}{1}\\
f'(x) &=& n x^{n - 1}
\end{eqnarray}$$
</div> 



