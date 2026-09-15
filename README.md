# 理论力学教学代码

以**前向欧拉法（Forward Euler）**为主线的理论力学数值计算教学笔记本：用最简单的数值格式求解各类经典力学系统，考察其解的精度与能量行为。

## 第一章：前向欧拉法

| 编号 | 笔记本 | 系统 | 关注点 |
| :--: | ------ | ---- | ------ |
| 1 | [匀速直线运动](Chapter1/1_uniform_motion_euler.ipynb) | $\dot x = v$ | 欧拉法与解析解的关系 |
| 2 | [自由落体运动](Chapter1/2_free_fall_euler.ipynb) | $\dot v = g$ | 位置误差与能量漂移随 $t$ 的增长 |
| 3 | [一维简谐振子](Chapter1/3_simple_oscillator_euler.ipynb) | $m\ddot x = -kx$ | 速度相空间中的轨迹演化 |
| 4 | [大振幅单摆](Chapter1/4_simple_pendulum_euler.ipynb) | $\ddot\theta = -\tfrac{g}{L}\sin\theta$ | 非线性、周期随振幅的变化 |
| 5 | [两耦合振子](Chapter1/5_coupled_oscillators_euler.ipynb) | 简正模叠加 | 拍、能量交换、多时间尺度 |

各册均采用同一教学结构：**运行前先写下预测 → 运行并对照 → 结论与思考**。

## 运行环境

Python 3 与 Jupyter，依赖 numpy、matplotlib、scipy：

```bash
pip install numpy matplotlib scipy jupyterlab
```

## 作者

[周详](mailto:xiangzhou@whu.edu.cn)、武汉大学
