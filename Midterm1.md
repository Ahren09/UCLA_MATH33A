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

* Example: Consider the system

  ```
   w  + 2x     + 3z = 0
  2w  +  x     + az = b
         x + y      = 1
             y + 3z = 0
  ```

    * Solution: In matrix form, we have Ax = c.
      ```
      | 1 2 0 3 |  | w |       | 0 |
      | 2 1 0 a |  | x |       | b |
      | 0 1 1 0 |  | y |   =   | 1 |
      | 0 0 1 3 |  | z |       | 0 |
      ```
      We now apply Gauss-Jordan. In order, our row operations are: -2(i)+(ii); 3(iii) + (ii); -3(iv) + (iii)
      As a result, we get the system:
      ```
       w  + 2x     +      3z = 0
          - 3x     + (-6+a)z = b
                3y + (-6+a)z = 3+b
                    (-15+a)z = b+3
       ```
       * If `a ≠ 15`, then `z = (3+b)/(-15+a)`. Through backwards substitution, we get a unique solution for the system.
       * If `a = 15` and `b ≠ -3`, then there is no solution.
       * If `a = 15` and `b = -3`, then we have infinitely many solutions of the form: 
         ```
         | 1 |   | -9 |
         | 1 |   |  3 |
         | 0 | + | -3 |
         | 0 |   |  1 |
         ```
#### Rank Examples
* Example 1: Is it always true that rank(A+B) = rank(A) + rank(B)?

  Let A, B be square matricies.
  
  Choose A = I, B = -I. Then, rank(A) + rank(B) = n + n = 2n.
  
  However, rank(A + B) = rank(0<sub>n x n</sub> = 0 ≠ 2n.
  
* Example 2: let `A` be an `m x n` matrix. If `Ax = b` has no solutions, is it true that `Ax = 0` has infinitely many solutions when `n > m`? Note that `n` is the number of unknowns and `m` is the number of equations.

  Answer: Since the number of unknowns is greater than the number of equations, `Ax = 0` has infinitely many solutions by looking at the rref(A).
