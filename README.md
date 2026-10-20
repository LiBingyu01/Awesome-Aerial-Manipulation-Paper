# Awesome Aerial Manipulation

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

**Language:** English | [简体中文](awesome-aerial-manipulation.zh-CN.md)

> **A curated collection of papers, benchmarks, open-source projects, and research resources for aerial manipulation.** From flying robotic arms and agile grasping to contact-rich control, multi-robot cooperation, and vision-language-action learning.

**Last updated:** October 19, 2026 · **58 research papers and perspectives** · **4 surveys and roadmaps**

Aerial manipulation enables flying robots to move beyond passive sensing and interact physically with the world. This list focuses on the intersection of **aerial robotics, dexterous manipulation, embodied AI, perception, planning, and control**.

The collection primarily covers research from **2024–2026**, with a few earlier foundational surveys. Each entry links to a paper or an official publication page. Some entries are closely related research on cable-suspended payloads, aerial grippers, or interaction-oriented flight rather than articulated aerial manipulators.

**Legend:** `Core` = aerial manipulator, flying hand/gripper, or direct manipulation/control research; `Related` = adjacent aerial interaction, transport, or enabling technology. `arXiv` means a preprint page; it does not imply that the work has not subsequently been accepted.

## Contents

- [Editor's Picks](#editors-picks)
- [Papers](#papers)
  - [Vision-Language-Action, Agents & Robot Learning](#vision-language-action-agents--robot-learning)
  - [Perception, Grasping & Autonomous Interaction](#perception-grasping--autonomous-interaction)
  - [Whole-Body Planning, Control & Contact](#whole-body-planning-control--contact)
  - [Robot Design, Morphology & Soft Manipulation](#robot-design-morphology--soft-manipulation)
  - [Cooperative Manipulation & Related Benchmarks](#cooperative-manipulation--related-benchmarks)
- [Surveys & Roadmaps](#surveys--roadmaps)
- [Projects & Code](#projects--code)
- [Open Research Directions](#open-research-directions)
- [Scope & Maintenance](#scope--maintenance)

## Editor's Picks

**A recommended starting point for readers interested in embodied aerial manipulation and learning-based systems.** These are editorial reading priorities, not paper rankings.

| Paper | Venue / Year | Why read it? |
|---|---|---|
| [**Flying Hand**](https://roboticsproceedings.org/rss21/p130.html) | RSS 2025 | A versatile end-effector-centric framework for teleoperation and imitation learning. |
| [**π, But Make It Fly / AirVLA**](https://arxiv.org/abs/2603.25038) | arXiv 2026 | Transfers pretrained manipulation VLA policies to the dynamics of aerial robots. |
| [**AeroManip-VLA**](https://arxiv.org/abs/2609.36915) | arXiv 2026 | Scalable RL-generated demonstrations and evaluation for aerial VLA. |
| [**AIR-VLA**](https://proceedings.mlr.press/v306/sun26an.html) | ICML 2026 | Aerial VLA tasks, demonstrations, and systematic model evaluation. |
| [**AM-Bench**](https://arxiv.org/abs/2609.00641) | arXiv 2026 | A modular benchmark for manipulation policies, embodiments, and low-level controllers. |
| [**Fly-by-Code**](https://arxiv.org/abs/2610.12549) | arXiv 2026 | Embodied coding agents with active visual and physical feedback. |
| [**Aerial Manipulation in the Wild**](https://arxiv.org/abs/2609.30521) | arXiv 2026 | Onboard localization, imitation learning, and whole-body control outdoors. |
| [**AERMANI-PLACE**](https://arxiv.org/abs/2606.14531) | arXiv 2026 | Language-grounded object placement with aerial manipulators. |
| [**AERMANI-VLM**](https://arxiv.org/abs/2511.01472) | arXiv 2025 | Structured VLM reasoning over safe aerial manipulation skills. |
| [**Whole-Body Integrated Motion Planning**](https://arxiv.org/abs/2501.06493) | IEEE T-RO 2025 | Joint vehicle–arm trajectory optimization under dynamic and collision constraints. |
| [**QuadHand**](https://arxiv.org/abs/2609.35094) | IROS 2026 | Compact 3-DoF aerial arm and robot-centric collision-aware planning. |
| [**FlyingToolbox**](https://www.nature.com/articles/s41586-025-09575-x) | Nature 2025 | Proximal cooperation and midair tool exchange between heterogeneous drones. |

## Papers

Papers are organized **by research theme**, not by publication date. The short notes summarize each paper's primary contribution. Each paper appears once in the main list.

### Vision-Language-Action, Agents & Robot Learning

- **[Fly-by-Code: Embodied Coding Agents for Aerial Manipulation with Active Visual and Physical Feedback](https://arxiv.org/abs/2610.12549)** — *arXiv, 2026* · `Core`  
  An embodied coding-agent framework that actively gathers visual and physical evidence to diagnose and refine manipulation programs.
- **[AeroManip-VLA: Scalable Vision-Language-Action Learning for Aerial Manipulation with RL-Generated Demonstrations](https://arxiv.org/abs/2609.36915)** — *arXiv, 2026* · `Core`  
  GPU-accelerated aerial manipulation environments with RL-generated demonstrations for grasping, placing, and long-horizon tasks.
- **[AM-Bench: A Modular Simulation Suite and Benchmark for Aerial Manipulation Policy Learning](https://arxiv.org/abs/2609.00641)** — *arXiv, 2026* · `Core`  
  A modular suite for studying the interaction between robot embodiment, disturbances, controllers, and manipulation policies.
- **[Aerial Manipulation in the Wild with Onboard Perception, Policy Learning, and Whole-Body Control](https://arxiv.org/abs/2609.30521)** — *arXiv, 2026* · `Core`  
  Combines onboard LiDAR–inertial localization, demonstration-based policies, and whole-body MPC for outdoor tasks.
- **[AERMANI-PLACE: Language Guided Object Placement with Aerial Manipulators](https://arxiv.org/abs/2606.14531)** — *arXiv, 2026* · `Core`  
  Grounds language-specified placement goals in 3D scenes and executes them using an aerial manipulator.
- **[π, But Make It Fly: Physics-Guided Transfer of VLA Models to Aerial Manipulation](https://arxiv.org/abs/2603.25038)** — *arXiv, 2026* · `Core`  
  Adapts manipulation-pretrained VLA models to aerial tasks using payload-aware guidance and synthetic visual data.
- **[AIR-VLA: Vision-Language-Action Systems for Aerial Manipulation](https://proceedings.mlr.press/v306/sun26an.html)** — *ICML, 2026* · `Core`  
  Introduces an aerial VLA benchmark with teleoperated demonstrations and evaluations of language, space, and long-horizon reasoning.
- **[Autonomous Aerial Manipulation via Contextual Contrastive Meta Reinforcement Learning](https://arxiv.org/abs/2606.08533)** — *arXiv, 2026* · `Related`  
  Learns payload-adaptive hook-based pickup, transport, and delivery without explicit online system identification.
- **[UMI-on-Air: Embodiment-Aware Guidance for Embodiment-Agnostic Visuomotor Policies](https://arxiv.org/abs/2510.02614)** — *ICRA 2026; preprint 2025* · `Core`  
  Guides diffusion-policy trajectories using embodiment-specific low-level tracking costs at inference time.
- **[AERMANI-VLM: Structured Prompting and Reasoning for Aerial Manipulation with Vision Language Models](https://arxiv.org/abs/2511.01472)** — *arXiv, 2025* · `Core`  
  Uses structured VLM reasoning to select interpretable, flight-safe manipulation skills.

### Perception, Grasping & Autonomous Interaction

- **[Learning High-Speed Aerial Grasping With a Simple Gripper](https://arxiv.org/abs/2603.05935)** — *arXiv, 2026* · `Core`  
  Learns fast aerial grasping with a lightweight gripper and zero-shot real-world policy deployment.
- **[An Aerial Manipulator for Perception-Driven Flower Targeting Toward Contactless Pollination in Vertical Farming](https://arxiv.org/abs/2605.06759)** — *arXiv, 2026* · `Core`  
  Integrates RGB-D perception, MPPI, and a lightweight arm for precise flower targeting in indoor agriculture.
- **[Aerial Manipulation with Contact-Aware Onboard Perception and Hybrid Control](https://arxiv.org/abs/2602.08251)** — *ICRA, 2026* · `Core`  
  Uses contact-aware visual–inertial estimation, image-based visual servoing, and hybrid force–motion control.
- **[Aerial Grasping via Maximizing Delta-Arm Workspace Utilization](https://arxiv.org/abs/2506.15539)** — *arXiv, 2025* · `Core`  
  Optimizes aerial grasping trajectories using learned representations of a Delta arm's reachable workspace.
- **[Reliable Aerial Manipulation: Combining Visual Tracking with Range Sensing for Robust Grasping](https://www.research-collection.ethz.ch/entities/publication/0f64ad6f-5ed2-4289-a365-6bb7c48ae182)** — *ICRA, 2025* · `Core`  
  Fuses visual tracking and ToF range sensing to improve grasping when the target leaves the camera view.
- **[An Open-Source Soft Robotic Platform for Autonomous Aerial Manipulation in the Wild](https://proceedings.mlr.press/v270/bauer25a.html)** — *CoRL 2024 / PMLR 2025* · `Core`  
  An onboard-perception, soft-gripper aerial manipulation platform with open-source software and hardware.
- **[Development of an Aerial Manipulation System Using Onboard Cameras and a Multi-Fingered Robotic Hand with Proximity Sensors](https://www.mdpi.com/1424-8220/25/2/470)** — *Sensors, 2025* · `Core`  
  Combines onboard cameras with a proximity-sensing multi-fingered hand for object localization and grasping.
- **[High-speed aerial grasping using a soft drone with onboard perception](https://www.nature.com/articles/s44182-024-00012-1)** — *npj Robotics, 2024* · `Core`  
  Explores fast vision-guided aerial grasping through the compliance of a soft gripper.
- **[Hook-Based Aerial Payload Grasping from a Moving Platform](https://arxiv.org/abs/2409.11788)** — *arXiv, 2024* · `Related`  
  Optimizes the timing and trajectory of hook-based pickup from a moving platform.
- **[Aerial Interaction with Tactile Sensing](https://ieeexplore.ieee.org/document/10611282/)** — *ICRA, 2024* · `Core`  
  Brings vision-based tactile feedback to contact-rich tasks on a fully actuated UAV.
- **[An Ultra-Light, Ultra-Fast, Passive Closing Aerial Gripping System Capable of Grasping, Perching, and Aerial Manipulation](https://ieeexplore.ieee.org/document/10770047/)** — *SSRR, 2024* · `Core`  
  A fast, lightweight passive-closing gripper for aerial grasping and perching.
- **[Design, Localization, Perception, and Control for GPS-Denied Autonomous Aerial Grasping and Harvesting](https://doi.org/10.1109/LRA.2024.3366015)** — *IEEE RA-L, 2024* · `Core`  
  An integrated perception, localization, and control system for autonomous aerial fruit harvesting.

### Whole-Body Planning, Control & Contact

- **[Physics-infused Learning for Aerial Manipulator in Winds and Near-Wall Environments](https://arxiv.org/abs/2603.07826)** — *AIAA SciTech, 2026* · `Core`  
  Combines aerodynamic modeling and learned residuals for robust operation near walls and in wind.
- **[Safety-Critical Bilateral Teleoperation for Omnidirectional Aerial Manipulation Using Force-Sensorless Haptic Feedback](https://arxiv.org/abs/2608.21735)** — *IROS, 2026* · `Core`  
  Integrates barrier-function safety filtering and sensorless haptic feedback into bilateral teleoperation.
- **[Effector-Centric NMPC of Tiltable-Multirotors for Offset-Free Omnidirectional Aerial Manipulation](https://arxiv.org/abs/2608.17819)** — *arXiv, 2026* · `Core`  
  Effector-centric nonlinear MPC for a tiltable platform, including omnidirectional contact tasks.
- **[FAM-DQ: A Dual-Quadrotor-Based Fully Actuated Aerial Manipulator for High-Torque Interaction](https://arxiv.org/abs/2608.13220)** — *arXiv, 2026* · `Core`  
  A dual-quadrotor mechanism designed for high-torque aerial physical interaction.
- **[Hybrid Impedance-Admittance Control with Multi-Link Aerial Robot for Contact-Rich Surface Sliding Task](https://arxiv.org/abs/2608.01800)** — *arXiv, 2026* · `Core`  
  Combines joint-level admittance and rotor-level impedance to slide compliantly along uncertain surfaces.
- **[Global End-Effector Pose Control of an Underactuated Aerial Manipulator via Reinforcement Learning](https://arxiv.org/abs/2512.21085)** — *ICRA, 2026; preprint 2025* · `Core`  
  Reinforcement learning for 6-DoF end-effector pose control with a lightweight 2-DoF aerial arm.
- **[Impact-Robust Posture Optimization for Aerial Manipulation](https://arxiv.org/abs/2602.13762)** — *ICRA, 2026* · `Core`  
  Optimizes robot posture to mitigate disturbances from impact and physical contact.
- **[Whole-body motion planning and safety-critical control for aerial manipulation](https://arxiv.org/abs/2511.02342)** — *arXiv, 2025* · `Core`  
  Employs superquadric geometry, clearance-aware planning, and barrier-function safety constraints.
- **[Prespecified-Performance Kinematic Tracking Control for Aerial Manipulation](https://arxiv.org/abs/2509.10065)** — *arXiv, 2025* · `Core`  
  Designs aerial end-effector tracking control with prescribed error-performance bounds.
- **[Autonomous Aerial Manipulation at Arbitrary Pose in SE(3) with Robust Control and Whole-body Planning](https://arxiv.org/abs/2508.19608)** — *arXiv, 2025* · `Core`  
  Couples robust geometric control and whole-body planning for omnidirectional aerial manipulation.
- **[Flying Hand: End-Effector-Centric Framework for Versatile Aerial Manipulation Teleoperation and Policy Learning](https://roboticsproceedings.org/rss21/p130.html)** — *RSS, 2025* · `Core`  
  Establishes a unified end-effector interface for aerial teleoperation, whole-body control, and policy learning.
- **[NDOB-Based Control of a UAV with Delta-Arm Considering Manipulator Dynamics](https://arxiv.org/abs/2501.06122)** — *arXiv, 2025* · `Core`  
  Uses a nonlinear disturbance observer to compensate for coupled vehicle–arm dynamics.
- **[Whole-Body Integrated Motion Planning for Aerial Manipulators](https://arxiv.org/abs/2501.06493)** — *IEEE T-RO, 2025* · `Core`  
  Jointly optimizes vehicle and arm trajectories with configuration-dependent collision constraints and imitation guidance.
- **[Safety-Critical Control for Aerial Physical Interaction in Uncertain Environment](https://arxiv.org/abs/2501.16719)** — *ICRA, 2025* · `Core`  
  Disturbance-observer-based safety-critical control for contact with uncertain static and dynamic structures.
- **[Design of a Flexible Robot Arm for Safe Aerial Physical Interaction](https://arxiv.org/abs/2410.15797)** — *arXiv, 2024* · `Core`  
  Studies lightweight compliant actuation and impact energy dissipation in aerial physical interaction.
- **[A Compact Aerial Manipulator: Design and Control for Dexterous Operations](https://link.springer.com/article/10.1007/s10846-024-02090-7)** — *Journal of Intelligent & Robotic Systems, 2024* · `Core`  
  Presents compact aerial manipulator hardware and control for dexterous operations.
- **[Observer-Based Nonlinear Control for Dual-Arm Aerial Manipulator Systems Suffering From Uncertain Center of Mass](https://ieeexplore.ieee.org/document/10466505/)** — *IEEE journal, 2024* · `Core`  
  Addresses uncertain center-of-mass dynamics in nonlinear control of a dual-arm aerial robot.
- **[Servo Integrated Nonlinear Model Predictive Control for Overactuated Tiltable-Quadrotors](https://ieeexplore.ieee.org/document/10659124/)** — *IEEE RA-L, 2024* · `Related`  
  Integrates servo dynamics into predictive control of a tiltable, overactuated aerial platform.
- **[Finite-Time Fast Adaptive Backstepping Attitude Control for Aerial Manipulators Based on Variable Coupling Disturbance Compensation](https://ieeexplore.ieee.org/abstract/document/10505853)** — *IEEE TIE, 2024* · `Core`  
  Adaptive finite-time attitude control with compensation for changing vehicle–manipulator coupling.

### Robot Design, Morphology & Soft Manipulation

- **[Self-assembling Modular Aerial Robot for Versatile Aerial Tasks](https://arxiv.org/abs/2605.19431)** — *arXiv, 2026* · `Core`  
  Reconfigures multiple independently flying units into a modular flying manipulator.
- **[An Open MuJoCo Simulation Framework for a Quadrotor Carrying a Tendon-Driven Soft Continuum Arm](https://arxiv.org/abs/2610.15308)** — *arXiv, 2026* · `Core`  
  An open simulation framework for a quadrotor carrying a tendon-actuated continuum arm.
- **[QuadHand: A Compact Quadrotor Aerial Manipulator with MRC-SDF-Based Whole-Body Motion Planning](https://arxiv.org/abs/2609.35094)** — *IROS, 2026* · `Core`  
  Combines a compact 3-DoF manipulator, center-of-gravity compensation, and collision-aware planning.
- **[AeRSoM: An Aerial Rigid-Soft Integrated Manipulator for Contact-Rich Manipulation](https://arxiv.org/abs/2609.28044)** — *arXiv, 2026* · `Core`  
  Uses rigid–soft integration and variable stiffness for compliant, precise contact manipulation.
- **[A Morphing Aerial Robot With Thruster-Integrated Flexible Continuum Links for Shape Adaptive Aerial Manipulation](https://arxiv.org/abs/2609.19328)** — *arXiv, 2026* · `Core`  
  Distributes thrusters along flexible continuum links to combine shape adaptation and interaction forces.
- **[U-Joint CAAMS: Experimental Evaluation of a Universal-Joint Continuum Manipulator for Aerial Manipulation](https://arxiv.org/abs/2607.03321)** — *arXiv, 2026* · `Core`  
  Investigates a universal-joint continuum manipulator designed to resist out-of-plane deformation.
- **[Tilt-X: Enabling Compliant Aerial Manipulation through a Tiltable-Extensible Continuum Manipulator](https://arxiv.org/abs/2602.23576)** — *ICRA, 2026* · `Core`  
  Adds tilting and telescopic mechanisms to expand the usable workspace of a continuum aerial arm.
- **[Hand-like autonomous flying robot for airborne grasping and interaction](https://www.nature.com/articles/s41467-026-68967-3)** — *Nature Communications, 2026* · `Core`  
  A hand-inspired flying robot for grasping, perching, opening doors, and continuous interactions.
- **[Integration of a Variable Stiffness Link for Long-Reach Aerial Manipulation](https://arxiv.org/abs/2510.15639)** — *arXiv, 2025* · `Core`  
  A variable-stiffness link that trades precision for compliance in long-reach dual-arm manipulation.
- **[Avian-Inspired High-Precision Tracking Control for Aerial Manipulators](https://arxiv.org/abs/2411.10966)** — *arXiv, 2024* · `Core`  
  An avian-inspired aerial arm design with coordinated high-precision tracking control.
- **[Aerial Manipulator With a Laterally Extendable Scissor Mechanism for Both Extension and Automatic Moment Compensation Using a Single Actuator](https://doi.org/10.1007/s12555-024-0483-2)** — *International Journal of Control, Automation, and Systems, 2025* · `Core`  
  Combines lateral extension with automatic moment compensation using a single actuator.

### Cooperative Manipulation & Related Benchmarks

- **[Benchmarking Interaction-Oriented Aerial Mobility across Heterogeneous Environments (CrossFly)](https://arxiv.org/abs/2610.18381)** — *arXiv, 2026* · `Related`  
  A long-horizon benchmark connecting aerial mobility and eventual interaction across heterogeneous environments.
- **[Aerial Manipulation: Contact, Medium Coupling, and the Geometry of Readiness](https://arxiv.org/abs/2607.04719)** — *arXiv perspective, 2026* · `Related`  
  A conceptual treatment of aerial manipulation through contact mechanics and surrounding-medium coupling.
- **[Decentralized Aerial Manipulation of a Cable-Suspended Load Using Multi-Agent Reinforcement Learning](https://proceedings.mlr.press/v305/zeng25a.html)** — *CoRL, 2025* · `Related`  
  Learns decentralized cooperative control for 6-DoF manipulation of a cable-suspended load.
- **[Multi-robot Aerial Soft Manipulator For Floating Litter Collection](https://arxiv.org/abs/2507.03517)** — *arXiv, 2025* · `Related`  
  Uses two aerial robots and a rope-based soft manipulation mechanism for floating-litter collection.
- **[Agile and Cooperative Aerial Manipulation of a Cable-Suspended Load](https://arxiv.org/abs/2501.18802)** — *arXiv, 2025* · `Related`  
  Investigates agile cooperative motion and manipulation of a shared suspended payload.
- **[Proximal cooperative aerial manipulation with vertically stacked drones](https://www.nature.com/articles/s41586-025-09575-x)** — *Nature, 2025* · `Core`  
  FlyingToolbox enables close-proximity cooperation and midair tool exchange between drones.

## Surveys & Roadmaps

Useful entry points for understanding the evolution, modeling assumptions, and open challenges of the field.

- **[From aerial transportation to aerial interaction: A review](https://www.sciencedirect.com/science/article/pii/S1000936126003808)** — *2026*. Reviews the transition from load transport to physical interaction.
- **[A Review of Real-Time Implementable Cooperative Aerial Manipulation Systems](https://www.mdpi.com/2504-446X/8/5/196)** — *Drones, 2024*. Surveys cooperative platforms, modeling, and real-time control.
- **[Past, Present, and Future of Aerial Robotic Manipulators](https://doi.org/10.1109/TRO.2021.3084395)** — *IEEE T-RO, 2022*. A foundational roadmap on aerial robot embodiments and physical interaction.
- **[Survey on Aerial Manipulator: System, Modeling, and Control](https://www.cambridge.org/core/journals/robotica/article/survey-on-aerial-manipulator-system-modeling-and-control/5FDD2404D65EF73477CF10CA62B69720)** — *Robotica, 2020*. Reviews aerial manipulator systems, dynamic models, and control schemes.

## Projects & Code

| Project | Paper | Resources |
|---|---|---|
| **Flying Hand** | RSS 2025 | [Paper](https://roboticsproceedings.org/rss21/p130.html) · [Project page](https://lecar-lab.github.io/flying_hand/) |
| **AM-Planner** | IEEE T-RO 2025 | [Paper](https://arxiv.org/abs/2501.06493) · [GitHub](https://github.com/SYSU-HILAB/am-planner) |
| **AirVLA** | arXiv 2026 | [Paper](https://arxiv.org/abs/2603.25038) · [Project page](https://airvla.github.io/) |
| **AIR-VLA** | ICML 2026 | [Proceedings](https://proceedings.mlr.press/v306/sun26an.html) |
| **Open-Source Soft Aerial Manipulation** | CoRL 2024 | [Proceedings](https://proceedings.mlr.press/v270/bauer25a.html) |
| **Decentralized Cable-Suspended Manipulation** | CoRL 2025 | [Proceedings](https://proceedings.mlr.press/v305/zeng25a.html) |
| **FlyingToolbox** | Nature 2025 | [Publisher page](https://www.nature.com/articles/s41586-025-09575-x) |

> Links to papers or project pages do not guarantee that source code or datasets are publicly available. Check the linked pages for current release status.

## Open Research Directions

1. **From perception to physical interaction.** How can an aerial robot jointly perform target discovery, approach, grasping, transport, and placement over long horizons? Evaluate each stage separately, including safety and recovery.
2. **Transferable aerial VLA policies.** How should foundation models account for floating-base dynamics, payloads, underactuation, and the interface between high-level actions and low-level control?
3. **Manipulation without external infrastructure.** Combine onboard visual localization, range sensing, contact-aware estimation, and force regulation in cluttered outdoor environments.
4. **Omnidirectional perception for manipulation.** Study whether panoramic observations improve non-frontal target acquisition and continuous tracking, while accounting for distortion during precise end-effector alignment.
5. **Benchmarking embodiment and control together.** Compare different arm morphologies, grippers, actuation strategies, sensing configurations, and policy classes under matched disturbances and task definitions.

## Scope & Maintenance

- **Time span:** Primarily 2024–2026, as of October 19, 2026.
- **Inclusion:** Aerial manipulators, flying grippers, aerial physical interaction, cooperative manipulation, task-relevant perception/control, and aerial manipulation learning benchmarks.
- **Exclusion:** Ordinary aerial navigation or tracking studies without a clear physical-interaction connection.
- **Bibliographic accuracy:** Use the publisher's version of record when citing a formally published paper. arXiv submission year and conference publication year may differ.
- **Completeness:** This is a curated, non-exhaustive research list. Titles, venues, and release status should be rechecked before use in a manuscript.
- **Search terms:** `aerial manipulation`, `aerial manipulator`, `aerial grasping`, `aerial physical interaction`, `whole-body aerial control`, `aerial VLA`, `cooperative aerial manipulation`.

**Discover more:** [arXiv Robotics](https://arxiv.org/list/cs.RO/recent) · [Robotics: Science and Systems](https://roboticsproceedings.org/) · [Proceedings of Machine Learning Research](https://proceedings.mlr.press/) · [IEEE Xplore](https://ieeexplore.ieee.org/)

---

*From flying cameras to flying hands — toward embodied aerial intelligence.*
