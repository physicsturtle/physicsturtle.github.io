---
layout: lesson
title: Least Upper Bound
course: real-analysis-I
unit: unit1
---

Definition: Let $(S,<)$ be an ordered set, let $E\subset S$, and let $E$ be bounded above. If there exists an element $\alpha\in S$ with the following properties:

1. $\alpha$ is an upper bound for $E$
2. If $\gamma\in S$ and $\gamma < \alpha$, then $\gamma$ is not an upper bound for $E$. 

Then we call $\alpha$ the *least upper bound* of $E$, or, the *supremum* of $E$. We write $\alpha = \sup E$. 

Definition: Let $(S,<)$ be an ordered set, let $E\subset S$, and let $E$ be bounded below. If there exists an element $\alpha\in S$ with the following properties:

1. $\alpha$ is a lower bound for $E$
2. If $\gamma\in S$ and $\alpha < \gamma$, then $\gamma$ is not a lower bound for $E$. 

Then we call $\alpha$ the *greatest lower bound* of $E$, or, the *infimum* of $E$. We write $\alpha = \inf E$. 


Definition: An ordered ste $S$ has the least upper bound property if for every $E\subset S$, $E\not= \emptyset$, if $E$ is bounded above, then it has a least upper bound. The least upper bound property is also known as the least upper bound axiom. 

Example: Does $\mathbb{Z}$ has the least upper bound property?
Example: Does $\mathbb{Q}$ have the least upper bound property?



### Exercises
<ol> 
<li><div> The rational numbers $\mathbb{Q}$ can be thought of as ordered pairs, $(m,n)$: $\mathbb{Q} = \left\{(m,n): m\in\mathbb{Z}, n\in\mathbb{N}\right\}$. Define the relation $R$ such that $(m_1,n_1) R (m_2,n_2)$ if $m_1n_2 = m_2n_1$. Show that $R$ is an equivalence relation. </div>

<button onclick="myFunction('answer1')" class="answerButton">Show Answer</button>
<div  id="answer1" class="answer">
Proove thissss
</div> </li>

<li> <div>  Every rational number has a lowest form. In this lowest form, $m$ and $n$ share no common factors, and $n$ is as small as possible. Show that every rational number has a lowest form, and furthermore, that it is unique. </div>

<button onclick="myFunction('answer2')" class="answerButton">Show Answer</button>
<div  id="answer2" class="answer">
Prove thisss
</div> </li>

<li> <div> Prove that there is no rational number whose square is $17$. </div>

<button onclick="myFunction('answer3')" class="answerButton">Show Answer</button>
<div  id="answer3" class="answer">
Prove thiss
</div> </li>

<li> <div> Prove that there is no rational number whose square is $14$. </div>

<button onclick="myFunction('answer4')" class="answerButton">Show Answer</button>
<div  id="answer4" class="answer">
Prove thiss
</div> </li>

<li> <div> Sketch the region where \(xy > 0\) </div>

<button onclick="myFunction('answer5')" class="answerButton">Show Answer</button>
<div  id="answer5" class="answer">
This is a plane that is parallel to the \(xz\) plane. 
</div> </li>
<li> <div> Sketch the set where \(z^2 = 4\) </div>

<button onclick="myFunction('answer6')" class="answerButton">Show Answer</button>
<div  id="answer6" class="answer">
This is a plane that is parallel to the \(xz\) plane. 
</div> </li>
</ol>
