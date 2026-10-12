---
updated_at: 2026-10-12T11:47:42.566-04:00
edited_seconds: 1340
course: PHY180H1
tags:
  - PHY180H1
"Lecture #": 16
Lecture Date: 2026-10-16
Week: 6
Created: October 10th 2026, 9:57:06 pm
---
Hub: [[PHY180 Hub]]
Previous: [[15 — Conservation of Momentum, Collisions]]
Next: N/A
> [!quote] Recommended Reading 
> University Physics 9.6, 9.7
> [[14 — Momentum and Impulse]]

--- 
# Lecture Notes

---
# Pre-Lecture Notes
## Extending Newtonian Mechanics
So far, all Newtonian mechanics have been focused on defining the behaviors of point loads: 
$$
F=ma
$$
Consider a particle composed of $N$ masses; where: 
$$
m_{\text{total}}= \sum _{j=1}^Nm_{j}
$$
Where $m_{j}$ represents the mass of the $j$-th particle of our system. Now consider that if we have an applied force $F_{a}^\text{ext}$ over our object, each miniscule particle will have it's own applied force $F_{j}^\text{ext}$ from the external source. Note that $F_{j}$ between particles may not be equivalent; and are often *not* equivalent. 

Consider now that each particle in isolation may *apply* forces to their neighbours. From Newton's Third Law, we know that each particle when a force is applied will feel a reactive force $F_{j}^\text{Int}$ in turn. Note that we say that this force does not inherently cancel out; but rather they are applied on separate bodies. Therefore for some particle $F_{j}$, the sum of the forces it experiences are defined as below: 
$$
F_{j} = F_{j}^\text{Ext} + F_{j}^\text{Int}
$$
Note that $F=\frac{dp}{dt}$; then: 
$$
\frac{dp_{j}}{dt} = F_{j}^\text{Ext} + F_{j}^\text{Int} \tag{1.1}
$$
Note now considering this whole system as a whole as some $F^\text{ext}_{a}$ is applied on our *entire object*. This changes the momentum of the entire system; thus: 
$$
F_{net} = \sum^N_{j=1} \frac{dp_{j}}{dt}
$$
Note that from $(1.1)$ that we can relate the sum the momentums with the sum of some internal forces of our objects; that is: 
$$
\sum_{j=1}^N F_{j}^\text{Ext} +\sum_{j=1}^N F_{j}^\text{Int}  =  \sum^N_{j=1} \frac{dp_{j}}{dt}
$$
Consider the term $\sum_{j=1}^N F_{j}^\text{Int}$, this represents the reaction force pairs within our body. Since these pairs are internal, and our object is *preferably* not tearing itself apart, then this term should equal 0; then: 
$$
\boxed{\sum_{j=1}^N F_{j}^\text{Ext}= F_{j}^\text{ext}  =  \sum^N_{j=1} \frac{dp_{j}}{dt}}

$$
That is, the net external force applied is equivalent to the sum of the corresponding change of momentum over the time period of *all* of the particles present in our object. 
### Center of Mass
Consider now that if our object has some total momentum represented by the points; some $P_{t}$; then: 
$$
F = \frac{dP_{t}}{dt}
$$
If we consider this situation; recall that we can define $P_{t}$ as $\sum p_{j}$; then take the following; note that $M$ represents the **total mass of the body**. 
$$
F = \sum^N_{j=1} \frac{d \vec{p_{j}}}{dt} = M\vec{a}
$$
Rewriting this; then: 
$$
\begin{align}
M\vec{a} &  = \sum_{j=1}^N \frac{d\vec{p_{j}}}{dt} \\
 & = \frac{d}{dt}\sum_{j=1}^N \vec{p_{j}}  & \text{Note, }\vec{p_{j}} = m_{j} \vec{v_{j}} = \frac{m_{j}\vec{x_{j}}}{dt}\\
 & = \frac{d}{dt}\sum_{j=1}^N m_{j} \frac{d\vec{x_{j}}}{dt} \\
 M\vec{a}&  = \frac{d^2}{dt^2}\sum_{j=1}^N m_{j}\vec{x_{j}}
\end{align}
$$
Then, dividing by the *total* mass of the body: 
$$
\vec{a} =  \frac{d^2}{dt^2}\left( \frac{1}{M}\sum_{j=1}^N m_{j} \vec{x_{j}} \right)
$$
Note that the term in the parenthesis *actually gives us the center of mass*. Or in other words; Center of Mass is the *mean* of the system as a weighed average as a function of distance and weight. 
> [!theorem] Center of Mass
> The vector pointing towards the center of mass of a system can be derived as the equation below: 
> $$\boxed{\vec{x_{\text{CoM}}} =  \frac{1}{M}\sum_{j=1}^N m_{j} \vec{x_{j}}}$$
> Where $M$ is the system's total energy, $m_{j}$ being the mass of an individual particle, and $\vec{x_{j}}$ being it's distance from some origin point as a vector. 

Note that this is in terms of a vector; we can break this up into it's dimensional components; then performing the traditional resultant vector math to get the equivalent center of mass: 
$$
\begin{align}
\vec{x_{\text{CoM}, x}} = \frac{1}{M}\sum_{j=1}^Nm_{j}\vec{x_{xj}} \\
\vec{x_{\text{CoM}, y}} = \frac{1}{M}\sum_{j=1}^Nm_{j}\vec{x_{xy}} \\
\vec{x_{\text{CoM}, z}} = \frac{1}{M}\sum_{j=1}^Nm_{j}\vec{x_{xz}}
\end{align}
$$
Where then the resultant combined center of mass vector is equivalent to combining all the corresponding vector components of the equation above. 

In terms of a continuous object; that is $m_{j} \to dm$; then: 
$$
\vec{x_{\text{CoM}}} = \frac{1}{M}\int \vec{r}dm
$$
Where $dm$ is the corresponding infinitesimally small amount of mass on an object; and $\vec{r}$ represents some physical dimensional characteristic *of* our object. 
## Rocket Propulsion
Rockets are vehicles which expel some material out from behind them in order to accelerate; or in other words; they are *reaction* engines. Let us define our rocket's initial momentum as the following: 
$$
p_{r}=v_{r}m_{r}
$$
Consider now the case when we have rocket gasses escaping out of the rocket. For the purposes of this derivation, we will assume that the change in the mass of the rocket due to rocket fuel being expelled (i.e; $dm_{g}$) is constant. 

This gas will travel towards the left with some velocity $u$; or in terms of the system from the surface; some velocity $v-u$. Our rocket will also now gain some speed $dv$ from the escape gasses pushing on the rocket; thus taking conservation of momentum: 
$$
\begin{align}
p_{t} &  = (m_{r}-dm_{g})(v+dv) + dm_{g}(v-u)  & \text{w/CoM} \\
m_{r}  & =m_{r}v + dvm_{r} -dm_{g}v - dm_{g}dv + dm_{g}v -dm_{g}u \\
0 & =dvm_{r}-dm_{g}dv-dm_{g}u \\
m_{r}dv  & =dm_{g}dv +dm_{g}u
\end{align}
$$
Note that $dm_{g}dv$ will be miniscule/negligible, therefore we can equate this as: 
$$
m_{r}dv = dm_{g}u 
$$
Note that $dm_{g}$ is a change of mass from the total mass of the rocket; that is $dm_{g} = -dm$: 
$$
\begin{align}
m_{r}dv  & = -dm u \\
dv  & =-u \frac{dm}{m_{r}} \\
\int_{t_{0}}^{t_{1}}dv  & =-u \int_{m_{0}}^m{f} \frac{1}{m}dm  \\
\Delta v  & =-u \ln\left( \frac{m_{0}}{m} \right) & \text{Since } u \text{ points opposite to } v \\
\Delta v  & =u\ln\left( \frac{m_{0}}{m} \right)
\end{align}
$$
Where $u$ represents the *exhaust velocity* of our propellant. The equation above represents the *rocket equation* of our rocket.
> [!theorem] Rocket Equation (without gravity) 
> $$\Delta v   =u\ln\left( \frac{m_{0}}{m_{d}} \right)$$
> Where $m_{0}$ represents the wet mass of the rocket, and $m_{d}$ represents the current dry mass of the rocket. This solves for the effective $\Delta v$ as a rocket goes from $m_{0} \to m_{d}$, or in other words, how much $\Delta v$ is offered by this rocket as it burns all of it's fuel. 
> 
### With Gravity
Recall our previous step: 
$$
p_{t} =  (m_{r}-dm_{g})(v+dv) + dm_{g}(v-u)
$$
Note that this is some $p_{i}=p_{f}$ situation. Recall that $p_{t}=m_{r}v$; then with this we can say that
$$
dp =  (m_{r}-dm_{g})(v+dv) + dm_{g}(v-u) - m_{r}v
$$
Recall that $dp = \vec{F}dt$, For our context; this would be some $m_{r}gdt$; then; reusing the steps we derived above; then: 
$$
\begin{align}
-m_{r}g dt & = m_{r}v + m_{r}dv - dm_{g}v - dm_{g}dv +  dm_{g}v -dm_{g}u-m_{r}v \\
-m_{r}g dt & = m_{r}dv - dm_{g}dv -dm_{g}u  & dm_{g}dv \to 0 \\
-m_{r}gdt  & =m_{r}dv - dm_{g}u & dm_{g} u = -udm_{r} \\
-m_{r}gdt  & =m_{r}dv +udm_{r}  \\
-m_{r}gdt - udm_{r} & =m_{r}dv \\
\end{align}
$$
From the last line there; then: 
$$
\begin{align}
m_{r}dv & =-u dm_{r}-m_{r}gdt \\
dv  & =-u \frac{1}{m_{r}}dm_{r} - gdt \\
\int _{v_{0}}^{v_{t}}dv & =-u\int_{m_{0}}^{m_{r}} \frac{1}{m_{r}}dm_{r} - g\int_{t_{0}}^t dt \\
v_{t}-v_{0}  & =-u\left[ \ln\left( \frac{x}{m_{r}} \right) \right]^{m_{r}}_{m_{0}}-g(t-t_{0}) \\
\Delta v & =-u\left( -\ln\left( \frac{m_{0}}{m_{r}} \right) \right)-g\Delta t \\[1.5em]
\end{align}
$$
From here, we get the rocket equation for a rocket affected by gravity: 
$$\boxed{\Delta v  =u\ln\left( \frac{m_{0}}{m_{r}} \right)-g\Delta t}$$
> [!theorem] Rocket Equation (with gravity) 
> The rocket equation, taking into account a term of gravity, is represented by the following: 
> $$\boxed{\Delta v  =u\ln\left( \frac{m_{0}}{m_{r}} \right)-g\Delta t}$$
> Where $m_{0}$ represents the wet mass of the rocket, $m_{r}$ represents the dry mass of the rocket, $u$ represents the exhaust velocity, and $\Delta t$ represents the time it takes for our rocket to go from $m_{0} \to m_{r}$. 


