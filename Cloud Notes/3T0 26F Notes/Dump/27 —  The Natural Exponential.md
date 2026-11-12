---
updated_at: 2026-11-12T10:04:14.737-05:00
edited_seconds: 200
course: ESC194H1
tags:
  - ESC194H1
"Lecture #": 17
Lecture Date: 2026-11-16
Week:
---
Hub: [[ESC194 Hub]]
Previous:  [[26 — The Natural Logarithmic Function]]
Next: N/A
> [!quote] Recommended Reading 
> Section 6.3\* of the Stewart Textbook (not 6.3, 6.3\*). 
> [[25 — Inverse Functions]]

--- 
# Lecture Notes

---
# Pre-Lecture Notes
## The Natural Exponential
Consider the natural logarithm, which we have defined earlier as the integral of $\frac{1}{x}$ with respects to $1$ and $x$: 
$$
\ln(x) = \int_{1}^{x} \frac{1}{t}\,dt
$$
Recall that we noted that the first and second derivatives of this function imply that this function is constantly increasing within it's domain: 
$$
\begin{align}
\frac{d}{dx}\ln(x)  & = \frac{1}{x} & \forall x\in[0,\infty), \frac{d}{dx} >0  \\
\frac{d^{2}}{dx^{2}}\ln (x)  & =-\frac{1}{x^{2}} & \forall x\in[0,\infty), \frac{d^{2}}{dx^{2}} < 0 
\end{align}
$$
As such, we note that this function is therefore fully bijective within it's domain (one-to-one). Therefore, there must exist some corresponding inverse function; which we will denote as $\exp(x)$: 

$$
\ln (y) = x \iff \exp(x) = y
$$
Noting some of the earlier properties that we had with our natural logarithm and extending it to our inverse: 
$$
\begin{align}
\ln(1) = 0 \iff \exp(0) = 1  \\
\ln(e) = 1 \iff \exp(1) = e
\end{align}
$$
And the corresponding cancellation equations are given to us by the usual: 
$$
\exp(\ln(x)) = x\\
\ln(\exp(x)) = x
$$
Note that the above applies for all values within the range of $\ln(x)$, whereas the one below applies for all values within the range of $\exp(x)$. Note that $\ln(x)$ is not inherently defined for negative numbers. From these properties above, we can actually build an expression for the natural exponent. 
