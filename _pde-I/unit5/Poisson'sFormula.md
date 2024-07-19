---
layout: lesson
title: Poisson's Formula 
dept: math
course: pde-I
unit: unit5
deptDisplay: Math
courseDisplay: Partial Differential Equations I
unitDisplay: Unit 5
---
In this section, we will describe Poisson's formula for solving Laplace's equation on a circular domain. The purpose of the formula is to formulate a very general expression for the solution, in terms of the boundary conditions. The PDE is the Laplace equation on a disk of radius \\(a\\), with a regularity condition at the origin \\(r=0\\).

$$\begin{align}
\begin{cases}
\nabla^2 u = 0, & r < a,\theta \in [0,2\pi)\\
u(r_0,\theta) = f(\theta), & \theta \in [0,2\pi)\\
\lim_{r\to 0} u(r,\theta) = \text{finite} & 
\end{cases}
\end{align}$$

To solve this, we first need to write the Laplacian in polar coordinates. The PDE becomes 

$$\begin{align}
\frac{1}{r}\frac{\partial}{\partial r}\left(r\frac{\partial u}{\partial r}\right) + \frac{1}{r^2}\frac{\partial^2 u}{\partial \theta^2} = 0
\end{align}$$

We separate variables by introducing

$$\begin{align}
u(r,\theta) = R(r)Y(\theta)
\end{align}$$

If we plug this in, we are lead to

$$\begin{align}
\frac{1}{r}(rR')Y + \frac{Y" R}{r^2} = 0
\end{align}$$

Rearranging slightly, we get

$$\begin{align}
\frac{r}{R}(rR')' = -\frac{Y"}{Y}
\end{align}$$

Now the variables are separated; the left hand side is only a function of \\(r\\) but the right hand side is only a function of \\(\theta\\). Thus we set both sides to be \\(m^2\\). This the \\(\theta\\) equation is

$$\begin{align}
Y" + m^2 Y = 0
\end{align}$$

which tells us that each \\(m\\) yields a solution, thus introducing an \\(m\\) index for \\(Y \to Y_m\\). Note that setting the separation constant to be \\(+m^2\\) (always a positive number) instead of \\(-m^2\\) (always a negative number) is because the negative case would yield solutions which cannot be periodic because they are exponential. Thus for the \\(+m^2\\) case we get the sine and cosine solutions:

$$\begin{align}
Y_m(\theta) = A\cos(m\theta) + B\sin(m\theta)
\end{align}$$

Since \\(u(r,\theta)\\) is periodic in \\(\theta\\) with period \\(2\pi\\), \\(Y_m(\theta)\\) is also periodic with period \\(2\pi\\), which tells us that \\(m\in \ZZ\\). Thus the \\(r\\) equation becomes

$$\begin{align}
r^2 R" + r R' - m^2 R = 0
\end{align}$$

This is an Euler type equation, so we make the ansatz \\(R = r^\alpha\\), which tell us that

$$\begin{align}
\alpha(\alpha-1) + \alpha - m^2 = 0
\end{align}$$

so \\(\alpha = \pm m\\). Thus the general solution for \\(R\\) is

$$\begin{align}
R = Cr^m + D r^{-m}.
\end{align}$$

Without loss of generality, we pick \\(m \geq 0\\) and ignore the \\(m<0\\) case because it just swaps the two solutions. Furthermore, we set \\(D = 0\\) because \\(Dr^{-m}\\) blows up at the origin \\(r\to 0\\). Thus, for the case \\(m > 0\\)

$$\begin{align}
u_m(r,\theta) = Cr^m(A\cos(m\theta) + B\sin(m\theta))
\end{align}$$

For the case \\(m = 0\\), we get that

$$\begin{align}
R = \lambda\log r + A_0
\end{align}$$

and get rid of \\(\lambda\\) because it causes a divergent solution at the origin, so we are left only with the constant term. Note that \\(Y_0\\) is also a constant. Thus, the total solution is a constant plus all of the positive \\(m\\) solutions:

$$\begin{align}
u(r,\theta) = \frac{1}{2}a_0 + \sum_{m=1}^\infty r^m(a_m\cos(m\theta) + b_m\sin(m\theta)).
\end{align}$$

Now plugging in the boundary condition \\(u(r_0,\theta) = f(\theta)\\), we have that

$$\begin{align}
u(r_0,\theta) = \frac{1}{2}a_0 + \sum_{m=1}^\infty r_0^m (a_m\cos(m\theta) + b_m\sin(m\theta)) = f(\theta)
\end{align}$$

This is an expansion of \\(f\\) in terms of a Fourier series! We can solve for the coefficients by using the formulas

$$\begin{align}
a_m = \frac{1}{\pi r_0^m}\int_0^{2\pi} f(\theta)\cos(m\theta) \d\theta,\qquad b_m = \frac{1}{\pi r_0^m}\int_0^{2\pi}f(\theta)\sin(m\theta) \d\theta.
\end{align}$$

Plugging these Fourier coefficients in to \\(u_m\\), we get

$$\begin{align}
u_m(r,\theta) ={}& \frac{1}{\pi r_0^m}r^m\left(\cos(m\theta)\int_0^{2\pi}f(\theta')\cos(m\theta') \d\theta' + \sin(m\theta) \int_0^{2\pi}f(\theta')\sin(m\theta') \d\theta'\right) \\
={}& \frac{r^m}{\pi r_0^m}\int_0^{2\pi}\cos(\theta-\theta')f(\theta') \d\theta'\\
={}& \frac{1}{2\pi r_0^m}\int f(\theta')\left(r^m e^{im(\theta-\theta')} + r^m e^{-im(\theta-\theta')}\right) \d\theta'
\end{align}$$

Now, plug this back into the series, which gives us

$$\begin{align}
u(r,\theta) = \frac{1}{2\pi}\int_0^{2\pi} f(\theta') \d\theta' + \frac{1}{2\pi}\sum_{m=1}^\infty \int_0^{2\pi} f(\theta') (z^m + (z^*)^m) \d\theta'
\end{align}$$

where \\(z = re^{i(\theta-\theta')}/r_0\\). Now interchanging the order of summation and integration, we get a geometric series (without the \\(m=0\\) term, so we subtract 1). Summing these series,

$$\begin{align}
u(r,\theta) ={}& \frac{1}{2\pi}\int_0^{2\pi} f(\theta') \d\theta' + \frac{1}{2\pi} \int_0^{2\pi} f(\theta') \left(\frac{1}{1-z} + \frac{1}{1-z^*} - 2\right) \d\theta' \\
={}& \frac{1}{2\pi}\int_0^{2\pi} f(\theta') \d\theta' + \frac{1}{2\pi}\int_0^{2\pi} f(\theta') \left[\frac{1 - z^* + 1-z - 2(1-z)(1-z^*)}{1 - z - z^* + \|z\|^2} \right] \d\theta' \\
={}& \frac{1}{2\pi}\int_0^{2\pi} f(\theta') \d\theta' + \frac{1}{2\pi} \int_0^{2\pi} f(\theta') \left(\frac{z+z^* - 2\|z\|^2}{1-z-z^*+\|z\|^2} \right) \d\theta' \\
={}& \frac{1}{2\pi}\int_0^{2\pi} f(\theta') \d\theta' + \frac{1}{2\pi} \int_0^{2\pi} f(\theta') \left(\frac{2r\cos(\theta-\theta') - 2r^2}{1- 2r\cos(\theta-\theta') + r^2}\right) \d\theta' \\
={}& \frac{1}{\pi}\int_0^{2\pi}f(\theta')\left(\frac{r\cos(\theta-\theta') - r^2}{1-2r\cos(\theta-\theta') + r^2} + \frac{1}{2}\right) \d\theta'
\end{align}$$

