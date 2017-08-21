接前面凸集的概念继续往下讨论。

* 界面

一个凸集$$ C $$，其一个非空凸子集$$ C^* $$，如果 $$ \mathbf u \in C^*, \exists \mathbf {x,y} \in C, \mathbf u \in (\mathbf {x, y}) $$ 那么就可以推得 $$ \mathbf {x, y} \in C^* $$，就称 $$ C^* $$ 是 $$ C $$ 的一个界面

理解这个概念首先需要知道，$$ C^* $$ 是非空凸子集，即 $$ C^*$$是一个凸集，且$$ C^*$$中点必然也在$$C$$ 中，然后再根据定义改写一下可能更符合我们的理解思维：给定$$\forall \mathbf u \in C^*$$，对于 $$ \forall \mathbf {x,y} \in C $$，只要$$ \mathbf u \in (\mathbf {x, y})$$，那么必然有 $$ \mathbf {x,y} \in C^* $$

例子

$$ C = \lbrace \mathbf x | x_1 + x_2 = 1, x_1,x_2,x_3 \ge 0 \rbrace$$的界面

这是一个三维空间的凸集，如下图

![](/assets/face.png)

当$$C^*$$是图中内部的那个小方块区域，显然对于红点$$\mathbf u, \exists \mathbf {x,y}, \mathbf u \in (\mathbf{x,y})$$，但不能推出$$\mathbf {x,y} \in C^*$$，而当$$C^*$$是左侧的那个边界线时，对于$$C$$内部点（图中黑点）$$ \mathbf u$$，只能存在类似图中的那个黄色粗线段，显然此时可以推导得到$$ \mathbf {x,y} \in C^*$$，因为如果是图中黑色的线段时，此时$$ \mathbf u = \mathbf x \Rightarrow \mathbf u \notin (\mathbf {x,y})$$，已经不符合条件了，所以，$$C$$ 有1个二维界面，即自身，有3个一维界面，为$$C$$的三个边（2个射线，1个线段），有2个零维界面（2个射线的端点）

一般地，凸集$$C $$ 的一维界面称为**边**，零维界面称为**极点**，位于同一条边上的极点是相邻的。对极点而言，并不存在满足上述界面定义中的那个$$\mathbf u$$，尽管如此，却不违背界面定义中的条件，所以极点也是一种界面

* 方向

假设$$ C \neq \varnothing $$ 是$$E^n$$中的一个凸集，给定一个$$ \mathbf d \in E^n, \mathbf d \neq \mathbf 0 $$，若对 $$ \forall \mathbf x \in C, \lambda \gt 0$$，均有 $$\mathbf x + \lambda \mathbf d \in C$$，则称$$\mathbf d$$ 是$$C$$ 的一个方向

显然$$C$$ 的方向不是任意的，即，$$\mathbf d $$ 不是任意的，而是要符合定义中的条件，注意$$ \mathbf x + \lambda \mathbf d $$ 是将点 $$\mathbf x$$移动，每个维度移动$$\lambda \mathbf d_i$$，即任意一点移动后仍在原凸集$$C$$ 中，这样的$$\mathbf d$$ 便是其方向

对于我们前面关注的非空凸集C的形式，可以写为$$C = \lbrace \mathbf x | A \mathbf x = \mathbf {b, x} \ge \mathbf 0 \rbrace \ne \varnothing$$，现在我们来研究一下其方向$$\mathbf d$$

设移动后的点为$$ \mathbf y = \mathbf x + \lambda \mathbf d$$，根据方向的定义有，$$\mathbf y \in C$$，故

$$\begin{cases}  A \mathbf  x + \lambda A \mathbf d = \mathbf b \\ \mathbf x + \lambda \mathbf d \ge \mathbf 0 \end{cases}$$

由于$$\mathbf x \ge \mathbf 0, \lambda \gt 0$$ 是任意的，所以根据上述第二个式子只能是$$ \mathbf d \ge \mathbf 0$$，再根据方向的定义，

$$\mathbf d \in E^n, \mathbf d \ne \mathbf 0$$

故$$ \mathbf d \gt \mathbf 0$$，再根据上述第一个式子以及本身$$\mathbf x$$ 就满足$$A \mathbf x = \mathbf b $$，于是，$$A \mathbf d = \mathbf b$$，

总结，$$\mathbf d$$ 是$$C$$ 的方向的充要条件是：$$\mathbf d \gt \mathbf 0, A \mathbf d = \mathbf b$$

