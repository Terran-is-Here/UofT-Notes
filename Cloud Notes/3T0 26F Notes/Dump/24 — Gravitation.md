---
updated_at: 2026-10-27T14:14:27.171-04:00
edited_seconds: 630
course:
tags:
"Lecture #": 0
Lecture Date: 2026-10-27
Week:
---
Hub: [[PHY180 Hub]]
Previous: [[22 and 23 — Static Equilibrium and Elasticity]]
Next: [[25 — Orbital and Keplerian Mechanics]]
> [!quote] Recommended Reading 
> Sections 13.1 - 13.3 of University Physics

--- 
# Lecture Notes

---
# Pre-Lecture Notes
## Newtonian Gravitation
Newton's Law of Universal Gravitation can be described as the generalization(\*) of the force of gravity, over any set of bodies, and is defined as the following equation: 

> [!theorem] Newton's Law of Universal Gravitation
> Let $F_{G}$ be the force of **gravity**, then: 
> $$F_{G} = \frac{Gm_{1}m_{2}}{r^2}$$
> Where $G=6.67\times 10^{-11}N*m^2*kg^{-2}$. Note that in a vector notation: 
> $$\vec{F_{G}}=\frac{Gm_{1}m_{2}}{r^{2}}\hat{r}$$
> Where $\hat{r}$ is a unit vector that points from some object $A$ to some object $B$, or vice versa. (This is an extension of NTL). 

Note that this has many interesting affects when we consider gravitation near a local body, and or with terms of one body present. 
### Gravitation Near Earth
Consider now the case when we are near a gravitational body, such as Earth, where $F_{g}=mg$, then considering that Newton's Law of Universal Gravitation also holds true, we find that, setting $m_{1}=m$, and $m_{2}=M_{E}$, then: 
$$
\begin{align}
mg &  = \frac{GmM_{E}}{r^{2}} \\
g  & =\frac{GM_{E}}{r^{2}}
\end{align}
$$

Note that this is true for any case in which we are trying to find the acceleration from gravity of an object within a single-object gravitational field; we can substitute $M_{E}$ and $r$  with values as we please to find the corresponding acceleration from gravity. Alternatively, you can describe this as the *gravitational field strength* at that point, in terms of $\frac{N}{kg}$.  

## Generalized Gravitational Potential Energy 
Recall that in an earlier note, we defined Gravitational Potential Energy (or more so, the change in it) as $\Delta U = mg(y_{t}-y_{0})$, where we assumed that the gravitational field strength would be held constant across the translation. 

Recall that we defined Potential Energy as the negative of work, which was defined as the path integral of a force over a distance: 
$$
\Delta U = -W = -\int_{r_{0}}^{r_{1}}F\cdot dr
$$
Setting $F$ = $F_{g}$, then: 
$$
\begin{align}
\Delta U & =-\int_{r_{0}}^{r_{1}} \frac{GM_{e}m}{r^{2}}dr \\
 & =-GM_{e}m \int_{r_{0}}^{r_{1}} \frac{1}{r^{2}}dr \\
 & =-GM_{e}m \left[ -\frac{1}{r} \right]_{r_{0}}^{r_{1}} \\
 & =-GM_{e}m\left[ \frac{1}{r_{0}}-\frac{1}{r_{1}} \right] &
\end{align}
$$
Since $\Delta U = U_{2}-U_{1}$, then: 
> [!theorem] Generalized Gravitational Potential Energy
> $$U_{n} = -\frac{GMm}{r_{n}}$$
> Where $r_{n}$ is the radius from an origin, this gives the potential energy at a certain point. 
> > Consider this as well as $gr$, where we multiply the Gravitational Field strength times a distance to get a term of voltage. 

Note the negative sign, as $r_{n}$ decreases, the work done by gravity increases (or in other words, objects inherently want to fall down). Consider as well that $U_{n}=0$ doesn't inherently exist, and only exists in the following case: 
$$
U_{n} \to 0 \iff \lim_{ r_{n} \to \infty } -\frac{GMm}{r_{n}} =0
$$
### Escape Velocity
Considering this now in the context of the conservation of energy, recall that we can define the total mechanical energy of a system as the sum of it's kinetic energy and the potential energy in the system. For our context, we will set the potential energy as the term we had defined earlier above. 

Consider now the case for the *minimum* escape velocity of an object, that is the absolute minimum velocity of an object to get out of a planet's gravitational field. In this case, the gravitational potential energy would tend to 0, as well as our final velocity reaching 0, then: 

$$
\frac{1}{2}mv_{i}^{2} -\frac{GMm}{r_{n}}= \frac{1}{2}mv_{t}^{2} - \frac{GMm}{r_{n'}}
$$
Note that the terms on the left both evaluate to $0$ ($\lim_{ r_{n'} \to \infty }\frac{GM_{e}m}{r_{n'}}=0$), then: 
$$
\begin{align}
\frac{1}{2}mv^{2}_{i} &  = \frac{GMm}{r_{n}} \\
 & v_{i}=\sqrt{ \frac{2GM}{r_{n}} } = \sqrt{ \frac{2GM}{R} }
\end{align}
$$
Where $v_{i}$ represents the escape velocity of the system. 
### Boundness 
Consider now our earlier implications for the above, we state that an object just barely escapes an object's gravitational field at an infinite radius when we set both the final kinetic and gravitational potential energies to 0. 

Recall that Gravitational Potential Energy only results to becoming 0 when $r_{n}$ becomes infinitely large; thus we define the other two cases for an object: 

If the kinetic energy of an object is not 0 when the gravitational potential energy is not 0, then our object fully escapes, and will not return. (Total Energy is Positive)

If the total energy of the system is Negative, then:
$$
\begin{align}
\frac{1}{2}mv_{t}^{2}-\frac{GMm}{r_{n'}} <0 \\
\frac{1}{2}mv_{t}^{2}<\frac{GMm}{r_{n'}}
\end{align}
$$
Since we know that this $v_{t}$ reaches 0, at some value where our gravitational potential energy *does not reach 0*, that is $\exists r_{n}$ that is finite, then we say that our object is gravitationally bound and would fall back into the potential energy well. 

Note that we can solve for the maximum potential distance (if it exists) by setting $v_{t}=0$ and solving for $r_{n'}$. 


