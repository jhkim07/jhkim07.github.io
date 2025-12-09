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

