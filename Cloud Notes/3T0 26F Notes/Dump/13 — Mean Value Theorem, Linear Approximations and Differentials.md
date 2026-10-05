---
updated_at: 2026-10-04T22:05:08.169-04:00
edited_seconds: 1280
course:
tags:
"Lecture #": 0
Lecture Date: 2026-10-04
Week:
---
Hub: 
Previous: 
Next:

--- 
# Lecture Notes

---
# Pre-Lecture Notes
## Mean Value Theorem
The mean value theorem is the following statement: 
> Mean Value Theorem
> Given: If $f$ is a real-valued function, defined and continuous on, and having a derivative on the open interval $(a,b)$, then there exists some point $c\in(a,b)$ such that: 
> $$\boxed{f'(c)=\frac{f(b)-f(a)}{b-a}}\tag{MVT}$$

The proof for this requires quite a bit of thinking, and required a few other theorems to build up to it. 

> [!theorem] Lemma 1
> > *Given:* 
> > $f$ is a function which is defined, continuous, and differentiable on an open interval $(u,v)$
> > $f$ assumes it's maximum value at some point $w$ within the interval. 
> 
> > *Prove*: $f'(w)=0$
> 
> *Proof:* Consider the definition of $f'(w)$ from the limit: 
> $$f'(w) = \lim_{ h \to 0 } \frac{f(w+h)-f(w)}{h}$$
> Since $f(w)$ assumes some maximum value; then $f(w+p) <f(w) \implies f(w+p)-f(w)<0$; which means that for any value $h$ on our numerator, then it must be some negative value; then from our one sided limits: $$\begin{align}f'_{+}(w) = \lim_{ h \to ^+0 } \frac{f(w+h)-f(w)}{h} \implies \frac{f(w+h)-f(w)}{h} < 0 \\f'_{-}(w) = \lim_{ h \to ^-0 } \frac{f(w+h)-f(w)}{h} \implies \frac{f(w+h)-f(w)}{h} > 0\end{align}$$
> For $f'(w)$ to exist, $f'_{+}(w) = f'_{-}(w)$ must be equal. The only way this can be true is if and only if $f'(w) = 0$. 
> 
> > [!theorem] Lemma 1.2 
> > This theorem also extends to some minimum value $m$ within some interval; where $f(m+p)> f(m) \implies f(m+p)-f(m) > 0$. From the above inequalities, then $f'(m)=0$. 

> [!theorem] Rolle's Theorem
> > *Given*: 
> > $f$ is continuous on a closed interval $[a,b]$
> > $f$ has a derivative on each point of $(a,b)$
> > $f(a)=f(b)$
> 
> Prove: There exists a point $c\in(a,b)$ where $f'(c) = 0$
> 
> Proof: 
> If $f(x)$ is continuous on some interval $[a,b]$, then it must possess some maximum value $M$ and minimum value $m$ in $[a,b] \to[f(a),f(b)]$. Since $f(a)=f(b)$, these values are not defined on $[a,b]$ and are thus defined in the open interval of $(a,b)$. 
> 
> Following from Lemma 1.1 and Lemma 1.2, then there exists some point $c\in(a,b) \implies f'(c)=0$. 

Using Rolle's Theorem, we can now build a proof for the MVT. [[#^768c51]]
> [!theorem] Mean Value Theorem
> Given: If $f$ is a real-valued function, defined and continuous on, and having a derivative on the open interval $(a,b)$, then there exists some point $c\in(a,b)$ such that: 
> $$\boxed{f'(c)=\frac{f(b)-f(a)}{b-a}}\tag{MVT}$$
*Proof*:
Take the secant line between some point $(a,f(a)), (b,f(b))$: 
$$\begin{align}m&=\frac{f(b)-f(a)}{b-a} & \text{ Take some point } (a,f(a)) \\f(a)&=\left(\frac{f(b)-f(a)}{b-a}\right)a + b \\b&= f(a)-\left(\frac{f(b)-f(a)}{b-a}\right)a \\y&=\left(\frac{f(b)-f(a)}{b-a}\right)(x-a) + f(a)\end{align}$$
Now, we define some function $g(x)$ which represents the distance between a point $y=f(x)$ and the secant line; then: $$g(x) = f(x) - f(a) - \left(\frac{f(b)-f(a)}{b-a}\right)(x-a)$$
Note that $g(x)$ at $g(a)=g(b)=0$, and that it is defined and continuous on $[a,b]$, and differentiable on $(a,b)$. From Rolle's Theorem, there therefore exists some $g'(c)=0$ where $c\in(a,b)$. 
If we rearrange this for some $f(x)$, then: 
$$f(x) = g(x) + f(a) + \left(\frac{f(b)-f(a)}{b-a}\right)(x-a)$$
Differentiating $f(x)$ with respects to $x$ gives us the following: $$f'(x) = g'(x) +\left(\frac{f(b)-f(a)}{b-a}\right)$$
Note from Rolle's Theorem, some value $c$ exists where $g'(c)=0$, which means for some value $c\in(a,b)$: 
$$\boxed{f'(c) = \frac{f(b)-f(a)}{b-a}}$$

^768c51
Note that MVT extends a very interesting corollary: 

> > *Given:* 
> > $f$ is a function defined & continuous on the closed interval $[a,b]$, 
> > $\exists f'(x)$, and $f'(x)=0$ for $x\in(a,b)$
> 
> Prove: $f$ is constant on the interval $[a,b]$. 
> 
> Proof: 
> If $f$ is continuous, defined on some closed interval $[a,b]$, then it is also continuous on some subinterval $[a,x]\subset[a,c]$, where $x\in(a,b]$. 
> If $f$ is differentiable on some open interval $(a,b)$, then it is also differentiable on some subinterval $(a,x)\subset(a,c)$ where $x\in(a,b]$.
> 
> Following from MVT, then there exists a point $g$ for $f'$ such that
> $$f'(g) = \frac{f(x)-f(a)}{x-a}$$
> Note from our givens, we know that $f'(w)=0$ if $w\in(a,b)$, but since $w\in(a,x)\subset(a,b)$ then the given concept of $f'(w)=0$ is still applicable: $$f'(g) = \frac{f(x)-f(a)}{x-a}=0 \implies f(x) = f(a)$$
> Note that our definition for $x$ was an arbitrary value between $a$ and $b$ (inclusive). If $x=a$, $f(a)=f(a)$, and if $x=b$, $f(b)=f(a)$ which means that across the interval of $[a,b]$, $f(x)=f(a)$, which implies that $f$ is some constant value. 
## Cauchy's Mean Value Theorem 
Cauchy's Mean Value Theorem is an 