---
updated_at: 2026-09-17T16:52:12.910-04:00
edited_seconds: 1220
course: PHY180H1
tags:
  - PHY180H1
"Lecture #": 4
date: 2026-09-17
Week: 2
Created: September 11th 2026, 10:41:21 pm
---
Hub: [[PHY180 Hub]]
Previous: [[3 — Position, Velocity, Acceleration]]
Next: [[5 —2D Kinematics]]

> [!quote] Textbook Chapters Discussed; 
> 3.4-3.6
--- 
# In-Lecture Notes
### Motion with Constant Acceleration
From $v=v_{0}+at$, we can integrate this into a term for displacement: 
$$
x - x_{0} = \int^t_{0}v(t')dt' + x_{0} = \left[v_{0}t' + \frac{at'}{2}\right]^{t}_{0}
$$
$$
x-x_{0} = v_{0}t + \frac{at^2}{2}
$$
$$
x = x_{0} + v_{0}t + \frac{at^2}{2}\tag{3.13 in the textbook}
$$

From here, using $v = v_{0}+at$ and $(3.13)$, we can solve for a term of *average velocity*: 
$$
\bar{v} = \frac{\Delta v}{\Delta t} = \frac{x-x_{0}}{t} 
$$
$$
\frac{\left( v_{0}t  + \frac{at^2}{2} \right)}{t} = v_{0} + \frac{at}{2}
$$
$$
v_{0}  +\frac{v-v_{0}}{2}
$$
$$
\bar{v} = \frac{v+v_{0}}{2}
$$
From this, recall that: 
$$
\bar{v} = \frac{\Delta x}{t} = \frac{x-x_{0}}{t}
$$
$$
\frac{v+v_{0}}{2} = \frac{x-x_{0}}{t} \implies x = t\left( \frac{v+v_{0}}{2} \right) + x_{0}
$$
Then, we can also solve for final velocity through the following: 
$$
v = v_{0} + at \implies t = \frac{v-v_{0}}{a}
$$
Plug it into our equation above, then: 
$$x = \left(\frac{v-v_{0}}{a}\right)\left( \frac{v+v_{0}}{2} \right) + x_{0}$$
Simplifying: 
$$
x-x_{0} = \left( \frac{v^2-v_{0}^2}{2a} \right)
$$
$$
2a(x-x_{0}) = v^2 - v_{0}^2 \implies v^2 = v_{0}^2 + 2a(\Delta x)
$$


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
Now we will try to derive the other popularly known kinematics equations; the others are put here for reference; 
* $\bar{v} =\frac{v_{t} + v_{0}}{2}$ (Does not contain acceleration) 
* $v = \bar{a}t + v_{0}$ (Does not contain displacement!)
* $x = x_{0} + \bar{v}t$

> [!axiom] Displacement Equation 1
> This does NOT have any final velocity as a term. 
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

>[!axiom] Time-Independent Velocity
>This does not have time as a term. 
>$$v^2 = v_{0}^2 + 2a\Delta x \tag{k.2}$$
>> [!theorem]- Proof 
>> Let's take equations $(3.1)$ and $(1.2)$ into the equation for $(2.1)$; that is: 
>> $$v=at + v_{0} \text{ and } \bar{v} = \frac{v + v_{0}}{2} \to x_{t} = \bar{v}t + x_{0}$$
>> We can solve our first equation into a term of time: 
>> $$\frac{v-v_{0}}{a} = t$$
>> Subbing both of these into equation $(2.1)$ then: 
>> $$x_{t} = \frac{v + v_{0}}{2}*\frac{v-v_{0}}{a} + x_{0}$$
>> $$(x_{t}-x_{0}) = \frac{v^2-v_{0}^2}{2a}$$
>> $$2a(x_{t}-x_{0}) = v^2-v_{0}^2$$
>> $$2a(x_{t}-x_{0}) + v_{0}^2 = v^2$$
>> $$v^2 = 2a\Delta x + v_{0}^2$$

Just like in SPH4U / SPH3U, we can utilize these equations to solve a Kinematics problem with respects to one dimension.
## Free-Fall 
Free-fall problems generally operate on the assumption that a system's net acceleration is equivalent to gravity; that is $\bar{a} = a = -g$. We can simply resubstitute these into our equations. **We assume that air resistance is nonexistent.**

**For the purposes of this course, g=9.8**. If air resistance is non-negligible, you cannot neglect it in your calculations. 

Note that with this new context; we can do some algebraic manipulation on our earlier equations to solve for solutions to problems with gravity. 

> [!theorem] Impact Time 
> Given a certain starting velocity, $v_{0}$, a starting displacement $x_{0}$, we can solve for the time it takes to impact to some surface ($x=0$ normally): Plug in our values; then we get: 
> $$x = x_{0} + vt + \frac{1}{2}at^2$$
> For sake of simplicity (for many cases of this problem), $x_{0} = 0$; then: 
> $$0 = vt + \frac{1}{2}at^2$$
> $$0 = t \left( v + \frac{1}{2}at \right)$$
> Where solutions are $t=0$ and: 
> $$v + \frac{1}{2}at = 0$$
> Normally, $a = -g$ for free fall problems (downwards is -'ve)
> $$\frac{1}{2}gt=v$$
> $$t = \frac{2v}{g}$$

With this logic; you can really adjust our earlier kinematics equations to solve for any question involving gravity in this context.
## Integration and Differentiation
Recall our definitions of Velocity and Acceleration. More generally, under Calculus, we define them as: 
$$v(t) = \frac{d}{dt}x(t)$$
$$
a(t) = \frac{d}{dt}v(t)
$$
That is, velocity is the derivative of our function of displacement, and acceleration is the derivative of our velocity. From here, we can actually solve for an equation for displacement using calculus. 

$$v(t) = \int \frac{d}{dt}v(t) dt \implies v(t) = \int a(t)dt +C_{1} $$
Where $C_{1}$ is some constant of integration. We can use the same logic using our equation for displacement: 
$$
\frac{d}{dt}x(t) = v(t) \implies x(t) = \int v(t)dt + C_{2}
$$
Where $C_2$ is another constant of acceleration. If $\bar{a}=a$, then $a(t)$ is some constant; therefore: 
$$v(t) = \int a \ dt + C_{1} \implies v(t) = at + C_{1}$$
If we take $t =0$, then $C_{1} = v_{0}$: 
$$v(t) = at + v_{0}$$
We can plug this into our earlier term for $x(t)$: 
$$
x(t) = \int at + v_{0} \ dt + C_{2}
$$
Using reverse power rules; we get: 
$$
x(t) = \frac{1}{2}at^2 + v_{0}t + C_{2}
$$
If $t=0, x(t) =C_{2} \implies C_{2}=x_{0}$, then: 
$$
x(t) = \frac{1}{2}at^2 + v_{0}t + x_{0}
$$
Which means we have arrived at one of our earlier kinematic equations. 