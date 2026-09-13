---
updated_at: 2026-09-13T19:13:28.453-04:00
edited_seconds: 380
course: PHY180H1
tags:
  - PHY180H1
"Lecture #": 4
date: 2026-09-11
Week: 2
Created: September 11th 2026, 10:41:21 pm
---
Hub: [[PHY180 Hub]]
Previous: [[3 — Position, Velocity, Acceleration]]
Next: N/A

> [!quote] Textbook Chapters Discussed; 
> 3.4-3.6
--- 
# In-Lecture Notes
# Pre-Lecture Notes
## Kinematics Equations
This section will detail the derivation and usage of some kinematics equations for use in $1d$ (really, $nD$) problems. 
Recall that we defined $\Delta t$ as the following relation: 
$$\Delta t= t_{f} - t_{0}$$
We can simplify this by taking $t_{0}$ to be $0s$; that is $t_{f}=t$; ergo $\Delta t = t$. We therefore have the following relations: 
* $\Delta t = t$ 
* $\Delta x=x_{t}-x_{0}$
* $\Delta v = v_{f}-v_{0}$

For the sake of this section; we will assume that *acceleration* is constant; that is $\bar{a}=a$. From this set we can get two useful kinematics equations: 
$$\bar{v} = \frac{\Delta x}{\Delta t} = \frac{x_{t}-x_{0}}{t}\tag{1.1}$$
$$\bar{v} = \frac{v_{t} + v_{0}}{2} \tag{1.2}$$
Note that $(1.2)$ arises from how we generally define the concept of an average; as well as the fact that $\bar{a}=a$. $x_{t}$ can be found from $(1.1)$ as follows: 
$$
x_{t} = \bar{v}t + x_{0} \tag{2.1}
$$
Also, since $\bar{a} = a$, then: 
$$\bar{a} = \frac{\Delta v}{\Delta t}=\frac{v_{t} - v_{0}}{t}$$
Which can be rearranged into: 
$$v=\bar{a}t + v_{0}\tag{3.1}$$

--- 
Now we will try to derive the other popularly known kinematics equations: 

> Displacement Equation 1
> $$x=\frac{1}{2}at^2 + v_{0}t + x_{0} \tag{k.1}$$
> > [!theorem]- Derivation
> > Take equation (3.1) and add a term of $v_{0}$ onto both sides, giving us: 
> > $$v+v_{0}=at + 2v_{0}$$
> > Divide by two on both sides: 
> > $$\frac{v+v_{0}}{2} = \frac{at}{2} + v_{0}$$
> > From $(1.2)$; we can sub in our term of $\bar{v}$: 
> > $$\bar{v} = \frac{at}{2} + v_{0}$$
> > Sub into $(2.1)$: 
> > $$x_{t} = \left(\frac{at}{2} + v_{0}\right)t + x_{0} $$
> > And we get our final answer: 
> > $$x=\frac{1}{2}at^2 + v_{0}t + x_{0}$$

> 