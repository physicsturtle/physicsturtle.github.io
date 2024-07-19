---
layout: lesson
title: Riemann Tensor
dept: math
unit: unit7
course: math-methods
deptDisplay: Math
unitDisplay: Unit 7
courseDisplay: Mathematical Methods in Physics
---



<div class="definition">
The <i>Riemann tensor</i> $R$ is the $(1,3)$ tensor field defined by 
$$R(\omega,X,Y,Z) = \omega(\nabla_X \nabla_Y Z - \nabla_Y \nabla_X Z - \nabla_{[X,Y]}Z)$$
</div>

The components of the Riemann tensor with respect to a chart $(U,x)$ can be found by plugging in the basis. They are

$$\begin{align*}
R\left(dx^i, \frac{\partial}{\partial x^j},\frac{\partial}{\partial x^k},\frac{\partial}{\partial x^\ell}\right) =&
dx^i\left(\nabla_{\frac{\partial}{\partial x^j}} \nabla_{\frac{\partial}{\partial x^k}}  \frac{\partial}{\partial x^\ell} - \nabla_{\frac{\partial}{\partial x^k}}  \nabla_{\frac{\partial}{\partial x^j}}  \frac{\partial}{\partial x^\ell} - \nabla_{[\frac{\partial}{\partial x^j},\frac{\partial}{\partial x^k}]}\frac{\partial}{\partial x^\ell}\right)\\
=& dx^i\left[\nabla_{\frac{\partial}{\partial x^j}}\left(\Gamma^m_{k\ell}\frac{\partial}{\partial x^m}\right) - \nabla_{\frac{\partial}{\partial x^k}} \left(\Gamma^m_{j\ell}\frac{\partial}{\partial x^m}\right) - \nabla_{0}\frac{\partial}{\partial x^\ell} \right]\\
=& dx^i\left[\frac{\partial\Gamma^m_{k\ell}}{\partial x^j}\frac{\partial}{\partial x^m} + \Gamma^m_{k\ell}\Gamma^n_{jm}\frac{\partial}{\partial x^n} - \frac{\partial \Gamma^m_{j\ell}}{\partial x^k}\frac{\partial}{\partial x^m} - \Gamma^m_{j\ell}\Gamma^n_{km}\frac{\partial}{\partial x^n}\right]\\
=& \frac{\partial\Gamma^m_{k\ell}}{\partial x^j}\delta^i_m + \Gamma^m_{k\ell}\Gamma^n_{jm}\delta^i_n - \frac{\partial \Gamma^m_{j\ell}}{\partial x^k}\delta^i_m - \Gamma^m_{j\ell}\Gamma^n_{km}\delta^i_n\\
=& \frac{\partial\Gamma^i_{k\ell}}{\partial x^j} + \Gamma^m_{k\ell}\Gamma^i_{jm}- \frac{\partial \Gamma^i_{j\ell}}{\partial x^k} - \Gamma^m_{j\ell}\Gamma^i_{km}\\
\end{align*}$$


<div class="result">
The components of the Riemann tensor in a chart $(U,x)$ are 
$$R^i_{jk\ell} = \frac{\partial\Gamma^i_{k\ell}}{\partial x^j} -\frac{\partial \Gamma^i_{j\ell}}{\partial x^k} + \Gamma^m_{k\ell}\Gamma^i_{jm} - \Gamma^m_{j\ell}\Gamma^i_{km}$$
</div>











































