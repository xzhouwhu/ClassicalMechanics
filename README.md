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

## 运行环境

Python 3 与 Jupyter，依赖 numpy、matplotlib、scipy：

```bash
pip install numpy matplotlib scipy jupyterlab
```


