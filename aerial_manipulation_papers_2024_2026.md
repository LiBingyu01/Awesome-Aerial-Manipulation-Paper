# Aerial Manipulation / 空中机械臂近期论文清单（2024–2026）

> 检索更新：**2026-10-19**。共 **58 篇独立研究论文/观点文章**，外加 **4 篇综述/路线图**。按首次公开或正式发表年份整理，同一工作不同版本只收录一次。关注空中机械臂（UAV + articulated/continuum arm）、飞行抓取器、接触操作、空中协同操纵，以及与具身智能相关的空中操作基准。  
> **标记说明：** `A`＝直接具有机械臂/手/接触执行器或直接研究其规划控制；`B`＝相关但较宽泛，如吊载、挂钩、协同、操作导向导航等。`预印本`表示在本次检索中未核实正式会议/期刊，不代表尚未被接收。优先以链接中的正式版本更新 BibTeX。

## 一、建议最先读的 12 篇（面向具身 UAV / VLA / 世界模型）

| 优先级 | 论文 | 为什么值得先读 |
|---|---|---|
| ★★★★★ | [Flying Hand](https://roboticsproceedings.org/rss21/p130.html) · RSS 2025 | 末端执行器中心的统一接口；真实遥操作、模仿学习、插孔、拾放和旋转操作 |
| ★★★★★ | [π, But Make It Fly / AirVLA](https://arxiv.org/abs/2603.25038) · 2026 | 把台面机械臂预训练 VLA 迁移到飞行平台，研究动力学鸿沟与载荷约束 |
| ★★★★★ | [AeroManip-VLA](https://arxiv.org/abs/2609.36915) · 2026 | RL 专家生成空中操作示范，含导航—抓取—放置长时任务与失败标注 |
| ★★★★★ | [AIR-VLA](https://proceedings.mlr.press/v306/sun26an.html) · ICML 2026 | 空中 VLA 基准、人工遥操作数据、多步指令和跨模型对比 |
| ★★★★★ | [AM-Bench](https://arxiv.org/abs/2609.00641) · 2026 | 12 类任务，系统比较飞行器结构、控制器、干扰与操作策略 |
| ★★★★★ | [Fly-by-Code](https://arxiv.org/abs/2610.12549) · 2026 | 具身代码 Agent 通过主动观察/探测修正空中操作失败 |
| ★★★★☆ | [Aerial Manipulation in the Wild](https://arxiv.org/abs/2609.30521) · 2026 | 机载定位 + Diffusion Policy + 整机 MPC，强调室外泛化 |
| ★★★★☆ | [AERMANI-PLACE](https://arxiv.org/abs/2606.14531) · 2026 | 语言指令映射至真实空间放置点，适合语言—几何—动作研究 |
| ★★★★☆ | [AERMANI-VLM](https://arxiv.org/abs/2511.01472) · 2025 | VLM 高层推理 + 安全技能库，不直接生成危险低层动作 |
| ★★★★☆ | [Whole-Body Integrated Motion Planning](https://arxiv.org/abs/2501.06493) · T-RO 2025 | 飞行器/机械臂联合规划、碰撞约束、可执行性与轨迹优化 |
| ★★★★☆ | [QuadHand](https://arxiv.org/abs/2609.35094) · IROS 2026 | 小型三自由度空中机械臂与整机碰撞距离场规划 |
| ★★★★☆ | [FlyingToolbox](https://www.nature.com/articles/s41586-025-09575-x) · Nature 2025 | 近距离上下堆叠的异构 UAV 协同空中工具交换 |

## 二、逐篇论文（研究论文 56 篇）

字段：**年份 / 论文 / 出处 / 方向 / 关键内容**。论文标题均指向 arXiv、出版方或作者官方论文页面；有 arXiv 的可将 `/abs/` 改为 `/pdf/` 下载全文。

### A. 2026 年：VLA、Agent、Benchmark、策略学习与真实操作（14 篇）

| # | 论文（原文链接） | 出处 | 标签 | 核心内容 |
|---:|---|---|:---:|---|
| 01 | [Fly-by-Code: Embodied Coding Agents for Aerial Manipulation with Active Visual and Physical Feedback](https://arxiv.org/abs/2610.12549) | arXiv, 2026-10 | A | 生成可执行操作程序；利用额外视角与物理探测诊断失败，并迁移到实机。 |
| 02 | [Benchmarking Interaction-Oriented Aerial Mobility across Heterogeneous Environments (CrossFly)](https://arxiv.org/abs/2610.18381) | arXiv, 2026-10 | B | 15K 轨迹与多种室内外场景，关注从导航转入物理交互的长时过程；不是纯机械臂基准。 |
| 03 | [AeroManip-VLA: Scalable Vision-Language-Action Learning for Aerial Manipulation with RL-Generated Demonstrations](https://arxiv.org/abs/2609.36915) | arXiv, 2026-09 | A | 大规模并行仿真，RL 专家与规则协同生成抓取、放置及导航—操作示范。 |
| 04 | [AM-Bench: A Modular Simulation Suite and Benchmark for Aerial Manipulation Policy Learning](https://arxiv.org/abs/2609.00641) | arXiv, 2026-09 | A | 覆盖欠驱动/全驱动/过驱动系统、12 个接触与搬运任务，并分析控制策略及风扰。 |
| 05 | [Aerial Manipulation in the Wild with Onboard Perception, Policy Learning, and Whole-Body Control](https://arxiv.org/abs/2609.30521) | arXiv, 2026-09；IROS 2026 workshop 版本 | A | 机载激光惯性里程计、示范学习和整机 MPC 配合，实现室外操作。 |
| 06 | [AERMANI-PLACE: Language Guided Object Placement with Aerial Manipulators](https://arxiv.org/abs/2606.14531) | arXiv, 2026-06 | A | 用图像编辑产生语言指定的放置标记，经深度恢复三维位置，实机验证。 |
| 07 | [$\pi$, But Make It Fly: Physics-Guided Transfer of VLA Models to Aerial Manipulation](https://arxiv.org/abs/2603.25038) | arXiv, 2026-03 | A | AirVLA：迁移预训练 VLA、载荷感知推理引导与 3DGS 数据扩充。 |
| 08 | [AIR-VLA: Vision-Language-Action Systems for Aerial Manipulation](https://proceedings.mlr.press/v306/sun26an.html) | **ICML 2026** | A | 空中操作 VLA 基准、3,000 条人工遥操作示范及语言/空间/长程规划评测。 |
| 09 | [Autonomous Aerial Manipulation via Contextual Contrastive Meta Reinforcement Learning](https://arxiv.org/abs/2606.08533) | arXiv, 2026-06 | B | Aco2：四旋翼挂钩自动取货、搬运、交付；对不同载荷动力学在线适应。 |
| 10 | [Learning High-Speed Aerial Grasping With a Simple Gripper](https://arxiv.org/abs/2603.05935) | arXiv, 2026-03 | A | 简单夹爪 + 学习策略，实现高速抓取与仿真到实机迁移。 |
| 11 | [An Aerial Manipulator for Perception-Driven Flower Targeting Toward Contactless Pollination in Vertical Farming](https://arxiv.org/abs/2605.06759) | arXiv, 2026-05 | A | RGB-D 花朵定位、MPPI 与轻量二自由度臂；聚焦末端对准，尚非完整授粉验证。 |
| 12 | [Physics-infused Learning for Aerial Manipulator in Winds and Near-Wall Environments](https://arxiv.org/abs/2603.07826) | **AIAA SciTech 2026** | A | 气动机理 + 学习残差，重点研究近墙和风扰下的末端接触跟踪。 |
| 13 | [Self-assembling Modular Aerial Robot for Versatile Aerial Tasks](https://arxiv.org/abs/2605.19431) | arXiv, 2026-05 | A | 多个可飞模块自组装为飞行机械臂，兼顾独立移动与组合操作。 |
| 14 | [Aerial Manipulation with Contact-Aware Onboard Perception and Hybrid Control](https://arxiv.org/abs/2602.08251) | **ICRA 2026** | A | 接触约束 VIO、视觉伺服与混合力/位控制，完全机载感知。 |

### B. 2026 年：本体设计、整机控制、接触操作（14 篇）

| # | 论文（原文链接） | 出处 | 标签 | 核心内容 |
|---:|---|---|:---:|---|
| 15 | [An Open MuJoCo Simulation Framework for a Quadrotor Carrying a Tendon-Driven Soft Continuum Arm](https://arxiv.org/abs/2610.15308) | arXiv, 2026-10 | A | 四旋翼与绳驱软体连续臂的耦合 MuJoCo 开源仿真。 |
| 16 | [QuadHand: A Compact Quadrotor Aerial Manipulator with MRC-SDF-Based Whole-Body Motion Planning](https://arxiv.org/abs/2609.35094) | **IROS 2026**（作者主页列出） | A | 3-DoF 机械臂、被动质心补偿及机器人中心 SDF 整机轨迹优化。 |
| 17 | [AeRSoM: An Aerial Rigid-Soft Integrated Manipulator for Contact-Rich Manipulation](https://arxiv.org/abs/2609.28044) | arXiv, 2026-09 | A | 刚柔耦合机械臂与可变刚度，验证插孔、旋拧、风机叶片接触等任务。 |
| 18 | [A Morphing Aerial Robot With Thruster-Integrated Flexible Continuum Links for Shape Adaptive Aerial Manipulation](https://arxiv.org/abs/2609.19328) | arXiv, 2026-09 | A | 推进器与柔性连续体集成，拓展可施加的末端力/力矩。 |
| 19 | [Safety-Critical Bilateral Teleoperation for Omnidirectional Aerial Manipulation Using Force-Sensorless Haptic Feedback](https://arxiv.org/abs/2608.21735) | **IROS 2026**（arXiv 注明已录用） | A | 全向飞行器双向遥操作、CBF 安全过滤与无力传感器触觉反馈。 |
| 20 | [Effector-Centric NMPC of Tiltable-Multirotors for Offset-Free Omnidirectional Aerial Manipulation](https://arxiv.org/abs/2608.17819) | arXiv, 2026-08 | A | 可倾转旋翼 6-DoF 力/力矩控制与末端 NMPC，验证阀门旋转。 |
| 21 | [FAM-DQ: A Dual-Quadrotor-Based Fully Actuated Aerial Manipulator for High-Torque Interaction](https://arxiv.org/abs/2608.13220) | arXiv, 2026-08 | A | 双四旋翼耦合本体，面向较大交互扭矩和拧螺丝。 |
| 22 | [Hybrid Impedance-Admittance Control with Multi-Link Aerial Robot for Contact-Rich Surface Sliding Task](https://arxiv.org/abs/2608.01800) | arXiv, 2026-08 | A | 关节导纳 + 推力阻抗的协同控制，在未知表面进行稳定滑动。 |
| 23 | [U-Joint CAAMS: Experimental Evaluation of a Universal-Joint Continuum Manipulator for Aerial Manipulation](https://arxiv.org/abs/2607.03321) | arXiv, 2026-07 | A | 万向节连续体臂，改善非目标平面的变形与末端定位稳定性。 |
| 24 | [Global End-Effector Pose Control of an Underactuated Aerial Manipulator via Reinforcement Learning](https://arxiv.org/abs/2512.21085) | **ICRA 2026**（2025-12 预印本） | A | 四旋翼 + 2-DoF 臂，通过 RL 控制全局 6-DoF 末端位姿。 |
| 25 | [Impact-Robust Posture Optimization for Aerial Manipulation](https://arxiv.org/abs/2602.13762) | **ICRA 2026** | A | 优化空中机械臂接触/冲击前姿态，改善冲击鲁棒性。 |
| 26 | [Tilt-X: Enabling Compliant Aerial Manipulation through a Tiltable-Extensible Continuum Manipulator](https://arxiv.org/abs/2602.23576) | **ICRA 2026** | A | 倾转 + 伸缩 + 连续体臂，扩大操作空间并分析旋翼下洗气流影响。 |
| 27 | [Hand-like autonomous flying robot for airborne grasping and interaction](https://www.nature.com/articles/s41467-026-68967-3) | **Nature Communications 2026** | A | HI-ARM 以类似手的紧凑结构执行抓取、开门、停栖与连续交互。 |
| 28 | [Aerial Manipulation: Contact, Medium Coupling, and the Geometry of Readiness](https://arxiv.org/abs/2607.04719) | arXiv, 2026-07；**观点/理论文章** | B | 从介质耦合、接触力与可操作性重新界定 aerial manipulation；非新硬件实验论文。 |

### C. 2025 年：整机规划、学习、协同与系统（18 篇）

| # | 论文（原文链接） | 出处 | 标签 | 核心内容 |
|---:|---|---|:---:|---|
| 29 | [UMI-on-Air: Embodiment-Aware Guidance for Embodiment-Agnostic Visuomotor Policies](https://arxiv.org/abs/2510.02614) | **ICRA 2026**（2025 预印本） | A | 扩散策略生成的轨迹接受飞行器低层控制代价引导，提升跨平台可执行性。 |
| 30 | [Integration of a Variable Stiffness Link for Long-Reach Aerial Manipulation](https://arxiv.org/abs/2510.15639) | arXiv, 2025-10 | A | 可调刚度长连杆连接无人机和双臂系统，权衡缓冲能力与末端精度。 |
| 31 | [Whole-body motion planning and safety-critical control for aerial manipulation](https://arxiv.org/abs/2511.02342) | arXiv, 2025-11 | A | Superquadric 几何建模、最小碰撞距离规划与高阶 CBF 安全约束。 |
| 32 | [AERMANI-VLM: Structured Prompting and Reasoning for Aerial Manipulation with Vision Language Models](https://arxiv.org/abs/2511.01472) | arXiv, 2025-11 | A | 结构化语言推理与预定义飞行安全技能，实现多步骤拾放。 |
| 33 | [Prespecified-Performance Kinematic Tracking Control for Aerial Manipulation](https://arxiv.org/abs/2509.10065) | arXiv, 2025-09 | A | 末端运动学跟踪，显式设计误差收敛与预设性能边界。 |
| 34 | [Autonomous Aerial Manipulation at Arbitrary Pose in SE(3) with Robust Control and Whole-body Planning](https://arxiv.org/abs/2508.19608) | arXiv, 2025-08 | A | 全向空中机械臂可在任意机身姿态工作，联合几何鲁棒控制和规划。 |
| 35 | [Decentralized Aerial Manipulation of a Cable-Suspended Load Using Multi-Agent Reinforcement Learning](https://proceedings.mlr.press/v305/zeng25a.html) | **CoRL 2025** | B | 多机无需通信、使用去中心化 RL 控制吊载 6-DoF 操作。 |
| 36 | [Multi-robot Aerial Soft Manipulator For Floating Litter Collection](https://arxiv.org/abs/2507.03517) | arXiv, 2025-07 | B | 双机与绳索组成柔性抓取结构，用于漂浮垃圾回收。 |
| 37 | [Aerial Grasping via Maximizing Delta-Arm Workspace Utilization](https://arxiv.org/abs/2506.15539) | arXiv, 2025-06 | A | 学习 Delta 臂的可达空间和正运动学近似，用于抓取轨迹优化。 |
| 38 | [Flying Hand: End-Effector-Centric Framework for Versatile Aerial Manipulation Teleoperation and Policy Learning](https://roboticsproceedings.org/rss21/p130.html) | **RSS 2025** | A | 全驱动六旋翼 + 4-DoF 臂；统一末端控制、遥操作、模仿学习。 |
| 39 | [Agile and Cooperative Aerial Manipulation of a Cable-Suspended Load](https://arxiv.org/abs/2501.18802) | arXiv, 2025-01 | B | 多机对共同吊载进行敏捷运输/操作，研究动力学与协调控制。 |
| 40 | [NDOB-Based Control of a UAV with Delta-Arm Considering Manipulator Dynamics](https://arxiv.org/abs/2501.06122) | arXiv, 2025-01 | A | 非线性扰动观测器处理飞行器与 Delta 臂的强耦合。 |
| 41 | [Whole-Body Integrated Motion Planning for Aerial Manipulators](https://arxiv.org/abs/2501.06493) | **IEEE Transactions on Robotics 2025** | A | 可变碰撞几何、整机轨迹联合优化；[代码](https://github.com/SYSU-HILAB/am-planner)。 |
| 42 | [Safety-Critical Control for Aerial Physical Interaction in Uncertain Environment](https://arxiv.org/abs/2501.16719) | **ICRA 2025** | A | 扰动观测与安全关键控制，使全驱动空中机械臂与静态/动态结构接触。 |
| 43 | [Reliable Aerial Manipulation: Combining Visual Tracking with Range Sensing for Robust Grasping](https://www.research-collection.ethz.ch/entities/publication/0f64ad6f-5ed2-4289-a365-6bb7c48ae182) | **ICRA 2025** | A | 视觉追踪联合 1D ToF 测距，解决目标脱离相机视野时的抓取定位。 |
| 44 | [An Open-Source Soft Robotic Platform for Autonomous Aerial Manipulation in the Wild](https://proceedings.mlr.press/v270/bauer25a.html) | **CoRL 2024 / PMLR 2025** | A | 机载感知、软夹爪、室内外自主抓取；开源 ROS 2 软件和硬件。 |
| 45 | [Proximal cooperative aerial manipulation with vertically stacked drones](https://www.nature.com/articles/s41586-025-09575-x) | **Nature 2025** | A | FlyingToolbox：垂直堆叠的异构机器人近距离交换工具与执行任务。 |
| 46 | [Development of an Aerial Manipulation System Using Onboard Cameras and a Multi-Fingered Robotic Hand with Proximity Sensors](https://www.mdpi.com/1424-8220/25/2/470) | **Sensors 2025** | A | 机载双相机 + 近距感知多指手，完成物体定位与抓取。 |

### D. 2024 年：高价值硬件、感知与力控（8 篇）

| # | 论文（原文链接） | 出处 | 标签 | 核心内容 |
|---:|---|---|:---:|---|
| 47 | [High-speed aerial grasping using a soft drone with onboard perception](https://www.nature.com/articles/s44182-024-00012-1) | **npj Robotics 2024** | A | 机载视觉配合柔性抓取系统，强调速度和真实环境适用性。 |
| 48 | [Design of a Flexible Robot Arm for Safe Aerial Physical Interaction](https://arxiv.org/abs/2410.15797) | arXiv, 2024-10 | A | 轻量柔顺机械臂、弹性耗能与飞行接触实验。 |
| 49 | [Avian-Inspired High-Precision Tracking Control for Aerial Manipulators](https://arxiv.org/abs/2411.10966) | arXiv, 2024-11 | A | 仿鸟形机械臂设计、耦合动力学与高精度跟踪控制。 |
| 50 | [Hook-Based Aerial Payload Grasping from a Moving Platform](https://arxiv.org/abs/2409.11788) | arXiv, 2024-09 | B | UAV 挂钩从运动平台抓取载荷，优化接触/抓取时机。 |
| 51 | [Aerial Interaction with Tactile Sensing](https://ieeexplore.ieee.org/document/10611282/) | **ICRA 2024** | A | 全驱动飞行器结合视觉式触觉传感开展动态接触。 |
| 52 | [A Compact Aerial Manipulator: Design and Control for Dexterous Operations](https://link.springer.com/article/10.1007/s10846-024-02090-7) | **Journal of Intelligent & Robotic Systems 2024** | A | 紧凑型机械臂机体集成和灵巧操作控制。 |
| 53 | [An Ultra-Light, Ultra-Fast, Passive Closing Aerial Gripping System Capable of Grasping, Perching, and Aerial Manipulation](https://ieeexplore.ieee.org/document/10770047/) | **SSRR 2024** | A | 快速被动闭合夹爪，支持抓取、停栖等操作。 |
| 54 | [Design, Localization, Perception, and Control for GPS-Denied Autonomous Aerial Grasping and Harvesting](https://doi.org/10.1109/LRA.2024.3366015) | **IEEE RA-L 2024** | A | Drone-Bee：无 GPS 环境中的感知、定位、控制及果实抓取。 |

**数量核对：**以上 A–D 四组共 **54 篇不重复论文**；下方补充 4 篇，共 **58 篇**。不将综述计入。

### E. 补充 4 篇独立研究论文（2024–2025）

| # | 论文（原文链接） | 出处 | 标签 | 核心内容 |
|---:|---|---|:---:|---|
| 55 | [Aerial Manipulator With a Laterally Extendable Scissor Mechanism for Both Extension and Automatic Moment Compensation Using a Single Actuator](https://doi.org/10.1007/s12555-024-0483-2) | **International Journal of Control, Automation, and Systems 2025** | A | 剪叉伸缩与单执行器自动力矩补偿。 |
| 56 | [Observer-Based Nonlinear Control for Dual-Arm Aerial Manipulator Systems Suffering From Uncertain Center of Mass](https://ieeexplore.ieee.org/document/10466505/) | **IEEE 期刊 2024** | A | 双臂空中机械臂的质心不确定性、观测器和稳定控制。 |
| 57 | [Servo Integrated Nonlinear Model Predictive Control for Overactuated Tiltable-Quadrotors](https://ieeexplore.ieee.org/document/10659124/) | **IEEE RA-L 2024** | B | 可倾转全驱动四旋翼的 NMPC，为 6-DoF 空中末端操作提供运动控制基础。 |
| 58 | [Finite-Time Fast Adaptive Backstepping Attitude Control for Aerial Manipulators Based on Variable Coupling Disturbance Compensation](https://ieeexplore.ieee.org/abstract/document/10505853) | **IEEE TIE 2024** | A | 耦合扰动补偿与有限时间姿态控制。 |

> **最终口径：58 篇独立研究论文/观点文章**。本文涵盖公开可检索的代表性工作，不能保证全世界所有 2024–2026 论文的数学意义上的穷尽；特别是 2026 年新论文可能继续更新。每篇均配有检索到的原始论文页面/出版页。

## 三、补充综述与路线图（不计入上面 58 篇）

1. [From aerial transportation to aerial interaction: A review](https://www.sciencedirect.com/science/article/pii/S1000936126003808) — 2026，着眼从运输到接触交互的演进。
2. [A Review of Real-Time Implementable Cooperative Aerial Manipulation Systems](https://www.mdpi.com/2504-446X/8/5/196) — *Drones*, 2024，多 UAV 协同操作、建模与实时控制。
3. [Past, Present, and Future of Aerial Robotic Manipulators](https://doi.org/10.1109/TRO.2021.3084395) — *IEEE T-RO*, 2022，领域经典路线图；不属于“最近”，但适合写引言。
4. [Survey on Aerial Manipulator: System, Modeling, and Control](https://www.cambridge.org/core/journals/robotica/article/survey-on-aerial-manipulator-system-modeling-and-control/5FDD2404D65EF73477CF10CA62B69720) — *Robotica*, 2020，按系统、模型与控制梳理基础。

## 四、对你的 PanoUAV-E / 空中 VLA 研究最有价值的切入点

**研究问题 1：从“看见/追踪目标”到“接近—抓取—搬运—放置”。**  
可以把 PanoUAV-E 的跟踪与目标获取能力向物理交互扩展；参考 **CrossFly (#02)** 的跨场景长时移动、**AeroManip-VLA (#03)** 的策略示范、**AIR-VLA (#08)** 的语言任务，以及 **Flying Hand (#38)** 的末端接口。核心评测应分开报告目标获取、接近定位、接触成功、操作完成与飞行安全，避免只用单一 SR 混淆感知和控制。

**研究问题 2：VLA 在飞行平台上为什么失效？**  
可综合 **AirVLA (#07)** 的载荷动力学、**UMI-on-Air (#29)** 的控制器可执行性引导、**AM-Bench (#04)** 的机体/控制/任务因素分析，构造 **perception × control × embodiment** 的系统性分解实验。

**研究问题 3：只用机载感知，如何实现接触操作？**  
对照 **Aerial Manipulation in the Wild (#05)**、**Contact-Aware Perception (#14)**、**Reliable Aerial Manipulation (#43)**。关键因素包括遮挡、视野脱离、接触期的状态估计漂移、末端力控制，以及风/下洗扰动。

**研究问题 4：将操作评测拓展至全景视角会怎样？**  
这是可探索的方向，而非已有上述论文的实证结论。可以设计固定机头与可转向两种飞行基线；控制机械臂自由度、任务距离、目标起始方位；比较 360° 感知对非前向目标发现和长期追踪的帮助，以及 ERP 视觉畸变对末端精定位的影响。

## 五、相关代码 / 项目 / 正式出版入口

- Flying Hand (RSS 2025)：[论文](https://roboticsproceedings.org/rss21/p130.html) · [项目](https://lecar-lab.github.io/flying_hand/)
- Whole-Body Integrated Motion Planning (T-RO 2025)：[论文](https://arxiv.org/abs/2501.06493) · [代码](https://github.com/SYSU-HILAB/am-planner)
- AirVLA：[$\pi$, But Make It Fly](https://arxiv.org/abs/2603.25038) · [项目](https://airvla.github.io/)
- AIR-VLA (ICML 2026)：[正式论文](https://proceedings.mlr.press/v306/sun26an.html)
- Soft aerial manipulation (CoRL)：[正式论文](https://proceedings.mlr.press/v270/bauer25a.html)
- Multi-agent cable-suspended (CoRL 2025)：[正式论文](https://proceedings.mlr.press/v305/zeng25a.html)
- FlyingToolbox (Nature 2025)：[正式论文](https://www.nature.com/articles/s41586-025-09575-x)

## 六、补检关键词和可复现的检索入口

建议持续按以下组合补检（会议新论文、在线优先发表、同一论文换题名尤其容易漏）：

```text
"aerial manipulation" OR "aerial manipulator" OR "flying manipulator"
"aerial grasping" OR "aerial physical interaction" OR "aerial contact manipulation"
"aerial manipulation" AND ("vision-language-action" OR "diffusion policy" OR "reinforcement learning")
"aerial manipulator" AND ("whole-body" OR "model predictive control" OR "continuum arm")
"cooperative aerial manipulation" OR "cable suspended load" OR "aerial teleoperation"
```

检索对象：[arXiv Robotics](https://arxiv.org/list/cs.RO/recent) · [RSS](https://roboticsproceedings.org/) · [CoRL/PMLR](https://proceedings.mlr.press/) · [IEEE Xplore](https://ieeexplore.ieee.org/) · [Nature](https://www.nature.com/)；本文件并不包含 PDF 文件本身，只整理可以点击的论文入口。

