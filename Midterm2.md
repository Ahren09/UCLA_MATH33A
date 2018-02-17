# Midterm 2 (Feb 16, 2018)
## Subspaces
Given a subset V of ℝ<sup>n</sup>, how do we check if V is a subspace?
* To show it is a subspace, verify:
  1. For all x and y, x+y exists in V
  2. For all x, x exists in V. Also, for any constant λ, λx exists in V.
  * Suggestion: pick two random x and y in V and show that λx + μy exist in V.
* To show it is not a subspace, it is enough to demonstrate that for either one of the two above conditions fail.
### Remark
If V is a subspace of ℝ<sup>n</sup>, then 0 is in V. If 0 is not in V, V cannot be a subspace.
### Examples
1. V = {(x,y,z) ∈ ℝ<sup>4</sup> | x-y+10w=0}. Is V a subspace of ℝ<sup>4</sup>?
   * Solution: Let X, Y be elements of V such that X = (x<sub>1</sub>+...+x<sub>4</sub>) and Y = (y<sub>1</sub>+...+y<sub>4</sub>). Check wheter λV + μY exist in ℝ<sup>4</sup> and all λμ are in R. 
     * Note: λX + μY = (λx<sub>1</sub>μy<sub>1</sub>, ..., λx<sub>4</sub>μy<sub>4</sub>) = (t<sub>1</sub>, ..., t<sub>4</sub>)
     * Need to check t<sub>1</sub>-t<sub>2</sub>+10t<sub>4</sub> = 0.
     * Note: t<sub>1</sub>-t<sub>2</sub>+10t<sub>4</sub> = λ(x<sub>1</sub>-x<sub>2</sub>+10x<sub>4</sub>) + μ(y<sub>1</sub>-y<sub>2</sub>+10y<sub>4</sub>)
     * Since as X and Y are elements of V, x<sub>1</sub>-x<sub>2</sub>+10x<sub>4</sub>=0 and y<sub>1</sub>-y<sub>2</sub>+10y<sub>4</sub> imply that t<sub>1</sub>-t<sub>2</sub>+10t<sub>4</sub> = 0 and λX + μY are elements of V. Hence, V is a subspace of ℝ<sup>4</sup>.
2. V = {y = x} contained in ℝ<sup>2</sup>. W = {y = -x} contained in ℝ<sup>2</sup>. Let Z = the union of V and W. Is Z a subspace of ℝ<sup>2</sup>?
   * Solution: No. Consider that the point (1,1) is in V and (1,-1) is in W. However, (1,1)+(1,-1)=(2,0) is not an element of V or W. Hence, (2,0) is not in the union of V and W, so condition (a) fails. Z cannot be a subspace of ℝ<sup>2</sup>.
## Range and Nullspace of a Linear Transformation
* Also known as image and kernel for general f: ℝ<sup>n</sup> -> ℝ<sup>m</sup>.
* Let T: ℝ<sup>n</sup> -> ℝ<sup>m</sup> be a linear transformation. R(T(x)) = {T(x) | x ∈ ℝ<sup>n</sup>} and N(T(x)) = {x ∈ ℝ<sup>n</sup> | T(x)=0}
### Fact
* R(T) is a subspace of ℝ<sup>m</sup>
* N(T) is a subspace of ℝ<sup>n</sup>
* If A is an `n x m` matrix:
  * R(X) = {Ax | x ∈ ℝ<sup>m</sup>}
  * N(A) = {x ∈ ℝ<sup>n</sup> | Ax=0}
### Remark
R(A) = all the linear combinations of v<sub>1</sub>, ..., v<sub>n</sub>, where all vectors in ℝ<sup>m</sup> are of the form  λv<sub>1</sub> + ... + λv<sub>2</sub> for any real number constant λ.
### Examples
1. f(t) = t<sup>3</sup> + at<sup>2</sup> + bt + c. The constants a, b, and c are in R. What is Im(f)?
   * Solution: Im(f) = R, because lim<sub>t→∞</sub>f(t) = +∞ and lim<sub>t→-∞</sub>f(t) = -∞.
2. Find a matrix whose kernel is the plane V = {(x,y,z) ∈ ℝ<sup>3</sup> | x + y + 3z = 0}.
   * Solution: Define the matrix `A = [1 1 3]`. If (x,y,z) is such that AX=0 (and thus x + y + 3z = 0).
3. What is the range and nullspace of the linear transformation T(x) = v+x for all x ∈ ℝ<sup>3</sup> and v = (v<sub>1</sub>, ..., v<sub>3</sub>) is a fixed nonzero vector?
   * Solution: What is N(T)? If x=(x<sub>1</sub>, ..., x<sub>3</sub>) ∈ N(T), then T(x) = 0 implies v<sub>1</sub>x<sub>1</sub>+...+v<sub>3</sub>x<sub>3</sub> = 0. Hence if x ∈ N(T) then x<sub>1</sub>, ..., x<sub>3</sub> need to satisfy v<sub>1</sub>x<sub>1</sub>+...+v<sub>3</sub>x<sub>3</sub> = 0
   * N(T) = {(x,y,z) ∈ ℝ<sup>3</sup> | v<sub>1</sub>x+v<sub>2</sub>y+v<sub>3</sub>z = 0} is the plane through (0,0,0) in ℝ<sup>3</sup>.
   * What is R(T)? Because any number can be written in the form v<sub>1</sub>x<sub>1</sub>+...+v<sub>3</sub>x<sub>3</sub> for some x<sub>1</sub>, ..., x<sub>3</sub> ∈ R, we know that R(T) = R.
4. A is a `u x p` matrix. B is `p x m`. How can you relate N(AB) and N(B)? Note that if x is an element of N(B), then Bx=0. This implies (AB)x=0. In turn, x is an element of N(AB), meaning N(B) is a subset of N(AB). Is it true that N(B) = N(AB)?
   * Solution: No. Pick a matrix B that is `p x p` that is invertible, so N(B) = {0}. Pick A=0, so N(AB) = ℝ<sup>n</sup>
## Linear Independence
v<sub>1</sub>, ..., v<sub>m</sub> are linearly independent if the only solution of c<sub>1</sub>v<sub>1</sub> + ... + c<sub>m</sub>v<sub>m</sub> = 0 if c<sub>1</sub>+...+c<sub>m</sub>=0. Or, let A be a matrix with column vectors v<sub>1</sub>,..., v<sub>m</sub>. The vectors are linearlly independent if the only solution of Ax=0 is x=0.
### Examples
1. Consider vectors v<sub>1</sub>,..., v<sub>m</sub>, v<sub>m+1</sub>. Are they linearly independent?
   * Solution: No, because for c<sub>1</sub> = ... = c<sub>m</sub> = 0 and c<sub>m</sub> ≠ 0 the folllowing is satisfied: c<sub>1</sub>v<sub>1</sub>+...+c<sub>m+1</sub>v<sub>m+1</sub>=0.
## Basis and Dimension
A set B = {v<sub>1</sub>, ..., v<sub>m</sub>} is a basis of a subspace V if B spans V and v<sub>1</sub>, ..., v<sub>m</sub> are linearly independent. The dim(V) = number of elements of a basis.
* How to find a basis for N(A)? Solve Ax = 0. Write x that satisfies Ax=0 in a general form. 
  * Note: dim(N(A)) = number of free variables.
### Remark
For a `n x n` matrix, the following are equivalent:
  1. A is invertible
  2. rank(A) = n
  3. dim(R(A)) = n (the dimension of range is simply rank)
  4. dim(N(A)) = 0
  5. R(A) = ℝ<sup>m</sup>
  6. N(A) = {0}
  7. B = {v<sub>1</sub>, ..., v<sub>n</sub>} is a basis of ℝ<sup>n</sup>
### Theorem
The rank-nullity theorem states that if A is an `m x n` matrix, then dim(R(A)) + dim(N(A)) = n.
* How to find a basis for R(A)? Find rref(A), pick the column vectors in the original matrix that have leading 1s in rref(A).
### Examples:
1. 
```
    1 3 3 4
A = 0 0 3 7
    0 0 0 0
```
Find a basis for R(A).
   * Solution: Apply Gauss-Jordan. We end up with the matrix:
     ```
     1  3  0  -3
     0  0  1  7/3
     0  0  0   0
     ```
    * Hence, the B = {v<sub>1</sub>, v<sub>3</sub>} where v<sub>i</sub> is the i<sup>th</sup> column vector of A.
    * dim(R(A)) = 2. As A is a `3 x 4` matrix, by rank-nullity theorem dim(R(A)) + dim(N(A)) = 4, implying dim(N(A))=2.
2. Let V and W be subspaces of ℝ<sup>n</sup>. Also, let the intersection of V and W be only {0}. Let B = {v<sub>1</sub>, ..., v<sub>m</sub>} be a basis of V. Let C = {w<sub>1</sub>, ..., v<sub>p</sub>} be a basis of W. Show that v<sub>1</sub>, ..., v<sub>m</sub>, w<sub>1</sub>, ..., v<sub>p</sub> are linearly independent.
   * *Remark*: dim(V) + dim(W) = m + p ⊆ n
   * Solution: Consider first v<sub>1</sub>, ..., v<sub>m</sub>, w<sub>1</sub>. The claim is that they are linearly independent. If they weren't, then there would exist c<sub>1</sub>, ..., c<sub>m</sub>, d<sub>1</sub> such that c<sub>1</sub>v<sub>1</sub>+...+c<sub>m</sub>v<sub>m</sub>+d<sub>1</sub>w<sub>1</sub> = 0.
   * If d<sub>1</sub> = 0, then not all of c<sub>1</sub>, ..., c<sub>m</sub> are 0. This is a contradiction, as v<sub>1</sub>, ..., v<sub>m</sub> are linearly independent.
   * If d<sub>1</sub> ≠ 0, then w<sub>1</sub> = (-c<sub>1</sub>/d<sub>1</sub>)v<sub>1</sub> - ... - (-c<sub>m</sub>/d<sub>m</sub>)v<sub>m</sub>. If each c = 0 and w<sub>1</sub> = 0, we have a contradiction since the w vectors are linearly independent. If not all c = 0, then w<sub>1</sub> is a linear combination of v<sub>1</sub>, ..., v<sub>m</sub>. Hence, w<sub>1</sub> is an element of V and w<sub>1</sub> ≠ 0. Therefore, w<sub>1</sub> is an element of the set that is the intersection of V and W. This is a contradiction.
5. v<sub>1</sub>, ..., v<sub>m</sub> are linearly independent. Show that if A is invertible, then Av<sub>1</sub>, ..., Av<sub>m</sub> are linearly independent.
   * Solution: We want to show that c<sub>1</sub>(Av<sub>1</sub>) + ... + c<sub>m</sub>(Av<sub>m</sub>) = 0 only when all c = 0. This is equivalent to A(c<sub>1</sub>v<sub>1</sub> + ... + c<sub>m</sub>v<sub>m</sub>) = Ax. Hence, as A is invertible, Ax=0 when x=0. 
   * c<sub>1</sub>v<sub>1</sub> + ... + c<sub>m</sub>v<sub>m</sub> = 0 implies that every c = 0 because v<sub>1</sub>, ..., v<sub>m</sub> are linearly independent.
6. Assume that A is a `5 x 5` matrix and A = BC. B is a `5 x 4` matrix. C is a `4 x 5` matrix. Show that A cannot be invertible.
   * Solution: if x ∈ R(BC), then there exists some y in ℝ<sup>5</sup> such that (BC)y = x implies B(Cy) = x. 
   * Let z ∈ ℝ<sup>4</sup>. Bz = x means x ∈ R(B). Hence, R(BC) ≤ R(B) ≤ ℝ<sup>5</sup>.
   * dim(BC) = dim(A) ≤ dim(B) ≤ 5. 
   * However, we need to show that dim(A) < 5.
   * Note: dim(R(C)) ≤ 4. By rank-nullity theorem, dim(N(C)) ≥ 1. Before, we showed that N(C) ⊆ N(BC) = N(A). Hence, dim(N(A)) ≥ dim(N(C)) ≥ 1. By the rank-nullity theorem, dim(R(A)) < 5.
## Coordinates
How to find the matrix of a linear transformation with respect to a given basis? If T is alinear transformation, [T(x)]<sub>B</sub> = A<sub>B</sub>[x]<sub>B</sub>, where B = {v<sub>1</sub>, ..., v<sub>m</sub>}. A<sub>B</sub> has column vectors [T(v<sub>1</sub>)]<sub>B</sub> through [T(v<sub>m</sub>)]<sub>B</sub>. 
### Remarks
If C, B are two different bases for V, then A<sub>B</sub> is similar to A<sub>C</sub>. There exists an invertible matrix S such that  A<sub>B</sub>S = SA<sub>C</sub>.
### Exercises
* 1(a) from practice midterm
