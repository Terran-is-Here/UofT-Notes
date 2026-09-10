---
updated_at: 2026-09-10T13:43:34.739-04:00
edited_seconds: 260
course: ESC194H1
tags:
  - ESC194H1
"Lecture #": 0
Date: 2026-09-10
Week:
---
Hub: [[ESC194 Hub]]
Previous: N/A 
Next: [[02 — The Real Number System]]

--- 

# Lecture Notes 
## Origin of Calculus / Some Problems
One of the early challenges where calculus is involved within a mathematical problem was attempting to find the precise area of a circle within Ancient Greece. Originally; mathematicians inscribed a rectangle within a circle; taking it's 4 triangular quadrants as it's area. 

They assumed that by increasing the number of triangular quadrants (ergo sides) to infinity; you would eventually attain the area of the circle (a concept they termed as exhaustion) 



# Pre-Written Notes
## The Tangent Problem
The concept of the *limit* arises during our attempts to derive the concept of taking the slope of a line *tangent* to an equation. Our traditional methods of deriving the slope of a line are only effective for finding the slope of a *secant* line: 
$$
m=\frac{y_{2}-y_{1}}{x_{2}-x_{1}}
$$
This equation requires us to find two points for us in order to find the slope; effectively preventing us from actually... finding the equation of the tangent (which by def. is only limited to only one point) 

We define the concept of the slope of the tangent line by it being the limit of the respective slope of our secant; or: 
$$
m_{s}=\lim_{ y_{2} \to y_{1} } \frac{y_{2}-y_{1}}{x_{2}-x_{1}}
$$

## The Velocity Problem 
A similar problem to our tangent problem arises when we want to derive what the concept of *instantaneous* velocity means. Velocity is broadly defined as: 
$$
v = \frac{ds(t)}{dt}
$$
Where $s(t)$ maps $t\in[T]$ and $s\in[L]$. 
Or; in terms of our slope formula: 
$$m=\frac{y_{2}-y_{1}}{x_{2}-x_{1}}$$
Where our points are equivalent to our $(t,v)$ pairs; alternatively defined as: 
$$m=\frac{s(t_{2})-s(t_{1})}{t_{2}-t_{1}}$$
If $t_{2} > t_{1}$, we can define $t_{2}$ in terms of $t_{1}$ with a certain value between them: $t_{2}-t_{1} = h$, then $t_{2} = t_{1} + h$. 
Subbing this into our expression: 
$$
m=\frac{s(t_{1} + h)-s(t_{1})}{t_{1} + h-t_{1}}
$$
Cancelling out our respective denominator terms: 
$$
m=\frac{s(t_{1} + h)-s(t_{1})}{h}
$$
Since $h$ is the effective distance between our two measurements / points; taking the limit of this as $h$ approaches 0 gives us our definition for instantaneous velocity: 
$$
m=\lim_{ h \to 0 } \frac{s(t_{1} + h)-s(t_{1})}{h}
$$
Which is basically equivalently formed as the Limit Definition of a Derivative. 