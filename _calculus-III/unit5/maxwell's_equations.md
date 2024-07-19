---
layout: lesson
title: Maxwell's Equations*
dept: math
course: calculus-III
unit: unit5
deptDisplay: Math
courseDisplay: Calculus III
unitDisplay: Unit 5
---

In this section, we will have a brief discussion of Maxwell's equations of electromagnetism. By this time, you are completely equipped to work with these equations in their full vector-calculus formulation. This is an essential skill for working through any course in electromagnetism, as well as any third year or beyond physics course. What we will do in this section is describe the relationship between the differential and integral forms of Maxwell's equations, as well as go through a short derivation for Maxwell's wave-equation in vacuum -- thus proving that light is an electromagnetic wave. 

Maxwell's equations in differential form are

$$\begin{eqnarray}
\nabla\cdot\textbf{E} &=& \frac{\rho}{\epsilon_0},\quad\text{(Gauss's Law for Electric FIelds)}\\
\nabla\cdot\textbf{B} &=& 0 \quad \text{(Gauss's Law for Magnetic Fields)}\\
\nabla\times\textbf{E} &=& -\frac{\partial\textbf{B}}{\partial t} \quad \text{(Faraday's Law)}\\
\nabla\times\textbf{B} &=& \mu_0\textbf{J} + \mu_0\epsilon_0 \frac{\partial\textbf{E}}{\partial t},\quad \text{(Ampere's Law)}
\end{eqnarray}$$

#### Gauss's Law for Electric Fields
Let's begin with Gauss's Law for Electric Fields. Taking the volume integral of both sides for an arbitrary volume $V$ enclosed by surface $S$, we get 

$$\begin{eqnarray}
\iiint_V \nabla\cdot\textbf{E} dV &=& \iiint_V \frac{\rho}{\epsilon_0} dV\\
\iint_{S} \textbf{E} \cdot d\textbf{S} &=& \frac{1}{\epsilon_0} \iiint_V \rho dV\\
\Phi_E&=& \frac{Q}{\epsilon_0}
\end{eqnarray}$$

which shows that the electric flux through a surface is proportional to the charge enclosed by the surface. 

#### Gauss's Law for Magnetic Fields
Gauss's Law for Magnetic Fields is easier than the previous:

$$\begin{eqnarray}
\iiint_V \nabla\cdot\textbf{E} dV &=& \iiint_V 0 dV\\
\iint_{S} \textbf{E} \cdot d\textbf{S} &=& 0\\
\Phi_B&=& 0
\end{eqnarray}$$

which says that the net magnetic flux through any closed surface is zero. 

#### Faraday's Law 
For Faraday's law, we instead take a surface integral over an *open* surface $S$, which has boundary $C$. $C$ is a closed curve. 

$$\begin{eqnarray}
\iint_S \nabla\times\textbf{E} \cdot d\textbf{S} &=& \iint_S -\frac{\partial\textbf{B}}{\partial t} \cdot d\textbf{S}\\
\int_C \textbf{E} \cdot d\textbf{r} &=& -\frac{\partial}{\partial t}\iint_S \textbf{B} \cdot d\textbf{S}\\
\mathcal{E} &=& -\frac{\partial\Phi_B}{\partial t}\\
\end{eqnarray}.$$

#### Ampère's Law
Finally we move on to Ampère's Law. Again, we take the integral over an open surface $S$ with closed loop boundary $C$. 

$$\begin{eqnarray}
\iint_S \nabla\times\textbf{B} \cdot d\textbf{S} &=& \iint_S \left(\mu_0\textbf{J} + \mu_0\epsilon_0 \frac{\partial\textbf{E}}{\partial t} \right)\cdot d\textbf{S}\\
\int_C \textbf{B} \cdot d\textbf{r} &=& \mu_0 \iint_S \textbf{J} \cdot d\textbf{S}+ \mu_0\epsilon_0 \frac{\partial}{\partial t}\iint_S \textbf{E}\cdot d\textbf{S}\\
\int_C \textbf{B} \cdot d\textbf{r} &=& \mu_0 I+ \mu_0\epsilon_0 \frac{\partial \Phi_E}{\partial t}\\
\end{eqnarray}$$

### The Wave Equation
Now we will show how Maxwell's equations in a vacuum imply that light is an electromagnetic wave. In a vacuum, Maxwell's equations reduce to a simpler form, because there is no charge density in a vacuum $\rho = 0$, and no current in a vacuum $\textbf{J} = 0$. Thus Maxwell's equations in vacuum take the form 

$$\begin{eqnarray}
\nabla\cdot\textbf{E} &=& 0\\
\nabla\cdot\textbf{B} &=& 0\\
\nabla\times\textbf{E} &=& -\frac{\partial\textbf{B}}{\partial t} \\
\nabla\times\textbf{B} &=& \mu_0\epsilon_0 \frac{\partial\textbf{E}}{\partial t}
\end{eqnarray}$$

The only other thing we need before starting is that $\mu_0\epsilon_0 = 1/c^2$. Now we start by taking the curl of both sides of Faraday's law. 

$$\begin{eqnarray}
\nabla\times\nabla\times\textbf{E} &=& \nabla\times\left(-\frac{\partial\textbf{B}}{\partial t} \right)\\
\nabla(\nabla\cdot\textbf{E}) - \nabla^2\textbf{E} &=& -\frac{\partial}{\partial t}\nabla\times\textbf{B}\\
\nabla(0) - \nabla^2\textbf{E} &=& -\frac{\partial}{\partial t}\mu_0\epsilon_0\frac{\partial\textbf{E}}{\partial t}\\
- \nabla^2\textbf{E} &=& -\frac{1}{c^2}\frac{\partial}{\partial t}\frac{\partial\textbf{E}}{\partial t}\\
\nabla^2\textbf{E} &=& \frac{1}{c^2}\frac{\partial^2\textbf{E}}{\partial t^2}\\
\end{eqnarray}$$

which is the wave equation, with waves travelling at speed $c$. This shows that light is a wave of an oscillating *electric field*. It can also be shown that the same equation must hold for the magnetic field. 

### Exercises

<ol>
<li> <div> Show that $$\nabla\cdot \textbf{J} + \frac{\partial \rho}{\partial t} = 0$$ must hold, given Maxwell's Equations.</div>

<button onclick="myFunction('answer1')" class="answerButton">Show Answer</button>
<div  id="answer1" class="answer">
First, we take the divergence of Ampère's law. 
$$\begin{eqnarray}
\nabla\cdot \nabla\times\textbf{B} &=&\nabla\cdot  \mu_0\textbf{J} + \nabla\cdot \mu_0\epsilon_0 \frac{\partial\textbf{E}}{\partial t} \\
0 &=& \mu_0\nabla\cdot\textbf{J} +  \mu_0\epsilon_0 \frac{\partial}{\partial t}\nabla\cdot\textbf{E}\\
0 &=& \nabla\cdot\textbf{J} +  \epsilon_0 \frac{\partial}{\partial t}\frac{\rho}{\epsilon_0}\\
0 &=& \nabla\cdot\textbf{J} + \frac{\partial \rho}{\partial t}\\
\end{eqnarray}$$

This is the law of the conservation of charge. 
</div> </li>

<li> <div> Show that $$\frac{1}{c^2}\frac{\partial ^2\textbf{B}}{\partial t^2} = \nabla^2\textbf{B}$$ in a vacuum. </div>

<button onclick="myFunction('answer2')" class="answerButton">Show Answer</button>
<div  id="answer2" class="answer">
Instead of taking the curl of both sides of Faraday's Law, let's take the curl of both sides of Ampère's law. 
$$\begin{eqnarray}
\nabla\times\nabla\times\textbf{B} &=& \mu_0\epsilon_0\nabla\times\left(\frac{\partial\textbf{E}}{\partial t} \right)\\
\nabla(\nabla\cdot\textbf{B}) - \nabla^2\textbf{B} &=& \mu_0\epsilon_0\frac{\partial}{\partial t}\nabla\times\textbf{E}\\
\nabla(0) - \nabla^2\textbf{B} &=& \frac{1}{c^2}\frac{\partial}{\partial t}\left(-\frac{\partial\textbf{B}}{\partial t}\right)\\
- \nabla^2\textbf{B} &=& - \frac{1}{c^2}\frac{\partial^2\textbf{B}}{\partial t^2}\\
\nabla^2\textbf{B} &=& \frac{1}{c^2}\frac{\partial^2\textbf{B}}{\partial t^2}\\
\end{eqnarray}$$
</div> </li>
</ol>
