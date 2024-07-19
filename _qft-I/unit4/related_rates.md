---
layout: lesson
title: Related Rates
dept: math
course: calculus-I
unit: unit4
deptDisplay: Math
courseDisplay: Calculus I
unitDisplay: Unit 4
---

In this section, we will apply the chain rule to a class of practical problems which come up all the time in geometry, physics, and more. In words, the chain rule can be described as relating rates of change of interdependent variables. Related rates problems are best illustrated with an example. 

<div class="example">
<p><b>Example:</b> Suppose we have a circle whose radius is increasing at a rate of 1 cm per second. How fast is its area increasing when its radius is 20 cm? </p>
<b>Solution:</b> The area of a circle is related to its radius by $A = \pi r^2$. Differentiating both sides of this equation with respect to time, keeping in mind that $r$ is a function of $t$, gives 
$$\frac{dA}{dt} = 2\pi r\frac{dr}{dt}.$$

We thus plug in $dr/dt = 1$ cm/s and $r = 20$ cm to get $dA/dt = 40\pi\,\text{cm}^2$. Thus, the area is increasing at a rate of $40\pi\,\text{cm}^2$. 
</div> <br>

One sees that, in this example, we have related the rate of change of the area of the circle to the rate of change of its radius. Furthermore, this rate of change of area depends on the radius of the circle at the moment we check what its rate of change of area is. That is why we needed to specify a value of $r$. Let's continue with another example. 

<div class="example">
<p><b>Example:</b> Suppose we have a particle moving along the curve $y = x^{3/2}$. Its $x$ coordinate increases with constant speed 2 units per second. 
<ol>
<li> How fast is its $y$ coordinate increasing when it is at $(x,y) = (4,8)$? </li>
<li> How fast is its distance to the origin increasing when it is at $(x,y) = (4,8)$? </li>
</ol> </p>

<b>Solution:</b> The distance to the origin is 

</div>
