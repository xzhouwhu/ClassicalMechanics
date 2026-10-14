# 经典力学教学代码
- [周详](mailto:xiangzhou@whu.edu.cn)
- 武汉大学

## 第一章：一维力学系统

| 编号 | 笔记本 | 系统 | 关注点 |
| :--: | ------ | ---- | ------ |
| 1 | [匀速直线运动](Chapter1/1_uniform_motion_euler.ipynb) | $\dot x = v$ | 欧拉法与解析解的关系 |
| 2 | [自由落体运动](Chapter1/2_free_fall_euler.ipynb) | $\dot v = g$ | 位置误差与能量漂移随 $t$ 的增长 |
| 3 | [一维简谐振子](Chapter1/3_simple_oscillator_euler.ipynb) | $m\ddot x = -kx$ | 速度相空间中的轨迹演化 |
| 4 | [大振幅单摆](Chapter1/4_simple_pendulum_euler.ipynb) | $\ddot\theta = -\tfrac{g}{L}\sin\theta$ | 非线性、周期随振幅的变化 |
| 5 | [两耦合振子](Chapter1/5_coupled_oscillators_euler.ipynb) | 简正模叠加 | 拍、能量交换、多时间尺度 |

各例均采用同一教学结构：**运行前先写下预测 → 运行并对照 → 结论与思考**。

## 第二章：二维力学系统

| 编号 | 笔记本 | 系统 | 关注点 |
| :--: | ------ | ---- | ------ |
| 1 | [匀速圆周运动](Chapter2/1_circular_motion_euler.ipynb) | $\boldsymbol F = -kr\boldsymbol e_r$ | 直角坐标 vs 极坐标：同一方法的两种命运 |
| 2 | [两种坐标画法](Chapter2/2_polar_vs_rectangular_euler.ipynb) | $\boldsymbol F = -kr\boldsymbol e_r$ | 极坐标网格 vs 直角化 $(r, \theta)$ 平面：坐标如何呈现运动 |
| 3 | [自由落体运动](Chapter2/3_free_fall_rk2.ipynb) | $\dot v = g$ | 常力下 RK2 精确到机器精度："恰好精确"的特例 |
| 4 | [一维简谐振子](Chapter2/4_simple_oscillator_rk2.ipynb) | $m\ddot x = -kx$ | 每步能量漂移律 $E_n = E_0(1 + z^4/4)^n$ 的解析推导 |
| 5 | [大振幅单摆](Chapter2/5_simple_pendulum_rk2.ipynb) | $\ddot\theta = -\tfrac{g}{L}\sin\theta$ | 非线性下的能量漂移：摆被"注"进旋转区；RK45 / DOP853 对比 |
| 6 | [匀速圆周运动](Chapter2/6_circular_motion_rk2.ipynb) | $\boldsymbol F = -kr\boldsymbol e_r$ | 漂移律原封照搬；极坐标下仍精确——精确性由坐标裁决 |
| 7 | [阻尼振子](Chapter2/7_damped_oscillator_euler_rk2.ipynb) | $\ddot x = -\omega_0^2 x - 2\beta\dot x$ | 欧拉法的数值"反阻尼"与稳定界限 $h^* = 2\beta/\omega_0^2$ |

## 第四章：变分积分器与混沌

| 编号 | 笔记本 | 系统 | 关注点 |
| :--: | ------ | ---- | ------ |
| 1 | [自由落体运动](Chapter4/1_free_fall_variational.ipynb) | $\dot x = v,\ \dot v = g$ | 离散哈密顿原理：位置精确到机器精度——二次解的特权 |
| 2 | [一维简谐振子](Chapter4/2_simple_oscillator_variational.ipynb) | $m\ddot x = -kx$ | 二次型能量严格恒等——对照 RK2 漂移律 $E_n = E_0(1+z^4/4)^n$ |
| 3 | [大振幅单摆](Chapter4/3_simple_pendulum_variational.ipynb) | $\ddot\theta = -\tfrac{g}{l}\sin\theta$ | 非线性下能量只剩 $O(h^2)$ 有界带宽：数值不改写运动拓扑 |
| 4 | [匀速圆周运动](Chapter4/4_circular_variational.ipynb) | $\boldsymbol F = -kr\boldsymbol e_r$ | 二维二次型：能量严格守恒之外，角动量同样守恒 |
| 5 | [受迫单摆的混沌](Chapter4/5_driven_pendulum_variational.ipynb) | 悬点竖直驱动 $y_s = a\cos\omega t$ | 真实 SI 参数下的混沌：双胞胎初值 $t = 60.66$ s 当屏分岔，$\lambda \approx 0.475$/周期 |

变分积分器不再离散运动方程，而是把哈密顿原理"作用量取极值"原封搬到离散时间：数值轨道即离散作用量的驻点序列。例 1–4 是自治系统，能量给出两级保证——二次型严格恒等、非线性 $O(h^2)$ 有界带宽；例 5 引入悬点驱动与真实参数（$m = 1$ kg，$l = 1$ m，$g = 9.8$ m/s²），混沌登台：初值只在小数点后第 10 位有差（$\dot\theta_0 = 0$ vs $10^{-10}$ rad/s）的双胞胎，$100$ s 动画里当屏分道。教学结构仍为**预测 → 对照 → 为什么**。

## 运行环境

Python 3 与 Jupyter，依赖 numpy、matplotlib、scipy：

```bash
pip install numpy matplotlib scipy jupyterlab
```


