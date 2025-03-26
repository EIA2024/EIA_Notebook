
```table-of-contents
title: 
style: nestedList # TOC style (nestedList|nestedOrderedList|inlineFirstLevel)
minLevel: 0 # Include headings from the specified level
maxLevel: 0 # Include headings up to the specified level
includeLinks: true # Make headings clickable
hideWhenEmpty: false # Hide TOC if no headings are found
debugInConsole: false # Print debug info in Obsidian console
```
# First-Order Linear equations
**一阶齐次线性微分方程**
$$
y'=P(x)y
$$
$$
\Rightarrow y=Ce^{\int P(x)dx}
$$
**一阶非齐次线性微分方程**
$$
y'=P(x)y+Q(x)$$
$$
\Rightarrow y=Ce^{\int P(x)dx}+e^{\int P(x)dx}\int Q(x)e^{-\int P(x)dx}dx
$$
![[Pasted image 20250319173648.png]]
C为常数，由初始条件决定

**注意到：**
上式右端第一项是对应的齐次线性方程式（式2）的通解，第二项是非齐次线性方程式（式1）的一个特解。由此可知，一阶非齐次线性方程的通解等于对应的齐次线性方程的通解与非齐次线性方程的一个特解之和

特殊情况：$(y'=a(t)y+b(t))$
###### a(t)=a, b(t)=b
$$
y'=ay+b \ (y(t_0)=y_0)
$$
$$
\Rightarrow y=y(t_0)e^{a(t-t_0)}+\frac{b}{a}(e^{a(t-t_0)}-1)
$$

# Introduction to Complex Numbers
$$
e^{i\theta}=\cos\theta+i\sin\theta
$$
$$
z=r(\cos\theta+i\sin\theta)=re^{i\theta}
$$
![[Pasted image 20250311160952.png]]
**复数相乘**
$$
z=re^{i\theta}
$$
$$
w=se^{i\phi}
$$
$$
zw=rse^{i(\theta + \phi)}
$$![[Pasted image 20250311161302.png]]
