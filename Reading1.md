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
