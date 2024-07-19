---
layout: lesson
title: Newton's Law of Cooling
dept: math
course: calculus-I
unit: unit4
deptDisplay: Math
courseDisplay: Calculus I
unitDisplay: Unit 4
---

### Introduction
Newton's law of cooling captures one of the three modes of heat transfer, convection, and we will apply it here to solve problems of cooling and heating. We consider an object of a certain temperature $T$ placed in a room of ambient temperature $T_a$. If $T_a > T$, then we expect that the object will start to heat up, and if $T_a < T$ we expect that the object will start to cool down. The goal is then to find the temperature $T$ of the object as a function of time $t$. 

In convective heat transfer, the rate at which the temperature of the object changes, $dT/dt$, is proportional to the difference between the temperature of the object and the room. This is captured in the following equation:

$$\frac{dT}{dt} = k(T_a - T)$$

where we expect that $k$ is a positive constant. This makes sense because if $T_a > T$ (or, equivalently, $T_a - T >  0$), then we want that $dT/dt >0$ (the object heats up), and if $T_a < T$ (or, equivalently, $T_a - T < 0$), then we want that $dT/dt < 0$ (the object cools down). What we have here is an *ordinary differential equation*. An ordinary differential equation is an equation which relates a function (in our case $T(t)$) to its own derivative (in our case $dT/dt$). To complete the problem that we want to solve, we need an *initial condition*, or, the temperature of the object at $t = 0$. This makes an *initial value problem*, which consists of an ordinary differential equation together with an initial condition. The initial value problem (IVP) that we want to solve is thus the following:

$$\begin{cases}
\frac{dT}{dt} = k(T_a - T) \\
T(0) = T_0 \end{cases}$$

### Solving the Model
Our goal now is to solve the problem that we just formulated. To do this, we will recall what we learned in the previous section on exponential growth and decay. The first step is to make the substitution $z = T_a - T$. Thus, $z$ is a function of time because $T$ is a function of time. If we differentiate both sides, we get that $dz/dt = -dT/dt$. The equation therefore becomes (ignoring the initial condition for now)

$$-\frac{dz}{dt} = kz$$

The solution to this, which we established in the exponential growth/decay section was 

$$z(t) = Ae^{-kt},$$

where $A$ is a constant that depends on the initial condition. If we recall that $z = T_a - T$, then we can find $T$ as a function of time. This gives us 

$$T(t) = T_a - Ae^{-kt}.$$

Finally, we plug in the initial condition $T(0) = T_0$. If we do this, then we find that 

$$T_0 = T_a - A$$

which gives us that $A = T_a - T_0$. Thus, the full solution is

$$T(t) = T_a(1-e^{-kt}) + T_0e^{-kt}.$$

### Examples
<div class="example">
<p><b>Example:</b> Suppose we have a fresh loaf of bread at a temperature of 180${}^\circ$C. It is then placed on a cooling rack in a room of temperature 25${}^\circ$C. If $k = 2/\text{min}$, then how long does the bread take to reach 50${}^\circ$? </p>
<b>Solution:</b> asdf
</div>

<div class="example">
<p><b>Example:</b> Suppose we have a hot cup of coffee at temperature 90${}^\circ$ 
</p>
</div>


### Summary: 
Here I will summarize how to solve Newton's law of cooling. One could of course just remember the final formula, but it can be difficult to remember. It may be easier to remember the derivation of the final formula instead. I certainly recommend learning the derivation because understanding this model is a useful skill that will come up many times in physics or math in the future. 
1. Given Newton's Law of cooling 














