# Math 33A: Linear Algebra - Final Exam Review
## 5.1: Orthogonal Projections and Orthonormal Bases
* Angle between two vectors: `cosθ = (u·v) / (|u||v|)`
* Vectors are orthogonal when their dot product is 0
* Unit vector: a vector that has length of 1
### Orthogonal Projection onto a Subspace
* [We want to project vector v onto a subspace spanned by multiple vectors](https://www.youtube.com/watch?v=kIWLliTGPEQ)
* Create a matrix A out of the vectors being spanned, then find A<sup>T</sup>
* Find A<sup>T</sup>A and A<sup>T</sup>v
* Find x in (A<sup>T</sup>A)x = A<sup>T</sup>v
* Multiply each element of x by its corresponding vector in the subspace (i.e. first row x multiplied by the first subspace vector)
### Orthogonal Projection onto a Subspace Shortcut
* If the subspace V is composed of orthonormal vectors u<sub>1</sub>...u<sub>m</sub>, then the orthogonal projection is simply (u<sub>1</sub>·x)u<sub>1</sub>+...+(u<sub>m</sub>·x)u<sub>m</sub>
## 5.2 Gram–Schmidt Process and QR Factorization
### Gram-Schmidt
* Orthonormalize 3 vectors x<sub>1</sub>, x<sub>2</sub>, x<sub>3</sub>:
  * v<sub>1</sub> = x<sub>1</sub>
  * v<sub>2</sub> = x<sub>2</sub> - ((x<sub>2</sub> • v<sub>1</sub>) / (v<sub>1</sub> • v<sub>1</sub>))v<sub>1</sub>
  * v<sub>3</sub> = x<sub>3</sub> - ((x<sub>3</sub> • v<sub>1</sub>) / (v<sub>1</sub> • v<sub>1</sub>))v<sub>1</sub> - ((x<sub>3</sub> • v<sub>2</sub>) / (v<sub>2</sub> • v<sub>2</sub>))v<sub>2</sub>
  * At this point, we have orthogonal vectors. To get orthonormal vectors, we need to divide each v by its maginitude, ||v||. In other words, we divide each vector by the square root of the sum of its elements squared. 
  * [Example](https://www.youtube.com/watch?v=swXcm_vTjWU)
### QR Factorization
1. Find an orthonormal basis of A using Gram-Schmidt; combine orthonormal column vectors to form matrix Q
2. R = Q<sup>T</sup>A
## 5.3 Orthogonal Transformations and Orthogonal Matricies
* For a square matrix, A is orthogonal if and only if A<sup>T</sup>A=I, or equivalently, A<sup>-1</sup>=A<sup>T</sup>
### Least Squares Solution to a System Ax = b
1. Find A<sup>T</sup>A and A<sup>T</sup>b
2. Solve the augmented matrix formed by A<sup>T</sup>A on the left and A<sup>T</sup>b on the right; [A<sup>T</sup>A | A<sup>T</sup>b]
