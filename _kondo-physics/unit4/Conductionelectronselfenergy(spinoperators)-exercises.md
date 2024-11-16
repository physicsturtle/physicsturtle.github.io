---
layout: exercises
title: Conduction electron self energy (spin operators)  - Exercises
dept: physics
course: kondo-physics
unit: unit4
deptDisplay: Physics
courseDisplay: Kondo and Heavy Fermion physics
unitDisplay: Unit 4
---
<ol>
<li> <div class="exercise"> 

</div> </li></ol>

### Conduction electron self-energy at 4th order

The fourth order contribution is given by

We need to compute the spin operator correlator 

$$\begin{align}
\langle T_\tau[\Shat^{\ell_1}_0(\tau_1)\Shat^{\ell_2}_0(\tau_2)\Shat^{\ell_3}_0(\tau_3)\Shat^{\ell_4}_0(\tau_4)]\rangle_0 ={}& 
\end{align}$$

It is very tedious to write out all 24 contributions. We note however that, using the cyclic property of the trace, there will be \\(3! = 6\\) distinct ways to arrange the spin operators: 1234, 1243,1324,1342,1423,1432. This gives us 

$$\begin{align}
\langle T_\tau[\Shat^{\ell_1}_0(\tau_1)\Shat^{\ell_2}_0(\tau_2)\Shat^{\ell_3}_0(\tau_3)\Shat^{\ell_4}_0(\tau_4)]\rangle_0 ={}& f(\tau_1,\tau_2,\tau_3,\tau_4)\langle \Shat^{\ell_1}_0\Shat^{\ell_2}_0\Shat^{\ell_3}_0\Shat^{\ell_4}_0\rangle_0 \\
&+ f(\tau_1,\tau_2,\tau_4,\tau_3)\langle \Shat^{\ell_1}_0\Shat^{\ell_2}_0\Shat^{\ell_4}_0\Shat^{\ell_3}_0\rangle_0 \\
&+ f(\tau_1,\tau_3,\tau_2,\tau_4)\langle \Shat^{\ell_1}_0\Shat^{\ell_3}_0\Shat^{\ell_2}_0\Shat^{\ell_4}_0\rangle_0 \\
&+ f(\tau_1,\tau_3,\tau_4,\tau_2)\langle \Shat^{\ell_1}_0\Shat^{\ell_3}_0\Shat^{\ell_4}_0\Shat^{\ell_2}_0\rangle_0 \\
&+ f(\tau_1,\tau_4,\tau_2,\tau_3)\langle \Shat^{\ell_1}_0\Shat^{\ell_4}_0\Shat^{\ell_2}_0\Shat^{\ell_3}_0\rangle_0 \\
&+ f(\tau_1,\tau_4,\tau_3,\tau_2)\langle \Shat^{\ell_1}_0\Shat^{\ell_4}_0\Shat^{\ell_3}_0\Shat^{\ell_2}_0\rangle_0 
\end{align}$$

whereby

$$\begin{align}
f(\tau_1,\tau_2,\tau_3,\tau_4) ={}& \theta(\tau_1-\tau_2)\theta(\tau_2-\tau_3)\theta(\tau_3-\tau_4) + \theta(\tau_2-\tau_3)\theta(\tau_3-\tau_4)\theta(\tau_4-\tau_1) \\
&+ \theta(\tau_3-\tau_4)\theta(\tau_4-\tau_1)\theta(\tau_1-\tau_2) + \theta(\tau_4-\tau_1)\theta(\tau_1-\tau_2)\theta(\tau_2-\tau_3) 
\end{align}$$

Next, we use the trace relation

$$\tr\left(\sigma^{\ell_1}\sigma^{\ell_2}\sigma^{\ell_3}\sigma^{\ell_4}\right)= 2\left(\delta _{\ell_1\ell_2}\delta _{\ell_3 \ell_4} - \delta _{\ell_1\ell_3}\delta _{\ell_2\ell_4}+\delta _{\ell_1\ell_4}\delta _{\ell_2\ell_3}\right)$$

to get 

$$\begin{align}
\langle \Shat^{\ell_1}_0\Shat^{\ell_2}_0\Shat^{\ell_3}_0\Shat^{\ell_4}_0\rangle_0 ={}& 2\left(\delta _{\ell_1\ell_2}\delta _{\ell_3 \ell_4} - \delta _{\ell_1\ell_3}\delta _{\ell_2\ell_4}+\delta _{\ell_1\ell_4}\delta _{\ell_2\ell_3}\right) \\
\langle \Shat^{\ell_1}_0\Shat^{\ell_2}_0\Shat^{\ell_4}_0\Shat^{\ell_3}_0\rangle_0 ={}& 2\left(\delta _{\ell_1\ell_2}\delta _{\ell_3 \ell_4} - \delta _{\ell_1\ell_4}\delta _{\ell_2\ell_3}+\delta _{\ell_1\ell_3}\delta _{\ell_2\ell_4}\right) \\
\langle \Shat^{\ell_1}_0\Shat^{\ell_3}_0\Shat^{\ell_2}_0\Shat^{\ell_4}_0\rangle_0 ={}& 2\left(\delta _{\ell_1\ell_3}\delta _{\ell_2 \ell_4} - \delta _{\ell_1\ell_2}\delta _{\ell_3\ell_4}+\delta _{\ell_1\ell_4}\delta _{\ell_2\ell_3}\right) \\
 \langle \Shat^{\ell_1}_0\Shat^{\ell_3}_0\Shat^{\ell_4}_0\Shat^{\ell_2}_0\rangle_0 ={}& 2\left(\delta _{\ell_1\ell_3}\delta _{\ell_2 \ell_4} - \delta _{\ell_1\ell_4}\delta _{\ell_2\ell_3}+\delta _{\ell_1\ell_2}\delta _{\ell_3\ell_4}\right) \\
\langle \Shat^{\ell_1}_0\Shat^{\ell_4}_0\Shat^{\ell_2}_0\Shat^{\ell_3}_0\rangle_0 ={}& 2\left(\delta _{\ell_1\ell_4}\delta _{\ell_3 \ell_2} - \delta _{\ell_1\ell_2}\delta _{\ell_4\ell_3}+\delta _{\ell_1\ell_3}\delta _{\ell_2\ell_4}\right) \\
\langle \Shat^{\ell_1}_0\Shat^{\ell_4}_0\Shat^{\ell_3}_0\Shat^{\ell_2}_0\rangle_0 ={}& 2\left(\delta _{\ell_1\ell_4}\delta _{\ell_2 \ell_3} - \delta _{\ell_1\ell_3}\delta _{\ell_2\ell_4}+\delta _{\ell_1\ell_2}\delta _{\ell_3\ell_4}\right) 
\end{align}$$

Plugging these in, we find 

$$\begin{align}
\langle T_\tau[\Shat^{\ell_1}_0(\tau_1)\Shat^{\ell_2}_0(\tau_2)\Shat^{\ell_3}_0(\tau_3)\Shat^{\ell_4}_0(\tau_4)]\rangle_0 ={}& f(\tau_1,\tau_2,\tau_3,\tau_4)2\left(\delta _{\ell_1\ell_2}\delta _{\ell_3 \ell_4} - \delta _{\ell_1\ell_3}\delta _{\ell_2\ell_4}+\delta _{\ell_1\ell_4}\delta _{\ell_2\ell_3}\right) \\
&+ f(\tau_1,\tau_2,\tau_4,\tau_3)2\left(\delta _{\ell_1\ell_2}\delta _{\ell_3 \ell_4} - \delta _{\ell_1\ell_4}\delta _{\ell_2\ell_3}+\delta _{\ell_1\ell_3}\delta _{\ell_2\ell_4}\right) \\
&+ f(\tau_1,\tau_3,\tau_2,\tau_4)2\left(\delta _{\ell_1\ell_3}\delta _{\ell_2 \ell_4} - \delta _{\ell_1\ell_2}\delta _{\ell_3\ell_4}+\delta _{\ell_1\ell_4}\delta _{\ell_2\ell_3}\right) \\ \\
&+ f(\tau_1,\tau_3,\tau_4,\tau_2)2\left(\delta _{\ell_1\ell_3}\delta _{\ell_2 \ell_4} - \delta _{\ell_1\ell_4}\delta _{\ell_2\ell_3}+\delta _{\ell_1\ell_2}\delta _{\ell_3\ell_4}\right) \\ \\
&+ f(\tau_1,\tau_4,\tau_2,\tau_3)2\left(\delta _{\ell_1\ell_4}\delta _{\ell_3 \ell_2} - \delta _{\ell_1\ell_2}\delta _{\ell_4\ell_3}+\delta _{\ell_1\ell_3}\delta _{\ell_2\ell_4}\right) \\ \\
&+ f(\tau_1,\tau_4,\tau_3,\tau_2)2\left(\delta _{\ell_1\ell_4}\delta _{\ell_2 \ell_3} - \delta _{\ell_1\ell_3}\delta _{\ell_2\ell_4}+\delta _{\ell_1\ell_2}\delta _{\ell_3\ell_4}\right) 
\end{align}$$

Now collecting like terms, we find 

$$\begin{align}
\langle T_\tau[\Shat^{\ell_1}_0(\tau_1)\Shat^{\ell_2}_0(\tau_2)\Shat^{\ell_3}_0(\tau_3)\Shat^{\ell_4}_0(\tau_4)]\rangle_0 ={}& 2(f(\tau_1,\tau_2,\tau_3,\tau_4) + f(\tau_1,\tau_2,\tau_4,\tau_3) - f(\tau_1,\tau_3,\tau_2,\tau_4) \\
&+ f(\tau_1,\tau_3,\tau_4,\tau_2) - f(\tau_1,\tau_4,\tau_2,\tau_3) + f(\tau_1,\tau_4,\tau_3,\tau_2))\delta_{\ell_1\ell_2}\delta_{\ell_3\ell_4} \\
&+ 2(f(\tau_1,\tau_2,\tau_3,\tau_4) + f(\tau_1,\tau_2,\tau_4,\tau_3) + f(\tau_1,\tau_3,\tau_2,\tau_4) \\
&+ f(\tau_1,\tau_3,\tau_4,\tau_2) + f(\tau_1,\tau_4,\tau_2,\tau_3) - f(\tau_1,\tau_4,\tau_3,\tau_2)) \delta_{\ell_1\ell_3}\delta_{\ell_2\ell_4} \\
&+ 2(f(\tau_1,\tau_2,\tau_3,\tau_4) ) \delta_{\ell_1\ell_4}\delta_{\ell_2\ell_3}
\end{align}$$




It is too tedious 

### Conduction electron self-energy at 5th order

The fifth order contribution is given by


We need to evaluate the following:

$$\begin{align}
\langle T_\tau[\Shat^{\ell_1}_0(\tau_1)\Shat^{\ell_2}_0(\tau_2)\Shat^{\ell_3}_0(\tau_3)\Shat^{\ell_4}_0(\tau_4)\Shat^{\ell_5}_0(\tau_5)]\rangle_0
\end{align}$$

This time, there are 120 possible time-orderings of this. However, when we take advantage of the cyclicity of the trace, there will be \\(4! = 24\\) distinct ways to arrange the spin operators. This is because we can think of always moving the 5th one to the end, and the other ones have any possible order. 



Then, we use the trace relation 

$$\begin{align}
\tr(\sigma^a\sigma^b\sigma^c\sigma^d\sigma^e) ={}& \tr(\sigma^a\sigma^b\sigma^c(\delta_{de}\sigma^0 + i\epsilon_{def}\sigma^f)) \\
={}& \delta_{de}\tr(\sigma^a\sigma^b\sigma^c) + i\epsilon_{def}\tr(\sigma^a\sigma^b\sigma^c\sigma^f) \\
={}& 2i\epsilon_{abc}\delta_{de} + 2i\epsilon_{def}(\delta_{ab}\delta_{cf} - \delta_{ac}\delta_{bf} + \delta_{af}\delta_{bc}) \\ 
={}& 2i\epsilon_{abc}\delta_{de} + 2i\delta_{ab}\epsilon_{dec} - 2i\epsilon_{deb}\delta_{ac} + 2i\epsilon_{dea}\delta_{bc} \\ 
={}& 2i(\epsilon_{abc}\delta_{de} + \delta_{ab}\epsilon_{cde} - \epsilon_{deb}\delta_{ac} + \epsilon_{dea}\delta_{bc})
\end{align}$$

### Conduction electron self-energy at 6th order

Finally, we consider the 6th order contribution to the self-energy. The spin correlator is given by 

$$\begin{align}
\langle T_\tau[\Shat^{\ell_1}_0(\tau_1)\Shat^{\ell_2}_0(\tau_2)\Shat^{\ell_3}_0(\tau_3)\Shat^{\ell_4}_0(\tau_4)\Shat^{\ell_5}_0(\tau_5)\Shat^{\ell_6}_0(\tau_6)]\rangle_0
\end{align}$$

If we evaluate the 6-Pauli matrix trace, we find that

$$\begin{align}
\tr(\sigma^a\sigma^b\sigma^c\sigma^d\sigma^e\sigma^f) ={}& \tr(\sigma^a\sigma^b\sigma^c\sigma^d(\delta_{ef}\sigma^0 + i\epsilon_{efg}\sigma^g)) \\
={}& \delta_{ef}\tr(\sigma^a\sigma^b\sigma^c\sigma^d) + i\epsilon_{efg} \tr(\sigma^a\sigma^b\sigma^c\sigma^d\sigma^g) \\
={}& 2\left(\delta _{ab}\delta _{cd} - \delta _{ac}\delta _{bd}+\delta _{ad}\delta _{bc}\right)\delta_{ef} + i\epsilon_{efg}2i(\epsilon_{abc}\delta_{de} + \delta_{ab}\epsilon_{cde} - \epsilon_{deb}\delta_{ac} + \epsilon_{dea}\delta_{bc}) \\
={}& 2\left(\delta _{ab}\delta _{cd} - \delta _{ac}\delta _{bd}+\delta _{ad}\delta _{bc}\right)\delta_{ef} - 2\epsilon_{efg}(\epsilon_{abc}\delta_{dg} + \delta_{ab}\epsilon_{cdg} - \epsilon_{dgb}\delta_{ac} + \epsilon_{dga}\delta_{bc})
\end{align}$$

To simplify this, we can use the formula 

$$\begin{align}
\tr(\sigma^a\sigma^b\sigma^c\sigma^d\sigma^e\sigma^f) ={}& 2\left(\delta _{ab}\delta _{cd} - \delta _{ac}\delta _{bd}+\delta _{ad}\delta _{bc}\right)\delta_{ef} - 2\epsilon_{efg}(\epsilon_{abc}\delta_{dg} + \delta_{ab}\epsilon_{cdg} - \epsilon_{dgb}\delta_{ac} + \epsilon_{dga}\delta_{bc})
\end{align}$$


