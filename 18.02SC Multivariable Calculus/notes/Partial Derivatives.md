# PartA: Functions of Two Variables, Tangent Approximation and Optimization
## Functions of two variables
### Dependent and independent variables
In $z = f (x, y)$ we say $x$, $y$ are independent variables and $z$ is a dependent variable.

### Graph
For $z = f (x, y)$ we have two independent and one dependent variable, so we need 3 dimen­sions to graph the function. The technique is the same as before.
*Level curves* and *contour plots* are another way of visualizing functions of two variables. If you have seen a topographic map then you have seen a contour plot.
![[Pasted image 20240514153723.png]]

## Partial Derivatives
Fix a value $y = y_{0}$ and just let $x$ vary. You get a function of one variable, $w = f(x, y_0)$, the ***partial function*** for $y = y_{0}$.
Its graph is a curve in the vertical plane $y = y_{0}$, whose slope at the  
point $P$ where $x = x_{0}$ is given by the derivative
$$\left.\frac{d}{dx} f(x,y_0)\right|_{x_0} ,\quad\text{or}\quad\left.\frac{\partial f}{\partial x}\right|_{(x_0,y_0)}.$$

## The Tangent Approximation
### Tangent plane
For a function of one variable, $w = f(x)$, the tangent line to its graph  at a point $(x_{0}, w_{0})$ is the line passing through $(x_{0}, w_{0})$ and having slope $(\frac{dw}{dx})_{0}$  .
For a function of two variables, $w = f(x, y)$, the natural analogue is the *tangent plane* to the graph, at a point $(x_{0}, y_{0}, w_{0})$.

The equation for of the tangent plane to $w = f(x, y)$ at $(x_{0}, y_{0})$ is
$$w-w_0 = \left(\frac{\partial w}{\partial x}\right)_0(x-x_0)+\left(\frac{\partial w}{\partial y}\right)_0(y-y_0)$$

### The approximation formula
The intuitive idea is that if we stay near $(x_{0}, y_{0}, w_{0})$, the graph of the tangent plane will be a good approximation to the graph of the function $w = f(x, y)$. Therefore if the point $(x, y)$ is close to $(x_{0}, y_{0})$,
$$\begin{gather}f(x,y)\quad&\approx\quad&w_0 + \left(\frac{\partial w}{\partial x}\right)_0(x-x_0)+\left(\frac{\partial w}{\partial y}\right)_0(y-y_0)\\\text{height of graph}\quad&\approx\quad&\text{height of tangent plane}\end{gather}$$
The function on the right side whose graph is the tangent plane is often called the *linearization* of $f(x, y)$ at $(x_{0}, y_{0})$: it is the linear function which gives the best approxima­tion to $f(x, y)$ for values of $(x, y)$ close to $(x_{0}, y_{0})$.

An equivalent form of the approximation is obtained by using $\Delta$ notation; if we put
$$\Delta x = x-x_0,\quad\Delta y = y-y_0,\quad\Delta w = w-w_0,$$
then becomes
$$\Delta w \approx \left(\frac{\partial w}{\partial x}\right)_0\Delta x+\left(\frac{\partial w}{\partial y}\right)_0\Delta y,\quad\mathrm{if}\quad\Delta x\approx0, \Delta y\approx0 .$$
This formula gives the approximate change in w when we make a small change in $x$ and $y$.

### Sensitivity Principle 
The numerical value of $w = f(x, y, . . . )$, calculated at some point $(x_{0}, y_{0}, . . . )$, will be most sensitive to small changes in that variable for which the corresponding partial derivative $w_x, w_{y} , . . .$ has the largest absolute value at the point.

### Critique of the approximation formula.
Intuitively, we should expect that this will be a good approximation if the graph of $f(x, y)$ is a “smooth” surface at $(x_{0}, y_{0})$ — it doesn’t have any sharp points, folds, or look peculiar. Here is the mathematical hypothesis which guarantees this.
**Smoothness hypothesis.** We say $f(x, y)$ is smooth at $(x0, y0)$ if $f_{x}$ and $f_{y}$ are continuous in some rectangle centered at $(x0, y0)$.
If this holds, the approximation formula will be valid.

### A non-geometrical argument for the approximation formula
It uses the one-variable approximation formula for a differentiable function $w = f(u)$ :
$$\Delta w\approx f'(u_0)\Delta u,\quad\text{ if }\Delta u\approx0 .$$
We are trying to calculate the change in w as we go from $P$ to $R$ in the  
picture, where $P = (x_{0}, y_{0})$, $R = (x_{0} + \Delta x, y_{0} + \Delta y)$. This change can be thought of as taking place in two steps:$\Delta w~=~\Delta w_1~+~\Delta w_2,$
the first being the change in $w$ as you move from $x$ to $x+\Delta x$, the second the change as you move from $y$ to $y+\Delta y$. Using the one-variable approximation formula
$$\begin{aligned}
&\Delta w_{1} \approx \frac{d}{dx} f(x,y_0)\bigg|_{x_0}\cdot\Delta x = f_x(x_0,y_0) \Delta x; \\
&\Delta w_{2} \approx \left.\frac{d}{dy} f(x_0+\Delta x,y)\right|_{y_0} \cdot\Delta y = f_y(x_0+\Delta x,y_0) \Delta y \\
&\approx f_y(x_0,y_0) \Delta y,
\end{aligned}$$

## Critical Points
Just as in single variable calculus we will look for maxima and minima (collectively called *extrema*) at points $(x_{0}, y_{0})$ where the first derivatives are 0. Accordingly we define a critical point as any point $(x_{0}, y_{0})$ where
$$\frac{\partial f}{\partial x}(x_0,y_0)=0\text{ and }\frac{\partial f}{\partial y}(x_0,y_0)=0.$$
Often we will abbreviate this as $f_{x} = 0$ and $f_{y} = 0$.
Since horizontal planes are of the form $z = \text{constant}$. and the equation of the tangent plane at $(x_0, y_0, z_0)$ is
$$z=z_0+f_x(x_0,y_0)(x-x_0)+f_y(x_0,y_0)(y-y_0)$$
we see it is horizontal when
$$f_x(x_0,y_0)=0\text{ and }f_y(x_0,y_0)=0.$$
Thus, extrema occur at critical points. But, just as in single variable calculus, not all critical points are extrema.

## Least Squares Interpolation
### The least-squares line
Suppose the data points are
$$(x_1,y_1),(x_2,y_2),\ldots,(x_n,y_n)$$
and we want to find the line
$$y=ax+b$$
which “best” passes through them.Assuming our errors in measurement are distributed randomly according to the usual bell-shaped curve (the so-called “Gaussian distribution”), it can be shown that the right choice of a and b is the one for which the sum D of the squares of the deviations
$$D = \sum_{i=1}^n\bigl(y_i-(ax_i+b)\bigr)^2$$
is a minimum.In the quantities in parentheses are the ***deviations*** between the **observed values** $y_i$ and the ones $ax_i + b$ that would be predicted using the line $y=ax+b$.
This prescription for finding the line is called the **method of least squares**, and the resulting line is called the **least-squares line** or the regression line.

To calculate the values of a and b which make D a minimum, we see where the two partial derivatives are zero:
$$\begin{aligned}\frac{\partial D}{\partial a}~&=~\sum_{i=1}^n2(y_i-ax_i-b)(-x_i)~=~0\\\frac{\partial D}{\partial b}~&=~\sum_{i=1}^n2(y_i-ax_i-b)(-1)~=~0~.\end{aligned}$$
These give us a pair of linear equations for determining a and b, as we see by collecting terms and cancelling the 2’s:
$$\begin{aligned}\left(\sum x_i^2\right)a~+~\left(\sum x_i\right)b~&=~\sum x_iy_i\\\left(\sum x_i\right)a~+~n b~&=~\sum y_i~.\end{aligned}$$
The equations are usually divided by n to make them more expressive:
$$\begin{aligned}\bar{s} a + \bar{x} b &= \frac{1}{n}\sum x_iy_i\\\bar{x} a + b &= \bar{y} ,\end{aligned}$$
where$\bar{x}$ and $\bar{y}$ are the average of the $x_{i}$ and $y_{i}$, and $\bar{s}=\sum x_{i}^2/n$ is the average of the squares.
### Fitting curves by least squares
If the experimental points seem to follow a curve rather than a line, it might make more sense to try to fit a second-degree polynomial
$$y=a_0+a_1x+a_2x^2$$
to them.If there are only three points, we can do this exactly (by the Lagrange interpolation formula). For more points, however, we once again seek the values of $a_0$, $a_1$,$a_2$ for which the sum of the squares of the deviations
$$D~=~\sum_1^n\bigl(y_i-(a_0+a_1x_i+a_2x_i^2)\bigr)^2$$
is a minimum. Now there are three unknowns, $a_0$, $a_1$,$a_2$.Calculating (remember to use the chain rule!) the three partial derivatives $\partial D/\partial a_i,i=0,1,2,$and setting them equal to zero leads to a square system of three linear equations.

In general, this method of least squares applies to a trial expression of the form
$$y = a_0f_0(x)+a_1f_1(x)+\ldots+a_rf_r(x),$$
where the $f_i(x)$ are given functions (usually simple ones like $1,x,x^2,1/x,e^{kx}$, etc. Such an expression is called a **linear combination** of the functions $f_i(x).$ The method produces a square inhomogeneous system of linear equations in the unknowns $a_0,\ldots,a_r$ which can be solved by finding the inverse matrix to the system, or by elimination.

The method also applies to finding a linear function
$$z~=~a_1+a_2x+a_3y$$
to fit a set of data points
$$(x_1,y_1,z_1),\ldots,(x_n,y_n,z_n) .$$


### Second Derivative Test
**saddle point**: A local minimax point; around such a point the graph of $f(x, y)$ looks like the central part of a saddle.

The second-derivative test for maxima, minima, and saddle points has two steps.
1. Find the critical points by solving the simultaneous equations$\left\{\begin{array}{l}f_x(x,y)=0,\\f_y(x,y)=0.\end{array}\right.$
2. To test such a point to see if it is a local maximum or minimum point, we calculate the three second derivatives at the point (we use subscript 0 to denote evaluation at $(x_0, y_0)$, so for example $(f)_0 = f(x_0, y_0)$), and denote the values by $A$, $B$, and $C$: