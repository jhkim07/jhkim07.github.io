---
layout: default
title: "AI Robot Projects"
---

<section class="section">
  <div class="container">
    <h2 class="section-title">AI Robot Projects</h2>
    <p class="section-text">
      This page introduces projects on <strong>autonomous driving</strong>,
      <strong>F1TENTH racing</strong>, and <strong>robotic platforms</strong>
      used for education and research on safe AI.
    </p>

    <div class="research-layout">
      <!-- 좌측 사이드바 메뉴 -->
      <aside class="research-sidebar">
        <nav>
          <ul class="sidebar-menu">
            <li class="sidebar-menu-item">
              <a href="#robot-racing" class="sidebar-menu-link active" data-section="robot-racing">RoboRacer</a>
            </li>
            <li class="sidebar-menu-item">
              <a href="#rl-racing-optimization" class="sidebar-menu-link" data-section="rl-racing-optimization">RL Racing Optimization</a>
            </li>
          </ul>
        </nav>
      </aside>

      <!-- 우측 콘텐츠 영역 -->
      <div class="research-content">
        <!-- RoboRacer 섹션 -->
        <div id="robot-racing" class="research-content-section active">
          <h3>RoboRacer</h3>
          <p class="section-text">
            <em>To be Updated</em>
          </p>
        </div>

        <!-- RL Racing Optimization 섹션 -->
        <div id="rl-racing-optimization" class="research-content-section">
          <h3>RL Racing Optimization</h3>
          <p class="section-text">
            <em>To be Updated</em>
          </p>
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
    if (sectionId === 'robot-racing' || sectionId === 'rl-racing-optimization') {
      const link = document.querySelector(`[data-section="${sectionId}"]`);
      if (link) {
        link.click();
      }
    }
  }
});
</script>
