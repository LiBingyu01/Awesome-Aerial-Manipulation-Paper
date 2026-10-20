# Awesome Aerial Manipulation：58 篇论文三点式对照总表

> **更新时间：2026 年 10 月 20 日**｜**58 篇研究论文及观点文章**｜按五大研究方向分类。

这份总表由 [Awesome Aerial Manipulation 中文版](awesome-aerial-manipulation.zh-CN.md) 整理而来，统一按照 **论文标题、正式发表位置或预印本状态、三项核心创新** 展示，便于快速横向比较、筛选精读对象和撰写 Related Work。

**使用说明：**

- 每篇论文的三点从 **问题与任务设定、方法与系统创新、验证或技术价值** 三个角度提炼；不代表作者原文明确分为这三条贡献。
- **arXiv 是预印本平台，不是会议中稿位置**。标为 arXiv 的工作，在本清单中未核实正式发表出处；2026 年较新的工作状态可能更新。
- **“相关”范围**包括无多关节机械臂的飞行抓取器、挂钩、吊载、协同操作和面向交互的移动基准。它们在方法上相关，但不完全等同于空中机械臂。
- 论文链接保留原文入口。真正引用时，请再核实出版社最终版的作者、题名、会议或期刊信息。

## 目录

1. [视觉—语言—动作、Agent 与学习策略](#视觉语言动作agent-与学习策略)
2. [机载感知、自主抓取与物理交互](#机载感知自主抓取与物理交互)
3. [整机规划、动力学控制与接触稳定性](#整机规划动力学控制与接触稳定性)
4. [机械臂本体、柔性机构与飞行平台设计](#机械臂本体柔性机构与飞行平台设计)
5. [多机协同操作与相关基准](#多机协同操作与相关基准)

## 视觉—语言—动作、Agent 与学习策略（10 篇）

| 论文标题 | 发表位置 / 状态 | 核心创新（三点） |
|---|---|---|
| [Fly-by-Code: Embodied Coding Agents for Aerial Manipulation with Active Visual and Physical Feedback](https://arxiv.org/abs/2610.12549) | arXiv 预印本， 2026-10 | 1. 面向复杂多步空中操作，将自然语言任务组织为可执行程序<br>2. 提出主动 View/Probe 反馈，补足不可见结果与失败原因<br>3. 在仿真中迭代修复操作程序，并展示向真实飞行机械臂迁移 |
| [AeroManip-VLA: Scalable Vision-Language-Action Learning for Aerial Manipulation with RL-Generated Demonstrations](https://arxiv.org/abs/2609.36915) | arXiv 预印本， 2026-09 | 1. 面向空中 VLA 训练数据难采集、难规模化的问题<br>2. 结合并行仿真、强化学习专家与任务规则自动生成示范<br>3. 引入事件标注、轨迹分类和多种模仿学习/VLA 基线评测 |
| [AM-Bench: A Modular Simulation Suite and Benchmark for Aerial Manipulation Policy Learning](https://arxiv.org/abs/2609.00641) | arXiv 预印本， 2026-09 | 1. 覆盖欠驱动、全驱动与过驱动空中操作机体<br>2. 提供接触、运输和受限交互等 12 类任务及标准控制器<br>3. 系统分解机体结构、控制接口、风扰和策略对任务表现的影响 |
| [Aerial Manipulation in the Wild with Onboard Perception, Policy Learning, and Whole-Body Control](https://arxiv.org/abs/2609.30521) | arXiv 预印本， 2026-09；IROS 2026 workshop 版本 | 1. 将空中操作从动捕实验室拓展到真实室外场景<br>2. 结合机载 LiDAR–惯性定位与示范训练的 Diffusion Policy<br>3. 通过整机 MPC 协同执行策略给出的末端动作 |
| [AERMANI-PLACE: Language Guided Object Placement with Aerial Manipulators](https://arxiv.org/abs/2606.14531) | arXiv 预印本， 2026-06 | 1. 把自然语言描述的放置意图转为可执行的空间目标<br>2. 用图像编辑生成目标标记，再借助深度恢复度量坐标<br>3. 进行语言放置基准评测与真实空中机械臂实验 |
| [$\pi$, But Make It Fly: Physics-Guided Transfer of VLA Models to Aerial Manipulation](https://arxiv.org/abs/2603.25038) | arXiv 预印本， 2026-03 | 1. 研究固定基座预训练 VLA 向飞行机械臂迁移时的动力学差异<br>2. 在策略采样过程中注入载荷感知的物理引导<br>3. 利用 3D Gaussian Splatting 合成飞行视觉数据并验证组合任务 |
| [AIR-VLA: Vision-Language-Action Systems for Aerial Manipulation](https://proceedings.mlr.press/v306/sun26an.html) | ICML 2026 | 1. 提出面向空中操作的视觉—语言—动作评测设置<br>2. 构建多模态遥操作数据，覆盖空间理解与长时指令<br>3. 评测多类 VLA/VLM 的能力及空中操作局限性 |
| [Autonomous Aerial Manipulation via Contextual Contrastive Meta Reinforcement Learning](https://arxiv.org/abs/2606.08533) | arXiv 预印本， 2026-06 | 1. 实现挂钩式自主取货、运输和交付的一体化任务<br>2. 通过对比式元强化学习从交互历史推断载荷上下文<br>3. 在载荷变化条件下研究在线适应和仿真到实机迁移 |
| [UMI-on-Air: Embodiment-Aware Guidance for Embodiment-Agnostic Visuomotor Policies](https://arxiv.org/abs/2510.02614) | ICRA 2026（2025 预印本） | 1. 将跨本体视觉动作示范应用于具有飞行动力学约束的系统<br>2. 在扩散采样时加入底层跟踪代价的梯度引导<br>3. 实现测试时对平台可执行性的自适应，而非单纯复用演示轨迹 |
| [AERMANI-VLM: Structured Prompting and Reasoning for Aerial Manipulation with Vision Language Models](https://arxiv.org/abs/2511.01472) | arXiv 预印本， 2025-11 | 1. 降低直接由 VLM 输出飞行动作的不稳定性和幻觉风险<br>2. 用结构化提示得到高层推理，再映射至预定义安全技能<br>3. 在多步抓取放置任务中评估对未见指令与物体的泛化 |

## 机载感知、自主抓取与物理交互（12 篇）

| 论文标题 | 发表位置 / 状态 | 核心创新（三点） |
|---|---|---|
| [Learning High-Speed Aerial Grasping With a Simple Gripper](https://arxiv.org/abs/2603.05935) | arXiv 预印本， 2026-03 | 1. 面向较高飞行速度下的空中抓取<br>2. 采用轻量商用夹爪和学习型控制策略<br>3. 研究无需实机微调的部署与抓取速度—成功率表现 |
| [An Aerial Manipulator for Perception-Driven Flower Targeting Toward Contactless Pollination in Vertical Farming](https://arxiv.org/abs/2605.06759) | arXiv 预印本， 2026-05 | 1. 面向垂直农场中精确花朵定位与末端对准<br>2. 融合机载 RGB-D 感知、MPPI 与轻量 2-DoF 机械臂<br>3. 在仿真与飞行实验中验证末端定位，尚不等于完成授粉任务 |
| [Aerial Manipulation with Contact-Aware Onboard Perception and Hybrid Control](https://arxiv.org/abs/2602.08251) | ICRA 2026 | 1. 面向无需外部动捕的接触式空中操作<br>2. 将接触一致性因素引入视觉—惯性估计，并结合视觉伺服<br>3. 以混合力/位控制闭合从感知到接触力的控制回路 |
| [Aerial Grasping via Maximizing Delta-Arm Workspace Utilization](https://arxiv.org/abs/2506.15539) | arXiv 预印本， 2025-06 | 1. 充分利用 Delta 臂非凸可达空间进行空中抓取<br>2. 学习可达性近似和正运动学的高效梯度表示<br>3. 在轨迹优化中兼顾机械臂可行域与任务约束 |
| [Reliable Aerial Manipulation: Combining Visual Tracking with Range Sensing for Robust Grasping](https://www.research-collection.ethz.ch/entities/publication/0f64ad6f-5ed2-4289-a365-6bb7c48ae182) | ICRA 2025 | 1. 应对抓取目标进入机载相机盲区后的定位问题<br>2. 融合视觉目标跟踪与一维 ToF 测距<br>3. 提高近距离抓取过程中的目标定位鲁棒性 |
| [An Open-Source Soft Robotic Platform for Autonomous Aerial Manipulation in the Wild](https://proceedings.mlr.press/v270/bauer25a.html) | CoRL 2024 / PMLR 2025 | 1. 构建无需外部动作捕捉系统的自主抓取平台<br>2. 集成机载感知、软抓手和开放的 ROS 2 软件/硬件设计<br>3. 在室内外多种环境完成实物抓取验证 |
| [Development of an Aerial Manipulation System Using Onboard Cameras and a Multi-Fingered Robotic Hand with Proximity Sensors](https://www.mdpi.com/1424-8220/25/2/470) | Sensors 2025 | 1. 为自主空中抓取增加更精细的近场目标感知<br>2. 融合机载双相机与带接近传感器的多指手<br>3. 利用近距离反馈修正飞行定位误差并完成抓取 |
| [High-speed aerial grasping using a soft drone with onboard perception](https://www.nature.com/articles/s44182-024-00012-1) | npj Robotics 2024 | 1. 关注较快飞行中精确接近和抓取的难题<br>2. 使用柔性抓手的被动形变吸收定位与接触误差<br>3. 结合机载视觉完成高速空中抓取实验 |
| [Hook-Based Aerial Payload Grasping from a Moving Platform](https://arxiv.org/abs/2409.11788) | arXiv 预印本， 2024-09 | 1. 研究从运动平台拾取悬挂载荷的动态抓取<br>2. 基于互补约束优化挂钩轨迹和接触时机<br>3. 结合物理仿真预测目标未来运动 |
| [Aerial Interaction with Tactile Sensing](https://ieeexplore.ieee.org/document/10611282/) | ICRA 2024 | 1. 为飞行接触交互引入触觉感知能力<br>2. 在全驱动无人机上集成视觉式触觉传感<br>3. 将接触反馈用于动态交互任务 |
| [An Ultra-Light, Ultra-Fast, Passive Closing Aerial Gripping System Capable of Grasping, Perching, and Aerial Manipulation](https://ieeexplore.ieee.org/document/10770047/) | SSRR 2024 | 1. 降低空中抓取机构的质量与闭合延迟<br>2. 提出超轻型被动快速闭合夹爪<br>3. 一套末端机构覆盖抓取、停栖与空中交互 |
| [Design, Localization, Perception, and Control for GPS-Denied Autonomous Aerial Grasping and Harvesting](https://doi.org/10.1109/LRA.2024.3366015) | IEEE RA-L 2024 | 1. 面向 GPS 不可用环境中的自主果实采摘<br>2. 联合定位、视觉检测、飞行控制和抓取机构设计<br>3. 在室内农业采摘场景验证完整系统 |

## 整机规划、动力学控制与接触稳定性（19 篇）

| 论文标题 | 发表位置 / 状态 | 核心创新（三点） |
|---|---|---|
| [Physics-infused Learning for Aerial Manipulator in Winds and Near-Wall Environments](https://arxiv.org/abs/2603.07826) | AIAA SciTech 2026 | 1. 研究风扰与近墙气动效应对空中机械臂的影响<br>2. 结合机理气动模型与学习残差估计未建模作用力<br>3. 在自由飞行和壁面接触跟踪场景中分析鲁棒性 |
| [Safety-Critical Bilateral Teleoperation for Omnidirectional Aerial Manipulation Using Force-Sensorless Haptic Feedback](https://arxiv.org/abs/2608.21735) | IROS 2026（arXiv 注明已录用） | 1. 处理全向空中操作遥操作中的反馈和电机饱和风险<br>2. 以安全过滤器协调指令、推力限制与触觉反馈<br>3. 无显式力传感器地呈现交互信息并验证不同任务 |
| [Effector-Centric NMPC of Tiltable-Multirotors for Offset-Free Omnidirectional Aerial Manipulation](https://arxiv.org/abs/2608.17819) | arXiv 预印本， 2026-08 | 1. 研究可倾转旋翼系统的全向末端控制<br>2. 建立末端中心的 NMPC，并处理奇异位形和扰动补偿<br>3. 实机展示推动接触与连续阀门旋转等操作 |
| [FAM-DQ: A Dual-Quadrotor-Based Fully Actuated Aerial Manipulator for High-Torque Interaction](https://arxiv.org/abs/2608.13220) | arXiv 预印本， 2026-08 | 1. 面向较大接触扭矩而传统机体承载受限的任务<br>2. 采用双四旋翼推进模块与齿轮伺服协调姿态<br>3. 验证六自由度操控和螺丝驱动等高扭矩场景 |
| [Hybrid Impedance-Admittance Control with Multi-Link Aerial Robot for Contact-Rich Surface Sliding Task](https://arxiv.org/abs/2608.01800) | arXiv 预印本， 2026-08 | 1. 解决未知表面滑动时抗扰与柔顺性难兼顾的问题<br>2. 通过关节角实现导纳行为、通过旋翼推力实现阻抗行为<br>3. 使多连杆空中机器人在接触滑动中兼顾顺应与稳定 |
| [Global End-Effector Pose Control of an Underactuated Aerial Manipulator via Reinforcement Learning](https://arxiv.org/abs/2512.21085) | ICRA 2026（2025-12 预印本） | 1. 用四旋翼与轻量 2-DoF 机械臂控制六自由度末端位姿<br>2. 训练强化学习策略输出飞行加速度/角速度和关节目标<br>3. 结合低层姿态控制，在推物与载荷扰动下开展实机验证 |
| [Impact-Robust Posture Optimization for Aerial Manipulation](https://arxiv.org/abs/2602.13762) | ICRA 2026 | 1. 面向接触或撞击瞬间空中机械臂易失稳的问题<br>2. 通过姿态/构型优化提高冲击条件下的可控性<br>3. 为动态接触前的机器人准备姿态提供规划思路 |
| [Whole-body motion planning and safety-critical control for aerial manipulation](https://arxiv.org/abs/2511.02342) | arXiv 预印本， 2025-11 | 1. 解决整机碰撞几何过粗和安全控制过保守的问题<br>2. 利用超二次曲面与代理几何构造可微碰撞约束<br>3. 结合最大间隙规划和高阶控制障碍函数 |
| [Prespecified-Performance Kinematic Tracking Control for Aerial Manipulation](https://arxiv.org/abs/2509.10065) | arXiv 预印本， 2025-09 | 1. 将预设收敛速度和跟踪误差边界引入空中操作<br>2. 围绕末端运动学构建具有性能约束的控制律<br>3. 关注误差在指定包络内的动态演化 |
| [Autonomous Aerial Manipulation at Arbitrary Pose in SE(3) with Robust Control and Whole-body Planning](https://arxiv.org/abs/2508.19608) | arXiv 预印本， 2025-08 | 1. 扩展全向飞行器在任意机体姿态下的机械臂工作空间<br>2. 使用 SE(3) 几何鲁棒控制抑制机械臂及接触反作用<br>3. 联合整机运动规划实现非水平姿态操作 |
| [Flying Hand: End-Effector-Centric Framework for Versatile Aerial Manipulation Teleoperation and Policy Learning](https://roboticsproceedings.org/rss21/p130.html) | RSS 2025 | 1. 为不同空中操作任务提供统一末端执行器接口<br>2. 结合全驱动六旋翼、4-DoF 机械臂与整机 MPC<br>3. 支持遥操作和模仿学习，并验证插孔、书写与旋转操作 |
| [NDOB-Based Control of a UAV with Delta-Arm Considering Manipulator Dynamics](https://arxiv.org/abs/2501.06122) | arXiv 预印本， 2025-01 | 1. 应对 Delta 臂动作导致的机体耦合扰动<br>2. 使用非线性扰动观测器补偿内外扰动<br>3. 结合机械臂动力学处理以兼顾快速运动与末端精度 |
| [Whole-Body Integrated Motion Planning for Aerial Manipulators](https://arxiv.org/abs/2501.06493) | IEEE Transactions on Robotics 2025 | 1. 将无人机和机械臂作为一个整体优化运动轨迹<br>2. 考虑变化的机体碰撞几何、动力学和运动学约束<br>3. 借助模仿学习辅助优化，展示多种基本操作技能 |
| [Safety-Critical Control for Aerial Physical Interaction in Uncertain Environment](https://arxiv.org/abs/2501.16719) | ICRA 2025 | 1. 解决不确定环境下空中物理接触的安全问题<br>2. 使用扰动观测与安全关键控制约束交互动作<br>3. 面向静态和动态结构的稳定接触 |
| [Design of a Flexible Robot Arm for Safe Aerial Physical Interaction](https://arxiv.org/abs/2410.15797) | arXiv 预印本， 2024-10 | 1. 设计轻量且可容忍接触冲击的机械臂<br>2. 采用柔性闭环连杆、绳驱和弹性耗能结构<br>3. 验证自由飞行和外界接触时的机构行为 |
| [A Compact Aerial Manipulator: Design and Control for Dexterous Operations](https://link.springer.com/article/10.1007/s10846-024-02090-7) | Journal of Intelligent & Robotic Systems 2024 | 1. 围绕紧凑机体开展灵巧空中操作硬件设计<br>2. 联合设计机械臂构型与飞行操作控制<br>3. 验证紧凑式机构完成灵巧操作的可行性 |
| [Observer-Based Nonlinear Control for Dual-Arm Aerial Manipulator Systems Suffering From Uncertain Center of Mass](https://ieeexplore.ieee.org/document/10466505/) | IEEE 期刊 2024 | 1. 处理双机械臂引起的质心变化和建模不确定性<br>2. 利用观测器估计不确定项并设计非线性控制<br>3. 建立面向双臂空中机械臂的稳定性分析 |
| [Servo Integrated Nonlinear Model Predictive Control for Overactuated Tiltable-Quadrotors](https://ieeexplore.ieee.org/document/10659124/) | IEEE RA-L 2024 | 1. 为可倾转过驱动四旋翼建立适合控制的动力学模型<br>2. 在非线性 MPC 中显式集成旋翼倾转伺服动态<br>3. 支持姿态与位置相对独立的六自由度机动 |
| [Finite-Time Fast Adaptive Backstepping Attitude Control for Aerial Manipulators Based on Variable Coupling Disturbance Compensation](https://ieeexplore.ieee.org/abstract/document/10505853) | IEEE TIE 2024 | 1. 处理空中机械臂关节运动造成的时变姿态耦合扰动<br>2. 采用快速自适应反步控制与扰动补偿<br>3. 关注有限时间的姿态稳定和跟踪精度 |

## 机械臂本体、柔性机构与飞行平台设计（11 篇）

| 论文标题 | 发表位置 / 状态 | 核心创新（三点） |
|---|---|---|
| [Self-assembling Modular Aerial Robot for Versatile Aerial Tasks](https://arxiv.org/abs/2605.19431) | arXiv 预印本， 2026-05 | 1. 兼顾独立无人机的机动性与组合后机械臂的操作能力<br>2. 设计带关节化对接结构的可自组装飞行模块<br>3. 通过不同组合形态拓展可执行的空中任务 |
| [An Open MuJoCo Simulation Framework for a Quadrotor Carrying a Tendon-Driven Soft Continuum Arm](https://arxiv.org/abs/2610.15308) | arXiv 预印本， 2026-10 | 1. 为四旋翼与绳驱软体连续体臂提供耦合仿真环境<br>2. 在 MuJoCo 中联合建模飞行基座、柔性臂和驱动<br>3. 为软体空中操作算法的复现与控制测试提供平台 |
| [QuadHand: A Compact Quadrotor Aerial Manipulator with MRC-SDF-Based Whole-Body Motion Planning](https://arxiv.org/abs/2609.35094) | IROS 2026（作者主页列出） | 1. 针对狭窄复杂环境中的紧凑型空中机械臂<br>2. 设计 3-DoF 手臂与被动质心补偿结构<br>3. 以机器人中心距离场支持整机时空轨迹优化 |
| [AeRSoM: An Aerial Rigid-Soft Integrated Manipulator for Contact-Rich Manipulation](https://arxiv.org/abs/2609.28044) | arXiv 预印本， 2026-09 | 1. 同时满足高精度操作与接触柔顺性的需求<br>2. 采用刚柔集成机构、可变刚度调节与复合控制<br>3. 验证抓线、叶片接触、插孔与旋拧等接触丰富任务 |
| [A Morphing Aerial Robot With Thruster-Integrated Flexible Continuum Links for Shape Adaptive Aerial Manipulation](https://arxiv.org/abs/2609.19328) | arXiv 预印本， 2026-09 | 1. 突破传统柔性空中机械臂可用接触力受限的问题<br>2. 将推进器分布集成在柔性连续体连杆上<br>3. 联合拓展形态适应性和末端可施加的力/力矩空间 |
| [U-Joint CAAMS: Experimental Evaluation of a Universal-Joint Continuum Manipulator for Aerial Manipulation](https://arxiv.org/abs/2607.03321) | arXiv 预印本， 2026-07 | 1. 针对连续体空中机械臂的侧向形变与末端偏差<br>2. 采用万向节式连续体结构提升非目标方向刚度<br>3. 通过实验分析结构对空中操作精度的影响 |
| [Tilt-X: Enabling Compliant Aerial Manipulation through a Tiltable-Extensible Continuum Manipulator](https://arxiv.org/abs/2602.23576) | ICRA 2026 | 1. 突破下挂式连续体臂工作空间方向受限的问题<br>2. 联合倾转、伸缩和绳驱连续体机构<br>3. 实测旋翼下洗气流对末端定位的影响 |
| [Hand-like autonomous flying robot for airborne grasping and interaction](https://www.nature.com/articles/s41467-026-68967-3) | Nature Communications 2026 | 1. 以手部形态启发紧凑型飞行操作机器人<br>2. 将飞行与抓取交互机构高度一体化<br>3. 展示抓物、开门、停栖以及连续人机交互任务 |
| [Integration of a Variable Stiffness Link for Long-Reach Aerial Manipulation](https://arxiv.org/abs/2510.15639) | arXiv 预印本， 2025-10 | 1. 面向长距离空中操作时精度和顺应性的权衡<br>2. 引入可调刚度连接件，使其在绳索与刚性杆件模式间切换<br>3. 在双臂空中系统中分析扰动隔离及位姿精度 |
| [Avian-Inspired High-Precision Tracking Control for Aerial Manipulators](https://arxiv.org/abs/2411.10966) | arXiv 预印本， 2024-11 | 1. 从鸟类形态提取飞行器—机械臂尺寸与结构启发<br>2. 结合递归牛顿—欧拉动力学和协同跟踪控制<br>3. 旨在提升空中机械臂运动精度和稳定性 |
| [Aerial Manipulator With a Laterally Extendable Scissor Mechanism for Both Extension and Automatic Moment Compensation Using a Single Actuator](https://doi.org/10.1007/s12555-024-0483-2) | International Journal of Control, Automation, and Systems 2025 | 1. 解决机械臂横向伸长引起的附加倾覆力矩<br>2. 使用剪叉伸缩与可移动配重的联动结构<br>3. 以单执行器同时完成伸展和力矩补偿 |

## 多机协同操作与相关基准（6 篇）

| 论文标题 | 发表位置 / 状态 | 核心创新（三点） |
|---|---|---|
| [Benchmarking Interaction-Oriented Aerial Mobility across Heterogeneous Environments (CrossFly)](https://arxiv.org/abs/2610.18381) | arXiv 预印本， 2026-10 | 1. 关注跨室内、室外及混合环境的长时空中移动—交互任务<br>2. 构建多场景、多机体的 CrossFly 轨迹数据与评测框架<br>3. 重点评测从飞行导航过渡到目标交互的过程，而非单独抓取精度 |
| [Aerial Manipulation: Contact, Medium Coupling, and the Geometry of Readiness](https://arxiv.org/abs/2607.04719) | arXiv 预印本， 2026-07；观点/理论文章 | 1. 将空中操作理解为飞行与环境介质持续耦合的过程<br>2. 从接触、介质反作用和几何可操作性建立概念框架<br>3. 属于观点与理论讨论，不是新硬件或新数据集论文 |
| [Decentralized Aerial Manipulation of a Cable-Suspended Load Using Multi-Agent Reinforcement Learning](https://proceedings.mlr.press/v305/zeng25a.html) | CoRL 2025 | 1. 研究多架飞行器对同一悬吊载荷的六自由度操作<br>2. 使用多智能体强化学习训练去中心化控制策略<br>3. 降低对全局状态、邻机通信和集中式指令的依赖 |
| [Multi-robot Aerial Soft Manipulator For Floating Litter Collection](https://arxiv.org/abs/2507.03517) | arXiv 预印本， 2025-07 | 1. 利用多架无人机协作构成柔性操作结构<br>2. 通过悬索形状规划调节抓取能力与绳索张力<br>3. 面向水面漂浮垃圾采集，兼顾载荷与下洗效应 |
| [Agile and Cooperative Aerial Manipulation of a Cable-Suspended Load](https://arxiv.org/abs/2501.18802) | arXiv 预印本， 2025-01 | 1. 研究多机协同悬吊载荷的敏捷机动和空间控制<br>2. 显式考虑飞行器—绳索—载荷耦合动力学<br>3. 为动态运输与协同操作提供轨迹/控制方法 |
| [Proximal cooperative aerial manipulation with vertically stacked drones](https://www.nature.com/articles/s41586-025-09575-x) | Nature 2025 | 1. 解决近距离多机协同存在的气动干扰与操作精度问题<br>2. 采用上下堆叠的操作无人机和工具箱无人机<br>3. 通过空中工具交换实现不同工具/任务的协作 |

## 建议优先精读

如果重点是 **具身 UAV、VLA、端到端策略或世界模型**，建议先看：

1. [Flying Hand](https://roboticsproceedings.org/rss21/p130.html)（RSS 2025）——统一末端控制和模仿学习接口。
2. [AIR-VLA](https://proceedings.mlr.press/v306/sun26an.html)（ICML 2026）——空中 VLA 数据与任务定义。
3. [AM-Bench](https://arxiv.org/abs/2609.00641)（2026）——机体、控制和策略的系统化评测。
4. [π, But Make It Fly](https://arxiv.org/abs/2603.25038)（2026）——预训练 VLA 的动力学迁移。
5. [AeroManip-VLA](https://arxiv.org/abs/2609.36915)（2026）——强化学习示范数据引擎。
6. [Aerial Manipulation in the Wild](https://arxiv.org/abs/2609.30521)（2026）——机载感知与真实室外部署。

---

**备注：** 这是一份从现有 58 篇文献摘要整理的结构化对照，不是逐篇全文审读后的系统性综述，也不保证覆盖领域全部工作。完整项目与综述链接请参考 [中文版 Awesome List](awesome-aerial-manipulation.zh-CN.md)。
