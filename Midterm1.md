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
* From rref(A), we can determine the *rank* of A, rank(A), which is the number of leading 1s.
* **KNOW THE PROPERTIES OF RANK(A); MEANING OF RANK**
