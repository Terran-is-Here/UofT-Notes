---
updated_at: 2026-10-20T18:28:15.808-04:00
edited_seconds: 520
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
600*2\pi = 1200\pi & =\omega_{0}\\
400*2\pi = 800\pi & = \omega _{t}
\end{align}
$$
Where $d\theta =80\pi$, then: 
$$
\begin{align}
\omega_{t}^2  & = \omega_{0}^2 + 2\alpha d\theta \\
\frac{\omega_{t}^2 - \omega_{0}^2}{2d\theta} & =\alpha \\
\alpha=\frac{800^2\pi^2-1200^2\pi^2}{160\pi}  & =\left( \frac{800^2-1200^2}{160} \right)\pi \approx-15,708 \frac{\text{rad}}{s^2}
\end{align}
$$

For the second part, plugging this into $a$ and solving for $t$ in a constant angular acceleration equation gives us: 
$$
\begin{align}
\omega_{t}  & = \omega_{0} + \alpha t \\
\frac{\omega_{t}-\omega_{0}}{\alpha}  & = t \\
\frac{800-1200}{-15708}  & \approx 0.025464731~s
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

Assume that winds are tangential, measured at the edge of the tornado; thus $r=60m$ and $v_{t} = 500 \frac{km}{h} = 138.\bar{8} \frac{m}{s}$; 