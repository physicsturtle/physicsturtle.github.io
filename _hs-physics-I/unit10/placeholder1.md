---
layout: lesson
title: Events and Inertial Reference Frames
course: calculus-III
unit: unit1
---

### Introduction
In special relativity, it is very important to understand the idea that different observers will have different notions of time and space. The first step to understanding this concept is looking at events and inertial reference frames.

<div class="definition">
<b> Definition</b>: An <i>inertial reference frame</i> is one which is not accelerating.
</div>
Examples:
\begin{itemize}
\item the reference frame of a car going quickly around a curve is non-inertial, because the car is experiencing an acceleration because its direction is changing. 
\item The frame of a person sitting at a desk is inertial because they are not moving and thus not accelerating
\item The frame of a runner moving at constant velocity is inertial because they are not accelerating
\end{itemize}

\textbf{Definition}: An event is a point in space-time, that is, a point in space at a certain time. A point in space-time is denoted by $(t,x)$, a time, and a place. 

\textbf{Remark}: In two distinct reference frames, the coordinates of a particular event will \textit{not} be the same. \\

There are two postulates of special relativity, from which all laws of the theory can be derived. They are:
\begin{itemize}
\item The laws of physics are the same in all inertial reference frames. That is, Newton's laws hold in all inertial reference frames.
\item The speed of light has the same value in all inertial reference frames, no matter the velocity of any observer or the source of the light.
\end{itemize}

A consequences of these two postulates is that two events which may be simultaneous in one observer's frame may not be simultaneous in another observers frame. Similarly, two events which may be at the same place in one observer's frame may not be at the same place in another observer's frame. 

\textbf{Definition}: If you measure the time between two events in the frame in which two events occur at the same position, then this time is called the \textit{proper time}, and it is the shortest time that one can observe between the two events.

\textbf{Definition}: If you measure the distance between two events in the frame in which two events occur simultaneously, then this length is called the \textit{proper length}, and is the longest length that one can observe between the two events.

\textbf{Time Dilation}: Suppose the time interval measured between two events is $t$ in some reference frame. Now, suppose we have another reference frame moving at speed $v$ with respect to the first reference frame. The time interval measured between the two events in the second reference frame is 
$$t' = \frac{t}{\sqrt{1-v^2/c^2}}$$

\textbf{Length Contraction}: Suppose the distance measured between two events is $\ell$ in some reference frame. Now, suppose we have another reference frame moving at speed $v$ with respect to the first reference frame. The time interval measured between the two events in the second reference frame is 
$$\ell' = \ell\sqrt{1-v^2/c^2}$$

\textbf{Velocity Addition}: Suppose $v_{AB}$ is the velocity of $A$ relative to $B$, $v_{AC}$ is the velocity of $A$ relative to $C$, and $v_{BC}$ is the velocity of $B$ relative to $C$. Then, 

$$v_{AB} = \frac{v_{AC} + v_{CB}}{1+v_{AC}v_{CB}/c^2}$$


\newpage
\begin{questions}
\question The speed of light in water is $v = 2.25\times 10^8$ m/s. If an object moves at $2.7\times 10^8$ m/s in water, does this violate any postulates of special relativity?

\begin{solution}
No. The absolute speed of the universe is $c$, the speed of light in a vacuum.
\end{solution}

\question When radiation hits Earth's upper atmosphere, muons are created. The lifetime of a muon is $2.2\si{\mu s}$ in its own reference frame. If the muons are created at 15 km above Earth's surface, at what speed do the muons need to travel to reach the Earth's surface before decaying?

\begin{solution}
Our two events are the muon's creation, and the muon hitting the Earth. We know that the distance travelled in the Earth's frame is 15 km, and the time traversed in the muon's frame is 2.2 \si{\mu s}. Since relative velocity is the same in all reference frames, $\Delta \ell_E /\Delta t_E = v = \Delta \ell_m/\Delta t_m$. The proper time is the time measured by the muon because, from its reference frame, both events occur at the same location. 


\end{solution}

\end{questions}



### Exercises
<ol> 
<li><div> Plot the points $P = (2,-1,2)$, $Q = (-3,-3,1)$, and $R = (0,2,-1)$ on a 3D Cartesian coordinate system. </div>

<button onclick="myFunction('answer1')" class="answerButton">Show Answer</button>
<div  id="answer1" class="answer">
To plot these points, we should draw lines from each of the axes to show where the points are. Without these lines, it could be ambiguous where points are. 

<figure class="center">
<p><img src="three-dimensional-cartesian-coordinates-Figures/q1Sol.svg" alt="Three Dimensional Coordinates" style="width:300px;height:300px;"> </p> </figure>
</div> </li>

</ol>

<!---
<li> <div> Sketch all of the points such that $y = 1$. </div>

<button onclick="myFunction('answer2')" class="answerButton">Show Answer</button>
<div  id="answer2" class="answer">
This is a plane that is parallel to the \(xz\) plane. 
</div> </li>
<li> <div> Sketch the region where $x^2 < 1$. </div>

<button onclick="myFunction('answer3')" class="answerButton">Show Answer</button>
<div  id="answer3" class="answer">
This is a plane that is parallel to the $xz$ plane. 
</div> </li>

<li> <div> Sketch the region where $y^2 + z^2 < 4$ </div>

<button onclick="myFunction('answer4')" class="answerButton">Show Answer</button>
<div  id="answer4" class="answer">
This is a plane that is parallel to the $xz$ plane. 
</div> </li>

<li> <div> Sketch the region where $xy > 0$ </div>

<button onclick="myFunction('answer5')" class="answerButton">Show Answer</button>
<div  id="answer5" class="answer">
This is a plane that is parallel to the \(xz\) plane. 
</div> </li>
<li> <div> Sketch the set where \(z^2 = 4\) </div>

<button onclick="myFunction('answer6')" class="answerButton">Show Answer</button>
<div  id="answer6" class="answer">
This is a plane that is parallel to the \(xz\) plane. 
</div> </li>
--->
