---
updated_at: 2026-10-16T16:58:06.018-04:00
edited_seconds: 2250
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
Next: [[17 — Rotational Kinematics, Rotational Variables]]
> [!quote] Recommended Reading 
> University Physics 9.6, 9.7
> [[14 — Momentum and Impulse]]

--- 
# Lecture Notes
## Center of Mass (LEC) 
Center of Mass is a generalization of Newton's Second Law to an object made out of an amount of particles with mass $m_{j}$; then: 
$$
M = \sum_{j=1}^Nm_{j}
$$
Then Newton's Second law is equivalent to the sum of the forces applied onto the particles, is equivalent to the force exterior applied to the Center of Mass: 
$$
\sum^N_{j=1}\vec{f_{j}^{ext}} = \vec{F}_{ext} =M\vec{a}_{\text{center of mass}}
$$

Then the position of the Center of Mass can be given by: 
$$
\vec{r}_{CM} = \frac{1}{M}\sum^N_{j=1}m_{j}\vec{r}_{j}
$$
Where $\vec{r}_{j}$ is defined around a certain origin point; normally one of the points. Refer to [[16 — Center of Mass and Rockets#Extending Newtonian Mechanics|the section in the pre-lecture notes]] for a detailed derivation of this equation; note that if we say now that our object is made out of infinitely many particles with some minute mass $dm$  and distance $dr$; then we should be able to equate this for a continuous system. Refer to this document for information pertaining to solving this: https://tutorial.math.lamar.edu/classes/calcii/centerofmass.aspx

However, for a continuous object; then this can be defined as: 
$$
\boxed{\vec{r}_{CM} = \frac{1}{M}\int_{m_{0}}^m \vec{r}dm}
$$
Note that $dm$ can be defined as some factor of $\rho lr$, or some factor of constant density across an object. For instance, you can set $m = \rho br,$, then $dm=\rho b dr$

> Example 
> Where is the center of mass of a quarter of a solid circle? 

Note that by symmetry; we should know that $x_{cm}=y_{cm}$; thus we need to solely find $x_{cm}$. 

For an infinitesimal element, we know it has some $dM$ , with a height of $y$ and a width of $dx$, thus: 
$$
dA = ydx
$$
Note from Pythagorean Theorem, then: 
$$
\begin{align}
x^2 + y^2 = R^2 \\
y = \sqrt{ R^2-x^2 }
\end{align}
$$
Then: 
$$
\begin{align}
dA = \sqrt{ R^2-x^2 } \ dx
\end{align}
$$
Note that the area of the entire circle is: 
$$
A = \pi R^2 \implies A = \frac{\pi R^2}{4}
$$
Since we're analyzing a quarter of our circle; then: 
$$
\begin{align}
dm = \frac{M}{A}dA\\
 & =\frac{M}{\frac{\pi R^2}{4}}dA \\
 dm& =\frac{4M}{\pi R^2}\sqrt{ R^2-x^2 }dx
\end{align}
$$
Thus: 
$$
\begin{align}
x_{com} & = \frac{1}{M}\int x \ dM \\
x_{com} & = \frac{1}{M}\int_{0}^R x *\frac{4M}{\pi R^2}\sqrt{ R^2-x^2 } \ dx \\
x_{com} & = \frac{4}{\pi R^2}\int_{0}^R x\sqrt{ R^2-x^2 } \ dx  &  u = R^2 - x^2 \implies \frac{du}{dx} = -2x \\
\end{align}

$$
Note with 
$$
\begin{align}
\frac{du}{dx}=-2x  \\
du=-2xdx \\
-\frac{du}{2} = xdx
\end{align}
$$
Then: 
$$
\begin{align}
x_{com} & = \frac{4}{\pi R^2}\int_{0}^R \sqrt{ R^2-x^2 } \ xdx \\
x_{com} & = \frac{4}{\pi R^2}\int_{0}^R -u^{1/2}\frac{1}{2}du = \frac{4}{\pi R^2}\int_{0}^R-\frac{u^{1/2}}{2} \\
 & =\frac{4}{\pi R^2} \left[ -\frac{1}{2} * \frac{2}{3} u^{3/2} \right] = \frac{4}{\pi R^2}\left[ -\frac{1}{3} u^{3/2} \right]_{0}^R \\
 & =-\frac{4}{3\pi R^2}[u^{3/2}]_{0}^R  & \text{Resub } u = R^2-x^2\\ 
 & =-\frac{4}{3\pi R^2}[(R^2-R^2)^{3/2} - (R^2-0^2)^{3/2} ] \\
 & =-\frac{4}{3\pi R^2}(-R^3) = \frac{4R}{3\pi}
\end{align}
$$
Since $x_{com}=y_{com}$, center of mass is present at $\left(\frac{4}{3\pi}, \frac{4}{3\pi} \right)$
## Rocket Equation (LEC)
The Rocket Equation arises from conservation of momentum; note that for a rocket: 
$$
\begin{align}
p_{i} = p_{f}
\end{align}
$$
For our rocket: 
$$
p_{fr} = (m-dm_{f})(v+dv)
$$
And for the gas present: 
$$
p_{fg} = dm_{g}u 
$$
Where $u$ is the exhaust velocity of our rocket; then setting $p_{i} = m_{0}v_{0}$ with $m=m_{0}$; then setting these equal: 
$$
\begin{align}
m_{0}v  & = (m_{0}-dm_{g})(v+dv) + dm_{g}(-u + v + dv)  \\
m_{0}v  & = m_{0}v + mdv - dm_{g}v -dm_{g}dv - dm_{g}u + dm_{g}v + dm_{g}dv  & dm_{g}dv \to 0\\
0 & = mdv   - dm_{g}u  & \text{note, } dm_{g}= -dm\\
dmu  & =mdv \\
dv & =\frac{1}{m_{0}}dmu  \\
\int_{v_{0}}^{v_{t}} dv & =-u\int_{m_{0}}^m \frac{1}{m}dm \\
\Delta v & =u[\ln(m_{0})-\ln (m)] = u\ln\left( \frac{m_{0}}{m} \right) \\
\Delta v & =u\ln\left( \frac{m}{m_{0}} \right)
\end{align}
$$


### Application
> A rocket is fired in deep space, where gravity is negligible. In the first second, it ejects $\frac{1}{160}$ of it's mass as exhaust gas, and has an acceleration of $15.2$m/s^2. What is the speed $u$ of the exhaust gas relative to the rocket? 

Note:
$$
a=  \frac{\Delta v}{\Delta t} = 15.2
$$
Where $\Delta t =1s$, note that $\Delta m = m-m_{0} \implies\left( m_{0}-\frac{m_{0}}{160} \right) = m_{0} \left( 1-\frac{1}{160} \right)=m_{0}\left( \frac{159}{160} \right)=m$; then
$$
\begin{align}
a=\frac{\Delta v}{\Delta t} = \frac{u}{\Delta t}\ln\left( \frac{m_{0}}{m} \right) \\
\frac{a\Delta t}{\ln\left( \frac{m_{0}}{m} \right)} = u \\
\frac{15.2}{\ln\left( \frac{160}{159} \right)} =  2424.39206& 
\end{align}
$$


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


