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
     * But as X and Y are elements of V, x<sub>1</sub>-x<sub>2</sub>+10x<sub>4</sub>=0 and y<sub>1</sub>-y<sub>2</sub>+10y<sub>4</sub> imply that t<sub>1</sub>-t<sub>2</sub>+10t<sub>4</sub> = 0 and λX + μY are elements of V
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
### Examples
1. f(t) = t<sup>3</sup> + at<sup>2</sup> + bt + c. The constants a, b, and c are in R. What is Im(f)?
