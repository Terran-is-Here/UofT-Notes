---
updated_at: 2026-11-02T21:43:17.396-05:00
edited_seconds: 1300
course: PHY180H1
tags:
  - PHY180H1
"Lecture #": 25
Lecture Date: 2026-10-27
Week:
---
Hub: [[PHY180 Hub]]
Previous: [[24 — Gravitation]]
Next: [[26 — Tidal Forces, General Relativity]]
> [!quote] Recommended Reading 
> Sections 13.4, 13.5 of University Physics


--- 
# Lecture Notes

---
# Pre-Lecture Notes
## Circular Orbits
Consider now the concept of a perfectly circular object. Recall that for a circular body, a centripetal force is applied onto it as it's net force: 
$$
F_{c}=ma_{c}=\frac{mv^{2}}{r}
$$
Consider now that if an object is orbiting a planetary body, this force is solely provided by $F_{g}$, that is the force of gravity. Taking Newton's Law of Universal Gravitation, we find that: 
$$
\frac{GMm}{r^{2}} = \frac{mv^{2}}{r}
$$
Where $v$ represents the orbital velocity. Note that $m$ cancels out in this expression, and thus we can solve for $v$: 
$$
\begin{align}
\frac{GMm}{r^{2}} & =\frac{mv^{2}}{r} \\
\frac{GM}{r} & =v^{2} \\
v & =\sqrt{ \frac{GM}{r} }
\end{align}
$$
> [!theorem] Orbital Velocity (perfectly circular orbits) 
> The orbital velocity of an object in a perfectly circular orbit is defined as the following expression: 
> $$v=\sqrt{ \frac{GM}{r} }$$
> Where $r$ is the radius of the orbit, with respects to the center of mass of the object being orbited. 

Recall that $v=\omega r$, as this is a rotating body, and recall that $\omega$ can be resolved as some $\frac{d\theta}{dt}$, or in terms of revolutions per second, $\frac{2\pi}{T}$, where $T$ represents the period, substituting this in, then: 
$$
\begin{align}
r\frac{2\pi}{T} & =\sqrt{ \frac{GM}{r} } \\
\frac{2\pi}{T} & =\sqrt{ \frac{GM}{r^{3}} } \\
T  & = 2\pi \sqrt{ \frac{r^{3}}{GM} }
\end{align}
$$
Where $T$ represents the rotational period of our body. or in other words: how long it takes to orbit. 
### Boundness
Recall that in our previous note, where we discussed how an object would be gravitationally bound if the total energy is *negative* (see [[24 — Gravitation#Boundness| PHY180(24) - Boundness]]): 
$$
E_{T} < 0
$$
Consider now the case when $v=\sqrt{ \frac{GM}{r} }$ as some term of orbital velocity, then we have: 
$$
\begin{align}
E_{t}  & = K + U_{g}  &\text{ Let }U_{g}=-\frac{GMm}{r},\, K=\frac{1}{2}mv^{2} \\
 & =\frac{1}{2}mv^{2} - \frac{GMm}{r} &\text{Recall, } v=\sqrt{ \frac{GM}{r} } \\
 & =\frac{1}{2}m\left( \frac{GM}{r} \right)-\frac{GMm}{r} \\
 & =\frac{GMm}{2r}-\frac{GMm}{r}= -\frac{GMm}{2r}
\end{align}
$$
Thus, we can see that the energy within a rotating system's total is equal to some negative value, thus an orbiting body in a perfectly circular orbit is gravitationally bound to the object in which it is orbiting with respects to. 

> This result also apparently applies to any two masses in circular orbits around their common center of mass, at a distance $r$ from each other, proof will be provided here when I get to doing this exercise. 


## Kepler's First Law 
Kepler's First Law states that every planet moves at an ellipse, where the sun (or rather, some mass $M \gg m$, where $M$ represents a star and $m$ represents the mass of the rotating body) located at one of the foci. 

In terms of terminology: 
* The Perihelion (generally, a Periapsis) represents the **closest** point in the orbit between some object and the main foci (i.e. $M$). 
* The Aphelion (generally, an Apoapsis) represents the **farthest** point in the orbit between some object and the main foci (i.e. $M$). 

The nature / shape of an ellipse is represented as a conic section as the equation below, where this equation returns a set of *points* which satisfy this value. 
$$
\boxed{\frac{\alpha}{r} = 1+e\cos \theta}
$$
Where $e$ defines the *eccentricity* of the orbit, and $r$ representing the distance from the main foci $M$ and our object orbiting it, some object with mass $m$. Note that from our definitions for boundness earlier (or, more specifically, the corresponding total energy of the system), we can derive some relationships for the corresponding values of eccentricity: 

* If $E_{T}<0$, then we know that our system is bounded; thus $0\leq e<1$ (representing an ellipse/circular orbit). 
* If $E_{T}=0$, then we know that our orbiting body has attained the **minimum escape velocity**, then $e=1$ (representing  a parabolic orbit)
* If $E_{T}>0$, then we know that our orbiting body has more kinetic energy than the required minimum escape velocity, then $e>1$, where this represents a *hyperbolic* orbit. 

### Hohmann Transfers
An interesting application of Kepler's First Law arises when we consider the concept of transferring from *one orbit* to another. Can we solve for the corresponding kinetic energies required to transfer from one orbit to another (and thus; the corresponding velocity injection that we need to make the orbital transfer?) 

For the purposes of this note (as well as the textbook, since they neglect to do so): We can actually solve for the kinetic energy present in an ellipse as some function of the *semi-major axis* of the Ellipse: 
$$
\boxed{E = -\frac{GMm}{2a}}\tag{1.1}
$$
Where $a$ represents the semi-major axis. The semi-major axis represents *half* the distance between the Apoapsis and Periapsis of some rotating body, that is: 
$$
a=\frac{1}{2}(r_{1}+r_{2})
$$
Where $r_{1}$ represents an initial orbit, and $r_{2}$ represents the radius of another circular orbit. Note that if $r_{1}$ represents an initial orbit, then $r_{1}$ represents the Periapsis of the transfer orbit, and $r_{2}$ therefore represents the Apoapsis of the corresponding transfer orbit. 

Then the equation above actually resolves as the following: 
$$
E = -\frac{GMm}{r_{1}+r_{2}}
$$
That is, twice the semi-major axis of the transfer orbit; or the sum of the corresponding radii of the planned circular orbits derived within a transfer orbit. Note that this represents the *total energy* of the orbital system: 

$$
-\frac{GMm}{r_{1}+r_{2}} = U_{g} + E_{k}
$$
Recall that $U_{g} = -\frac{GMm}{r}$. In this context, $r$ would represent the initial orbital radius, then: 
$$
-\frac{GMm}{r_{1}+r_{2}} + \frac{GMm}{r_{1}} = \frac{1}{2}mv^{2}
$$
> [!theorem] Vis-Visa Equation
> Note that solving this in terms of $v^{2}$ gives us the Vis-Visa Equation: $$\begin{align}-\frac{GMm}{r_{1}+r_{2}} + \frac{GMm}{r_{1}}  & = \frac{1}{2}mv^{2} \\2GM\left[ \frac{1}{r_{1}} - \frac{1}{r_{1}+r_{2}} \right] & =v^{2} & r_{1}+r_{2} = 2a \\GM \left[ \frac{2}{r_{1}} - \frac{1}{a} \right]  & =v^{2}\end{align}$$
> Texts normally set $GM=\mu$, where this represents the gravitational characteristics of the primary body that is being orbited then: 
> $$\boxed{v^{2}=\mu\left[ \frac{2}{r_{1}}-\frac{1}{a} \right]}$$
> Where $v$ represents the orbital velocity. 


So far, we've been setting $M$ as some mass at the foci; considering that in the Solar System, this would be the Sun (particularly for interplanetary trajectories), then we can find the corresponding velocity to transfer from some arbitrary orbit $r_{1}$ to some orbit $r_{2}$ as the following: 
$$
\begin{align}
-\frac{GM_{s}m}{r_{1}+r_{2}} + \frac{GM_{s}m}{r_{1}}   & = \frac{1}{2}mv^{2} \\
2GM_{s}m\left[ \frac{1}{r_{1}}-\frac{1}{r_{1}+r_{2}} \right] & =mv^{2} \\
\sqrt{ 2GM_{s} \left[ \frac{1}{r_{1}}-\frac{1}{r_{1}+r_{2}} \right] } & =v \\
\sqrt{ 2GM_{s} \left[ \frac{r_{2}}{r_{1}(r_{1}+r_{2})} \right]} & =v \\
\sqrt{ \frac{2GM_{s}r_{2}}{r_{1}(r_{1}+r_{2})} } & =v_{trans}
\end{align}
$$
Note that this corresponds to the total velocity required to obtain this outer-most orbit. To find the corresponding change in velocity required, we compare this velocity with the orbital velocity in a (circular) orbit around $r_{1}$ maintained with respects to $M_{s}$
$$
v_{i} = \sqrt{ \frac{GM_{s}}{r_{1}} }
$$
Then: 
$$
\begin{align}
\Delta v  & = v_{trans}-v_{i} \\
 & =\sqrt{ \frac{2GM_{s}r_{2}}{r_{1}(r_{1}+r_{2})} } - \sqrt{ \frac{GM_{s}}{r_{1}} } \\
 & =\sqrt{ \frac{GM_{s}}{r_{1}} }\left[ \sqrt{ \frac{2r_{2}}{(r_{1}+r_{2})} }-1 \right]
\end{align}
$$
We note that $\sqrt{ \frac{GM_{s}}{r_{1}} }=v_{i}$, then: 
$$
\boxed{\Delta v = v_{i}\left[ \sqrt{ \frac{2r_{2}}{r_{1}+r_{2}} }-1 \right]}\tag{1.2}
$$

> [!theorem] Hohmann Transfer Velocity 
> $$\Delta v = v_{i}\left[ \sqrt{ \frac{2r_{2}}{r_{1}+r_{2}} }-1 \right]$$
> This equation represents the $\Delta v$ needed to **transfer** from an orbit with radius $r_{1}$ to an orbit with radius $r_{2}$ around some major foci $M$, where $v_{i}$ is the orbital velocity at the original $r_{1}$, that is: 
> $$v_{i} = \sqrt{ \frac{GM}{r_{1}} }$$
> Note that however, this does **not** solve for the corresponding second burn needed to circularize. You would need to take the difference of the corresponding final kinetic energy (given by) $(1.1)$ and the corresponding required orbital velocity for $r_{2}$. 

We can test the equation above with an example. Calculate the transfer velocity between Earth and Mars. From the textbook, we get the following sets of astronomical data: 
* $r_{e}$ = $149.6\times 10^{6}\,km$ --> $149.6 \times 10^{9} m$
* $r_{m}=227.9 \times 10^{6}\,km$ --> $227.9 \times 10^{9}\,m$
* $M_{s}=1.99 \times 10^{30}\,kg$ 

Solving for the initial orbital velocity: 
$$
v_{1} =\sqrt{ \frac{6.67\times 10^{-11}\times 1.99\times 10^{30}}{149.6\times 10^{9}} } \approx 29786.78690 \frac{m}{s}
$$
Thus, solving for the equivalent transfer velocity: 
$$
\begin{align}
\Delta v  & = v_{i}\left[ \sqrt{ \frac{2r_{2}}{r_{1}+r_{2}} }-1 \right] \\
 & =v_{i}\left[ \sqrt{ \frac{2\times 227.9\times 10^{9}}{149.6\times 10^{9} + 227.9\times 10^{9}} }-1 \right] \\
 & \approx v_{i}*0.098825381 \\
 & \approx 29786.78690 * 0.098825381 \\
 \Delta v& \approx 2944 \frac{m}{s}
\end{align}
$$

> Note that we can actually go *one step further with this*. We know that we can relate $\Delta v$ with a rocket's fuel efficiency with the rocket equation, that is: 
> $$\Delta v=u\ln\left( \frac{m_{f}}{m_{r}} \right)-g\Delta t$$
> Note however that the Hohmann Transfer implicitly assumes $\Delta t \to0$; if it's not equal to zero, the expression above actually evaluates as a path integral in terms of that $g\Delta t$ term on the right there, and is outside the bounds of this course. 

## Kepler's Second Law 
