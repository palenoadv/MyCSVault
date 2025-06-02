# Part A: Vectors, Determinants, and Planes
## Vectors 
### Geometric view 
### Scaling, adding and subtracting vectors
### Notation and terminology

## Dot Product
If **A** = (a1,a2) and **B** = (b1,b2) then $A · B = a_1b_1 + a_2b_2$. 
The figure below shows **A**, **B** with the angle θ between them. We get $A · B = |A||B| cos θ$
### Definition of the term orthogonal and the test for orthogonality
When two vectors are perpendicular to each other we say they are orthogonal.
**A** ⊥ **B** ⇔ **A** · **B** =0.
### Dot product and length 
Both the algebraic and geometric formulas for dot product show it is intimately connected to length.In fact, they show for a vector **A** 
**A** · **A** = |**A**|^2 . 
### Uses of dot product
- Find the angle between two vectors.
- whether the vectors are orthogonal.
### Components and Projection 
If **A** is any vector and **u** is a unit vector then the component of **A** in the direction of u is **A • u**.
## Determinants
Given a square array A of numbers, we associate with it a number called the determinant of A, and written either det(A), or |A|.
Do not memorize this as a formula — learn instead the pattern which gives the terms. The 2 × 2 case is easy: the product of the elements on one diagonal (the “main diagonal”), minus the product of the elements on the other (the “antidiagonal”).
### Important facts about |A| : 
- D-1. |A| is multiplied by −1 if we interchange two rows or two columns. 
- D-2. |A| = 0 if one row or column is all zero, or if two rows or two columns are the same. 
- D-3. |A| is multiplied by c, if every element of some row or column is multiplied by c. 
- D-4. The value of |A| is unchanged if we add to one row (or column) a constant multiple of another row (resp. column).
In general, the **ij-entry**, written aij , is the number in the i-th row and j-th column. 
Its **ij-minor**, written |Aij |, is the determinant that’s left after deleting from |A| the row and column containing aij.
Its **ij-cofactor**, written here $A_{ij}$ , is given as a formula by $A_{ij} = (−1)^{i+j} |A_{ij}|$.
### Laplace expansion by cofactors
Select any row (or column) of the determinant. Multiply each entry $a_{ij}$ in that row (or column) by its cofactor $A_{ij}$ , and add the three resulting numbers; you get the value of the determinant.
### Areas and Determinants
An area of a parallelogram equals to the determinants of two sides.
# Part B: Matrices and Systems of Equations
## Cross Product
### Determinant definition for cross product
For the vectors A = (a1, a2, a3) and B = (b1, b2, b3) we define the cross product by the following formula
$$\begin{aligned}
\mathbf{A} \times \mathbf{B} & =\left|\begin{array}{ccc}
\mathbf{i} & \mathbf{j} & \mathbf{k} \\
a_{1} & a_{2} & a_{3} \\
b_{1} & b_{2} & b_{3}
\end{array}\right| \\
& =\mathbf{i}\left|\begin{array}{cc}
a_{2} & a_{3} \\
b_{2} & b_{3}
\end{array}\right|-\mathbf{j}\left|\begin{array}{cc}
a_{1} & a_{3} \\
b_{1} & b_{3}
\end{array}\right|+\mathbf{k}\left|\begin{array}{cc}
a_{1} & a_{2} \\
b_{1} & b_{2}
\end{array}\right| \\
& =\left(a_{2} b_{3}-a_{3} b_{2}\right) \mathbf{i}+\left(a_{3} b_{1}-a_{1} b_{3}\right) \mathbf{j}+\left(a_{1} b_{2}-a_{2} b_{1}\right) \mathbf{k} \\
& =\left\langle a_{2} b_{3}-a_{3} b_{2}, a_{3} b_{1}-a_{1} b_{3}, a_{1} b_{2}-a_{2} b_{1}\right\rangle .
\end{aligned}$$
### Algebraic facts: 
(these follow easily from properties of determinant). 
1. $A × A = 0$
2. Anti-commutivity: $A × B = −B × A$
3. Distributive law: $A × (B + C) = A × B + A × C$ 
4. Non-associativity: $(A × B) × C \ne A × (B × C)$ (example in a moment). 
For the unit vectors i, j, k we have 
$$i × j = k, j × k = i, k × i = j.$$
### Geometric description
Theorem: The magnitude of $A × B$ is
$|A × B| = |A||B|sin θ$, where θ is the angle between them 
= area of the parallelogram spanned by A and B.

The direction of $A × B$ is determined as follows. 
	$A × B$ is perpendicular to the plane of A and B. In the figure below there are two directions perpendicular to the plane –up and down. The choice is made by the right hand rule. This rule says to take your right hand and point your fingers in the direction of A so that they curl towards B; then your thumb points in the direction of A × B.![[Pasted image 20240410153920.png]]
We will not go through the proof of this theorem. It makes use of the Lagrange identity
$$|A × B|^2 = |A|^2|B|^2 − (A · B)^2.$$
This identity is easily show by expanding both sides using components.
**DON’T FORGET THE GEOMETRY -it will be used to solve problems.**
### Equation of a Plane
The standard terminology for the vector N is to call it a normal to the plane.

The basic data which determines a plane is a point $P_0$ in the plane and a vector $N$ orthogonal to the plane. We call $N$ a normal to the plane and we will sometimes say $N$ is normal tothe plane, instead of orthogonal.  Now, suppose we want the equation of a plane and we have a point $P_0 = (x_0, y_0, z_0)$ in the  
plane and a vector$\overrightarrow{N} = \langle a, b, c\rangle$ normal to the plane. 
Let $P = (x, y, z)$ be an arbitrary point in the plane. Then the vector$\overrightarrow{P_0P}$ is in the plane and therefore orthogonal to $N$. This means
$$
\begin{aligned}
& \mathbf{N} \cdot \overrightarrow{\mathbf{P}_{0} \mathbf{P}}=0 \\
\Leftrightarrow & \langle a, b, c\rangle \cdot\left\langle x-x_{0}, y-y_{0}, z-z_{0}\right\rangle=0 \\
\Leftrightarrow & a\left(x-x_{0}\right)+b\left(y-y_{0}\right)+c\left(z-z_{0}\right)=0
\end{aligned}
$$
We call this last equation the point-normal form for the plane.
## matrix
### matrix algebra
A rectangular array of numbers having m rows and n columns is called an m ×n matrix. The number in the i-th row and j-th column(where$1≤i≤m$, $1 ≤j ≤n$) is called the **ij-entry**, and denoted aij ; the matrix itself is denoted by A, or sometimes by($a_{ij}$). 

Two special kinds of matrices are the row-vectors: the 1 ×n matrices(a1,a2,... ,an); and the column vectors: the m ×1 matrices consisting of a column of m numbers. 
	From now on, row-vectors or column-vectors will be indicated by boldface small letters; when writing them by hand, put an arrow over the symbol. 
### Matrix operations
There are four basic operations which produce new matrices from old.
1. **Scalar multiplication**: Multiply each entry by c : $cA = (ca_{ij})$
2. **Matrix addition**: Add the corresponding entries: $A + B = (a_{ij} + b_{ij} )$; the two matrices must have the same number of rows and the same number of columns.
3. **Transposition**: The *transpose* of the $m ×n$ matrix $A$ is the $n ×m$ matrix obtained by making the rows of $A$ the columns of the new matrix. Common notations for the transpose are $A^T$ and $A′$; using the first we can write its definition as $A^T = (a_{ji})$.
4. **Matrix multiplication**: This is the most important operation. Schematically, we have$$\begin{array}{cccc}
A & \cdot & B & = & C \\
m \times n & & n \times p & & m \times p \\
& & & & \\
& & c_{i j} & = & \sum_{k=1}^{n} a_{i k} b_{k j}
\end{array}$$The essential points are:
1. For the multiplication to be defined, A must have as many columns as B has rows;
2. The $ij$-th entry of the product matrix C is the dot product of the i-th row of A with  the j-th column of B.

#### Laws and properties of matrix multiplication

1. $\begin{array}{lll} A(B+C)=A B+A C, & (A+B) C=A C+B C & \text { distributive laws } \end{array}$
2. $\begin{array}{lll} (A B) C=A(B C) ; & (c A) B=c(A B) . & \text { associative laws } \end{array}$
3. Let $I_3=\begin{pmatrix}   1 & 0  & 0\\    0 & 1  & 0\\  0 & 0 & 1\end{pmatrix}$; then $AI=A$ and $IA=A$ for any $3 \times 3$ matrix.
*I* is called the **identity matrix** of order 3.
4. In general, for two square n×n matrices $A$ and $B$, $AB\ne BA$: *matrix multiplication is not commutative*. (There are a few important exceptions, but they are very special — for example, the equality $AI = IA$ where $I$ is the identity matrix.)
5. For two square $n × n$ matrices $A$ and $B$, we have the *determinant law*:$$\begin{array}{lll} |AB| = |A||B|, & \text{also written} & \det(AB) = \det(A)\det(B) \end{array}$$
6. A useful fact is this: matrix multiplication can be used to pick out a row or column of a given matrix: you multiply by a simple row or column vector to do this.
#### Meaning of matrix multiplication
For example the matrix $A = \begin{pmatrix} 4&1 \\ 1&3 \end{pmatrix}$transforms the unit square into a parallelogram as follows.
![[Pasted image 20240414234416.png]]
#### inverse matrices
Linear algebra is essentially about solving systems of linear equations, here we will just stick to the most important case, where the system is square, i.e., there are as many variables as there are equations.In low dimensions such systems look as follows:$$\begin{array}{l}
a_{11} x_{1}+a_{12} x_{2}+a_{13} x_{3}=b_{1} \\
a_{21} x_{1}+a_{22} x_{2}+a_{23} x_{3}=b_{2} \\
a_{31} x_{1}+a_{32} x_{2}+a_{33} x_{3}=b_{3}
\end{array}$$Using matrix multiplication, we can abbreviate the system by
$$\begin{array}{lll} A\mathbf{x}=\mathbf{b},&\mathbf{x}=\begin{pmatrix} x_1\\ x_2\\x_3\end{pmatrix}，&\mathbf{b}=\begin{pmatrix} b_1\\ b_2\\b_3\end{pmatrix}\end{array}$$
where A is the square matrix of coefficients ($a_{ij}$).

Suppose we can find a square matrix M, the same size as A, such that$$MA=I \text{(the identity matrix).}$$we  can then solve the by matrix multiplication, using the successive steps,$$\begin{array}{rcl}
A\mathbf{x}&=&\mathbf{b}\\
M(A\mathbf{x})&=&M\mathbf{b}\\
\mathbf{x}&=&M\mathbf{b}\\
\end{array}$$$M$ dosn't always exist.$$\begin{array}{llll}M & \text{exists} & 
\Leftrightarrow & \left|A\right| \ne0.\end{array}$$**Definition.** Let A be an $n × n$matrix, with $|A| \ne 0$. Then the inverse of $A$ is an $n × n$
matrix, written $A^{−1}$, such that$$\begin{array}{cc}A^{-1}A=I_n,&AA^{-1}=I_n\end{array}$$Using the above notation, our previous reasoning show that$$|A|\ne0 \Rightarrow\text{the unique solution of}\ A\mathbf{x}=\mathbf{b} \ \text{is} \ \mathbf{x}=A^{-1}\mathbf{b}$$Let A be the matrix. The formulas for its inverse $A^{−1}$ and for an auxiliary matrix adj $A$  called the **adjoint** of $A$ (or in some books the **adjugate** of $A$) are(as for $3\times3$ matrix)

In the formula, $A_{ij}$ is the cofactor of the element $a_{ij}$ in the matrix, i.e., its minor with its sign changed by the checkerboard rule (see section 1 on determinants).
The steps in calculating the inverse matrix are:
1. Calculate the matrix of minors.
2. Change the signs of the entries according to the checkerboard rule.
3. Transpose the resulting matrix; this gives adj $A$.
4. Divide every entry by $|A|$.
### Homogeneous and Inhomogeneous Systems
**Definition.** The linear system $A\mathbf{x} = \mathbf{b}$ is called **homogeneous** if $\mathbf{b} = \mathbf{0}$; otherwise, it is
called **inhomogeneous**.
**Theorem 1.** Let $A$ be an $n \times n$ matrix
$$|A|\neq0 \ \Rightarrow A\mathbf{x}=\mathbf{b} \ \text{has the unique solution,}\ \mathbf{x}=A^{-1}\mathbf{b} $$
$$|A|\ne0 \ \Rightarrow A\mathbf{x}=\mathbf{b} \ \text{has only the trivial solution,}\ \mathbf{x}=\mathbf{0}$$$$A\mathbf{x}=\mathbf{b}\ \text{has a non-zero solution} \ \Rightarrow \ |A|=\mathbf{0}$$
**Theorem 2.** Let $A$ be an $n \times n$matrix.
$$|A|=0 \ \Rightarrow \ A \mathbf{x}=\mathbf{0} \ \text{has non-trivial (i.e., non-zero) solutions.}$$$$ |A|=0 \Rightarrow A \mathbf{x}=\mathbf{b} \ \text{usually has no solutions, but has solutions for some } \mathbf{b}. $$
we call the system **consistent** if it has solutions, **inconsistent** otherwise.
**Homogeneous systems:** $A\mathbf{x} = 0 \ \text{has non-trivial solutions} \Leftrightarrow |A| = 0.$
**Inhomogeneous systems:** $A\mathbf{x} = \mathbf{b}$ has the unique solution $\mathbf{x} = A^{−1}\mathbf{b}$, if $|A| \ne 0$.
If $|A| = 0$,$ then $A\mathbf{x} = \mathbf{b}$ usually has no solutions, but does have solutions for some $\mathbf{b}$.
#### Singular matrices
We say the square matrix A is **singular** if $|A| = 0$, and **nonsingular** or **invertible** if $|A| \ne 0$.
## homework
### 1H-3
**Q:** b) For what c-value(s) will $\left(\begin{array}{rr}2 & 1 \\0 & -1\end{array}\right)\left(\begin{array}{l}x \\y\end{array}\right)=c\left(\begin{array}{l}x \\y\end{array}\right)$have a non-trivial solution?(Write it as a system of homogeneous equations.)
**A:** b)  $\left\{\begin{matrix}   (2 −c)x + y = 0 \\ (−1 −c)y = 0 \end{matrix}\right.$ has a nontrivial solution if $\begin{vmatrix}  2-c & 1 \\  0 & -1-c\end{vmatrix}$ ,i.e.,if $(2 −c)(−1 −c) = 0,$ or $c = 2$, $c = −1$.
# Part C: Parametric Equations for Curves
There are four variables to consider, the position of the point$(x, y, z)$ and an independent variable $t$, which we can think of as time.
Since the position of the point depends on t we write
$$x = x(t),\ y = y(t),\ z = z(t)$$
to indicate that $x, y$ and $z$ are functions of $t$. We call $t$ the parameter and the equations for $x, y$ and $z$ are called ***parametric equations***.
## Parametric equations of lines
The basic data we need in order to specify a line are a point on the line and a vector parallel to the line. That is, we need a point and a direction.
**Exmple:**
If P = (x, y, z) is on the line then the vector
$$\overrightarrow{\mathbf{P}_{0} \mathbf{P}}=\langle x-1, y-2, z-3\rangle$$
is parallel to $\langle x-1, y-2, z-3\rangle$. That is, $\overrightarrow{\mathbf{P}_{0} \mathbf{P}}$ is a scalar multiple of $\langle 1, 3, 5\rangle$.We call the scale $t$ and write:
$$\begin{array}{rc} 
& \langle x, y, z\rangle=\langle x-1, y-2, z-3\rangle=t\langle 1,3,5\rangle \\
\Leftrightarrow & x-1=t, y-2=3 t, \quad z-3=5 t \\
\Leftrightarrow & x=1+t, y=2+3 t, \quad z=3+5 t .
\end{array}$$
## Parametric Curves
### General parameter equations
We can use a parameter to describe this motion. Quite often we will use $t$ as the parameter and think of it as time. Since the position of the point depends on $t$ we write$$x = x(t), \ y = y(t), \ z = z(t)$$to indicate that $x$, $y$ and $z$ are functions of t. We call $t$ the parameter and the equations for $x$, $y$ and $z$ are called ***parametric equations***.
## Position vector
In order to use vector techniques we define the ***position vector***$$r(t) = x(t)\mathbf{i} + y(t)\mathbf{j} + z(t)\mathbf{k} = \langle x(t),y(t),z(t)\rangle.$$This is just the vector from the origin to the moving point.
## Velocity and acceleration
### Velocity
$$\text{average velocity} =\frac{\Delta\mathbf{r}}{\Delta t}{\mathrm{d}t^2}=\frac{\Delta x}{\Delta t}\mathbf{i}+\frac{\Delta y}{\Delta t}\mathbf{j}$$
Now, as we usually do in calculus, we let $\Delta t\rightarrow0.$ The average velocity becomes the (instan­-taneous) velocity and the ratios in the formula above become derivatives. For completeness we write the velocity vector in a number of different forms
$$\text{velocity} = \frac{\mathrm{d}\mathbf{r}}{\mathrm{d}t}=\frac{\mathrm{d}x}{\mathrm{d}t}\mathbf{i}+\frac{\mathrm{d}y}{\mathrm{d}t}\mathbf{j}=x'\mathbf{i}+y'\mathbf{j}=\langle x',y'\rangle$$
If we are thinking geometrically or want to be precise, we will call the derivative by its geometric name: the ***tangent vector***.
### Acceleration
There is no reason to stop taking derivatives after one. Since acceleration is change in velocity per unit time, we get
$$\text{acceleration }=\mathbf{a}(t)=\frac{d\mathbf{v}}{dt}=\frac{d^2\mathbf{r}}{dt^2}=x^{\prime\prime}(t)\mathbf{i}+y^{\prime\prime}(t)\mathbf{j}=\left\langle x^{\prime\prime},y^{\prime\prime}\right\rangle $$
### Unit tangent vector  
As its name implies, the unit tangent vector is a unit vector in the same direction as the tangent vector. We usually denote it $\mathbf{T}$. We compute it by dividing the tangent vector by its length. Here are several ways of writing this.
$$\mathbf{T}=\frac{\mathbf{v}}{|\mathbf{v}|}=\frac{d\mathbf{r}/dt}{ds/dt}=\frac{\mathbf{v}}{ds/dt}.$$
Multiply $\mathbf{T}$ by $ds/dt$ gives the formula
$$\mathbf{v}=\frac{ds}{dt}\mathbf{T},$$
which expresses velocity as a magnitute, $ds/dt$ and a dirrection $\mathbf{T}$ 