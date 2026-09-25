---
updated_at: 2026-09-25T12:11:15.408-04:00
edited_seconds: 180
course:
tags:
"Lecture #": 0
Lecture Date: 2026-09-23
Week:
---
Hub: [[ESC180 Hub]]
Previous: [[5 — ESC180 Lecture 5]]
Next: [[8 — ESC180 Lecture 8]]

--- 
# Lecture Notes
## Calculating Pi 
Given a random allotment of points within $(0,0)-(1,1)$, we can check if they lie within the top-right corner of a square if their $x^2 + y^2 \geq 1$. Recall that $\pi r^2 = a$ where $a$ is the area of a circle. Pi can be generally calculated as 
$$
4 * \frac{\text{number of points within unit circle quadrant}}{\text{number of points within unit square quadrant}}
$$

```python
import random

# Let N be equal to the number of points that we place within the circle: 
N = 100000
count = 0 # And let count be equal to the number of points that lie within the unit circle inscribed within the unit square: 

for i in range(N): 
	x,y = random.random(), random.random() # generates (random.random(), random.random()) 
	if (x**2 + y**2) < 1: #Check if they lie within the unit circle: 
		count += 1 # If they do lie within the unit circle, increment our count. 
		
pi = (4*count/N) 
```
