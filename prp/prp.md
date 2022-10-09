#### 0.背景知识：
* 范畴(category)：有限维向量空间的集合
* 对象(object)：范畴中的元素
* 态射(mophism)：对象之间的关系
#### 1.幂零范畴与幂零态射

##### 1.1 幂零范畴与幂零态射的定义
* 幂零范畴(nilpotent category)：
  设$A$是一个有限维线性空间，$a$是$A$上的幂零算子，则$(A,a)$构成幂零范畴
* 幂零态射(nilpotent mophism)：
  若$f\in Hom_{Nil(V)}\left((X,x),(Y,y)\right)$，且有$fx=yf$，则$f$为幂零态射
  <img src=幂零态射关系图.jpg width=70%/>

##### 1.2 幂零态射的维数
用$K^p$表示$p$维的线性空间；$J_p$表示$K^p$上的幂零变换，其在标准基下对应的矩阵是$p$阶约当块。定义$dim(X,x)=dim(X)$

**【定理】**  
（1）$(X,x)\in Nil(V)$是不可分解的$\iff (X, x) \cong\left(K^{p}, J_{p}\right)$  
（2）设$p,q$为两个正整数，则$\operatorname{dim} \operatorname{Hom}\left(\left(K^{p}, J_{p}\right),\left(K^{q}, J_{q}\right)\right)=\min \{p, q\}$  
进一步：对于$\forall(X, x)=\bigoplus\limits_{i=1}^{s}\left(K^{p_{i}}, J_{p_{i}}\right),(Y, y)=\bigoplus\limits_{j=1}^{t}\left(K^{p_{j}}, J_{q_{j}}\right) \in nil(V).$  
$ \operatorname{dim} \operatorname{Hom}((X, x),(Y, y))=\sum \limits_{1 \leq i \leq s, 1 \leq j \leq t} \min \left(p_{i}, q_{j}\right)$  
**【证明】**
由定义:$$f\in Hom\left((K^p,J_p),(K^q,J_q)\right)\iff f\in Hom(K^p,K^q)\;satisfies\;fJ_p=J_qf$$
在一组特定的基下，实则是一个李雅普诺夫方程$MX-XN=0$($X$为未知矩阵)
提取$X$的列，该方程等价于$(M^{T}\otimes I-I\otimes N)x=0$，其中$M=J_q,N=J_p$，代入得：
$$
J_{q}^{T} \otimes I_{p}-I_{q} \otimes J_{p}=\left(\begin{array}{cccccc}
-J_{p} & 0 & 0 & \cdots & 0 & 0 \\
I_{p} & -J_{p} & 0 & \cdots & 0 & 0 \\
0 & I_{p} & -J_{p} & \cdots & 0 & 0 \\
\vdots & \vdots & \ddots & \ddots & \vdots & \vdots \\
0 & \cdots & 0 & I_{p} & -J_{p} & 0 \\
0 & \cdots & 0 & 0 & I_{p} & -J_{p}
\end{array}\right)_{p q \times p q}
$$
> $A \otimes B$  将$B$乘以$A$中的元素并放至相应位置

欲计算$f$维数，只需计算$J_{q}^{T} \otimes I_{p}-I_{q} \otimes J_{p}$零空间的维数
>$dimR(A^T)=dimR(A)=r$
>$dimN(A)=dimN(A^T)=n-r$

$r\left(J_{q}^{T} \otimes I_{p}-I_{q} \otimes J_{p}\right)=pq-min\left\{p,q\right\}$
故 $dim\;Hom((K^p,J_p),(k^q,J_q))=pq-(pq-min\left\{p,q\right\})=min\left\{p,q\right\}$

##### 1.3 幂零态射的基
给定$Hom((K^p,J_p),(k^q,J_q))$，则满足以下条件的$\left\{f_i\right\}$为$f$的一组基
1. $J_qf_i=f_iJ_p$（$f_i$满足$f$定义）
2. $J_qf_i=f_{i+1},\;i=1\cdots,min\left\{p,q\right\}-1$（每次迭代向上移动一行）
3. 满足条件1、2 的 $f_1$ 对应矩阵的最后一行不为 0（0不可为基）

#### 2.函子

##### 2.1 函子的定义
令$C$和$D$是两个范畴。一个从$C$到$D$的函子$F$由如下信息给出： 
1) 将每个对象 $ X \in C  $映射至一对象 $ F(X) \in D $ 上，
2) 将每个态射 $ f: X \rightarrow Y \in C $ 映射至一态射 $ F(f): F(X) \rightarrow F(Y) \in D $ 上，使之满足下列条件:
3) 对任何对象 $ X \in C $，恒有 $ F\left(\mathbf{i d}_{X}\right)=\mathbf{i d}_{F(X)} $ (单位元映到单位元)
4) 对任何态射  $f: X \rightarrow Y, g: Y \rightarrow Z $ ，恒有 $ F(g \circ f)=F(g) \circ F(f)$  （保持态射的复合）
<img src=函子关系图.png width=70%/>

##### 2.2 $\bf{tensor}$函子
给定线性空间$B$，$b\in End_v(B)$是$B$上的可逆线性算子，则$tensor$函子$Nil(v)\rightarrow Nil(v)$由以下组成：
- 函数$ob(Nil(v))\rightarrow ob(Nil(v))$
  $$(X,x)\longmapsto (X\otimes B,x\otimes b)$$
- $\forall (X,x),(Y,y)\in Nil(v)$，函数
$Hom((X,x),(Y,y))\rightarrow Hom((X\otimes B,x\otimes b),(Y\otimes B,y\otimes b))$
  $$f\longmapsto f\otimes 1_B$$

##### 2.3 $\bf{Hom}$函子
给定幂零范畴$(A,a)$，$Hom$函子$Hom((A,a),-)：Nil(v)\rightarrow Nil(v)$由以下组成：
- 函数$ob(Nil(v))\rightarrow ob(Nil(v))$
  $$(X,x)\longmapsto (Hom((A,a),(X,x)),\theta_x)$$
  其中 $\theta_x=fx,\;\forall f\in Hom((A,a),(X,x))$
- $\forall (X,x),(Y,y)\in Nil(v)$，函数
$Hom((X,x),(Y,y))\otimes Hom(Hom((A,a),(X,x)),Hom((A,a),(Y,y)))$
$$f\longmapsto Hom((A,a),f)$$