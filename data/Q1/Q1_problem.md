# 题目
# 电动力系绳的轨道衰减与电热平衡

## 引言
电动力系绳（EDT）是用来与行星磁场交换能量与动量的长导线。本题考虑由两颗相同小卫星组成的 EDT 系统，每颗质量为 $m$，之间由一根长度 $L$、总电阻 $R$ 的细直导电系绳连接。系统在地球赤道面内、位于电离层高度的轨道上运行。由于重力梯度，系绳稳定保持径向指向地心。

**已知信息：**
- 地球磁场可近似为磁偶极子。在赤道面内，磁场方向与轨道面垂直。
- 距地心 $r$ 处的磁场强度为：
  \[
  B(r) = B_0 \left( \frac{R_E}{r} \right)^3
  \]
  其中 $R_E$ 为地球半径，$B_0$ 为赤道地表磁场强度。
- 半径为 $r$、总质量为 $M_{tot}$ 的圆轨道机械能为：
  \[
  E = -\frac{G M_E M_{tot}}{2r}
  \]
- 当 $x \ll 1$ 时，可用近似 $(1+x)^n \approx 1 + nx$。
- 阴极的有效发射面积 $S_{emit} = \eta S$，其中 $S$ 为系绳总表面积，$\eta$ 为无量纲系数。

---

### 第 A 部分：轨道动力学与动生电动势（3.0 分）

考虑该系绳系统初始在半径为 $r$ 的稳定圆轨道上运动（$r \gg L$）。忽略系绳质量（取 $m_{tether} = 0$），系统的主要质量仅为两颗卫星。系统质心以开普勒速度 $v$ 运动。

**A.1.** 在以系统质心为原点的旋转参考系中，求系绳中点处的张力 $T_N$。要求对 $L/r$ 做一阶泰勒展开以简化结果。**[1.2 分]**

**A.2.** 导电系绳切割地磁场磁力线，会在两端产生动生电动势（EMF）。求电动势大小 $\mathcal{E}$，用 $r$、$L$ 及给定行星常数表示。**[1.0 分]**

**A.3.** 判断感应电动势的极性。哪一端卫星（靠近地球或远离地球）会积累正电荷？**[0.8 分]**

---

### 第 B 部分：电动力阻力与轨道演化（4.0 分）

系绳浸没在电离层等离子体中。通过系绳两端的电接触器（如低端中空阴极、高端电子收集器），回路通过等离子体闭合，等离子体回路电阻可忽略。系绳中有稳定电流 $I$。

**B.1.** 推导作用在系绳上的总洛伦兹力 $\vec{F}_L$。证明该力方向恰与轨道速度矢量 $\vec{v}$ 相反。**[1.0 分]**

**B.2.** 洛伦兹力做功导致机械能耗散、轨道衰减。假设轨道始终准圆，推导轨道半径变化率 $dr/dt$ 的微分方程，结果用 $I$、$B(r)$、$L$、$m$、$M_E$ 和 $r$ 表示。**[1.5 分]**

**B.3.** 设系统从初始半径 $r_1$ 下降到 $r_2$ 的过程中，系绳中通过的总电荷为 $Q$。证明
\[
Q = \int I\,dt
\]
仅依赖于 $r_1$、$r_2$ 和行星常数（$M_E, R_E, B_0$），与系绳电阻 $R$ 或电流时间演化无关。求 $Q$ 的表达式。**[1.5 分]**

---

### 第 C 部分：电热限制与渐近演化（3.0 分）

在真实情形下，电流 $I$ 会受到系绳端部向等离子体发射电子能力的限制。在阴极（负端），电流由理查德森热电子发射定律控制，同时系绳会强烈加热。

**第 C 部分已知信息：**
- 斯特藩-玻尔兹曼定律：表面积 $S$、发射率 $\epsilon$、温度 $T$ 的辐射功率为
  \[
  P_{rad} = \epsilon \sigma S T^4
  \]
  其中 $\sigma$ 为斯特藩-玻尔兹曼常数。
- 理查德森定律：温度 $T$、发射面积 $S_{emit}$ 的饱和发射电流为
  \[
  I = S_{emit} A_R T^2 \exp\left(-\frac{\Phi}{k_B T}\right)
  \]
  其中 $A_R$ 为理查德森常数，$\Phi$ 为逸出功。

**C.1.** 当焦耳热功率与辐射散热及电子带走的能量平衡时，系绳达到稳态温度 $T_{eq}$。假设每个电子携带的动能相对于逸出功 $\Phi$ 可忽略，并假设感应电动势 $\mathcal{E}$ 足够大，使得电流 $I$ 恰等于阴极温度允许的饱和电流 $I_{sat}$。写出一个自洽方程组，用以确定 $T_{eq}$ 与 $I_{sat}$，并用系绳参数（$R, S, \eta, \epsilon, \Phi$）以及局部电动势 $\mathcal{E}$ 表示。**[1.2 分]**

**C.2.** 考虑极限情形：焦耳热主导发射冷却（$I^2 R \gg I\Phi/e$），且热能远大于逸出功（$k_B T \gg \Phi$），此时理查德森定律中的指数项可近似为 $\exp(-\Phi/k_B T) \approx 1 - \Phi/k_B T$。假设系统在“临界点”工作，即 $I_{sat}$ 被可用电动势 $\mathcal{E}(r)$ 正好限制，求该极限下的轨道衰减率 $|dr/dt|$。结果用系绳材料/几何常数（$S, \epsilon, R, L$）、卫星质量 $m$ 以及局部轨道参数（$B, v, r$）表示。**[1.8 分]**

# 题目评审
### [1] 最终评估结论
**通过（可直接采用）**
题目物理背景严谨、数学结构优雅，并很好地契合 IPhO 的“渐进叙事”风格。它把轨道力学、电动力学与热学三部分整合成一个自洽反馈链路。B.3 中的“总电荷只依赖轨道半径”的发现非常有亮点，C. 部分的热发射限制则提供了区分高水平选手的门槛。

### [2] 多维评审反馈

- **2.1 叙事节奏与引导文本：**
  叙事节奏优秀。引言部分信息简洁，关键热学定律推迟到 C 部分再给出，避免“信息倾倒”。A→B→C 的模型升级（被动导线 → 闭合回路 → 热限制）具有研究推进感。

- **2.2 符号一致性与自由度检查：**
  - **一致性：** 所有符号（$M_E, R_E, B_0, m, L, R, S, \epsilon, A_R, \Phi$）与框架一致。
  - **闭合性：** $r$ 决定 $v$ 与 $B$，进而确定 $\mathcal{E}$；$\mathcal{E}$ 与 $R$（及热限制）决定 $I$；$I$ 决定 $F_L$，从而决定 $dr/dt$。不存在冗余或缺失自由度。

- **2.3 设问标准与分值审核：**
  - **动词规范：** “证明…”“推导…微分方程…”“求渐近表达式…”符合 IPhO 标准。
  - **分值核对：**
    - A 部分：1.2 + 1.0 + 0.8 = **3.0**
    - B 部分：1.0 + 1.5 + 1.5 = **4.0**
    - C 部分：1.2 + 1.8 = **3.0**
    - **总分：10.0 分**，符合框架要求。

- **2.4 隐含条件与计算评估：**
  - **A.1：** 一阶重力梯度展开是标准但不低阶的考点。
  - **B.3：** 通过积分得到 $Q$ 与 $R$ 无关，是题目的“顿悟”点。
  - **C.2：** 利用 $\exp(-x) \approx 1-x$ 将超越方程简化为可解的极限形式，对尺度判断有要求。

### [3] 主要风险提示

**A.1 张力系数歧义：**
在旋转系中，对两个点质量 $m$、相距 $L$ 的系统，张力应为
\[
T = \frac{3 G M_E m L}{2 r^3}
\]
但某些教材（或框架原文）在把系统当作总质量为 $2m$ 的连续杆时会出现 $3/4$ 系数。题干已给出 $m_{tether}=0$，因此应明确采用点质量推导（系数 $3/2$）。

**C.2 逻辑难点：**“临界点 $I_{sat}$ 正好受电动势限制”的措辞较复杂，会让学生在 $I^2 R$ 与 $T^4$ 的替换中迷失。评分细则中需明确演算路径，指出如何在此条件下消除 $I$ 或得到材料常数主导的表达式。

### [4] 可执行修改建议
**无。** 题目可直接用于竞赛。

*(可选优化：在解答中明确替换 $v = \sqrt{G M_E/r}$ 与 $B \propto r^{-3}$ 的步骤，使 B.3 中的 $r^{3/2}$ 积分结构一目了然。)*

### [5] 题目与答案可能不妥之处（补充）
- **地磁场方向假设可能引起混淆：** 真实偶极场在赤道面内的磁场方向并非垂直于轨道面。若要简化为垂直，应在题干明确这是理想化假设。
- **C.1 的“包含 $\mathcal{E}$”要求与饱和假设不一致：** 在“电动势足够大、完全饱和”情形下，$\mathcal{E}$ 实际不进入稳态方程。可在题干中补充“若电动势不足，则需加上 $I=\mathcal{E}/R$ 约束”。
- **C.2 的变量要求与结果不一致：** 题干要求结果“用 $S, \epsilon$ 等表示”，但在电压瓶颈假设下最终表达式不含这些量。建议改写为“可包含或可能不包含”。
- **总质量表达需更显式：** 题干虽说每颗质量为 $m$，但在 B.2 中需用总质量 $2m$。可在 B.2 题干中显式提醒，以减少误解。
- **A.2 的速度场假设：** 计算动生电动势时默认系绳各点具有相同角速度，建议在题干中说明“刚性随体运动”。

# 答案
### 第 A 部分
**[A.1 标准解]**
- **[物理依据]**：在以质心为原点、角速度
  \[
  \omega = \sqrt{\frac{G M_E}{r^3}}
  \]
  的旋转参考系中，距离质心 $x$ 的质量点所受的径向有效力为重力与离心力之和。
- **[方程]**：
  \[
  F_{eff} = m\omega^2(r+x) - \frac{G M_E m}{(r+x)^2} \quad (1)
  \]
- **[推导步骤]**：对 $x \ll r$ 做一阶展开：
  \[
  F_{eff} \approx m\frac{G M_E}{r^3}(r+x) - \frac{G M_E m}{r^2}\left(1 - \frac{2x}{r}\right)
  = \frac{3 G M_E m x}{r^3}
  \]
  对外端卫星取 $x = L/2$，由于系绳无质量，张力在绳上均匀。
- **[最终结果]**：
  \[
  T_N = \frac{3 G M_E m L}{2 r^3}
  \]

**[A.2 标准解]**
- **[物理依据]**：系绳切割磁场产生动生电动势。
- **[方程]**：
  \[
  \mathcal{E} = \int_{r-L/2}^{r+L/2} v(r') B(r')\,dr' \quad (2)
  \]
- **[推导步骤]**：代入 $v(r') = \omega r'$、$B(r') = B_0(R_E/r')^3$：
  \[
  \mathcal{E} = \omega B_0 R_E^3 \left[-\frac{1}{r'}\right]_{r-L/2}^{r+L/2}
  \approx \frac{\omega B_0 R_E^3 L}{r^2}
  \]
  再用 $\omega = \sqrt{G M_E / r^3}$。
- **[最终结果]**：
  \[
  \mathcal{E} = B_0 R_E^3 L \sqrt{\frac{G M_E}{r^7}}
  \]

**[A.3 标准解]**
- **[物理依据]**：感应电场方向为 $\vec{E}_{ind} = \vec{v} \times \vec{B}$。
- **[推导步骤]**：在赤道面内，$\vec{v}$ 沿切向，$\vec{B}$ 沿轨道面法向。右手定则给出 $\vec{v} \times \vec{B}$ 指向径向外侧。
- **[最终结果]**：远离地球的一端积累正电荷。

---

### 第 B 部分
**[B.1 标准解]**
- **[物理依据]**：洛伦兹力为 $d\vec{F}_L = I\,d\vec{l} \times \vec{B}$。
- **[推导步骤]**：电流由内端流向外端，$d\vec{l}$ 沿 $+\hat{r}$。于是
  \[
  \vec{F}_L = \int I (\hat{r} \,dr') \times (B(r')\hat{z})
  = \int I B(r')(-\hat{\phi})\,dr'
  \]
  轨道速度 $\vec{v}$ 沿 $+\hat{\phi}$，故 $\vec{F}_L$ 与 $\vec{v}$ 反向。
- **[最终结果]**：
  \[
  \vec{F}_L \approx - I B(r) L\,\hat{v}
  \]

**[B.2 标准解]**
- **[方程]**：总机械能
  \[
  E = -\frac{G M_E (2m)}{2r} = -\frac{G M_E m}{r}
  \]
  功率损失 $P = \vec{F}_L \cdot \vec{v} = - I B L v$。
- **[推导步骤]**：
  \[
  \frac{dE}{dt} = \frac{G M_E m}{r^2}\frac{dr}{dt} = - I B L \sqrt{\frac{G M_E}{r}}
  \]
- **[最终结果]**：
  \[
  \frac{dr}{dt} = - \frac{I B_0 R_E^3 L}{m \sqrt{G M_E} \, r^{3/2}}
  \]

**[B.3 标准解]**
- **[推导步骤]**：
  \[
  Q = \int I\,dt = \int \frac{I}{dr/dt}\,dr
  \]
  由 B.2 得
  \[
  I\,dt = -\frac{m \sqrt{G M_E}}{B(r) L r^{3/2}}\,dr
  \]
  因而
  \[
  Q = \frac{m \sqrt{G M_E}}{B_0 R_E^3 L} \int_{r_2}^{r_1} r^{3/2}\,dr
  \]
- **[最终结果]**：
  \[
  Q = \frac{2 m \sqrt{G M_E}}{5 B_0 R_E^3 L} \left(r_1^{5/2} - r_2^{5/2}\right)
  \]

---

### 第 C 部分
**[C.1 标准解]**
- **[方程组]**：
  \[
  I^2 R = \epsilon \sigma S T_{eq}^4 + \frac{I\Phi}{e}
  \]
  \[
  I_{sat} = \eta S A_R T_{eq}^2 \exp\left(-\frac{\Phi}{k_B T_{eq}}\right)
  \]
  并取 $I = I_{sat}$。

**[C.2 标准解]**
- **[推导步骤]**：在 $I^2 R \gg I\Phi/e$、$k_B T \gg \Phi$ 情况下，
  \[
  I^2 R \approx \epsilon \sigma S T^4, \quad I \approx \eta S A_R T^2
  \]
  临界点由可用电动势限制：
  \[
  I = \frac{\mathcal{E}}{R} = \frac{B L v}{R}
  \]
  代入 B.2 的衰减率表达式 $|dr/dt| = \frac{I B L r}{m v}$，得到
  \[
  |dr/dt| = \frac{(B L v / R)\, B L r}{m v} = \frac{B^2 L^2 r}{m R}
  \]
- **[最终结果]**：
  \[
  |dr/dt| = \frac{B^2 L^2 r}{m R}
  \]

# 答案校核
### [第 1 部分：推导严谨性审计]
- **步骤检查：**
  - **A.1**：重力梯度与离心力在旋转系中正确处理，一阶展开得到净外向力并导出张力。
  - **A.2**：动生电动势的积分设定正确，结合 $v(r')$ 与 $B(r')$ 得到一阶结果。
  - **A.3**：$\vec{v} \times \vec{B}$ 方向判断正确。
  - **B.1**：洛伦兹力表达式与方向判断正确。
  - **B.2**：功-能关系建立正确，且正确使用总质量 $2m$ 得到 $E = -G M_E m / r$。
  - **B.3**：变量替换 $dt \to dr$ 正确处理符号，积分正确。
  - **C.1**：能量平衡与发射电流约束建立正确。
  - **C.2**：临界点条件处理正确，直接用 $I = \mathcal{E}/R$ 得到简洁结果。

- **逻辑缺陷标记：**
  - **[跳步/逻辑缺口]**：无。题干要求“包含 $\mathcal{E}$”，但在纯饱和发射情形下 $\mathcal{E}$ 与稳态方程解耦；答案正确。
  - **[不当近似]**：无。一阶泰勒近似合理。
  - **[数学错误]**：无。

### [第 2 部分：正确性与闭合性核验]
- **最终结果核验：**
  - **A.1**：正确。
  - **A.2**：正确。
  - **A.3**：正确。
  - **B.1**：正确。
  - **B.2**：正确。
  - **B.3**：正确。
  - **C.1**：正确。
  - **C.2**：正确。
- **闭合性评估：**
  所有最终变量均可由给定常量确定。C.2 中最终表达式不含 $S$ 与 $\epsilon$，体现了“电压瓶颈”条件下热发射参数被剔除的物理事实。

### [第 3 部分：物理一致性压力测试]
- **量纲检查：**
  - **B.2 结果：**
    \[
    \frac{dr}{dt} \propto \frac{I B_0 R_E^3 L}{m \sqrt{G M_E} \, r^{3/2}}
    \]
    分子 $[I B L]$ 为力，分母为质量×频率，商为速度，量纲正确。
  - **C.2 结果：**
    \[
    |dr/dt| \propto \frac{B^2 L^2 r}{m R}
    \]
    等价于功率/（质量×速度），量纲为速度，正确。

- **极限检验：**
  - **绝缘极限 $R \to \infty$：** $|dr/dt| \to 0$，符合无电流则无阻力的物理预期。
  - **惯性极限 $m \to \infty$：** $|dr/dt| \to 0$，符合巨大惯性下轨道难以变化。

- **守恒律检查：**
  角动量 $L_{ang} = 2m \sqrt{G M_E r}$，磁力矩 $\tau = -I B L r$。计算 $dL_{ang}/dt$ 后可与 $\tau$ 一致，物理闭合。

### [第 4 部分：最终结论]
- **严谨评分：** 10 / 10
- **可用性结论：** 可直接采用
- **专家意见：** 该解答非常稳健，C.2 中通过临界点条件将热发射复杂性简化为欧姆瓶颈，是物理直觉的高质量体现。

# 评分细则
### [IPhO 官方评分方案]
**总分：10.0 分**

#### 第 A 部分：轨道动力学与动生电动势（总分：3.0 分）

| 小问 | 关键步骤/公式 | 分值 | 阅卷说明 |
| :--- | :--- | :--- | :--- |
| **A.1** | **有效力方程：** 旋转系中径向合力（重力+离心力）$F_{eff} = m\omega^2(r+x) - \frac{G M_E m}{(r+x)^2}$ | 0.3 | 允许使用等价的广义坐标或潮汐力表述。 |
| | **泰勒展开：** $x \ll r$ 时一阶展开，得到 $F_{eff} \approx \frac{3 G M_E m x}{r^3}$ | 0.4 | 0.2 给出 $\omega^2=GM_E/r^3$，0.2 为代数展开。 |
| | **受力平衡与张力一致性：** 系绳无质量，张力均匀；取 $x=L/2$。 | 0.3 | 需显式代入 $x=L/2$。 |
| | **最终结果：** $T_N = \frac{3 G M_E m L}{2 r^3}$ | 0.2 | 量纲必须为力。 |
| **A.2** | **动生电动势表达式：** $\mathcal{E} = \int_{r-L/2}^{r+L/2} v(r') B(r') dr'$ 或 $\mathcal{E} \approx v_{cm} B_{cm} L$ | 0.3 | 由于 $L \ll r$，两种写法均可。 |
| | **代入场与速度：** $v=\omega r$，$B=B_0(R_E/r)^3$ | 0.3 | |
| | **开普勒替换：** $\omega=\sqrt{G M_E/r^3}$ | 0.2 | |
| | **最终结果：** $\mathcal{E} = B_0 R_E^3 L \sqrt{\frac{G M_E}{r^7}}$ | 0.2 | **ECF：** 若 $r$ 次幂错误但推导连贯，扣 0.2。**A.2 总分 1.0** |
| **A.3** | **方向判断：** 使用右手定则判断 $\vec{v} \times \vec{B}$ | 0.4 | 必须说明正电荷受力方向径向外。 |
| | **结论：** 远离地球的卫星积累正电荷 | 0.4 | 无推理过程不给分。**A.3 总分 0.8** |
| **小计** | **A 部分总分** | **3.0** | |

---

#### 第 B 部分：电动力阻力与轨道演化（总分：4.0 分）

| 小问 | 关键步骤/公式 | 分值 | 阅卷说明 |
| :--- | :--- | :--- | :--- |
| **B.1** | **洛伦兹力表达式：** $d\vec{F}_L = I d\vec{l} \times \vec{B}$ | 0.3 | 可接受积分式或宏观式 $\vec{F}_L = I\vec{L} \times \vec{B}$。 |
| | **电流方向与叉乘：** 电流从内端流向外端，$d\vec{l} = \hat{r} dr$ | 0.3 | |
| | **大小与方向：** $F_L = I B(r) L$ 且方向为 $-\hat{\phi}$ | 0.4 | 0.2 给大小，0.2 给方向。**B.1 总分 1.0** |
| **B.2** | **总能量/角动量：** $E_{tot} = -\frac{G M_E (2m)}{2r} = -\frac{G M_E m}{r}$ | 0.4 | **陷阱：** 忘记总质量为 $2m$。若写成 $-G M_E m/(2r)$ 扣 0.2。 |
| | **功率/力矩：** $\frac{dE}{dt} = \vec{F}_L \cdot \vec{v} = -I B L v$ | 0.4 | 需负号表示能量耗散。 |
| | **对 $r$ 求导：** $\frac{dE}{dt} = \frac{G M_E m}{r^2}\frac{dr}{dt}$ | 0.4 | |
| | **最终结果：** $\frac{dr}{dt} = - \frac{I B_0 R_E^3 L}{m \sqrt{G M_E} r^{3/2}}$ | 0.3 | 需正确代入 $B(r)$。**B.2 总分 1.5** |
| **B.3** | **积分设置与变量替换：** $Q = \int I dt = \int I \left(\frac{dt}{dr}\right) dr$ | 0.5 | |
| | **消去电流：** 由 B.2 得 $I dt = -\frac{m\sqrt{G M_E}}{B(r) L r^{3/2}} dr$ | 0.5 | **ECF：** 若 B.2 使 $I$ 无法消去，则后续不给分。 |
| | **积分：** $\int r^{3/2} dr = \frac{2}{5} r^{5/2}$ | 0.3 | 极限需正确。 |
| | **最终结果：** $Q = \frac{2 m \sqrt{G M_E}}{5 B_0 R_E^3 L}(r_1^{5/2} - r_2^{5/2})$ | 0.2 | 与 $I(t)$、$R$ 无关即满足“证明”。**B.3 总分 1.5** |
| **小计** | **B 部分总分** | **4.0** | |

---

#### 第 C 部分：电热限制与渐近演化（总分：3.0 分）

| 小问 | 关键步骤/公式 | 分值 | 阅卷说明 |
| :--- | :--- | :--- | :--- |
| **C.1** | **焦耳热与辐射：** $P_{in} = I^2 R$，$P_{rad} = \epsilon \sigma S T_{eq}^4$ | 0.4 | 各 0.2 分。 |
| | **发射冷却：** $P_{emit} = I \Phi/e$ | 0.2 | 需写出完整能量平衡。 |
| | **理查德森定律：** $I_{sat} = \eta S A_R T_{eq}^2 \exp(-\Phi/k_B T_{eq})$ | 0.4 | |
| | **系统闭合：** $I = I_{sat}$ 且列出两条耦合方程 | 0.2 | 两式完整才给分。**C.1 总分 1.2** |
| **C.2** | **临界点条件：** 若受电动势限制，则 $I = \mathcal{E}/R$ | 0.4 | 不罚学生多余求 $T_{eq}$。 |
| | **代入局部电动势：** $\mathcal{E} = v B L$ | 0.4 | |
| | **代入衰减率：** 使用 B.2 式得到 $|dr/dt|$ | 0.5 | 需使用自身的 B.2 结果。 |
| | **最终化简：** $|dr/dt| = \frac{B^2 L^2 r}{m R}$ | 0.5 | 需为允许变量。**C.2 总分 1.8** |
| **小计** | **C 部分总分** | **3.0** | |

---

### [阅卷补充说明]

1. **允许误差与冗余推导：**
   - **A.2**：$L \ll r$ 时直接用质心处 $\mathcal{E} = v_{cm} B_{cm} L$ 也给满分。
   - **C.2**：若学生直接使用 $I = \mathcal{E}/R$ 跳过热学代数，给满分。

2. **常见错误与扣分：**
   - **致命错误（模型崩溃）：**
     - **B.3** 中若 $I$ 无法消去，则后续不给分。
     - **量纲不一致** 的最终结果，对该项给 0 分。
   - **轻微错误（扣 0.2–0.4）：**
     - **B.2 的质量陷阱：** 忘记总质量 $2m$ 扣 0.2。
     - **符号错误：** B.2 漏负号扣 0.2；C.2 若未取绝对值扣 0.2。

3. **替代解法提示：**
   - **A.1 潮汐力法：** 通过重力梯度与离心力差得到 $\frac{3 G M_E m \Delta r}{r^3}$，等价可给满分。
   - **B.2 角动量法：** 用 $L_{ang} = 2m \sqrt{G M_E r}$ 与 $\tau = -I B L r$ 推导，按同等分值给分。

![](image/ipho_2025_1_1.png)

# 图示代码
### [1] 视觉方案

**图表数量：2**

**图 1：轨道构型与动生电动势**
- **插入位置：** 引言之后、A 部分之前。
- **绘制内容与配色：**
  - **全局视图：** 地球（浅蓝）与虚线圆轨道。
  - **系绳系统：** 两颗卫星（深灰圆点）由实线系绳连接，整体径向指向地心。
  - **向量：** 轨道速度 $\vec{v}$（蓝色箭头，切向）、磁场 $\vec{B}$（绿色出屏符号 $\odot$）、径向距离 $r$。
  - **物理隐喻：** 用 $(r, \theta)$ 坐标展示“重力梯度”稳定。
- **核心符号：** $R_E$, $r$, $L$, $\vec{v}$, $\vec{B}$, $m$。

**图 2：电动力与等离子体回路模型**
- **插入位置：** B 部分过渡文字之后、B.1 之前。
- **绘制内容与配色：**
  - **局部视图：** 放大系绳。
  - **电流与受力：** 红色电流箭头 $I$；橙色洛伦兹力 $\vec{F}_L$，方向与 $\vec{v}$ 相反。
  - **回路：** 浅蓝虚线表示电离层回路。
  - **热效应：** 紫色波纹箭头表示辐射功率 $P_{rad}$，与 C 部分呼应。
- **核心符号：** $I$, $\vec{F}_L$, $\vec{v}$, $P_{rad}$, 内端卫星, 外端卫星。

---

### [2] 集成 Python 脚本

```python
import matplotlib.pyplot as plt
import matplotlib.patches as patches
import numpy as np

# 使用 Matplotlib 内置数学字体，避免外部 LaTeX 依赖
plt.rcParams.update({
    "text.usetex": False,
    "mathtext.fontset": "cm",  # 使用 Computer Modern 学术字体
    "font.family": "serif",
    "font.size": 11
})

def generate_figure_1():
    """绘制图 1：轨道构型与动生电动势。"""
    fig, ax = plt.subplots(figsize=(7, 6))
    ax.set_aspect('equal')
    ax.axis('off')

    # 地球
    earth_radius = 2.0
    earth = patches.Circle((0, 0), earth_radius, color='#AADDFF', ec='#5588AA', lw=2, label='Earth')
    ax.add_patch(earth)
    ax.text(0, 0, r'地球 ($M_E$)', ha='center', va='center', fontsize=12, fontweight='bold')

    # 轨道
    orbit_r = 5.0
    orbit_arc = patches.Arc((0, 0), 2*orbit_r, 2*orbit_r, theta1=20, theta2=70, ls='--', color='gray', alpha=0.6)
    ax.add_patch(orbit_arc)

    # 系绳系统位于 45 度方向
    angle = np.deg2rad(45)
    r1 = orbit_r - 0.6
    r2 = orbit_r + 0.6
    x1, y1 = r1 * np.cos(angle), r1 * np.sin(angle)
    x2, y2 = r2 * np.cos(angle), r2 * np.sin(angle)

    # 卫星
    ax.plot([x1, x2], [y1, y2], color='black', lw=2, zorder=3)
    ax.scatter([x1, x2], [y1, y2], color='#444444', s=80, zorder=4)
    ax.text(x1-0.2, y1-0.4, r'$m$', ha='center')
    ax.text(x2+0.2, y2+0.3, r'$m$', ha='center')

    # 几何标注
    ax.annotate('', xy=(x2, y2), xytext=(x1, y1), arrowprops=dict(arrowstyle='<->', color='black'))
    ax.text((x1+x2)/2 + 0.3, (y1+y2)/2, r'$L$', fontsize=12)

    # 半径向量
    ax.annotate('', xy=(x1, y1), xytext=(0, 0), arrowprops=dict(arrowstyle='->', color='black', ls=':'))
    ax.text(1.2, 2.2, r'$r$', fontsize=12)

    # 速度矢量
    v_dir = np.array([-np.sin(angle), np.cos(angle)])
    v_start = np.array([(x1+x2)/2, (y1+y2)/2])
    ax.quiver(v_start[0], v_start[1], v_dir[0], v_dir[1], color='blue', scale=4, width=0.015, zorder=5)
    ax.text(v_start[0]-0.8, v_start[1]+0.5, r'$\vec{v}$', color='blue', fontsize=14)

    # 磁场（出屏）
    for i in range(3):
        for j in range(3):
            bx, by = 3.5 + i*0.8, 0.5 + j*0.8
            ax.text(bx, by, r'$\odot$', color='forestgreen', fontsize=15, ha='center', va='center')
    ax.text(5.5, 1.5, r'$\vec{B}$', color='forestgreen', fontsize=14)

    plt.title("图 1：赤道面内 EDT 轨道构型", pad=20)
    plt.tight_layout()
    plt.savefig("Figure_1.png", dpi=300, bbox_inches='tight')
    plt.close(fig)
    print("已生成 Figure_1.png")

def generate_figure_2():
    """绘制图 2：电动力与等离子体回路。"""
    fig, ax = plt.subplots(figsize=(7, 5))
    ax.set_aspect('equal')
    ax.axis('off')

    # 系绳
    tether_y = np.linspace(-2, 2, 100)
    tether_x = np.zeros_like(tether_y)
    ax.plot(tether_x, tether_y, color='black', lw=3, zorder=3)

    # 卫星（内端与外端）
    ax.scatter([0, 0], [-2, 2], color='#444444', s=150, zorder=4)
    ax.text(0.3, 2, '外端卫星（远地）', va='center')
    ax.text(0.3, -2, '内端卫星（近地）', va='center')

    # 电流 I
    ax.annotate('', xy=(0, 0.5), xytext=(0, -0.5), arrowprops=dict(arrowstyle='->', color='red', lw=2))
    ax.text(-0.4, 0, r'$I$', color='red', fontsize=14, fontweight='bold')

    # 洛伦兹力 F_L
    ax.quiver(0, 0, -1.5, 0, color='orangered', scale=5, width=0.02, zorder=5)
    ax.text(-1.2, 0.3, r"$\vec{F}_L$", color='orangered', fontsize=14)

    # 速度 v
    ax.quiver(0, 0, 1.5, 0, color='blue', scale=5, width=0.01, alpha=0.5)
    ax.text(1.0, 0.3, r"$\vec{v}$", color='blue', fontsize=14)

    # 等离子体回路
    arc_theta = np.linspace(-np.pi/2, np.pi/2, 50)
    arc_x = 1.5 * np.cos(arc_theta)
    arc_y = 2.0 * np.sin(arc_theta)
    ax.plot(arc_x, arc_y, color='skyblue', ls='--', lw=2, alpha=0.7)
    ax.text(1.6, 0, '电离层\n回路路径', color='skyblue', ha='left', fontsize=10)

    # 热辐射（对应 C 部分）
    for y_pos in [-1.2, 0, 1.2]:
        for direction in [-1, 1]:
            dx = 0.3 * direction
            ax.annotate('', xy=(dx*2, y_pos+0.2), xytext=(dx, y_pos),
                         arrowprops=dict(arrowstyle='->', connectionstyle="arc3,rad=.3", color='purple', alpha=0.6))
    ax.text(-1.2, -1.8, r'$P_{rad} \propto T^4$', color='purple', fontsize=10)

    # 磁场符号
    ax.text(-1.5, 2, r'$\vec{B} = \odot$', color='forestgreen', fontsize=14)

    plt.title("图 2：电动力与等离子体回路", pad=20)
    plt.tight_layout()
    plt.savefig("Figure_2.png", dpi=300, bbox_inches='tight')
    plt.close(fig)
    print("已生成 Figure_2.png")

if __name__ == "__main__":
    generate_figure_1()
    generate_figure_2()
    print("IPhO 第 1 题所有示意图已生成。")
```
