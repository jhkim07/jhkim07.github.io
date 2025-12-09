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
              <a href="#robot-racing" class="sidebar-menu-link active" data-section="robot-racing">RoboRacer (F1Tenth)</a>
            </li>
            <li class="sidebar-menu-item">
              <a href="#rl-racing-optimization" class="sidebar-menu-link" data-section="rl-racing-optimization">RL Racing Optimization</a>
            </li>
          </ul>
        </nav>
      </aside>

      <!-- 우측 콘텐츠 영역 -->
      <div class="research-content">
        <!-- RoboRacer 섹션 - 동적으로 로드됨 -->
        <div id="robot-racing" class="research-content-section active">
          <div class="loading-placeholder" style="text-align: center; padding: 2rem; color: var(--muted);">
            <p>Loading RoboRacer content...</p>
          </div>
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
  
  // 동적 콘텐츠 로드 함수
  const loadContent = async (sectionId, url) => {
    const section = document.getElementById(sectionId);
    if (!section || section.dataset.loaded === 'true') {
      return; // 이미 로드되었으면 다시 로드하지 않음
    }
    
    try {
      const response = await fetch(url);
      if (!response.ok) {
        throw new Error('Failed to load content');
      }
      
      const html = await response.text();
      const parser = new DOMParser();
      const doc = parser.parseFromString(html, 'text/html');
      
      // .main-content 또는 .container 내부의 내용만 추출
      const mainContent = doc.querySelector('.main-content .container') || doc.querySelector('.container');
      if (mainContent) {
        section.innerHTML = mainContent.innerHTML;
        section.dataset.loaded = 'true';
        
        // 이미지와 링크의 경로는 Jekyll이 이미 절대 경로로 변환했으므로 그대로 사용
        // 필요시 스크립트 재실행을 위한 이벤트 리스너 재등록 등 추가 처리 가능
      }
    } catch (error) {
      console.error('Error loading content:', error);
      section.innerHTML = '<p class="section-text" style="color: var(--muted);">Failed to load content. Please refresh the page.</p>';
    }
  };

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
        
        // RoboRacer 섹션인 경우 동적으로 콘텐츠 로드
        if (targetSection === 'robot-racing') {
          // 현재 페이지 경로를 기준으로 상대 경로 계산
          const currentPath = window.location.pathname;
          const basePath = currentPath.substring(0, currentPath.lastIndexOf('/'));
          const roboracerUrl = basePath + '/roboracer/';
          loadContent('robot-racing', roboracerUrl);
        }
        
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
  } else {
    // 기본적으로 robot-racing 섹션이 활성화되어 있으면 콘텐츠 로드
    const robotRacingSection = document.getElementById('robot-racing');
    if (robotRacingSection && robotRacingSection.classList.contains('active')) {
      // 현재 페이지 경로를 기준으로 상대 경로 계산
      const currentPath = window.location.pathname;
      const basePath = currentPath.substring(0, currentPath.lastIndexOf('/'));
      const roboracerUrl = basePath + '/roboracer/';
      loadContent('robot-racing', roboracerUrl);
    }
  }
});
</script>
