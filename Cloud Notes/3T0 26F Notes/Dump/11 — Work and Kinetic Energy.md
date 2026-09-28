---
updated_at: 2026-09-27T21:20:20.083-04:00
edited_seconds: 610
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
Next: N/A

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
Where $k$ is some material component, and $x$ is some displacement from the baseline. Note that this is a linear force (so we can use our simplified integral). If we wanted to solve for the linear elastic energy present in a spring; recall our definition from above: 
$$\begin{align}W_{AB} = \underset{\text{path AB}}{\int }\vec{F}\cdot d\vec{r} \\\end{align}$$
In this case, $\vec{F} = -kx$, and $d\vec{r}$ is equivalent to the path length, or *displacement* experienced by our spring, some term $dx$, therefore: 
$$
\begin{align}
W_{E} &= \int_{A}^B-kx\ dx \\
&= -k \int_{A}^Bx \ dx \\
&=-k\left[\right]
\end{align}

$$