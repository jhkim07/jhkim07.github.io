---
layout: default
title: "RoboRacer (F1TENTH)"
---

<section class="section">
  <div class="container">
    <h2 class="section-title">RoboRacer (F1TENTH)</h2>

    <!-- Language Tabs -->
    <div class="language-tabs">
      <button type="button" class="lang-tab active" data-lang="ko">한국어</button>
      <button type="button" class="lang-tab" data-lang="en">English</button>
    </div>

    <!-- Content Area -->
    <div id="content-area" class="content-area">
      <!-- Korean Content -->
      <div id="ko-content" class="lang-content" data-lang="ko" style="display: block !important;">
        <p class="section-text">
          <strong>RoboRacer</strong> (<a href="https://roboracer.or.kr" target="_blank">roboracer.or.kr</a>)는 1/10 크기의 고성능 자율주행 레이싱 플랫폼으로,
          실제 자동차와 동일한 <strong>센서–계산–제어 파이프라인</strong>을 축소한 형태로 구현한 연구·교육용 오픈 플랫폼입니다.
        </p>

        <!-- RoboRacer 이미지 -->
        <div style="margin: 2rem 0; text-align: center;">
          <img 
            src="{{ '/research/ai-robot/roboracer/f1tenth.png' | relative_url }}" 
            alt="F1TENTH RoboRacer Platform"
            style="max-width: 45%; border-radius: 0.75rem; border: 1px solid #333;"
          >
          <p style="color: #bdbdbd; font-size: 0.9rem; margin-top: 0.5rem;">
            F1TENTH RoboRacer Platform
          </p>
        </div>

        <h3>RoboRacer의 기본 목표</h3>
        <ul class="section-text">
          <li><strong>현실성 높은 자율주행 알고리즘 실험 환경 제공</strong>
            <br>LiDAR 기반 인지, 로컬·글로벌 플래닝, 제어, 안전성 검증 등
          </li>
          <li><strong>학생·연구자·산업체가 동일한 표준 플랫폼에서 연구를 공유할 수 있는 생태계 구축</strong></li>
          <li><strong>실제 주행 환경에서 알고리즘의 한계를 극적으로 드러낼 수 있는 레이싱 기반 벤치마크 제공</strong></li>
        </ul>

        <p class="section-text">
          RoboRacer는 미국 UPenn PRECISE Lab에서 시작된 F1TENTH 프로젝트를 기반으로
          글로벌 커뮤니티가 함께 발전시키고 있으며, 한국에서는 <strong>RoboRacer Korea</strong>가 교육·연구·경기 생태계를 주도하고 있습니다.
        </p>

        <hr style="margin: 2.5rem 0; border: 0.5px solid #333;">

        <h3>RoboRacer 플랫폼의 특징과 성능</h3>
        <p class="section-text">
          RoboRacer 플랫폼은 실제 자율주행차의 구조를 그대로 축소해, 연구자가 알고리즘 개발에만 집중할 수 있도록 설계되었습니다.
        </p>

        <h4>주요 특징</h4>

        <h5>1) 고정밀 2D LiDAR 기반 인지</h5>
        <ul class="section-text">
          <li>270도 이상의 FOV(Field of View)</li>
          <li>약 40 Hz 스캔 속도</li>
          <li>실내 환경에서 안정적인 장애물 감지·추적 가능</li>
          <li>→ Follow-The-Gap, AEB, SLAM, Tracking 등 다양한 알고리즘 실험에 사용</li>
        </ul>

        <h5>2) 고성능 임베디드 컴퓨팅</h5>
        <ul class="section-text">
          <li>NVIDIA Jetson/NUC 등 고연산 장치 장착 가능</li>
          <li>ROS 2 기반 운영</li>
          <li>실시간 제어 루프(20–50 Hz) 유지 가능</li>
        </ul>

        <h5>3) 모터·서보 기반 고응답 주행 제어</h5>
        <ul class="section-text">
          <li>VESC 기반 속도 제어, Ackermann steering 또는 트랙 기반 플랫폼 모두 가능</li>
          <li>빠른 조향 응답으로 고속 레이싱에 적합</li>
        </ul>

        <h5>4) 시뮬레이터와 실제 차량의 완전한 호환</h5>
        <ul class="section-text">
          <li>F1TENTH Gym, Gazebo, Isaac 기반 시뮬레이션 제공</li>
          <li>시뮬레이션–현실(Sim2Real) 전이 실험에 최적</li>
        </ul>

        <h4>성능 개요</h4>
        <ul class="section-text">
          <li>최고 속도: 약 5–10 m/s (구성에 따라 상이)</li>
          <li>제동거리 및 회전 반경: 실제 차량과 유사하게 비선형적 거동</li>
          <li>다양한 주행 환경(협소 코너, 직선 가속, 장애물 회피)에서 안정적</li>
        </ul>

        <p class="section-text">
          RoboRacer는 "단순 취미용 RC"가 아니라, <strong>제어 이론·AI·로보틱스 연구가 실제 주행 성능으로 검증되는 과학적 실험 플랫폼</strong>입니다.
        </p>

        <!-- RoboRacer 환경 이미지 -->
        <div style="margin: 2rem 0; text-align: center;">
          <img 
            src="{{ '/research/ai-robot/roboracer/RoboRacer_env.png' | relative_url }}" 
            alt="RoboRacer Environment"
            style="width: 100%; max-width: 100%; border-radius: 0.75rem; border: 1px solid #333;"
          >
          <p style="color: #bdbdbd; font-size: 0.9rem; margin-top: 0.5rem;">
            RoboRacer Racing Environment
          </p>
        </div>

        <hr style="margin: 2.5rem 0; border: 0.5px solid #333;">

        <h3>RoboRacer 경기</h3>
        <p class="section-text">
          RoboRacer 경기는 "자율주행 알고리즘의 실제 성능"을 겨루는 글로벌 레이싱 대회입니다.
        </p>

        <!-- RoboRacer Korea 2023 이미지 -->
        <div style="margin: 2rem 0; text-align: center;">
          <img 
            src="{{ '/research/ai-robot/roboracer/roboracer_korea_2023.jpg' | relative_url }}" 
            alt="RoboRacer Korea 2023"
            style="max-width: 90%; border-radius: 0.75rem; border: 1px solid #333;"
          >
          <p style="color: #bdbdbd; font-size: 0.9rem; margin-top: 0.5rem;">
            RoboRacer Korea 2023
          </p>
        </div>

        <h4>경기 구성</h4>

        <h5>1) Time-Trial Race</h5>
        <p class="section-text">
          가장 빠르고 안정적으로 트랙을 완주하는 알고리즘이 우승합니다.
          Pure Pursuit, MPC, RRT*, A*, Gap-Following, RL 기반 제어 등 다양한 접근이 가능합니다.
        </p>

        <h5>2) Head-to-Head Race</h5>
        <p class="section-text">
          두 차량이 동시에 출발합니다. 충돌 회피, 최적 라인 선택, 전략적 속도 조절 등 고도화된 판단이 필요합니다.
        </p>

        <h5>3) Safety & Reliability Challenge</h5>
        <p class="section-text">
          AEB(긴급 제동), 안전성 판단, TTC(Time-to-Collision) 기반 충돌 회피 테스트를 수행합니다.
        </p>

        <h5>4) SLAM & Perception Challenge</h5>
        <p class="section-text">
          LiDAR 기반 SLAM 정확도, Localization Drift, 동적 장애물 대응력 등을 평가합니다.
        </p>

        <p class="section-text">
          RoboRacer 경기는 <strong>연구 성과가 실전에서 어떻게 작동하는지를 가장 명확하게 보여주는 벤치마크</strong>로 활용됩니다.
        </p>

        <hr style="margin: 2.5rem 0; border: 0.5px solid #333;">

        <h3>RoboRacer 플랫폼으로 수행 가능한 연구</h3>
        <p class="section-text">
          RoboRacer는 단순한 교육용 키트가 아니라, <strong>최신 AI·로보틱스 연구의 실험 장(實驗場)</strong>으로 널리 사용되고 있습니다.
        </p>

        <h4>1) 인지(Perception)</h4>
        <ul class="section-text">
          <li>LiDAR 기반 객체 감지 및 추적</li>
          <li>신호 처리 기반 노이즈 제거 및 스캔 정합(Scan Matching)</li>
          <li>실시간 환경 모델 학습(SLAM, ICP, NDT 등)</li>
        </ul>

        <h4>2) 경로 계획(Path Planning)</h4>
        <ul class="section-text">
          <li>최적 트랙 생성 (Optimal Racing Line)</li>
          <li>RRT*/Hybrid A* 등 샘플링 기반 플래너</li>
          <li>다중 장애물 회피, 동적 환경 대응</li>
        </ul>

        <h4>3) 제어(Control & Driving Policy)</h4>
        <ul class="section-text">
          <li>Pure Pursuit, Stanley, PID 기반 주행</li>
          <li>MPC(Model Predictive Control) 기반 레이싱</li>
          <li>Adaptive Lookahead / Speed Profile 생성</li>
          <li>차륜 마찰 기반 동역학 모델링</li>
        </ul>

        <h4>4) 강화학습(Reinforcement Learning)</h4>
        <ul class="section-text">
          <li>RL 기반 레이싱 전략 학습</li>
          <li>안전 강화학습(Safe RL)</li>
          <li>시뮬레이션–현실 전이(Sim2Real) 기법 연구</li>
          <li>TTC 기반 위험도 평가 + 정책 안정화</li>
        </ul>

        <h4>5) 자율주행 안전성(Safety, Verification)</h4>
        <ul class="section-text">
          <li>AEB 및 안전 정지 알고리즘</li>
          <li>Formal Methods(모델체킹)과 RL의 결합</li>
          <li>안전 제약을 준수하는 제어 정책 생성</li>
          <li>Responsibility-sensitive safety(RSS) 개념 실험</li>
        </ul>

        <h4>6) 고속 레이싱을 위한 통합 AI 연구</h4>
        <ul class="section-text">
          <li>멀티모달 센서 융합</li>
          <li>세계모델(World Model) 기반 주행 예측</li>
          <li>End-to-End Neural Racing</li>
          <li>대규모 데이터 기반 Self-Supervised Learning</li>
        </ul>

        <p class="section-text">
          RoboRacer는 <strong>작고 빠른 플랫폼 덕분에 실험 비용이 매우 낮아</strong>, 고위험 시나리오까지 직접 검증할 수 있다는 장점이 있습니다.
        </p>

        <hr style="margin: 2.5rem 0; border: 0.5px solid #333;">

        <h3>우리 연구실(AiX Lab)에서 집중하는 연구</h3>
        <h4>RL-based Control Synthesis & Lookahead Computation</h4>
        <p class="section-text">
          AiX Lab에서는 RoboRacer 플랫폼을 활용해 다음과 같은 프레임워크를 발전시키고 있습니다.
        </p>

        <h4>1) 강화학습 기반 제어 합성 (RL-based Control Synthesis)</h4>
        <p class="section-text">
          기존 Pure Pursuit, MPC 기반 제어는 <strong>모델 불확실성</strong> 또는 <strong>예측 불일치</strong>에서 한계가 존재합니다.
          우리는 <strong>환경 모델(모델체킹 기반) + RL 정책</strong>을 결합하여
          "안전 제약을 보장하는 학습 기반 제어"를 목표로 합니다.
        </p>

        <h5>연구 내용:</h5>
        <ul class="section-text">
          <li>제약 조건을 내장한 Safe RL Policy 설계</li>
          <li>환경 모델의 reachable set을 RL 제어 정책에 통합</li>
          <li>TTC 기반 위험도 계산과 RL 보상 구조 연계</li>
          <li>시뮬레이터–실차 통합 테스트</li>
        </ul>

        <h4>2) Dynamic Lookahead Computation</h4>
        <p class="section-text">
          순수한 Pure Pursuit은 고정 lookahead를 사용하지만,
          고속 환경에서는 <strong>상황(커브·장애물·속도)에 따라 lookahead를 동적으로 조정해야</strong> 최적 성능을 낼 수 있습니다.
        </p>

        <h5>연구 내용:</h5>
        <ul class="section-text">
          <li>LiDAR 기반 curvature 추정 → 최적 lookahead 계산</li>
          <li>속도 프로파일과 lookahead의 상호 최적화</li>
          <li>race line geometry 기반 adaptive lookahead</li>
          <li>RL 또는 MPC와 lookahead 동시 설계</li>
        </ul>

        <p class="section-text">
          이 연구는 <strong>고속 안정성 확보 + Lap Time 최소화</strong>라는 두 가지 목적을 동시에 달성하는 것을 목표로 합니다.
        </p>

        <p class="section-text" style="margin-top: 2rem;">
          <strong>Related Links:</strong><br>
          • <a href="https://roboracer.or.kr" target="_blank">RoboRacer Korea (roboracer.or.kr)</a><br>
          • <a href="https://f1tenth.org" target="_blank">F1TENTH Official Website</a>
        </p>
      </div>
      
      <!-- English Content -->
      <div id="en-content" class="lang-content" data-lang="en" style="display: none !important;">
        <p class="section-text">
          <strong>RoboRacer</strong> (<a href="https://roboracer.or.kr" target="_blank">roboracer.or.kr</a>) is a high-performance 1/10-scale autonomous racing platform that implements a scaled-down version of the same <strong>sensor–computation–control pipeline</strong> as real vehicles, designed as an open platform for research and education.
        </p>

        <!-- RoboRacer Image -->
        <div style="margin: 2rem 0; text-align: center;">
          <img 
            src="{{ '/research/ai-robot/roboracer/f1tenth.png' | relative_url }}" 
            alt="F1TENTH RoboRacer Platform"
            style="max-width: 45%; border-radius: 0.75rem; border: 1px solid #333;"
          >
          <p style="color: #bdbdbd; font-size: 0.9rem; margin-top: 0.5rem;">
            F1TENTH RoboRacer Platform
          </p>
        </div>

        <h3>Core Objectives of RoboRacer</h3>
        <ul class="section-text">
          <li><strong>Providing a realistic experimental environment for autonomous driving algorithms</strong>
            <br>LiDAR-based perception, local and global planning, control, safety verification, etc.
          </li>
          <li><strong>Building an ecosystem where students, researchers, and industry can share research on a common standard platform</strong></li>
          <li><strong>Providing a racing-based benchmark that dramatically reveals algorithm limitations in real-world driving environments</strong></li>
        </ul>

        <p class="section-text">
          RoboRacer is based on the F1TENTH project initiated by the UPenn PRECISE Lab in the United States,
          and is being developed collaboratively by a global community. In Korea, <strong>RoboRacer Korea</strong> leads the education, research, and competition ecosystem.
        </p>

        <hr style="margin: 2.5rem 0; border: 0.5px solid #333;">

        <h3>Features and Performance of the RoboRacer Platform</h3>
        <p class="section-text">
          The RoboRacer platform is designed by scaling down the structure of real autonomous vehicles, allowing researchers to focus solely on algorithm development.
        </p>

        <h4>Key Features</h4>

        <h5>1) High-Precision 2D LiDAR-Based Perception</h5>
        <ul class="section-text">
          <li>FOV (Field of View) of 270 degrees or more</li>
          <li>Scan rate of approximately 40 Hz</li>
          <li>Stable obstacle detection and tracking in indoor environments</li>
          <li>→ Used for various algorithm experiments including Follow-The-Gap, AEB, SLAM, Tracking, etc.</li>
        </ul>

        <h5>2) High-Performance Embedded Computing</h5>
        <ul class="section-text">
          <li>Capable of mounting high-computation devices such as NVIDIA Jetson/NUC</li>
          <li>ROS 2-based operation</li>
          <li>Can maintain real-time control loops (20–50 Hz)</li>
        </ul>

        <h5>3) Motor·Servo-Based High-Response Driving Control</h5>
        <ul class="section-text">
          <li>VESC-based speed control, supports both Ackermann steering and track-based platforms</li>
          <li>Suitable for high-speed racing with fast steering response</li>
        </ul>

        <h5>4) Full Compatibility Between Simulator and Real Vehicle</h5>
        <ul class="section-text">
          <li>Provides F1TENTH Gym, Gazebo, Isaac-based simulations</li>
          <li>Optimal for simulation-to-reality (Sim2Real) transfer experiments</li>
        </ul>

        <h4>Performance Overview</h4>
        <ul class="section-text">
          <li>Maximum speed: approximately 5–10 m/s (varies by configuration)</li>
          <li>Braking distance and turning radius: nonlinear behavior similar to real vehicles</li>
          <li>Stable in various driving environments (narrow corners, straight acceleration, obstacle avoidance)</li>
        </ul>

        <p class="section-text">
          RoboRacer is not a "simple hobby RC" but a <strong>scientific experimental platform where control theory, AI, and robotics research are validated through actual driving performance</strong>.
        </p>

        <!-- RoboRacer Environment Image -->
        <div style="margin: 2rem 0; text-align: center;">
          <img 
            src="{{ '/research/ai-robot/roboracer/RoboRacer_env.png' | relative_url }}" 
            alt="RoboRacer Environment"
            style="width: 100%; max-width: 100%; border-radius: 0.75rem; border: 1px solid #333;"
          >
          <p style="color: #bdbdbd; font-size: 0.9rem; margin-top: 0.5rem;">
            RoboRacer Racing Environment
          </p>
        </div>

        <hr style="margin: 2.5rem 0; border: 0.5px solid #333;">

        <h3>RoboRacer Competitions</h3>
        <p class="section-text">
          RoboRacer competitions are global racing events that compete on the "actual performance of autonomous driving algorithms."
        </p>

        <!-- RoboRacer Korea 2023 Image -->
        <div style="margin: 2rem 0; text-align: center;">
          <img 
            src="{{ '/research/ai-robot/roboracer/roboracer_korea_2023.jpg' | relative_url }}" 
            alt="RoboRacer Korea 2023"
            style="max-width: 90%; border-radius: 0.75rem; border: 1px solid #333;"
          >
          <p style="color: #bdbdbd; font-size: 0.9rem; margin-top: 0.5rem;">
            RoboRacer Korea 2023
          </p>
        </div>

        <h4>Competition Format</h4>

        <h5>1) Time-Trial Race</h5>
        <p class="section-text">
          The algorithm that completes the track fastest and most stably wins.
          Various approaches are possible, including Pure Pursuit, MPC, RRT*, A*, Gap-Following, and RL-based control.
        </p>

        <h5>2) Head-to-Head Race</h5>
        <p class="section-text">
          Two vehicles start simultaneously. Advanced decision-making is required, including collision avoidance, optimal line selection, and strategic speed control.
        </p>

        <h5>3) Safety & Reliability Challenge</h5>
        <p class="section-text">
          Tests AEB (Automatic Emergency Braking), safety assessment, and TTC (Time-to-Collision)-based collision avoidance.
        </p>

        <h5>4) SLAM & Perception Challenge</h5>
        <p class="section-text">
          Evaluates LiDAR-based SLAM accuracy, localization drift, and dynamic obstacle response capabilities.
        </p>

        <p class="section-text">
          RoboRacer competitions serve as a <strong>benchmark that most clearly demonstrates how research outcomes perform in real-world scenarios</strong>.
        </p>

        <hr style="margin: 2.5rem 0; border: 0.5px solid #333;">

        <h3>Research Enabled by the RoboRacer Platform</h3>
        <p class="section-text">
          RoboRacer is not a simple educational kit but is widely used as a <strong>testing ground for cutting-edge AI and robotics research</strong>.
        </p>

        <h4>1) Perception</h4>
        <ul class="section-text">
          <li>LiDAR-based object detection and tracking</li>
          <li>Signal processing-based noise removal and scan matching</li>
          <li>Real-time environment model learning (SLAM, ICP, NDT, etc.)</li>
        </ul>

        <h4>2) Path Planning</h4>
        <ul class="section-text">
          <li>Optimal track generation (Optimal Racing Line)</li>
          <li>Sampling-based planners such as RRT*/Hybrid A*</li>
          <li>Multiple obstacle avoidance, dynamic environment response</li>
        </ul>

        <h4>3) Control & Driving Policy</h4>
        <ul class="section-text">
          <li>Pure Pursuit, Stanley, PID-based driving</li>
          <li>MPC (Model Predictive Control)-based racing</li>
          <li>Adaptive Lookahead / Speed Profile generation</li>
          <li>Wheel friction-based dynamics modeling</li>
        </ul>

        <h4>4) Reinforcement Learning</h4>
        <ul class="section-text">
          <li>RL-based racing strategy learning</li>
          <li>Safe Reinforcement Learning (Safe RL)</li>
          <li>Simulation-to-reality (Sim2Real) transfer research</li>
          <li>TTC-based risk assessment + policy stabilization</li>
        </ul>

        <h4>5) Autonomous Driving Safety & Verification</h4>
        <ul class="section-text">
          <li>AEB and safe stop algorithms</li>
          <li>Combining Formal Methods (model checking) with RL</li>
          <li>Generating control policies that comply with safety constraints</li>
          <li>Responsibility-sensitive safety (RSS) concept experiments</li>
        </ul>

        <h4>6) Integrated AI Research for High-Speed Racing</h4>
        <ul class="section-text">
          <li>Multimodal sensor fusion</li>
          <li>World Model-based driving prediction</li>
          <li>End-to-End Neural Racing</li>
          <li>Large-scale data-based Self-Supervised Learning</li>
        </ul>

        <p class="section-text">
          RoboRacer has the advantage that <strong>experimental costs are very low due to its small and fast platform</strong>, allowing direct verification of even high-risk scenarios.
        </p>

        <hr style="margin: 2.5rem 0; border: 0.5px solid #333;">

        <h3>Research Focus at Our Lab (AiX Lab)</h3>
        <h4>RL-based Control Synthesis & Lookahead Computation</h4>
        <p class="section-text">
          At AiX Lab, we are advancing the following frameworks using the RoboRacer platform.
        </p>

        <h4>1) Reinforcement Learning-Based Control Synthesis</h4>
        <p class="section-text">
          Existing Pure Pursuit and MPC-based control have limitations in <strong>model uncertainty</strong> or <strong>prediction mismatch</strong>.
          We combine <strong>environment models (model checking-based) + RL policies</strong> to achieve
          "learning-based control that guarantees safety constraints."
        </p>

        <h5>Research Topics:</h5>
        <ul class="section-text">
          <li>Designing Safe RL Policies with embedded constraints</li>
          <li>Integrating reachable sets from environment models into RL control policies</li>
          <li>Linking TTC-based risk calculation with RL reward structures</li>
          <li>Simulator–real vehicle integrated testing</li>
        </ul>

        <h4>2) Dynamic Lookahead Computation</h4>
        <p class="section-text">
          Pure Pure Pursuit uses a fixed lookahead, but
          in high-speed environments, <strong>lookahead must be dynamically adjusted according to the situation (curves, obstacles, speed)</strong> to achieve optimal performance.
        </p>

        <h5>Research Topics:</h5>
        <ul class="section-text">
          <li>LiDAR-based curvature estimation → optimal lookahead calculation</li>
          <li>Mutual optimization of speed profiles and lookahead</li>
          <li>Race line geometry-based adaptive lookahead</li>
          <li>Simultaneous design of RL or MPC with lookahead</li>
        </ul>

        <p class="section-text">
          This research aims to simultaneously achieve two objectives: <strong>ensuring high-speed stability + minimizing Lap Time</strong>.
        </p>

        <p class="section-text" style="margin-top: 2rem;">
          <strong>Related Links:</strong><br>
          • <a href="https://roboracer.or.kr" target="_blank">RoboRacer Korea (roboracer.or.kr)</a><br>
          • <a href="https://f1tenth.org" target="_blank">F1TENTH Official Website</a>
        </p>
      </div>
    </div>
  </div>
</section>

<script>
(function() {
  function initLanguageTabs() {
    const langTabs = document.querySelectorAll('.lang-tab');
    const koContent = document.getElementById('ko-content');
    const enContent = document.getElementById('en-content');

    console.log('Initializing language tabs...');
    console.log('langTabs:', langTabs.length);
    console.log('koContent:', koContent);
    console.log('enContent:', enContent);

    if (!langTabs.length || !koContent || !enContent) {
      console.error('Language elements not found');
      return;
    }

    langTabs.forEach(function(tab) {
      tab.addEventListener('click', function(e) {
        e.preventDefault();
        const lang = this.getAttribute('data-lang');
        console.log('Tab clicked, lang:', lang);

        // Update active tab
        langTabs.forEach(function(t) {
          t.classList.remove('active');
        });
        this.classList.add('active');

        // Show/hide content
        if (lang === 'ko') {
          koContent.style.cssText = 'display: block !important;';
          enContent.style.cssText = 'display: none !important;';
          console.log('Showing Korean content');
        } else if (lang === 'en') {
          enContent.style.cssText = 'display: block !important;';
          koContent.style.cssText = 'display: none !important;';
          console.log('Showing English content');
        }
      });
    });
  }

  // Run when DOM is ready
  if (document.readyState === 'loading') {
    document.addEventListener('DOMContentLoaded', initLanguageTabs);
  } else {
    initLanguageTabs();
  }
})();
</script>

