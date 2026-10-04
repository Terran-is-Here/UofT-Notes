---
updated_at: 2026-10-03T21:54:36.382-04:00
edited_seconds: 500
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
> 