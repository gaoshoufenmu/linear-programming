# 基本概念 {#基本概念}

* 标准形式的LP问题如下：

$$ min \quad \mathbf {cx} $$

$$ s.t. \quad A \mathbf x = \mathbf b$$

$$\quad \quad \quad \mathbf x \ge \mathbf 0$$

* 仿射集和子空间

$$ E^n $$ 表示 $$ n $$ 维欧式空间，设 $$ \mathbf x, \mathbf y $$ 是 $$ E^n $$ 中任意不同的两个点，则

$$ P = \lbrace \lambda \mathbf x + (1 - \lambda) \mathbf y | \lambda \in E^1\rbrace $$

称为通过 $$ \mathbf x, \mathbf y $$ 的直线

对于集合 $$ S \subseteq E^n, \forall \mathbf {x, y} \in S, \lambda \in E^1 $$，均有

$$ \lambda \mathbf x + (1 - \lambda) \mathbf y \in S $$

那么 $$ S $$ 称为仿射集，也就是说，$$ S $$ 中的任意两点的直线上的所有点仍在$$ S $$ 中

若$$ S $$ 中任意两点的任意线性组合仍在$$ S $$ 中，即 $$ \forall \mathbf {x,y} \in S, \alpha, \beta \in E^1 $$，均有

$$ \alpha \mathbf x + \beta \mathbf y \in S $$

那么$$ S $$ 称为$$ E^n $$ 的一个子空间。$$ S $$ 对数乘和加法封闭，且 $$ 0 \le dim(S) \le n $$ :

> $$ dim(S) = 0 \quad \mapsto \quad S $$ 表示一个点
>
> $$ dim(S) = 1 \quad \mapsto \quad S $$ 表示一条线
>
> $$ dim(S) = 2 \quad \mapsto \quad S $$ 表示一个面
>
> $$ \cdot \cdot \cdot$$
>
> $$ dim(S) = n -1 \quad \mapsto \quad S $$ 表示一个超平面
>
> $$ dim(S) = n \quad \mapsto \quad S $$ 表示 $$ E^n $$

$$ L $$ 是子空间，则集

$$ \lbrace \mathbf x \| \mathbf x \bot L \rbrace = \lbrace \mathbf x \| \mathbf x \bot \mathbf y, \forall \mathbf y \in L \rbrace $$

称为 $$ L $$ 的正交补，记作 $$ L^{\bot} $$ ，且有 $$ dim(L) + dim(L^{\bot}) = n, \quad (L^{\bot})^{\bot} = L$$

* 有以下定理：

1. $$ S $$ 是 $$ E^n $$ 的子空间 $$ \Leftrightarrow \quad S $$ 是过原点的仿射集

2. $$ \forall $$ 非空仿射集 $$ S $$ 都平行于唯一的子空间 $$ L $$

3. 给定 $$ b \in E^1, \mathbf a \in E^n, \mathbf a \ne \mathbf 0 $$ ，那么 $$ H = \lbrace \mathbf x | \mathbf {ax} = b \rbrace $$ 表示 $$ E^n $$ 中一个超平面

4. 给定实矩阵 $$ A_{mn} $$ 和 $$ \mathbf b \in E^m $$，那么 $$ K = \lbrace \mathbf x \in E^n | A \mathbf x = \mathbf b \rbrace $$ 表示 $$ E^n $$ 中的一个仿射集

如果开始不容易理解，可以令 $$ n = 2 $$，从而在二维中去想象一下，比如上面定理第三条，此时 $$ H $$ 就是一个直线。

现在我们回到$$ n $$ 维欧式空间中来，联合上面定理第三条和第四条，当右端 $$ b $$ 从一个标量升为一个 $$ m $$ 维向量 $$ \mathbf b $$ 时，对 $$ \mathbf x $$ 所表示区域的约束也增加，从而区域维度（也可理解为自由度）从 $$ n - 1 $$ 降到 $$ n - m $$

* 凸集

对 $$ C \subseteq E^n, \forall \mathbf {x, y} \in C, \lambda \in (0, 1) $$，均有

$$ \lambda \mathbf x + (1 - \lambda) \lambda \in C $$

则 $$ C $$ 称为凸集，直观的讲就是 $$ C $$ 中任意两点的连接形成线段上的任意一点仍在 $$ C $$ 中

以下为三个凸集图形，你们可以感受一下

![](/assets/import.png)![](/assets/convex.png)

下面这个则不是凸集，因为图中线段的两个端点在集合中，而线段中存在不在集合中的点

![](/assets/nonconvex.png)

$$ E^n $$ 中有限个闭半空间的交是凸集，这个结论很好理解，一个闭半空间由一个超平面切割 $$ E^n $$ 得到，根据上面定理第三条，这个闭半空间可以表示为$$ \lbrace \mathbf x | \mathbf {ax} \le b \rbrace $$，于是一组有限个闭半空间可以用同样数量（假设为$$ m $$个）的不等式表示，即 $$ \lbrace \mathbf x | A \mathbf x \le \mathbf b \rbrace $$，而不等式组等价于$$D = \lbrace \mathbf x | A \mathbf x = \mathbf {b, x} \ge \mathbf 0 \rbrace $$，于是证明这个区域是一个凸集即可：

设$$ \mathbf {x, y} \in D, \mathbf w = \lambda \mathbf x + (1 - \lambda)\mathbf y, \lambda \in (0, 1) $$，因为$$ \mathbf {x,y}, \lambda, (1 - \lambda) \ge \mathbf 0 $$，故$$ \mathbf w \ge \mathbf 0 $$，又$$ A \mathbf x = \mathbf b, A \mathbf y = \mathbf b $$，所以

$$ A \mathbf w = \lambda A \mathbf x + (1 - \lambda)A \mathbf y = \lambda \mathbf b + (1 - \lambda) \mathbf b = \mathbf b $$

于是，$$ \mathbf w \in D $$，证毕。



