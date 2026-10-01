---
updated_at: 2026-10-01T14:43:46.230-04:00
edited_seconds: 530
course: ESC103H1
tags:
  - Tutorial
  - ESC103H1
"Lecture #": -1
Lecture Date: 2026-09-30
Week: 4
---
Hub: [[ESC103 Hub]]
Previous: [[T2 - ESC103 Tutorial 2]]
Relevant Notes: 
```query
tag:#ESC103H1 [week:4]
```
--- 
# Questions 
1. Consider the plane that intersects the coordinate axes at $x=a$, $y=b$, $z=c$ where $a,b,c \neq 0$ scalars. Using the vector cross product, derive and show that the scalar equation of this plane is given by: $$\frac{x}{a}+\frac{y}{b}+\frac{z}{c} = 1$$
2. Find the vector equation for the line through $(-2,5,0)$ that is parallel to the planes $2x+y-4z=0$ and $-x+2y+3x+1=0$. 
3. Let $A,B,C(2,-1,1)$ be the vertices of a triangle when $\vec{AB}$ is parallel to $\begin{bmatrix}1\\-1\\1\end{bmatrix}$ and $\vec{AC}$ is parallel to $\begin{bmatrix}2\\0\\-1\end{bmatrix}$, and angle $C=90\degree$. Find the vector equation of the line through $B$ and $C$. 
4. Find all unit vectors parallel to the $yz$ plane that are orthogonal to the vector $\begin{bmatrix}3\\-1\\2\end{bmatrix}$. 
5. The volume of a tetrahedron is given by $\frac{1}{3}(\text{area of the base})(\text{height})$. Use this result to prove that the volume of a tetrahedron with sides defined by the vectors $\vec{a},\vec{b},\vec{c}$ is given by $\frac{1}{6}|\vec{a}\cdot(\vec{b}\times \vec{c})|$, taking the base to be defined by vectors $\vec{b}$ and $\vec{c}$. Note, $\vec{a}\cdot (\vec{b}\times \vec{c})$ is referred to as the scalar triple product.
6. Find the distance between the point $P(-3,1,3)$ and the plane $5x+z=3y-4$. 
7. Show that the planes $3x-y+6z=7$ and $-6x+2y-12z=1$ are parallel, and find the distance between the planes. 
8. Find the vector equation for the line in $\mathbb{R}^3$ that contains the point $P(-1,6,0)$ and is orthogonal to the plane $4x-z=5$
9. Find the scalar equation for the plane that is represented by the vector equation: $$\begin{bmatrix}x\\y\\z\end{bmatrix} = \begin{bmatrix}-1\\5\\6\end{bmatrix} + t\begin{bmatrix}0\\-1\\3\end{bmatrix} + s\begin{bmatrix}2\\-1\\0\end{bmatrix}$$
10. The equation $ax+by=0$ represents a line through the origin in $\mathbb{R}^2$ if $a$ and $b$ are not zero. What does this equation represent in $\mathbb{R}^3$ if you think of it as $ax+by+0z = 0$? Explain. 

11. Consider the following planes in $\mathbb{R}^3$: $$\begin{align}1x+0y+0z = 2 \\0x + 1y + 0z = 3 \\0x + 0y + 1z = 4\end{align}$$
	1. Construct a mental image of the row picture. 
	2. Express the 3 equations as a single vector equation. 
	3. Construct a mental image of the column picture. 
	4. What does the solution to these 3 equations represent in $\mathbb{R}^3$? 
12. Consider the following planes in $\mathbb{R}^3$: $$\begin{align}x + y + z &= 2 \\x + 2y + z &= 3 \\ 2x +3y + 2z &= 5 \end{align}$$
	1. Express these 3 equations as a single vector equation.
	2. Find two linear combinations of the column vectors on the left hand side that equal the right hand side vector. 
	3. Show that it is only possible to find linear combinations of the column vectors on the left-hand side when the right-hand side vector is equal to $\begin{bmatrix}4\\6\\ c\end{bmatrix}$ and $c$ is equal to what value? 
	4. Express these 3 equations in the form of $A\vec{v}=\vec{b}$. 

# Answers

> *Question 1:* 
> > Consider the plane that intersects the coordinate axes at $x=a$, $y=b$, $z=c$ where $a,b,c \neq 0$ scalars. Using the vector cross product, derive and show that the scalar equation of this plane is given by: $$\frac{x}{a}+\frac{y}{b}+\frac{z}{c} = 1$$
> 
> Let $x=a,y=b,z=c$. If we say these points exist on the plane, then the following are vectors which also exist on the plane: 
> $$\vec{ac} = \begin{bmatrix}-a\\0\\c\end{bmatrix},\vec{ab}= \begin{bmatrix}-a\\b\\0\end{bmatrix}$$Which means that the cross product of these two vectors give us the normal vector of this plane: 
> $$\vec{n}=\vec{ac} \times \vec{ab} = \det \begin{bmatrix}\hat{i} & \hat{j} & \hat{k} \\-a & 0 & c \\-a & b & 0\end{bmatrix} = \begin{bmatrix}-bc\\-ac\\-ab\end{bmatrix}$$
> Which means that the following is the corresponding scalar equation of our plane: 
> $$-bcx -acy-abz = d \tag{1}$$
> Sub in the point $(0,0,c)$ into our equation, then
> $$\begin{align}-bc(0) -ac(0)-ab(c) &= d \\-abc&=d\end{align}$$Resubstitute as $d$ back into $1$: 
> $$\begin{align}-bcx -acy-abz &= d \tag{1} \\-bcx -acy-abz &= -abc \\\frac{-bcx}{-abc} + \frac{-acy}{-abc} + \frac{-abz}{-abc} &= 1 \\\frac{x}{a} + \frac{y}{b} + \frac{z}{c} = 1\end{align}$$Therefore, the equation of this plane is the equation of $\frac{x}{a}+\frac{y}{b}+\frac{z}{c} = 1$. 

> *Question 2:*
> > Find the vector equation for the line through $(-2,5,0)$ that is parallel to the planes $2x+y-4z=0$ and $-x+2y+3x+1=0$. 
> 
> Note that a line parallel through the two planes listed is therefore perpendicular to both planes; or in other words, the direction vector provided by this point is given by the cross product of the normal vectors present: $$\begin{bmatrix}2\\1\\-4\end{bmatrix} \times \begin{bmatrix}-1\\2\\3\end{bmatrix} = \det \begin{bmatrix}\hat{i} & \hat{j} & \hat{k} \\2 & 1 & -4 \\-1 & 2 & 3 \end{bmatrix} = \begin{bmatrix}11 \\2\\5\end{bmatrix}$$Therefore our line is defined by the following: $$\begin{bmatrix}x\\y\\z\end{bmatrix} = \begin{bmatrix}11\\2\\5\end{bmatrix}t + \begin{bmatrix}-2\\5\\0\end{bmatrix}$$

> *Question 3:*
> > Let $A,B,C(2,-1,1)$ be the vertices of a triangle when $\vec{AB}$ is parallel to $\begin{bmatrix}1\\-1\\1\end{bmatrix}$ and $\vec{AC}$ is parallel to $\begin{bmatrix}2\\0\\-1\end{bmatrix}$, and angle $C=90\degree$. Find the vector equation of the line through $B$ and $C$. 
> 
> 