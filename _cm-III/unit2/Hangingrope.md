---
layout: lesson
title: Hanging rope 
dept: physics
course: cm-III
unit: unit2
deptDisplay: Physics
courseDisplay: Classical Mechanics III
unitDisplay: Unit 2
---

Today, we will analyze the famous problem of what shape a rope of uniform mass density takes if it is hung between two points. The problem is illustrated below

(insert picture here)

Here, we will solve the problem by using a minimization of the overall potential energy of the rope. The first step is to construct the potential energy. We start by considering the potential energy \\(dV\\) of a small mass \\(dm\\) of the rope. Suppose the rope has shape \\(y = y(x)\\), with boundary conditions \\(y(0) = h_1\\) and \\(y(L) = h_2\\). A small mass \\(\d m\\) has length \\(\d s = \sqrt{1 + (y')^2} \d x\\), and thus mass \\(\d m = \mu \d s\\), where \\(\mu\\) is the linear mass density of the rope, measured in kg/m. Thus, the potential energy of this small piece of mass is \\(\d V = gy \d m\\). Integrating this potential energy over the entire rope, we get the potential energy functional:

$$V[y] = g\mu \int_0^L y\sqrt{1+(y')^2} \d x.$$

Defining the Lagrangian \\(\mathcal{L} = y\sqrt{1+(y')^2}\\) (we ignore the constants) If we plug this into the Euler-Lagrange equation

$$\frac{\d}{\d x}\left(\frac{\partial\mathcal{L}}{\partial y'}\right) = \frac{\partial\mathcal{L}}{\partial y},$$

we get the differential equation 

$$ \frac{d}{\d x}\left(\frac{yy'}{\sqrt{1+(y')^2}}\right) = \sqrt{1+(y')^2} $$

If we expand out all the terms, then we get 

$$\frac{(y')^2}{\sqrt{1+(y')^2}} +  \frac{yy"}{\sqrt{1+(y')^2}} - \frac{y(y')^2y"}{(1+(y')^2)^{3/2}}= \sqrt{1+(y')^2}$$

If we simplify the terms and cancel, then we get 

$$\frac{yy"}{1+(y')^2} = 1$$

There are multiple ways to solve this differential equation. Here, I will show only one. If, in general, we have a (linear or nonlinear) differential equation where there is no appearance of the independent variable \\(x\\), then we can make a substitution \\(y' = v(y)\\). This means that 

$$y" = \frac{\d y'}{\d x} = \frac{\d v}{\d y}\frac{\d y}{\d x} = v' y' = v'v$$

so we have defined a function \\(v\\) whose independent variable is \\(y\\). Thus the differential equation becomes 

$$\frac{vv'y}{1+v^2} = 1$$

This equation is separable, so it can be written as 

$$\frac{v\d v}{1+v^2} = \frac{1}{y} \d y$$

If we integrate both sides, 

$$\frac{1}{2}\log(1+v^2) = \log y + C$$

Exponentiating both sides, we can substitute in our definition of \\(v\\):

$$\sqrt{1+v^2} = c_1 y = \sqrt{1+(y')^2}.$$

Next, we can separate variables again:

$$\int \frac{\d y}{\sqrt{c_1^2 y^2 - 1}} = \int \d x$$

Making the substitution \\(c_1y = \cosh \theta\\), \\(\d y = \frac{1}{c_1}\sinh\theta\\) allows us to evaluate the integral quickly:

$$\arccosh(c_1 y)= c_1x + c_2$$

Isolating for \\(y\\), we get 

$$y = \frac{1}{c_1}\cosh(c_1 x + c_2)$$

Now we can plug in our boundary conditions, \\(y(0) = h_1\\) and \\(y(L) = h_2\\). This gives us 

$$h_1 = \frac{1}{c_1}\cosh(c_2), \qquad h_2 = \frac{1}{c_1}\cosh(c_1 L + c_2)$$

This system of equations, in general, needs to be solved numerically. 

