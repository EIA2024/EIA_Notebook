# Math 285 微分方程课程笔记

## 1. 一致收敛 (Uniform Convergence)

### 1.1 定义
- **点态收敛**：函数序列 $( f_n )$ 在区间 $( I )$ 上点态收敛到 $( f )$，如果对于每个 $x \in I$ ，序列  $(f_n(x$))  收敛到  $f(x)$ 。
- **一致收敛**：函数序列 \( $(f_n)$ \) 在区间 \( $I$ \) 上一致收敛到 \( $f$ \)，如果对于任意 \( $\epsilon > 0$ \)，存在一个与 \( $x$ \) 无关的 \( $N$ \)，使得对于所有 \( $n > N$ \) 和所有 \( $x \in I$ \)，都有 \( $|f(x) - f_n(x)| < \epsilon$ \)。

### 1.2 几何解释
- 一致收敛意味着除了有限个函数外，所有函数的图像都位于 \( $f$ \) 图像的 \( $2\epsilon$ \) 宽度的带状区域内。

### 1.3 重要定理
- **连续性定理**：如果 \( $(f_n)$ \) 在 \( $I$ \) 上一致收敛到 \( $f$ \)，且每个 \( $f_n$ \) 在 \( $x_0 \in I$ \) 处连续，则 \( $f$ \) 也在 \( $x_0$ \) 处连续。
- **微分定理**：如果 \( $(f_n)$ \) 在 \( $I$ \) 上点态收敛到 \( $f$ \)，且 \( $(f_n')$ \) 在 \( $I$ \) 上一致收敛到 \( $g$ \)，则 \( $f$ \) 在 \( $I$ \) 上可微，且 \( $f' = g$ \)。
- **积分定理**：如果 \( $(f_n)$ \) 在 \( $I$ \) 上一致收敛到 \( $f$ \)，且每个 \( $f_n$ \) 在 \( I \) 上可积，则 \( $f$ \) 也在 \( $I$ \) 上可积，且 \( $\int_I f = \lim_{n \to \infty} \int_I f_n$ \)。

### 1.4 Weierstrass 判别法
- 如果 \( $|f_n(x)| \leq M_n$ \) 对所有 \( $x \in D$ \) 和 \( $n \in \mathbb{N}$ \) 成立，且 \( $\sum_{n=0}^\infty M_n$ \) 收敛，则 \( $\sum_{n=0}^\infty f_n$ \) 在 \( D \) 上一致收敛。

## 2. 幂级数 (Power Series)

### 2.1 定义
- 幂级数形式为 \( $\sum_{n=0}^\infty a_n (z - a)^n$ \)，其中 \( $a_n$ \) 是系数，\( $a$ \) 是中心。

### 2.2 收敛半径
- 收敛半径 \( R \) 由 Cauchy-Hadamard 公式给出：
  \[
$$
  R = \frac{1}{L}, \quad L = \limsup \sqrt[n]{|a_n|}
$$
  \]
- 幂级数在 \( $|z - a| < R$ \) 时收敛，在 \( $|z - a| > R$ \) 时发散。

### 2.3 幂级数的性质
- **连续性**：幂级数在其收敛域内是连续的。
- **可微性**：幂级数在其收敛域内是无限次可微的，且导数可以通过逐项微分得到。

## 3. 复可微性与实可微性 (Complex vs Real Differentiability)

### 3.1 复可微性
- 复函数 \( $f(z) = u(x, y) + iv(x, y)$ \) 在 \( $z = (x, y)$ \) 处复可微，当且仅当 \( $u$ \) 和 \( $v$ \) 在 \( $(x, y)$ \) 处可微，且满足 Cauchy-Riemann 方程：
  \[
$$
  u_x = v_y, \quad u_y = -v_x
$$
  \]

## 4. 复对数 (Complex Logarithm)

### 4.1 定义
- 复对数的主分支定义为：
  \[
$$
  \ln z = \ln |z| + i \arg z
$$
  \]
  其中 \( $\arg z \in (-\pi, \pi]$ \)。

### 4.2 可微性
- \( $\ln z$ \) 在其定义域内复可微，且导数为 \( $\frac{1}{z}$ \)。

## 5. 三角级数 (Trigonometric Series)

### 5.1 三角级数的收敛性
- 三角级数 \( $\sum_{n=1}^\infty \frac{\cos(nx)}{n}$ \) 和 \( $\sum_{n=1}^\infty \frac{\sin(nx)}{n}$ \) 在 \( $(0, 2\pi)$ \) 上收敛。

### 5.2 三角级数的求值
- 例如：
  \[
$$
  \sum_{n=1}^\infty \frac{\cos(nx)}{n} = -\ln \left( 2 \sin \frac{x}{2} \right)
$$
  \]
  \[
$$
  \sum_{n=1}^\infty \frac{\sin(nx)}{n} = \frac{\pi - x}{2}
$$
  \]

## 6. 多变量情况 (Multivariable Case)

### 6.1 多变量函数的微分定理
- 如果 \( $f_k: D \to \mathbb{R}$\) 是 \( $C^1$ \) 函数，\( $(f_k)$ \) 在 \( $D$ \) 上点态收敛到 \( $f$ \)，且偏导数序列 \( $(\partial f_k / \partial x_i)$ \) 在 \( $D$ \) 上一致收敛，则 \( $f$ \) 也是 \( $C^1$ \) 函数，且 \( $\frac{\partial f}{\partial x_i} = \lim_{k \to \infty} \frac{\partial f_k}{\partial x_i}$ \)。

## 7. 含参变量的广义积分 (Uniform Convergence of Improper Parameter Integrals)

### 7.1 定义
- 含参变量的广义积分 \( $\int_0^\infty f(x, t) \, dt$ \) 在 \( D \) 上一致收敛，如果对于任意 \( $\epsilon > 0$ \)，存在 \( $R_0$ \) 使得对于所有 \( $R > R_0$ \) 和所有 \( $x \in D$ \)，都有 \( $\left| \int_R^\infty f(x, t) \, dt \right| < \epsilon$ \)。

### 7.2 连续性定理
- 如果 \( $f: I \times [a, \infty) \to \mathbb{R}$ \) 是连续函数，且 \( $\int_a^\infty f(x, t)$ \, dt \) 在 \( $I$ \) 上一致收敛，则 \( $F(x) = \int_a^\infty f(x, t) \, dt$ \) 在 \( $I$ \) 上连续。

### 7.3 微分定理
- 如果 \( $f: I \times [a, \infty) \to \mathbb{R}$ \) 是连续函数，偏导数 \( $f_x$ \) 存在且连续，且 \( $\int_a^\infty f(x, t) \, dt$ \) 在 \( $I$ \) 上点态收敛，\( $\int_a^\infty f_x(x, t) \, dt$ \) 在 \( $I$ \) 上一致收敛，则 \( $F(x) = \int_a^\infty f(x, t) \, dt$ \) 在 \( I \) 上可微，且 \( $F'(x) = \int_a^\infty f_x(x, t) \, dt$ \)。

## 8. 重要公式总结

### 8.1 幂级数的收敛半径
\[
$$
R = \frac{1}{\limsup \sqrt[n]{|a_n|}}
$$
\]

### 8.2 复对数的导数
\[
$$
\frac{d}{dz} \ln z = \frac{1}{z}
$$
\]

### 8.3 三角级数的求值
\[
$$
\sum_{n=1}^\infty \frac{\cos(nx)}{n} = -\ln \left( 2 \sin \frac{x}{2} \right)
$$
\]
\[
$$
\sum_{n=1}^\infty \frac{\sin(nx)}{n} = \frac{\pi - x}{2}
$$
\]

### 8.4 含参变量的广义积分的连续性
\[
$$
F(x) = \int_a^\infty f(x, t) \, dt \quad \text{在} \quad I \quad \text{上连续}
$$
\]

### 8.5 含参变量的广义积分的微分
\[
$$
F'(x) = \int_a^\infty f_x(x, t) \, dt
$$
\]

---

