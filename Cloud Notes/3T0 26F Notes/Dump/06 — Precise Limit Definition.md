---
updated_at: 2026-09-23T15:36:36.321-04:00
edited_seconds: 1560
course: ESC194H1
tags:
  - ESC194H1
"Lecture #": 6
Lecture Date: 2026-09-21
Week: 3
created:
Created: September 14th 2026, 9:42:17 pm
---
Hub: [[ESC194 Hub]]
Previous: [[05 — The Limit of a Function]]
Next: [[07 — Limit Laws]]

--- 

# Lecture Notes
Take the following function: 
$$
f(x) = \frac{2x^2 - x -1}{(x-1)} = \frac{(2x+1)(x-1)}{(x-1)}
$$

We know from intuition (and algebra) that $\lim_{ x \to 1}f(x)=3$. Note that we should be able to now mathematically quantify how close $x$ has to be for $f(x)$ to be within $0.1$ of $3$. Mathematically, we can define this as: 
$$|x-1|<\delta \implies |f(x)-3| < 0.1$$
That is: 
* For what value of $|x-1| < ?$ that will give $|f(x) - 3| < 0.1$? 

We could sub in our function to our second inequality to figure this out:
$$
\left|\frac{(2x+1)(x-1)}{(x-1)} - 3\right| = |(2x+1) - 3 | = |2x-2| = 2|x-1| <0.1
$$
Note that we do not consider $x=1$; then from our earlier condition of $|x-1| < ?$, we can see that $|x-1| < 0.05$. Therefore: 
* $|f(x) -3| < 0.1 \implies 0<|x-1| <0.05$; Or: 
* $0<|x-1|<0.05 \implies |f(x)-3| <0.01$, That is $x\in(1-0.05, 1+0.05)$ and $y\in(3-0.01, 3+0.01)$. 
## Generalization 
Note that if we set our $\delta = \frac{\epsilon}{2}$, then we always have a solution for this inequality. 

More generally:
* we use $\epsilon$ to represent the tolerance of our $y$ values in $|f(x) - L| <\epsilon$
* We use $\delta$ to represent the *corresponding* tolerance of our $x$ values in $|x-a| < \delta$

Our goal is to search for some $\delta>0$ such that $|x-a|<\delta \implies|f(x)-L|<\epsilon$. 
* That is , $\epsilon$ is a term that's **given**, we always try to solve for a term of $\delta$ that agrees.

Retaking our earlier example; then we can perform the same algebra: 
$$
|x - 1| < \delta
$$
$$
$$
$$
\left|\frac{(2x+1)(x-1)}{(x-1)} - 3\right| = |(2x+1) - 3 | = |2x-2| = 2|x-1| < \epsilon \implies |x-1| < \frac{\epsilon}{2}
$$
From here, we can see that we can choose that $\delta = \frac{\epsilon}{2}$, since $$|x-1| < \delta \land |x-1| < \frac{\epsilon}{2} \implies \delta = \frac{\epsilon}{2}$$
Or in English: 
* Taking the value of $x\neq 1$ to be in the interval of $(1-\delta,1+\delta)$, we can make the value of $f(x)$ lie in the interval of $(3-\epsilon,3+\epsilon)$). 

## Precise Limit Definition
See [[06 — Precise Limit Definition#Epsilon-Delta Definition]] for a formal one, but in terms of the in course one: 

> [!theorem] Definition
> Let $f(x)$ be a function defined on some *open* interval that contains the number $c$ (except possibly at $x=c$, inclusion is not required), then we say that: $$\lim_{ x \to c }f(x) = L $$
> If, $\forall\epsilon>0,\exists\delta>0$ such that: 
> $$ 0 < |x-c| < \delta \implies|f(x) - L| < \epsilon$$

That is, we attempt to trap our value of $f(x)$ within a bound of $\epsilon$ and $\delta$, if we can squeeze these values arbitrarily small, we can say that our limit exists. 

### Examples
Prove the following: 
> $$\lim_{ x \to 2 } (3x-2) = 4 $$

First, find a value for $\delta$ from $\epsilon$: 
$$
|x-2| <\delta
$$
$$
|f(x) - L| = |3x-2-4| = |3x-6| = 3|x-2| < \epsilon \implies |x-2| < \frac{\epsilon}{3}
$$
This implies that we should choose $\delta = \frac{\epsilon}{3}$. From here, we prove the other direction that it holds true: 
> Choose $\delta = \frac{\epsilon}{3}$;  then: 
> $$|x-2| < \delta$$
> Then from our $\epsilon$ inequality: 
> $$|3x-2 -4| = |3x-6| = 3|x-2| < 3\delta$$
> Take $\delta = \frac{\epsilon}{3}$, then: 
> $$3|x-2| = |(3x-2)-4| < 3\left( \frac{\epsilon}{3} \right) \implies |(3x-2)-4| < \epsilon$$
> Which is what we wanted, showing that our choice of $\delta$ satisfies our definition, and therefore our limit holds as desired. 
## One-Handed Limits
> [!theorem] Left-Handed Limit
> We define the following left handed limit: $$\lim_{ x \to c^- } f(x) = L$$ 
> For $\forall\epsilon > 0, \exists\delta>0$ such that: 
> $$c-\delta < x < c \implies |f(x) - L| < \epsilon$$
> That is, $x\in(c-\delta, c)$

> [!theorem] Right-Handed Limit
> We define the following left handed limit: $$\lim_{ x \to c^+ } f(x) = L$$ 
> For $\forall\epsilon > 0, \exists\delta>0$ such that: 
> $$c < x < c+\delta \implies |f(x) - L| < \epsilon$$
> That is, $x\in(c, c+\delta)$

### Example
> Prove the following: $$\lim_{ x \to 0^+ } \sqrt{ x } = 0$$

Our first step is to find some value of $\delta$ in the following: 
$$0<x<\delta\implies|\sqrt{ x } -0 | < \epsilon$$
Taking the $\epsilon$ side: 
$$
|\sqrt{ x }-0|=|\sqrt{ x }| =\sqrt{ x } < \epsilon  \implies x < \epsilon^2
$$
Note from the earlier definition, then we choose that $\delta = \epsilon^2$

Our next step is to actually prove this: 
> Given $\delta =\epsilon^2$, then if $0 < x < \delta$: 
> $$|\sqrt{ x }-0|=|\sqrt{ x }| =\sqrt{ x } \implies \sqrt{ x } < \sqrt{ \delta }$$
> Now, sub in our value for $\delta=\epsilon^2$, then: 
> $$\sqrt{ x }=\sqrt{ \epsilon^2 } \implies \sqrt{ x } < \epsilon$$
> Note that, taking our earlier definition, then $$|\sqrt{ x }-0| <\epsilon$$


## General Example
$$
\lim_{ x \to 2 } (x^2-1)=3
$$
Step 1: Solve for $\delta$: 
$$
|x-2| < \delta
$$
$$
|f(x) - 3| = |x^2-1-3| = |(x+2)(x-2)| = |x+2||x-2| < \epsilon
$$
Note that from here, we have a problem: We have an additional $|x+2|$ term here. We need to  constrain this more. We can constrain it by some value $k$, that is some *upper limit*: 
$$
|x+2| < k
$$
Note from our inequality properties, this implies then: 
$$
|x+2||x-2| < k|x-2|<\epsilon
$$
From our earlier $\delta$ inequality, then: 
$$
k|x-2| < \epsilon \implies |x-2| < \frac{\epsilon}{k} \implies \delta \text{ should be chosen from } \frac{\epsilon}{k}
$$

So, let's assume $\delta$ is some value $1$, that is it is an upper bound. Sub it into our earlier case for $\delta$: 
$$
|x-2| < \delta \implies |x-2| < 1 \implies 1 < x < 3 \implies 3 < x+2 < 5 \implies |x+2| < 5
$$
Note from here, we can substitute this into our earlier equation, that is $k=5$, therefore: 
$$
|x+2| < 5 \implies 5|x-2| < \epsilon \implies |x-2| < \frac{\epsilon}{5} \implies \delta = \frac{\epsilon}{5}
$$
	Note that we *we also have the condition of* $\delta=1$. That means that $$\delta = \text{min}\left\{  1, \frac{\epsilon}{5}  \right\}$$

Now let's attempt to prove this: 
Choose delta as: $$\delta = \text{min}\left\{  1, \frac{\epsilon}{5}  \right\}$$
Then, if $$0 < |x-2|< \delta$$
Then, we know that: 
$$
0 < |x-2| < \frac{\epsilon}{5} \land |x-2| < 1
$$
Note that from the inequality on the right: then: 
$$
-1 < x-2 < 1 \implies 3 < x+2 < 5 \implies |x+2| < 5
$$
Therefore, we take our $\epsilon$ term: 
$$
|f(x) - 3| = |x^2-1-3| = |(x+2)(x-2)| = |x+2||x-2| < \epsilon
$$
From here, substitute $5$ for $|x+2|$, then we can substitute in our earlier $\delta$ definition. 
$$
5|x-2| < 5\delta
$$
Assume that $\epsilon \to 0$, then $\delta = \frac{\epsilon}{5}$, meaning that the above inequality resolves to $|f(x)-3|=|x-2| <\epsilon$, therefore by definition our limit exists. 


# Pre-Lecture Notes
## Epsilon-Delta Definition
The Epsilon-Delta Definition of a limit is the formal definition of a limit past the intuitive one we tackled in the previous note. It is formally defined as the following: 
$$\lim_{ x \to c }f(x)=L \iff \forall \epsilon>0, \exists\delta >0 \text{ s.t. }$$
$$|f(x)-L|<\epsilon$$
> Note that the above line can be rewritten as:
> $$-\epsilon+L < f(x) < \epsilon + L$$

whenever: 
$$0<|x-c|<\delta \text{ though, more specifically } |x-c|<\delta$$ 
> Note that the above line implies that $x \neq c$. as that would lead to the $0<\dots$ inequality becoming false.
> We are really straight up concerned about the behavior of the function around $c$, but not at it. 


This can all be written in one line as: 
$$0<|x-c|<\delta \implies |f(x)-L| < \epsilon$$
Note that our first inequality gives us our equivalent $y$-tolerance, and our second inequality gives us our equivalent $x$-compliance. The main goal of using Epsilon Delta is found within the first line: 
$$
\forall\epsilon >0,\exists\delta > 0
$$
That is, for all $\epsilon$ greater than 0, there must exist a $\delta$ greater than 0. We need to find a consistent definition for $\delta$ with respects to $\epsilon$. We are *given* $\epsilon$. 

> [!caution] Important
> Note that the bounds of the base form of epsilon-delta are: 
> $$x\in(c-\delta,c+\delta)$$
> $$y\in(L-\epsilon,L+\epsilon)$$

> [!theorem] Tips 
> 1. Break down complex proofs into cases and work from there—and recall all of the requirements for that following statement to be true. 
> 2. If other terms exist where it isn't equivalent to our $\delta$ term, work to a way to get to it. 
> 3. Recall your inequality properties. 
> 4. Sometimes, adding and multiplying to add another bound can also be a viable candidate. 
> 5. 

> **Note** that we always should prove the previous step, and prove the forward step (i.e. solve for $\delta$), and show that this choice holds true for $\epsilon$. That is we want to work from $\epsilon$ back to $\delta$ back to $\epsilon$ for our original statement. 
### Linear Case 
Take the following function: 
$$
\lim_{ x \to 2 } f(x) = 2x+4 = 8 
$$
Taking our earlier definition, then we come with the following: 
* Given $\epsilon >0$, there exists a $\delta> 0$ such that: 
$$|f(x) -L| < \epsilon$$
$$
0 < |x-a| < \delta
$$

> [!axiom] Proof 
> Fill in our definitions for the two inequalities we have above: 
> $$|2x+4-8| < \epsilon$$
> $$0<|x-2|<\delta$$
> Simplify our first inequality: 
> $$|2x-4| < \epsilon$$
> Note that we can factor this; ergo: 
> $$2|x-2| < \epsilon$$
> Recall how $|x-2| <\delta$, then this implies that $\delta = \frac{\epsilon}{2}$. Since we have defined $\delta$ in terms of $\epsilon$, this holds for all values of $\epsilon$, ergo the limit exists. 
> > Forward Direction Proof
> > Let's take the forward direction, choose $\delta = \frac{\epsilon}{2}$, then take our corresponding $y$ tolerance: 
> > $$|(2x)|$$
## One-Sided Limits
Recall our intuitive definitions of one-sided limits from our previous note: 
> [!theorem] Intuitive One-Sided Limit Definition: 
> Let us define our one-sided limits: 
> $$\lim_{ x \to ^-a } f(x) = L$$
> The limit $L$ exists if we can make $f(x)$ arbitrarily close to $L$ while ensuring $x$ is sufficiently close to and also less than $a$. 
> $$\lim_{ x \to ^+a }f(x) = L $$
> The limit $L$ exists if we can make $f(x)$ arbitrarily close to $L$ while ensuring that $x$ is sufficiently close to, and also greater than $a$.

These can be formally defined under the Epsilon-Delta Framework. Note that for one-sided limits converging to a value; the $|f(x)-L|<\epsilon$ rule holds. 

> [!theorem] Positive One-Sided Limits
> Recall how we defined approaching a limit from the right as approaching from values of $x>c$; we can specify this in our $\delta$ tolerances, that being that we want to approach via the interval of $(c,c+\delta)$, therefore: 
> $$\lim_{ x \to ^+c } f(x) = L$$
> Which for $\forall\epsilon>0,\exists\delta>0 \text{ such that:}$
> $$c \leq x \leq c+\delta \text{ or } x \leq c+\delta$$
> $$|f(x) - L|<\epsilon$$

> [!theorem] Negative One-Sided Limits
> Recall how we defined approaching a limit from the right as approaching from values of $x<c$; we can specify this in our $\delta$ tolerances, that being that we want to approach via the interval of $(c-\delta,c)$, therefore: 
> $$\lim_{ x \to ^+c } f(x) = L$$
> Which for $\forall\epsilon>0,\exists\delta>0 \text{ such that:}$
> $$c-\delta \leq x \leq c$$
> $$|f(x) - L|<\epsilon$$

> [!caution] Note
> Recall that if both one-sided limits are equal, then our limit overall exists. 
> This means that **from either direction, our function must be at minimum defined in some way.**

### Examples
## Infinite Limits
We also seek to define the concept of *infinite limits* rigorously within our function, that are limits with diverge out into infinity. 

> [!theorem] Infinite Limit - $+\infty$
> Given the following limit: 
> $$\lim_{ x \to c }f(x) = \infty $$
> Then, $\forall M, \exists\delta>0 \text{ such that}$
> $$0<|x-c| < \delta$$
> $$f(x) > M$$
> Where $M$ is any positive number.  
> > What this means is that the value of our function will be *greater than any positive number* at $x$.

> [!theorem] Infinite Limit: $-\infty$
> Given the following limit: 
> $$\lim_{ x \to c } f(x) = -\infty$$
> Then, $\forall N, \exists\delta>0$ such that: 
> $$0 < |x-c| <\delta$$
> $$f(x) < N$$
> Where $N$ is any negative number. 
> > Note that the second inequality means that the value of our function will be *less than any negative number* at $x$

Note that for one-sided limits, the bounds of $\delta$'s inequality change, while the term for the respective $y$ term (i.e, the one including $N \text{ or }M$) remains the same. We can combine these inequalities at will to describe the type of behavior we want to describe. 


