---
layout: lesson
dept: physics
title: Boltzmann Equation
course: kt
unit: unit1
deptDisplay: Physics
courseDisplay: Kinetic Theory
unitDisplay: Unit 1
---

### Boltzmann Equation
To finally derive the Boltzmann equation, let's examine the first two equations of the BBGKY heierarchy. These equations are for $f_1(\q_1,\p_1,t)$ and $f_2(\q_1,\p_1,\q_2,\p_2,t)$. Written out explicitly for $s=1$ and $s=2$, they are 

$$\begin{align*}
\frac{\partial f_1}{\partial t} + \{f_1,\H_1\} =& \int \sum_{j=1}^1 \frac{\partial V(\q_{2} - \q_j)}{\partial \q_j} \frac{\partial f_{2}}{\partial\p_j}d\q_{2} d\p_{2} \\
\frac{\partial f_1}{\partial t} + \frac{\partial f_1}{\partial\q_1}\frac{\partial \H_1}{\partial\p_1} - \frac{\partial f_1}{\partial\p_1} \frac{\partial \H_1}{\partial\q_1} =& \int \frac{\partial V(\q_2 - \q_1)}{\partial \q_1} \frac{\partial f_2}{\partial\p_1} d\q_2 d\p_2\\
\frac{\partial f_1}{\partial t} + \frac{\p_1}{m} \frac{\partial f_1}{\partial\q_1}- \frac{\partial U}{\partial\q_1}  \frac{\partial f_1}{\partial\p_1}=& \int \frac{\partial V(\q_2 - \q_1)}{\partial \q_1} \frac{\partial f_2}{\partial\p_1} d\q_2 d\p_2
\end{align*}$$

The second equation in the BBGKY heierarchy is already much more complicated! To simplify this equation we will have to make note of the fact that $V$ is a symmetric potential. That is, $V(\q_1 - \q_2) = V(\q_2 - \q_1)$.

$$\begin{align*}
\frac{\partial f_2}{\partial t} + \{f_2,\H_2\} =& \int \sum_{j=1}^2 \frac{\partial V(\q_{3} - \q_j)}{\partial \q_j} \frac{\partial f_{3}}{\partial\p_j}d\q_{3} d\p_{3}\\
\frac{\partial f_2}{\partial t}  + \frac{\partial f_2}{\partial \q_1}\frac{\partial \H_2}{\partial\p_1} - \frac{\partial f_2}{\partial\p_1}\frac{\partial\H_2}{\partial\q_1} +  \frac{\partial f_2}{\partial \q_2}\frac{\partial \H_2}{\partial\p_2} - \frac{\partial f_2}{\partial\p_2}\frac{\partial\H_2}{\partial\q_2}  =& \int \left( \frac{\partial V(\q_{3} - \q_1)}{\partial \q_1} \frac{\partial f_{3}}{\partial\p_1} +  \frac{\partial V(\q_{3} - \q_2)}{\partial \q_2} \frac{\partial f_{3}}{\partial\p_2} \right) d\q_{3} d\p_{3}\\
\frac{\partial f_2}{\partial t}  + \frac{\p_1}{m}\frac{\partial f_2}{\partial \q_1} - \left(\frac{\partial U}{\partial\q_1} + \frac{\partial V(\q_1 - \q_2)}{\partial\q_1}\right)\frac{\partial f_2}{\partial\p_1} +  \frac{\p_2}{m}\frac{\partial f_2}{\partial \q_2}- \left(\frac{\partial U}{\partial\q_2} + \frac{\partial V(\q_1 - \q_2)}{\partial\q_2}\right)\frac{\partial f_2}{\partial\p_2} =& \int \left( \frac{\partial V(\q_{3} - \q_1)}{\partial \q_1} \frac{\partial f_{3}}{\partial\p_1} +  \frac{\partial V(\q_{3} - \q_2)}{\partial \q_2} \frac{\partial f_{3}}{\partial\p_2} \right) d\q_{3} d\p_{3} 
\end{align*}$$

If we note that 

$$\frac{\partial V(\q_2 - \q_1)}{\partial\q_1} = -\frac{\partial V(\q_2 - \q_1)}{\partial\q_2},$$

then we can simplify this to 

$$\begin{align*}
\frac{\partial f_2}{\partial t}  + \frac{\p_1}{m}\frac{\partial f_2}{\partial \q_1} - \frac{\partial U}{\partial\q_1}\frac{\partial f_2}{\partial\p_1} +  \frac{\p_2}{m}\frac{\partial f_2}{\partial \q_2}- \frac{\partial U}{\partial\q_2}\frac{\partial f_2}{\partial\p_2} - \frac{\partial V(\q_1 - \q_2)}{\partial\q_1}\left(\frac{\partial f_2}{\partial\p_1} - \frac{\partial f_2}{\partial\p_2}\right) =& \int \left( \frac{\partial V(\q_{3} - \q_1)}{\partial \q_1} \frac{\partial f_{3}}{\partial\p_1} +  \frac{\partial V(\q_{3} - \q_2)}{\partial \q_2} \frac{\partial f_{3}}{\partial\p_2} \right) d\q_{3} d\p_{3} 
\end{align*}$$

Let's summarize the two equations:

<div class="result">
The two equations of the BBGKY heierarchy that are of interest to us are 

$$\begin{align*}\left[\frac{\partial }{\partial t} + \frac{\p_1}{m} \frac{\partial }{\partial\q_1}- \frac{\partial U}{\partial\q_1}  \frac{\partial }{\partial\p_1}\right] f_1 =& \int \frac{\partial V(\q_2 - \q_1)}{\partial \q_1} \frac{\partial f_2}{\partial\p_1} d\q_2 d\p_2 \end{align*}$$

$$\begin{align*}
\left[\frac{\partial }{\partial t}  + \frac{\p_1}{m}\frac{\partial }{\partial \q_1} - \frac{\partial U}{\partial\q_1}\frac{\partial }{\partial\p_1} +  \frac{\p_2}{m}\frac{\partial }{\partial \q_2}- \frac{\partial U}{\partial\q_2}\frac{\partial }{\partial\p_2} - \frac{\partial V(\q_1 - \q_2)}{\partial\q_1}\left(\frac{\partial }{\partial\p_1} - \frac{\partial }{\partial\p_2}\right)\right] f_2 =& \int \left( \frac{\partial V(\q_{3} - \q_1)}{\partial \q_1} \frac{\partial f_{3}}{\partial\p_1} +  \frac{\partial V(\q_{3} - \q_2)}{\partial \q_2} \frac{\partial f_{3}}{\partial\p_2} \right) d\q_{3} d\p_{3} 
\end{align*}$$

</div> <br>

These are the two equations of the BBGKY heierarchy that we will analyze. These equations have different limits that can be studied. This is done by analyzing the different time scales over which these terms act. 

* The terms like $\partial U/\partial\q \cdot \partial/\partial\p_2$ have order $1/\tau$ which is the average collision time of a particle with the walls of the box it's contained in
* The terms like $\partial V/\partial \q \cdot \partial/\partial \p$ have order $1/\tau_c$, which is the average time it takes for two particles to come together and then scatter.
* The term on the right hand side of the second equation has order $1/\tau_x$ which is the average time between consecutive collisions of two particles. 

In the Boltzmann formalism, we set the RHS of the second equation to zero and simply have the first two equations in the BBGKY heierarchy as 

$$\begin{align*}\left[\frac{\partial }{\partial t} + \frac{\p_1}{m} \frac{\partial }{\partial\q_1}- \frac{\partial U}{\partial\q_1}  \frac{\partial }{\partial\p_1}\right] f_1 =& \int \frac{\partial V(\q_2 - \q_1)}{\partial \q_1} \frac{\partial f_2}{\partial\p_1} d\q_2 d\p_2 \end{align*}$$

$$\begin{align*}
\left[\frac{\partial }{\partial t}  + \frac{\p_1}{m}\frac{\partial }{\partial \q_1} - \frac{\partial U}{\partial\q_1}\frac{\partial }{\partial\p_1} +  \frac{\p_2}{m}\frac{\partial }{\partial \q_2}- \frac{\partial U}{\partial\q_2}\frac{\partial }{\partial\p_2} - \frac{\partial V(\q_1 - \q_2)}{\partial\q_1}\left(\frac{\partial }{\partial\p_1} - \frac{\partial }{\partial\p_2}\right)\right] f_2 =& 0
\end{align*}$$

The second equation is an equation for $f_2$, which can then be plugged into the first equation to find $f_1$. It is possible to do some more manipulations to simplify these further. We attempt to massage the first equation so that it looks like the second equation, which will allow us to "plug in" the second equation to the first. Let's look more closely at the first equation. 

$$\begin{align*}\left[\frac{\partial }{\partial t} + \frac{\p_1}{m} \frac{\partial }{\partial\q_1}- \frac{\partial U}{\partial\q_1}  \frac{\partial }{\partial\p_1}\right] f_1 =& \int \frac{\partial V(\q_2 - \q_1)}{\partial \q_1} \frac{\partial f_2}{\partial\p_2} d\q_2 d\p_2 \end{align*}$$

Let's add a term to the right hand side. 

$$\begin{align*}\left[\frac{\partial }{\partial t} + \frac{\p_1}{m} \frac{\partial }{\partial\q_1}- \frac{\partial U}{\partial\q_1}  \frac{\partial }{\partial\p_1}\right] f_1 =& \int \frac{\partial V(\q_2 - \q_1)}{\partial \q_1} \left(\frac{\partial }{\partial\p_1} - \frac{\partial}{\partial\p_2}\right)f_2  d\q_2 d\p_2 \end{align*}$$

The term that we added is actually zero because we can integrate it over $\p_2$ and end up with a negligible surface term. This term looks exactly like part of the second equation in the BBGKY heierarchy! 

When we discuss collision/scattering processes, it is often useful to consider the centre of mass coordinate system. Consider two particles with positions $\q_1$ and $\q_2$. Define the center of mass coordinate and relative coordinate to be 

$$\textbf{Q} = \frac{\q_1 + \q_2}{2},\qquad \q = \q_2 - \q_1$$

respectively. We then change the derivatives

$$\frac{\partial}{\partial \q_1} = -\frac{\partial}{\partial\q}, \qquad \frac{\partial}{\partial \q_2} = \frac{\partial}{\partial\q}$$

so that the second equation of the BBGKY heierarchy becomes 

$$\begin{align*}
\left[\frac{\partial }{\partial t} + \frac{\p_2-\p_1}{m}\frac{\partial }{\partial \q} - \frac{\partial U}{\partial\q_1}\frac{\partial }{\partial\p_1} - \frac{\partial U}{\partial\q_2}\frac{\partial }{\partial\p_2} - \frac{\partial V(\q_1 - \q_2)}{\partial\q_1}\left(\frac{\partial }{\partial\p_1} - \frac{\partial }{\partial\p_2}\right)\right] f_2 =& 0
\end{align*}$$

We now recognize that the external forces $\partial U/\partial\q_1$ and $\partial U/\partial\q_2$ are much smaller than the interaction term. Thus we ignore them to get 

$$\begin{align*}
\left[\frac{\partial }{\partial t} + \frac{\p_2-\p_1}{m}\frac{\partial }{\partial \q} - \frac{\partial V(\q_1 - \q_2)}{\partial\q_1}\left(\frac{\partial }{\partial\p_1} - \frac{\partial }{\partial\p_2}\right)\right] f_2 =& 0
\end{align*}$$

Now we isolate 

$$\begin{align*}
\left[\frac{\partial }{\partial t} + \frac{\p_2-\p_1}{m}\frac{\partial }{\partial \q}\right]  f_2 =& \frac{\partial V(\q_1 - \q_2)}{\partial\q_1}\left(\frac{\partial }{\partial\p_1} - \frac{\partial }{\partial\p_2}\right)f_2
\end{align*}$$

and thus plug this result into the first equation from the BBGKY heierarchy. 

$$\begin{align*}\left[\frac{\partial }{\partial t} + \frac{\p_1}{m} \frac{\partial }{\partial\q_1}- \frac{\partial U}{\partial\q_1}  \frac{\partial }{\partial\p_1}\right] f_1 =& \int \left[\frac{\p_2-\p_1}{m}\frac{\partial }{\partial \q}\right]  f_2  d\q_2 d\p_2 \end{align*}$$

Now we change variables in the integral from being over $\q_2$ to being over $\q$. 

$$\begin{align*}\left[\frac{\partial }{\partial t} + \frac{\p_1}{m} \frac{\partial }{\partial\q_1}- \frac{\partial U}{\partial\q_1}  \frac{\partial }{\partial\p_1}\right] f_1 =& \int \left[\frac{\p_2-\p_1}{m}\frac{\partial }{\partial \q}\right]  f_2  d\q d\p_2 \end{align*}$$

The volume element $\q$ can in fact be split up. Recall that $\q$ is the displacement vector between the two colliding particles. Recall that in any scattering event, we have an impact parameter $\textbf{b}$. Define the axial vector $\textbf{a}$ to be parallel to the momenta $\p_1 - \p_{cm}$ and $\p_2 - \p_{cm}$. Writing $d^3\q = d^2\b da$ allows us to integrate in the $a$ direction. 

We also note that the change in variables for our coordinates implies changes of variables for our momenta as well. This allows us to simplify the integral by writing in terms of the momenta relevant to the collision. 

(show figure of scattering event here)

The vector $\textbf{a}$ is parallel to the line $\p_2 - \p_1$. It is also parallel to $\q$. This allows us to put an absolute value sign on the difference in momenta and integrate over $a$. 

$$\int\left[\frac{\p_2 - \p_1}{m}\frac{\partial}{\partial\q} \right] f_2 d\q d\p_2 = \int\left[\frac{|\p_2 - \p_1|}{m}\frac{\partial}{\partial a} \right] f_2  da d^2\textbf{b} d\p_2$$

Explicitly integrating over $a$, we can actually evaluate the bounds just outside the region of interaction as opposed to at the edges of the box we're working in. 

$$\int\left[\frac{|\p_2 - \p_1|}{m}\frac{\partial}{\partial a} \right] f_2  da d^2\textbf{b} d\p_2 = \int\frac{|\p_2 - \p_1|}{m} [f_2(\p'_1,\p'_2,t) - f_2(\p_1,\p_2,t)] d^2\textbf{b} d\p_2 $$

The explicit dependence on $\q$ has been integrated out, but $\p_1'$ and $\p_2'$ are both functions of $\p_1$, $\p_2,$ and $\textbf{b}$. Now, we claim the assumption of molecular chaos. If the two particles that are colliding are far away from one another, the distribution function $f_2$ can be split up into two. The assumption comes from assuming that they can also be split up when they are close to one another, and that this splitting up occurs just outside the region of interaction. Writing 

$$f_2(\q_1,\q_2,\p_1,\p_2,t) = f_1(\q_1,\p_1,t) f_1(\q_2,\p_2,t),$$

$$\int\left[\frac{|\p_2 - \p_1|}{m}\frac{\partial}{\partial a} \right] f_2  da d^2\textbf{b} d\p_2 = \int\frac{|\p_2 - \p_1|}{m} [f_1(\q_2,\p'_1,t) f_1(\q_2, \p'_2,t) - f_1(\q_1\p_1,t) f_1(\q_1,\p_2,t)] d^2\textbf{b} d\p_2 $$

and then let the two positions $\q_1$ and $\q_2$ to be the same, which makes sense just outside the region of interaction.

$$\int\left[\frac{|\p_2 - \p_1|}{m}\frac{\partial}{\partial a} \right] f_2  da d^2\textbf{b} d\p_2 = \int\frac{|\p_2 - \p_1|}{m} [f_1(\q_1,\p'_1,t) f_1(\q_1, \p'_2,t) - f_1(\q_1, \p_1,t) f_1(\q_1, \p_2,t)] d^2\textbf{b} d\p_2 $$

We now define the collision integral

$$C[f_1,f_1] =  \int\frac{|\p_2 - \p_1|}{m} [f_1(\p'_1,t) f_1(\p'_2,t) - f_1(\p_1,t) f_1(\p_2,t)] d^2\textbf{b} d\p_2$$

We further define the Liouville operator 

$$\L f_1 = \left[\frac{\partial }{\partial t} + \frac{\p_1}{m}\frac{\partial }{\partial \q_1} - \frac{\partial U}{\partial q}\frac{\partial }{\partial \p}\right]f_1$$

which allows us to define 

<div class="result">
The Boltzmann equation $\L f_1 = C[f_1,f_2]$ is the PDE

$$ \left[\frac{\partial }{\partial t} + \frac{\p_1}{m}\frac{\partial }{\partial \q_1} - \frac{\partial U}{\partial \q}\frac{\partial }{\partial \p}\right]f_1 = \int\frac{|\p_2 - \p_1|}{m} [f_1(\p'_1,t) f_1(\p'_2,t) - f_1(\p_1,t) f_1(\p_2,t)] d^2\textbf{b} d\p_2$$
</div> <br>
 
 The Boltzmann equation is a PDE of seven variables: $\q$ is a 3D vector, $\p$ is a 3D vector, and we also have time $t$. 










