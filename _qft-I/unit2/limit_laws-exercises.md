---
layout: exercises
title: Limit Laws - Exercises
dept: math
course: calculus-I
unit: unit2
deptDisplay: Math
courseDisplay: Calculus I
unitDisplay: Unit 2
---

### Exercises


<ol>
<!--- Exercise 1 --->
<li> <div> Evaluate the limit.   $$\lim_{x \to 4} \frac{x-4}{x^2 - x - 12}$$ </div>
<button onclick="myFunction('answer1')" class="answerButton">Show Answer</button>

<div  id="answer1" class="answer">
$$\begin{eqnarray*}
\lim_{x \to 4} \frac{x-4}{x^2 - x - 12} &=& \lim_{x \to 4} \frac{x-4}{(x-4)(x+3)} \\
&=& \lim_{x \to 4} \frac{1}{x+3} \\
&=& \frac{1}{7}
\end{eqnarray*}$$
</div> </li>


<!--- Exercise 2 --->
<li> <div> Evaluate the limit.  $$\lim_{x \to 3} \frac{x^3 - 27}{x^2-9}$$ </div>

<button onclick="myFunction('answer2')" class="answerButton">Show Answer</button>
<div  id="answer2" class="answer">
$$\begin{eqnarray*}
\lim_{x \to 3} \frac{x^3 - 27}{x^2-9} &=& \lim_{x \to 3} \frac{(x-3)(x^2 + 3x + 9)}{(x-3)(x+3)}\\
&=& \lim _{x \to 3} \frac{x^2+3x+9}{x+3} \\
&=& \frac{27}{6} \\
&=& \frac{9}{2}
\end{eqnarray*}$$
</div> </li>

<!--- Exercise 3 --->
<li> <div> Evaluate the limit.   $$\lim_{x \to 2} \frac{4-x^2}{3-\sqrt{x^2 + 5}}$$ </div>

<button onclick="myFunction('answer3')" class="answerButton">Show Answer</button>
<div  id="answer3" class="answer">
$$\begin{eqnarray*}
\lim_{x \to 2} \frac{4-x^2}{3-\sqrt{x^2 + 5}} &=& \lim_{x \to 2} \frac{(4-x^2)(3+\sqrt{x^2 + 5})}{(3-\sqrt{x^2 + 5})(3+\sqrt{x^2 + 5})} \\
&=& \lim_{x \to 2} \frac{(4-x^2)(3+\sqrt{x^2 + 5})}{9-x^2-5} \\
&=&\lim_{x \to 2} \frac{(4-x^2)(3+\sqrt{x^2 + 5})}{4-x^2}  \\
&=&\lim_{x\to2} (3 + \sqrt{x^2+5} )\\
&=&3+3\\
&=& 6
\end{eqnarray*}$$
</div> </li>


<!--- Exercise 4 --->
<li> <div> Evaluate the limit. $$\lim_{x \to 0} \frac{1}{3 + 2^{1/x}}$$ </div>

<button onclick="myFunction('answer4')" class="answerButton">Show Answer</button>
<div  id="answer4" class="answer">
We will calculate the right hand side and left hand side limits separately. First, the right side limit.
$$\begin{eqnarray*}
\lim_{x \to 0^+} \frac{1}{3+2^{1/x}} &=& \frac{1}{3+2^{+\infty}} \\
&=& \frac{1}{3 +\infty} \\
&=& \frac{1}{\infty} \\
&=& 0
\end{eqnarray*}$$

Now, we do the left limit.
$$\begin{eqnarray*}
\lim_{x \to 0^-} \frac{1}{3+2^{1/x}} &=& \frac{1}{3+2^{-\infty}} \\
&=& \frac{1}{3+0^+} \\
&=& \frac{1}{3}
\end{eqnarray*}$$
</div> </li>

<!--- Exercise 5 --->
<li> <div> Evaluate the limit.  $$\lim_{x \to -1} \frac{x^2 + 3x + 2}{x^2 + 4x + 3}$$ </div>

<button onclick="myFunction('answer5')" class="answerButton">Show Answer</button>
<div  id="answer5" class="answer">
$$\begin{eqnarray*}
\lim_{x \to -1} \frac{x^2 + 3x + 2}{x^2 + 4x + 3} &=& \lim_{x\to -1} \frac{(x+1)(x+2)}{(x+1)(x+3)} \\
&=& \lim_{x \to -1} \frac{x+2}{x+3} \\
&=& \frac{1}{2}
\end{eqnarray*}$$
</div> </li>


<!--- Exercise 6 --->
<li> <div> Evaluate the limit.  $$\lim_{x \to 1} \frac{x-1}{\sqrt{x^2+3} - 2}$$ </div>

<button onclick="myFunction('answer6')" class="answerButton">Show Answer</button>

<div  id="answer6" class="answer">
$$\begin{eqnarray*}
\lim_{x \to 1} \frac{x-1}{\sqrt{x^2+3} - 2} &=&\lim_{x \to 1} \frac{(x-1)(\sqrt{x^2+3} + 2)}{(\sqrt{x^2+3} - 2)(\sqrt{x^2+3} + 2)} \\
&=&\lim_{x \to 1} \frac{(x-1)(\sqrt{x^2+3} + 2)}{x^2+3-4}\\
&=&\lim_{x\to1} \frac{(x-1)(\sqrt{x^2+3} + 2)}{x^2-1}\\
&=&\lim_{x\to1} \frac{(x-1)(\sqrt{x^2+3} + 2)}{(x-1)(x+1)}\\
&=&\lim_{x \to 1} \frac{\sqrt{x^2+3} + 2}{x+1}\\
&=&\frac{2+2}{2}\\
&=&2
\end{eqnarray*}$$
</div> </li>



<!--- Exercise 7 --->
<li> <div> Evaluate the limit.    $$\lim_{x \to 0} \frac{1}{\arctan \left ( \frac{1}{2^x-1} \right )}$$ </div>

<button onclick="myFunction('answer7')" class="answerButton">Show Answer</button>

<div  id="answer7" class="answer">
In this solution we use some unique notation. The $0^+$ means that it is a number very close to zero, but slightly bigger than 0. Similarly with $0^-$ signifying a number very close to zero but slightly smaller than zero. The same applies to where I have $1^+$ and $1^-$ \\
Right Limit:
$$\begin{eqnarray*}
\lim_{x \to 0^+} \frac{1}{\arctan \left ( \frac{1}{2^x-1} \right )} &=& \frac{1}{\arctan \left ( \frac{1}{2^{0^+}-1} \right )} \\
&=&  \frac{1}{\arctan \left ( \frac{1}{1^+-1} \right )} \\
&=&  \frac{1}{\arctan \left ( \frac{1}{0^+} \right )}\\
&=& \frac{1}{\arctan \left ( +\infty \right )}\\
&=& \frac{2}{\pi}
\end{eqnarray*}$$


Left Limit
$$\begin{eqnarray*}
\lim_{x \to 0^-} \frac{1}{\arctan \left ( \frac{1}{2^x-1} \right )} &=& \frac{1}{\arctan \left ( \frac{1}{2^{0^-}-1} \right )} \\
&=& \frac{1}{\arctan \left ( \frac{1}{1^- - 1} \right )}\\
&=&\frac{1}{\arctan \left(\frac{1}{0^-} \right )} \\
&=& \frac{1}{\arctan \left ( -\infty \right )}\\
&=& \frac{-2}{\pi}
\end{eqnarray*}$$
 Since the right and left hand limits are not equal, the limit does not exist. \\

</div> </li>



<!--- Exercise 8 --->
<li> <div> Evaluate the limit. $$\lim_{x \to \pi} \frac{|\sin x| + 2\tan x}{\sin x}$$ </div>

<button onclick="myFunction('answer8')" class="answerButton">Show Answer</button>

<div  id="answer8" class="answer">
First we apply the definition of the absolute value to $\sin x$:
\begin{displaymath}
|\sin x| = \left \{
\begin{array}{lr}
 \sin x & , \sin x \geq 0 \\
 -\sin x &, \sin x < 0
 \end{array}
 \right.
 \end{displaymath}
 Left Hand Side Limit: For $x \in (0,\pi), \sin(x) >0 \Rightarrow |\sin x| = \sin x$.


\begin{eqnarray*}
\lim_{x \to \pi^-} \frac{|\sin x| + 2\tan x}{\sin x} &=& \lim_{x \to \pi^-} \frac{\sin x + 2\tan x}{\sin x} \\
&=& \lim_{x \to \pi^-} 1 + 2\sec x \\
&=& 1-2 \\
&=& -1
\end{eqnarray*}

Right Hand Side Limit: For $x \in (\pi, 2\pi), \sin(x) < 0 \Rightarrow |\sin x| = -\sin x$.

\begin{eqnarray*}
\lim_{x \to \pi^+} \frac{|\sin x| + 2\tan x}{\sin x} &=& \lim_{x \to \pi^+} \frac{-\sin x + 2\tan x}{\sin x}\\
 &=& \lim_{x \to \pi^+} -1 + 2\sec x \\
 &=& -1-2 \\
 &=& -3
\end{eqnarray*}
The left and right hand side limits do not match, therefore we conclude that the limit \textit{does not exist}.

</div> </li>



<!--- Exercise 9 --->
<li> <div> Compute the limit $$\lim_{x\to\infty} x\left(\sqrt{x+2} - \sqrt{x}\right)$$ </div>

<button onclick="myFunction('answer9')" class="answerButton">Show Answer</button>

<div  id="answer9" class="answer">
\begin{eqnarray*}
\lim_{x\to\infty} x\cdot({\sqrt{x+2}-\sqrt{x}}) &=& \lim_{x\to\infty}x\cdot({\sqrt{x+2}-\sqrt{x}})\cdot \frac{\sqrt{x+2}+\sqrt{x}}{\sqrt{x+2}+\sqrt{x}} \\
&=& \lim_{x\to\infty}x\cdot \frac{x+2 - x}{\sqrt{x+2} + \sqrt{x}}\\
&=& \lim_{x\to\infty} \frac{2x}{\sqrt{x+2} + \sqrt{x}}\\
&=& \lim_{x\to\infty} \frac{2\sqrt{x}}{\sqrt{1 + \frac{2}{x}} + 1}\\
&=& \frac{\infty}{2}
\end{eqnarray*}
Thus the limit diverges to $+\infty$.
</div> </li>







<li> <div> Evaluate the limit: $$\lim_{x\to 1}\frac{\sqrt[3]{x} - 1}{x-1}$$ </div>

<button onclick="myFunction('answer10')" class="answerButton">Show Answer</button>

<div  id="answer10" class="answer">
\begin{solution}[70 mm]
The well known formula
$$(a^3 - b^3) = (a-b)(a^2 + ab + b^2)$$
can be applied here:
$$\begin{eqnarray*}
\lim_{x\to 1}\frac{\sqrt[3]{x} - 1}{x-1} &=& \lim_{x\to1} \frac{\sqrt[3]{x} - 1}{(\sqrt[3]{x} - 1)(\sqrt[3]{x^2} + \sqrt[3]{x} + 1)}\\
&=& \lim_{x\to 1}\frac{1}{\sqrt[3]{x^2} + \sqrt[3]{x} + 1}\\
&=& \frac{1}{1+1+1}\\
&=& \frac{1}{3}
\end{eqnarray*}$$
\end{solution}
</div>
</li>



</ol>









