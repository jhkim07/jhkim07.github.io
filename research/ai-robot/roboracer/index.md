---
layout: default
title: "RoboRacer (F1TENTH)"
---

<section class="section">
  <div class="container">
    <h2 class="section-title">RoboRacer (F1TENTH)</h2>

    <!-- Language Tabs -->
    <div class="language-tabs">
      <input type="radio" id="lang-ko" name="language" value="ko" checked>
      <input type="radio" id="lang-en" name="language" value="en">
      <label for="lang-ko" class="lang-tab">한국어</label>
      <label for="lang-en" class="lang-tab">English</label>
    </div>

    <!-- Content Area -->
    <div id="content-area" class="content-area">
      <!-- Korean Content -->
      <div id="ko-content" class="lang-content" data-lang="ko">
        <div class="intro-section">

**RoboRacer(F1TENTH)** ([roboracer.or.kr](https://roboracer.or.kr))는 실제 자율주행차의 개발 파이프라인을 축소·정제하여 연구·교육 현장에서 재현할 수 있도록 만든 **표준화된 연구 플랫폼**입니다.

본 플랫폼은 단순한 소형 RC 자동차가 아니라 아래 요소들을 모두 포함하는 **완전한 자율주행 시스템의 축소판**입니다:

{: .feature-highlights}
- 고정밀 LiDAR 센서 기반 인지(perception)
- 실시간 계산(embedded computing)
- 미분 가능한 동역학 기반 제어(control)
- 경로 계획과 최적화(planning & optimization)
- 안전성 평가와 검증(formal verification)

RoboRacer는 *연구자가 알고리즘을 변경하면 즉각 실제 주행 결과로 확인할 수 있는* 실험 친화적 구조를 갖고 있어 전 세계 대학·연구소·기업에서 자율주행 연구의 **일반적 벤치마크 플랫폼**으로 채택되고 있습니다.

        </div>

        <div class="image-container">
          ![F1TENTH RoboRacer Platform]({{ '/research/ai-robot/roboracer/f1tenth.png' | relative_url }}){: .content-image}
          <p class="image-caption">F1TENTH RoboRacer Platform</p>
        </div>

---

## RoboRacer 플랫폼의 특징과 성능

### (1) 정밀 센서·동역학 기반 구조

- 실제 차량과 동일한 **Ackermann 또는 트랙 기반 동역학** 적용
- 타이어 마찰, 코너링, 과·부조향 등 차량 동역학 특성을 명확히 구현
- **2D LiDAR**: 270° 이상 FOV, 0.25° 해상도, 약 40Hz 스캔 빈도 제공
- SLAM·ICP·NDT 등 고급 알고리즘도 실시간 적용 가능

### (2) 고성능 임베디드 시스템

- **NVIDIA Jetson Xavier/Orin** 또는 **Intel NUC** 기반 고성능 연산
- **ROS2** 통신 구조를 사용하여 연구자·학생뿐 아니라 산업용 로봇 시스템과도 구조적 일관성 확보
- Control cycle **20–50Hz** 안정 유지로 고속 레이싱이 가능

### (3) Simulation–Reality 완전 호환성

- **F1TENTH Gym(PyBullet)**, **Gazebo**, **NVIDIA Isaac Sim** 모두 지원
- **Domain Randomization**을 활용한 Sim2Real 연구 수행 가능
- 동일 ROS 인터페이스로 시뮬레이터와 실차 코드가 자동 호환

### (4) 레이싱을 위한 실제적 성능

- 최대 약 **5–10 m/s** 속도로 주행 가능
- 실내 코너링·급가속·급제동에서도 제어 알고리즘 성능 차이가 명확히 관찰됨
- 오버스티어/언더스티어 현상까지 재현되므로 고속 제어 실험이 가능

        <div class="image-container full-width">
          ![RoboRacer Environment]({{ '/research/ai-robot/roboracer/RoboRacer_env.png' | relative_url }}){: .content-image}
          <p class="image-caption">RoboRacer Racing Environment</p>
        </div>

---

## RoboRacer 경기

RoboRacer 경기는 단순한 속도 경쟁이 아니라 **자율주행 알고리즘의 종합적인 품질을 평가하는 국제 연구 대회**입니다.

경기는 다음 요소들을 상세하게 시험합니다:

        <div class="image-container">
          ![RoboRacer Korea 2023]({{ '/research/ai-robot/roboracer/roboracer_korea_2023.jpg' | relative_url }}){: .content-image}
          <p class="image-caption">RoboRacer Korea 2023</p>
        </div>

### (1) Time-Trial Race

- 최적 경로 생성 및 속도 프로파일의 품질
- 차량 동역학을 이해한 제어 알고리즘 설계 능력
- SLAM drift 보정 및 안정성

### (2) Head-to-Head Race

- 상대 차량의 행동을 고려한 전략적 주행
- 충돌 위험 관리(TTC 기반 안전 판단)
- 게임 이론적 상호작용 모델 연구 가능

### (3) Safety & Reliability Challenge

- 급작스러운 장애물 출현에 대한 긴급 제동(AEB) 성능
- 과도한 속도·회전 각속도에서의 안전 제어 능력
- 오차 누적 환경에서도 시스템이 안전하게 수렴하는지 평가

### (4) SLAM / Perception Challenge

- LiDAR scan 정합 정확도
- 실내·동적 환경에서 Localization의 안정성
- multi-frame tracking 최적화

이 대회는 **연구·교육·산업 검증 플랫폼**으로서 기능하며, 국내에서는 **RoboRacer Korea**가 정기 대회를 개최하여 생태계를 확대하고 있습니다.

---

## RoboRacer 플랫폼으로 수행 가능한 연구

RoboRacer는 단순한 교육용 키트가 아니라, **최신 AI·로보틱스 연구의 실험 장(實驗場)**으로 널리 사용되고 있습니다.

### (1) 인지(Perception)

- LiDAR point cloud segmentation / clustering
- scan-to-map localization (ICP, NDT, Fast-LIO2 등 경량화 연구 가능)
- range image 기반 neural perception 연구
- tracking-by-detection / end-to-end BEV 모델 실험

### (2) 경로 계획(Path Planning)

- 고속 레이싱용 최적 레이싱 라인 생성
- Frenet Frame 기반 속도–위치 최적화
- 샘플링 기반 플래너(RRT*, Hybrid A*) + smoothing
- 동적 장애물 회피 및 안전한 reachable tube 생성

### (3) 제어(Control)

- Pure Pursuit, Stanley, PID
- MPC(MPC-LQR, LMPC, Koopman-based MPC)
- Vehicle dynamic model identification(마찰계수 추정 등)

### (4) 강화학습(RL)

- Off-policy RL(SAC, TD3) 기반 주행 정책 학습
- On-policy RL(PPO, TRPO) 기반 레이싱 전략
- Safe RL(Constraint-aware RL, Lagrangian RL, Shielded RL) 적용
- Sim2Real Gap 감소를 위한 Domain Randomization / adversarial training

### (5) 안전성 검증(Safety & Formal Methods)

- 모델체킹 기반 안전성 보증 제어
- Reachable set 기반 속도 제한 자동 계산
- 보험수리 모델(RSS) 적용 실험
- Crash-avoidance 성능을 정량화하는 벤치마크 구축

### (6) 고속 레이싱을 위한 통합 AI

- World Model 기반 예측 제어(Dreamer, ViT-based latent dynamics)
- End-to-End neural control
- Multi-sensor fusion(LiDAR + IMU + wheel odometry)
- Self-supervised trajectory prediction

RoboRacer는 **작고 빠른 플랫폼 덕분에 실험 비용이 매우 낮아**, 고위험 시나리오까지 직접 검증할 수 있다는 장점이 있습니다.

---

## AiX Lab이 집중하는 연구

### RL-based Control Synthesis & Dynamic Lookahead Computation

AiX Lab은 RoboRacer 플랫폼을 활용해 다음과 같은 프레임워크를 발전시키고 있습니다.

        <div class="research-focus">

### (1) 강화학습 기반 제어 합성 (RL-based Control Synthesis)

AiX Lab은 기존 제어기(Pure Pursuit, MPC)의 한계를 넘어서는 **학습 기반 제어기**를 구축하고 있습니다.

**핵심 연구 개념:**

- 모델체킹 기반 환경 제약(safety constraints)을 RL 학습 과정에 내재
- reachable tube / safety envelope을 실시간 계산
- RL reward 설계에 TTC·accumulated risk·trajectory curvature 등을 포함
- simulator + real-world loop를 통한 정책 안정성 검증

> 결과적으로, **"고속에서 빠르면서도 안전을 보장하는 제어기"**를 만드는 것이 목표입니다.
{: .highlight-box}

        </div>

        <div class="research-focus">

### (2) Dynamic Lookahead Computation

Pure Pursuit에서 lookahead는 크게 성능을 좌우합니다.

**AiX Lab의 목표:**

- LiDAR curvature estimation → 실시간 optimal lookahead 산출
- speed profile + lookahead 간의 상호 최적화
- vehicle dynamics + track geometry를 동시에 고려한 adaptive tuning
- RL/MPC로 lookahead를 학습/최적화하는 구조 개발

> 이 연구는 next-generation Pure Pursuit으로 볼 수 있으며, **Lap Time 최소화 + 고속 안정성 확보**라는 두 요구를 동시에 만족시키는 것을 목표로 합니다.
{: .highlight-box}

        </div>

        <div class="related-links">

**Related Links:**
- [RoboRacer Korea (roboracer.or.kr)](https://roboracer.or.kr)
- [F1TENTH Official Website](https://f1tenth.org)

        </div>
      </div>
      
      <!-- English Content -->
      <div id="en-content" class="lang-content" data-lang="en">
        <div class="intro-section">

**RoboRacer(F1TENTH)** ([roboracer.or.kr](https://roboracer.or.kr)) is a **standardized research platform** that scales down and refines the development pipeline of real autonomous vehicles to enable reproduction in research and educational settings.

This platform is not a simple small-scale RC car but a **scaled-down version of a complete autonomous driving system** that includes all of the following elements:

{: .feature-highlights}
- High-precision LiDAR sensor-based perception
- Real-time computation (embedded computing)
- Differentiable dynamics-based control
- Path planning and optimization
- Safety assessment and verification (formal verification)

RoboRacer has an experiment-friendly structure where *researchers can immediately verify algorithm changes through actual driving results*, making it a **general benchmark platform** for autonomous driving research adopted by universities, research institutes, and companies worldwide.

        </div>

        <div class="image-container">
          ![F1TENTH RoboRacer Platform]({{ '/research/ai-robot/roboracer/f1tenth.png' | relative_url }}){: .content-image}
          <p class="image-caption">F1TENTH RoboRacer Platform</p>
        </div>

---

## Features and Performance of the RoboRacer Platform

### (1) Precision Sensor and Dynamics-Based Structure

- Application of **Ackermann or track-based dynamics** identical to real vehicles
- Clear implementation of vehicle dynamics characteristics such as tire friction, cornering, oversteer/understeer
- **2D LiDAR**: 270°+ FOV, 0.25° resolution, approximately 40Hz scan frequency
- Real-time application of advanced algorithms such as SLAM, ICP, NDT

### (2) High-Performance Embedded System

- High-performance computing based on **NVIDIA Jetson Xavier/Orin** or **Intel NUC**
- Use of **ROS2** communication structure ensures structural consistency with industrial robot systems as well as researchers and students
- Stable maintenance of control cycle at **20–50Hz** enables high-speed racing

### (3) Complete Simulation–Reality Compatibility

- Support for **F1TENTH Gym (PyBullet)**, **Gazebo**, and **NVIDIA Isaac Sim**
- Sim2Real research using **Domain Randomization**
- Automatic compatibility between simulator and real vehicle code through identical ROS interface

### (4) Practical Performance for Racing

- Capable of driving at maximum speed of approximately **5–10 m/s**
- Clear observation of control algorithm performance differences in indoor cornering, rapid acceleration, and emergency braking
- Reproduction of oversteer/understeer phenomena enables high-speed control experiments

        <div class="image-container full-width">
          ![RoboRacer Environment]({{ '/research/ai-robot/roboracer/RoboRacer_env.png' | relative_url }}){: .content-image}
          <p class="image-caption">RoboRacer Racing Environment</p>
        </div>

---

## RoboRacer Competitions

RoboRacer competitions are not simple speed races but **international research competitions that comprehensively evaluate the quality of autonomous driving algorithms**.

Competitions test the following elements in detail:

        <div class="image-container">
          ![RoboRacer Korea 2023]({{ '/research/ai-robot/roboracer/roboracer_korea_2023.jpg' | relative_url }}){: .content-image}
          <p class="image-caption">RoboRacer Korea 2023</p>
        </div>

### (1) Time-Trial Race

- Quality of optimal path generation and speed profiles
- Ability to design control algorithms that understand vehicle dynamics
- SLAM drift correction and stability

### (2) Head-to-Head Race

- Strategic driving considering opponent vehicle behavior
- Collision risk management (TTC-based safety assessment)
- Research on game-theoretic interaction models

### (3) Safety & Reliability Challenge

- Emergency braking (AEB) performance for sudden obstacle appearance
- Safe control capability at excessive speed and angular velocity
- Evaluation of whether the system safely converges even in error-accumulating environments

### (4) SLAM / Perception Challenge

- LiDAR scan matching accuracy
- Localization stability in indoor and dynamic environments
- Multi-frame tracking optimization

These competitions function as a **research, education, and industry verification platform**, and in Korea, **RoboRacer Korea** regularly hosts competitions to expand the ecosystem.

---

## Research Enabled by the RoboRacer Platform

RoboRacer is not a simple educational kit but is widely used as a **testing ground for cutting-edge AI and robotics research**.

### (1) Perception

- LiDAR point cloud segmentation / clustering
- Scan-to-map localization (enables lightweight research such as ICP, NDT, Fast-LIO2)
- Range image-based neural perception research
- Tracking-by-detection / end-to-end BEV model experiments

### (2) Path Planning

- Optimal racing line generation for high-speed racing
- Frenet Frame-based speed–position optimization
- Sampling-based planners (RRT*, Hybrid A*) + smoothing
- Dynamic obstacle avoidance and safe reachable tube generation

### (3) Control

- Pure Pursuit, Stanley, PID
- MPC (MPC-LQR, LMPC, Koopman-based MPC)
- Vehicle dynamic model identification (friction coefficient estimation, etc.)

### (4) Reinforcement Learning (RL)

- Off-policy RL (SAC, TD3)-based driving policy learning
- On-policy RL (PPO, TRPO)-based racing strategies
- Safe RL application (Constraint-aware RL, Lagrangian RL, Shielded RL)
- Domain Randomization / adversarial training for Sim2Real gap reduction

### (5) Safety & Formal Methods

- Model checking-based safety-guaranteed control
- Automatic speed limit calculation based on reachable sets
- Responsibility-sensitive safety (RSS) model application experiments
- Benchmark construction for quantifying crash-avoidance performance

### (6) Integrated AI for High-Speed Racing

- World Model-based predictive control (Dreamer, ViT-based latent dynamics)
- End-to-End neural control
- Multi-sensor fusion (LiDAR + IMU + wheel odometry)
- Self-supervised trajectory prediction

RoboRacer has the advantage that **experimental costs are very low due to its small and fast platform**, allowing direct verification of even high-risk scenarios.

---

## Research Focus at AiX Lab

### RL-based Control Synthesis & Dynamic Lookahead Computation

At AiX Lab, we are advancing the following frameworks using the RoboRacer platform.

        <div class="research-focus">

### (1) Reinforcement Learning-Based Control Synthesis

AiX Lab is building **learning-based controllers** that go beyond the limitations of existing controllers (Pure Pursuit, MPC).

**Core Research Concepts:**

- Embedding model checking-based environmental constraints (safety constraints) into the RL learning process
- Real-time calculation of reachable tubes / safety envelopes
- Including TTC, accumulated risk, trajectory curvature, etc. in RL reward design
- Policy stability verification through simulator + real-world loop

> As a result, the goal is to create a **"controller that is fast at high speeds while guaranteeing safety"**.
{: .highlight-box}

        </div>

        <div class="research-focus">

### (2) Dynamic Lookahead Computation

In Pure Pursuit, lookahead significantly affects performance.

**AiX Lab's Goals:**

- LiDAR curvature estimation → real-time optimal lookahead calculation
- Mutual optimization between speed profile + lookahead
- Adaptive tuning simultaneously considering vehicle dynamics + track geometry
- Development of structures that learn/optimize lookahead with RL/MPC

> This research can be viewed as next-generation Pure Pursuit, aiming to simultaneously satisfy two requirements: **minimizing Lap Time + ensuring high-speed stability**.
{: .highlight-box}

        </div>

        <div class="related-links">

**Related Links:**
- [RoboRacer Korea (roboracer.or.kr)](https://roboracer.or.kr)
- [F1TENTH Official Website](https://f1tenth.org)

        </div>
      </div>
    </div>
  </div>
</section>

<script>
// Simple and reliable language switching
(function() {
  const langKo = document.getElementById('lang-ko');
  const langEn = document.getElementById('lang-en');
  const koContent = document.getElementById('ko-content');
  const enContent = document.getElementById('en-content');

  function updateContent() {
    if (langKo && langEn && koContent && enContent) {
      if (langKo.checked) {
        koContent.style.display = 'block';
        enContent.style.display = 'none';
      } else if (langEn.checked) {
        enContent.style.display = 'block';
        koContent.style.display = 'none';
      }
    }
  }

  if (langKo && langEn) {
    langKo.addEventListener('change', updateContent);
    langEn.addEventListener('change', updateContent);
    // Initial state
    updateContent();
  }
})();
</script>
