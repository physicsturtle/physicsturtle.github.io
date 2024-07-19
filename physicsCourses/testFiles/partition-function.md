---
layout: page
title: Partition Function
course: test
unit: unit1
permalink: /test/partition-function/
---

The partition function is the sum of all the Boltzmann factors. if $E(s)$ is the energy of microstate $s$, then the Boltzmann factor is 

$$e^{-E(s)/kT}$$

and the partition function is the sum of all of the Boltzmann factors.

$$Z = \sum_s e^{-E(s)/kT}$$

The probability of measuring the system in state $s$ is given by 

$$P(s) = \frac{1}{Z}e^{-E(s)/kT}$$

<div class="example">
<p><b>Example:</b> Calculate the partition function of the quantum harmonic oscillator. </p>
<b>Solution:</b> To calculate the partition function, we need to sum over the Boltzmann factors of all the energies. This amounts to
$$Z(\beta) = \sum_{n=0}^\infty e^{-\beta\omega\hbar(n+1/2)}.$$
This can be rewritten in the following way:
$$Z(\beta) = e^{-\beta\hbar\omega/2} \sum_{n=0}^\infty \left(e^{-\beta\omega\hbar}\right)^n.$$
This suggests the use of the geometric series formula.
$$Z(\beta) = \frac{e^{-\beta\hbar\omega/2}}{1-e^{-\beta\hbar\omega}}.$$


</div>


