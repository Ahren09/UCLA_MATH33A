# Math 33A: Linear Algebra - Final Exam Review
## 3.1 Subspaces of ℝ<sup>n</sup> and their Dimensions
### Finding Kernel of a Matrix (AKA Null Space)
1. rref(A)
2. Write the non-pivot columns of rref(A) as their own column vectors, separated by commas, in order
   * If there are no non-pivot columns in rref(A), then the columns are independent. This means the kernel only contains the zero vector, where the number of rows equals the number of columns in A 
3. ***Multiply each of these column vectors by -1***
4. Append the identity matrix to the bottom of these column vectors such that their number of rows equals the number of columns in A
5. The resulting columns span the kernel of A
* [Example](https://www.youtube.com/watch?v=bqBacABVCeQ)
### Invertibility
* A matrix is invertible iff: rref(A) = I, rank(A) = n, im(A) = n, ker(A) = {0}
### Finding Image of a Matrix (AKA Range)
1. rref(A)
2. Note the pivot columns. Write the corresponding original columns from A as their own column vectors, separated by commas, in order
3. The resulting columns span the image of A
* [Example](https://www.youtube.com/watch?v=xa92zIehBZ8)
## 3.2 Subspaces of ℝ<sup>n</sup>, Bases and Linear Independence
* The pivot columns of a matrix A are linearly independent vectors, while the non-pivot columns are linearly dependent
### Prove V is a Subspace
1. V must contain the zero vector
2. V is closed under addition (for any two vectors in V, the sum of these vectors is also in V)
3. V is closed under scalar multiplication (for any vector in V multiplied by a scalar, the product is also in V)
* [Example](https://www.youtube.com/watch?v=rPF6Xk5OGU8)
### Determine if Vectors are Linearly Independent
1. Create an augmented matrix with the vectors in question and add a zero column to the right-most side
2. Determine rref of the matrix
3. If there is a leading 1 in each column, the vectors are linearly independent. Otherwise, they are linearly dependent
## 3.3 The Dimension of a Subspace of ℝ<sup>n</sup>
### Finding Dimension of a Subspace
1. Find a basis of the subspace
2. How many vectors are in the basis? The subspace has that many dimensions
* [Example](https://www.youtube.com/watch?v=kfVI7Tp98WM)
### Rank-Nullity Theorem
* For any `n x m` matrix: dim(ker A) + dim(imA) = m
* Equivalently, (nullity of A) + (rank of A) = m
## 3.4 Coordinates
* [x]<sub>B</sub> indicates that the vector x has been written with respect to the basis B, not the standard basis
### Find x given [x]<sub>B</sub>
1. Multiply each element in [x]<sub>B</sub> by its corresponding vector in the basis B
2. Sum the resulting vectors to yield x
* [Example](https://www.youtube.com/watch?v=7P_XGrb3d3c)
### Find [x]<sub>B</sub> given x
1. Create an augmented matrix with the vectors in the basis B on the left and the vector x on the right
2. Find rref of the matrix from step (1). The result in the right-most column of the augmented matrix is [x]<sub>B</sub>
* [Example](https://www.youtube.com/watch?v=4sBXY1BCU3w)
### Find the Matrix B of the Linear Transformation T(x) = Ax with Respect to the Basis (v<sub>1</sub>, ... , v<sub>m</sub>)
1. Write the basis v<sub>1</sub>, ... , v<sub>m</sub> as a single matrix with each v<sub>i</sub> being a column vector. Call it C.
2. Find C<sup>-1</sup>.
   * To find the inverse of a `2 x 2` matrix, swap the positions of a and d, put negatives in front of b and c, and divide everything by the determinant (ad-bc).
3. Multiply the matricies C<sup>-1</sup>AC. This will give us B. 
* [Example](https://www.youtube.com/watch?v=lCRGNykWqFI)
### Similar Matricies
* Consider two `n × n` matrices A and B. We say that A is similar to B if there exists an invertible matrix S such that AS = SB, or B = S<sup>−1</sup>AS.
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
* Orthogonal matricies must have unit vector columns
* A symmetric matrix is a matrix that is equal to its transpose
## 5.4 Least Squares and Data Fitting
### Least Squares Solution to a System Ax = b
1. Find A<sup>T</sup>A and A<sup>T</sup>b
2. Solve the augmented matrix formed by A<sup>T</sup>A on the left and A<sup>T</sup>b on the right; [A<sup>T</sup>A | A<sup>T</sup>b]
## 6.1 Intro to Determinants
* Determinant of a 2x2 matrix: det(A) = ad-bc
* If a matrix's determinant is 0, it is not invertible
* Inverse of a 2x2 matrix: 
```
   1
 _____   | d   -b |
 ad-bc   | -c   a |
```
### Determinant of a 3x3 Matrix
* [Copy the first two columns of the matrix, put them on the right of the matrix](https://www.youtube.com/watch?v=V3e7m-qFDFU)
* Notice that we can form three diagonals (left-right) of three elements. Multiply the elements of each diagonal, then add them all together. Call this result A.
* Notice that there are three more diagonals (right-left). Again, multiply the elements of each and add them all together. Call this result B.
* det(A) = A - B
### Inverse of a 3x3 Matrix
* [A<sup>-1</sup> = (1/|det(A)|)(adj(A))](https://www.youtube.com/watch?v=pKZyszzmyeQ)
* Where adj(A) is the 3x3 matrix generated by finding the 2x2 determinant of each element in A (block the row and column of the current element, find the determinant; that value is the new element for that position). 
* THEN, TAKE THE TRANSPOSE
* Then, change the signs of each element in adj(A) as follows:
```
| +  -  + |
| -  +  - |
| +  -  + |
```
## 6.2 Properties of the Determinant
* If A is a square matrix, the determininant of the transpose is the same as the determinant of the original: det(A<sup>T</sup>) = det(A) 
* Similar matricies have the same determinants
### Elementary Row / Column Operations and Determinants
* If B is obtained from A by dividing a row of A by a scalar k, then det(B) = (1/k)(det(A))
* If B is obtained from A by a row swap, then det(B) = - det(A); the determinant is *alternating* on rows
* If B is obtained from A by adding a multiple of row A to another row, then det(B) = det(A)
### Determinants of Products and Powers
* If A and B are square matricies and m is a positive integer:
  * det(AB) = (det A) (det B) 
  * det(A<sup>m</sup>) = (det A)<sup>m</sup>
## 6.3 Geometrical Interpretations of the Determinant; Cramer’s Rule
* The determinant of an orthogonal matrix is either 1 or −1
* An orthogonal n×n matrix A with det A = 1 is called a rotation matrix, and the linear transformation T (x) = Ax is called a rotation
### Area of a Parallelogram
* Same as finding the determininant of the 2x2 matrix formed by the vectors that define the parallelogram
### Volume of a Parallelopiped 
* Same as computing a 3x3 determinant
* Build a matrix out of the vectors that define the edges, switch the result to a positive if it comes out negative
### Cramer's Rule to Solve a 3x3 Matrix
* We have a system of three equations that forms a 3x3 matrix A, with an augmented matrix on the right
* Let A_x denote the matrix formed by replacing the first column of A with the augmented matrix, A_y is the matrix formed by replaying the second column of A with the augmented matrix, and so on.
* x = det(A_x)/det(A), y = det(A_y)/det(y), z = det(A_z)/det(A)
## 7.2 Finding the Eigenvalues of a Matrix
* The sum of the diagonal entries of a square matrix A is called the trace of A, denoted by tr(A)
### Using the Characteristic Polynomial to Find Eigenvalues
* Characteristic polynomial of A: f<sub>A</sub>(λ) = det(λI-A)
* Eigenvalues of A are the roots of the characteristic polynomial 
## 7.3 Finding the Eigenvectors of a Matrix
* [The Eigenspace E<sub>λ</sub> is the set of all solutions Ax = λx; basically all Eigenvectors with Eigenvalue λ, except 0](https://www.youtube.com/watch?v=MU_KCNKKEA0)
* Eigenspace = null(λI-A) = ker(λI-A)
* To find the basis for the Eigenspace, just find null(λI-A) for each Eigenvalue λ, one at a time
* Geometric multiplicity: the dimension of the Eigenspace, dim(null(λI-A))
### When are matricies diagonalizable?
* [Only when the geometric multiplicities of the Eigenvalues add up to 1](https://www.youtube.com/watch?v=OR3_o1VERy)
* For every Eigenvalue, the algebraic multiplicity is equal to the geometric multiplicity
  * We don't have to check cases where algebraic multiplicity is 1
## 8.1 Orthogonal Diagonalization
1. [Find Eigenvalues of the matrix](https://www.youtube.com/watch?v=-eKA0mYNDDQ)
2. Find Eigenvectors of the matrix for each Eigenspace
4. Orthonormalize each set of Eigenvectors with Gram-Schmidt
5. Combine all the vectors together to form a matrix
