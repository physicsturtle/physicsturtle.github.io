---
layout: page
title: Adiabatic Processes
course: test
unit: unit1
permalink: /test/adiabatic-process/
---

An adiabatic process is one in which no heat is transferred in or out of the system, so $dQ = 0$ for an adiabatic process. We can from this derive a few interesting properties of these systems. 
Starting with the first law of thermodynamics 

$$dU = dQ - dW$$

we can simplify to make

$$dU = -PdV$$

the change in internal energy is always $dU = nC_V dT$, so we get 

$$nC_VdT = -PdV$$

which can be integrated to find some interesting relationships. 

$$\begin{eqnarray}
nC_V dT &=& -P dV\\
nC_V dT &=& -\frac{nRT}{V} dV\\
\frac{C_V}{T} dT &=& - \frac{C_P - C_V}{V} dV\\
\int \frac{1}{T} dT &=& - \int \frac{C_P/C_V - 1}{V} dV\\
\ln T &=& - (\gamma - 1)\ln V + C\\
T &=& V^{1-\gamma}C\\
TV^{\gamma - 1} &=& C\\
\end{eqnarray}$$

which tells that, throughout an adiabatic process, the quantity $TV^{\gamma - 1}$ stays constant. In other words, 

$$T_iV_i^{\gamma - 1}  = T_fV_f^{\gamma - 1}. $$

Through the ideal gas law, we can also write 

$$\begin{eqnarray}
\frac{PV}{nR}V^{\gamma - 1} &=& C\\
PV^{\gamma} &=& C\\
\end{eqnarray}$$

this value of $C$ has absorbed the $nR$. This second equation is true only in the case that the number of moles of gas stay constant, while the first one can have an addition of gas to the system. Note that this constant $C$ is not the same as the constant $C$ from the first equation. This result also implies that 

$$P_iV_i^{\gamma}  = P_fV_f^{\gamma}. $$

Now, let's find the work done during an adiabatic process. We have that 

$$dW = P dV$$

and during an adiabatic process, we $PV^{\gamma} = C$. Then let's integrate the formula for work to find:

$$\begin{eqnarray}
W &=& \int_{V_1}^{V_2} P dV\\
&=& \int_{V_1}^{V_2} CV^{-\gamma} dV\\
&=& \frac{C}{1-\gamma}\left( V_2^{1-\gamma} - V_1^{1-\gamma}\right)
\end{eqnarray}$$

where $C = P_1 V_1^\gamma = P_2 V_2^\gamma$. (one could even use values for $P$ and $V$ that happen any time during the adiabatic process)













