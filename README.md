This is a old repository. I had renamed it. But now I've renamed it to the original name.

And this is a testing code for markdown.

### 矩阵快速幂

$a_{i, j} = a_{i - 1, j} + a_{i, j - 1}$，可推出 $a_{i, j} = a_{0, j} + \sum\limits_{k = 1}^{i}{a_{k, j - 1}}$

再由 $233...3$ 的初值条件，考虑构造一维矩阵 $F_{n + 2} = $

$$
\begin{bmatrix}
a_{0, \ j}, \ a_{1, \ j - 1}, \ a_{2, \ j - 1}, \ \cdots, \ a_{n, \ j - 1}, \ 3
\end{bmatrix}
$$

再考虑变换矩阵 $A_{(n + 2) \times (n + 2)} = $

$$
\begin{bmatrix}
10 & 1 & 1 & \cdots & 1 & 0 \\
0 & 1 & 1 & \cdots & 1 & 0 \\
0 & 0 & 1 & \cdots & 1 & 0 \\
\vdots & \vdots & \vdots & \ddots & \vdots & \vdots \\
0 & 0 & 0 & \cdots & 1 & 0 \\
1 & 0 & 0 & \cdots & 0 & 1 \\
\end{bmatrix}
$$

就得到

$$
F \times A = 
\begin{bmatrix}
a_{0, \ j + 1}, \ a_{1, \ j}, \ a_{2, \ j}, \ \cdots, \ a_{n, \ j}, \ 3
\end{bmatrix}
$$

#### 时间复杂度 $O(\sum{(n^3\log m)})$

We can see that it works. But the final effect is not so good.
