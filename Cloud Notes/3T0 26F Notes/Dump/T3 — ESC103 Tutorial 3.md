---
updated_at: 2026-10-07T09:02:41.196-04:00
edited_seconds: 1800
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
Relevant Notes: [[T4- ESC103 Tutorial 4]]
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

> [!theorem] Question 1:
> > Consider the plane that intersects the coordinate axes at $x=a$, $y=b$, $z=c$ where $a,b,c \neq 0$ scalars. Using the vector cross product, derive and show that the scalar equation of this plane is given by: $$\frac{x}{a}+\frac{y}{b}+\frac{z}{c} = 1$$
> 
> > [!caution]- Answer
> > Let $x=a,y=b,z=c$. If we say these points exist on the plane, then the following are vectors which also exist on the plane: 
> > $$\vec{ac} = \begin{bmatrix}-a\\0\\c\end{bmatrix},\vec{ab}= \begin{bmatrix}-a\\b\\0\end{bmatrix}$$Which means that the cross product of these two vectors give us the normal vector of this plane: 
> > $$\vec{n}=\vec{ac} \times \vec{ab} = \det \begin{bmatrix}\hat{i} & \hat{j} & \hat{k} \\-a & 0 & c \\-a & b & 0\end{bmatrix} = \begin{bmatrix}-bc\\-ac\\-ab\end{bmatrix}$$
> > Which means that the following is the corresponding scalar equation of our plane: 
> > $$-bcx -acy-abz = d \tag{1}$$
> > Sub in the point $(0,0,c)$ into our equation, then
> > $$\begin{align}-bc(0) -ac(0)-ab(c) &= d \\-abc&=d\end{align}$$Resubstitute as $d$ back into $1$: 
> > $$\begin{align}-bcx -acy-abz &= d \tag{1} \\-bcx -acy-abz &= -abc \\\frac{-bcx}{-abc} + \frac{-acy}{-abc} + \frac{-abz}{-abc} &= 1 \\\frac{x}{a} + \frac{y}{b} + \frac{z}{c} = 1\end{align}$$Therefore, the equation of this plane is the equation of $\frac{x}{a}+\frac{y}{b}+\frac{z}{c} = 1$. 

> [!theorem] Question 2:
> > Find the vector equation for the line through $(-2,5,0)$ that is parallel to the planes $2x+y-4z=0$ and $-x+2y+3x+1=0$. 
> 
> > [!caution]- Answer
> > Note that a line parallel through the two planes listed is therefore perpendicular to both planes; or in other words, the direction vector provided by this point is given by the cross product of the normal vectors present: $$\begin{bmatrix}2\\1\\-4\end{bmatrix} \times \begin{bmatrix}-1\\2\\3\end{bmatrix} = \det \begin{bmatrix}\hat{i} & \hat{j} & \hat{k} \\2 & 1 & -4 \\-1 & 2 & 3 \end{bmatrix} = \begin{bmatrix}11 \\2\\5\end{bmatrix}$$Therefore our line is defined by the following: $$\begin{bmatrix}x\\y\\z\end{bmatrix} = \begin{bmatrix}11\\2\\5\end{bmatrix}t + \begin{bmatrix}-2\\5\\0\end{bmatrix}$$

> [!theorem] Question 3:
> > Let $A,B,C(2,-1,1)$ be the vertices of a triangle when $\vec{AB}$ is parallel to $\begin{bmatrix}1\\-1\\1\end{bmatrix}$ and $\vec{AC}$ is parallel to $\begin{bmatrix}2\\0\\-1\end{bmatrix}$, and angle $C=90\degree$. Find the vector equation of the line through $B$ and $C$. 
>
> > [!caution]- Answer
> > Note that $\vec{AB}$ is parallel to $\begin{bmatrix}1\\-1\\1\end{bmatrix}$, meaning that $\vec{AC}=t\begin{bmatrix}1\\-1\\1\end{bmatrix}$ . Using the same logic, $\vec{AC} = s\begin{bmatrix}2\\0\\-1\end{bmatrix}$. $\vec{BC} = \vec{AC}-\vec{AB}$. Then: $$\begin{align}\vec{BC}&=\vec{AC}-\vec{AB} \\&=-t\begin{bmatrix}1\\-1\\1\end{bmatrix} + s\begin{bmatrix}2\\0\\-1\end{bmatrix} \\&=\begin{bmatrix}2s-t \\t \\-t-s\end{bmatrix}\end{align}$$
> > Since $C$ is $90\degree$, then $\vec{BC}\cdot \vec{AC} = 0$: $$\begin{align}\begin{bmatrix}2s-t \\t \\-t-s\end{bmatrix}\cdot\begin{bmatrix}2\\0\\-1\end{bmatrix} = -4s-2t +t+s = 0 \\  -t=-3s \implies t=3s\end{align}$$Working backwards then: $$\begin{bmatrix}2s-t \\t \\-t-s\end{bmatrix} = \begin{bmatrix}2s- 3s\\3s \\-3s-s\end{bmatrix}  = \begin{bmatrix}-1\\3\\-4\end{bmatrix}s$$
> > Therefore, the vector equation of our line is given by the following: $$\begin{bmatrix}x\\y\\z\end{bmatrix} = \begin{bmatrix}-1\\3\\-4\end{bmatrix}s + \begin{bmatrix}2\\-1\\1\end{bmatrix}$$

> [!theorem] Question 4: 
> > Find all unit vectors parallel to the $yz$ plane that are orthogonal to the vector $\begin{bmatrix}3\\-1\\2 \end{bmatrix}$. 
> 
> > [!caution]- Answer
> > If a vector is on the $yz$ plane; then they must be of some form $\begin{bmatrix}0\\a\\ b\end{bmatrix}$; We want to find what values of $a$ and $b$ with the dot product of the equation above gives us soemthing orthogonal to such a vector; that is their dot product is 0. $$\begin{bmatrix}0\\a\\b\end{bmatrix}\cdot \begin{bmatrix}3\\-1\\2\end{bmatrix} = -a + 2b = 0 \to 2b=a$$
> > From this, then we can see that $b=\frac{a}{2}$; therefore our vector is now currently $\begin{bmatrix}0\\a\\ \frac{a}{2}\end{bmatrix}$. If this is a unit vector; then it's magnitude must be some value 1, then: 
> > $$\begin{align}a^2 + \frac{a^2}{4} &= 1 \\a^2\left( \frac{5}{4} \right) &= 1  \\a &= \pm \frac{2}{\sqrt{ 5 }}\end{align}$$
> > Then our unit vector is some value $\begin{bmatrix}0\\ \frac{2}{\sqrt{5 }}\\ \frac{1}{\sqrt{ 5 }}\end{bmatrix}$

> [!theorem] Question 5: 
> The area of a tetrahedron is given by $\frac{1}{3}(\text{area of the base})(\text{height})$. Use this result to prove that the volume of a tetrahedron with sides defined by the vectors $\vec{a},\vec{b},\vec{c}$ is given by $\frac{1}{6}|\vec{a}\cdot(\vec{b}\times \vec{c})|$, taking the base to be defined by vectors $\vec{b},\vec{c}$. Note that $\vec{a}\cdot(\vec{b}\times \vec{c})$ is referred to as the scalar triple product. 
> 
> > [!caution]- Answer
> > The area of the base of a tetrahedron is some triangle; thus we know that $\text{area of the base}=\frac{1}{2}|\vec{b}\times \vec{c}|$. The vector *normal* to this is given to us by $\vec{b}\times \vec{c}$. To solve for the magnitude of the height, we perform a scalar projection on $\vec{b}\times \vec{c}$ using $\vec{a}$. This gives us the resulting height of $$h=\frac{\vec{a}\cdot(\vec{b}\times \vec{c})}{|\vec{b}\times \vec{c}|}$$
> > Note that we only care for *height as some positive value*, thus we take the absolute value. Taking our above equation, then$$\frac{1}{3}\left( \frac{|\vec{a}\cdot(\vec{b}\times \vec{c})|}{|\vec{b}\times \vec{c}|} \right)* \frac{1}{2}(|\vec{b}\times \vec{c}|) = \frac{1}{6}|\vec{a}\cdot (\vec{b}\times \vec{c})|$$

> [!theorem] Question 6
> Find the distance between the point $P(-3,1,3)$ and the plane $5x+z=3y-4$. 
> > [!caution]- Answer
> > First, rewrite the plane into it's proper scalar form. $5x-3y+z=-4$. From here we know the normal vector from this plane as some vector $\begin{bmatrix}5\\-3\\1\end{bmatrix}$. Let us find a *point* on this plane. A solution that comes to mind quickly is $A(-1,0,1)$, which satisfies the inequality. From here, the vector $AP$ is given by the matrix $\begin{bmatrix}-2\\1\\2\end{bmatrix}$. 
> > We want to solve for the plain distance between our plane, and our point. Our vector $AP$ points directly to $P$; and we know that $n_{1}$ is the shortest line (well, parallel direction vector) from the plane to the point. Thus, we take the scalar projection of $AP$ onto $n_{1}$, taking the absolute value as we only care about the distance.$$d=\frac{AP\cdot n_{1}}{|n_{1}|} = \frac{-10-3+2}{\sqrt{ 35 }} = -\frac{11}{\sqrt{ 35 }} \to \frac{11}{\sqrt{ 35 }}$$

> [!theorem] Question 7
> Show that the planes $3x-y+6z=7$ and $-6x+2y-12z=1$ are parallel, and find the distance between the planes.
> > Note, that for the Answer, we notate the first equation as $\pi_{1}$, and the second as some $\pi_{2}$. 
> 
> > [!caution]- Answer
> > To show that the planes are parallel, we only need to see if the normal vectors are scalar multiples of each other. If they are; then they are parallel, and thus the planes are parallel. 
> > For $\pi_{1}$; $n_{1}=\begin{bmatrix}3\\-1\\6\end{bmatrix}$. For $\pi_{2}$, $n_{2}=\begin{bmatrix}-6\\2\\-12\end{bmatrix}$. From here, it's trivial that $n_{2}=-2n_{1}$, and thus the planes are parallel. To find the distance between the planes we can use the similar kind of logic that we used to solve Question 6. 
> > A point on $\pi_{1}$ is the point $(1,2,1)$. A point on $\pi_{2}$ is the point $(0,0.5,0)$; The resulting vector from $\pi_{1}\pi_{2}$ is $\begin{bmatrix}-1\\-1.5\\-1\end{bmatrix}$. Taking the absolute value of the scalar projection will give the associated distance: $$d= \left| \frac{\pi_{1}\pi_{2}\cdot n_{1}}{|n_{1}|} \right| = \left| \frac{-3 +1.5 - 6 = -7.5}{\sqrt{ 46 }}\right| = \frac{7.5}{\sqrt{ 46 }}$$

> [!theorem] Question 8
> Find the vector equation for the line in $\mathbb{R}_{3}$ that contains the point $P(-1,6,0)$ and is orthogonal to the plane $4x-z=5$. 
> 
> > [!caution]- Answer
> > The corresponding normal vector to the plane is $n_{1}=\begin{bmatrix}4\\0\\-1\end{bmatrix}$, If our line is orthogonal to the plane, then our direction vector of our point is parallel to $n_{1}$; thus: $$\begin{bmatrix}x\\y\\z\end{bmatrix}= \begin{bmatrix}4\\0\\-1\end{bmatrix}t + \begin{bmatrix}-1\\6\\0\end{bmatrix}, t\in \mathbb{R}$$

> [!theorem] Question 9 
> Find the scalar equation for the plane that is *represented* by the following vector equation: 
> $$\begin{bmatrix}x\\y\\z\end{bmatrix} = \begin{bmatrix}-1\\5\\6\end{bmatrix} + t\begin{bmatrix}0\\-1\\3\end{bmatrix} + s\begin{bmatrix}2\\-1\\0\end{bmatrix}$$
> > [!caution]- Answer
> > Given our two direction vectors, simply solve for the corresponding normal vector by taking the Determinant of the $3\times3$ matrix below: $$\det\begin{bmatrix}\hat{i} & \hat{j} & \hat{k} \\0 & -1 & 3 \\2 & -1 & 0\end{bmatrix} = \begin{bmatrix}3\\6\\2\end{bmatrix}$$
> > Thus the corresponding scalar equation at the moment is $3x+6y+2z=d$, Plug in the point $(-1,5,6)$ to solve for $d$: $-3+30+12 =39=d$, therefore the equation is $3x+6y+2z=39$. 

> [!theorem] Question 10
> The equation $ax+by=0$ represents a line through the origin in $\mathbb{R}^2$ if $a,b\neq0$. What does this equation represent in $\mathbb{R}^3$ if you think of it as $ax+by+0z=0$ ? 
> > [!caution]- Answer
> > The new equation in $\mathbb{R}_{3}$ now represents a new plane, vertically defined from the line $ax+by$ in the $xy$ plane. Since $z$ can take on *any* value in this equation, and it still remains true; then any $z$ value above the line $ax+by$ is included in the corresponding space formed by this **plane**. 

> [!theorem] Question 11
> Consider the following planes in $\mathbb{R}^3$: $$\begin{align}1x+0y+0z = 2 \\0x + 1y + 0z = 3 \\0x + 0y + 1z = 4\end{align}$$
> 1.  Construct a mental image of the row picture. 
> 2. Express the 3 equations as a single vector equation.
> 3. Construct a mental image of the column picture.
> 4. What does the solution to these 3 equations represent in $\mathbb{R}^3$? 
> > [!caution]- Answer(s) 
> > 1. The row picture gives us three planes, one in $yz$, one in $xz$, and one in $xy$. 
> > 2. The vector equation from the normal vectors gives us the following: $$\begin{bmatrix}1\\0\\0\end{bmatrix}x+\begin{bmatrix}0\\1\\0\end{bmatrix}y +\begin{bmatrix}0\\0\\1\end{bmatrix}z = \begin{bmatrix}2\\3\\4\end{bmatrix}$$
> > 3. The column picture gives us a linear combination of the resultant vector. 
> > 4. The solutions give us the intersection point of all 3 planes; or the scalar multiples of the linear combination above to get to the resultant vector desired. 
> 
> 


> [!theorem] Question 12 
> Consider the following planes in $\mathbb{R}^3$: $$\begin{align}x + y + z &= 2 \\x + 2y + z &= 3 \\ 2x +3y + 2z &= 5 \end{align}$$
> 1. Express these 3 equations as a single vector equation.
> 2. Find two linear combinations of the column vectors on the left hand side that equal the right hand side vector. 
> 3. Show that it is only possible to find linear combinations of the column vectors on the left-hand side when the right-hand side vector is equal to $\begin{bmatrix}4\\6\\ c\end{bmatrix}$ and $c$ is equal to what value? 
> 4. Express these 3 equations in the form of $A\vec{v}=\vec{b}$. 
>
> > [!caution]- Answer
> > 1. As an equation: $$\begin{bmatrix}1\\1\\2\end{bmatrix}x + \begin{bmatrix}1\\2\\3\end{bmatrix}y + \begin{bmatrix}1\\1\\2\end{bmatrix}z = \begin{bmatrix}2\\3\\5\end{bmatrix}$$
> > 2. $(0,1,1)$ and $(1,1,0)$
> > 3. $$\begin{align}\left[\begin{array}{ccc|c}1 & 1 & 1 & 4 \\1 & 2 & 1 & 6 \\2 & 3 & 2 & c\end{array}\right] \to \left[\begin{array}{ccc|c}1 & 1 & 1 & 4 \\1 & 2 & 1 & 6 \\2 & 3 & 2 & c\end{array}\right]  &\to \left[\begin{array}{ccc|c}1 & 1 & 1 & 4 \\1 & 2 & 1 & 6 \\0 & 1 & 0 & c-8\end{array}\right]  \to \left[\begin{array}{ccc|c}0 & -1 & 0 & -2 \\1 & 2 & 1 & 6 \\0 & 1 & 0 & c-8\end{array}\right]  \\y&=2 \implies 2 = c-8 \to c=10\end{align}$$
> >    Thus, the only possible linear combinations for this arrangement is when $c=10$; or conversely with $\begin{bmatrix}2\\3\\5\end{bmatrix}*2$; since both are parallel. 
> > 4. $$\begin{bmatrix}1 & 1 & 1 \\1 & 2 & 1 \\2 & 3 & 2\end{bmatrix}\begin{bmatrix}x\\y\\z\end{bmatrix} =\begin{bmatrix}2\\3\\5\end{bmatrix}$$
