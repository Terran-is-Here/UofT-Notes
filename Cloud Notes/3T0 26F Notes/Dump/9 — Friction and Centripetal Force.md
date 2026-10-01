---
updated_at: 2026-10-01T16:25:08.098-04:00
edited_seconds: 600
course: PHY180H1
tags:
  - PHY180H1
"Lecture #": 9
Lecture Date: 2026-09-28
Week: 4
created:
---
Hub: [[PHY180 Hub]]
Previous:  [[8 — 3rd Law of Newton, FBDs]]
Next: [[10 — Drag Force and Terminal Velocity]]

> [!quote] Textbook Chapters Discussed: 
> 6.1-6.2 (though really, 6.3 is also included.) 

> [!caution] Note
> It may be useful to refresh on some Integration characteristics and the relationship a term of $F,p,v,a$ has in terms of each other as some rate to $dt$; see [[4 — 1D Kinematics]] for more information. 

--- 
# Lecture Notes

### Lab Notes
Given the 2d system of the following: 
![[9 — Friction and Centripetal Force-1790628165756.webp]]
Can we use this to solve for gravity? First, solve for the centripetal force; given by: 
$$
F_{C} = \frac{mv^2}{r}
$$
Note that $F_{C} = \cos\theta F_{T}$, then: 
$$
\begin{align}
F_{T}&= \frac{F_{C}}{\cos\theta} \\
&=\frac{mv^2}{r\cos\theta}
\end{align}
$$
Note that $F_{y} = \sin \theta F_{T}$, note that assuming this is a static system at that moment, then this is equivalent to some $mg$: 
$$
\begin{align}
mg &= \sin\theta F_{T} \\
&=\frac{\sin\theta mv^2}{r\cos\theta} \\
mg&= \frac{\tan\theta mv^2}{r} \\
g &= \tan\theta * \frac{v^2}{r} & \text{Note, }\tan\theta = \frac{y}{r} \\
&= \frac{yv^2}{r^2} & \text{Note } v=\frac{2\pi r}{T} \\
&= \frac{y}{r^2} * \left( \frac{2\pi r}{T} \right)^2  \\
g&=\boxed{\frac{4\pi^2y}{T^2}}
\end{align}
$$
Note that this is the equation that will be applied within our Lab on 09/30. 
## Friction
See the corresponding ILA blocks within Force of Friction. 


---
# Pre-Lecture Notes
## Force of Friction
The Force of Friction is generally defined as a force *opposite* the direction of acceleration (or, from [[7 — 1st and 2nd Laws of Newton#Newton's First Law|Newton's First Law]], the net acceleration). There exists two definitions of friction: Static and Kinetic Friction: 
> [!theorem] Static Friction
> $$F_{S} \leq \mu_{s}N$$
> Note that this inequality exists, as Static Friction can only provide friction up to this amount. Once this is exceeded, our object now has some velocity, meaning that our object is no longer static. Therefore, we can also denote: 
> $$\text{max}(F_{S}) = \mu_{s}$$

> [!theorem] Kinetic Friction
> Kinetic Friction is defined as the following: $$F_{K} = \mu_{k}N$$
> Note that this only exists if and only if our object has a speed greater than 0, that is at that instantaneous moment.

Recall that friction forces are reaction forces *which always point against the direction of motion*. 
> [!ILA] ILA
> $$\mu_{k},\mu_{s}$$ 
> These are obtained via experimentation and are normally found within data tables. 

## Centripetal Force
Centripetal force is the extension of the concept of Centripetal Acceleration into the world of dynamics; with it generally defined as: 
$$
F_{C} = ma_{c} = \frac{mv^2}{r} = mr\omega^2
$$
Note that the second definition is the extension of $v_{a} = r\omega$ into acceleration. Note that this implies that: 
$$
F_{C} = \frac{mv^2}{r} \implies r = \frac{mv^2}{F_{C}}
$$
That is, a ever increasing centripetal force decreases the effective radius for a given object travelling at a certain velocity. Centripetal Force is *however* not a force on it's own, rather it is provided by other forces (such as $F_{F},F_{N},F_{T}$); or in other words; it is often equivalent to the net force of the corresponding rotational system.  

### Banked Curves
Banked Curves are extensions of both the inclined surface problems in combination with centripetal acceleration. Note that for these problems, it is easier to keep our axis aligned to the cardinal directions; as we want our vector pointing inwards to be directly pointing inwards (i.e. we don't have to do more math than is needed.) 