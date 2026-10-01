---
updated_at: 2026-10-01T16:17:08.777-04:00
edited_seconds: 1170
course: PHY180H1
tags:
  - PHY180H1
  - TBF
"Lecture #": 11
Lecture Date: 2026-10-02
Week: 4
Created: September 23rd 2026, 10:02:18 pm
---
Hub: [[PHY180 Hub]]
Previous: [[10 — Drag Force and Terminal Velocity]]
Next: [[12 — Potential Energy, Conservative and Non-Conservative Forces]]

> [!quote] Recommended Reading 
> 7.1-7.4
--- 
# Lecture Notes
# Pre-Lecture Notes
## Work 
Work is generally defined as the integral of the path of a force with respect to it's displacement. To begin, we can define the definition of an infinitesimally small amount of work: 
$$dW = \vec{F} \cdot d\vec{r} = |\vec{F}||d\vec{r}|\cos\theta$$
Note, $\vec{r}$ is the terms of our relative path length, and $\vec{F}$ is the terms of force applied onto our object. Work is generally defined as a term of $[N\cdot m] =[J]$. 
$$W_{AB} = \underset{\text{path AB}}{\int }\vec{F}\cdot d\vec{r}$$
Where $\vec{F}$ could vary along the path, and where $d\vec{r}$ can also vary along the general path length. 
### Constant Forces & Work
Note that if $\vec{F} = \bar{F} = F$, that is force is some constant value; the above integral evaluates as the following: 
$$
\begin{align}
W_{AB} &= \underset{\text{Path AB}}{\int}\vec{F} \cdot d\vec{r}  = \underset{\text{Path AB}}{\int}dW\\
&= \vec{F}\underset{\text{Path AB}}{\int}d\vec{r}  \\
&= \vec{F}\cdot(\vec{r}_{B}-\vec{r}_{A}) \\
&= |\vec{F}||\vec{r}_{b} - \vec{r}_{a}|\cos\theta
\end{align}
$$
With $\vec{r}_{b}-\vec{r}_{a}$ of the path of $AB$, this generally approximates the vector $\vec{d}$; therefore
$$
=|\vec{F}||\vec{d}|\cos\theta
$$
Or, without vector notation: 
$$
W=Fd\cos\theta
$$
### Non-Constant Forces & Work 
In general for non-constant forces which vary over some distance; it may help to show them as a function of their components. Recall that we defined force in the direction of it's path as the following: 
$$
dW = \vec{F}\cdot d\vec{r}
$$
If we take this to it's component form; then: 
$$
dW = F_{x}dx + F_{y}dy + F_{z}dz
$$
Where $F_{x},F_{y},F_{z}$ are the relative components of some force vector $F$. 
Note then that if we are given the formula for some work; we can sub in and differentiate corresponding statements of $x,y,z\to dx,dy,dz$ to sub into this equation. We normally want to get these all to some evaluable term e.g. $dx$ to take the definite integral of. 
### Hooke's Law & Elastic Energy
Hooke's Law is defined as the following: 
$$
F_{E} = -kx
$$
Where $k$ is some material component (in terms of $\frac{F}{D}$ or commonly, $\frac{N}{m}$), and $x$ is some displacement from the baseline. Note that this is a linear force (so we can use our simplified integral). If we wanted to solve for the linear elastic energy present in a spring; recall our definition from above: 
$$\begin{align}W_{AB} = \underset{\text{path AB}}{\int }\vec{F}\cdot d\vec{r} \\\end{align}$$
In this case, $\vec{F} = -kx$, and $d\vec{r}$ is equivalent to the path length, or *displacement* experienced by our spring, some term $dx$, therefore: 
$$
\begin{align}
W_{E} &= \int_{A}^B-kx\ dx \\
&= -k \int_{A}^Bx \ dx \\
&=-k\left[\frac{1}{2}x_{b}^2-\frac{1}{2}x_{a}^2\right] \\
W_{E}&= -\frac{k}{2}[x_{b}^2 - x_{a}^2]
\end{align}$$
## Kinetic Energy 
Kinetic Energy is generally defined as the following: 
>[!theorem] Kinetic Energy
> $$K = \frac{1}{2}mv^2$$
> Note that $K$ can sometimes be notated as $E_{K}$; this is in terms of Joules. Note that $p=mv \to v=\frac{p}{m}$, which means that this can be rewritten as: 
> $$K = \frac{mp^2}{2m^2} = \frac{p^2}{2m}$$

Note however that $v$, like other values, are based off a certain reference frame. Refer to [[6 — Rotational Kinematics#]] and [[7 — 1st and 2nd Laws of Newton#Newton's First Law|Newton's First Law (PHY180-7)]] for a brief review on this. 
## Work-Energy Theorem 
The Work-Energy Theorem states that the Net Work of a system is equivalent to a change in it's kinetic energy. Let us retake the definition of work to show how this is true: 
$$
\begin{align}
dW &= \vec{F} \cdot d\vec{r} & \text{Note, }\vec{F} = m\frac{d\vec{v}}{dt} \\
&= m\frac{d\vec{v}}{dt} \cdot d\vec{r} & \\
&=md\vec{v} \cdot \frac{d\vec{r}}{dt} & \text{Note, } \frac{d\vec{r}}{dt} = d\vec{v} \\
&=md\vec{v} \cdot d\vec{v} & md\vec{v} \to m\vec{v} \\
&=m\vec{v}\cdot d\vec{v}
\end{align}
$$
I personally (Aries) am not that familiar yet with integration of vectors; we can break this up into it's component form: 
$$
\begin{align}
dW &= mv_{x}dv_{x} + mv_{y}dv_{y} + mv_{z}dv_{z} = m\left[v_{x}dv_{x} + v_{y}dv_{y} + v_{z}dv_{z}\right] \\
W_{net}=\int_{A}^BdW &= \int_{A}^Bm\left[v_{x}dv_{x} + v_{y}dv_{y} + v_{z}dv_{z}\right] & \\
&=\left[\frac{m}{2}v_{x}^2 + \frac{m}{2}v_{y}^2 + \frac{m}{2}v_{x}^2\right]^B_{A} \\
&= \left[\frac{m}{2}v_{x}^2 + \frac{m}{2}v_{y}^2 +\frac{m}{2}v_{z}^2\right]^B_{A} = [\frac{m}{2}v^2]^B_{A} &v_{x}^2 + v_{y}^2 +v_{z}^2 = v^2\\
W_{net}&=K_{B}-K_{A} = \Delta K
\end{align}
$$
What this means is that for instance, if Work is *negative*, then the kinetic energy of our object will proportionally decrease. 
## Power 
Power is generally defined as some term of Energy over time, that is: 
$$P_{av} = \frac{W}{t}$$
This is often notated in the term of a $W$ (Watt), where $1W = \frac{1J}{s}$; $W$ in this context can be defined as the non-instantaneous form of $\vec{F}\cdot \vec{d}$ or $|\vec{F}||\vec{d}|\cos\theta$. 

> [!theorem] Instantaneous Power
> Instantaneous power is defined as the following: 
> $$P = \frac{dW}{dt}$$
> Note that this can also be expressed as: $$\begin{align}P&= \frac{dW}{dt}& dW = \vec{F} \cdot d\vec{v} \\&= \frac{\vec{F}\cdot d\vec{r}}{dt} \\&= \vec{F} \cdot \frac{d\vec{r}}{dt} \\&=\vec{F} \cdot \vec{v}\end{align}$$

Note that if $P$ is constant for some time interval $dt$, then we can say that: 
$$
\begin{align}
Pdt &= dW \\
\int Pdt &= \int dW  \\ \\
Pt&=W\end{align}$$
That is to say, that if $P$ is constant, the net work is defined as the area under the Power curve with respects to time. 