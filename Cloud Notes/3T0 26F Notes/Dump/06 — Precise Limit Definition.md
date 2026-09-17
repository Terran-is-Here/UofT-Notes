---
updated_at: 2026-09-17T13:56:41.598-04:00
edited_seconds: 400
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


This can all be written in one line as: 
$$0<|x-c|<\delta \implies |f(x)-L| < \epsilon$$
Note that our first inequality gives us our equivalent $y$-tolerance, and our second inequality gives us our equivalent $x$-compliance. The main goal of using Epsilon Delta is found within the first line: 
$$
\forall\epsilon >0,\exists\delta > 0
$$
That is, for all $\epsilon$ greater than 0, there must exist a $\delta$ greater than 0. We need to find a consistent definition for $\delta$ with respects to $\epsilon$. We are *given* $\epsilon$. 
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
