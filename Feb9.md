# Lecture (Feb 9)
## Bases and Dimension
### Definitions
* The member of elements of a basis of a subspace V is called the dimension of V (denoted by `dim(V)`)
* N(A) is the null space of A
* R(A) is the range of A
#### Examples
* Ex: `V = {(x,y,z) such that y = 3x}`. Show that V is a subspace of ℝ<sup>3</sup> (can be done directly).
  * Note: 
    ```
    if A = [3 -1 0]
    
             | x |                            | x |
    then if  | y |  is in N(A), then [3 -1 0] | y | = 0.
             | z |                            | z | 
             
    Hence 3x-y = 0, so y = 3x. Therefore, N(A) = V.
    ```
  * Note: 
    ```
        | x |                          
    If  | y |  is in N(A)
        | z |                      
             
    Then z can be anything z = s, where s is a real number. Also, x can be anything such that x = t, where t is a real number.
    
    Then, y = 3t.
    
           | x |                                 | 0 |     | 1 |
    So if  | y |  is in N(A), it's of the form s | 0 | + t | 3 | for s, t.
           | z |                                 | 1 |     | 0 |
    ```
  * Every element of N(A) is a linear combination of 
    ```
         | 0 |       | 3 |
    v1 = | 0 |, v2 = | 1 |
         | 1 |       | 0 |
    ```
* Ex: Show that v<sub>1</sub> and v<sub>2</sub> are linearly independent. 
  * v<sub>1</sub> and v<sub>2</sub> span N(A) = V. Hence, {v<sub>1</sub>, v<sub>2</sub>} is a basis of N(A) = V. Therefore, dim(N(A)) = dim(V) = 2.
### Fact
* Let V be a subspace of ℝ<sup>n</sup> (V ⊆ ℝ<sup>n</sup>) and let `dim(V) = k`. Then the following are equivalent:
  1. We can find at most K linearly independent vectors in V
  2. We need at least k vectors to span V
  3. If k vectors in V are linearly independent, then they form a basis of V
  4. If k vectors in V span V, then they form a basis of V
## Solving a Typical Basis Exercise
* Find a basis for
  * N(A) -> solve Ax = 0.
  * R(A) -> find rref(A). Consider the columns with leading 1s.
### Fact
* `dim(R(A)) = rank(A)`
### Theorem
* Let A be an `n x m` matrix. Then, **dim(N(A)) + dim(R(A)) = m**.
### Application
```
Let A be an invertible `n x m` matrix. 

Then, rank(A) = n; so dim(R(A)) = n.

Hence, dim(R(A)) + dim(N(A)) = n

n + dim(N(A)) = n
dim(N(A)) = 0
N(A) = {0}
```
Hence, we get the following fact:
#### Fact
* The columns of every invertible `n x n` matrix form a basis of ℝ<sup>n</sup>; conversely, if you have n vectors v<sup>1</sup>, ...,  v<sup>m</sup> that form a basis of ℝ<sup>n</sup>, then:
```
    | ...    ... |
A = | v1      v2 | is invertible.
    | ...    ... |
```
#### Theorem
* Let A be `n x n`. The following are true:
  1. A is invertible
  2. Ax = b has a unique solution 
  3. Ax = 0 means that x = 0. In other words, N(A) = {0}.
  4. R(A) =  ℝ<sup>n</sup>
  5. rref(A) = I<sub>n</sub>
  6. 
   ```
       | ...    ... |
   A = | v_1    v_m | => {v_1, ..., v_m} is a basis of ℝ^n.
       | ...    ... |
   ```
* On the rank-nullity theorem: if A is `n x m`, dim(R(A)) + dim(N(A)) = m.
  * Why? 
    * N(A) is a subspace of ℝ<sup>n</sup>. 
    * dim(N(A)) = number of free variables of Ax = 0.
