---
updated_at: 2026-10-18T12:44:59.125-04:00
edited_seconds: 1570
course: PHY180H1
tags:
  - Assignment
  - PHY180H1
"Assignment #": 5
Lecture Date: 2026-09-22
Week:
---
Hub: [[PHY180 Hub]]
Connected Notes: 
* [[12 — Potential Energy, Conservative and Non-Conservative Forces]]
* [[13 — Conservation of Energy, Stability]]
* [[14 — Momentum and Impulse]]
* [[15 — Conservation of (Translational) Momentum, Collisions]]
* [[16 — Center of Mass and Rockets]]
---
Questions taken from [[hw5.pdf]]: 

> Question 1: 
> Acceleration decreases, speed increases (tangential acceleration from gravity decreases; but maintains velocity / keeps gaining a smaller amount of it) (D)

> Question 2: 
> A particle of mass $2.0\ kg$ moves under influence of the force $F(x) = \frac{3}{\sqrt{ x }}$. If it's speed at $x=2.0\ m$  is $6.0m/s$, what is it's speed at $x=7$? 
> > $$\begin{align}W = \Delta K &  = \int_{2}^7 F(x)dx \\& =3 \int_{2}^7 x^{-1/2}dx \\& =3[2\sqrt{ x }]^7_{2} \\& =6[\sqrt{ 7 }-\sqrt{ 2 }] \approx 7.389226492\ J\end{align}$$$$\begin{align}W  & = E_{k_{t}}-E_{k_{0}} \\W + E_{k_{0}} & =E_{kt}   \\\left( W + \frac{1}{2}mv_{0}^2 \right)  & =\frac{1}{2}mv^2 \\\sqrt{ \frac{2\left( W + \frac{1}{2}mv_{0}^2 \right)}{m} }  & =v \\v & =\sqrt{ \frac{2\left( 7.389226492 + \frac{1}{2}(2)(6)^2 \right)}{2} } \\v & \approx 6.587049908\ \frac{m}{s}\end{align}$$





> Question 3: 
> A $5.00\times 10^5$ kg subway train is brought to a stop from a speed of $0.500 \frac{m}{s}$ in $0.400\ m$ by a large spring bumper at the end of it's track. What is $k$ for this spring bumper? 
$$
\begin{align}
\frac{1}{2}mv^2 + \frac{1}{2}k(0)^2  & = \frac{1}{2}m(0)^2 + \frac{1}{2}k\Delta x^2 \\
\frac{1}{2}mv^2  & =\frac{1}{2}k\Delta x^2 \\
mv^2 & =k\Delta x^2 \\
k  & =\frac{mv^2}{\Delta x^2} = \frac{5\times 10^5 \times(0.5^2)}{(0.4)^2} =781250 \frac{N}{m}
\end{align}
$$

> Question 4: 
> How much energy is lost to a dissipative drag force if a $60$kg person falls at constant speed for 15m? 
> 
> If a person falls at constant speed; then the drag force is equal to the force of gravity on our person; thus $F_{d} = F_{g}$. We also know that this force would be constant (as $mgh$ is a constant force, and $F_{d}$ will asymomatically approach it's maximum being equal to the terminal velocity); thus: $$\begin{align}W_{L}  & =\int_{0}^{15]}mg dh \\& =mg(15) = 60(9.8)(15) = 8820J\end{align}$$

> Question 5 *: 
> An 80.0 kg bungee jumper drops from rest off a bridge that is 200.0 m above a river. As he falls, air resistance is negligible, and the unstretched bungee cord attached to him uncoils. 
> 
> When the jumper is 50.0 m below the bridge, the bungee cord is completely uncoiled and forms a straight line. Below that point, the bungee cord acts as a spring, obeying Hooke’s law as it is stretched beyond its equilibrium length of 50.0 m, with a spring constant of k = 15N/m. How far above the river will the jumper be when he first momentarily stops?

Solve via conservation of energy; taking analysis at maximum height, and at height of corresponding spring equilibrium: 
$$
\begin{align}
mgh & =mg(h-50-\Delta h) + \frac{1}{2}k\Delta h^2 \\
mg(200) & =mg(150-\Delta h) + \frac{1}{2}k\Delta h^2 \\
mg(50) & =-mg\Delta h + \frac{1}{2}k\Delta h^2 \\
0  & =-(80)(9.8)(50) - (80)(9.8)\Delta h + 7.5\Delta h^2 \\
 & = -39200 - 787\Delta h + 7.5\Delta h^2
\end{align}
$$
Solve via Quadratic Formula; then we get $\Delta h=141.4769302, -36.94$m Then the height of our jumper above the river will be $8.5230698$m 

> Question 6 **
>Two sailboats have identical size and shape, but sailboat A has a significantly larger mass than sailboat B. They are both subject to the same wind and the same constant net force as they start from rest and move the same distance of 100 m. After traveling 100 m (multiple choice question)

Consider if an applied net force $F$ was applied over a distance $d$ to two objects, $m$ and $xm$; where $xm$ represents our larger structure, $x>1$. Their corresponding kinetic energies are as follows: 
$$
\begin{align}
Fd  & = \frac{1}{2}mv_{1}^2 \implies v_{1}=\sqrt{ \frac{2Fd}{m} }\\ \\
Fd  & =\frac{1}{2}xmv^2_{2} \implies v_{2} = \sqrt{ \frac{2Fd}{xm} }
\end{align}
$$
Which makes sense; our objects would have the same kinetic energy. Consider now their momentums: 
$$
\begin{align}
m_{1}v_{1}  & = m\sqrt{ \frac{2Fd}{m} } =\sqrt{ m 2Fd }\\
m_{2}v_{2} & =xm\sqrt{ \frac{2Fd}{xm} } = \sqrt{2xmFd }
\end{align}
$$
Considering now for our above cases; then: 
$$
\begin{array}{cc|cc}
\text{Boat A} &  & \text{Boat B} \\
\frac{1}{2}xmv_{1}^2 &  & \frac{1}{2}mv_{2}^2 \\
\sqrt{2xmFd } &  & \sqrt{ 2mFd }
\end{array}
$$
Since the same net force is applied onto both boats; their kinetic energies would be equal. However, due to the mass difference, the *Momentum* of boat $A$ will always be larger than boat $B$; That is: 
$$
\begin{align}
\frac{1}{2}xmv_{1}^2 &  = \frac{1}{2}mv_{2}^2 & \text{Object Kinetic Energies} \\
\sqrt{ 2xmFd } &  > \sqrt{ 2xmFd } &  \iff x>1, \text{Object Momentums}
\end{align}
$$
The answer for 6 is therefore B. 

> Question 7
> A croquet mallet balances when suspended from its center of mass, as shown in the left part of the figure. If you cut the mallet into two pieces at its center of mass, as shown in the right part of the figure, how do the masses of the two pieces compare?
> 
> The answer to this will be C. (i think) 

> Question 8
> A 2000-kg railway car coasts at 4.4m/s underneath a grain terminal, which dumps grain directly down into the freight car. If the speed of the unloaded freight car must not go below 3.0m/s, what is the maximum mass of grain it can accept? 

> For this case, solve for the mass of our final object via Conservation of Momentum: 

$$
\begin{align}
m_{0}v_{0} &  = m_{1}v_{1} \\
\frac{m_{0}v_{0}}{v_{1}} & =m_{1} \\
\frac{(2000)(4.4)}{(3.0)}  & =m_{1}  \\
m_{1} & =2933.\bar{3}\ kg
\end{align}
$$
Since the initial weight of the railway car was $2000\ kg$, then the maximum mass of grain acceptable would be a value of around $933.\bar{3}$ kg. 

> Question 9
> A 100-g firecracker is launched vertically into the air and explodes into two pieces at the peak of it's trajectory. If a 72-g piece is projected horizontally to the left at 20m/s, what is it's speed and direction of the other piece? 
> > Solve via Conservation of Momentum: 
> > Define left as negative, then
$$
\begin{align}
0 &  =(72)(-20) + 28v \\
\frac{1440}{28} & =v = 51.4285\ \frac{m}{s}
\end{align}
$$

> Question 10
> Two cars of the same mass approach an extremely icy four-way perpendicular intersection, Car A travels northward at 30m/s, and car B is travelling eastward. They collide and stick together, travelling at 28 degrees north of east. What was the initial velocity of Car B? 

> Solve via cardinal dimensions. 
> Solving the Y dimension first; then: 


$$
\begin{align}
mv = 2mv'_{x} \\
v'_{x}=\frac{1}{2}v = 15\ \frac{m}{s}
\end{align}
$$
Using trig, we can solve for the corresponding $x$ component, then: 
$$
v'_{x} = \frac{15}{\tan 28}
$$
From here, then using $x$ dimension then: 
$$
\begin{align}
mv_{x} = 2mv'_{x} \\
v_{x} = 2v'_{x} = \frac{30}{\tan 28} \approx 58.42179396\ \frac{m}{s}
\end{align}
$$

> Question 11
> Determine the $x$ position of the center of mass; with $x$ defined in the diagram. 

> For analysis, assume the object is of a dimension of $1\times 1$ meters; to simplify the corresponding $dm$ terms; then the corresponding linear density is $8 \frac{g}{cm}$  and $2.4 \frac{g}{cm}$; then our total $M = 520g$; solving for the center of mass; then: 

$$
X_{c} = \frac{1}{M} \left( \int_{0}^{50}xdm_{Fe} + \int_{50}^{100}xdm_{Al} \right)
$$
Note that $dm_{Fe} = 8*dx$, and $dm_{Al} = 2.4dx$; then: 
$$
\begin{align}
X_{c}  & = \frac{1}{M} \left( \int_{0}^{50}8xdx + \int_{50}^{100}2.4xdx \right) \\
X_{c}  & = \frac{1}{M}\left[  \left( \frac{8x^2}{x} \right)^{50}_{0 } + \left( \frac{2.4x^2}{2} \right)_{50}^{100} \right] \\
\end{align}
$$
Evaluating the integrals separately; then: 
$$
\begin{align}
4x^2|_{0}^{50} &  = 10000 \\
1.2x^2|_{50}^{100}  & = 1.2(100)^2 -1.2(50)^2=9000
\end{align}
$$
Thus: 
$$
X_{c} = \frac{(19000)}{520} \approx 36.53846154 \ cm
$$

> Question 12 **
> A rocket takes off from Earth and reaches a speed of 100m/s in 10s. If the exhaust speed is 1500m/s, and the mass of fuel burned was 100kg, what is the original mass ($m_{0}$) of the rocket? 

> Taking into account the Rocket Equation with gravity: 

$$
\Delta v = u\ln\left( \frac{m_{0}}{m_{r}} \right) - g\Delta t
$$
Note that $m_{0}=m_{r}+m_{f}$; then: 
$$
\begin{align}
\Delta v & =u\ln \left( \frac{m_{0}}{m_{r}} = \frac{m_{r}+m_{f}}{m_{r}} \right)-g\Delta t \\
\frac{\Delta v + g\Delta t}{u}  & = \ln\left( \frac{m_{r}+m_{f}}{m_{r}} \right) \\
e^{\frac{\Delta v + g\Delta t}{u}} &  = \frac{m_{r}+m_{f}}{m_{r}} \\
m_{r}  & =\frac{m_{f}}{e^{\frac{\Delta v + g\Delta t}{u}}-1}
\end{align}
$$
Subbing in our values; then: 
$$
m_{r} = \frac{100}{e^{\frac{100+ 9.8*10}{1500}}-1} \approx 708.6754383 \ kg
$$
Then, $m_{0}=808.6754383 \ kg$

> Question 13
> A big wagon with a mass of 250kg is initially rolling without friction at 3.00m/s. It starts to rain, and the rain accumulates in the wagon at the constant rate of 10.0kg/hr. The rain is falling straight down. After 2 hours of rain, what is the speed of the wagon? 

> Apply conservation of Momentum as usual; 

$$
\begin{align}
m_{0}v_{0} & =m_{1}v_{1} \\
\frac{m_{0}v_{0}}{m_{1}} & =v_{1}  & m_{1} = m_{0} + 20 \implies m_{1}=270 \\
\frac{(250)(3)}{270} & =v_{1}\approx 2.\bar{7} \ \frac{m}{s}
\end{align}
$$

> Question 14,15
> A puck of mass m1 = 0.2 kg is sliding on an ice table without friction. Its initial velocity is along the x-axis with v0 = 10 m/s as shown in the figure. 
> The puck collides elastically with an identical puck, m2, which is initially at rest. The pucks exit the collision as shown in the figure.
> 
> It is observed that, after the collision, the velocity components of puck 2 are =(8.6 m/s, −3.5 m/s).
> > Question 14: What is the x component of puck 1 after the collision? (Trivial examination; 1.4m/s)
> > Question 15: What is the y component of puck 1 after the collision? (Trivial examination, 3.5 m/s)
> 
> 