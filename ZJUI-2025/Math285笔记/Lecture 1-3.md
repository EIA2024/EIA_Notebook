# Lecture 1

An ordinary differential equation (ODE) is an equation for a one-variable function f(t) and its derivatives f (t), f (t), etc.

Partial differential equations (PDE) involve multi-variable functions 
$$
f(x_1,x_2,x_3,...,x_n,)
$$
 and their partial derivatives 
$$
\frac{\partial f}{\partial x_i},\frac{\partial^2 f}{\partial x_i\partial x_j},etc.
$$

#### **Definition**:

微分方程定义：关于某函数与其各级导数与常数的方程

![image-20250218153800071](C:\Users\21207\Desktop\编程\Github\Study-ZJUI-Spring-2025\Math285\图片\image-20250218153800071.png)

微分方程的解的定义：以上方程的解，以及此函数各级导的关系

![image-20250218154000195](C:\Users\21207\Desktop\编程\Github\Study-ZJUI-Spring-2025\Math285\图片\image-20250218154000195.png)

#### Example:

![image-20250219151403548](C:\Users\21207\Desktop\编程\Github\Study-ZJUI-Spring-2025\Math285\图片\image-20250219151403548.png)

![image-20250219151440107](C:\Users\21207\Desktop\编程\Github\Study-ZJUI-Spring-2025\Math285\图片\image-20250219151440107.png)

T2/3:
$$
y(t)=ce^t \quad  and\quad y(t)=ce^{AT}
$$
T4:![image-20250219152429684](C:\Users\21207\AppData\Roaming\Typora\typora-user-images\image-20250219152429684.png)

T5:
$$
y'=2ty

$$

$$
=>y(t)=ce^{t^2}
$$

T6:
$$
y'=y^2
$$

$$
=>y(t)=\frac{1}{t_0+y(t_0)^{-1}-t}
$$

$$
=>y(t)=\frac{1}{c-t} \quad with \quad c=t_0+y(t_0)^{-1}
$$

区间在
$$
(-\infty,-c)\quad or\quad (c,\infty)
$$


![image-20250219154420944](C:\Users\21207\Desktop\编程\Github\Study-ZJUI-Spring-2025\Math285\图片\image-20250219154420944.png)

![image-20250219154732550](C:\Users\21207\Desktop\编程\Github\Study-ZJUI-Spring-2025\Math285\图片\image-20250219154732550.png)

T7:
$$
y'=\sqrt{|y|} \\ 
\Rightarrow \quad 
y(t)=
\begin{cases} 
-\frac{1}{4}(t-c_1)^2 \quad &if\quad t\leq c_1\\
0  \quad &if\quad c_1 \leq t \leq c_2 \\ 
\frac{1}{4}(t-c_2)^2 \quad &if\quad t\geq c_2 
\end{cases} 
$$
![屏幕截图 2025-02-21 155112](C:\Users\21207\Desktop\编程\Github\Study-ZJUI-Spring-2025\Math285\图片\屏幕截图 2025-02-21 155112.png)
$$

$$





# Math 285

# Math 241