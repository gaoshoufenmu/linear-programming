接前面凸集的概念继续往下讨论。

* 界面

一个凸集$$ C $$，其一个非空凸子集$$ C^* $$，如果 $$ \mathbf u \in C^*, \exists \mathbf {x,y} \in C, \mathbf u \in (\mathbf {x, y}) $$ 那么 $$ \mathbf {x, y} \in C^* $$，就称 $$ C^* $$ 是 $$ C $$ 的一个界面

理解这个概念首先需要知道，$$ C^* $$ 是非空凸子集，即 $$ C^*$$是一个凸集，且$$ C^*$$中点必然也在$$C$$ 中，然后再根据定义改写一下可能更符合我们的理解思维：给定$$\forall \mathbf u \in C^*$$，对于 $$ \forall \mathbf {x,y} \in C $$，只要$$ \mathbf u \in (\mathbf {x, y})$$，那么必然有 $$ \mathbf {x,y} \in C^* $$

例子

$$ C = \lbrace \mathbf x | x_1 + x_2 = 1, x_1,x_2,x_3 \ge 0 \rbrace$$的界面

这是一个三维空间的凸集，如下图

![](/assets/face.png)

当$$C^*$$是图中内部的那个小方块区域，显然对于红点$$\mathbf u, \exists \mathbf {x,y}, \mathbf u \in (\mathbf{x,y})$$，但不能推出$$\mathbf {x,y} \in C^*$$，而当$$C^*$$是左侧的那个边界线时，对于$$C$$内部点（图中黑点）$$ \mathbf u$$，只能存在类似图中的那个黄色粗线段，显然此时可以推导得到$$ \mathbf {x,y} \in C^*$$，因为如果是图中黑色的线段时，此时$$ \mathbf u = \mathbf x \Rightarrow \mathbf u \notin (\mathbf {x,y})$$，已经不符合条件了，所以，$$C$$ 有1个二维界面，即自身，有3个一维界面，为$$C$$的三个边（2个射线，1个线段），有2个零维界面（2个射线的端点）

