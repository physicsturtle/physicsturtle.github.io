---
layout: lesson
title: Limit Laws
dept: math
course: calculus-I
unit: unit2
deptDisplay: Math
courseDisplay: Calculus I
unitDisplay: Unit 2
---

### Introduction

In the last section, we introduced the idea of a limit and worked some elementary examples. In this section, we introduce some rules for calculating limits and some strategies for evaluating more complicated limits. 

### Limit Properties

The properties of limits are thus. In the following, let $f,g$ be functions of $x$.

* $$\lim_{x\to a} \left[ f(x) \pm g(x)\right] = \lim_{x\to a} f(x) \pm \lim_{x\to a} g(x)$$
* $$\lim_{x\to a} \left[ f(x)g(x)\right] = \left[\lim_{x\to a} f(x)\right]\left[ \lim_{x\to a} g(x)\right]$$
* $$\lim_{x\to a} \left[ cf(x)\right] = c\lim_{x\to a} f(x)$$
* If $\lim_{x\to a} g(x) \not= 0$, then $$ \lim_{x\to a}\left[\frac{f(x)}{g(x)}\right] = \frac{\lim_{x\to a} f(x)}{\lim_{x\to a}g(x)}$$
* 

These limits properties can be applied to evaluate complicated limits. Many of these limit properties probably appear intuitive and you probably apply them without thinking. However, it is important to keep them in mind at all times. 

### Limit Evaluation Strategies

In the previous section on limits, we looked at limits where one could evaluate the limit simply by plugging in the limiting value of $x$. However, it is possible that plugging in the limiting value of $x$ leads to something like $\frac{0}{0}$. In these cases, more work must be done. 

#### Cancelling a Common Factor

Sometimes, if we have a function which is a ratio of polynomials, then the polynomials in the numerator and denominator can be factored, and something cancelled out. 

<div class="example">
<b>Example:</b> Evaluate the limit
  $$\lim_{x\to 3} \frac{x^2 + 2x - 15}{2x^2-3x-9}$$
<b>Solution:</b> If we first try to plug in $x = 3$ to the numerator and denominator, we get $\frac{0}{0}$. This means that more work must be done. 
$$\begin{eqnarray*}
\lim_{x\to 3} \frac{x^2 + 2x - 15}{2x^2-3x-9} &=& \lim_{x\to 3} \frac{(x-3)(x+5)}{(x-3)(2x+3)}\\
  &=& \lim_{x\to 3} \frac{x+5}{2x+3}\\
  &=& \frac{3+5}{2(3)+3}\\
  &=& \frac{8}{9}
  \end{eqnarray*}$$
  where we notice that, after the factors of $x-3$ have been cancelled out, we no longer get $\frac{0}{0}$ when directly plugging in 3. 
</div>

#### Multiplying by the Conjugate

There is another situation that leads to $\frac{0}{0}$ but does not allow a simple factorization as before. Often these situations involve a square root expression.

<div class="example">
<b>Example:</b> Evaluate the limit
  $$\lim_{x\to 1}\frac{2-\sqrt{5-x^2}}{x^2+x-2}$$
<b>Solution:</b>
  First, we notice that naïvely plugging in $x = 1$ leads to $\frac{0}{0}$. If we multiply numerator and denominator by $2 + \sqrt{5-x^2}$, then we get
$$\begin{eqnarray*}
\lim_{x\to 1}\frac{2-\sqrt{5-x^2}}{x^2+x-2}&=& \lim_{x\to 1}\frac{2-\sqrt{5-x^2}}{(x-1)(x+2)} \left(\frac{2 + \sqrt{5-x^2}}{2 + \sqrt{5-x^2}}\right)\\
&=& \lim_{x\to 1}\frac{4-(5-x^2)}{(x-1)(x+2)(2 + \sqrt{5-x^2})}\\
&=& \lim_{x\to 1}\frac{x^2-1}{(x-1)(x+2)(2+\sqrt{5-x^2})}\\
&=& \lim_{x\to 1}\frac{(x-1)(x+1)}{(x-1)(x+2)(2+\sqrt{5-x^2})}\\
&=& \lim_{x\to 1}\frac{(x+1)}{(x+2)(2+\sqrt{5-x^2})} \\
&=& \frac{(1+1)}{(1+2)(2+\sqrt{5-1^2})}\\
&=& \frac{2}{(3)(4)}\\
&=& \frac{1}{6}
\end{eqnarray*}$$
where we notice again that plugging in $x = 1$ only works after we have done the cancellations. 
</div>

#### Reducing to a Known Limit

There are certain limits whose values are known, but which are difficult to prove. I advise that you memorize these results. A couple examples of ones which you should memorize are 

$$\lim_{x\to 0} \frac{\sin x}{x},\qquad \lim_{n\to\infty} \left(1 + \frac{x}{n}\right)^{n} = e^x$$

The first of these two will be shown geometrically in a separate lesson. The second is much more difficult to prove, and we quote it without proof.

<div class="example">
<b>Example:</b> Calculate the following limit
  $$\lim_{x\to 0}\frac{1-\cos x}{x^2}$$
<b>Solution:</b> Notice that plugging in zero gives us $\frac{0}{0}$. Thus, we multiply and divide by the conjugate $1+\cos x$, as has been done before. This gives us
$$\begin{eqnarray*}
\lim_{x\to 0}\frac{1-\cos x}{x^2} &=& \lim_{x\to 0}\frac{1-\cos x}{x^2}\frac{1+\cos x}{1+\cos x}\\
&=& \lim_{x\to 0}\frac{1-\cos^2 x}{x^2(1+\cos x)}\\
&=& \lim_{x\to 0}\frac{\sin^2 x}{x^2(1+\cos x)}\\
&=& \left(\lim_{x\to 0}\frac{\sin x}{x}\right)^2 \lim_{x\to 0}\frac{1}{(1+\cos x)}\\
&=& \frac{1}{2}
\end{eqnarray*}$$
</div>

