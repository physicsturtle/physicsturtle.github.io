---
layout: exercises
title: Spin Density Wave Order  - Exercises
dept: physics
course: many-body-II
unit: unit10
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 10
---
<ol>
<li> <div class="exercise">  Evaluate the quantity 
$$\begin{equation}
\frac{1}{\beta}\sum_{ip_0} \mathcal{G}_0(k+p)\mathcal{G}_0(p),
\end{equation}$$

and recall that 
$$\begin{equation}
\mathcal{G}_0(p) = \mathcal{G}_0(\p, ip_0) = \frac{1}{ip_0 - \xi_{\p}}
\end{equation}$$

<div class="answerBox"> 
 <button onclick="myFunction('answer11')" class="answerButton">Show Answer</button> 
 <div  id='answer11' class="answer" >

Thus the final result is given by
$$\begin{equation}
\frac{1}{\beta}\sum_{ip_0}\mathcal{G}_0(k+p)\mathcal{G}_0(p) = \frac{n_F(\xi_{\p}) - n_F(\xi_{\p+\k})}{ik_0 + \xi_{\p} - \xi_{\p+\k}}
\end{equation}$$
</div> 
 </div>

</div> </li>
<li> <div class="exercise">  Itinerant electron ferromagnetism is a special case of a spin-density wave. 
<ol type="a">
<li> What is the ordering vector \(\k\) for ferromagnetism?
</li>
<li> Does this model have a ferromagnetic transition at temperature \(T_C\) for any value of the parameters \(U\), \(\mu\), \(t\)? If so, what is \(T_C\)?
</li></ol>

<div class="answerBox"> 
 <button onclick="myFunction('answer25')" class="answerButton">Show Answer</button> 
 <div  id='answer25' class="answer" >
Clearly, if \(k_0\neq 0\), then there is no solution to the equation 

\(\)\frac{3}{U} + \frac{2}{N}\sum_{\p}\frac{n_F(\xi_{\p}) - n_F(\xi_{\p+\k})}{ik_0 + \xi_{\p} - \xi_{\p+\k}} = 0.\(\)

for \(\k=0\). If however we set \(k_0 = 0\), then we end up with a \(0/0\) situation. We set \(k_0 = 0\) and then take a limit \(\k\to 0\). Doing this, we find that 
</div> 
 </div>

</div> </li>
<li> <div class="exercise">  Determine how the correlation functions \(\langle \mathbf{m}_{i\tau} \cdot \mathbf{m}_{j\tau'} \rangle\) and \(\langle(\bar{c}_{j\tau'\sigma} \boldsymbol{\sigma}_{\alpha\beta} c_{j\tau'\beta})\cdot (\bar{c}_{i\tau\sigma} \boldsymbol{\sigma}_{\alpha\beta} c_{i\tau\beta})\rangle\) are related.

<div class="answerBox"> 
 <button onclick="myFunction('answer35')" class="answerButton">Show Answer</button> 
 <div  id='answer35' class="answer" >
Consider the partition function which is 

$$\begin{equation}
Z = \int e^{-S} \D[\bar{c},c]\D\mathbf{m}
\end{equation}$$

and the action is \(S = S_0 + S_\text{int}\):

$$\begin{equation}
S_0 = \sum_{k\sigma}\bar{c}_{k\sigma}(-ik_0+\xi_{\k})c_{k\sigma},\quad S_{\text{int}} = \frac{3}{2U\beta N}\sum_k \mathbf{m}_k \cdot\mathbf{m}_{-k} - \frac{1}{\beta N}\sum_{kp\alpha\beta} \mathbf{m}_k\cdot \bar{c}_{k+p,\alpha}\boldsymbol{\sigma}_{\alpha\beta}c_{p\beta}.
\end{equation}$$

To show this, let's introduce an additional term in the action 

$$\begin{equation}
S_{J} = -\int_0^\beta \mathbf{J}_{i\tau} \cdot \mathbf{m}_{i\tau} \d\tau
\end{equation}$$

so that the partition function becomes 

$$\begin{equation}
Z[\mathbf{J}] = \int e^{-S - S_J} \D[\bar{c},c]\D\mathbf{m}
\end{equation}$$

Then, we have that 

$$\begin{equation}
\langle \mathbf{m}_{i\tau} \cdot \mathbf{m}_{j\tau'} \rangle = \sum_{a=1}^3 \frac{1}{Z[\mathbf{J}]}\frac{\delta}{\delta J_{i\tau}^a}\frac{\delta}{\delta J_{j\tau'}^{a}} Z[\mathbf{J}]\bigg|_{\mathbf{J} = 0}
\end{equation}$$

Alternatively, we can integrate over the \(\mathbf{m}\) fields first. This will generate a coupling between \(\mathbf{J}\) and the fermions. We recall that the interacting part of the action can also be rewritten as 

$$\begin{equation}
S_\text{int} = \int_0^\beta\left(\frac{3}{2U}\sum_i |\mathbf{m}_{i\tau}|^2 - \sum_{i\alpha\beta} \mathbf{m}_{i\tau} \bar{c}_{i\tau\alpha} \boldsymbol{\sigma}_{\alpha\beta} c_{i\tau\beta}\right)\d\tau
\end{equation}$$

Then, we need to evaluate the integral 

$$\begin{equation}
\int \exp\left(-\int_0^\beta\left(\frac{3}{2U}|\mathbf{m}_{i\tau}|^2 - \mathbf{m}_{i\tau}\cdot\left(\mathbf{J}_{i\tau} + \bar{c}_{i\tau\alpha} \boldsymbol{\sigma}_{\alpha\beta} c_{i\tau\beta}\right)\right)\d\tau \right)\D\mathbf{m} = \exp\left(\int_0^\beta \frac{U}{6} \sum_i (\mathbf{J}_{i\tau} + \bar{c}_{i\tau\alpha} \boldsymbol{\sigma}_{\alpha\beta} c_{i\tau\beta})^2 \d\tau \right)
\end{equation}$$

Thus, we have that the partition function is

\(\)Z[\mathbf{J}] = \int \exp\left(\int_0^\beta \left(\sum_{\k} \bar{c}_{\k\tau\sigma}(\partial_\tau + \xi_{\k}) c_{\k\tau\sigma} - \frac{U}{6}\sum_i (\mathbf{J}_{i\tau} + \bar{c}_{i\tau\alpha} \boldsymbol{\sigma}_{\alpha\beta} c_{i\tau\beta})^2 \d\tau \right)\right)\(\)

Then, taking the derivatives with respect to \(J\) as before, we have that 

$$\begin{align}
\sum_{a=1}^3 \frac{1}{Z[\mathbf{J}]} \frac{\delta}{\delta J^a_{i\tau}} \frac{\delta}{\delta J^a_{j\tau'}} Z[\mathbf{J}] \bigg|_{\mathbf{J} = 0} ={}& \sum_{a=1}^3 \frac{1}{Z[\mathbf{J}]} \frac{\delta}{\delta J^a_{i\tau}} \int \left(-\frac{U}{3} (J^a_{j\tau'} + \bar{c}_{j\tau'\sigma} \sigma^a_{\alpha\beta} c_{j\tau'\beta}) \right) e^{-S} \D[\bar{c},c] \\
={}& \sum_{a=1}^3 \frac{1}{Z[\mathbf{J}]} \left[ \frac{U^2}{9} \int \left( (J^a_{j\tau'} + \bar{c}_{j\tau'\sigma} \sigma^a_{\alpha\beta} c_{j\tau'\beta})(J^a_{i\tau} + \bar{c}_{i\tau\sigma} \sigma^a_{\alpha\beta} c_{i\tau\beta}) \right) e^{-S} \D[\bar{c},c] \right. \\
&\left. -\frac{U}{3} \int \delta_{ij}\delta(\tau-\tau') e^{-S}\D[\bar{c},c] \right]\bigg|_{\mathbf{J} = 0} \\
={}& \sum_{a=1}^3 \frac{1}{Z} \left[ \frac{U^2}{9} \int (\bar{c}_{j\tau'\sigma} \sigma^a_{\alpha\beta} c_{j\tau'\beta}) (\bar{c}_{i\tau\sigma} \sigma^a_{\alpha\beta} c_{i\tau\beta}) e^{-S} \D[\bar{c},c] -\frac{U}{3} Z\delta_{ij}\delta(\tau-\tau') \right] \\
={}& \frac{U^2}{9}\langle(\bar{c}_{j\tau'\sigma} \boldsymbol{\sigma}_{\alpha\beta} c_{j\tau'\beta})\cdot (\bar{c}_{i\tau\sigma} \boldsymbol{\sigma}_{\alpha\beta} c_{i\tau\beta})\rangle - U \delta_{ij}\delta(\tau-\tau')
\end{align}$$

Thus, we find that 

\(\)\langle \mathbf{m}_{i\tau} \cdot \mathbf{m}_{j\tau'}\rangle = \frac{U^2}{9}\langle(\bar{c}_{j\tau'\sigma} \boldsymbol{\sigma}_{\alpha\beta} c_{j\tau'\beta})\cdot (\bar{c}_{i\tau\sigma} \boldsymbol{\sigma}_{\alpha\beta} c_{i\tau\beta})\rangle - U \delta_{ij}\delta(\tau-\tau')\(\)

where the correlation function on the left hand side is taken with respect to the partition function where we have the Hubbard-Stratonovich field, and the correlation function on the left hand side is the one where we only have a fermionic action. 
</div> 
 </div>

</div> </li></ol>


