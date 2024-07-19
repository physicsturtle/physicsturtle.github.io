---
layout: lesson
title: Functions 
dept: math
course: calculus-I
unit: unit1
deptDisplay: Math
courseDisplay: Calculus I
unitDisplay: Unit 1
---
### Introduction


In high school, we learn what functions are, but many people forget the formal definition by the time they reach university. In this lesson, we will review this definition, as well as the definitions of domain, range, and function notation. Additionally, we will introduce some definitions which are likely new to you, such as the codomain, image, and preimage. These terms will not be used too frequently in this course, but are useful to know especially if you take further math courses in the future.

### Definitions


<div class="definition">
<b>Definition:</b>
Let \(A\) and \(B\) be sets. We say \(f\) is a <i>function from \(A\) to \(B\)</i> if to each element \(x\) of \(A\), there corresponds one and only one element \(f(x)\) of \(B\). This is written as \(f : A\to B\). 

</div>

This can be represented schematically by the following Figure 

<figure class="center">
<p><img src="figures/function.pdf" alt="Function" class="center" style="width:360.0px;height:250.0px;"> </p><figcaption class="center">A function \(f : A \to B\)</figcaption>
</figure>

We call \\(A\\) the domain of the function \\(f\\), and \\(B\\) the codomain. It is possible that not every element of \\(B\\) is reached by the function \\(f\\). For example, if we define \\(f : \RR\to\RR\\) by \\(f(x) = x^2\\), then, although the codomain is \\(\RR\\), we never actually reach the negative numbers. This leads us to the following definition.

<div class="definition">
<b>Definition:</b>
Let \(f:A\to B\) be a function. We define the <i>range</i> of \(f\) to be 
\(\)\text{range}(f) = \{f(x) \| x\in A\}.\(\)

</div>

Closely related to the definition of range are the definitions of image and preimage. 

<div class="definition">
<b>Definition:</b>
Suppose we have a function \(f:A\to B\), and that \(U\) is a subset of \(A\). Then, we define 
$$\begin{equation}
f(U) = \{f(x)\in B \| x\in U\|\}
\end{equation}$$
as the <i>image of \(U\) under \(f\)</i>.

</div>

<div class="definition">
<b>Definition:</b> 
Suppose we have a function \(f:A\to B\), and that \(V\) is a subset of \(B\). Then, we define 
$$\begin{equation}
f^{-1}(V) = \{x\in A \| f(x)\in V\|\}
\end{equation}$$
as the <i>preimage of \(V\) under \(f\)</i>.

</div>

### Examples


<div class="example">
<b>Example:</b>
Consider \(f : [2,4] \to \RR\), where \(f(x) = x^2\). 
<ol type="a">
<li> What is the domain of \(f\)? 
</li>
<li> What is the codomain of \(f\)? 
</li>
<li> What is the range of \(f\)? 
</li></ol>

<b>Solution:</b>
<ol type="a">
<li> The domain of \(f\) is \([2,4]\). 
</li>
<li> The codomain of \(f\) is \(\RR\).
</li>
<li> The range of \(f\) is \([2^2,4^2] = [4,16]\).
</li></ol>

</div>

<div class="example">
<b>Example:</b>Consider the function \\(f : \RR\to\RR\\), where \\(f(x) = x^2\\). Find the following sets.
<ol type="a">
<li> \(f([-1,1])\) 
</li>
<li> \(f([0,1])\) 
</li>
<li> \(f((0,\infty))\)
</li>
<li> \(f^{-1}([0,1])\) 
</li>
<li> \(f^{-1}((0,1])\) 
</li>
<li> \(f^{-1}([-2,-1])\) 
</li>
<li> \(f^{-1}([-1,1])\) 
</li></ol>

<b>Solution:</b>
<ol type="a">
<li> \(f([-1,1]) = [0,1]\)
</li>
<li> \(f([0,1]) = [0,1]\) 
</li>
<li> \(f((0,\infty)) = (0,\infty)\)
</li>
<li> \(f^{-1}([0,1]) = [-1,1]\)
</li>
<li> \(f^{-1}((0,1]) = [-1,0) \cup (0,1]\)
</li>
<li> \(f^{-1}([-2,-1]) = \emptyset\)
</li>
<li> \(f^{-1}([-1,1]) = [0,1]\)
</li></ol>

</div>


