---
updated_at: 2026-10-12T13:40:44.713-04:00
edited_seconds: 850
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
* [[15 — Conservation of Momentum, Collisions]]
* [[16 — Center of Mass and Rockets]]
---
Questions taken from [[hw5.pdf]]: 

> Question 1: 
> Acceleration decreases, speed increases (tangential acceleration from gravity decreases; but maintains velocity / keeps gaining a smaller amount of it) 

> Question 2: 
> A particle of mass $2.0\ kg$ moves under influence of the force $F(x) = \frac{3}{\sqrt{ x }}$. If it's speed at $x=2.0\ m$  is $6.0m/s$, what is it's speed at $x=7$? 
> > $$\begin{align}W = \Delta K &  = \int_{2}^7F(x) dx \\& =\left[ -\frac{3}{2(\sqrt{ x })^3} \right]_{2}^7 \\& =\left[ -\frac{3}{2(\sqrt{ 7 })^3} + \frac{3}{2\sqrt{ 2 }^3} \right] \\& \approx 0.449337699J\end{align}$$$$\begin{align}W  & = E_{k_{t}}-E_{k_{0}} \\W + E_{k_{0}} & =E_{kt}   \\\left( W + \frac{1}{2}mv_{0}^2 \right)  & =\frac{1}{2}mv^2 \\\sqrt{ \frac{2\left( W + \frac{1}{2}mv_{0}^2 \right)}{m} }  & =v \\v & =\sqrt{ \frac{2\left( 0.449337699 + \frac{1}{2}(2)(6)^2 \right)}{2} } \\v & \approx 6.037328689\ \frac{m}{s}\end{align}$$

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

> Question 5: 
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
Solve via Quadratic Formula; then we get $\Delta h=36.86$m Then the height of our jumper above the river will be $113.14$m 

> Question 6
>Two sailboats have identical size and shape, but sailboat A has a significantly larger mass than sailboat B. They are both subject to the same wind and the same constant net force as they start from rest and move the same distance of 100 m. After traveling 100 m (multiple choice question)
> If $F$ is constant for both; then $dm$ is the same for both over some time period $\Delta t$; but since $m_{a} > m_{b}$; then $v_{a}<v_{b}$; Since $v_{a}<v_{b}$; Boat A will have less kinetic energy than B, but both would have the same momentum. 

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

> For analysis, assume the object is of a mass o
> 
