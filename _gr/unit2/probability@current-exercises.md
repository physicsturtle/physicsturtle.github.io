---
layout: lesson
title: Probability Current
course: quantum-mechanics-I
unit: unit1
---


Exercise: For the three dimensional probability current, show that $$\nabla\cdot J +\frac{\partial\rho}{\partial t} = 0,$$ where $\rho = \|\psi\|^2$. 

Solution: The divergence of the probability current is 

$$\begin{eqnarray*}
\nabla\cdot\textbf{J} &=& \frac{\hbar}{2mi}\nabla\cdot \left(\psi^*\nabla \psi - \psi\nabla\psi^*\right) \\
&=&  \frac{\hbar}{2mi}\left( \psi^*\nabla^2 \psi + \nabla\psi \cdot \nabla\psi^* - \nabla \psi\nabla\psi^* - \psi^*\nabla^2\psi\right) \\
&=& \frac{\hbar}{2mi}\left(\psi^*\nabla^2 \psi - \psi\nabla^2\psi^*\right) 
\end{eqnarray*}$$

The time derivative of the density $\rho$ is most easily found by writing is as $\rho = \psi^*\psi$. We then get 

$$\frac{\partial\rho}{\partial t} = \frac{\partial\psi}{\partial t}\psi^* + \psi\frac{\partial\psi^*}{\partial t}$$

We can now substitute in from the Schrödinger equation that 

$$i\hbar\frac{\partial\psi}{\partial t} = -\frac{\hbar^2}{2m}\nabla^2\psi + V\psi.$$

If we divide through by $i\hbar$ to isolate the time derivative, when we plug in we get 

$$\begin{eqnarray*}
\frac{\partial\rho}{\partial t} &=& \left[\frac{\hbar i}{2m}\nabla^2\psi - \frac{iV\psi}{\hbar}\right]\psi^* + \left[\frac{\hbar i}{2m}\nabla^2\psi - \frac{iV\psi}{\hbar}\right]^*\psi\\
&=&  \left[\frac{\hbar i}{2m}\nabla^2\psi - \frac{iV\psi}{\hbar}\right]\psi^* - \left[\frac{\hbar i}{2m}\nabla^2\psi - \frac{iV\psi}{\hbar}\right]\psi\\
&=& \left[\frac{\hbar i}{2m}\nabla^2\psi\right]\psi^* - \left[\frac{\hbar i}{2m}\nabla^2\psi\right]\psi\\
&=&  -\frac{\hbar}{2mi}\left[\psi^* \nabla^2\psi -\psi \nabla^2\psi\right]\\
\end{eqnarray*}$$

so we immediately recognize that 

$$\nabla\cdot\textbf{J} + \frac{\partial\rho}{\partial t} = 0$$

