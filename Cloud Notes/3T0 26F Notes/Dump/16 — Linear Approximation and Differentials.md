---
updated_at: 2026-10-16T13:50:06.343-04:00
edited_seconds: 310
course: ESC194H1
tags:
  - ESC194H1
"Lecture #": 16
Lecture Date: 2026-10-16
Week: 6
---
Hub: [[ESC194 Hub]]
Previous: [[15 — Summary of Curve Sketching]]
Next: [[17— Optimization, Antiderivatives and Sigma Notation]]
> [!caution] Note
> This note was written primarily in lecture. 

> [!quote] Recommended Reading 
> Section 2.9 of the Stewart Textbook.
--- 
# Lecture Notes

## Linear Approximations
Given a function $f(x)$, we may want to ask the question; what is the value of $f(x+h)$? Consider the tangent line to the function $f(x)$. We know this tangent line would have the slope of $f'(x)$. 

Note that we can denote the difference or increment between our functions as $f(x+h)-f(x)$

We define the concept of the differential as the rate of change / slope of our function. For our case, we can denote $\Delta y = f'(x)h$. This is the *approximation* of the real difference between $f(x+h)-f(x)$. 

We can extend this to the full concept of a linear approximation. 

> Linear Approximation
> Take the function $f(x)$; If we take the tangent line at a point $a$, we can see that $f'(a)=m_{a}$, where $m_{a}$ is the slope at $a$, as per the definition of the limit. The tangent line can then be defined as: 
> $$y(x) = f(a) + f'(a)(x-a)$$
> This tangent line can be used as an approximation for $f(x)$ near $a$, that is $f(a)+f'(a)(x-a) \approx f(x)$ for values of $x$ near $a$, or $a + \delta$. This term is what we define as the linear approximation. 
> $$f(x) \approx f'(a)(x-a) + f(a) \text{ for }x \text{ near } a$$

The question then arises, *how good* *is* this approximation? How close is our $f'(a)(x-a)+f(a)$ for some value? 

Take the following example: 
Use Linear Approximation to estimate $(1.1)^3$ and $(1.001)^3$; then approximate $(1.1)^{77}$ and $(1.001)^{77}$. We have two approximations for these functions. 

> For the first, $f(x) = x^3, f'(x)=3x^2$, then following our linear approximation, using $a=1$, then: 
$$
\begin{align}
f(x)  & \approx f'(a)(x-a)+f(a) \\
1.1^3 & \approx 3(1.1-1)+1 \\
1.1^3 & \approx 1.3 \\
1.331 & \approx 1.3
\end{align}$$
$$
\begin{align}
1.001^3  & \approx 3(1.001-1) + 1 \\
1.003003  & \approx 0.003 + 1 = 1.003
\end{align}
$$

> For the second, $f(x)=x^{77}, f'(x) = 77x^{76}$, then $a=1$
$$
\begin{align}
f(x)  & \approx f'(a)(x-a) + f(a)  \\
 & \approx 76(x-1) + 1
\end{align}
$$
Then: 
$$
\begin{align}
f(1.1)  & \approx(76)(0.1)+1 \\
1538.993 & \approx
\end{align}
$$