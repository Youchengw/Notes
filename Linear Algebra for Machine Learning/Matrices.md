# Matrices
Matrices are as fundamental as vectors in machine learning. With vectors, we can represent single variables as sets of numbers or instances. With matrices, we can represent sets of variables. In this sense, a matrix is simply an ordered collection of vectors.
More formally, we represent a matrix with a italicized upper-case letter like $A$. In two dimensions, we say the matrix A has m rows and n columns.Each entry of $A$ is difined as $a_ij, i=1, \ldots ,m, and j=1, \ldots ,n$. A matrix $A\in\mathbb{R}^{m\times n}$ is defined as：
$$
\begin{bmatrix}
a_{11} & a_{12} & \cdots & a_{1n} \\
a_{21} & a_{22} & \cdots & a_{2n} \\
\vdots & \vdots & \ddots & \vdots \\
a_{m1} & a_{m2} & \cdots & a_{mn}
\end{bmatrix}, a_{ij}\in\mathbb{R}
$$

## Basic Matrix operations
### Matrix-matrix addition
We add matrices in a element-wise fashion. The sum of $A\in\mathbb{R}^{m\times n}$ and $B\in\mathbb{R}^{m\times n}$ is defined as:
$$
A+B:=\begin{bmatrix}
a_{11} + b_{11} & \cdots & a_{1n}+b_{1n} \\
a_{21} + b_{21} & \cdots & a_{2n}+b_{2n} \\
\vdots & \ddots & \vdots \\
a_{m1} + b_{m_1} & \cdots & a_{mn}+b_{mn}
\end{bmatrix}\in\mathbb{R}
$$
### Matrix-scalar multipication
Matrix-scalar multiplication is an element-wise operation. Each element of the matrix $A$ is multiplied by the scalar $\alpha$. It is defined as:
$$
a_{ij}\times\alpha, such\ that (\alpha A)_{ij}=\alpha(A)_{ij}
$$

### Matrix-vector multiplication: dot product
Matrix-vector multiplication equals to taking the dot product of each column $n$ of a $A$ with each element $x$ resulting in a vector $y$. It is defined as:
