# HW1 

裴嘉政

### Problem 1

1.  A="the second card is a heart", B="the first card is a heart"
   $$
   P(A|B)=\frac{P(AB)}{P(B)}=\frac{\frac{P_{13}^2}{P_{52}^2}}{\frac{1}{4}}=\frac{4}{17}
   $$

2. A="both cards are hearts", B="at least one card is heart"

$$
P(A|B)=\frac{P(AB)}{P(B)}=\frac{P(A)}{1-P(\bar{B})}=\frac{\frac{P_{13}^2}{P_{52}^2}}{1-\frac{P_{39}^2}{P_{52}^2}}=\frac{2}{15}
$$

### Problem 2

1. A="a card drawn from the first deck is an ace", B="a card drawn from the second deck is an ace"

$$
P(B)=P(A)P(B|A)+P(\bar{A})P(B|\bar{A})=\frac{1}{13}\times \frac{5}{53}+\frac{12}{13}\times \frac{4}{53}=\frac{1}{13}
$$

2. $$
   P(B)=P(A)P(B|A)+P(\bar{A})P(B|\bar{A})=\frac{1}{13}\times \frac{5}{55}+\frac{12}{13}\times \frac{4}{55}=\frac{53}{715}
   $$

3. A="an ace was drawn from the second deck in (ii)", B="an ace was transferred from the first deck"

$$
P(B|A)=\frac{P(AB)}{P(A)}=\frac{\frac{1}{13}\times \frac{5}{55}}{\frac{53}{715}}=\frac{5}{53}
$$

### Problem 3

1. A="the person's system was infected with the virus", B="the person is a Windows user"

$$
P(B|A)=\frac{P(AB)}{P(A)}=\frac{0.5\times 0.82}{0.5\times 0.82+0.3\times 0.65+0.2\times 0.5}=\frac{82}{141}
$$

2. A="the side shown is green", B="the other side is green"

$$
P(B|A)=\frac{P(AB)}{P(A)}=\frac{\frac{1}{3}}{\frac{1}{3}+\frac{1}{3}\times \frac{1}{2}}=\frac{2}{3}
$$

### Problem 4

​    X="expected winnings", a="how much she should pay me"
$$
EX=(-5)\times P(total=5\ or\ total=10)+a\times P(o.w.)\\
=(-5)\times (\frac{1}{9}+\frac{1}{12})+a\times (1-\frac{1}{9}-\frac{1}{12})=0
$$

$$
a=\frac{29}{35}
$$

### Problem 5

1. $$
   E(H)=E[E(H|D)]=\frac{1}{6}\sum\limits_{i=1}^6E[H|D=i]=\frac{1}{6}\sum\limits_{i=1}^6\frac{i}{2}=\frac{7}{4}
   $$

   

2. Proof:
   $$
   \begin{align*}
   cov(X+W,Y+Z)&=E[(X+W)(Y+Z)]-E[X+W]E[Y+Z]\\
   &=E[XY+XZ+WY+WZ]-(E[X]+E[W])(E[Y]+E[Z])\\
   &=E[XY]-E[X]E[Y]+E[YZ]-E[Y]E[Z]\\
   &\quad+E[WY]-E[W]E[Y]+E[WZ]-E[W]E[Z]\\
   &=cov(X,Y)+cov(Y,Z)+cov(W,Y)+cov(W,Z)
   \end{align*}
   $$
   

### Problem 6

$$
AB=
\begin{bmatrix}
1&-1&1\\
2&0&1\\
3&0&1
\end{bmatrix} 
\begin{bmatrix}
2&-2\\
1&3\\
4&-4
\end{bmatrix} =
\begin{bmatrix}
5&-9\\
8&-8\\
10&-10
\end{bmatrix}\\
A(AB)=\begin{bmatrix}
1&-1&1\\
2&0&1\\
3&0&1
\end{bmatrix} 
\begin{bmatrix}
5&-9\\
8&-8\\
10&-10
\end{bmatrix}=
\begin{bmatrix}
7&-11\\
20&-28\\
25&-37
\end{bmatrix}
$$

$$
A^2=\begin{bmatrix}
1&-1&1\\
2&0&1\\
3&0&1
\end{bmatrix}\begin{bmatrix}
1&-1&1\\
2&0&1\\
3&0&1
\end{bmatrix}=\begin{bmatrix}
2&-1&1\\
5&-2&3\\
6&-3&4
\end{bmatrix}\\
A^2B=\begin{bmatrix}
2&-1&1\\
5&-2&3\\
6&-3&4
\end{bmatrix}\begin{bmatrix}
2&-2\\
1&3\\
4&-4
\end{bmatrix}=\begin{bmatrix}7&-11\\20&-28\\25&-37\end{bmatrix}
$$

$$
\therefore A(AB)=A^2B
$$

### Problem 7

1. $$
   \frac{1}{2}\mathbf{x}^\mathrm{T}\mathbf{Ax}=\frac{1}{2}\sum\limits_{i=1}^n\sum\limits_{j=1}^nx_ix_ja_{ij}
   $$

2. Proof:
   $$
   \because \mathbf{A}是正定矩阵\\ 
   \therefore \mathbf{x}^\mathrm{T}\mathbf{Ax}>0,\forall \mathbf{x} \in \mathbb{R}^n\\
   令\quad \mathbf{x}=\left(0\cdots 1\cdots 0\right)^\mathrm{T}，其中第i个分量为1，其他都为0\\
   则\mathbf{x}^\mathrm{T}\mathbf{Ax}=a_{ii}>0,\forall1\leq i\leq n
   $$

### Problem 8

1. gradient:
   $$
   f(x)=\sum\limits_{i=1}^n\sum\limits_{j=1}^nx_ix_ja_{ij}+\sum\limits_{i=1}^nb_ix_i\\
   \frac{\partial f}{\partial x_j}=\sum\limits_{i=1}^na_{ji}x_i+\sum\limits_{i=1}^na_{ij}x_i+b_j\\
   \therefore \nabla f(x)=(\mathbf{A}+\mathbf{A}^\mathrm{T})\mathbf{x}+\mathbf{b}=2\mathbf{Ax}+\mathbf{b}\\
   \nabla^2f(x)=2\mathbf{A}
   $$

2. Hessian:
   $$
   f(x)的Hessian矩阵即为\nabla^2f(x)=2A\\
   \nabla^2f(x)的Hessian矩阵为零矩阵
   $$

3. f(A)是凸函数，理由如下：

   对于一个多元函数来说，可以通过Hessian矩阵来判断它的凹凸性。如果该函数的Hessian半正定，则函数是凸函数；如果Hessian半负定，则函数为凹函数。我们已经求出该函数的Hessian矩阵为2A，由于A是一个半正定矩阵，因此该函数是一个凸函数。

   

### Problem 9

Proof:
$$
若-f(x)是凸函数，对\forall \mathbf{x},\mathbf{y}\in \mathbb{R}^n则有\\
-f(a\mathbf{x}+(1-a)\mathbf{y})\leq a·(-f(\mathbf{x}))+(1-a)·(-f(\mathbf{y})),\forall 0\leq a\leq 1\\
不等式两边同时乘以-1，得到\\
f(a\mathbf{x}+(1-a)\mathbf{y})\geq af(\mathbf{x})+(1-a)f(\mathbf{y}),\forall 0\leq a\leq 1\\
\therefore f(x)是凹函数，反之亦然
$$

### Problem 10

Proof:
$$
\forall x,y\in dom(f),a\in[0,1],\ check\\
\begin{align*}
f(ax+(1-a)y)&=\sum\limits_{i=1}^nw_if_i(ax+(1-a)y)\\
&\leq \sum\limits_{i=1}^nw_i(af_i(x)+(1-a)f_i(y))\\
&=a\sum\limits_{i=1}^nw_if_i(x)+(1-a)\sum\limits_{i=1}^nw_if_i(y)\\
&=af(x)+(1-a)f(y)
\end{align*} \\
\therefore f是一个凸函数
$$
