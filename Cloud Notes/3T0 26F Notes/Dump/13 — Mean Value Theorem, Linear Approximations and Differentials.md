---
updated_at: 2026-10-10T14:15:47.267-04:00
edited_seconds: 2060
course: ESC194H1
tags:
  - ESC194H1
"Lecture #": 13
Lecture Date: 2026-10-04
Week: 5
Created: October 4th 2026, 6:51:22 pm
---

Hub: [[ESC194 Hub]]
Previous: [[12 — Related Rates, Min and Max Values]]
Next: [[14 — Derivatives, Function Shape, Horizontal Asymptotes]]
> [!quote] Recommended Reading 
> Section 3.2, 2.9 of the textbook. 
--- 
# Lecture Notes
## Mean Value Theorem (LEC) 
The mean value theorem is the following: 
> If $f$ is differentiable on the open interval $(a,b)$ **AND** continuous on the *closed* interval $[a,b]$, then there is *at least* one number $c\in(a,b)$, where: 
> $$f'(c) = \frac{f(b)-f(a)}{b-a}$$

To prove this, we need Rolle's Theorem: 
> [!ila] Rolle's Theorem
> Let $f$ be differentiable on the open interval $(a,b)$ and continuous on the closed interval $[a,b]$. Then, if $f(a)=f(b)=0$, then there exists at least one number $c\in(a,b)$ where $f'(c)=0$
> > Proof: Consider the following cases. 
> > 1. $f(x)=f(a)=f(b)=0 \implies f(x)$ is a constant function, $f'(x)=0 \forall x\in(a,b)$. 
> > 2. $f(x) >0$ for some values $x\in (a,b)$
> > 3. $f(x) <0$ for some values $x\in(a,b)$. 
>
>
> > We can perform a proof using Case 2. 
> >  $f(x) > 0$ for $x\in(a,b)$.
> >  Since $f(x)$ is continuous on $[a,b]$, then it has to take some maximum value $f(c)=M,c\in[a,b]$ from [[12 — Related Rates, Min and Max Values#Extreme Value Theorem (LEC)|EVT]]. Note for case 2, $f(x)>0 \implies f(c)>0$; since $f(a)=f(b) =0$, then $c\in(a,b)$. 
> >  Since $f'(x)$ is differentiable on $(a,b)$, $f'(c)$ exists. From Fermat's Theorem, $f'(c)=0$. Therefore there exists some location $x=c$ on the open interval $x=c\in(a,b) \implies f(c)=0$

Now we can move MVT: 

> Take the following equation: $$g(x) = f(x) - \left[ \frac{f(b)-f(a)}{b-a}(x-a) +f(a) \right]$$
> Note that the term in the brackets is equivalent to some line from $(a,f(a)) \to (b,f(b))$. Then this represents to us the distance between some $f(x)$ and the line between it's endpoints. 
> 
> Note that $g(a)=g(b)=0$, and $g(x)$ is continuous and differentiable on $f(x)$ being continuous and differentiable; then $g(x)$ continuous on $[a,b]$ and differentiable on $(a,b)$. Then $g(x)$ satisfies the criteria for Rolle's Theorem. Then there is at least one $g(c),c\in(a,b), g'(c)=0$. $$g'(x) = f'(x) - \left( \frac{f(b)-f(a)}{b-a} \right)$$We know from Rolle that $\exists c, g'(c) = 0$, therefore: $$\begin{align}g'(c) = f'(c) - \left( \frac{f(b)-f(a)}{b-a} \right) = 0 \\\boxed{f'(c) = \frac{f(b)-f(a)}{b-a}}\end{align}$$

## Application
Take the following example:
> Two runners start a race at the same time, and finish in a tie. Show that at some time during the race, they have the same velocity. 

> Let $h(t)$ be the position of Runner 1, Let $g(t)$ be the position of Runner 2. Then we can define that: 

$$f(t) = h(t)-g(t)$$
Note from this, that we want to show some time $t_{0}$ where $g'(t_{0}) = h'(t_{0}) \implies f'(t)=0$ from above if differentiated. 
Note that, at the beginning of the race, $h(0)=g(0)=0$, and $f(0)=0$. At the end of the race, $h(T) = g(T)\implies f(T)=0$. Since $f(0)=f(T)=0$, we can apply Rolle's Theorem (letting $h,t$ are continuous.). From RT, $\exists t_{0}\in(0,T) \implies f'(t_{0})=0$. Note that: 
$$
\begin{align}
f'(t) = h'(t) - g'(t) \\
f'(t_{0}) = h'(t_{0}) - g'(t_{0}) = 0 \\
\implies h'(t_{0}) = g'(t_{0})
\end{align}$$



---
# Pre-Lecture Notes
## Mean Value Theorem
The mean value theorem is the following statement: 
> Mean Value Theorem
> Given: If $f$ is a real-valued function, defined and continuous on, and having a derivative on the open interval $(a,b)$, then there exists some point $c\in(a,b)$ such that: 
> $$\boxed{f'(c)=\frac{f(b)-f(a)}{b-a}}\tag{MVT}$$

^646c42

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
> Given: If $f$ is a real-valued function, defined and continuous on, and having a derivative on the open interval $(a,b)$, then there exists at least one point $c\in(a,b)$ such that: 
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
> > Note the implications of this theorem; it basically states that at some point $c$ in the closed interval of a function's domain, then there exists a derivative $f'(c)$ which returns a slope equal to the secant line of the endpoints of our function. 


^768c51
Note that MVT extends a very interesting corollary: 

> [!theorem] Corollary 1.1
> > *Given:* 
> > $f$ is a function defined & continuous on the closed interval $[a,b]$, 
> > $\exists f'(x)$, and $f'(x)=0$ for $x\in(a,b)$
> 
> Prove: $f$ is constant on the interval $[a,b]$. 
> 
> Proof: 
> If $f$ is continuous, defined on some closed interval $[a,b]$, then it is also continuous on some subinterval $[a,x]\subset[a,b]$, where $x\in(a,b]$. 
> If $f$ is differentiable on some open interval $(a,b)$, then it is also differentiable on some subinterval $(a,x)\subset(a,b)$ where $x\in(a,b]$.
> 
> Following from MVT, then there exists a point $g$ for $f'$ such that
> $$f'(g) = \frac{f(x)-f(a)}{x-a}$$
> Note from our givens, we know that $f'(g)=0$ if $g\in(a,b)$, but since $g\in(a,x)\subset(a,b)$ then the given concept of $f'(g)=0$ is still applicable: $$f'(g) = \frac{f(x)-f(a)}{x-a}=0 \implies f(x) = f(a)$$
> Note that our definition for $x$ was an arbitrary value between $a$ and $b$ (inclusive). If $x=a$, $f(a)=f(a)$, and if $x=b$, $f(b)=f(a)$ which means that across the interval of $[a,b]$, $f(x)=f(a)$, which implies that $f$ is some constant value. 

^4698a8

Or in other words, we can show that the derivative of any function across an interval will be $0$ if and only if that function is some constant.  
## Cauchy's Mean Value Theorem 
Cauchy's Mean Value Theorem is an extension of the Mean Value Theorem: 

> [!theorem] Cauchy's Mean Value Theorem
> *Given:*
> $f,g$ are two functions defined *and* continuous on an interval $[a,b]$. 
> $f,g$ also have a derivative at every interval $(a,b)$. Suppose further that $g(a)\neq g(b)$. 
> 
> Prove: There exists a point $c\in(a,b)$ for which $$\frac{f(b)-f(a)}{g(b)-g(a)} = \frac{f'(c)}{g'(c)}$$
> Proof: 
> Consider the following function: 
> $$h(x) = f(x)(g(b)-g(a))-g(x)(f(b)-f(a))$$
> Consider then $h(a)$ and $h(b)$: $$\begin{align}h(a) &= f(a)(g(b)-g(a))-g(a)(f(b)-f(a)) \\&= f(a)g(b) - f(a)g(a) -g(a)f(b) + g(a)f(a) = f(a)g(b) - f(b)g(a) \\h(b) &= f(b)(g(b)-g(a)) - g(b)(f(b)-f(a)) \\&= f(b)g(b) - f(b)g(a) - g(b)f(b) + g(b)f(a) = -f(b)g(a) + f(a)g(b) \\&\implies h(a)=h(b)\end{align}$$
> From this, Rolle's Theorem holds true, then there exists some value where $h'(c)=0$. Differentiating with respects to $x$: $$\begin{align}h'(x) = f'(x)(g(b)-g(a))-g'(x)(f(b)-f(a)) &= 0 \\f'(x)(g(b)-g(a))&=g'(x)(f(b)-f(a))  \\\frac{g(b)-g(a)}{f(b)-f(a)} &= \frac{g'(x)}{f'(x)} \\\boxed{\frac{f'(x)}{g'(x)}= \frac{f(b)-f(a)}{g(b)-g(a)}}\end{align}$$