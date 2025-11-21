---
layout: default
title: "Home"
---

<section id="about" class="section section-hero">
  <div class="container hero-grid">
    <div class="hero-photo">
      <!-- 나중에 assets/images로 옮겨도 됨 -->
      <img src="{{ '/assets/images/main-photo.jpg' | relative_url }}" alt="Jin H Kim">
    </div>
    <div class="hero-text">
      <p class="tagline">Associate Professor · AI Safety & CPS</p>
      <h2>About Me</h2>
      <p>
        I am an <strong>associate professor</strong> in the Department of AI Information Engineering
        at <strong>Gyeongsang National University</strong>. I completed my postdoctoral research
        under the supervision of <strong>Professor Insup Lee</strong> at the University of Pennsylvania.
      </p>

      <p>
        My research interests include <strong>software verification and validation</strong>, especially for
        <strong>cyber-physical systems (CPS)</strong>, and the <strong>safety and trustworthiness of AI</strong>
        in domains such as medical AI and autonomous driving. I recently developed
        <strong>Ophtimus</strong> (Ophthalmological Small Language Models), a domain-specialized ophthalmology LLM
        designed to support reliable clinical decision-making
        (<a href="https://github.com/jinkimh/Ophtimus-Ophthalmology-LLM" target="_blank">GitHub</a>).
      </p>

      <p>
        I have collaborated with groups at the PRECISE Lab of the University of Pennsylvania, KAIST,
        Aalborg University, and INRIA/RISA, and previously worked with advisors including
        <strong>Kim G. Larsen</strong>, <strong>Axel Legay</strong>, and <strong>Sungwon Kang</strong>.
      </p>

      <!-- ⭐ 추가된 이메일 섹션 -->
      <p class="contact-email">
        <strong>Email:</strong>
        <a href="mailto:jin.kim@gnu.ac.kr">jin.kim@gnu.ac.kr</a> |
        <a href="mailto:jhkim07@gmail.com">jhkim07@gmail.com</a>
      </p>
      
    </div>
  </div>
</section>

<section id="research" class="section">
  <div class="container">
    <h2>Research Interests</h2>
    <div class="pill-list">
      <span class="pill">Safety and trustworthiness of AI and Large Language Models</span>
      <span class="pill">Formal verification of CPS</span>
      <span class="pill">Software verification & validation</span>
      <span class="pill">Medical AI (Ophthalmology)</span>
      <span class="pill">Autonomous driving & F1TENTH (RoboRacer)</span>
    </div>
    <p class="section-text">
      I aim to develop methods that provide <strong>formal guarantees</strong> for systems
      that directly affect human lives, combining formal methods, data-driven learning,
      and practical engineering.
    </p>
  </div>
</section>

<section id="news" class="section">
  <div class="container">
    <h2>Latest News</h2>
    <p class="section-text">
      Recent achievements and updates from our research group, including newly accepted
      SCI(E) papers in AI Safety, Medical AI, and Cyber-Physical Systems.
    </p>

    <ul class="section-text">
      <li>
        <strong>Soomin Cho, Inhye Kang, and Jin Hyun Kim</strong>.  
        <em>"From timed automata to go: Formally verified code generation and runtime monitoring for cyber-physical systems."</em>  
        <strong>IEEE Access</strong>, 2025.  
        <span class="pill">Accepted</span>
      </li>

      <li>
        <strong>Jin Hyun Kim et al.</strong>  
        <em>"Low-cost and fast epiretinal membrane detection and quantification based on SD-OCT."</em>  
        <strong>IEEE Access</strong>, 2025.  
        <span class="pill">Accepted</span>
      </li>

      <li>
        <strong>Jin Hyun Kim et al.</strong>  
        <em>"Noise-robust markerless video gait anomaly detection via two-stage acquisition and LSTM autoencoders."</em>  
        <strong>Scientific Reports</strong>, 2025.  
        <span class="pill">Accepted</span>
      </li>

      <li>
        <strong>Jin Hyun Kim et al.</strong>  
        <em>"Ophtimus-V2-Tx: A compact domain-specific LLM for ophthalmic diagnosis and treatment planning."</em>  
        <strong>Scientific Reports</strong>, 2025.  
        <span class="pill">Accepted</span>
      </li>
    </ul>

    <p class="section-text" style="margin-top:1rem;">
      More updates coming soon as our group continues advancing AI Safety, 
      Medical LLMs, and CPS verification research.
    </p>
  </div>
</section>


<section id="contact" class="section">
  <div class="container">
    <h2>Contact</h2>
    <p class="section-text">
      For collaboration or inquiries, please contact me via email.
    </p>
    <p class="contact-email">
      Email: <a href="mailto:jinhkim@gnu.ac.kr">jinhkim@gnu.ac.kr</a>
    </p>
  </div>
</section>
