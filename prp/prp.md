#### 背景知识：
* 范畴(category)：有限维向量空间的集合
* 对象(object)：范畴中的元素
* 态射(mophism)：对象之间的关系
#### 相关概念：
* 幂零范畴(nilpotent category)：
  设$A$是一个有限维线性空间，$a$是$A$上的幂零算子，则$(A,a)$构成幂零范畴
* 幂零态射(nilpotent mophism)：
  若$f\in Hom_{Nil(V)}\left((X,x),(Y,y)\right)$，且有$fx=yf$，则$f$为幂零态射
  <img src=幂零态射关系图.jpg width=70%/>
#### 幂零态射的维数
用$K^p$表示$p$维的线性空间；$J_p$表示$K^p$上的幂零变换，其在标准基下对应的矩阵是$p$阶约当块。定义$dim(X,x)=dim(X)$

**定理**  
（1）$(X,x)\in Nil(V)$是不可分解的$\iff (X, x) \cong\left(K^{p}, J_{p}\right)$  
（2）设$p,q$为两个正整数，则$\operatorname{dim} \operatorname{Hom}\left(\left(K^{p}, J_{p}\right),\left(K^{q}, J_{q}\right)\right)=\min \{p, q\}$  
进一步：对于$\forall(X, x)=\bigoplus_{i=1}^{s}\left(K^{p_{i}}, J_{p_{i}}\right),(Y, y)=\bigoplus_{j=1}^{t}\left(K^{p_{j}}, J_{q_{j}}\right) \in nil(V).$  
$ \operatorname{dim} \operatorname{Hom}((X, x),(Y, y))=\sum \limits_{1 \leq i \leq s, 1 \leq j \leq t} \min \left(p_{i}, q_{j}\right)$  
**证明**  
由定义:$f\in Hom\left((K^p,J_p),(K^q,J_q)\right)\iff f\in Hom(K^p,K^q)\;satisfies\;fJ_p=J_qf$