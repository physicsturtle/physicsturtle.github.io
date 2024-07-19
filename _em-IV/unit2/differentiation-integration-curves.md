---
layout: lesson
title: DIFFERENTIATION AND INTEGRATION OF CURVES
course: calculus-III
unit: unit2
lessonID: differentiation-integration-curves
nextID: arc-length
---

- Componentwise integration -- initial and final points

We now want to discuss how to differentiate vector valued functions. The definition of differentiation of vector valued functions is identical to the definition for a single variable. 

\\[ \textbf{r}'(t) = \lim_{h\to 0}\frac{\textbf{r}(t+h) - \textbf{r}(t)}{h}\\]

It can be shown that this derivative exists if and only if all of the *components* of $$\textbf{r}$$ have derivatives at \\(x(t)\\)

<button onclick="myFunction('answer')" class="answerButton">Show Proof</button>

<div  id="answer" class="answer">
The limit exists if and only if for every \(\epsilon>0\) there exists \(\delta > 0\) for which \(\|\textbf{r}\| \)
</div>


This is done in the obvious way; that is, if \\(\textbf{r}(t) = (x(t),y(t),z(t))\\), we define the componentwise differentiation

$$ \frac{d\textbf{r}}{dt} = \left(\frac{dx}{dt},\frac{dy}{dt},\frac{dz}{dt}\right).$$

Geometrically, \\(\textbf{r}'(t)\\) represents the *tangent* vector to the curve at the point \\(\textbf{r}(t)\\). We then define the *unit tangent vector* as 

$$\hat{\textbf{T}} = \frac{\textbf{r}'(t)}{|\textbf{r}'(t)|}$$

which encodes only the direction of the tangent vector. 

Higher derivatives can be similarly calculated. We will discuss the geometric interpretations of higher derivatives in the following section.

### Integration
Integration for curve is defined componentwise. This is identical to how differentiation is defined. In symbols, 

$$\int_a^b \textbf{r}(t) dt = \left(\int_a^b x(t) dt, \int_a^b y(t) dt,\int_a^b z(t) dt\right)$$


### Exercises

<ol>
<li> <div> Sketch all of the points such that \(y = 1\). </div>

<button onclick="myFunction('answer2')" class="answerButton">Show Answer</button>
<div  id="answer2" class="answer">
This is a plane that is parallel to the \(xz\) plane. 
</div> </li>
<li> <div> Sketch all of the points such that \(y = 1\). </div>

<button onclick="myFunction('answer2')" class="answerButton">Show Answer</button>
<div  id="answer2" class="answer">
This is a plane that is parallel to the \(xz\) plane. 
</div> </li>
</ol>
