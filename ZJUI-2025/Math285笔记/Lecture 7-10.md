```table-of-contents
title: 
style: nestedList # TOC style (nestedList|nestedOrderedList|inlineFirstLevel)
minLevel: 0 # Include headings from the specified level
maxLevel: 0 # Include headings up to the specified level
includeLinks: true # Make headings clickable
hideWhenEmpty: false # Hide TOC if no headings are found
debugInConsole: false # Print debug info in Obsidian console
```
# Separable Equations
![[Pasted image 20250312143718.png]]
可将xy分开单独积分的方程
![[Pasted image 20250312144150.png]]
>    初始点附近存在唯一的解，这一结论在微分方程的理论和应用中具有极其重要的意义。以下是一些主要的用处：
> 1. **理论上的保证**
> - **解的存在性**：它告诉我们，在给定的初始条件下，方程确实有一个解。这避免了我们在寻找解时的徒劳无功。
> - **解的唯一性**：它确保了解的唯一性，即在初始点附近只有一个解满足该初始条件。这使得我们可以确定系统的行为是唯一确定的，没有歧义。 
> 

#### The Logistic Equation
逻辑斯蒂方程是一个形如 $y′=ay−by^2$ 的常微分方程，其中 a 和 b 是正的常数。这个方程由比利时数学家 P. Verhulst 在 1837 年提出，作为人口增长的数学模型。它比指数增长模型 y′=ay 更准确，因为它增加了一个 $−by^2$ 项，用于描述当资源有限时个体之间的竞争。

逻辑斯蒂方程具有可分离变量的形式 $y′=f_1​(t)f_2​(y)$，其中 $f_1​(t)=1$ 和 $f_2​(y)=ay−by^2$，因此它是可分离的，同时也是自治的（即方程右边不显含时间变量 t）。

由于 $ay−by^2=y(a−by)$，逻辑斯蒂方程的稳态解（即方程右边为零时的解）是 $y≡0$ 和 $y≡a/b$。这些稳态解代表了系统可能的平衡状态。
**证明过程**
![[Pasted image 20250312145627.png]]
**图像**
示例：
https://www.desmos.com/calculator/mwjnc0f2ri
![[Pasted image 20250312145820.png]]
#### 上述可被描述为Asymptotic behaviour(渐进)

$d>0:$
![[Pasted image 20250312150751.png]]

# The Harvesting Equation
**The ODE $y′= ay − by^2 − h \ (a, b, h> 0)$ is called harvesting equation.
![[Pasted image 20250313131615.png]]



**转换为标准形式
![[Pasted image 20250312153246.png]]
![[Pasted image 20250312153339.png]]
#### Analysis of the Canonical Forms
![[Pasted image 20250312153627.png]]
###### 1.  $z^′= −z^2+ 1$
![[Pasted image 20250312153850.png]]
对于一阶自治方程 $z^′=f(z)$，稳态解 $z^∗$ 的稳定性可以通过 $f^′(z^∗)$ 的符号来判断：如果 $f^′(z^∗)<0$，则解是稳定的；如果 $f^′(z^∗)>0$，则解是不稳定的。
![[Pasted image 20250312153814.png]]
###### 2.  $z^′= −z^2-1$
![[Pasted image 20250312154411.png]]
$\Rightarrow z(s)=\tan (s_0+\arctan z_0-s)$
Solutions z(s) with $z(s_0)= z_0$ exist only on$(C − π/2, C+ π/2)$ and satisfy $lim_{s↑C+π/2} z(s)= −∞$.

**不存在稳态解**
![[Pasted image 20250312155052.png]]

###### 3.  $z^′= −z^2$
![[Pasted image 20250312154854.png]]
$\Rightarrow z(s)=\frac{1}{s-(s_0-\frac{1}{z_0})}$
![[Pasted image 20250312155020.png]]
![[Pasted image 20250312155029.png]]

# Exact First-Order Equations
$$
M(x,y)dx+N(x,y)dy=0
$$
![[Pasted image 20250312174016.png]]
#### 精确方程定义 exact function

一个一阶微分方程 $M(x,y)dx+N(x,y)dy=0$ 称为**精确方程**（exact equation），如果存在一个函数 $f(x,y)$ 使得： $df=M(x,y)dx+N(x,y)dy$ 即：$\frac{∂f}{∂x}​=M(x,y)$和$\frac{∂f}{∂y​}=N(x,y)$
###### 判断条件

一个微分方程 $M(x,y)dx+N(x,y)dy=0$ 是精确的，当且仅当以下条件满足： $\frac{∂M}{∂y}​=\frac{∂N}{∂x}$​

#### 积分因子 integrating Factor
###### 定义

积分因子是一个函数 $μ(x,y)$，其作用是将一个非精确的微分方程 $M(x,y)dx+N(x,y)dy=0$ 转换为精确方程。具体来说，如果存在一个函数 $μ(x,y)$ 满足以下条件：

1. $μ(x,y)\neq 0$ 在其定义域 $D^′⊆D$ 上；
2. $μ(x,y)M(x,y)x+μ(x,y)N(x,y)dy=0$ 在 $D^′$ 上是精确的；

那么 $μ(x,y)$ 就被称为 $M(x,y)dx+N(x,y)dy=0$ 的一个积分因子。
###### 引理
![[Pasted image 20250312181349.png]]
引理指出，如果方程有通解形式 $f(x,y)=C$，则一定存在积分因子。
###### 找到因子方法
本质：
![[Pasted image 20250319164042.png]]

通过解$\mu (x)$的微分方程
![[Pasted image 20250319162638.png]]
![[Pasted image 20250312182335.png]]


###### 示例分析

考虑微分方程： ydx+(x2y−x)dy=0
![[Pasted image 20250312181310.png]]
![[Pasted image 20250312181257.png]]


# Orthogonal Trajectories 正交
对于$y_1'=f(x,y)$曲线族，我们有正交曲线族：
![[Pasted image 20250312183356.png]]



