# Lecture (Feb 12, 2018)
## Subspaces
* Notation: V ⊆ ℝ<sup>n</sup>
  * V is a subspace of ℝ<sup>n</sup>
* B = {v<sub>1</sub>, ..., v<sub>m</sub>}
* For every v in V, there exist unique numbers (with respect to B) c<sub>1</sub>, ..., c<sub>m</sub> such that v=c<sub>1</sub>v<sub>1</sub>+c<sub>m</sub>v<sub>m</sub> where c values are *B-coordinates of V*
* Notation: [v]<sub>B</sub> = 
  ```
  | c_1 |
  | ... |
  | c_m |
  ```
* Another basis for ℝ<sup>2</sup>: 
  ```
  B =  { | 2 |   | 0 | }
         | 0 | , | 2 |
  ```
  * Then for v = 
  ```
  | x |
  | y |
  ```
    * We have that v = (x/2)v<sub>1</sub>+(y/2)v<sub>2</sub>
    * Means:
      ```
      [v]_b = | x/2 |
              | y/2 |
      ```
### Finding A
* For {e<sub>1</sub>, ..., e<sub>m</sub>}, the standard basis of ℝ<sup>n</sup> we evaluate
  ```
      |  ...     ...  |
  A = | f(e_1) f(e_m) |
      |  ...     ...  |
  ```
#### Theorem
* Let f ℝ<sup>m</sup> -> ℝ<sup>n</sup> be a linear transformation and let B={v<sub>1</sub>, ..., v<sub>1</sub>} be a basis of  ℝ<sup>m</sup>. Then there exists a matrix A<sub>B</sub> that takes [x]<sub>B</sub> to [f(x)]<sub>B</sub>.
  * [f(x)]<sub>B</sub> = A<sub>B</sub>[x]<sub>B</sub>
* How to find A<sub>B</sub>:
  ```
        |    ...           ...     |
  A_B = | [f(v_1)]_b    [f(v_m)]_b |
        |    ...           ...     |
  ```
  * Ex: f is ℝ<sup>2</sup> -> ℝ<sup>2</sup>, f(x,y) = (x+y, y). F is a linear transformation such that B<sub>ℝ<sup>2</sup></sub>={e<sub>1</sub>, e<sub>2</sub>}. What is A (2x2) such that f(x) = Ax?
    ```
    B =  { | 2 |   | 0 | }
           | 0 | , | 2 |
           
          |  ...       ...  |
    A_B = | f(2,0)   f(0,2) |
          |  ...       ...  |
        
         = | 2 2 |
           | 0 2 |
    ```
### Coordinate System Changes
* Where
  ```
        | ...   ... |
    S = | v_1   v_m |
        | ...   ... |
  ```
  * AS = SA<sub>B</sub>
  * A<sub>B</sub> = S<sup>-1</sup>AS
