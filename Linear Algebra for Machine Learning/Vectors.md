Linear algebra is the study of vectors. At the most general level, vectors are **ordered finite lists of numbers**. 
**Vectors are the most fundamental mathematical object in machine learning**

Representation: $\vec{v}$

## Types of vectors
(1) geometric vectors; (2) polynomials; (3) elements of $\mathbb{R}^n$

### Geometric vectors
Geometric vectors are oriented segments. 
### Polynomials
A polynomial is an expression like $f(x)=x^2+y+1.$ This is, an expression adding multiple "terms" (nomials). Polynomials are vectors because they meet the definition of a vector: they can be added together to get anothter polynomial, and they can be multiplied together to get another polynomial.

Function addition is valid and multiplying by a scalar is valid.
### Elements of $\mathbb{R}^n$ space
Elements of $\mathbb{R}^n$ are sets of real numbers. This type of reperest is arguably the most important for applied machine learning. It is how data is commonly represented in comuters to build machine learning models. For instance in $\mathbb{R}^3$ takes the shapeof:
$$ \vec{x}\ =\ \begin{pmatrix}
x_1 \\
x_2 \\
x_3 
\end{pmatrix} \ \in \mathbb{R}^3
$$

Indicating that it contains three dimensions. 
Addition is valid and multiplying by a scalar is valid

## Zero vector, unit vector, and sparse vector

Zero vector:
$$
\vec{0}\ =\ \begin{pmatrix}
0 \\
0 \\
\vdots \\
0
\end{pmatrix}
$$

Unit vectors:$$
\vec{x_1}\ =\ \begin{pmatrix}
1 \\
0 \\
0 \\
\vdots \\
0
\end{pmatrix},\ 
\vec{x_2}\ =\ \begin{pmatrix}
0 \\
1 \\
0 \\
\vdots \\
0 
\end{pmatrix},\ 
\cdots,\ 
\vec{x_n}\ =\ \begin{pmatrix}
0 \\
0 \\
0 \\
\vdots \\
1
\end{pmatrix}
$$
Sparse vectors, are vectors with most of their elements equal to zero. We denote the number of nonzero elements of a vector $\vec{x}$ as $nnz(x)$. The sparse possible vector is the zero vector. 

## Vector dimensions and coordinate system

Vectors dimensions map into **coordinate systems** or **perpendicular axes**. Coordinate systems have an origin at $(0,0,0)$, hencem when we define a vector:
$$
\vec{x}\ =\ \begin{pmatrix}
3 \\
2 \\
1
\end{pmatrix}\ \in \mathbb{R}^3
$$
We are saying: starting from the origin, move 3 units in the 1st perpendicular axis, 2 units in the 2nd perpendicular axis, and 1 unit in the 3rd perpendicular axis. 

## Basic vector operations
### Vector-vector addition
Vector-vector addition is an element-wise operation operation, only defined for vectors of the same size (i.e., number of elements)
$$
\vec{x}+\vec{y}=
\begin{pmatrix}
x_1 \\
\vdots \\
x_n    
\end{pmatrix}+
\begin{pmatrix}
y_1 \\
\vdots \\
y_n    
\end{pmatrix}=
\begin{pmatrix}
x_1+y_1 \\
\vdots \\
x_n+y_n    
\end{pmatrix}
$$

Fundamental properties:
1. Commutativity: $x+y=y+x$
2. Associativity: $(x+y)+z=x+(y+z)$
3. Adding the zero vector has no effect
4. Substracting a vector from itself returns the zero vector

## Vector-scalar multiplication
It is defined as:
$$
\alpha \vec{x}=
\begin{pmatrix}
\alpha x_1\\
\alpha x_2\\
\vdots \\
\alpha x_n
\end{pmatrix}
$$
Vecto-scalar multiplication satisfies a series of important properties:
1. Associativity: $(\alpha \beta)\vec{x}=\alpha(\beta\vec{x})$
2. Left-distributive property: $(\alpha+\beta)\vec{x}=\alpha\vec{x}+\beta\vec{x}$
3. Right-distributive property: $\vec{x}(\alpha+\beta)=\vec{x}\alpha+\vec{x}\beta$
4. Right-distributive property for vector addition: $\alpha(\vec{x}+\vec{y})=\alpha\vec{x}+\alpha\vec{y}$

## Linear combination of vectors
Only two operations with vectors in linear algebra are legal: **addition** and **mutiplication by numbers**. When we combine these, we get a **linear combination**.
$$
\alpha\vec{x}+\beta\vec{y}=\alpha
\begin{pmatrix}
x_1 \\
x_2
\end{pmatrix}+\beta
\begin{pmatrix}
y_1 \\
y_2
\end{pmatrix}=
\begin{pmatrix}
\alpha x_1+\alpha x_2 \\
\beta y_1+\beta y_2
\end{pmatrix}
$$
## Vector-vector multiplication: dot product
Vector-vector multiplication is commonly know as a **dot product** or **inner product**. The dot product of $x$ and $y$ is defined as:
$$
\vec{x}\cdot\vec{y}= 
\begin{pmatrix}
x_1 & x_2
\end{pmatrix}
\begin{pmatrix}
y_1 \\
y_2
\end{pmatrix}=
\begin{pmatrix}
x_1 \\
x_2
\end{pmatrix}^T
\begin{pmatrix}
y_1 \\
y_2
\end{pmatrix}=
x_1\times y_1+x_2\times y_2
$$
The **T** denotes the transpose of the vector.

## Vector space, span, and subspace
### Vector space
A vector spaces, also known as linear space, is a collection of objects that follow the rules defined for vectors in $\mathbb{R}^n$. A vector space is the set of proper vectors and all possible linear combinations of the vector set. In addition, vector addition and multiplication must follow these eight rules:
1. Commutativity: $x+y=y+x$
2. Associativity: $x+(y+z)=(x+y)+z$
3. Unique zero vector such that: $x+0=x\ \forall \ x$
4. $\forall\ x$ there is a unique vector $x$ such that $x+ - x=0$
5. Identity element of scalar multiplication: $1\times x=x$
6. Distributivity of scalar multiplication w.r.t vector addition: $x(y+z)=xz+xy$
7. $x(yz)=(xy)z$
8. $(y+z)x=yx+zx$

### Vector span
If our vectors $\vec{x}$ and $\vec{y}$ point into different directions in the 2-dimensions in the 2-dimensional space, we get that the span$(x,y)$ is equal to the **entire 2-dimensional plane**
If you combine vectors which point in the same direction, you just can span a line. **Multicollinearity** is closely related to this issue: when two variables are "colinear", they are pointing in the same direction, hence they provide redundant information, so can drop one without information loss.
With three vectors pointing into different directions, we can span the entire 3-dimensional space or a **hyper-plane**.

### Vector subspaces
A vector subspace (or linear subspace) is a vector space that lies within a larger vector space. These are also know as linear subspaces. Consider a subspaces $S$. For a vector to be a valid subspace it has to meet three conditions:
1. Contains the zero vector, $0 \in S$
2. Closure under multiplication, $\forall\alpha\in\mathbb{R}\rightarrow\alpha\times s_i \in S$
3. Closure under addition, $\forall s_i \in S\rightarrow s_1+s_2 \in S$

Intuitively, you can think in closure as being unable to "jump out" from space into another. A pair of vectors laying flat in the 2-dimensional space, can't by either addition or multiplicatin, "jump out" into the 3-dimensional space.

## Linear dependence and independence
A set of vectors is linearly dependent if at least one vector can be obtanined as a linear combination of other vectors in the set. There is more rigurous definition of linear dependence. Consider a set of vectors $x_1, \ldots, x_k$ and scalars $\beta\in\mathbb{R}$. If there is a way to get $0=\sum_{i=1}^k\beta_i x_i$ with at least one $\beta\neq 0$, we have linearly combination of the vectors in the set, with weights that are not all zero, we have a linearly dependent set.