---
updated_at: 2026-09-17T13:11:43.907-04:00
edited_seconds: 490
course: ESC194H1
tags:
  - ESC194H1
"Lecture #": 5
Lecture Date: 2026-09-18
Week: 2
created:
Created: September 12th 2026, 11:37:56 am
---
Hub: [[ESC194 Hub]]
Previous: [[02 — The Real Number System]], [[04-05 — Overview of Basic Mathematical Concepts]]
Next: [[06 — Precise Limit Definition]]

> [!quote] Material Source
> Chapter 1.5 of the Textbook ([[Stewart 9th Edition Textbook.pdf#page=88|Stewart 9th Edition Textbook, p.51]])

--- 

# Lecture Notes
# Pre-Lecture Notes
## Definitions of a Limit 
Intuitively, we can define the limit as the following: 
> [!theorem] Intuitive Limit Definition
> Let $f(x)$ be defined when some value $x$ is near $a$; then we can write: 
> $$\lim_{ x \to a} f(x) = L $$
> That is, the limit of $f(x)$ as it approaches $a$ is some value $L$. 
> Or: $$x \to a \implies f(x) \to L$$
> Note that $x$ does not need to equal $a$; we simply wish to determine what (or if) there is a value that our function **converges** onto as we approach our value $a$. 
> **A more formal definition will come in a later note (future me, please link it here)**

Recall that in general, a limit is solely concerned with the state of the function at a locality around a point. Also recall the intuitive definition of the concept of a one-sided limit: 
> [!theorem] Intuitive One-Sided Limit Definition: 
> Let us define our one-sided limits: 
> $$\lim_{ x \to ^-a } f(x) = L$$
> The limit $L$ exists if we can make $f(x)$ arbitrarily close to $L$ while ensuring $x$ is sufficiently close to and also less than $a$. 
> $$\lim_{ x \to ^+a }f(x) = L $$
> The limit $L$ exists if we can make $f(x)$ arbitrarily close to $L$ while ensuring that $x$ is sufficiently close to, and also greater than $a$.

From here we can also glean another property with limits: 
> $$\lim_{ x \to a }f(x) = L \iff \lim_{ x \to ^+a }f(x) = \lim_{ x \to ^-a }f(x) = L  $$
> Or in other words; our Limit only exists if and only if both one-sided limits share the same value $L$. 

## Limits that Don't Exist
Recall our two main means that we determine if a limit exists: 
* Our one-sided limits do not agree on a value; that is they do not have equality. 
* Our limits do not have convergence: 
	* They either diverge into infinity
	* Or they diverge on a range of numbers. 

> [!theorem]+ Heaviside Function
> $$f(x) = \begin{cases}1 : x\geq0\\-1: x < 0 \\ \end{cases}$$
> Let's attempt to find the limit of this function at 0; that is: 
> $$\lim_{ x \to 0 }f(x) = ?$$
> Let's try approaching from the left; then: 
> $$\lim_{  x \to ^-0 }f(x) = ? $$
> Since $x < 0$ as we are approaching from the right, then: 
> $$\lim_{  x \to ^-0 }f(x) = -1 $$
> Conversely we can also find our corresponding right-sided limit using the same logic: 
> $$\lim_{  x \to ^+0 }f(x) = +1 $$
> Therefore, our limit does not exist. 

We shall take the divergent cases separately in order to develop our definitions for them: 

### Infinite Limits
Take the following function: 
$$
f(x) = \frac{1}{x^2}, \lim_{ x \to 0 }f(x) = ? 
$$
To find the limit of this; let's try testing this function for values approaching $0$. We find that our values for both sides of the function explode into incredibly larger and larger numbers.

The value of this function does not exist; ergo we describe this as an infinite limit. 