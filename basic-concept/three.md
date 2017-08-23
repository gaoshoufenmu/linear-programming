对于凸集$$C = \lbrace \mathbf x | A \mathbf x = \mathbf b, \mathbf x \ge \mathbf 0 \rbrace$$，我们将讨论其可行解

现假设 $$rank(A) = m$$，令$$A= (B,N)$$，其中 $$B$$ 为满秩矩阵，对应地将$$\mathbf x = (x_1, x_2, ..., x_n)^T$$ 也改写为$$\mathbf x = (\mathbf x_B, \mathbf x_N)^T$$ ，于是，

$$B \mathbf x_B + N \mathbf x_N = \mathbf b $$

因为$$B$$ 是满秩矩阵，两边同乘以$$B^{-1}$$ ，

$$\mathbf x_B = B^{-1} \mathbf b - B^{-1}N \mathbf x_N$$

将$$\mathbf x_N$$ 看作自由变量，每个$$\mathbf x_N$$ 对应一个$$\mathbf x_B$$ ，从而得到一个$$\mathbf x$$

下面给出几个概念：将上述的$$B$$ 称作一个**基**（显然还可能有其他的满秩矩阵可作为基），$$B$$ 中的$$m$$ 个线性无关（必须线性无关否则就不是满秩了）的列向量称为**基向量**，$$\mathbf x$$ 中与之对应的$$m$$ 个分量称为**基变量**，其他为**非基变量**，令非基变量为0，得到的解为**基本解**，如下，然而这个解不一定是可行的，必须满足$$\mathbf x \ge \mathbf 0$$ 才是可行的，

$$\mathbf x = (\mathbf x_B, \mathbf x_N)^T = (B^{-1} \mathbf b, \mathbf 0)^T$$

上面我们讲到，$$B$$ 不一定是唯一的，只要在$$A$$ 中能选取 $$m$$ 个线性无关的列向量便能组成一个满秩矩阵，从而可作为一个基。所以对于$$\mathbf x$$ 的可行解，记作$$\overline {\mathbf x}$$，当且仅当其正分量所对应于$$A$$ 中的列向量线性无关，$$\overline {\mathbf x}$$ 就是基本可行解。这里$$\overline {\mathbf x}$$ 是可行解是一个前提条件，且根据要求$$\mathbf x \ge \mathbf 0$$ ，即 $$\mathbf x$$ 的分量非正即0，我们假设$$ \mathbf x$$ 的前

有以下几个定理，

1. $$\overline {\mathbf x}$$ 是基本可行解当且仅当其是凸集$$C$$ 的极点
2. 若一个标准形的LP问题有可行解，则其必定有基本可行解



