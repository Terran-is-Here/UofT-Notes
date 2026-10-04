---
updated_at: 2026-10-03T23:29:10.335-04:00
edited_seconds: 1410
course: PHY180H1
tags:
  - PHY180H1
"Lecture #": 12
Lecture Date: 2026-09-27
Week: 5
Created: September 27th 2026, 10:01:18 pm
---
Hub: [[PHY180 Hub]]
Previous: [[11 — Work and Kinetic Energy]]
Next: N/A 
> [!quote] Recommended Reading 
> University Physics 8.1-8.2
--- 
# Lecture Notes


---
# Pre-Lecture Notes
## Gravitational Potential Energy
The concept of gravitational potential energy is roughly defined as: $$mgh = E_{PG}$$where $m$ stands for mass, $g$ stands for gravity and $h$ stands for the height of the body. 

Taking a $1d$ kinematic example; when we shoot a ball from the surface upwards with a speed of $v$, then it's corresponding energy is defined as: 
$$
E_{T}= \frac{1}{2}mv^2
$$
When it reaches the *top* of it's trajectory, all of it's energy is defined as
$$
E_{T} = E_{PG}= mgh
$$
Note that since gravity works *against* the direction of upwards motion; then we can say that it did negative work on our object. Taking $E_{PG0}$ as the gravitational potential energy at $t=0$, and $E_{PGt}$ at $t=t$ at the apex; then: 
$$
\Delta E_{PG} = E_{PGt} - E_{PG0} = -W
$$
Recall that we defined $W=\Delta E_{K}$, then $\Delta E_{PG} = -\Delta E_{EK}$ or $\Delta E_{EK} = -\Delta E_{PG}$; that is to say that the change of kinetic energy is equal to the negative gravitational potential energy. This applies for any potential energy: 

> [!theorem] Potential Energy
> $$\Delta E_{P} = -\Delta E_{K}$$
> Where $\Delta E_{P}$ is any potential energy, and $\Delta E_{K}$ is the change in kinetic energy. 
> > In the textbook, potential energy is normally notated as some $\Delta U$. This is the convention we will share for the remainder of this note packet. 

Note that for Gravitational Potential Energy, whatever we define $h$ as, is arbitrary. We normally define it as the surface, or any medium that makes it convenient for the sake of analysis. 

> [!axiom] Potential Energy Integration
> Recall that we defined work as the following: 
> $$W = \int_{A}^B\vec{F}\cdot d\vec{r}$$
> But from our earlier definition above; then: 
> $$\Delta U = -W = -\underset{\text{Path AB}}{\int_{A}^B}\vec{F}\cdot d\vec{r}$$
> Note that since $\Delta U$ is some value based off an integral, during the cases where we have an indefinite integral; our $+C$ value represents the initial potential energy already present within the system. 

## Potential Energy
Generally for any potential energy, at least from how we define it, the difference in potential energy is normally directly linked to work (as per the statement above). This flows more generally into the general principle of the conservation of energy. 

> Elastic Potential Energy
> Recall in [[11 — Work and Kinetic Energy#Hooke's Law & Elastic Energy|PHY180 (11) - Hooke's Law]] that we derived the work from Hooke's law from the following: 
> $$\begin{align}dW &= \int_{A}^B \vec{F}\cdot d\vec{v} \\&= \int_{A}^B-kx \cdot dx = \left[-\frac{1}{2}kx^2\right]^B_{A} \\W_{E}&=-\frac{1}{2}k(x_{B}^2-x_{A}^2)\end{align}$$Then: $$\begin{align}\Delta U_{E} &= -W_{E} = \frac{1}{2}k(x_{B}^2-x_{A}^2) & \text{ Setting } x_{A} = 0 \text{ for starting position} \\&= \frac{1}{2}kx^2\end{align}$$

### Multiple Potential Energies
Given cases in which multiple potential energies exist, assuming energy conservation exists, then the following will always hold true: 
$$
E_{K} + \Sigma U =E_{M} \text{ Where } E_{M} \text{ is our system's total energy.}
$$
$E_{M}$ can be defined from a case by case basis. For instance, take the following example from the textbook: 

> Assume that a spring system is affected by gravity. Assume that this spring at it's initial position is also in it's equilibrium position, that is $x=0$ in $\frac{1}{2}kx^2$. Then: 
> > We can define our gravitational potential energy's relevant baseline at the peak of this spring, that is $y=0$, and at this point by convention with $mgy_{a} = mg(0) = 0$, then this point has no relevant gravitational potential energy.  
> > Denote this point $y_{A}$. At this point, $E_{K}=0$.
> 
> From here, note at the lowest point of this spring / it's maximum deformation (some value $y_{B}$), $E_{K}$ is momentarily 0 at this point, as our object's velocity drops to 0. Then: 
> $$E_{KA}+ U_{A} = E_{KB} + U_{B}$$
> Since $E_{KA},E_{KB} = 0$, and $U_{A}=0$ (as $y=0$), and $U_{B} = U_{E} + U_{G}$, then: $$\begin{align}0 &= U_{E} + U_{G} \\0 &= \frac{1}{2}ky_{B}^2 + mgy_{B} \\y_{B} &=-\frac{2mg}{k}\end{align}$$
> Where $y_{b}$ would then be the value of the maximum stretch deformation of our spring. 

## Conservative and Non-Conservative Forces
Recall that our earlier definition of Work: 
$$\begin{align}
dW&=\vec{F}\cdot d\vec{r}\\
W&=\underset{\text{Path AB}}{\int_{A}^B}\vec{F}\cdot d\vec{r}
\end{align}$$
Where our integral is a path integral of all possible paths taken. We now define the concept of a conservative and a non-conservative force: 

> Conservative Forces 
> The work done by a *conservative force* is independent of the path; that is it is a state function. The work done by a conservative force is the same for *any* path connecting two points $AB$: 
> $$W=\underset{\text{Path 1 of AB}}{\int_{A}^B}\vec{F}\cdot d\vec{r}=\underset{\text{Path 2 of AB}}{\int_{A}^B}\vec{F}\cdot d\vec{r}$$
> Consecutively, we can define a conservative force if and only if it's closed path results in a net work of 0: 
> $$W=0=\oint \vec{F}\cdot d\vec{r}\implies \vec{F}\text{ is a conservative force}$$
> Note that for any $\oint$ over the path $AB$; we can express this as:  $$\begin{align}\oint \vec{F} \cdot d\vec{r} &= \underset{\text{Path 1 AB}}{\int}\vec{F}\cdot d\vec{r} + \underset{\text{Path 2 BA}}{\int}\vec{F}\cdot d\vec{r} \\&=\underset{\text{Path 1 AB}}{\int}\vec{F}\cdot d\vec{r} - \underset{\text{Path 2 AB}}{\int}\vec{F}\cdot d\vec{r} = 0\end{align}$$
> Note that we defined that this summed to $0$, since a path $BA$ is equivalent to having a negative work for the corresponding path $AB$. 

> Non-Conservative Forces
> The work done by a conservative force is *dependent* on the path; that is it is not a state function. 

### Proving Conservativity
The question then arises; how *can* we define if a force is conservative or not? The core concept (at least the one defined by the textbook) is that our function is an exact differential. Recall that we defined work as the following: 
$$
\begin{align}
dW &= \vec{F} \cdot d\vec{r} \\
dW&=F_{x}dr_{x} + F_{y}dr_{y} + F_{z}dr_{z}
\end{align}
$$
Where we can expand it into a corresponding multivariable differential. 
> [!theorem] Equivalent Differential
> The textbook defines the concept of an equivalent differential in $\mathbb{R}^2$ to be the following: 
> $$dW = \vec{F}\cdot d\vec{r} = F_{x}dr_{x}+F_{y}dr_{y}\to F_{x}dx + F_{y}dy$$
> This is an exact differential if: 
> $$\frac{dF_{x}}{dr_{y}}=\frac{dF_{y}}{dr_{x}}\implies \frac{dF_{x}}{dy} =\frac{dF_{y}}{dx}$$
> (Note that in reality, equivalent differentials are more accurately defined by partial differential.)

This can be shown in the following examples: 
> $$axy^3\hat{i} + ayx^3\hat{j}$$$$\begin{align}\frac{dF_{x}}{dy} = \frac{d(axy^3)}{dy}= 3axy^2 && \frac{dF_{y}}{dx} = \frac{d(ayx^3)}{dx} & =3ayx^2 \\3axy^2\neq {3}ayx^2 && \therefore\text{ Force is N.C}\end{align}$$

> $$a\left[\frac{y^2}{x}\hat{i}+2y\ln\left( \frac{x}{b} \right)\hat{j}\right]$$$$\begin{align}\frac{dF_{x}}{dy}=\frac{d\left( \frac{ay^2}{x} \right)}{dy}=\frac{2ay}{x} && \frac{dF_{y}}{dx}=\frac{d\left( 2ay\ln \left( \frac{x}{b} \right) \right)}{dx} = \frac{2ay}{\left( \frac{x}{b} \right)}\left( \frac{1}{b} \right) = \frac{2ay}{x} \\\frac{2ay}{x}=\frac{2ay}{x} && \therefore \text{Force is C.}\end{align}$$

> $$\frac{ax\hat{i} + ay\hat{j}}{x^2 + y^2} = \frac{ax\hat{i}}{x^2+y^2} + \frac{ay\hat{j}}{x^2+y^2}$$
> Note that for this case, we are solving this as a partial differential: $$\begin{align}\frac{\delta F_{x}}{\delta y} = \frac{\delta\left[\frac{ax}{x^2+y^2} \right]}{\delta y} &= ax \frac{\delta\left[(x^2+y^2)^{-1}\right]}{\delta y} \\&=ax* (-1(x^2+y^2)^{-2}2y) \\\frac{\delta F_{x}}{\delta y}&= -\frac{2axy}{(x^2+y^2)^2}\end{align}$$
> $$\begin{align}\frac{\delta F_{y}}{\delta x} = \frac{\delta\left[ \frac{ay}{x^2+y^2} \right]}{\delta y} &= ay \frac{\delta[(x^2+y^2)^{-1}]}{\delta y} \\&= ay * (-1(x^2+y^2)^{-2}2x) \\\frac{\delta F_{x}}{\delta y}&=-\frac{2axy}{(x^2+y^2)^2}\end{align}$$
> Note that: $$\frac{\delta F_{y}}{\delta x}=-\frac{2axy}{(x^2+y^2)^2}=\frac{\delta F_{x}}{\delta y} \implies \text{Force is Conservative}$$
## Differentiating Potential Energy
Another implication of potential energy; since we defined it as negatively proportional to work, and work is the integral of a force and some distance: 
$$
U=-W = -\int \vec{F}\cdot d\vec{r}
$$
Therefore, differentiating $U$ with respects to displacement gives us an infinitesimal amount of  potential energy with respects of a force applied: 
$$
\begin{align}
U&=-\int \vec{F}\cdot d\vec{r} \\
dU&= -\vec{F}\cdot d\vec{r} & \text{Let } d\vec{r}=dl\text{ where } l \text{ is a infinitesimal displacement}\\
-\frac{dU}{d\vec{r}}=-\frac{dU}{dl}&=\vec{F}
\end{align}
$$
For multidimensional forces, such as ones in $\mathbb{R}^2$, then this can be expanded as: 
$$
\vec{F} =- \left( \frac{\delta U}{\delta x} \right)\hat{i} - \left( \frac{\delta U}{\delta y} \right)\hat{j}
$$