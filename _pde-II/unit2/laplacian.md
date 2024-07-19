---
layout: lesson
title: Eigenfunctions of the Laplacian
dept: math
course: pde-II
unit: unit2
deptDisplay: Math
courseDisplay: Partial Differential Equations II
unitDisplay: Unit 2
---

### Introduction

In this section, we will find the eigenfunctions of the Laplacian for the case of spherical symmetry. This includes spherically symmetric boundary conditions. In considering spherical symmetry, we can split the equation into an angular and a radial part. The radial part will be solved only after boundary conditions are applied, but the angular part can be solved regardless of what the boundary condition is (assuming it obeys spherical symmetry). In three dimensions, the Laplacian in spherical coordinates is 

$$\nabla^2 u = \frac{1}{r^2}\frac{\partial}{\partial r}\left(r^2\frac{\partial u}{\partial r}\right) + \frac{1}{r^2\sin\theta}\frac{\partial}{\partial\theta}\left(\sin\theta\frac{\partial u}{\partial\theta}\right) + \frac{1}{r^2\sin^2\theta}\frac{\partial^2 u}{\partial\varphi^2}$$

where $\theta$ is the polar coordinate and $\varphi$ is the azimuthal coordinate. Our goal is to understand the eigenvalue problem 

$$\nabla^2 u = -\lambda^2 u.$$

### Separation of Variables

If we separate variables by writing the solution as a product of two functions $R(r)$ and $Y(\theta,\varphi)$

$$u(r,\theta,\varphi) = R(r)Y(\theta,\varphi)$$

then the equation can be separated by first substituting in for $u$, then dividing both sides by $u$:

$$\left[\frac{1}{R}\frac{\partial}{\partial r}\left( r^2 \frac{\partial R}{\partial r}\right) + \lambda^2 r^2\right] + \frac{1}{Y}\left(\frac{1}{\sin\theta}\frac{\partial}{\partial\theta}\left(\sin\theta\frac{\partial Y}{\partial\theta}\right) + \frac{1}{\sin^2\theta}\frac{\partial^2 Y}{\partial\varphi^2}\right) = 0$$

We let the separation constant be $-\ell(\ell+1)$, which gives us 

$$\frac{1}{Y}\left(\frac{1}{\sin\theta}\frac{\partial}{\partial\theta}\left(\sin\theta\frac{\partial Y}{\partial\theta}\right) + \frac{1}{\sin^2\theta}\frac{\partial^2 Y}{\partial\varphi^2}\right) = -\ell(\ell+1).$$

If we multiply both sides by $Y$, it becomes clear that we have an eigenvalue problem again! 

$$\frac{1}{\sin\theta}\frac{\partial}{\partial\theta}\left(\sin\theta\frac{\partial Y}{\partial\theta}\right) + \frac{1}{\sin^2\theta}\frac{\partial^2 Y}{\partial\varphi^2} = -\ell(\ell+1)Y.$$

Note that by making this choice of separation constant, we are restricting the eigenvalue of this angular Laplacian to be at most $1/4$, which occurs for the value of $\ell = -1/2$. Any other value of $\ell$ will cause the quantity $-\ell(\ell+1)$ to be more negative. This might seem as though we are sacrificing some generality! In fact, I leave it to you to consider a general eigenvalue instead of the special form $-\ell(\ell+1)$. As you will see later in the calculation, this eigenvalue will end up having to be less than $1/4$.

Now with the angular Laplacian eigenvalue problem, we separate variables again by writing $Y(\theta,\varphi) = P(\theta)\Phi(\varphi)$. This gives us the separated equation

$$\frac{1}{P}\left[\sin\theta\frac{\partial}{\partial\theta}\left(\sin\theta\frac{\partial P}{\partial\theta}\right) + \ell(\ell+1)P\sin^2\theta\right] + \frac{1}{\Phi}\frac{\partial^2\Phi}{\partial\varphi^2} = 0.$$

#### $\varphi$ Equation

Now, we let the $\varphi$ part be equal to yet another separation constant, which we call $-m^2$, thus giving us the equation

$$\frac{\partial^2\Phi}{\partial\varphi^2} = -m^2\Phi,\qquad \Phi\,\text{ periodic with period } 2\pi.$$

If we solve this equation, we get a set of solutions $\Phi_m$ depending on $m$

$$\Phi_m = e^{im\varphi} \qquad m\in \Z,$$

and find that, in order for periodicity to hold, we must have that $m$ be an integer; $m$ can be positive or negative.

#### $\theta$ Equation

We now proceed to the $\theta$ equation, 

$$\frac{1}{P}\left[\sin\theta\frac{\partial}{\partial\theta}\left(\sin\theta\frac{\partial P}{\partial\theta}\right) + \ell(\ell+1)P\sin^2\theta\right] - m^2 = 0.$$

First, we multiply both sides by $P$ and get 

$$\sin\theta\frac{\partial}{\partial\theta}\left(\sin\theta\frac{\partial P}{\partial\theta}\right) + \ell(\ell+1)P\sin^2\theta - m^2P = 0.$$

Solving this equation is much easier if we make the substitution $x = \cos\theta$. This means that the derivative operator with respect to $\theta$ becomes 

$$\frac{\partial }{\partial\theta} = \frac{\partial x }{\partial\theta} \frac{\partial}{\partial x} = -\sin\theta \frac{\partial P}{\partial x}.$$

Changing our derivatives to be in terms of $x$ gives us 

$$-\sin^2\theta\frac{\partial}{\partial x}\left(-\sin^2\theta \frac{\partial P}{\partial x}\right) + \ell(\ell+1)\sin^2\theta P - m^2 O = 0.$$

Using the identity $\sin^2\theta = 1-\cos^2\theta = 1-x^2$, we can rewrite the equation entirely in terms of $x$.

$$(1-x^2)\theta\frac{\partial}{\partial x}\left((1-x^2)theta \frac{\partial P}{\partial x}\right) + \ell(\ell+1)(1-x^2)\theta P - m^2 P = 0.$$

Finally, we write it in familiar form by dividing through by $1-x^2$:

$$\frac{\partial}{\partial x}\left((1-x^2)\frac{\partial P}{\partial x}\right) - \frac{m^2}{1-x^2}P + \ell(\ell+1)P = 0.$$

This is the Legendre equation, whose solutions are the *associated Legendre polynomials*, $P^m_\ell(x)$. If you want to see how these are derived, please consult a course on ordinary differential equations. Now, we substitute back in $x = \cos\theta$ to find the solution to the equation $P^m_\ell (\cos\theta)$. 

#### $r$ Equation

Lastly, we tackle the radial equation. The radial equation is

$$\frac{1}{R}\frac{\partial}{\partial r}\left(r^2\frac{\partial R}{\partial r}\right) + \lambda^2 r^2 - \ell(\ell+1) = 0.$$

This equation is most easily solved by letting $R(r) = Q(r)/\sqrt{r}$. If we make this substitution, then the equation becomes (after expanding the first derivative)

$$\frac{\partial}{\partial r}\left(r^2\frac{Q'}{\sqrt{r}} - \frac{r^2}{2}\frac{Q}{r^{3/2}}\right) + \lambda^2\frac{Q}{\sqrt{r}}r^2 - \ell(\ell+1)\frac{Q}{\sqrt{r}} = 0$$

If we simplify the equation a little bit, we get 

$$\frac{\partial}{\partial r}\left(r^{3/2}Q' - \frac{r^{1/2}}{2}Q\right) + \lambda^2 Q r^{3/2} - \ell(\ell+1)\frac{Q}{\sqrt{r}} = 0.$$

Now, we expand out the second derivative and get 

$$Q''r^{3/2} + \frac{3}{2}r^{1/2}Q' - \frac{1}{4r^{1/2}}Q - \frac{r^{1/2}}{2}Q' + \lambda^2 Q r^{3/2} - \ell(\ell+1)\frac{Q}{\sqrt{r}} = 0.$$

After collecting like terms, we get 

$$r^2 Q'' + rQ' - \left(\ell(\ell+1) + \frac{1}{4}\right)Q + \lambda^2 r^2 Q = 0.$$

Lastly, we divide through by $r^2$ and see an equation which closely resembles the Bessel equation:

$$Q'' + \frac{Q'}{r} + \left(\lambda^2 - \frac{\ell(\ell+1)+1/4}{r^2}\right)Q = 0.$$

To make it identical to the Bessel equation, we let $r = \rho/\lambda$. This gives us 

$$\frac{d^2Q}{d\rho^2} + \frac{1}{\rho}\frac{dQ}{d\rho} + \left(1 - \frac{(\ell+1/2)^2}{\rho^2}\right)Q = 0.$$

The solution to this equation is the Bessel equation, $Q = J_{\ell+1/2}(\rho)$. Thus, the solution to this is 

$$R(r) = \frac{1}{\sqrt{r}}J_{\ell+1/2}(\lambda r).$$

#### Total Solution

Putting it all together, the solution is 

$$u_{\lambda\ell m}(r,\theta,\varphi) = \frac{1}{\sqrt{r}}J_{\ell+1/2}(\lambda r) P^{m}_\ell(\cos\theta) e^{im\varphi}.$$

If one wants to find the values of $\lambda$, then one needs to use the boundary conditions on $R$. 









