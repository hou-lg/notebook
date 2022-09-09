### 线性空间与线性变换
#### **1. 线性空间**
   
##### **1.1 定义**

设 $V$ 是一个非空集合，$F$ 是一个数域。

* 在集合 $V$ 的元素之间定义了一种代数运算，叫做加法，使得 $V$ 中任意两个元素 $\alpha,\beta$ 相加，都能在 $V$中找到唯一一个元素 $\gamma$ 与之对应，记为：$\gamma=\alpha+\beta$；
* 在数域 $F$ 与集合 $V$ 的元素之间还定义了一种运算，叫做数乘，使得数域 $F$ 中任一数 $k$ 与 $V$ 中任一元素 $\alpha$ 相乘，在 $V$ 中都有唯一的一个元素 $\delta$ 与之对应，记为 $\delta=k\alpha$ 

若满足以下8条规则：
* 加法交换律：$\alpha+\beta=\beta+\alpha$
* 加法结合律：$(\alpha+\beta)+\gamma=\alpha+(\beta+\gamma)$ 
* 加法零元：$\forall \,\alpha \in V,\exists \, 0\in V,st \; 0+\alpha=\alpha$
* 加法逆元：$\forall \,\alpha \in V,\exists \, \beta \in V,st \; \alpha+\beta=0$
* 乘法单位元：$\forall \,\alpha \in V,\exists \, 1 \in F,st \; 1\alpha=\alpha$
* 乘法交换律：$\alpha \beta=\beta \alpha$
* 乘法分配律：$(k+l)\alpha=k\alpha+l\alpha$
* 乘法分配律：$k(\alpha+\beta)=k\alpha+k\beta$

则对满足以上条件的代数结构成为**线性空间**。例如：  

(1) 数域 $F$ 上的一元多项式环，按通常的多项式加法和数与多项式的乘法，构成一个数域 $F$ 上的线性空间，记为 $H_n$  
(2) 元素属于数域 $F$ 的 $n$ 维向量，按向量的加法与数量乘法，构成数域 $F$ 上的一个线性空间，记为 $F_n$  
(3) 元素属于数域 $F$ 的 $m*n$ 矩阵，按矩阵的加法和矩阵与数量乘法，构成数域 $F$ 上的一个线性空间，记为 $F^{m*n}$  
(4) 在闭区间 $[a,b]$ 上连续的实函数，按函数的加法和数与函数的数量乘法，构成一个实数域上的线性空间，记为 $C_{[a,b]}$  
(5) 数域 $F$ 按照本身的加法与乘法，即构成一个自身上的线性空间  

我们常用向量来表示线性空间中的元素
##### **1.2 维数，基，坐标**

**线性组合定义**：
设 $V$ 是数域 $F$ 上的一个线性空间，$ \alpha_{1}, \alpha_{2}, \cdots, \alpha_{r}(r \geq 1)  $是 $V$ 中一组元素，$k_{1}, k_{2}, \cdots, k_{r}$ 是数域 $\mathrm{F}$ 中的数，那么元素：$\alpha=k_{1} \alpha_{1}+k_{2} \alpha_{2}+\cdots+k_{r} \alpha_{r}$ 称为元素组 $\alpha_{1}, \alpha_{2}, \ldots, \alpha_{r}$ 的一个线性组合，也称元素 $ \alpha  $ 可以用元素组  $\alpha_{1}, \alpha_{2}, \cdots, \alpha_{r} $ 线性表出。

**线性相关定义**： 
如果 $ k_{1} \alpha_{1}+k_{2} \alpha_{2}+\cdots+k_{r} \alpha_{r}=0 \iff $ 数域 $F$ 中的 $k_{1},k_{2},\cdots,k_{r} $ 不全为 0，则称线性空间 $ V $ 中元素  $\alpha_{1}, \alpha_{2}, \cdots, \alpha_{r} $ 线性相关。

**线性无关定义**：
如果 $ k_{1} \alpha_{1}+k_{2} \alpha_{2}+\cdots+k_{r} \alpha_{r}=0 \iff  $ 数域 $F$ 中的 $k_{1}=k_{2}=\cdots=k_{r}=0 $ ，则称线性空间 $V$ 中元素 $ \alpha_{1}, \alpha_{2}, \cdots, \alpha_{r} $ 线性无关。

**维数的定义**：
如果在线性空间 $V$ 中有 $n$ 个线性无关的元素，且是没有更多数目的线性无关的元素，那么 $V$ 就称为 $n$  维的；如果在  $V$ 中可以找到任一多个线性无关的元素，那么 $V$ 就称为无限维的。

>维数描述线性空间的自由度

**基与坐标的定义**：
在  $n$  维线性空间 $ V$  中，$n$ 个线性无关的元素 $ e_{1}, e_{2}, \cdots,e_{n}$  ，称为 $V$ 的一组基。设  $\alpha $ 是  $V$ 中任一元素，于是  $e_{1}, e_{2}, \cdots, e_{n}, \alpha$  线性相关，因此  $\alpha $ 可以被基 $e_{1}, e_{2}, \cdots, e_{n} $ 线性表出：$\alpha=a_{1} \varepsilon_{1}+a_{2} \varepsilon_{2}+\cdots+a_{n} \varepsilon_{n}$ 其中系数 $ a_{1}, a_{2}, \cdots, a_{n}  $ 是被元素 $ \alpha  $ 和基 $  e_{1}, e_{2}, \cdots,e_{n} $ 下的坐标，记为 $ (a_{1}, a_{2}, \cdots, a_{n}) $

##### **1.3 基变换与坐标变换**

在 $n$ 维线性空间中，任意 $n$ 个线性无关的元素都可以取作空间的基。对不同的基，同一个向量的坐标一般不同。
设 $e_{1}, e_{2}, \cdots, e_{n}  与  e_{1}^{\prime}, e_{2}^{\prime}, \cdots, e_{n}^{\prime}  $是 $n$ 维线性空间 $V$  中两组基，它们的关系为:
$$
\left\{\begin{array}{l}
e_{1}^{\prime}=a_{11} e_{1}+a_{21} e_{2}+\cdots+a_{n 1} e_{n} \\
e_{2}^{\prime}=a_{12} e_{1}+a_{22} e_{2}+\cdots+a_{n 2} e_{n} \\
\cdots \;\cdots\\
e_{n}^{\prime}=a_{1 n} e_{1}+a_{2 n} e_{2}+\cdots+a_{n n} e_{n}
\end{array}\right.
$$
用矩阵乘法的形式写成:
$$
\left(e_{1}^{\prime}, e_{2}^{\prime}, \cdots, e_{n}^{\prime}\right)=\left(e_{1}, e_{2}, \cdots, e_{n}\right)\left(\begin{array}{cccc}
a_{11} & a_{12} & \cdots & a_{1 n} \\
a_{21} & a_{22} &\cdots & a_{2 n} \\
\vdots & \vdots & & \vdots \\
a_{n 1} & a_{n 2} & \cdots & a_{n n}
\end{array}\right)
$$
设元素  $\xi$  在这两组基下的坐标分别是 $ \left(x_{1}, x_{2}, \cdots, x_{n}\right) $ 与 $  \left(x_{1}^{\prime}, x_{2}^{\prime}, \cdots, x_{n}^{\prime}\right) $ ，即：
$$
\xi=x_{1} e_{1}+x_{2} e_{2}+\cdots+x_{n} e_{n}=x_{1}^{\prime} e_{1}^{\prime}+x_{2}^{\prime} e_{2}^{\prime}+\cdots+x_{n}^{\prime} e_{n}^{\prime}
$$
用矩阵乘法的形式写成:
$$
\xi=\left(e_{1}, e_{2}, \cdots, e_{n}\right)\left(\begin{array}{c}
x_{1} \\
x_{2} \\
\vdots \\
x_{n}
\end{array}\right)=\left(e_{1}^{\prime}, e_{2}^{\prime}, \cdots, e_{n}^{\prime}\right)\left(\begin{array}{c}
x_{1}^{\prime} \\
x_{2}^{\prime} \\
\vdots \\
x_{n}^{\prime}
\end{array}\right)
$$
带入两组基的关系式得:
$$
\left(e_{1}, e_{2}, \cdots, e_{n}\right)\left(\begin{array}{c}
x_{1} \\
x_{2} \\
\vdots \\
x_{n}
\end{array}\right)=\left(e_{1}, e_{2}, \cdots, e_{n}\right)\left(\begin{array}{cccc}
a_{11} & a_{12} & \cdots & a_{1 n} \\
a_{21} & a_{22} & \cdots& a_{2 n} \\
\vdots & \vdots & & \vdots \\
a_{n 1} & a_{n 2} & \cdots & a_{n n}
\end{array}\right)\left(\begin{array}{c}
x_{1}^{\prime} \\
x_{2}^{\prime} \\
\vdots \\
x_{n}^{\prime}
\end{array}\right)
$$
由上式，我们可以得到两组坐标之间的关系:
$$
\left(\begin{array}{c}
x_{1} \\
x_{2} \\
\vdots \\
x_{n}
\end{array}\right)=\left(\begin{array}{cccc}
a_{11} & a_{12} & \cdots & a_{1 n} \\
a_{21} & a_{22} & \cdots& a_{2 n} \\
\vdots & \vdots & & \vdots \\
a_{n 1} & a_{n 2} & \cdots & a_{n n}
\end{array}\right)\left(\begin{array}{c}
x_{1}^{\prime} \\
x_{2}^{\prime} \\
\vdots \\
x_{n}^{\prime}
\end{array}\right)
$$

>相当于对原坐标轴进行拉伸和旋转得到新坐标轴，对应的坐标也发生同样的改变

##### **1.4线性空间的同构**

**定义**：数域 $F$ 上两个线性空间 $ V$ 与 $ V^{\prime} $，若由 $ V $ 到  $V^{\prime}$  存在一个双射$\sigma $满足：
* $\sigma(\alpha+\beta)=\sigma(\alpha)+\sigma(\beta) $
* $\sigma(k \alpha)=k \sigma(\alpha) $  

其中 $ \alpha, \beta $ 是 $V$ 中任意元素，$k$ 是数域 $F$ 中任意数；
这样的映射 $\sigma$ 称为同构映射，称线性空间 $ V$ 与 $ V^{\prime} $同构。

>同构的可以建立一一对应的关系，将$V$中的运算迁移到$V^{prime}$中
    例如：解析几何利用了三维几何矢量空间与$R^3$的同构
    一般地：数域$F$上任意一个n维线性空间都与$F^n$同构

**定理**：数域 $F$ 上两个有限维线性空间同构 $\iff$ 它们有相同的维数。
#### **2. 线性变换**

##### **2.1定义**

线性映射是从一个线性空间 $V$ 到另一个线性空间 $W$ 的映射，保持加法运算和数乘运算，而线性变换是线性空间 $V$ 到其自身的线性映射（也叫线性算子）。  

**线性变换的定义**：
线性空间 $V$ 的一个变换 $T$ ，如果对于 $V$ 中任意的元素  $\alpha, \beta $ 和数域 $F$ 中任意数 $k$ ，都有:
$$
\begin{array}{l}
T(\alpha+\beta)=T(\alpha)+T(\beta) \\
T(k \alpha)=k T(\alpha)
\end{array}
$$
则$T$称为$V$上的一个线性变换。例如： 
1. 在多项式空间 $ H_{n}$  中的求导运算
$$
\begin{array}{l}
\mathscr{D}\left(x^{3}+x\right)=\left(x^{3}+x\right)^{\prime}=\left(x^{3}\right)^{\prime}+(x)^{\prime}=\mathscr{D}\left(x^{3}\right)+\mathscr{D}(x) \\
\mathscr{D}\left(k x^{3}\right)=\left(k x^{3}\right)^{\prime}=k\left(x^{3}\right)^{\prime}=k \mathscr{D}\left(x^{3}\right)
\end{array}
$$
2. 在函数空间$  C(a, b)  $上的变上限积分
$$
\begin{array}{l}
\mathscr{I}(f(x)+g(x))=\int_{a}^{x}(f(t)+g(t)) d t=\int_{t}^{x} f(t) d t+\int_{a}^{x} g(t) d t=\mathscr{I}(f(x)) 
+\mathscr{I}(g(x)) \\
\mathscr{I}(k f(x))=\int_{a}^{x} k f(t) d t=k \int_{a}^{x} f(t) d t=k \mathscr{I}(f(x))
\end{array}
$$

**特殊的线性变换**
* 恒等变换：线性空间 $V$ 中的恒等变换或称单位变换 $E$，即  $E(a)=a $
* 零变换：线性空间 $V$ 中的零变换 $0$ ，即 $ 0(a)=0 $

##### 2.2**线性变换的性质**：
* 设 $A$ 是 $V$ 上的线性变换，则$A(0)=0,A(-α)=-A(α)$
* 线性变换保持线性组合与线性关系式不变
* 线性变换把线性相关的向量组变成线性相关的向量组。
* 线性变换可能把线性无关的向量组变成线性相关的向量组

线性相关意味着几何关系上的共线/共面，线性变换不会改变这种关系
例如：解析几何中的旋转变换是一个线性变换。 

##### 2.3**线性变换的运算**：

1. $A,B\in L(V),\alpha\in V,\;(A+B)\alpha=A\alpha+B\alpha$
2. $A\in L(V),k\in F,\;(kA)\alpha=k(A\alpha)$
3. $A,B\in L(V),\alpha\in V,\;(AB)\alpha=A(B\alpha)$
4. $\forall A\in L(V),$若 $\exists B\in L(V) ,st\, AB=BA=E$, 则记$B=A^{-1}$

##### 2.4**线性变换矩阵**：
设 $V$ 是数域 $F$ 上 $n$ 维线性空间，$e_{1},e_{2}, \cdots, e_{n}  $是  $V$  的一组基。空间  $V$  中任一元素  $\xi$  可以被基  $e_{1}, e_{2}, \cdots, e_{n}$  线性表出，即有关系式：
$$
\xi=x_{1} e_{1}+x_{2} e_{2}+\cdots+x_{n} e_{n}
$$
其中系数是唯一确定的，它们就是 $ \xi$  在这组基下的坐标。根据线性变换的定义：
$$
\begin{aligned}
T \boldsymbol{\xi} &=T\left(x_{1} e_{1}+x_{2}e_{2}+\cdots+x_{n} e_{n}\right) \\
&=x_{1} T\left(e_{1}\right)+x_{2} T\left(e_{2}\right)+\cdots+x_{n} T\left(e_{n}\right)
\end{aligned}
$$
设 $T\left(e_{i}\right)=a_{i},\,(i=1,2, \cdots, n)$，则 $a_{i}$  是线性空间  $V$  中的元素，它也可由基  $e_{1}, e_{2}, \cdots, e_{n}$  线性表出:
$$
a_{i}=a_{i 1} e_{1}+a_{i 2} e_{2}+\cdots+a_{i n} e_{n}
$$
结合上式，我们可以发现基 $e_{i}$ 在线性变换 $T$ 的像 $T\left(\varepsilon_{i}\right)$ 可由自己这组基线性表出:
$$
\left\{\begin{array}{l}
T\left(e_{1}\right)=a_{11} e_{1}+a_{21} e_{2}+\cdots+a_{n 1} e_{n} \\
T\left(e_{2}\right)=a_{12} e_{1}+a_{22} e_{2}+\cdots+a_{n 2} e_{n} \\
\cdots \;\cdots \\
T\left(e_{n}\right)=a_{1 n} e_{1}+a_{2 n} e_{2}+\cdots+a_{n n} e_{n}
\end{array}\right.
$$
写成矩阵形式
$$
\begin{aligned}
T\left(e_{1}, e_{2}, \cdots, e_{n}\right) &=\left(T e_{1}, T e_{2}, \cdots, T e_{n}\right) \\
&=\left(e_{1}, e_{2}, \cdots, e_{n}\right) A
\end{aligned}
$$
其中:
$$
A=\left(\begin{array}{cccc}
a_{11} & a_{12} & \cdots & a_{1 n} \\
a_{21} & a_{22} & \cdots & a_{2 n} \\
\vdots & \vdots & & \vdots \\
a_{n 1} & a_{n 2} & \cdots & a_{n n}
\end{array}\right)
$$

**注：区别1.3与2.4中的矩阵$A$**
* 1.3中的基变换矩阵(即坐标变换矩阵)描述了同一向量空间的两组不同基的关系，由于基的线性无关性，矩阵 $A$ 满秩。
* 2.4中的线性变换矩阵描述了$\left(e_{1}, e_{2}, \cdots, e_{n}\right) $与$\left(T e_{1}, T e_{2}, \cdots, T e_{n}\right)$的关系，而$T e_{1}, T e_{2}, \cdots, T e_{n}$未必线性无关，矩阵A可能不满秩, 但 $r\left(T e_{1}, T e_{2}, \cdots, T e_{n}\right)=r(A)$.

矩阵  $A $ 称为 $A$  在基 $e_{1},e_{2}, \cdots,e_{n} $ 下的线性变换矩阵。在取定一组基之后，$n$ 维线性空间 $V$ 上的线性变换与 $F$ 上 $n \times n $ 的矩阵实现了一一对应(即双射)，具体而言：
* 线性变换的和对应于矩阵的和
* 线性变换的乘积对应于矩阵的乘积
* 线性变换的数量乘积对应于矩阵的数量乘积
* 可逆的线性变换与可逆矩阵对应，且逆变换对应于逆矩阵

这说明数域 $F$ 上 $n$ 维线性空间 $V$ 的全部线性变换组成的集合 $L(V)$ 对于线性变换的加法与数乘构成 $F$ 上一个线性空间，与数域 $F$ 上 $n \times n$方阵构成的线性空间 $ F^{n \times n}$  同构。

设线性变换 $T$ 在基 $e_{1},e_{2}, \cdots, e_{n}$ 下的矩阵是 $A$，元素 $ \xi $ 在基 $e_{1}, e_{2}, \cdots,e_{n} $ 下的坐标是 $ \left(x_{1}, x_{2}, \cdots, x_{n}\right) $ ，则 $A(\xi) $ 在基  $e_{1}, e_{2}, \cdots, e_{n} $ 下的坐标 $\left(y_{1}, y_{2}, \cdots, y_{n}\right) $ 为：
$$
\left(\begin{array}{c}
y_{1} \\
y_{2} \\
\vdots \\
y_{n}
\end{array}\right)=\boldsymbol{A} \cdot\left(\begin{array}{c}
x_{1} \\
x_{2} \\
\vdots \\
x_{n}
\end{array}\right)
$$

>线性变换的矩阵是与空间中一组基联系在一起的。
一般来说，随着基的改变，同一个线性变换就有不同的矩阵。

##### 2.5**矩阵的相似**：    
为了利用矩阵来研究线性变换，我们需要弄清楚线性变换的矩阵是如何随着基的改变而改变的。