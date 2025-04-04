# Linear and affine mappings
## Linear mappings
Linear mappings, also known as *linear transformations* and *linear functions*, indicate the correspondence between vectors in a vector space $V$ and the same vectors in a different vector space $W$. 

Linear mappings transform vector spaces into others. Yet, such transformations are constrained to a specific kind: linear ones. Consider a linear mapping $T$ and a pair of vectors $x$ and $y$. To be valid, a linear mapping must satisfies these rules:
$$
T(x+y)=T(x)+T(y) \\
T(\alpha x)=\alpha T(x), \forall\alpha
$$

In words:
>>The transformation of the sum of the vectors must be equal to taking the transformation of each vector individually and then adding them up.
>>The transformation of a scaled version of a vectors must be equal to taking the transformation of the vector first and then scaling the result.

The two properties above can be condenced into one, the superposition porperty:
$$
T(\alpha x+\beta y)=\alpha T(x)+\beta T(y)
$$
As a result of satisfying those properties, linear mappings preserve the structure of the original vector space. Imagine a vector space $\in \mathbb{R}^2$, like a grid on lines in a cartesian plane. Visually, preserving the structure of the vector space after a mapping means to: (1) the origin of the coordinate space remains fixed, and (2) the lines remian lines and parallel to each other.

In linear algebra, linear mappings are represented as matrices and performed by matrix multiplication. Take a vector $x$ and a matrix $A$. We say that when $A$ multiplies $x$, the matrix transform the vector into another one:
$$
T(x)=Ax
$$
The typically notation for a linear mapping is the same we used for functions. For the vector spaces $V$ and $W$, we indicate the linear mapping as $T: V \rightarrow W$.

## Examples of linear mappings
In general, *dot products are linear mappings*. This should come as no surprise since dot products are linear operations by definition. Dot products sometimes take special names, when they have a well-known effect on a linear space. Two simple cases are **negation** and **reversal**. 

### Negation matrix
A negation matrix returns the opposite sign of each element of a vector. It can be defined as:
$$
T:=A:=-1
$$
This is, the negative identity matrix. Consider a pair of vectors $x\in \mathbb{R}^3$ and $x\in \mathbb{y}^3$, and the negation matrix $-1\in \mathbb{R}^{3\times 3}$. 

### Reversal matrix
A $reversal matrix$ returns reverses the order of the elements of a vector. This is, the last become the first, the second to last becomes the second, and so on. For a matrix in $\mathbb{R}^{3\times 3}$ is defined as:
$$
\begin{pmatrix}
0&0&1\\
0&1&0\\
1&0&0
\end{pmatrix}
$$
In general, it is the identity matrix but backwards, with ones from the bottom left corner to the top right corner. 

## Examples of nonlinear mappings
As with most subjects, examing examples of what things are not can be enlightening. Let's take a couple of non-linear mappings: norms and translation.

### Norms
This may come as a surprise, but norms are not linear transformations. Not "some" norms, but all norms. This is because of the very definition of a norm, in particular, the triangle inequality and positive definite properties, colliding with the requrements of linear mappings.

First, the triangle inequality defines: $||x+y||\leq ||x||+||y||$, whereas the first requirement for linear mappings demands: $T(x+y)=T(x)+T(y)$. 

Second, the positive definite difines: $||x||\geq 0$ and $||x||=0\Leftrightarrow x=0$. Put simply, norms have to be a positive value. For instance, the norm of $||-x||=||x||$, instead of $-||x||$. But, the second property for linear mappings requires $||-\alpha x||=-\alpha ||x||$. Hence, it fails when we multiply by a negative number (i.e., it can preserve the negative sign).

### Translation
Translation is a geometric transformation that moves every vector in a vector space by the same distance in a given direction. Translation is an operation that matches our everyday life intuitions: move a cup of coffee from your left to your right, and you would have performed translation in $\mathbb{R}^3$ space. 

Contrary to what we have seen so far, the translation matrix is represented with homogeneous coordinates instead of cartesian coordinates. Put simply, the homogeneous coordinate system adds a extra 1 at the end of vectors. For instance, the vector in $\mathbb{R}^2$ cartesian coordinates:
$$
x=\begin{bmatrix}
2\\
2
\end{bmatrix}
$$
Becomes the following in $\mathbb{R}^2$ homogeneous coordinates:
$$
\begin{bmatrix}
2\\
2\\
1
\end{bmatrix}
$$
In fact, the translation matrix for the general case can't be represented with cartesian coordinates. Homogeneous coordinates are the standard in fields like computer gradphics since they allow us to better represent a series of transformations (or mappings) like scaling, translation, rotation, etc.

A translation matrix in $\mathbb{R}^3$ can be denoted as:
$$
\begin{bmatrix}
1&0&v_1\\
0&1&v_2\\
0&0&1
\end{bmatrix}
$$
Where $v_1$ and $v_2$ are the values added to each dimension for translation. For instance, consider $x=\left[2\ \ 2\right]^T\in \mathbb{R}^2$. If we want translate this 3 units in the first dimension, and 1 units in the second dimenstion, we first transfer the vevctor to homogeneous coordinates $x=\left[2\ \ 2\ \ 1\right]^T$, and then perform matrix-vector multiplication as usual:
$$
\begin{bmatrix}
1&0&3\\
0&1&1\\
0&0&1
\end{bmatrix}
\begin{bmatrix}
2\\
2\\
1
\end{bmatrix}
\begin{bmatrix}
5\\
3\\
1
\end{bmatrix}
$$
The first two vectors in the translation matrix simple reproduce the original vector (i.e., the identity), and the third vector is the one actually "moving" the vectors.

Translation is not a linear mapping simply because $T(x+y)=T(x)+T(y)$ does not hold. In the case of translation $T(x+y)=T(x+v_1)+T(y+v_1)$, which invalidates the operation as a linear mapping. This type of mapping is known as an affine mapping or transformation.

## Affine mappings
The simplest way to describe affine mappings (or transformations) is as a linear mapping+translation. Hence, an affine mapping $M$ takes the form of:
$$
M(x)=Ax+b
$$
Where $A$ is a linear mapping or transformation and $b$ is the translation vector. 

If you are familiar with the linear regression, you would notice that the above expression is its matrix form. Linear regression is usually analyzed as a linear mapping plus noise, but it can also be seen as an affine mapping. Alternative, we can say that $Ax+b$ is a linear mapping *if and only if $b=0$*.

From a geometrical perspective, affine mappings displace spaces (lines or hyperplanes) from the origin of the coordinate space. Consequently, affine mappings do not operate over vector spaces as the zero vector condition $0\in S$ does not hold anymore. Affine mappings act onto affine subspaces.

## Affine combination of vectors
We can think in affine combinations of vectors, as linear combinations with an added constraint. Let's recall the definition for a linear combination. Consider a set of vectors $x_1, \ldots ,x_{k}$ and scalars $\beta_1, \ldots , \beta_{k}\in \mathbb{R}$, then a linear combination is:
$$
\sum_{j=1}^{k}\beta_{j}x_{j}:=\beta_1x_1+ \ldots+\beta_{k}x_{k}
$$
For affine combinations, we add the condition:
$$
\sum_{j=1}^{k}\beta_{j}=1
$$
In words, we constrain the sum of the weight $\beta$ to 1. In practice, this defines a weitghted average of the vectors. This restriction has palpable effect which is easier from a geometric perspective.

## Affine span
The set of all linear combinations, defines the vector span. Similarly, the set of all affine combinations determine the affine span. Every affine of vectors $x$ and $y$ maps onto the line $z$. More generally, we say that the affine span of vectors $x_1, \ldots , x_{k}$ is:
$$
x_1, \ldots , x_{k}:=\sum_{j=1}^{k}\beta_{j}x_{j},\\
\sum_{j=1}^{k}\beta_{j}=1\in \mathbb{R}\forall\beta
$$
Again, in words: the affine span is the set of all linear combinations of the vector set, such that the weight add up to 1 and all weights are real numbers. Hence, the fundamental difference between vector spaces and affine spaces, is the former will span the entire $\mathbb{R}^n$ space (assuming independent vectors), whereas the latter will span a line.

Let's consider three cases in $\mathbb{R}^3$:(1) three linearly independent vectors;(2) two linearly independent vectors and one dependent vector; (3) three linearly dependent vectors. In case (1), the affine span is the 3-dimensional space containing those vectors. In case (2), the affine span is a 2-dimensional plane. In case (3), the affine span is a line. If all three are the same point, the affine span is a point.

## Affine space and subspace
In simple terms, addine spaces are *translations* of vector spaces, this is, vector spaces that have been offset from the origin of the coordinate system. such a notion makes sound affine spaces as a special case of vector spaces, but they are actually more general. Indeed, affine spaces provide a more general framework to do geometric manipulation, as they work independently of the choice of the coordinate system (i.e., it is not constrained to the origin). For instance, the set of solutions of the system of linear equations $Ax=y$ (i.e., linear regression), is an affine space, not a linear vector space.

Consider a vector space $V$, a vector $x_0\in V$, and a subset $U\subseteq V$. We define an affine subspace $L$ as:
$$
L=x_0+U:={x_0+u:u\in U}
$$
Further, any point, line, plane, or hyperplane in $\mathbb{R}^n$ that does not go through the origin, is an affine subspace.

## Affine mappings using the augmented matrix
Consider the matrix $A\in \mathbb{R}^{m\times n}$, and vectors $x,b,y\in \mathbb{R}^n$
We can represent the system of linear equations:
$$
Ax+b=y
$$
As a single matrix vector multiplication, by using an augmented matrix of the form:
$$
\left[
\begin{matrix}
& \textit{} &\\
& \textit{A} &\\
& \textit{} &\\
0 & \cdots & 1 
\end{matrix}
  \left|
    \,
\begin{matrix}
x_1 \\
\vdots \\
x_n \\
1
\end{matrix}
  \right.
\right] =
\begin{bmatrix}
y_1 \\
\vdots \\
y_n \\
1
\end{bmatrix}
$$
This form is know as the affine transformation matrix. We made use of this form when we exemplified *translation*, which happens to be an affine mapping.

## Special linear mappings