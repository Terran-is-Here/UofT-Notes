---
updated_at: 2026-11-20T12:12:39.625-05:00
edited_seconds: 700
course:
tags:
"Lecture #": 0
Lecture Date: 2026-11-20
Week:
---
Hub: 
Previous: 
Next:
> [!quote] Recommended Reading 
> Section 6.8 of the Stewart Textbook
> [[13 — Mean Value Theorem, Linear Approximations and Differentials#Cauchy's Mean Value Theorem]] (as we use it for the proof of l\`Hospital's rule). 

--- 
# Lecture Notes

---
# Pre-Lecture Notes
## Indeterminate Forms
Consider the case in which we have a function such as the following: 
$$
f(x)=\frac{\ln(x)}{x-1}
$$
Where we want to find the following: 
$$
\lim_{ x \to 1 } f(x) = \lim_{ x \to 1 }  \frac{\ln(x)}{x-1} \to \frac{0}{0}
$$
We have an issue: If we wanted to find the value of such a function, where taking the limit results in something that we term as an *indeterminate* form. We now define the following as indeterminate forms *which we can analyze*. 
* $\frac{0}{0}$
* $\frac{\infty}{\infty}$
In terms of the means we analyze this, we now introduce the concept of l\`Hospital's Rule: 
## l\`Hospital's Rule 
l\`Hospital's Rule (noted from here as LHoR) is defined as the following: 

> [!theorem] LHoR
> Let $f,g$ be differentiable and $g'(x) \neq 0$ on an open interval $I$ that contains $a$ (except possibly at $a$), Suppose that: 
> $$\lim_{ x \to a } f(x) = 0, \lim_{ x \to a } g(x) = 0\text{ or }\\ \lim_{ x \to a } f(x) = \infty, \lim_{ x \to a } g(x) = \infty$$
> Or in other words, we have the following expression that evaluates into an indeterminate form as the ones that we have had above. 
> $$\lim_{ x \to a } \frac{f(x)}{g(x)} \to\frac{0}{0} \lor \lim_{ x \to a } \frac{f(x)}{g(x)} \to \frac{\infty}{\infty}$$
> Then we define that:
> $$\lim_{ x \to a } \frac{f(x)}{g(x)} = \lim_{ x \to a } \frac{f'(x)}{g'(x)}$$
> If the limit on the right side exists. 

In other words, it states that given a ratio of functions which, when the limit is taken, that they fall into an indeterminate form of $\frac{\infty}{\infty}$ or $\frac{0}{0}$, the limit of that ratio of functions is equal to the limit of the ratio of the derivatives of those functions. 
### Proof 
We can prove this by reconsidering the Mean Value Theorem from earlier. For the purpose of completeness, we will prove the necessary theorems that we need to prove that this rule holds true. **Note that this only proves $\frac{0}{0}$** (as the proof of $\frac{\infty}{\infty}$ is outside the scope of this course). 

Recall that the mean value theorem is defined as the following (see [[13 — Mean Value Theorem, Linear Approximations and Differentials#Mean Value Theorem|ESC194 (13)]]): 
> Mean Value Theorem
> Given: If $f$ is a real-valued function, defined and continuous on, and having a derivative on the open interval $(a,b)$, then there exists some point $c\in(a,b)$ such that: 
> $$\boxed{f'(c)=\frac{f(b)-f(a)}{b-a}}\tag{MVT}$$

Let us define this in terms of $h(x)$, where we let $h(x)$ be the following expression: 
$$
h(x) = f(x) - f(a) - \frac{f(b)-f(a)}{g(b)-g(a)}(g(x)-g(a))
$$
Evaluating this as $h(b),h(a)$ and taking the derivative: 
$$
\begin{align}
h(b)  & = f(b)-f(a) - \frac{f(b)-f(a)}{g(b)-g(a)}(g(b)-g(a)) \\
 & =f(b) - f(a) - f(b) +f(a) \\
 & = 0 \\
h(a)  & = f(a)-f(a) - \frac{f(b)-f(a)}{g(b)-g(a)}(g(a)-g(a)) \\
 & =0 \\
h'(x)  & = f'(x) - \frac{f(b)-f(a)}{g(b)-g(a)}g'(x)
\end{align}
$$
Note that we find, $h(b)=0,h(a)=0$, we know that there exists some value $h'(c), c\in[a,b]$ where $h'(c) = 0$, thus: 

$$
\begin{align}
h'(c) & =0 = f'(c) - \frac{f(b)-f(a)}{g(b)-g(a)}g'(c) \\
-f'(c) & = - \frac{f(b)-f(a)}{g(b)-g(a)}g'(c) \\
\frac{f'(c)}{g'(c)} & = \frac{f(b)-f(a)}{g(b)-g(a)}
\end{align}
$$
This is the Cauchy Mean Value Theorem, that is, $\exists c\in[a,b]$ such that this is true. From this, we can now actually prove LHoR. 

Consider the case when we have an indeterminate form of $\frac{0}{0}$, that is given two functions, we have the following: 
$$
\begin{align}
F(x) &  = \begin{cases}
f(x) & : x\neq a \\
0 & : x=a
\end{cases} \\
G(x) & =\begin{cases}
g(x) & :x\neq a \\
0 & : x=a
\end{cases}
\end{align}
$$
Note that $F$ is continuous in $A$, where $A=\{ x\in I |x\neq a\}$. The same applies for $G(x)$. Consider now that $x\in I$ and $x>a$, then $F,G$ are continuous on $x\in [a,x]$. From this, we note that $F,A$ is differentiable on $(a,x)$, thus following Cauchy's MVT, we find the following: 
$$
\begin{align}
\exists c  & \in (a,x) \text{ s.t.} \\
\frac{F'(c)}{G'(c)} & = \frac{F(x)-F(a)}{G(x)-G(a)} = \frac{F(x)}{G(x)} \\[2em]
 & \text{note, } x\to a^{+} \implies c \to a^{+} \\
\lim_{ c \to a^{+} }  \frac{F'(c)}{G'(c)} & = \lim_{ x \to a^{+} }  \frac{F(x)}{G(x)}  \implies \lim_{ c \to a^{+} }  \frac{f'(c)}{g'(c)} = \lim_{ x \to a^{+} }  \frac{f(x)}{g(x)} =L
\end{align}
$$
Similarly, defining $x<a$ where $F,A$ are now continuous on $[x,a]$, and therefore differentiable in $(x,a)$, then we find that the right hand limits also hold: 
$$
\begin{align}
   & \exists c\in(x,a) \text{ s.t } \\
\frac{F'(c)}{G'(c)} & = \frac{F(a)-F(x)}{G(a)-G(x)} = \frac{F(x)}{G(x)} \\[1.5em]
x\to a^{-}  & \implies c \to a^{-} \\
\implies \lim_{ c \to a^{-} } \frac{F'(c)}{G'(c)} = \lim_{ x \to a^{-} } \frac{F(x)}{G(x)} &  \implies \lim_{ c \to a^{-} } \frac{f'(c)}{g'(c)} = \lim_{ x \to a^{-} } \frac{f(x)}{g(x)}
\end{align}
$$
Noting that the right and left hand limits are equal, we thus find that: 
$$
\lim_{ x \to a } \frac{f(x)}{g(x)} = \lim_{ x \to a } \frac{f'(x)}{g'(x)} = \text{L}
$$
#### Extension
Consider now we can extend this if $x \to \infty$, we can express this as $x \to \frac{1}{t}$, where $t\to 0$, where this is finite value, thus: 
$$
\lim_{ x \to \infty } \frac{f(x)}{g(x)} = \lim_{ x \to \infty } \frac{f'(x)}{g(x)} \iff\lim_{ t \to 0 }  \frac{f\left( \frac{1}{t} \right)}{g\left( \frac{1}{t} \right)} = \lim_{ t \to 0 } \frac{f'\left( \frac{1}{t} \right)}{g'\left( \frac{1}{t} \right)} = L
$$
