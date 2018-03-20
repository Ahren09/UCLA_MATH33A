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
