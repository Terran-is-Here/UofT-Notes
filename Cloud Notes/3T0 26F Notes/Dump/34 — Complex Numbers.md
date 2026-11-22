---
updated_at: 2026-11-22T18:01:06.329-05:00
edited_seconds: 310
course: ESC194H1
tags:
  - ESC194H1
"Lecture #": 34
Lecture Date: 2026-11-22
Week:
---
Hub: [[ESC194 Hub]]
Previous: [[33 — Linear Equations]]
Next:
> [!quote] Recommended Reading 
> Stewart Section 5, (???), [[25 — Inverse Functions]]
--- 
# Lecture Notes

---
# Pre-Lecture Notes
> [!caution] Note
> This section was (primarily) written out of my own memory pertaining to the world of Complex Numbers, thus lending to quite a surface level field of the field of $\mathbb{C}$. 

## Imaginary Numbers
Consider the following expression: 
$$
2x^{2} - 2x + 1 = 0
$$
The solutions for this can be given by the quadratic formula: 
$$
\frac{4 \pm \sqrt{ 4 - 4*2*1 }}{4} = \frac{4\pm \sqrt{ -4 }}{4}
$$
The question then arises, $\sqrt{ -4 }$, what does this equal to? Recall from inverse functions that: 
$$
\begin{align}
f(x)  & = x^{2} & \mathbb{R}\mapsto[0,\infty) \\
f^{-1}(x)  & =\sqrt{ x } & [0,\infty) \mapsto \mathbb{R}
\end{align}
$$
Our square root function inherently by itself does not have the idea of a negative number within it's inherent domain. In fact, it's not even part of it's domain at all $\forall \mathbb{R}$. We can see this intuitively, as the square root asks us "what number to square which gives us the thing we're square rooting", and all squares in $\mathbb{R}$ inherently result in positive numbers.

We have to expand our domain past the real number system by introducing the concept of the imaginary number: 

> [!theorem] Imaginary Number
> We define the symbol $i$ as having the following properties: 
> $$i^{2}=-1$$
> Thus:
> $$\sqrt{ -1 }=i$$
> We define the range of numbers which are some multiple of $i$ as being within the set of Imaginary Numbers:
> $$c = ni \implies c\in \mathbb{I}$$

We also now expand this, to define the set of Complex Numbers: 
> [!theorem] Complex Number
> We define a complex number as the following: 
> $$a+bi$$
> Where $a$ is some real number, and $b$ is some multiple of an imaginary number. In other words, $a\in \mathbb{R}$, $b\in \mathbb{I}$. This number is part of the set of Complex Numbers, composed of numbers of this same form, and are notated as being members of the set $\mathbb{C}$. 
> > We can also alternatively notate this as an ordered pair: 
> > $$(a,b)$$
> > Where $a$ corresponds to our real coefficient, and $b$ corresponds to our imaginary component. 
> 
> We also note that $\mathbb{R} \subset \mathbb{C}$, as well as $\mathbb{I}\in \mathbb{C}$. In other words, the real and imaginary numbers are subsets of the set of complex numbers. 

Considering now our earlier expressions: 
$$
\begin{align}
f(x)  & = x^{2} & \mathbb{R}\mapsto[0,\infty) \\
f^{-1}(x)  & =\sqrt{ x } & [0,\infty) \mapsto \mathbb{R}
\end{align}
$$
If we let $x\in \mathbb{C}$, we note that this function would map to *all* of $\mathbb{R}$ (well i mean, it would map to $\mathbb{C}$ too, but would be restricted to real-numbered coefficients): 
$$
\begin{align}
f(x)  & = x^{2} & \mathbb{C}\mapsto \mathbb{C} \\
f^{-1}(x)  & =\sqrt{ x } & \mathbb{C} \mapsto \mathbb{C}
\end{align}
$$
In this case, using our above definitions, then our solutions to $2x^{2}-2x+1=0$ are: 
$$
x=\frac{4\pm2i}{4} = 1 \pm 0.5i, x\in \mathbb{C}
$$
## The Complex Plane