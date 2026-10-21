---
updated_at: 2026-10-20T22:56:41.902-04:00
edited_seconds: 1340
course:
tags:
"Lecture #": 0
Lecture Date: 2026-10-20
Week:
---
Hub: [[PHY180 Hub]]
Connected Notes: 
* [[17 — Rotational Kinematics, Rotational Variables]]
* [[18 — Moment of Inertia, Torque]]
* [[19 —Newton's Second Law for Rotation, Rotational Energy]]

Previous Assignment: [[A5 — PHY180 Assignment 5]]
Next: N/A

> [!caution]
> ok i got lazy and didnt bother to write down the questions. 

---

> Question 1
> Which of the following is the best explanation of why it is difficult for a high speed car to stay on the road when it is going around an unbanked turn?
> A. There is a very large force pushing the car outward, away from the centre of circular motion.
> B. There is a very large kinetic friction force pushing the car in a direction opposite its velocity.
> C. There is a very large force of air resistance pushing the car in a direction opposite its velocity.
> D. It requires a very large static friction force to provide the necessary inward force, pushing the car toward the centre of circular motion.
> E. It requires a very large torque for the driver to turn the steering wheel.
> > D: A very high $v_{t}$ implies, that to maintain the same radius $r$, $a_{c}$ scales appropriately. This links to the centripetal force, which is the net force of the system. For a car turning quickly on an unbanked road, this is solely provided by friction, thus the static friction force needs to be very high in order to maintain the turn without skidding out.  

> Question 2
> A clock is mounted on the wall. As you look at it, what is the direction of the angular velocity vector of the second hand? 
> > Into the clock hand / wall.

> Question 3,4
> A flywheel slows from 600 to 400 rev/min while rotating through 40 revolutions. 
> a) What is the angular acceleration of the flywheel? (-15,708 rad/s^2)
> b) How much time elapses during the 40 revolutions? (0.02546s)

First, we convert the angular velocity terms into radians: 
$$
\begin{align}
\frac{600}{60}*2\pi = 20\pi = \omega_{0} \\
\frac{400}{60} * 2\pi =13.33\pi =\omega _{1}
\end{align}
$$
Where $d\theta =80\pi$, then: 
$$
\begin{align}
\omega_{t}^2  & = \omega_{0}^2 + 2\alpha d\theta \\
\frac{\omega_{t}^2 - \omega_{0}^2}{2d\theta} & =\alpha \\
\alpha=\frac{800^2\pi^2-1200^2\pi^2}{160\pi}  & =\left( \frac{800^2-1200^2}{160} \right)\pi \approx-15,708 \frac{\text{rad}}{m^2} = -43.63323130
\end{align}
$$

For the second part, plugging this into $a$ and solving for $t$ in a constant angular acceleration equation gives us: 
$$
\begin{align}
\omega_{t}  & = \omega_{0} + \alpha t \\
\frac{\omega_{t}-\omega_{0}}{\alpha}  & = t \\
\frac{800-1200}{-43.63323130}  & \approx 9.1673~s
\end{align}
$$

> Question 5
> ![[A6 - PHY180 Assignment 6-1792535102194.webp]]

The angle can be found by integrating this graph; which can be seen as the area of a triangle, thus 
$$
\theta = \frac{\left( \frac{400}{60}*8 \right)}{2} \approx 26.\bar{6}  *2\pi = 167.551~\text{rad}
$$

> Question 6
> ![[A6 - PHY180 Assignment 6-1792535262000.webp]]

At it's peak, a tornado is 60.0m in diameter and carries 500km/h winds. What is it's angular velocity in radians per second?

Assume that winds are tangential, measured at the edge of the tornado; thus $r=60m$ and $v_{t} = 500 \frac{km}{h} = 138.\bar{8} \frac{m}{s}$; Then: 
$$
\begin{align}
v_{t} = r\omega_{t} \\
\frac{v_{t}}{r} = \omega_{t} \\
\frac{138.8}{30}  & \approx 4.629629630 \frac{\text{rad}}{s} = 29.09 rps
\end{align}
$$

> Question 7
> ![[A6 - PHY180 Assignment 6-1792535486821.webp]]

Recall that we define rotational kinetic energy by substituting mass with $I$ and $v$ with $\omega$; then: 
$$
\begin{align}
K  & = \frac{1}{2}I\omega^2 \\
\sqrt{ \frac{2K}{I} }  & = \omega \\
\sqrt{ \frac{2(100)}{9.0} } & =\omega \approx 4.714045208 \frac{\text{rad}}{s}
\end{align}
$$

> Question 8: 
> ![[A6 - PHY180 Assignment 6-1792535665158.webp]]

Using the torque equation; then we can solve for $t$, set all of the values to be scalar values; then: 
$$
\begin{align}
\tau &  = rF_{t}\sin\theta \\
\frac{\tau}{r\sin\theta} & =F_{t} \\
\frac{5.00\times 10^3}{6*\sin(30)} & \approx 1,666.6666\bar{6} \text{ N}
\end{align}
$$

> Question 9,10
> ![[A6 - PHY180 Assignment 6-1792535803914.webp]]

Assuming that a constant acceleration was applied; we can solve for $\alpha$ from $\frac{d\omega}{dt}$; that is: 
$$
\alpha = \frac{200}{5} = 40 \frac{\text{ rad}}{s}
$$
Then, using N2L: 
$$
\begin{align}
\tau &  = I\alpha \\
 & =50*40 = 2000 ~ \text{N}
\end{align}

$$

> Question 11: 
> ![[A6 - PHY180 Assignment 6-1792545985331.webp]]

Consider the forces present at $m_{1}$; that is: 
$$
\begin{align}
\sum F = m_{1}g - F_{t_{1}} = m_{1}a \\
F_{t_{1}} = m_{1}g-m_{1}a = m_{1}(g-a)
\end{align}
$$
Consider now the forces present around $m_{2}$, that is: 
$$
\begin{align}
\sum F = F_{2t} = m_{2}a = 2m_{1}a \\
F_{2t} = 2m_{1}a
\end{align}
$$
Consider now that both of these rope forces are acting on the pulley on the radius. Note that with the RHL convention on signs; , $\alpha r$ is actually pointing towards an acceleration towards the left, which is negative. In our case; we have to say that $a_{t}=-\alpha r$
$$
\begin{align}
\sum \tau  & = rF_{t2} - rF_{t1 } = I\alpha  & a_{t} = \alpha r \\
-\frac{r(F_{t_{2}}-F_{t_{1}})}{I} & =\alpha
\end{align}
$$
Then: 
$$
\begin{align}
-\frac{r^2(F_{t_{2}}-F_{t_{1}})}{I}  & = a_{t} \\
-\frac{r^2(2m_{1}a - m_{1}g+m_{1}a)}{I} & =a_{t} \\
-3r^2m_{1}a + r^2m_{1}g  & =a_{t}I  \\
r^2m_{1}g & =aI + 3r^2m_{1}a \\
\frac{r^2m_{1}g}{(I+3r^2m_{1})}  & =a \\
\frac{(0.2^2)(2)(9.8)}{(0.4 + 3(0.2^2)2)}  & =1.225 \frac{~m}{s^2}
\end{align}
$$

> Question 12
> ![[A6 - PHY180 Assignment 6-1792549265699.webp]]

Recall that we defined Work as the force applied over a rotational quadrant; that is an angle measure: 
$$
dw= F\cdot d\theta
$$
Recall that $dP = \frac{dw}{dt}$, then $dP = \tau\cdot \frac{d\theta}{dt} = \tau\cdot \omega$, then with the applied forces present: 
$$
\begin{align}
dP  & = -1*0.2*20\pi = -12.5663W
\end{align}
$$
Thus, to ensure that the wheel has to keep rotating at a constant rate, then $dP_{potter}=12.5663J$

> Question 13
> ![[A6 - PHY180 Assignment 6-1792549561437.webp]]

Consider for Circle A: 
$$
\sum \tau = F_{a}r = I_{a}\alpha \implies \frac{F_{a}r}{I_{a}} = \alpha_{a}
$$
For a disk; with the same uniform board, we can assume that $\sigma$ is the same; then: 
$$
I_{a} = \frac{\sigma r^3}{2}
$$
Then, for circle $b$ with $r=2r$, then: 
$$
I_{b} = \frac{\sigma 8r^3}{2} = 8I_{a}
$$
Then:
$$
\begin{align}
\sum\tau = 2F_{a}2r  & = 8I_{a}\alpha _{b} \\
\alpha_{b}=\frac{F_{a}r}{2I_{a}} = \frac{1}{2}\alpha_{a}
\end{align}
$$
Then $\alpha_{a}=2\alpha_{b}$; thus the answer is B. 

> Question 14
> ![[A6 - PHY180 Assignment 6-1792550097711.webp]]

Using equilibrium on $m_{2}$: 
$$
\begin{align}
\sum F : m_{2}g - F_{t}  & = m_{2}a \\
F_{t} & =m_{2}g-m_{2}a
\end{align}
$$
Let downwards be positive, then $+\alpha\to+x$; Taking the net torque: 
$$
\begin{align}
\sum \tau  & = F_{t}r = I\alpha \\
\frac{r(m_{2}g-m_{2}a)}{I}  & = \alpha  & a = \alpha r \\
\frac{r^2(m_{2}g-m_{2}a)}{I} & =a \\
r^2m_{2}g - r^2m_{2}a  & = Ia \\
r^2m_{2}g  & =Ia + r^2m_{2}a \\
\frac{r^2m_{2}g}{I + r^2m_{2}} & =a = \frac{(0.2^2)(2.5)(9.8)}{0.05 + 0.2^2*2.5} ={6}.5\bar{3}  \frac{m}{s^2}
\end{align}
$$

