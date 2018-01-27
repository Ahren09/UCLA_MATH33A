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
  / 
* Example 2: Let A be an `m x n` matrix. If `Ax = b` has no solutions, is it true that `Ax = 0` has infinitely many solutions when `n > m`? Note that `n` is the number of unknowns and `m` is the number of equations.

  Answer: Since the number of unknowns is greater than the number of equations, `Ax = 0` has infinitely many solutions by looking at the rref(A).

* Example 3: Following from the previous example, what happens when `n < m` (the number of unknowns is less than the number of equations)?

  Answer: There is only one solution. 

* Example 4: If `Ax = 0` has infinitely many solutions, does there exist some real number `b` such that `Ax = b` has no solution when `n > m`?
  
  Answer: No.

* Example 4: Following from the previous example, what if `m > n`?
  
  Answer: Yes. Consider the rref(A). If `Ax = 0` has infinitely many solutions, then rref(A) cannot be I<sub>n x n</sub>.

* Example 5: If `Ax = 0` has a unique solution, does `Ax = b` have a unique solution if `n = m` and we know that there exists at least one solution to `Ax = b`?

  Answer: Yes. Assume that the given solution to `Ax = b` is x = x<sub>b</sub> and assume that there is another solution to it. x = x<sub>c</sub> ≠ x<sub>b</sub>. Then, Ax<sub>b</sub> - Ax = 0.
  
  However, A(x<sub>b</sub> - Ax<sub>c</sub>) = 0 has two solutions. This is a contradiction.
  
### Matricies
* Add, multiply, compuute inverse when `n = m`
* Properties of inverses
  * If you are given A, B and you are asked to prove that A = B, it's enough to show that A<sup>-1</sup> = B<sup>-1</sup>.
* Transpose properties
#### Matrix Examples
* Example 1: Show that a square matrix with two rows equal to each other is not invertible.
  
  Answer: Consider the rref(A. If x<sub>j</sub> = x<sub>k</sub> for `j ≠ k`, then by adding -x<sub>j</sub> to x<sub>k</sub> we get a row of zeros in the rref(A). Note that j and k denote rows.

* Example 2: Take x, project it on L; w is a vector parallel to L. [Consider the matrix A](Images/ex1.jpg)
