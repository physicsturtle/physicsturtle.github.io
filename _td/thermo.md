---
layout: page
title: thermo
course: td
unit: unit1
---

We consider a system and construct the conservation of energy. In a physical system, there are different ways to add energy to it. The energy $E$ in a system does not have a general formula. However, we can find a formula for the change in energy in a system due to changes in thermodynamic quantities. The change in energy is

$$dE = TdS - PdV + \mu dN.$$

In multivariable calculus, taking the differential of a function leads to a sum in terms of differentials of the independent variables. This tells us then that $E = E(S,V,N)$, and that

$$T = \frac{\partial E}{\partial S}\bigg|_{V,N},\qquad -P = \frac{\partial E}{\partial V}\bigg|_{S,N},\qquad \mu = \frac{\partial E}{\partial N}\bigg|_{S,V}.$$

If we define $F = E - TS$, then taking the differential leads to  

$$\begin{eqnarray*}

dF &=& dE - d(TS)\\

&=& (TdS - PdV + \mu dN) - (TdS + SdT) \\

&=& -SdT - PdV + \mu dN

\end{eqnarray*}$$

This means that we can change $E$ from being a function of $S$ into being a function of $T$. 

$$d(E-TS) = -SdT - PdV + \mu dN$$

Thus, 

$$\begin{eqnarray*}

-S &=& \frac{\partial}{\partial T}\bigg|_{V,N}(E - TS) \\

&=& \frac{\partial E}{\partial T}\bigg|_{V,N} - \frac{\partial(TS)}{\partial T}\bigg|_{V,N} \\

&=& \frac{\partial E}{\partial T}\bigg|_{V,N} - S - T\frac{\partial S}{\partial T}\bigg|_{V,N}

\end{eqnarray*}$$



