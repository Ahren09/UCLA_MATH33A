# Lecture (Feb 9)
## Bases and Dimension
### Definition
* The member of elements of a basis of a subspace V is called the dimension of V (denoted by `dim(V)`)
* Ex: V = {(x,y,z) such that y=3x}. Show that V is a subspace of ℝ<sup>3</sup> (can be done directly).
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
* Ex: Show that v<sub>1</sub> and v<sub>2</sub> are linearlly independent. 
  * v<sub>1</sub> and v<sub>2</sub> span N(A) = V. Hence, {v<sub>1</sub>, v<sub>2</sub>} is a basis of N(A) = V. Therefore, dim(N(A)) = dim(V) = 2.
