# Midterm 2 (Feb 16, 2018)
## Subspaces
Given a subset V of R<sup>n</sup>, how do we check if V is a subspace?
* To show it is a subspace, verify:
  1. For all x and y, x+y exists in V
  2. For all x, x exists in V. Also, for any constant λ, λx exists in V.
  * Suggestion: pick two random x and y in V and show that λx + μy exist in V.
* To show it is not a subspace, it is enough to demonstrate that for either one of the two above conditions fail.
### Remark
If V is a subspace of R<sup>n</sup>, then 0 is in V. If 0 is not in V, V cannot be a subspace.
### Examples
1. V = {(x,y,z) ∈ R<sup>4</sup> | x-y+10w=0}. Is V a subspace of R<sup>4</sup>?
   * Solution: Let X, Y be elements of V such that X = (x<sub>1</sub>+...+x<sub>4</sub>) and Y = (y<sub>1</sub>+...+y<sub>4</sub>). Check wheter λV + μY exist in R<sup>4</sup> and all λμ are in R. 
     * Note: λX + μY = (λx<sub>1</sub>μy<sub>1</sub>, ..., λx<sub>4</sub>μy<sub>4</sub>) = (t<sub>1</sub>, ..., t<sub>4</sub>)
     * Need to check t<sub>1</sub>-t<sub>2</sub>+10t<sub>4</sub> = 0.
     * Note: t<sub>1</sub>-t<sub>2</sub>+10t<sub>4</sub> = λ(x<sub>1</sub>-x<sub>2</sub>+10x<sub>4</sub>) + μ(y<sub>1</sub>-y<sub>2</sub>+10y<sub>4</sub>)
     * Since as X and Y are elements of V, x<sub>1</sub>-x<sub>2</sub>+10x<sub>4</sub>=0 and y<sub>1</sub>-y<sub>2</sub>+10y<sub>4</sub> imply that t<sub>1</sub>-t<sub>2</sub>+10t<sub>4</sub> = 0 and λX + μY are elements of V. Hence, V is a subspace of R<sup>4</sup>.
2. V = {y = x} contained in R<sup>2</sup>. W = {y = -x} contained in R<sup>2</sup>. Let Z = the union of V and W. Is Z a subspace of R<sup>2</sup>?
   * Solution: No. Consider that the point (1,1) is in V and (1,-1) is in W. However, (1,1)+(1,-1)=(2,0) is not an element of V or W. Hence, (2,0) is not in the union of V and W, so condition (a) fails. Z cannot be a subspace of R<sup>2</sup>.
## Range and Nullspace of a Linear Transformation
* Also known as image and kernel for general f: R<sup>n</sup> -> R<sup>m</sup>.
* Let T: R<sup>n</sup> -> R<sup>m</sup> be a linear transformation. R(T(x)) = {T(x) | x ∈ R<sup>n</sup>} and N(T(x)) = {x ∈ R<sup>n</sup> | T(x)=0}
### Fact
* R(T) is a subspace of R<sup>m</sup>
* N(T) is a subspace of R<sup>n</sup>
* If A is an `n x m` matrix:
  * R(X) = {Ax | x ∈ R<sup>m</sup>}
  * N(A) = {x ∈ R<sup>n</sup> | Ax=0}
### Remark
R(A) = all the linear combinations of v<sub>1</sub>, ..., v<sub>n</sub>, where all vectors in R<sup>m</sup> are of the form  λv<sub>1</sub> + ... + λv<sub>2</sub> for any real number constant λ.
### Examples
1. f(t) = t<sup>3</sup> + at<sup>2</sup> + bt + c. The constants a, b, and c are in R. What is Im(f)?
   * Solution: Im(f) = R, because lim<sub>t→∞</sub>f(t) = +∞ and lim<sub>t→-∞</sub>f(t) = -∞.
2. Find a matrix whose kernel is the plane V = {(x,y,z) ∈ R<sup>3</sup> | x + y + 3z = 0}.
   * Solution: Define the matrix `A = [1 1 3]`. If (x,y,z) is such that AX=0 (and thus x + y + 3z = 0).
3. What is the range and nullspace of the linear transformation T(x) = v+x for all x ∈ R<sup>3</sup> and v = (v<sub>1</sub>, ..., v<sub>3</sub>) is a fixed nonzero vector?
   * Solution: What is N(T)? If x=(x<sub>1</sub>, ..., x<sub>3</sub>) ∈ N(T), then T(x) = 0 implies v<sub>1</sub>x<sub>1</sub>+...+v<sub>3</sub>x<sub>3</sub> = 0. Hence if x ∈ N(T) then x<sub>1</sub>, ..., x<sub>3</sub> need to satisfy v<sub>1</sub>x<sub>1</sub>+...+v<sub>3</sub>x<sub>3</sub> = 0
   * N(T) = {(x,y,z) ∈ R<sup>3</sup> | v<sub>1</sub>x+v<sub>2</sub>y+v<sub>3</sub>z = 0} is the plane through (0,0,0) in R<sup>3</sup>.
   * What is R(T)? Because any number can be written in the form v<sub>1</sub>x<sub>1</sub>+...+v<sub>3</sub>x<sub>3</sub> for some x<sub>1</sub>, ..., x<sub>3</sub> ∈ R, we know that R(T) = R.
4. A is a `u x p` matrix. B is `p x m`. How can you relate N(AB) and N(B)? Note that if x is an element of N(B), then Bx=0. This implies (AB)x=0. In turn, x is an element of N(AB), meaning N(B) is a subset of N(AB). Is it true that N(B) = N(AB)?
   * Solution: No. Pick a matrix B that is `p x p` that is invertible, so N(B) = {0}.
