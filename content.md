Construct the matrix equation for

$$
\begin{aligned}
x + 3y - z&=0\\
4x + 2y + 3z&=10\\
-5y + z&=4.
\end{aligned}
$$

Use NumPy to represent the matrix and the vector of this matrix equation and use `numpy.linalg.solve()` to find $x$, $y$, and $z$.

```py-cell

```

Check your result in the original equations. The solution is approximately $x=2.56$, $y=-0.72$, and $z=0.4$.

# Sample Solution

Click below to reveal the sample solution

> [!HIDDEN]
> The first step is convert the simultaneous equations into matrix form:
>
> $$
> \begin{bmatrix}
> 1 & 3 & -1 \\
> 4 & 2 & 3 \\
> 0 & -5 & 1
> \end{bmatrix}
> \begin{bmatrix}
> x \\
> y \\
> z
> \end{bmatrix}
> =
> \begin{bmatrix}
> 0 \\
> 10 \\
> 4
> \end{bmatrix}
> $$
>
> The next step is to represent the matrix as a two-dimensional NumPy array and the vector as a one-dimensional NumPy array. Finally, we pass these arrays to `numpy.linalg.solve()` to find the solution.
>
> ```py-cell
> import numpy as np
>
> A = np.array([[1, 3, -1],
>               [4, 2, 3],
>               [0, -5, 1]])
> b = np.array([0, 10, 4])
>
> solution = np.linalg.solve(A, b)
> print(f"x={solution[0]}, y={solution[1]}, z={solution[2]}")
> ```
