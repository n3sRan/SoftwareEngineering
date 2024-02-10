[TOC]

# NJU 微积分笔记 (一层次)

## 食用指南

- 期末微积分复习所写, 使用软件: Typora, 支持LaTeX公式内联, 故需要使用支持该功能的软件才能正常查看以及编辑这份笔记, 否则请下载并查看html版本.
- 内容有所详略, 不能面面俱到, 请见谅

## 第1章 极限与连续性

### 1.2 极限

#### 数列极限

- $\varepsilon-N$语言
- $G-N$语言

#### 函数极限

- $\varepsilon-\delta$语言
- $\varepsilon-k$语言
- $G-\delta$语言
- 有界性, 唯一性 (反证法), 保号性

- 证明数列发散: 构造两个取不同极限的子数列
- 证明函数极限不存在: 构造取不同极限的子数列

#### 极限的存在准则

- 两个基本极限
- 夹逼准则
- 单调有界准则
- 柯西准则

#### 无穷小量阶的比较

- 等价无穷小的性质: 自反性, 对称性, 传递性
- 等价无穷小因子替换定理: 只能在乘法用
  - $x \to 0, \ (1+x)^\mu - 1 \sim \mu x$
- 无穷小的主部: 在某极限过程中, 选定$\beta$为基准无穷小, 若$\alpha \sim c\beta^k $,则称$c\beta^k$为$\alpha$的主部

### 1.3 连续函数

#### 连续函数的定义

- 点连续:三个要点
  1. 函数$f(x)$必须在点$x_0$处有定义;
  2. $\lim_{x \to x_0} f(x)$必须存在;
  3. $\lim_{x \to x_0} f(x) = f(x_0)$.
- 左右连续:
- 连续函数: 局部保号性

#### 连续函数的运算法则

- 四则运算
- 反函数, 复合函数
- 初等函数在其定义域內的每一点处都是连续的.

#### 函数的间断

- 三个要点至少有一个不成立
- 第一类间断点: $f(x_0^-), f(x_0^+)$均存在
  - 跳跃间断点: $f(x_0^-) \neq f(x_0^+)$
  - 可去间断点: $f(x_0^-) = f(x_0^+)$
- 第二类间断点: $f(x_0^-), f(x_0^+)$至少有一个不存在
  - 无穷间断点, 等价间断点

#### 闭区间內连续函数的性质

- 零点定理
- 介值定理
- 有界性定理, 最值定理

## 第2章 导数与微分

### 2.1 导数

- 可导的定义

- 可导 $\Rightarrow$ 连续 (不能反过来)

- 反函数求导: $有 x = \varphi(y)和 y = f(x),则f'(x) \varphi'(y) = 1$

- 复合函数求导: 链式法则

  - 对数求导法

- 隐函数求导: 明确谁关于谁求导

- 参数方程求导: $y$对$x$的导数等于$y$对参数$t$的导数除以$x$对参数$t$的导数

- 高阶导数:

  - $(x^n)^{(n)} = n!$
  - $(\frac{1}{x})^{(n)} = (-1)^n \frac{n!}{x^{n+1}}$

- n阶导数的莱布尼兹公式:
  $$
  \frac{d^n}{dx^n} (uv) = \sum_{k=0}^{n} C_{n}^{k} \frac{d^{n-k}u}{dx^{n-k}} \cdot \frac{d^k v}{dx^k}
  $$

- 参数式函数的二阶导数: 再来一次

### 2.2 微分

- 可微 $\Leftrightarrow$ 可导 
- $\mathrm{d}f(x) = f'(x) \Delta x$
- 一阶微分的形式不变性 (二阶微分不具有)
- 高阶微分: 莱布尼兹公式

### 2.3 微分学中值定理

#### 中值定理

- 费马引理
- 洛尔定理
- 拉格朗日中值定理: $f(b) - f(a) = f'(\xi)(b - a)$
  - 拉格朗日中值公式的有限增量形式: $f(x_0 + \Delta x) = f(x_0) + f'(x_0 + \theta \Delta x) \Delta x$
- 单侧导数极限定理: 注意$f'(x_0)$和$\lim_{x \to x_0}f'(x)$的区别联系
- 柯西中值定理 (构造函数): $\frac{f(b) - f(a)}{g(b) - g(a)} = \frac{f'(\xi)}{g'(\xi)}$

#### 洛必达法则

- 定理条件是充分的而非必要

#### 泰勒公式

- 带皮亚诺余项: $f(x) = \sum_{k=0}^{n} \frac{f^{(k)}(x_0)}{k!}(x - x_0)^{k} + o((x - x_0)^n)$
- 带拉格朗日余项: $f(x) = \sum_{k=0}^{n} \frac{f^{(k)}(x_0)}{k!}(x - x_0)^{k} + \frac{f^{(n+1)}(\xi)}{(n+1)!}(x - x_0)^{n+1}$

### 2.4 导数的应用

- 极值点
- 拐点
- 函数作图:

## 第3章 一元函数积分学

### 3.1 不定积分

- 不要忘记积分常数$C$
- 微分运算与不定积分的关系: $\mathrm{d} \int f(x) \, \mathrm{d} x = f(x) \, \mathrm{d} x$, $\int \mathrm{d} f(x)=f(x)+C$

#### 积分方法

- 换元积分法: $\int f(u) \,\mathrm{d}u =  \int f(\varphi(v)) \cdot \varphi'(v) \,\mathrm{d}v$
  - 凑微分法: $ \int f(\varphi(v)) \cdot \varphi'(v) \,\mathrm{d}v = \int f(u) \,\mathrm{d}u = F(u)+C$
    -  $例:求 \ I = \int \csc x \ \mathrm{d}x $
  - 第二换元法: 将左端换右端计算, 需假定$u = \varphi(v)$存在反函数$v = \varphi^{-1}(x)$,
    $\int f(u) \,du = \int f(\varphi(v)) \cdot \varphi'(v) \,dv = G(v)+C = G(\varphi^{-1}(u))+C$
    - 三角函数变换
      - $\sqrt{a^2-x^2}:令\ x = a\sin t$
      - $\sqrt{x^2+a^2}:令\ x = a\tan t$
      - $\sqrt{x^2-a^2}:令\ x = a\sec t$
    - 根式替换: 将带根号的整体替换为$t$, 如$令\ t = \sqrt{1+x^2}\ 或令\ t=\sqrt[6]{x-1}$
    - 倒变量代换: $令\ x = \frac{1}{t}$
    - 注意: 若原函数为对数函数, 则被积函数应该为正
- 分部积分法: $\int u \,\mathrm{d}v = uv - \int v \,\mathrm{d}u$
  - 补充1: 分部积分过程中右端可能会出现原式$I$, 可以整体求解
    - $例:I = \int \mathrm{e}^x \sin x \mathrm \ {d}x$
  - 补充2: 如果 $\int f(x) \,\mathrm{d}x \ $中$f(x)$太复杂, 可以将$x$看作$v$先进行一次分部积分
    - $例:I = \int \sqrt{a^2+x^2}\ \mathrm{d}x$
  - 补充3: 可能通过分部积分获得递推表达式, 特征: $I_k,I_n$
    - $例:I_k = \int \frac{\mathrm{d}x}{(a^2+x^2)^k} \ (a \neq 0,\ k = 1,2,\cdots)$

##### 有理函数积分

- 有理假分式 -> 有理真分式 -(待定系数法)-> 最简分式 -> 进行积分

##### 三角函数有理式积分

- 万能代换
- 特殊情况下的特殊代换

##### 带根式的积分

- 变量代换: $令 \ t = \sqrt[n]{\frac{ax+b}{cx+d}}$

- 初等函数的导数仍然是初等函数, 但初等函数的原函数不一定是初等函数

### 3.2 定积分

- 定积分 (黎曼积分) 的定义, 黎曼和

- 函数可积的必要条件: 在闭区间$[a,b]$上有界

  - 常见几类: 在闭区间$[a,b]$上连续, 在闭区间$[a,b]$上单调有界, 在闭区间$[a,b]$上有界且只有有限多个间断点

- $若在[a,b]上f(x) \geq g(x)则\int_{a}^{b} f(x) \geq \int_{a}^{b} g(x)$

- $设f(x)在[a,b]上连续,且f(x) \geq 0,则 \ \int_{a}^{b} f(x) \mathrm{d}x > 0 \Leftrightarrow 存在 c \in [a,b],使得f(c)>0$

- 积分中值定理: 
  $设f(x),g(x)在闭区间[a,b]上连续,且g(x)在[a,b]上不变号,则存在\xi \in (a,b)使得 \int_{a}^{b} f(x) g(x) \,\mathrm{d}x = f(\xi)  \int_{a}^{b} g(x) \mathrm{d}x$

- 微积分学第一基本定理 (原函数存在定理): $\Phi'(x) = f(x)$

- 微积分学第二基本定理 (牛顿-莱布尼兹公式): $\int_{a}^{b} f(x) \, \mathrm{d} x = F(b)-F(a) = F(x)|_{a}^{b}$

  - 补充1: 数列极限的求和可转为黎曼和从而求定积分, $例:求极限 \lim_{n \to \infty} (\frac{1}{n+1}+\frac{1}{n+2}+ \cdots + \frac{1}{n+n})$

- 定积分换元法: 注意上下限以及$\mathrm{d}x$的变换

  - 补充2: 注意奇偶函数定积分的性质
  - 补充3: 在变上限积分的被积函数中若含有变量$x$, 则需要通过变量代换使得被积函数不再含有变量$x$

- 定积分分部积分法

  - 补充4: 使用分部积分法的证明题:
    $$
    求证: \int_{0}^{x}f(t)(x-t) \mathrm{d}t = \int_{0}^{x} ( \int_{0}^{t} f(x)\mathrm{d}x) \mathrm{d}t
    $$

### 3.3 定积分的应用

#### 几何学

- 直角坐标系中平面图形的面积: $A = \int_{a}^{b} (f(x)-g(x)) \  \mathrm{d} x$ 或 $A = \int_{a}^{b} (\varphi(y)-\psi(y)) \  \mathrm{d} y$
- 极坐标系中平面图形的面积: 即曲线$\rho = \rho(\theta)$与矢径$\theta = \alpha,\theta = \beta$所围的平面图形, $A = \frac{1}{2} \int_{\alpha}^{\beta} \rho^2(\theta) \ \mathrm{d}\theta$ 或 $A = \frac{1}{2} \int_{\alpha}^{\beta} (\rho_2^2(\theta)-\rho_1^2(\theta)) \ \mathrm{d}\theta$
  - 注意运用对称性缩小区间
- 旋转体体积公式:
  - 旋转圆: $V_x = \pi \int_{a}^{b} [f(x)]^2 \  \mathrm{d} x$ $V_y = \pi \int_{c}^{d} [\phi(y)]^2 \  \mathrm{d} y$
  - 薄圆筒: $V_y = 2 \pi \int_{a}^{b} x f(x) \  \mathrm{d} x$
- 平面曲线的弧长: $s = \int_{a}^{b} \sqrt{1 + f'^2(x)} \  \mathrm{d} x$, $s = \int_{\alpha}^{\beta} \sqrt{\varphi'^2(t) + \psi'^2(t)} \  \mathrm{d} t$, $s = \int_{\alpha}^{\beta} \sqrt{\rho^2(\theta) + \rho'^2(\theta)} \  \mathrm{d} \theta$
- 平面曲线的弧微分: $\mathrm{d}s = \sqrt{1 + f'^2(x)} \ \mathrm{d}x$...
- 三类椭圆积分
- 旋转曲面的面积: $A_x = 2 \pi \int_{a}^{b} f(x) \sqrt{1 + f'^2(x)} \  \mathrm{d} x$ ...

### 3.4 广义积分

#### 无穷区间上的积分

#### 无界函数的积分

- 都可以使用换元公式以及分部积分公式

## 第4章 向量代数与空间解析几何

### 4.1 向量代数

#### 向量积

右手法则

**反交换律**, 结合律, 分配律
$$
|\mathbf{a} \times \mathbf{b}| = |\mathbf{a}| \cdot |\mathbf{b}| \cdot \sin<\mathbf{a},\mathbf{b}>
\\
\\
\begin{align*}
    \mathbf{a} \times \mathbf{b} &= 
    \begin{vmatrix}
        \mathbf{i} & \mathbf{j} & \mathbf{k} \\
        a_1 & a_2 & a_3 \\
        b_1 & b_2 & b_3
    \end{vmatrix} \\
\end{align*}\\
\\
|\mathbf{a} \times \mathbf{b}|= (a_2b_3 - a_3b_2)\mathbf{i} + (a_3b_1 - a_1b_3)\mathbf{j} + (a_1b_2 - a_2b_1)\mathbf{k}
$$
海伦公式: $S = \sqrt{p \cdot (p - a) \cdot (p - b) \cdot (p - c)}$ 其中$p$为三角形的半周长

#### 混合积

几何意义: 以$a,b,c$为邻边的平行六面体的体积

$(\mathbf{a},\mathbf{b},\mathbf{c})=\mathbf{a} \times \mathbf{b} \cdot\mathbf{c}=|\mathbf{a} \times \mathbf{b}| \cdot|\mathbf{c}| \cdot \cos\theta$  (其中$\theta$是向量$\mathbf{a} \times \mathbf{b}$与$\mathbf{c}$的夹角)

$\begin{align*}
    \mathbf{a} \times \mathbf{b} \cdot\mathbf{c} &= 
    \begin{vmatrix}
        a_1 & a_2 & a_3 \\
        b_1 & b_2 & b_3 \\
        c_1 & c_2 & c_3
    \end{vmatrix} \\
\end{align*}$

$\mathbf{a} \times \mathbf{b} \times \mathbf{c} = (\mathbf{a} \cdot \mathbf{c}) \mathbf{b} - (\mathbf{b} \cdot \mathbf{c}) \mathbf{a}$

### 4.2 平面与直线

#### 平面

- 平面的点法式方程: $A(x - x_0) + B(y - y_0) + C(z - z_0) = 0$
- 平面的一般式方程: $Ax + By + Cz + D = 0$
- 平面的三点式方程: $\begin{vmatrix}
      x - x_1 & y - y_1 & z - z_1 \\
      x_2 - x_1 & y_2 - y_1 & z_2 - z_1 \\
      x_3 - x_1 & y_3 - y_1 & z_3 - z_1
  \end{vmatrix} = 0$
- 平面的截距式方程: $\frac{x}{a} + \frac{y}{b} + \frac{z}{c} = 1$
- 平面外一点到平面的距离: $d = \frac{|Ax_1 + By_1 + Cz_1 + D|}{\sqrt{A^2 + B^2 + C^2}}$

#### 直线

- 直线的点向式方程 (标准式方程, 对称式方程): $\frac{x - x_0}{l} = \frac{y - y_0}{m} = \frac{z - z_0}{n}$
- 直线的参数式方程: $\begin{cases}\begin{align*}  x &= x_0 + l t \\  y &= y_0 + m t \\  z &= z_0 + nt \end{align*}\end{cases}$
- 直线的两点式方程: $\frac{x - x_1}{x_2 - x_1} = \frac{y - y_1}{y_2 - y_1} = \frac{z - z_1}{z_2 - z_1}$
- 直线的一般式方程: $\begin{cases}  A_1x + B_1y + C_1z + D_1 = 0 \\  A_2x + B_2y + C_2z + D_2 = 0 \end{cases}$
- 直线外一点到直线的距离: $d = \frac{|\overrightarrow{M_0M_1} \times \mathbf{s}|}{|\mathbf{s}|}$
- 两直线$L_1$与$L_2$共面的充分必要条件: $\mathbf{s_1},\mathbf{s_2},\overrightarrow{M_1M_2}$这三个向量共面, 即它们混合积为0
- 两条异面直线的公垂线的方向向量: $\mathbf{s} = \mathbf{s_1} \times \mathbf{s_2}$, 距离: $d = |\mathrm{Prj}_\mathbf{s}\overrightarrow{M_1M_2}|$
- <u>(投影用数量积, 点到直线距离用向量积)</u>
- 求公垂线方程的三个方法

#### 平面与直线的关系

- 平行: $\mathbf{s} \perp \mathbf{n}$
- 垂直: $\mathbf{s} \parallel \mathbf{n} $
- 夹角: $\sin\varphi = \cos\theta = \frac{|\mathbf{s} \cdot \mathbf{n}|}{|\mathbf{s}| \cdot |\mathbf{n}|}$
- 投影与投影直线

#### 平面束

- 设直线$L$的方程为$\begin{cases}  \Pi_1: A_1x + B_1y + C_1z + D_1 = 0 \\  \Pi_2: A_2x + B_2y + C_2z + D_2 = 0 \end{cases}$, 
  则平面束的方程为: $ \Pi_\lambda:A_1x + B_1y + C_1z + D_1+\lambda(A_2x + B_2y + C_2z + D_2)=0$

### 4.3 空间曲面和空间曲线

#### 空间曲面和空间曲线的方程

- 空间曲面的一般式方程: $F(x,y,z) = 0$
- 空间曲面的参数式方程
- 空间直线的方程: 一般式, 对称式, 参数式
- 空间曲线的一般式方程 (一般式方程不唯一): $\begin{cases}
  \text{$F(x,y,z) = 0$} \\
  \text{$G(x,y,z) = 0$}
  \end{cases}$
- 空间曲线的参数式方程: $\begin{cases}
  \text{$x = x(t)$} \\
  \text{$y = y(t)$}  \\ 
  \text{$z = z(t)$}
  \end{cases}
  \space t \in [\alpha,\beta]$
  - 例: 螺旋线的参数式	方程: $\begin{cases}
    \text{$x = acos\theta$} \\
    \text{$y = bsin\theta$}  \\ 
    \text{$z = b\theta \space (b = \frac{v}{\omega})$}
    \end{cases}
    \space \theta \in R$

#### 柱面

- 直线$L$(**母线**)绕定曲线$C$(**准线**)进行平移后所形成的轨迹即为**柱面**
- 没有哪个坐标母线平行哪个坐标轴
- 柱面的参数式方程: 以曲线$C: \begin{equation}
  \left
  \{\begin{aligned}
    &\text{$F(x,y,z) = 0$} \\
    &\text{$G(x,y,z) = 0$}
  \end{aligned}
  \right.
  \end{equation}$ 为准线, 母线方向向量为$s = (l,m,n)$的柱面的方程为:
  $\begin{cases}
   \text{$F(x-lt,y-mt,z-nt) = 0$} \\
   \text{$G(x-lt,y-mt,z-nt) = 0$}
  \end{cases}$

#### 空间曲线在坐标面上的投影

- 对空间曲线 $C:\begin{equation}
  \left
  \{\begin{aligned}
    &\text{$F(x,y,z) = 0$} \\
    &\text{$G(x,y,z) = 0$}
  \end{aligned}
  \right.
  \end{equation}$ 的方程式消去变量$z$后得到的方程$h(x,y)=0$称为曲线$C$到$xOy$平面的**投影柱面**, 而投影柱面与$xOy$平面的交线 $\begin{equation}
  \left\{\begin{aligned}
    &\text{$h(x,y)=0$,} \\
    &\text{$z = 0$}
  \end{aligned}\right.\end{equation}$ 就是空间曲线$C$在$xOy$平面上的**投影曲线** (或称**投影**), 同理可得在其他平面上投影.

#### 旋转曲面

- 某个平面上的一条连续曲线$C$绕**该平面**上的一条定直线$L$选择一周生成的曲面称为**旋转曲面**. 这条定直线称为**旋转轴**, 曲线$C$称为旋转曲面的**生成曲线**.

  - 注意: 是**同一平面內**的曲线和旋转轴.

- 例: $xOy$平面上的曲线$C:\begin{equation}
  \left\{\begin{aligned}
    &\text{$f(x,y) = 0$,} \\
    &\text{$z = 0$.}
  \end{aligned}\right.\end{equation}$ 绕$x$轴旋转一周生成的旋转曲面方程为
  $$
  f(x,\pm\sqrt{y^2+z^2}) = 0.
  $$

  - 即绕哪个坐标轴哪个坐标不变.

#### 锥面

- 已知一定点$M_0(x_0,y_0,z_0)$和一条与其不共面的空间曲线$C$, 由点$M_0$与曲线$C$上所有的点的连线$L$所生成的曲面称为锥面. 点$M_0$称为锥面的顶点, 曲线$C$称为锥面的准线, 锥面上过顶点的任一条直线$L$称为锥面的母线, 方程为 (锥面的参数式方程) : $\begin{cases}
  \text{$F(x_0+t(x-x_0),y_0+t(y-y_0),z_0+t(z-z_0)) = 0$} \\
  \text{$G(x_0+t(x-x_0),y_0+t(y-y_0),z_0+t(z-z_0)) = 0$}
  \end{cases}$

#### 二次曲面

- 三元二次方程
  $$
  a_{11}x^2+a_{22}y^2+a_{33}z^2+2a_{12}xy+2a_{23}yz+2a_{31}zx+2b_1x+2b_2y+2b_3z+c = 0
  $$
  可以通过平移变换和旋转变换把一般的二次曲面方程化为标准形式. 通过平移变换消去一次项, 通过旋转变换消去混合项.

- 平移变换公式: $x=x'+a,\space y=y'+b,\space z=z'+c$

- 坐标旋转变换公式: 
  $$
  \begin{bmatrix}
    x \\ y \\z
  \end{bmatrix}
  =
  \begin{bmatrix}
    \cos{\alpha_1}& \cos{\alpha_2}& \cos{\alpha_3} \\ 
    \cos{\beta_1}& \cos{\beta_2}& \cos{\beta_3} \\
    \cos{\gamma_1}&  \cos{\gamma_2}&  \cos{\gamma_3}
  \end{bmatrix}
  \begin{bmatrix}
    x' \\ y' \\z'
  \end{bmatrix}
  $$
  或写为:
  $$
  \begin{bmatrix}
    x' \\ y' \\z'
  \end{bmatrix}
  =
  \begin{bmatrix}
    \cos{\alpha_1}& \cos{\beta_1}& \cos{\gamma_1} \\ 
    \cos{\alpha_2}& \cos{\beta_2}& \cos{\gamma_2} \\
    \cos{\alpha_3}&  \cos{\beta_3}&  \cos{\gamma_3}
  \end{bmatrix}
  \begin{bmatrix}
    x \\ y \\z
  \end{bmatrix}
  $$

- 二次曲面的分类 (见Week16作业)

- 绘制二次曲面: 平面截痕法

