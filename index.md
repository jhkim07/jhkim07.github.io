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
