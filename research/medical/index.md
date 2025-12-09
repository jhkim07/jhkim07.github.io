---
layout: default
title: "Medical AI Projects"
---

<section class="section">
  <div class="container">
    <h2 class="section-title">Medical AI Projects</h2>
    <p class="section-text">
      This page summarizes ongoing and past projects in
      <strong>medical AI</strong>, with a particular focus on
      ophthalmology, retinal imaging, and trustworthy clinical decision
      support.
    </p>

    <div class="research-layout">
      <!-- 좌측 사이드바 메뉴 -->
      <aside class="research-sidebar">
        <nav>
          <ul class="sidebar-menu">
            <li class="sidebar-menu-item">
              <a href="#medical-llm" class="sidebar-menu-link active" data-section="medical-llm">Medical LLM</a>
            </li>
            <li class="sidebar-menu-item">
              <a href="#erm-quantification" class="sidebar-menu-link" data-section="erm-quantification">ERM Quantification</a>
            </li>
            <li class="sidebar-menu-item">
              <a href="#gait-anomaly-detection" class="sidebar-menu-link" data-section="gait-anomaly-detection">Gait Anomaly Detection</a>
            </li>
          </ul>
        </nav>
      </aside>

      <!-- 우측 콘텐츠 영역 -->
      <div class="research-content">
        <!-- Medical LLM 섹션 -->
        <div id="medical-llm" class="research-content-section active">
          {% include_relative medical-llm.md %}
        </div>

        <!-- ERM Quantification 섹션 -->
        <div id="erm-quantification" class="research-content-section">
          {% include_relative erm-quantification.md %}
        </div>

        <!-- Gait Anomaly Detection 섹션 -->
        <div id="gait-anomaly-detection" class="research-content-section">
          {% include_relative gait-anomaly-detection.md %}
        </div>
      </div>
    </div>
  </div>
</section>

<script>
document.addEventListener('DOMContentLoaded', function() {
  const menuLinks = document.querySelectorAll('.sidebar-menu-link');
  const contentSections = document.querySelectorAll('.research-content-section');

  menuLinks.forEach(link => {
    link.addEventListener('click', function(e) {
      e.preventDefault();
      
      const targetSection = this.getAttribute('data-section');
      
      // Remove active class from all links and sections
      menuLinks.forEach(l => l.classList.remove('active'));
      contentSections.forEach(s => s.classList.remove('active'));
      
      // Add active class to clicked link and corresponding section
      this.classList.add('active');
      const section = document.getElementById(targetSection);
      if (section) {
        section.classList.add('active');
        // Scroll to top of content area
        section.scrollIntoView({ behavior: 'smooth', block: 'start' });
      }
    });
  });

  // Handle hash navigation on page load
  const hash = window.location.hash;
  if (hash) {
    const sectionId = hash.replace('#', '');
    if (sectionId === 'medical-llm' || sectionId === 'erm-quantification' || sectionId === 'gait-anomaly-detection') {
      const link = document.querySelector(`[data-section="${sectionId}"]`);
      if (link) {
        link.click();
      }
    }
  }
});
</script>
