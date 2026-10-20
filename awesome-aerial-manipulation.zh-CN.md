# Awesome Aerial Manipulation · 空中机械臂论文精选

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

**语言：** [English](awesome-aerial-manipulation.md) | 简体中文

> **持续整理空中机械臂（Aerial Manipulation）领域的代表性论文、研究基准、开源项目与学习资源。** 从飞行机械臂和高速抓取，到接触交互、协同操作以及视觉—语言—动作模型。

**最后更新：** 2026 年 10 月 19 日 · **58 篇研究论文及观点文章** · **4 篇综述与路线图**

空中操作使无人机从被动的“空中眼睛”进一步发展为能够抓取、推动、旋拧和接触环境的“空中双手”。本清单关注 **空中机器人、灵巧操作、具身智能、视觉感知、运动规划与控制** 的交叉研究。

主要收录 **2024–2026 年** 的公开工作，并补充少量经典综述。部分论文属于空中挂钩、吊载、多机协作和面向交互的飞行等紧密相关方向，不一定使用传统多关节机械臂。

**标签说明：** `核心` 代表直接研究空中机械臂、飞行抓取器或物理交互/控制的工作；`相关` 代表支撑性或拓展性研究。标记为 arXiv 仅说明提供预印本入口，不意味着论文一定未被会议或期刊接收。

## 目录

- [优先阅读](#优先阅读)
- [论文分类](#论文分类)
  - [视觉—语言—动作、智能体与机器人学习](#视觉语言动作智能体与机器人学习)
  - [感知、空中抓取与自主交互](#感知空中抓取与自主交互)
  - [整机规划、控制与接触交互](#整机规划控制与接触交互)
  - [机器人本体、机构设计与柔性操作](#机器人本体机构设计与柔性操作)
  - [协同空中操作与相关基准](#协同空中操作与相关基准)
- [综述与路线图](#综述与路线图)
- [项目与开源代码](#项目与开源代码)
- [值得探索的研究问题](#值得探索的研究问题)
- [收录范围与维护说明](#收录范围与维护说明)

## 优先阅读

以下 12 篇适合作为 **空中具身操作、VLA 与学习型机器人系统** 的入门主线。推荐顺序基于阅读价值与方向关联，并不代表论文质量排名。

| 论文 | 发表信息 | 推荐理由 |
|---|---|---|
| [**Flying Hand**](https://roboticsproceedings.org/rss21/p130.html) | RSS 2025 | 末端执行器中心的统一接口；真实遥操作、模仿学习、插孔、拾放和旋转操作 |
| [**π, But Make It Fly / AirVLA**](https://arxiv.org/abs/2603.25038) | 2026 | 把台面机械臂预训练 VLA 迁移到飞行平台，研究动力学鸿沟与载荷约束 |
| [**AeroManip-VLA**](https://arxiv.org/abs/2609.36915) | 2026 | RL 专家生成空中操作示范，含导航—抓取—放置长时任务与失败标注 |
| [**AIR-VLA**](https://proceedings.mlr.press/v306/sun26an.html) | ICML 2026 | 空中 VLA 基准、人工遥操作数据、多步指令和跨模型对比 |
| [**AM-Bench**](https://arxiv.org/abs/2609.00641) | 2026 | 12 类任务，系统比较飞行器结构、控制器、干扰与操作策略 |
| [**Fly-by-Code**](https://arxiv.org/abs/2610.12549) | 2026 | 具身代码 Agent 通过主动观察/探测修正空中操作失败 |
| [**Aerial Manipulation in the Wild**](https://arxiv.org/abs/2609.30521) | 2026 | 机载定位 + Diffusion Policy + 整机 MPC，强调室外泛化 |
| [**AERMANI-PLACE**](https://arxiv.org/abs/2606.14531) | 2026 | 语言指令映射至真实空间放置点，适合语言—几何—动作研究 |
| [**AERMANI-VLM**](https://arxiv.org/abs/2511.01472) | 2025 | VLM 高层推理 + 安全技能库，不直接生成危险低层动作 |
| [**Whole-Body Integrated Motion Planning**](https://arxiv.org/abs/2501.06493) | T-RO 2025 | 飞行器/机械臂联合规划、碰撞约束、可执行性与轨迹优化 |
| [**QuadHand**](https://arxiv.org/abs/2609.35094) | IROS 2026 | 小型三自由度空中机械臂与整机碰撞距离场规划 |
| [**FlyingToolbox**](https://www.nature.com/articles/s41586-025-09575-x) | Nature 2025 | 近距离上下堆叠的异构 UAV 协同空中工具交换 |

## 论文分类

**按研究主题整理，而非严格按年份排序。** 每篇论文只在下面的主列表中出现一次，概要侧重其主要创新点。

### 视觉—语言—动作、智能体与机器人学习

- **[Fly-by-Code: Embodied Coding Agents for Aerial Manipulation with Active Visual and Physical Feedback](https://arxiv.org/abs/2610.12549)** — *arXiv, 2026* · `核心`  
  生成可执行操作程序；利用额外视角与物理探测诊断失败，并迁移到实机。
- **[AeroManip-VLA: Scalable Vision-Language-Action Learning for Aerial Manipulation with RL-Generated Demonstrations](https://arxiv.org/abs/2609.36915)** — *arXiv, 2026* · `核心`  
  大规模并行仿真，RL 专家与规则协同生成抓取、放置及导航—操作示范。
- **[AM-Bench: A Modular Simulation Suite and Benchmark for Aerial Manipulation Policy Learning](https://arxiv.org/abs/2609.00641)** — *arXiv, 2026* · `核心`  
  覆盖欠驱动/全驱动/过驱动系统、12 个接触与搬运任务，并分析控制策略及风扰。
- **[Aerial Manipulation in the Wild with Onboard Perception, Policy Learning, and Whole-Body Control](https://arxiv.org/abs/2609.30521)** — *arXiv, 2026* · `核心`  
  机载激光惯性里程计、示范学习和整机 MPC 配合，实现室外操作。
- **[AERMANI-PLACE: Language Guided Object Placement with Aerial Manipulators](https://arxiv.org/abs/2606.14531)** — *arXiv, 2026* · `核心`  
  用图像编辑产生语言指定的放置标记，经深度恢复三维位置，实机验证。
- **[π, But Make It Fly: Physics-Guided Transfer of VLA Models to Aerial Manipulation](https://arxiv.org/abs/2603.25038)** — *arXiv, 2026* · `核心`  
  AirVLA：迁移预训练 VLA、载荷感知推理引导与 3DGS 数据扩充。
- **[AIR-VLA: Vision-Language-Action Systems for Aerial Manipulation](https://proceedings.mlr.press/v306/sun26an.html)** — *ICML, 2026* · `核心`  
  空中操作 VLA 基准、3,000 条人工遥操作示范及语言/空间/长程规划评测。
- **[Autonomous Aerial Manipulation via Contextual Contrastive Meta Reinforcement Learning](https://arxiv.org/abs/2606.08533)** — *arXiv, 2026* · `相关`  
  Aco2：四旋翼挂钩自动取货、搬运、交付；对不同载荷动力学在线适应。
- **[UMI-on-Air: Embodiment-Aware Guidance for Embodiment-Agnostic Visuomotor Policies](https://arxiv.org/abs/2510.02614)** — *ICRA 2026; preprint 2025* · `核心`  
  扩散策略生成的轨迹接受飞行器低层控制代价引导，提升跨平台可执行性。
- **[AERMANI-VLM: Structured Prompting and Reasoning for Aerial Manipulation with Vision Language Models](https://arxiv.org/abs/2511.01472)** — *arXiv, 2025* · `核心`  
  结构化语言推理与预定义飞行安全技能，实现多步骤拾放。

### 感知、空中抓取与自主交互

- **[Learning High-Speed Aerial Grasping With a Simple Gripper](https://arxiv.org/abs/2603.05935)** — *arXiv, 2026* · `核心`  
  简单夹爪 + 学习策略，实现高速抓取与仿真到实机迁移。
- **[An Aerial Manipulator for Perception-Driven Flower Targeting Toward Contactless Pollination in Vertical Farming](https://arxiv.org/abs/2605.06759)** — *arXiv, 2026* · `核心`  
  RGB-D 花朵定位、MPPI 与轻量二自由度臂；聚焦末端对准，尚非完整授粉验证。
- **[Aerial Manipulation with Contact-Aware Onboard Perception and Hybrid Control](https://arxiv.org/abs/2602.08251)** — *ICRA, 2026* · `核心`  
  接触约束 VIO、视觉伺服与混合力/位控制，完全机载感知。
- **[Aerial Grasping via Maximizing Delta-Arm Workspace Utilization](https://arxiv.org/abs/2506.15539)** — *arXiv, 2025* · `核心`  
  学习 Delta 臂的可达空间和正运动学近似，用于抓取轨迹优化。
- **[Reliable Aerial Manipulation: Combining Visual Tracking with Range Sensing for Robust Grasping](https://www.research-collection.ethz.ch/entities/publication/0f64ad6f-5ed2-4289-a365-6bb7c48ae182)** — *ICRA, 2025* · `核心`  
  视觉追踪联合 1D ToF 测距，解决目标脱离相机视野时的抓取定位。
- **[An Open-Source Soft Robotic Platform for Autonomous Aerial Manipulation in the Wild](https://proceedings.mlr.press/v270/bauer25a.html)** — *CoRL 2024 / PMLR 2025* · `核心`  
  机载感知、软夹爪、室内外自主抓取；开源 ROS 2 软件和硬件。
- **[Development of an Aerial Manipulation System Using Onboard Cameras and a Multi-Fingered Robotic Hand with Proximity Sensors](https://www.mdpi.com/1424-8220/25/2/470)** — *Sensors, 2025* · `核心`  
  机载双相机 + 近距感知多指手，完成物体定位与抓取。
- **[High-speed aerial grasping using a soft drone with onboard perception](https://www.nature.com/articles/s44182-024-00012-1)** — *npj Robotics, 2024* · `核心`  
  机载视觉配合柔性抓取系统，强调速度和真实环境适用性。
- **[Hook-Based Aerial Payload Grasping from a Moving Platform](https://arxiv.org/abs/2409.11788)** — *arXiv, 2024* · `相关`  
  UAV 挂钩从运动平台抓取载荷，优化接触/抓取时机。
- **[Aerial Interaction with Tactile Sensing](https://ieeexplore.ieee.org/document/10611282/)** — *ICRA, 2024* · `核心`  
  全驱动飞行器结合视觉式触觉传感开展动态接触。
- **[An Ultra-Light, Ultra-Fast, Passive Closing Aerial Gripping System Capable of Grasping, Perching, and Aerial Manipulation](https://ieeexplore.ieee.org/document/10770047/)** — *SSRR, 2024* · `核心`  
  快速被动闭合夹爪，支持抓取、停栖等操作。
- **[Design, Localization, Perception, and Control for GPS-Denied Autonomous Aerial Grasping and Harvesting](https://doi.org/10.1109/LRA.2024.3366015)** — *IEEE RA-L, 2024* · `核心`  
  Drone-Bee：无 GPS 环境中的感知、定位、控制及果实抓取。

### 整机规划、控制与接触交互

- **[Physics-infused Learning for Aerial Manipulator in Winds and Near-Wall Environments](https://arxiv.org/abs/2603.07826)** — *AIAA SciTech, 2026* · `核心`  
  气动机理 + 学习残差，重点研究近墙和风扰下的末端接触跟踪。
- **[Safety-Critical Bilateral Teleoperation for Omnidirectional Aerial Manipulation Using Force-Sensorless Haptic Feedback](https://arxiv.org/abs/2608.21735)** — *IROS, 2026* · `核心`  
  全向飞行器双向遥操作、CBF 安全过滤与无力传感器触觉反馈。
- **[Effector-Centric NMPC of Tiltable-Multirotors for Offset-Free Omnidirectional Aerial Manipulation](https://arxiv.org/abs/2608.17819)** — *arXiv, 2026* · `核心`  
  可倾转旋翼 6-DoF 力/力矩控制与末端 NMPC，验证阀门旋转。
- **[FAM-DQ: A Dual-Quadrotor-Based Fully Actuated Aerial Manipulator for High-Torque Interaction](https://arxiv.org/abs/2608.13220)** — *arXiv, 2026* · `核心`  
  双四旋翼耦合本体，面向较大交互扭矩和拧螺丝。
- **[Hybrid Impedance-Admittance Control with Multi-Link Aerial Robot for Contact-Rich Surface Sliding Task](https://arxiv.org/abs/2608.01800)** — *arXiv, 2026* · `核心`  
  关节导纳 + 推力阻抗的协同控制，在未知表面进行稳定滑动。
- **[Global End-Effector Pose Control of an Underactuated Aerial Manipulator via Reinforcement Learning](https://arxiv.org/abs/2512.21085)** — *ICRA, 2026; preprint 2025* · `核心`  
  四旋翼 + 2-DoF 臂，通过 RL 控制全局 6-DoF 末端位姿。
- **[Impact-Robust Posture Optimization for Aerial Manipulation](https://arxiv.org/abs/2602.13762)** — *ICRA, 2026* · `核心`  
  优化空中机械臂接触/冲击前姿态，改善冲击鲁棒性。
- **[Whole-body motion planning and safety-critical control for aerial manipulation](https://arxiv.org/abs/2511.02342)** — *arXiv, 2025* · `核心`  
  Superquadric 几何建模、最小碰撞距离规划与高阶 CBF 安全约束。
- **[Prespecified-Performance Kinematic Tracking Control for Aerial Manipulation](https://arxiv.org/abs/2509.10065)** — *arXiv, 2025* · `核心`  
  末端运动学跟踪，显式设计误差收敛与预设性能边界。
- **[Autonomous Aerial Manipulation at Arbitrary Pose in SE(3) with Robust Control and Whole-body Planning](https://arxiv.org/abs/2508.19608)** — *arXiv, 2025* · `核心`  
  全向空中机械臂可在任意机身姿态工作，联合几何鲁棒控制和规划。
- **[Flying Hand: End-Effector-Centric Framework for Versatile Aerial Manipulation Teleoperation and Policy Learning](https://roboticsproceedings.org/rss21/p130.html)** — *RSS, 2025* · `核心`  
  全驱动六旋翼 + 4-DoF 臂；统一末端控制、遥操作、模仿学习。
- **[NDOB-Based Control of a UAV with Delta-Arm Considering Manipulator Dynamics](https://arxiv.org/abs/2501.06122)** — *arXiv, 2025* · `核心`  
  非线性扰动观测器处理飞行器与 Delta 臂的强耦合。
- **[Whole-Body Integrated Motion Planning for Aerial Manipulators](https://arxiv.org/abs/2501.06493)** — *IEEE T-RO, 2025* · `核心`  
  可变碰撞几何、整机轨迹联合优化；[代码](https://github.com/SYSU-HILAB/am-planner)。
- **[Safety-Critical Control for Aerial Physical Interaction in Uncertain Environment](https://arxiv.org/abs/2501.16719)** — *ICRA, 2025* · `核心`  
  扰动观测与安全关键控制，使全驱动空中机械臂与静态/动态结构接触。
- **[Design of a Flexible Robot Arm for Safe Aerial Physical Interaction](https://arxiv.org/abs/2410.15797)** — *arXiv, 2024* · `核心`  
  轻量柔顺机械臂、弹性耗能与飞行接触实验。
- **[A Compact Aerial Manipulator: Design and Control for Dexterous Operations](https://link.springer.com/article/10.1007/s10846-024-02090-7)** — *Journal of Intelligent & Robotic Systems, 2024* · `核心`  
  紧凑型机械臂机体集成和灵巧操作控制。
- **[Observer-Based Nonlinear Control for Dual-Arm Aerial Manipulator Systems Suffering From Uncertain Center of Mass](https://ieeexplore.ieee.org/document/10466505/)** — *IEEE journal, 2024* · `核心`  
  双臂空中机械臂的质心不确定性、观测器和稳定控制。
- **[Servo Integrated Nonlinear Model Predictive Control for Overactuated Tiltable-Quadrotors](https://ieeexplore.ieee.org/document/10659124/)** — *IEEE RA-L, 2024* · `相关`  
  可倾转全驱动四旋翼的 NMPC，为 6-DoF 空中末端操作提供运动控制基础。
- **[Finite-Time Fast Adaptive Backstepping Attitude Control for Aerial Manipulators Based on Variable Coupling Disturbance Compensation](https://ieeexplore.ieee.org/abstract/document/10505853)** — *IEEE TIE, 2024* · `核心`  
  耦合扰动补偿与有限时间姿态控制。

### 机器人本体、机构设计与柔性操作

- **[Self-assembling Modular Aerial Robot for Versatile Aerial Tasks](https://arxiv.org/abs/2605.19431)** — *arXiv, 2026* · `核心`  
  多个可飞模块自组装为飞行机械臂，兼顾独立移动与组合操作。
- **[An Open MuJoCo Simulation Framework for a Quadrotor Carrying a Tendon-Driven Soft Continuum Arm](https://arxiv.org/abs/2610.15308)** — *arXiv, 2026* · `核心`  
  四旋翼与绳驱软体连续臂的耦合 MuJoCo 开源仿真。
- **[QuadHand: A Compact Quadrotor Aerial Manipulator with MRC-SDF-Based Whole-Body Motion Planning](https://arxiv.org/abs/2609.35094)** — *IROS, 2026* · `核心`  
  3-DoF 机械臂、被动质心补偿及机器人中心 SDF 整机轨迹优化。
- **[AeRSoM: An Aerial Rigid-Soft Integrated Manipulator for Contact-Rich Manipulation](https://arxiv.org/abs/2609.28044)** — *arXiv, 2026* · `核心`  
  刚柔耦合机械臂与可变刚度，验证插孔、旋拧、风机叶片接触等任务。
- **[A Morphing Aerial Robot With Thruster-Integrated Flexible Continuum Links for Shape Adaptive Aerial Manipulation](https://arxiv.org/abs/2609.19328)** — *arXiv, 2026* · `核心`  
  推进器与柔性连续体集成，拓展可施加的末端力/力矩。
- **[U-Joint CAAMS: Experimental Evaluation of a Universal-Joint Continuum Manipulator for Aerial Manipulation](https://arxiv.org/abs/2607.03321)** — *arXiv, 2026* · `核心`  
  万向节连续体臂，改善非目标平面的变形与末端定位稳定性。
- **[Tilt-X: Enabling Compliant Aerial Manipulation through a Tiltable-Extensible Continuum Manipulator](https://arxiv.org/abs/2602.23576)** — *ICRA, 2026* · `核心`  
  倾转 + 伸缩 + 连续体臂，扩大操作空间并分析旋翼下洗气流影响。
- **[Hand-like autonomous flying robot for airborne grasping and interaction](https://www.nature.com/articles/s41467-026-68967-3)** — *Nature Communications, 2026* · `核心`  
  HI-ARM 以类似手的紧凑结构执行抓取、开门、停栖与连续交互。
- **[Integration of a Variable Stiffness Link for Long-Reach Aerial Manipulation](https://arxiv.org/abs/2510.15639)** — *arXiv, 2025* · `核心`  
  可调刚度长连杆连接无人机和双臂系统，权衡缓冲能力与末端精度。
- **[Avian-Inspired High-Precision Tracking Control for Aerial Manipulators](https://arxiv.org/abs/2411.10966)** — *arXiv, 2024* · `核心`  
  仿鸟形机械臂设计、耦合动力学与高精度跟踪控制。
- **[Aerial Manipulator With a Laterally Extendable Scissor Mechanism for Both Extension and Automatic Moment Compensation Using a Single Actuator](https://doi.org/10.1007/s12555-024-0483-2)** — *International Journal of Control, Automation, and Systems, 2025* · `核心`  
  剪叉伸缩与单执行器自动力矩补偿。

### 协同空中操作与相关基准

- **[Benchmarking Interaction-Oriented Aerial Mobility across Heterogeneous Environments (CrossFly)](https://arxiv.org/abs/2610.18381)** — *arXiv, 2026* · `相关`  
  15K 轨迹与多种室内外场景，关注从导航转入物理交互的长时过程；不是纯机械臂基准。
- **[Aerial Manipulation: Contact, Medium Coupling, and the Geometry of Readiness](https://arxiv.org/abs/2607.04719)** — *arXiv perspective, 2026* · `相关`  
  从介质耦合、接触力与可操作性重新界定 aerial manipulation；非新硬件实验论文。
- **[Decentralized Aerial Manipulation of a Cable-Suspended Load Using Multi-Agent Reinforcement Learning](https://proceedings.mlr.press/v305/zeng25a.html)** — *CoRL, 2025* · `相关`  
  多机无需通信、使用去中心化 RL 控制吊载 6-DoF 操作。
- **[Multi-robot Aerial Soft Manipulator For Floating Litter Collection](https://arxiv.org/abs/2507.03517)** — *arXiv, 2025* · `相关`  
  双机与绳索组成柔性抓取结构，用于漂浮垃圾回收。
- **[Agile and Cooperative Aerial Manipulation of a Cable-Suspended Load](https://arxiv.org/abs/2501.18802)** — *arXiv, 2025* · `相关`  
  多机对共同吊载进行敏捷运输/操作，研究动力学与协调控制。
- **[Proximal cooperative aerial manipulation with vertically stacked drones](https://www.nature.com/articles/s41586-025-09575-x)** — *Nature, 2025* · `核心`  
  FlyingToolbox：垂直堆叠的异构机器人近距离交换工具与执行任务。

## 综述与路线图

适合系统理解领域发展、空中操作系统建模以及尚待解决的问题。

1. **[From aerial transportation to aerial interaction: A review](https://www.sciencedirect.com/science/article/pii/S1000936126003808)** — *2026*。梳理从空中运输到主动接触交互的研究演进。
2. **[A Review of Real-Time Implementable Cooperative Aerial Manipulation Systems](https://www.mdpi.com/2504-446X/8/5/196)** — *Drones, 2024*。聚焦协同操作系统、动力学模型与实时控制。
3. **[Past, Present, and Future of Aerial Robotic Manipulators](https://doi.org/10.1109/TRO.2021.3084395)** — *IEEE T-RO, 2022*。空中机械臂系统形态与物理交互的重要经典综述。
4. **[Survey on Aerial Manipulator: System, Modeling, and Control](https://www.cambridge.org/core/journals/robotica/article/survey-on-aerial-manipulator-system-modeling-and-control/5FDD2404D65EF73477CF10CA62B69720)** — *Robotica, 2020*。系统总结空中机械臂的机构、动力学和控制方法。

## 项目与开源代码

| 项目 | 论文出处 | 资源 |
|---|---|---|
| **Flying Hand** | RSS 2025 | [论文](https://roboticsproceedings.org/rss21/p130.html) · [项目主页](https://lecar-lab.github.io/flying_hand/) |
| **AM-Planner** | IEEE T-RO 2025 | [论文](https://arxiv.org/abs/2501.06493) · [GitHub](https://github.com/SYSU-HILAB/am-planner) |
| **AirVLA** | arXiv 2026 | [论文](https://arxiv.org/abs/2603.25038) · [项目主页](https://airvla.github.io/) |
| **AIR-VLA** | ICML 2026 | [会议论文](https://proceedings.mlr.press/v306/sun26an.html) |
| **开源软体空中操作平台** | CoRL 2024 | [会议论文](https://proceedings.mlr.press/v270/bauer25a.html) |
| **去中心化吊载操作** | CoRL 2025 | [会议论文](https://proceedings.mlr.press/v305/zeng25a.html) |
| **FlyingToolbox** | Nature 2025 | [出版页面](https://www.nature.com/articles/s41586-025-09575-x) |

> 提供论文或项目页面链接，并不代表相应代码、模型权重或数据集已经公开；请以项目当前发布状态为准。

## 值得探索的研究问题

1. **从感知走向物理交互：** 如何让无人机连续完成目标发现、接近、抓取、运输与放置？建议分别衡量各阶段成功率、飞行安全和失败恢复能力。
2. **可迁移的空中 VLA：** 预训练机器人模型如何适应浮动基座动力学、载荷变化、欠驱动约束，以及高层动作与底层控制器之间的接口？
3. **完全依赖机载感知的自主操作：** 如何融合视觉定位、测距、接触感知与力控制，在复杂室外环境中稳定完成操作？
4. **面向操作的全景感知：** 360° 观测是否有助于发现非前向目标并实现连续跟踪？ERP 投影畸变又会如何影响末端精定位？
5. **联合评测本体与控制：** 如何在相同的任务和扰动条件下公平比较机械臂结构、夹爪、驱动方式、传感器与学习策略？

## 收录范围与维护说明

- **时间范围：** 以 2024–2026 年为主，检索更新截至 2026 年 10 月 19 日。
- **收录主题：** 空中机械臂、飞行抓取器、空中物理交互、协同操纵，以及紧密相关的感知、规划、控制与学习基准。
- **不收录：** 与物理交互没有明确关联的普通无人机导航、航拍或视觉跟踪论文。
- **正式引用：** 论文已有会议/期刊最终版时，优先核对出版方信息；arXiv 投稿年份与正式发表年份可能不同。
- **完整性：** 这是经筛选的文献合集，并非对全球全部论文的穷尽式统计，正式写作引用前请再次核验题目、作者、年份和出处。
- **建议检索词：** `aerial manipulation`、`aerial manipulator`、`aerial grasping`、`aerial physical interaction`、`aerial VLA`、`cooperative aerial manipulation`。

**继续检索：** [arXiv Robotics](https://arxiv.org/list/cs.RO/recent) · [RSS](https://roboticsproceedings.org/) · [PMLR](https://proceedings.mlr.press/) · [IEEE Xplore](https://ieeexplore.ieee.org/)

---

*从“空中眼睛”走向“空中双手”——迈向具身化的空中智能。*
