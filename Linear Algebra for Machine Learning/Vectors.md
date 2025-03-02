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
