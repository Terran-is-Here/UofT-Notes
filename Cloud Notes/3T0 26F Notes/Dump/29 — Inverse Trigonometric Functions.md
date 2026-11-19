---
updated_at: 2026-11-19T11:51:08.845-05:00
edited_seconds: 500
course: ESC194H1
tags:
  - ESC194H1
"Lecture #": 29
Lecture Date: 2026-11-15
Week:
---
Hub: [[ESC194 Hub]]
Previous: [[28 — General Logarithmic and Exponential Functions]]
Next: N/A
> [!quote] Recommended Reading 
> Section 6.6 of the Stewart Textbook. 
--- 
# Lecture Notes

---
# Pre-Lecture Notes
## Inverse Trigonometric Functions
Recall how we defined that for a function to have an inverse, it must be bijective. If we consider our trigonometric functions, these functions are never bijective due to their periodicity. As such, we find that to make them bijective, we must restrict our domain. 

Consider now the function $\sin(x)$. This function's period is from $[0,2\pi]$, Noting that $f(-x) = -f(x)$ (odd symmetry), we find that to make this function bijective, we restrict it's domain from $\left[ -\frac{\pi}{2}, \frac{\pi}{2} \right]$:
![[29 — Inverse Trigonometric Functions-1795105738113.webp]]

Noting that this function is now bijective, and that $\cos(x) > 0 x\in\left[ -\frac{\pi}{2}, \frac{\pi}{2} \right]$, thus we can define the inverse under our familiar set of relations: 
$$
\begin{align}
\sin ^{-1}(x)  & = y \\
x & =\sin(y)
\end{align}
$$
Finding the derivative of our inverse, we thus find that: 
$$
\begin{align}
\sin(y)  & = x \\ 
\frac{d}{dx}\sin(y)  & =\frac{d}{dx}x \\
\cos(y) \frac{dy}{dx}  & =1 \\
\frac{dy}{dx} & =\frac{1}{\cos(y)}  & \cos ^{2}(y) = 1-\sin ^{2}(y) \\
\frac{dy}{dx} & = \frac{1}{\sqrt{ 1-\sin ^{2}(y) }} =\frac{1}{\sqrt{ 1-x^{2} }} \\
[\sin ^{-1}(x)]'  & =\frac{1}{\sqrt{ 1-x^{2} }}
\end{align}
$$
Similarly, we can find the corresponding derivative of the inverse for $\cos ^{-1}(x)$. Note that $\cos ^{-1}(x) \iff x\in(0,\pi)$ in terms of it's domain to maintain bijectivity. 
$$
\begin{align}
\cos ^{-1}(x) = y  & \iff x=\cos (y)  \\[2em]
\cos(y)  & =x  \\
\frac{d}{dx}\cos(y)  & = \frac{d}{dx} x  \\
-\sin(y) \frac{dy}{dx}  & =1 \\
\frac{dy}{dx}  & =\frac{1}{-\sin(y)} & \sin(y) = \sqrt{ 1-\cos ^{2}(y) } = \sqrt{ 1-x^{2} } \\
\frac{dy}{dx} & = -\frac{1}{\sqrt{ 1-x^{2} }}

\end{align}
$$
Consider now finding the expression for the derivative of the inverse of $\tan ^{-1}(x)$. Using a similar tactic we set up the following: 
$$
\begin{align}
\tan ^{-1}(x) =y & \iff x=\tan(y) \\[2em]
\tan(y) & =x \\
\frac{d}{dx}\tan(y)  & = \frac{d}{dx} x \\
\sec ^{2}(y) \frac{dy}{dx} & = 1  \\
\frac{dy}{dx}  & =\cos ^{2}(y)
\end{align}
$$
Now we have a problem here: How do we now attempt to redefine $y$ in terms of $x$? Or in other words, can we get $\cos ^{2}(y) \to \tan(y)$? For this case, we have to consider the geometry. 

Recall that $\tan(x) = \frac{o}{a}$, thus we find that if $x=\tan(y)$, then $\frac{x}{1} = \tan (y)$, or in other words, the far side is a term of $x$, the close side is a term fo $1$, and the angle containing them is defined by some $y$: 
![[29 — Inverse Trigonometric Functions-1795106408025.webp]]

Thus: 
$$
\cos(y) = \frac{1}{\sqrt{ 1+x^{2} }}
$$
Resubstituting this into our earlier expression, then: 
$$
\begin{align}
\frac{dy}{dx}  & = \left( \frac{1}{\sqrt{ 1+x^{2} }} \right)^{2} = \frac{1}{1+x^{2}} = [\tan ^{-1}(x)]'
\end{align}
$$
### Reciprocal Inverse Trig Functions
We can also use the similar set of logic to find the derivatives of our inverse trig functions. 

For instance, take $\csc(x) = \frac{1}{\sin(x)}$, then: 
$$
\begin{align}
\csc ^{-1}(x) = y  & \iff x = \csc(y) = \frac{1}{\sin(y)} \\[1.5em]
\csc(y) & = x \\
\frac{d}{dx}\csc(y)  & =\frac{d}{dx}x \\
-\cot(y)\csc(y) \frac{dy}{dx} & = 1  \\
\frac{dy}{dx} & = -\frac{1}{\cot(y)\csc(y)}= -\frac{1}{\frac{\cos(y)}{\sin(y)} \frac{1}{\sin(y)}} = \frac{-\sin ^{2}(y)}{\cos(y)} \\
 & =-\frac{1}{x^{2}\cos(y)} & \cos(y) & = \sqrt{ 1-\sin ^{2}(y) } = \sqrt{ 1-\frac{1}{x^{2}} } \\
 & =-\frac{1}{x^{2}\sqrt{ 1-\frac{1}{x^{2}} }} = -\frac{1}{x^{2}\sqrt{ \frac{x^{2}-1}{x^{2}} }}
\end{align}
$$