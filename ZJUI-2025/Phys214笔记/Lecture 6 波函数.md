# Lecture 6 The Wave function
#### Two slit experiment for electrons
电子也具有波的性质
$$
p=\frac{h}{\lambda}
=k\hbar
$$
对于一个动量p电子，先算其速度v，低速用$\cfrac{1}{2}mV^2$
#### Probability density from wave functions
**Important:**
The state of a particle is described using a wave function, which at some particular time is a function of position $\Psi(x)^2$.

结合上一个 Lecture， 我们有
$$
P(a<x<b)= \int^{b}_{a}\rho(x)dx=\int^{b}_{a}\Psi^*(x)\Psi(x)dx=\int^{b}_{a}|\Psi(x)|^2dx
$$
量子力学中的一个规则取代了经典力学中的一些概念。在经典力学中，人们通常认为粒子的状态可以通过其在特定时间的位置 x 来描述。如果在区域 [a,b] 内有一个探测器，那么当 x 在这个区域内时，探测器会被触发；如果不在，探测器则不会触发。
而在量子力学的描述中，粒子在任何给定时间触发探测器的概率是从波函数计算出来的。波函数是复数（complex number），波函数是一个复数，干涉现象正是由于波函数的复数性质产生的。（可以理解为粒子随时都有可能以波函数描述的概率出现在任意位置）

###### KIMI解释：可以理解为粒子随时都有可能以波函数描述的概率出现在任意位置
在量子力学中，粒子的状态不是由其确定的位置来描述的，而是由波函数来描述。波函数提供了粒子在空间中各个位置出现的概率分布。这意味着，对于一个给定的粒子，在任何特定的时刻，它在空间中的某个位置被发现的概率是由波函数决定的。

这种概率性是量子力学的一个核心特征，与经典力学中粒子具有确定位置和轨迹的观点截然不同。在量子力学中，粒子的位置是不确定的，直到我们对其进行测量。测量行为本身会影响粒子的状态，导致波函数“坍缩”到一个特定的位置。

因此，粒子可以被理解为以波函数描述的概率出现在空间中的任意位置，直到进行测量。这种概率性是量子世界的基本特征之一，也是量子力学与经典力学的主要区别之一。
#### Explaining the two-slit experiment using electrons
$$
\Psi(x)=A(e^{ikr_1}+e^{ikr_2})
$$
$$
\Rightarrow \rho(x)=4|A|^2cos^2(\frac{k(r_2-r_1)}{2})
$$
![[Pasted image 20250311183954.png]]
由于公式相似，对于电子我们也可以用
$$
d\sin(\theta)=m\lambda
$$
#### Normalization of wave functions
对于一个波函数：
$$
\Psi(x)=Ae^{ikx}(0<x<L)
$$
$$
\Rightarrow \int^{\infty}_{-\infty}\Psi^*(x)\Psi(x)dx=1
$$
$$
\Rightarrow A=\sqrt{\frac{1}{L}}
$$
则在a<x<b 间发现电子概率为：
$$
\int^{b}_{a}\frac{1}{L}dx=\frac{b-a}{L}
$$
看出这是一个平均分布，则该波函数在（0，L）上发现的概率一致
