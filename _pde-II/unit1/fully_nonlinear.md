---
layout: lesson
title: Fully Nonlinear Equations
dept: math
course: pde-II
unit: unit1
deptDisplay: Math
courseDisplay: Partial Differential Equations II
unitDisplay: Unit 1
---

### Introduction

In this section, we consider partial differential equations of the form

$$\begin{equation} \label{fullyNonlin} F(x,y,u,u_x,u_y) = 0 \end{equation}$$

where $F$ is some arbitrary but differentiable function of its arguments. We introduce the notation $p = u_x$ and $q = u_y$ for simplicity. 

There are many important systems from physics whose phenomena fall under this category. For example,

* The eikonal equation from optics $$u_x^2 + u_y^2 = 1$$
* The Hamilton-Jacobi equation from classical mechanics $$u_t + H(\textbf{x},\nabla u) = 0$$

### Charpit's Equations

To actually solve an equation of this form, we change it from being 1 partial differential equation to being 5 ordinary differential equations. First, we differentiate equation $\eqref{fullyNonlin}$ with respect to $x$ to get

$$\begin{equation} \frac{dF}{dx} = F_x + F_u u_x + F_p p_x + F_q q_x = 0. \end{equation}$$

If we substitute in $q_x = p_y$ and $u_x = p$, then we have a quasi-linear equation for $p$:

$$\begin{equation} \label{quasi1} F_p p_x + F_q p_y = - F_x - pF_u. \end{equation}$$

To solve this quasi-linear equation, we employ the method of characteristics we discussed before by considering a curve in $(x,y,u)$ space parametrized in terms of a variable $s$. This gives us 

$$\begin{equation} \label{char1} \frac{dx}{ds} = F_p,\qquad \frac{dy}{ds} = F_q,\qquad \frac{dp}{ds} = -F_x - pF_u. \end{equation}$$

If we do the same procedure by differentiating equation $\eqref{fullyNonlin}$ with respect to $y$, we find that

$$\begin{equation}\frac{dF}{dy} = F_y + F_u u_y + F_p p_y + F_q q_y = 0. \end{equation}$$

Next, we substitute in $p_y = q_x$ and $u_y = q$ and end up with a quasi-linear equation for $q$:

$$\begin{equation} \label{quasi2} F_p q_x + F_q q_y = - F_y - qF_u. \end{equation}$$

Solving equation $\eqref{quasi2}$ is identical to solving equation $\eqref{quasi1}$, which gives us the following characteristic equations

$$\begin{equation} \label{char2} \frac{dx}{ds} = F_p,\qquad \frac{dy}{ds} = F_q, \qquad \frac{dq}{ds} = -F_y - qF_u\end{equation}$$

So far, we have characteristic equations for $x,y,p,q$. Note that the equations for $x$ and $y$ are repeated in both $\eqref{char1}$ and $\eqref{char2}$ The last one we need is for $u$. Differentiating $u$ with respect to $s$ and substituting in our equations for $u_x, dx/ds,u_y,dy/ds$, we find

$$\begin{equation} \frac{du}{ds} = u_x \frac{dx}{ds} + u_y\frac{dy}{ds} = pF_p + q F_q.\end{equation}$$

Now, we collect together our 5 equations

<div class="result">
<b>Charpit's Equations:</b>  To solve $F(x,y,u,p,q) = 0$ where $p = u_x$ and $q = u_y$, solve the following system of 5 ordinary differential equations, known as <i>Charpit's equations</i>
$$\frac{dx}{ds} = F_p,\qquad \frac{dy}{ds} = F_q,\qquad \frac{du}{ds} = pF_p + qF_q,\qquad \frac{dp}{ds} = -F_x - pF_u,\qquad \frac{dq}{ds} = -F_y - q F_u.$$
</div>

To actually solve Charpit's equations, we need some initial data. Because we are looking for a surface $u(x,y)$, we need to supply two dimensional initial data. We do this in the form
$$x(s=0) = x_0(\tau),\qquad y(s=0) = y_0(\tau), \qquad u(s=0) = u_0(\tau).$$
where we have specified parametrically the values of $x,y,u$ on the line $s=0$. Given these initial conditions, we find the conditions $p(s=0) = p_0(\tau)$ and $q(s=0) = q_0(\tau)$ from
$$F(x_0,y_0,u_0,p_0,q_0) = 0 \qquad \frac{d_0}{ds} = p_0 \frac{dx_0}{ds} + q_0 \frac{dy_0}{ds}$$

Note that since $F$ is nonlinear, it is possible that more than one characteristic passes through each point on the data curve. 

<div class="example">
<b>Example:</b> Consider the Hamilton-Jacobi equation for a free particle:
$$u_y + u_x^2 = 0.$$
Let's pick initial conditions $u(x,0) = ax$ for $x\in\R$. Then, $F(x,y,u,u_x,u_y) = u_y + u_x^2 = p^2 + q$. Charpit's equations are thus 
$$\begin{align}
\frac{dx}{ds} = 2p & x(0) = \tau \\
\frac{dy}{ds} = 1 & y(0) = 0 \\
\frac{du}{ds} = 2p^2 + q & u(0) = a\tau \\
\frac{dp}{ds} = 0 & p(0) = a \\
\frac{dq}{ds} = 0 & q(0) = -a^2
\end{align}$$

Thus means that $p = a$, $q = -a^2$, $x = 2as + \tau$, $y = s$, and $u = a^2 s + a\tau$. If we eliminate $s$ and $\tau$, we get 
$$u = a(x-ay).$$
and the characteristic curves are $x = 2ay + \tau$; we get one characteristic curve for each value of $\tau$. 
</div>

<div class="example">
<b>Example:</b>

</div>
















