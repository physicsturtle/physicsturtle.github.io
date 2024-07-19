---
layout: lesson
title: Derivatives of Trigonometric Functions
dept: math
course: calculus-I
unit: unit3
deptDisplay: Math
courseDisplay: Calculus I
unitDisplay: Unit 3
---

In this section we will learn how to take derivatives of sine and cosine functions. I will show the derivations of the results, but it is not necessary for you to be able to reproduce these, only to memorize the results. I show the derivations simply for completeness. If you're looking only for reference, I have collected the main results in the following table:

<div class="result">
<b>Derivatives of Trigonometric Functions:</b>
<table style="width:100%">
<tr>
<th>$$\frac{d}{dx}\sin x = \cos x$$</th>
<th>$$\frac{d}{dx}\cos x = -\sin x$$</th> 
</tr>
<tr>
<td>$$\frac{d}{dx}\tan x = \sec^2 x$$ </td>
<td>$$\frac{d}{dx}\cot x = -\csc^2 x$$</td> 
</tr>
<tr>
<td>$$\frac{d}{dx}\sec x = \sec x \tan x$$</td>
<td>$$\frac{d}{dx}\csc x = -\csc x \cot x$$</td> 
</tr>
</table>
</div>

### Derivations
We start with the derivative of the sine function using the definition of the derivative. The rest we can derive using the product and quotient rules. For sine, we will need to compute two preliminary limits. The first is done through a geometric argument. 

$$\lim_{h\to 0}\frac{\sin h}{h}.$$

The next limit we need is 

$$\lim_{h\to 0}\frac{1-\cos h}{h}.$$

This limit is simply computed by multiplying by the conjugate. 

$$\begin{eqnarray*}
\lim_{h\to 0}\frac{1-\cos h}{h} &=& \lim_{h\to 0}\frac{1-\cos h}{h}\frac{1+\cos h}{1 + \cos h} \\
&=&  \lim_{h\to 0}\frac{1-\cos^2 h}{h(1+\cos h)} \\
&=& \lim_{h\to 0}\frac{\sin^2 h}{h(1+\cos h)} \\
&=& \left(\lim_{h\to 0}\frac{\sin h}{h}\right)\left(\lim_{h\to 0}\frac{\sin h}{1+\cos h}\right) \\
&=& 1\cdot \frac{0}{2}\\
&=& 0
\end{eqnarray*}$$

Now, we compute the derivative of $f(x) = \sin x$.

$$\begin{eqnarray*}
\frac{d}{dx}\sin x &=& \lim_{h\to 0} \frac{\sin(x+h) - \sin x}{h} \\
&=& \lim_{h\to 0} \frac{\sin x \cos h + \sin h \cos x - \sin x}{h} \\
&=& \lim_{h\to 0} \frac{\sin x (\cos h -1) + \sin h \cos x }{h} \\
&=& \lim_{h\to 0} \frac{\sin x (\cos h -1)}{h}  +  \lim_{h\to 0}\frac{\sin h \cos x }{h} \\
&=& \sin x\lim_{h\to 0} \frac{\cos h -1}{h}  +  \cos x\lim_{h\to 0}\frac{\sin h}{h} \\
&=& \cos x
\end{eqnarray*}$$

I will not show the process of using the definition of the derivaitve to compute the derivative of $\cos x$, that will be left to the exercises. It is nearly an exact copy of the derivation shown for the derivative of $\sin x$. 

Equipped with the derivatives of $\sin x$ and $\cos x$, it is possible to derive the other results via the quotient rule. 

First, we do the derivative of $\tan$. 

$$\begin{eqnarray*}
\frac{d}{dx}\tan x &=& \frac{d}{dx}\frac{\sin x}{\cos x} \\
&=& \frac{\cos x \cos x - \sin x (-\sin x)}{\cos^2 x}\\
&=& \frac{1}{\cos^2 x}\\
&=& \sec^2 x
\end{eqnarray*}$$

Now, we apply the quotient rule again for $\sec x$, but this time the numerator function is simply 1.

$$\begin{eqnarray*}
\frac{d}{dx}\sec x &=& \frac{d}{dx}\frac{1}{\cos x} \\
&=& \frac{0\cos x - 1(-\sin x)}{\cos^2 x}\\
&=& \frac{1}{\cos x} \frac{\sin x}{\cos x}\\
&=& \sec x \tan x
\end{eqnarray*}$$

The other three derivatives we will leave to the exercises. Note that at the top of this page we have summarized the results just derived as well as the results which I left out. Now, let's proceed with some examples that apply what we have learned so far. 

<div class="examples">


</div>




