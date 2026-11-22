---
updated_at: 2026-11-22T13:02:47.661-05:00
edited_seconds: 210
course:
tags:
"Lecture #": 0
Lecture Date: 2026-11-22
Week:
---
Hub: 
Previous: 
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
> Complex Number
> We define a complex