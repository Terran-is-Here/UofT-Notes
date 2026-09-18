---
updated_at: 2026-09-18T13:33:31.721-04:00
edited_seconds: 520
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
Next: N/A

--- 

# Lecture Notes
# Pre-Lecture Notes
## Epsilon-Delta Definition
The Epsilon-Delta Definition of a limit is the formal definition of a limit past the intuitive one we tackled in the previous note. It is formally defined as the following: 
$$\lim_{ x \to c }f(x)=L \iff \forall \epsilon>0, \exists\delta >0 \text{ s.t. }$$
$$|f(x)-L|<\epsilon$$
> Note that the above line can be rewritten as:
> $$-\epsilon+L < f(x) < \epsilon + L$$

whenever: 
$$0<|x-c|<\delta$$
> Note that the above line implies that $x \neq c$. as that would lead to the $0<\dots$ inequality becoming false.
> We are really straight up concerned about the behavior of the function around $c$, but not at it. 


This can all be written in one line as: 
$$0<|x-c|<\delta \implies |f(x)-L| < \epsilon$$
Note that our first inequality gives us our equivalent $y$-tolerance, and our second inequality gives us our equivalent $x$-compliance. The main goal of using Epsilon Delta is found within the first line: 
$$
\forall\epsilon >0,\exists\delta > 0
$$
That is, for all $\epsilon$ greater than 0, there must exist a $\delta$ greater than 0. We need to find a consistent definition for $\delta$ with respects to $\epsilon$. We are *given* $\epsilon$. 

> [!theorem] Tips 
> 1. Break down complex proofs into cases and work from there—and recall all of the requirements for that following statement to be true. 
> 2. If other terms exist where it isn't equivalent to our $\delta$ term, work to a way to get to it. 
> 3. Recall your inequality properties. 
> 4. Sometimes, adding and multiplying to add another bound can also be a viable candidate. 
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
> Recall how we defined approaching a limit from the right as 