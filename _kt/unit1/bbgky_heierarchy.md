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

### BBGKY Heierarchy

In kinetic theory, we define a distribution function $\rho(\textbf{q},\textbf{p},t)$ for $N$ particles. This distribution function has units 

$$[\rho] = \frac{1}{[\text{momentum}]^{3N}[\text{position}]^{3N}}$$

and has the interpretation that the quantity (where $d\textbf{q}$ is a $3N$ dimensional element, and $d\textbf{q}$ is also a $3N$ dimensional element)

$$\rho(\textbf{q},\textbf{p},t) d \textbf{q} d\textbf{p}$$

is the probability that particle 1 is in $[\textbf{q}_1, \textbf{q}_1 + d\textbf{q}_1]$ with momentum $[\textbf{p}_1,\textbf{p}_1 + d\textbf{p}_1]$,  particle 2 is in $[\textbf{q}_2, \textbf{q}_2 + d\textbf{q}_2]$ with momentum $[\textbf{p}_2,\textbf{p}_2 + d\textbf{p}_2]\dots$  particle $N$ is in $[\textbf{q}_N, \textbf{q}_N + d\textbf{q}_N]$ with momentum $[\textbf{p}_N,\textbf{p}_N + d\textbf{p}_N]$, all at time $t$. 

This distribution function is very complicated! It is a function of $6N$ variables (not including time) and $N$ is normally on the order of Avogadro's number. It is made simpler if we define a 1-particle distribution function $f_1(\textbf{q},\textbf{p},t)$ as the following: 

$$\begin{align*}
f_1(\textbf{q},\textbf{p},t) =& \left<\sum_{i=1}^N\delta^{(3)}(\textbf{q}-\textbf{q}_i)\delta^{(3)}(\textbf{p}-\textbf{p}_i) \right>\\
=& \int \sum_{i=1}^N\delta^{(3)}(\textbf{q}-\textbf{q}_i)\delta^{(3)}(\textbf{p}-\textbf{p}_i) \rho(\textbf{q},\textbf{p},t) d\textbf{q}d\textbf{p}\\
=& \sum_{i=1}^N\int \delta^{(3)}(\textbf{q}-\textbf{q}_i)\delta^{(3)}(\textbf{p}-\textbf{p}_i) \rho(\textbf{q},\textbf{p},t) d\textbf{q}d\textbf{p}\\
=& \sum_{i=1}^N\int \rho(\textbf{q}_1,..,\textbf{q}_{i-1},\textbf{q},\textbf{q}_{i+1},..,\textbf{q}_N,\textbf{p}_1, \dots \textbf{p}_i = \textbf{p},\dots,\textbf{p}_N,t) \prod_{\substack{j=1\\ j\neq i}}^N d\textbf{q}_j d\textbf{p}_j
\end{align*}$$

I claim that all of the integrals in this sum (there are $N$ integrals) will be the same. We assume that the distribution $\rho$ is symmetric upon permuting different particles' positions and momenta. Thus, this simplifies to (arbitrarily picking $1$ as the argument which we set to $\textbf{q}$,$\textbf{p}$.)

$$\begin{align*}
f_1(\textbf{q},\textbf{p},t) =& N\int \rho(\textbf{q}_1 = \textbf{q},\textbf{q}_2\dots \textbf{q}_N,\textbf{p}_1 = \textbf{p},\textbf{p}_2,\dots,\textbf{p}_N,t) \prod_{i=2}^N d\textbf{q}_i d\textbf{p}_i 
\end{align*}$$

We can similarly define a 2-particle density 

$$\begin{align*}
f_2(\textbf{q}_1,\textbf{p}_1,\textbf{q}_2,\textbf{p}_2,t) =& N(N-1)\int \rho(\textbf{q}_1, \textbf{q}_2\dots \textbf{q}_N,\textbf{p}_1, \textbf{p}_2,\dots,\textbf{p}_N,t) \prod_{i=3}^N d\textbf{q}_i d\textbf{p}_i 
\end{align*}$$

which suggests the form for an $s$-particle density

$$f_s(\textbf{q}_1,\dots,\textbf{q}_s,\textbf{p}_1,\dots,\textbf{p}_s,t) = \frac{N!}{(N-s)!}\int \rho(\textbf{q}_1,\dots,\textbf{q}_s,\dots\textbf{q}_N,\textbf{p}_1,\dots,\textbf{p}_s,\dots,\textbf{p}_N,t)  \prod_{i=s+1}^N d\textbf{q}_i d\textbf{p}_i $$

and note that 

$$f_N(\textbf{q},\textbf{p},t) = N!\rho(\textbf{q},\textbf{p},t).$$

We further define $\rho_s$ by 

$$f_s = \frac{N!}{(N-s)!} \rho_s.$$

We can then ask, how does the $s$-particle density evolve through time at a fixed point in space (we want to know the partial derivative of $\rho_s$ with respect to time, not the total derivative)? We already know that the time evolution of an observable $\mathcal{O}$ of all the $\textbf{q}$'s and $\textbf{p}$'s evolves according to

$$\frac{d\mathcal{O}}{dt} = \frac{\partial \mathcal{O}}{\partial t} + \left\{\mathcal{O}, \mathcal{H}\right\}.$$

The form of the Hamiltonian clearly plays an important role in how the distribution evolves! We will use the simplest Hamiltonian including a two-body interaction. This two body interaction could be a Coulomb interaction, Lennard-Jones potential, or something else. The point is that we don't consider three or four body interactions. The Hamiltonian describing this is 

$$\mathcal{H} = \sum_{i=1}^N\left[\frac{\textbf{p}_i^2}{2m} + U(\textbf{q}_i)\right] + \frac{1}{2}\sum_{i,j = 1}^N V(\textbf{q}_i - \textbf{q}_j)$$

where the sum over $i,j$ omits term where $i=j$; the particles don't interact with themselves.

Consider now

$$\begin{align*}
\frac{d\rho_s}{dt} =& \frac{d}{dt}\int\rho(\textbf{q},\textbf{p},t)  \prod_{i=s+1}^N d\textbf{q}_i d\textbf{p}_i \\
=& \int  \frac{d}{dt}\rho(\textbf{q},\textbf{p},t)  \prod_{i=s+1}^N d\textbf{q}_i d\textbf{p}_i \\
=& 0
\end{align*} $$

This tells us that $d\rho_s/dt = 0$ too! Thus, it is possible to represent 

$$\begin{align*}
\frac{\partial\rho_s}{\partial t} = \frac{\partial}{\partial t} \int\rho(\textbf{q},\textbf{p},t)  \prod_{i=s+1}^N d\textbf{q}_i d\textbf{p}_i \\
=& \int   \frac{\partial}{\partial t}\rho(\textbf{q},\textbf{p},t)  \prod_{i=s+1}^N d\textbf{q}_i d\textbf{p}_i 
\end{align*}$$

We can thus use the fact that 

$$\frac{\partial\rho}{\partial t} + \{\rho,H\} = 0$$

to get 

$$\begin{align*}
\frac{\partial\rho_s}{\partial t} =& - \int \{\rho,\mathcal{H}\}  \prod_{i=s+1}^N d\textbf{q}_i d\textbf{p}_i
\end{align*}$$

We thus split up $\mathcal{H}$ into three parts:

$$\mathcal{H} = \mathcal{H}_s + \mathcal{H}_{N-s} + \tilde{\mathcal{H}}$$

whereby

$$\mathcal{H}_s = \sum_{i=1}^s \left[\frac{\textbf{p}_i^2}{2m} + U_i(\textbf{q})\right] + \frac{1}{2}\sum_{i,j=1}^s V(\textbf{q}_i - \textbf{q}_j)$$

$$\mathcal{H}_{N-s} = \sum_{i=s+1}^N \left[\frac{\textbf{p}_i^2}{2m} + U_i(\textbf{q})\right] + \frac{1}{2}\sum_{i,j=s+1}^N V(\textbf{q}_i - \textbf{q}_j)$$

$$\tilde{\mathcal{H}}= \sum_{i=1}^s\sum_{j=s+1}^N V(\textbf{q}_i - \textbf{q}_j)$$

so, 

* $\mathcal{H}_s$ contains only energies of the first $s$ particles and their interactions with one another
* $\mathcal{H}_{N-s}$ contains only energies of the last $N-s$ particles and their interactions with one another
* $\tilde{\mathcal{H}}$ contains the interactions between the first $s$ particles and the last $N-s$ particles.

We substitute these expressions in and note that we have three separate integrals to evaluate.  

$$\begin{align*}
\frac{\partial\rho_s}{\partial t} =& - \int \{\rho,\mathcal{H}_s + \mathcal{H}_{N-s} + \tilde{\mathcal{H}}\}  \prod_{i=s+1}^N d\textbf{q}_i d\textbf{p}_i
\end{align*}$$

Looking at the first Poisson bracket, we want to evaluate 

$$\int\{\rho,\mathcal{H}_s\}  \prod_{i=s+1}^N d\textbf{q}_i d\textbf{p}_i,$$

but immediately notice that the (surviving) differentiations are all with respect to $\q_1,\dots,\q_s$, and $\p_1,\dots,\p_s$ because $\H_s$ is independent of the variables $\textbf{q}_{s+1},\dots,\textbf{q}_N$ and $\textbf{p}_s,\dots,\textbf{p}_N$. This means that we can interchange the order of differentiation and integration:

$$\begin{align*}
\int\{\rho,\H_s\}  \prod_{i=s+1}^N d\textbf{q}_i d\textbf{p}_i =& \left\{\int\rho \prod_{i=s+1}^N d\textbf{q}_i d\textbf{p}_i,\H_s\right\}\\
=& \{\rho_s,\H_s\}\end{align*}$$

That wasn't so bad! Now, let's move on to the next Poisson bracket. 

$$\begin{align*}
\int\{\rho,\H_{N-s}\} \prod_{i=s+1}^N d\q_i d\p_i =& \int \sum_{j=1}^N \left( \frac{\partial\rho}{\partial\q_j}\frac{\partial \H_{N-s}}{\partial \p_j} - \frac{\partial\rho }{\partial\p_j}\frac{\partial H_{N-s}}{\partial \q_j}\right)\prod_{i=s+1}^N d\q_i d\p_i\\
=& \int \sum_{j=s+1}^N \left( \frac{\partial\rho}{\partial\q_j}\frac{\partial \H_{N-s}}{\partial \p_j} - \frac{\partial\rho }{\partial\p_j}\frac{\partial H_{N-s}}{\partial \q_j}\right)\prod_{i=s+1}^N d\q_i d\p_i
\end{align*}$$

where we used the fact that $\H_{N-s}$ is independent of $\q_1,\dots \q_s$ and $\p_1,\dots \p_s$ to go from the first line to the second line. Now, we plug in our actual Hamiltonian $\H_{N-s}$. The actual form of the Hamiltonian does not matter at this point, but what does matter is that the derivatives

$$\frac{\partial \H_{N-s}}{\partial \q_j}$$

are all independent of momenta $\p_i$, and that 

$$\frac{\partial \H_{N-s}}{\partial \p_j}$$

are all independent of positions $\q_i$. 

Plugging these in, making sure to note all dependencies now,

$$\begin{align*}
\int\{\rho,\H_{N-s}\} \prod_{i=s+1}^N d\q_i d\p_i =& \int \sum_{j=s+1}^N \left( \frac{\partial\rho(\q,\p,t)}{\partial\q_j}\frac{\partial \H_{N-s}}{\partial \p_j}(\p) - \frac{\partial\rho(\q,\p,t) }{\partial\p_j}\frac{\partial H_{N-s}}{\partial \q_j}(\q) \right)\prod_{i=s+1}^N d\q_i d\p_i
\end{align*}$$

We can split this up into two integrals, and also rearrange some brackets with the derivatives. This is where the derivatives of the Hamiltonian with respect to $\q$ and $\p$ being independent of $\p$ and $\q$ respectively comes in useful.

$$\begin{align*}
\int\{\rho,\H_{N-s}\} \prod_{i=s+1}^N d\q_i d\p_i =& \int \sum_{j=s+1}^N \frac{\partial\rho(\q,\p,t)}{\partial\q_j}\frac{\partial \H_{N-s}}{\partial \p_j}(\p) \prod_{i=s+1}^N d\q_i d\p_i-  \int  \frac{\partial\rho(\q,\p,t) }{\partial\p_j}\frac{\partial H_{N-s}}{\partial \q_j}(\q) \prod_{i=s+1}^N d\q_i d\p_i \\
=& \int \sum_{j=s+1}^N \frac{\partial}{\partial\q_j}\left(\rho(\q,\p,t)\frac{\partial \H_{N-s}}{\partial \p_j}(\p)\right) \prod_{i=s+1}^N d\q_i d\p_i - \int  \frac{\partial}{\partial\p_j}\left(\rho(\q,\p,t) \frac{\partial H_{N-s}}{\partial \q_j}(\q)\right) \prod_{i=s+1}^N d\q_i d\p_i
\end{align*}$$

Now, in the first integral, we perform the $\q$ integration first. This leaves us with a surface term, which gives us zero. In the second integral, we perform the $\p$ integration first. This leaves us again with a surface term, which again gives us zero. Thus 

$$\int\{\rho,\H_{N-s}\} \prod_{i=s+1}^N d\q_i d\p_i  = 0$$

Now, we proceed onto the last Poisson bracket. 

$$\begin{align*}
\int\{\rho,\H'\} \prod_{i=s+1}^N d\q_i d\p_i =& \int\sum_{j=1}^N\left(\frac{\partial\rho}{\partial\q_j} \frac{\partial\tilde{\H}}{\partial\p_j} - \frac{\partial\rho}{\partial\p_j} \frac{\partial\tilde{\H}}{\partial\q_j}\right)\prod_{i=s+1}^N d\q_i d\p_i\\
=& -\int\sum_{j=1}^N\left(\frac{\partial\rho}{\partial\p_j} \frac{\partial\tilde{\H}}{\partial\q_j}\right)\prod_{i=s+1}^N d\q_i d\p_i
\end{align*}$$

where, because $\tilde{\H}$ is independent of all momenta $\p$, we dropped the first term of the Poisson bracket. Now, we split up the sum over $j$ into two. 

$$\begin{align*}
\int\{\rho,\H'\} \prod_{i=s+1}^N d\q_i d\p_i =& -\int\left(\sum_{j=1}^s \frac{\partial\rho}{\partial\p_j} \frac{\partial\tilde{\H}}{\partial\q_j} + \sum_{j=s+1}^N \frac{\partial\rho}{\partial\p_j} \frac{\partial\tilde{\H}}{\partial\q_j} \right)\prod_{i=s+1}^N d\q_i d\p_i
\end{align*}$$

This means that we can easily evaluate the derivatives of $\tilde{H}$. If $1 \leq j \leq s$, then

$$\frac{\partial\tilde{\H}}{\partial \q_j} = \sum_{k=s+1}^N \frac{\partial V(\q_k - \q_j)}{\partial \q_j}$$

and if $s+1 \leq j \leq N$, then 

$$\frac{\partial\tilde{\H}}{\partial\q_j} = \sum_{k=1}^s \frac{\partial V(\q_k - \q_j)}{\partial \q_j}.$$

Plugging these in, we get 

$$\begin{align*}
\int\{\rho,\H'\} \prod_{i=s+1}^N d\q_i d\p_i =& -\int\left(\sum_{j=1}^s \frac{\partial\rho}{\partial\p_j} \sum_{k=s+1}^N \frac{\partial V(\q_k - \q_j)}{\partial \q_j}+ \sum_{j=s+1}^N \frac{\partial\rho}{\partial\p_j} \sum_{k=1}^s \frac{\partial V(\q_k - \q_j)}{\partial \q_j} \right)\prod_{i=s+1}^N d\q_i d\p_i
\end{align*}$$

Looking at the second term, we see that the potential has no dependence on any $\p$, so, it evaluates to a surface term over momenta. This is the same logic as we used when we concluded that the integral of the second Poisson bracket was zero. 

$$\begin{align*}
\int\{\rho,\H'\} \prod_{i=s+1}^N d\q_i d\p_i =& -\int\left(\sum_{j=1}^s \frac{\partial\rho}{\partial\p_j} \sum_{k=s+1}^N \frac{\partial V(\q_k - \q_j)}{\partial \q_j} \right)\prod_{i=s+1}^N d\q_i d\p_i
\end{align*}$$

Now we recognize that the sum over $k$ produces $N-s$ terms. We are integrating over all the positions and momenta of the $j = s+1$ to $j=N$ particles, so when integrating over this sum we get the same for each term in it. Thus, we can simplify this to 

$$\begin{align*}
\int\{\rho,\H'\} \prod_{i=s+1}^N d\q_i d\p_i =& -(N-s) \int\left(\sum_{j=1}^s \frac{\partial\rho}{\partial\p_j} \frac{\partial V(\q_{s+1} - \q_j)}{\partial \q_j} \right)\prod_{i=s+1}^N d\q_i d\p_i
\end{align*}$$

where we have just substituted $k = s+1$, but we could have substituted any value between $s+1$ and $N$ inclusive. Now, we integrate over $\p_{s+1}$ and $\q_{s+1}$ last, and the remaining coordinates and momenta first. This looks like 

$$\begin{align*}
\int\{\rho,\H'\} \prod_{i=s+1}^N d\q_i d\p_i =& -(N-s) \int \sum_{j=1}^s \left[\int\left(\frac{\partial\rho}{\partial\p_j} \frac{\partial V(\q_{s+1} - \q_j)}{\partial \q_j} \right)\prod_{i=s+2}^N d\q_i d\p_i \right]d\q_{s+1} d\p_{s+1}
\end{align*}$$

Since the term with $V$ has no dependence on any $\p_j$ and only the $\q_j$ for which $j < s+1$, it can be moved out of the innermost integral. Further, the derivative on $\rho$ with respect to $\p_j$ has $j < s+1$, so it can also be moved out. 

$$\begin{align*}
\int\{\rho,\H'\} \prod_{i=s+1}^N d\q_i d\p_i =& -(N-s) \int \sum_{j=1}^s \frac{\partial V(\q_{s+1} - \q_j)}{\partial \q_j} \frac{\partial}{\partial\p_j} \left[\int \rho \prod_{i=s+2}^N d\q_i d\p_i \right]d\q_{s+1} d\p_{s+1}
\end{align*}$$

And now we recognize the innermost quantity as $\rho_{s+1}$. Thus, 

$$\begin{align*}
\int\{\rho,\H'\} \prod_{i=s+1}^N d\q_i d\p_i =& -(N-s) \int \sum_{j=1}^s \frac{\partial V(\q_{s+1} - \q_j)}{\partial \q_j} \frac{\partial \rho_{s+1}}{\partial\p_j}d\q_{s+1} d\p_{s+1}
\end{align*}$$

This is now an integral over only 6 variables! Unfortunately, we can't make any further simplifications at this point. We are now ready to put the three calculations for these Poisson brackets together. This gives us 

$$\frac{\partial\rho_s}{\partial t} = - \{\rho_s,\H_s\} + (N-s) \int \sum_{j=1}^s \frac{\partial V(\q_{s+1} - \q_j)}{\partial \q_j} \frac{\partial \rho_{s+1}}{\partial\p_j}d\q_{s+1} d\p_{s+1}$$

Let's rearrange this slightly to get 

$$\frac{\partial\rho_s}{\partial t} + \{\rho_s,\H_s\} = (N-s) \int \sum_{j=1}^s \frac{\partial V(\q_{s+1} - \q_j)}{\partial \q_j} \frac{\partial \rho_{s+1}}{\partial\p_j}d\q_{s+1} d\p_{s+1}$$

We have now constructed the BBGKY heierarchy. If we want to find $\partial \rho_1/\partial t$, then we already need $\rho_2$. Similarly, if we want to find $\partial\rho_2/\partial t$, then we already need $\rho_3$. This sequence of dependencies is called the BBGKY heierarchy. 

Note that it is also possible to write the BBGKY heierarchy in terms of the unnormalized densities $f_s$, which gives us 

$$\frac{\partial f_s}{\partial t} + \{f_s,\H_s\} = \int \sum_{j=1}^s \frac{\partial V(\q_{s+1} - \q_j)}{\partial \q_j} \frac{\partial f_{s+1}}{\partial\p_j}d\q_{s+1} d\p_{s+1}$$










