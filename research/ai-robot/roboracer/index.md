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
      <label for="lang-ko" class="lang-tab">한국어</label>
      <input type="radio" id="lang-en" name="language" value="en">
      <label for="lang-en" class="lang-tab">English</label>
    </div>

    <!-- Content Area -->
    <div id="content-area" class="content-area">
      <!-- Korean Content -->
      <div id="ko-content" class="lang-content" data-lang="ko">
        <div class="intro-section">
          <p class="section-text">
            <strong>RoboRacer(F1TENTH)</strong> (<a href="https://roboracer.or.kr" target="_blank">roboracer.or.kr</a>)는 실제 자율주행차의 개발 파이프라인을 축소·정제하여 연구·교육 현장에서 재현할 수 있도록 만든 <strong>표준화된 연구 플랫폼</strong>입니다.
          </p>
          <p class="section-text">
            본 플랫폼은 단순한 소형 RC 자동차가 아니라 아래 요소들을 모두 포함하는 <strong>완전한 자율주행 시스템의 축소판</strong>입니다:
          </p>
          <ul class="feature-highlights">
            <li>고정밀 LiDAR 센서 기반 인지(perception)</li>
            <li>실시간 계산(embedded computing)</li>
            <li>미분 가능한 동역학 기반 제어(control)</li>
            <li>경로 계획과 최적화(planning & optimization)</li>
            <li>안전성 평가와 검증(formal verification)</li>
          </ul>
          <p class="section-text">
            RoboRacer는 <em>연구자가 알고리즘을 변경하면 즉각 실제 주행 결과로 확인할 수 있는</em> 실험 친화적 구조를 갖고 있어 전 세계 대학·연구소·기업에서 자율주행 연구의 <strong>일반적 벤치마크 플랫폼</strong>으로 채택되고 있습니다.
          </p>
        </div>

        <div class="image-container">
          <img src="{{ '/research/ai-robot/roboracer/f1tenth.png' | relative_url }}" alt="F1TENTH RoboRacer Platform" class="content-image">
          <p class="image-caption">F1TENTH RoboRacer Platform</p>
        </div>

        <hr class="section-divider">

        <h3>RoboRacer 플랫폼의 특징과 성능</h3>

        <h4>(1) 정밀 센서·동역학 기반 구조</h4>
        <ul class="section-text">
          <li>실제 차량과 동일한 <strong>Ackermann 또는 트랙 기반 동역학</strong> 적용</li>
          <li>타이어 마찰, 코너링, 과·부조향 등 차량 동역학 특성을 명확히 구현</li>
          <li><strong>2D LiDAR</strong>: 270° 이상 FOV, 0.25° 해상도, 약 40Hz 스캔 빈도 제공</li>
          <li>SLAM·ICP·NDT 등 고급 알고리즘도 실시간 적용 가능</li>
        </ul>

        <h4>(2) 고성능 임베디드 시스템</h4>
        <ul class="section-text">
          <li><strong>NVIDIA Jetson Xavier/Orin</strong> 또는 <strong>Intel NUC</strong> 기반 고성능 연산</li>
          <li><strong>ROS2</strong> 통신 구조를 사용하여 연구자·학생뿐 아니라 산업용 로봇 시스템과도 구조적 일관성 확보</li>
          <li>Control cycle <strong>20–50Hz</strong> 안정 유지로 고속 레이싱이 가능</li>
        </ul>

        <h4>(3) Simulation–Reality 완전 호환성</h4>
        <ul class="section-text">
          <li><strong>F1TENTH Gym(PyBullet)</strong>, <strong>Gazebo</strong>, <strong>NVIDIA Isaac Sim</strong> 모두 지원</li>
          <li><strong>Domain Randomization</strong>을 활용한 Sim2Real 연구 수행 가능</li>
          <li>동일 ROS 인터페이스로 시뮬레이터와 실차 코드가 자동 호환</li>
        </ul>

        <h4>(4) 레이싱을 위한 실제적 성능</h4>
        <ul class="section-text">
          <li>최대 약 <strong>5–10 m/s</strong> 속도로 주행 가능</li>
          <li>실내 코너링·급가속·급제동에서도 제어 알고리즘 성능 차이가 명확히 관찰됨</li>
          <li>오버스티어/언더스티어 현상까지 재현되므로 고속 제어 실험이 가능</li>
        </ul>

        <div class="image-container full-width">
          <img src="{{ '/research/ai-robot/roboracer/RoboRacer_env.png' | relative_url }}" alt="RoboRacer Environment" class="content-image">
          <p class="image-caption">RoboRacer Racing Environment</p>
        </div>

        <hr class="section-divider">

        <h3>RoboRacer 경기</h3>

        <p class="section-text">
          RoboRacer 경기는 단순한 속도 경쟁이 아니라 <strong>자율주행 알고리즘의 종합적인 품질을 평가하는 국제 연구 대회</strong>입니다.
        </p>
        <p class="section-text">
          경기는 다음 요소들을 상세하게 시험합니다:
        </p>

        <div class="image-container">
          <img src="{{ '/research/ai-robot/roboracer/roboracer_korea_2023.jpg' | relative_url }}" alt="RoboRacer Korea 2023" class="content-image">
          <p class="image-caption">RoboRacer Korea 2023</p>
        </div>

        <h4>(1) Time-Trial Race</h4>
        <ul class="section-text">
          <li>최적 경로 생성 및 속도 프로파일의 품질</li>
          <li>차량 동역학을 이해한 제어 알고리즘 설계 능력</li>
          <li>SLAM drift 보정 및 안정성</li>
        </ul>

        <h4>(2) Head-to-Head Race</h4>
        <ul class="section-text">
          <li>상대 차량의 행동을 고려한 전략적 주행</li>
          <li>충돌 위험 관리(TTC 기반 안전 판단)</li>
          <li>게임 이론적 상호작용 모델 연구 가능</li>
        </ul>

        <h4>(3) Safety & Reliability Challenge</h4>
        <ul class="section-text">
          <li>급작스러운 장애물 출현에 대한 긴급 제동(AEB) 성능</li>
          <li>과도한 속도·회전 각속도에서의 안전 제어 능력</li>
          <li>오차 누적 환경에서도 시스템이 안전하게 수렴하는지 평가</li>
        </ul>

        <h4>(4) SLAM / Perception Challenge</h4>
        <ul class="section-text">
          <li>LiDAR scan 정합 정확도</li>
          <li>실내·동적 환경에서 Localization의 안정성</li>
          <li>multi-frame tracking 최적화</li>
        </ul>

        <p class="section-text">
          이 대회는 <strong>연구·교육·산업 검증 플랫폼</strong>으로서 기능하며, 국내에서는 <strong>RoboRacer Korea</strong>가 정기 대회를 개최하여 생태계를 확대하고 있습니다.
        </p>

        <hr class="section-divider">

        <h3>RoboRacer 플랫폼으로 수행 가능한 연구</h3>
        <p class="section-text">
          RoboRacer는 단순한 교육용 키트가 아니라, <strong>최신 AI·로보틱스 연구의 실험 장(實驗場)</strong>으로 널리 사용되고 있습니다.
        </p>

        <h4>(1) 인지(Perception)</h4>
        <ul class="section-text">
          <li>LiDAR point cloud segmentation / clustering</li>
          <li>scan-to-map localization (ICP, NDT, Fast-LIO2 등 경량화 연구 가능)</li>
          <li>range image 기반 neural perception 연구</li>
          <li>tracking-by-detection / end-to-end BEV 모델 실험</li>
        </ul>

        <h4>(2) 경로 계획(Path Planning)</h4>
        <ul class="section-text">
          <li>고속 레이싱용 최적 레이싱 라인 생성</li>
          <li>Frenet Frame 기반 속도–위치 최적화</li>
          <li>샘플링 기반 플래너(RRT*, Hybrid A*) + smoothing</li>
          <li>동적 장애물 회피 및 안전한 reachable tube 생성</li>
        </ul>

        <h4>(3) 제어(Control)</h4>
        <ul class="section-text">
          <li>Pure Pursuit, Stanley, PID</li>
          <li>MPC(MPC-LQR, LMPC, Koopman-based MPC)</li>
          <li>Vehicle dynamic model identification(마찰계수 추정 등)</li>
        </ul>

        <h4>(4) 강화학습(RL)</h4>
        <ul class="section-text">
          <li>Off-policy RL(SAC, TD3) 기반 주행 정책 학습</li>
          <li>On-policy RL(PPO, TRPO) 기반 레이싱 전략</li>
          <li>Safe RL(Constraint-aware RL, Lagrangian RL, Shielded RL) 적용</li>
          <li>Sim2Real Gap 감소를 위한 Domain Randomization / adversarial training</li>
        </ul>

        <h4>(5) 안전성 검증(Safety & Formal Methods)</h4>
        <ul class="section-text">
          <li>모델체킹 기반 안전성 보증 제어</li>
          <li>Reachable set 기반 속도 제한 자동 계산</li>
          <li>보험수리 모델(RSS) 적용 실험</li>
          <li>Crash-avoidance 성능을 정량화하는 벤치마크 구축</li>
        </ul>

        <h4>(6) 고속 레이싱을 위한 통합 AI</h4>
        <ul class="section-text">
          <li>World Model 기반 예측 제어(Dreamer, ViT-based latent dynamics)</li>
          <li>End-to-End neural control</li>
          <li>Multi-sensor fusion(LiDAR + IMU + wheel odometry)</li>
          <li>Self-supervised trajectory prediction</li>
        </ul>

        <p class="section-text">
          RoboRacer는 <strong>작고 빠른 플랫폼 덕분에 실험 비용이 매우 낮아</strong>, 고위험 시나리오까지 직접 검증할 수 있다는 장점이 있습니다.
        </p>

        <hr class="section-divider">

        <h3>AiX Lab이 집중하는 연구</h3>
        
        <h4>RL-based Control Synthesis & Dynamic Lookahead Computation</h4>
        <p class="section-text">
          AiX Lab은 RoboRacer 플랫폼을 활용해 다음과 같은 프레임워크를 발전시키고 있습니다.
        </p>

        <div class="research-focus">
          <h4>(1) 강화학습 기반 제어 합성 (RL-based Control Synthesis)</h4>
          <p class="section-text">
            AiX Lab은 기존 제어기(Pure Pursuit, MPC)의 한계를 넘어서는 <strong>학습 기반 제어기</strong>를 구축하고 있습니다.
          </p>
          
          <h5>핵심 연구 개념:</h5>
          <ul class="section-text">
            <li>모델체킹 기반 환경 제약(safety constraints)을 RL 학습 과정에 내재</li>
            <li>reachable tube / safety envelope을 실시간 계산</li>
            <li>RL reward 설계에 TTC·accumulated risk·trajectory curvature 등을 포함</li>
            <li>simulator + real-world loop를 통한 정책 안정성 검증</li>
          </ul>
          
          <p class="section-text highlight-box">
            결과적으로, <strong>"고속에서 빠르면서도 안전을 보장하는 제어기"</strong>를 만드는 것이 목표입니다.
          </p>
        </div>

        <div class="research-focus">
          <h4>(2) Dynamic Lookahead Computation</h4>
          <p class="section-text">
            Pure Pursuit에서 lookahead는 크게 성능을 좌우합니다.
          </p>
          
          <h5>AiX Lab의 목표:</h5>
          <ul class="section-text">
            <li>LiDAR curvature estimation → 실시간 optimal lookahead 산출</li>
            <li>speed profile + lookahead 간의 상호 최적화</li>
            <li>vehicle dynamics + track geometry를 동시에 고려한 adaptive tuning</li>
            <li>RL/MPC로 lookahead를 학습/최적화하는 구조 개발</li>
          </ul>
          
          <p class="section-text highlight-box">
            이 연구는 next-generation Pure Pursuit으로 볼 수 있으며,
            <strong>Lap Time 최소화 + 고속 안정성 확보</strong>라는 두 요구를 동시에 만족시키는 것을 목표로 합니다.
          </p>
        </div>

        <div class="related-links">
          <p class="section-text">
            <strong>Related Links:</strong><br>
            • <a href="https://roboracer.or.kr" target="_blank">RoboRacer Korea (roboracer.or.kr)</a><br>
            • <a href="https://f1tenth.org" target="_blank">F1TENTH Official Website</a>
          </p>
        </div>
      </div>
      
      <!-- English Content -->
      <div id="en-content" class="lang-content" data-lang="en">
        <div class="intro-section">
          <p class="section-text">
            <strong>RoboRacer(F1TENTH)</strong> (<a href="https://roboracer.or.kr" target="_blank">roboracer.or.kr</a>) is a <strong>standardized research platform</strong> that scales down and refines the development pipeline of real autonomous vehicles to enable reproduction in research and educational settings.
          </p>
          <p class="section-text">
            This platform is not a simple small-scale RC car but a <strong>scaled-down version of a complete autonomous driving system</strong> that includes all of the following elements:
          </p>
          <ul class="feature-highlights">
            <li>High-precision LiDAR sensor-based perception</li>
            <li>Real-time computation (embedded computing)</li>
            <li>Differentiable dynamics-based control</li>
            <li>Path planning and optimization</li>
            <li>Safety assessment and verification (formal verification)</li>
          </ul>
          <p class="section-text">
            RoboRacer has an experiment-friendly structure where <em>researchers can immediately verify algorithm changes through actual driving results</em>, making it a <strong>general benchmark platform</strong> for autonomous driving research adopted by universities, research institutes, and companies worldwide.
          </p>
        </div>

        <div class="image-container">
          <img src="{{ '/research/ai-robot/roboracer/f1tenth.png' | relative_url }}" alt="F1TENTH RoboRacer Platform" class="content-image">
          <p class="image-caption">F1TENTH RoboRacer Platform</p>
        </div>

        <hr class="section-divider">

        <h3>Features and Performance of the RoboRacer Platform</h3>
        
        <h4>(1) Precision Sensor and Dynamics-Based Structure</h4>
        <ul class="section-text">
          <li>Application of <strong>Ackermann or track-based dynamics</strong> identical to real vehicles</li>
          <li>Clear implementation of vehicle dynamics characteristics such as tire friction, cornering, oversteer/understeer</li>
          <li><strong>2D LiDAR</strong>: 270°+ FOV, 0.25° resolution, approximately 40Hz scan frequency</li>
          <li>Real-time application of advanced algorithms such as SLAM, ICP, NDT</li>
        </ul>

        <h4>(2) High-Performance Embedded System</h4>
        <ul class="section-text">
          <li>High-performance computing based on <strong>NVIDIA Jetson Xavier/Orin</strong> or <strong>Intel NUC</strong></li>
          <li>Use of <strong>ROS2</strong> communication structure ensures structural consistency with industrial robot systems as well as researchers and students</li>
          <li>Stable maintenance of control cycle at <strong>20–50Hz</strong> enables high-speed racing</li>
        </ul>

        <h4>(3) Complete Simulation–Reality Compatibility</h4>
        <ul class="section-text">
          <li>Support for <strong>F1TENTH Gym (PyBullet)</strong>, <strong>Gazebo</strong>, and <strong>NVIDIA Isaac Sim</strong></li>
          <li>Sim2Real research using <strong>Domain Randomization</strong></li>
          <li>Automatic compatibility between simulator and real vehicle code through identical ROS interface</li>
        </ul>

        <h4>(4) Practical Performance for Racing</h4>
        <ul class="section-text">
          <li>Capable of driving at maximum speed of approximately <strong>5–10 m/s</strong></li>
          <li>Clear observation of control algorithm performance differences in indoor cornering, rapid acceleration, and emergency braking</li>
          <li>Reproduction of oversteer/understeer phenomena enables high-speed control experiments</li>
        </ul>

        <div class="image-container full-width">
          <img src="{{ '/research/ai-robot/roboracer/RoboRacer_env.png' | relative_url }}" alt="RoboRacer Environment" class="content-image">
          <p class="image-caption">RoboRacer Racing Environment</p>
        </div>

        <hr class="section-divider">

        <h3>RoboRacer Competitions</h3>
        <p class="section-text">
          RoboRacer competitions are not simple speed races but <strong>international research competitions that comprehensively evaluate the quality of autonomous driving algorithms</strong>.
        </p>
        <p class="section-text">
          Competitions test the following elements in detail:
        </p>

        <div class="image-container">
          <img src="{{ '/research/ai-robot/roboracer/roboracer_korea_2023.jpg' | relative_url }}" alt="RoboRacer Korea 2023" class="content-image">
          <p class="image-caption">RoboRacer Korea 2023</p>
        </div>

        <h4>(1) Time-Trial Race</h4>
        <ul class="section-text">
          <li>Quality of optimal path generation and speed profiles</li>
          <li>Ability to design control algorithms that understand vehicle dynamics</li>
          <li>SLAM drift correction and stability</li>
        </ul>

        <h4>(2) Head-to-Head Race</h4>
        <ul class="section-text">
          <li>Strategic driving considering opponent vehicle behavior</li>
          <li>Collision risk management (TTC-based safety assessment)</li>
          <li>Research on game-theoretic interaction models</li>
        </ul>

        <h4>(3) Safety & Reliability Challenge</h4>
        <ul class="section-text">
          <li>Emergency braking (AEB) performance for sudden obstacle appearance</li>
          <li>Safe control capability at excessive speed and angular velocity</li>
          <li>Evaluation of whether the system safely converges even in error-accumulating environments</li>
        </ul>

        <h4>(4) SLAM / Perception Challenge</h4>
        <ul class="section-text">
          <li>LiDAR scan matching accuracy</li>
          <li>Localization stability in indoor and dynamic environments</li>
          <li>Multi-frame tracking optimization</li>
        </ul>

        <p class="section-text">
          These competitions function as a <strong>research, education, and industry verification platform</strong>, and in Korea, <strong>RoboRacer Korea</strong> regularly hosts competitions to expand the ecosystem.
        </p>

        <hr class="section-divider">

        <h3>Research Enabled by the RoboRacer Platform</h3>
        <p class="section-text">
          RoboRacer is not a simple educational kit but is widely used as a <strong>testing ground for cutting-edge AI and robotics research</strong>.
        </p>

        <h4>(1) Perception</h4>
        <ul class="section-text">
          <li>LiDAR point cloud segmentation / clustering</li>
          <li>Scan-to-map localization (enables lightweight research such as ICP, NDT, Fast-LIO2)</li>
          <li>Range image-based neural perception research</li>
          <li>Tracking-by-detection / end-to-end BEV model experiments</li>
        </ul>

        <h4>(2) Path Planning</h4>
        <ul class="section-text">
          <li>Optimal racing line generation for high-speed racing</li>
          <li>Frenet Frame-based speed–position optimization</li>
          <li>Sampling-based planners (RRT*, Hybrid A*) + smoothing</li>
          <li>Dynamic obstacle avoidance and safe reachable tube generation</li>
        </ul>

        <h4>(3) Control</h4>
        <ul class="section-text">
          <li>Pure Pursuit, Stanley, PID</li>
          <li>MPC (MPC-LQR, LMPC, Koopman-based MPC)</li>
          <li>Vehicle dynamic model identification (friction coefficient estimation, etc.)</li>
        </ul>

        <h4>(4) Reinforcement Learning (RL)</h4>
        <ul class="section-text">
          <li>Off-policy RL (SAC, TD3)-based driving policy learning</li>
          <li>On-policy RL (PPO, TRPO)-based racing strategies</li>
          <li>Safe RL application (Constraint-aware RL, Lagrangian RL, Shielded RL)</li>
          <li>Domain Randomization / adversarial training for Sim2Real gap reduction</li>
        </ul>

        <h4>(5) Safety & Formal Methods</h4>
        <ul class="section-text">
          <li>Model checking-based safety-guaranteed control</li>
          <li>Automatic speed limit calculation based on reachable sets</li>
          <li>Responsibility-sensitive safety (RSS) model application experiments</li>
          <li>Benchmark construction for quantifying crash-avoidance performance</li>
        </ul>

        <h4>(6) Integrated AI for High-Speed Racing</h4>
        <ul class="section-text">
          <li>World Model-based predictive control (Dreamer, ViT-based latent dynamics)</li>
          <li>End-to-End neural control</li>
          <li>Multi-sensor fusion (LiDAR + IMU + wheel odometry)</li>
          <li>Self-supervised trajectory prediction</li>
        </ul>

        <p class="section-text">
          RoboRacer has the advantage that <strong>experimental costs are very low due to its small and fast platform</strong>, allowing direct verification of even high-risk scenarios.
        </p>

        <hr class="section-divider">

        <h3>Research Focus at AiX Lab</h3>
        
        <h4>RL-based Control Synthesis & Dynamic Lookahead Computation</h4>
        <p class="section-text">
          At AiX Lab, we are advancing the following frameworks using the RoboRacer platform.
        </p>

        <div class="research-focus">
          <h4>(1) Reinforcement Learning-Based Control Synthesis</h4>
          <p class="section-text">
            AiX Lab is building <strong>learning-based controllers</strong> that go beyond the limitations of existing controllers (Pure Pursuit, MPC).
          </p>
          
          <h5>Core Research Concepts:</h5>
          <ul class="section-text">
            <li>Embedding model checking-based environmental constraints (safety constraints) into the RL learning process</li>
            <li>Real-time calculation of reachable tubes / safety envelopes</li>
            <li>Including TTC, accumulated risk, trajectory curvature, etc. in RL reward design</li>
            <li>Policy stability verification through simulator + real-world loop</li>
          </ul>
          
          <p class="section-text highlight-box">
            As a result, the goal is to create a <strong>"controller that is fast at high speeds while guaranteeing safety"</strong>.
          </p>
        </div>

        <div class="research-focus">
          <h4>(2) Dynamic Lookahead Computation</h4>
          <p class="section-text">
            In Pure Pursuit, lookahead significantly affects performance.
          </p>
          
          <h5>AiX Lab's Goals:</h5>
          <ul class="section-text">
            <li>LiDAR curvature estimation → real-time optimal lookahead calculation</li>
            <li>Mutual optimization between speed profile + lookahead</li>
            <li>Adaptive tuning simultaneously considering vehicle dynamics + track geometry</li>
            <li>Development of structures that learn/optimize lookahead with RL/MPC</li>
          </ul>
          
          <p class="section-text highlight-box">
            This research can be viewed as next-generation Pure Pursuit, aiming to simultaneously satisfy two requirements: <strong>minimizing Lap Time + ensuring high-speed stability</strong>.
          </p>
        </div>

        <div class="related-links">
          <p class="section-text">
            <strong>Related Links:</strong><br>
            • <a href="https://roboracer.or.kr" target="_blank">RoboRacer Korea (roboracer.or.kr)</a><br>
            • <a href="https://f1tenth.org" target="_blank">F1TENTH Official Website</a>
          </p>
        </div>
      </div>
    </div>
  </div>
</section>

