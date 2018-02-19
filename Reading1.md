# Linear Algebra with Applications - Bretscher (2015)
## 3.1 Subspaces of ℝ<sup>n</sup> and their Dimensions
### Finding Kernel of a Matrix (AKA Null Space)
1. rref(A)
2. Write the non-pivot columns of rref(A) as their own column vectors, separated by commas, in order
   * If there are no non-pivot columns in rref(A), then the columns are independent. This means the kernel only contains the zero vector, where the number of rows equals the number of columns in A 
3. Multiply each of these column vectors by -1
4. Append the identity matrix to the bottom of these column vectors such that their number of rows equals the number of columns in A
5. The resulting columns span the kernel of A
### Finding Image of a Matrix
1. rref(A)
2. Note the pivot columns. Write the corresponding original columns from A as their own column vectors, separated by commas, in order
3. The resulting columns span the kernel of A
## 3.2 Subspaces of ℝ<sup>n</sup>, Bases and Linear Independence
* The pivot columns of a matrix A are linearly independent vectors, while the non-pivot columns are linearly dependent
### Prove V is a Subspace
1. V must contain the zero vector
2. V is closed under addition (for any two vectors in V, the sum of these vectors is also in V)
3. V is closed under scalar multiplication (for any vector in V multiplied by a scalar, the product is also in V)
## 3.3 The Dimension of a Subspace of ℝ<sup>n</sup>
### Finding Dimension of a Subspace
1. Find a basis of the subspace
2. How many vectors are in the basis? The subspace has that many dimensions
