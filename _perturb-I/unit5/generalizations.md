---
layout: lesson
title: Generalizations
dept: math
course: asymptotics
unit: unit5
deptDisplay: Math
courseDisplay: Asymptotics
unitDisplay: Unit 5
---

### Introduction

In this section, we will introduce some problems which can be reduced to a form to which WKB can be applied. 

What happens if we have the equation

$$y'' + p(x)y' + q(x)y = 0$$

We want to get rid of the $py'$ term. To do this, we let $y = Au$. Plugging this expression into the main differential equation gives us 

$$A'' u + 2A'u' + Au'' + pA'u + pAu' + qAu = 0$$

If we set the coefficient of $u'$ to be zero, we get 

$$2A' + pA = 0$$

This gives us that 

$$A = \exp\left(-\int\frac{p}{2} dx\right),$$

and we have the equation 

$$u'' + \left(q + \frac{A''}{A} + p\frac{A'}{A}\right)u = 0$$

We can apply WKB to this equation. 
