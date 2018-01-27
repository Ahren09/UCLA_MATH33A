# Midterm 1 Review (Jan 26, 2018)
## Main Topics
* Solving linear systems
* Gauss-Jordan elimination 
  * Notion of "rank"
* Matrix calculus
* Matrix inversion
* Linear transformations
* Geometric operations through linear transformation
## Suggested Exercises
* Chapter 1.1: 31-41
* Chapter 1.2: 19-30
* Chapter 1.3: 6-8, 22-48
### How to solve linear systems and the Gauss-Jordan algorithm
* Gauss-Jordan algorithm
  1. Set coefficient of x<sub>j</sub> equal to 1 in the j<sup>th</sup> equation and eliminate it from the rest
  2. Switch order of equations if step (1) is not immediately possible
  3. In matrix form, we start with the system Ax = b. From Guass-Jordan, we get the reduced-row echelon form, rref(A).
* From rref(A), we can determine rank(A), which is simply the number of leading 1s.
* **KNOW THE PROPERTIES OF RANK(A); MEANING OF RANK**

Example: Consider the system

```
 w  + 2x     + 3z = 0
2w +   x     + az = b
       x + y      = 1
           y + 3z = 0
```

Solution:

In matrix form, we have Ax = c
```
| 1 2 0 3 |  | w |       | 0 |
| 2 1 0 a |  | x |       | b |
| 0 1 1 0 |  | y |   =   | 1 |
| 0 0 1 3 |  | z |       | 0 |
```
