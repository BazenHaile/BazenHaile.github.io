---
layout: splash
permalink: /
header:
  overlay_color: "#0a1628"
  overlay_filter: "0.5"
  overlay_image: "/assets/images/ireland-satellite.jpg"
  actions:
    - label: "📊 View Portfolio"
      url: "https://storymaps.arcgis.com/stories/c17fd354712e43a58c23dbbd8db4f417"
      btn_class: "btn--primary btn--large"
    - label: "📄 Download CV"
      url: "/assets/cv/Bazen_Amene_2025_CV.pdf"
      btn_class: "btn--inverse btn--large"
excerpt: "MSc GIS & Remote Sensing graduate from Maynooth University specializing in spatial analysis, satellite imagery processing, and geospatial solutions for environmental monitoring and sustainable development."

intro: 
  - excerpt: 'Transforming spatial data into actionable insights for a sustainable future. Based in Dublin, Ireland 🇮🇪'
---

<style>
/* Modern CSS Variables */
:root {
  --primary-color: #0a1628;
  --secondary-color: #2a4865;
  --accent-color: #00c896;
  --accent-secondary: #00a676;
  --text-dark: #1a1a1a;
  --text-light: #6c757d;
  --bg-light: #f8f9fa;
  --shadow-sm: 0 2px 10px rgba(0,0,0,0.08);
  --shadow-md: 0 5px 20px rgba(0,0,0,0.12);
  --shadow-lg: 0 10px 30px rgba(0,0,0,0.15);
  --border-radius: 16px;
}

/* Hero Section Enhancement */
.page__hero--overlay {
  min-height: 500px;
  background-attachment: fixed;
}

/* Modern Card Grid */
.modern-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
  gap: 30px;
  margin: 60px 0;
}

/* Feature Cards with Glassmorphism */
.feature-card {
  background: rgba(255, 255, 255, 0.95);
  backdrop-filter: blur(10px);
  border-radius: var(--border-radius);
  box-shadow: var(--shadow-sm);
  overflow: hidden;
  transition: all 0.4s cubic-bezier(0.165, 0.84, 0.44, 1);
  border: 1px solid rgba(255, 255, 255, 0.18);
}

.feature-card:hover {
  transform: translateY(-8px);
  box-shadow: var(--shadow-lg);
}

.card-header {
  height: 180px;
  position: relative;
  background: linear-gradient(135deg, var(--secondary-color) 0%, var(--primary-color) 100%);
  display: flex;
  align-items: center;
  justify-content: center;
  overflow: hidden;
}

.card-icon {
  font-size: 4rem;
  color: rgba(255, 255, 255, 0.9);
  z-index: 2;
  animation: float 3s ease-in-out infinite;
}

@keyframes float {
  0%, 100% { transform: translateY(0px); }
  50% { transform: translateY(-10px); }
}

/* Animated Background Patterns */
.pattern-dots {
  position: absolute;
  width: 100%;
  height: 100%;
  opacity: 0.1;
  background-image: radial-gradient(circle, #fff 1px, transparent 1px);
  background-size: 20px 20px;
  animation: slide 20s linear infinite;
}

@keyframes slide {
  from { transform: translateX(0); }
  to { transform: translateX(20px); }
}

.card-content {
  padding: 30px;
}

.card-content h3 {
  color: var(--primary-color);
  font-size: 1.4rem;
  margin-bottom: 15px;
  font-weight: 700;
}

.card-content p {
  color: var(--text-light);
  line-height: 1.7;
  margin-bottom: 20px;
}

/* Modern Buttons */
.btn--modern {
  background: linear-gradient(135deg, var(--accent-color) 0%, var(--accent-secondary) 100%);
  color: white;
  padding: 12px 28px;
  border-radius: 30px;
  text-decoration: none;
  display: inline-block;
  font-weight: 600;
  transition: all 0.3s ease;
  box-shadow: 0 4px 15px rgba(0, 200, 150, 0.3);
}

.btn--modern:hover {
  transform: translateY(-2px);
  box-shadow: 0 6px 20px rgba(0, 200, 150, 0.4);
  color: white;
}

/* Skills Section */
.skills-container {
  background: var(--bg-light);
  border-radius: var(--border-radius);
  padding: 40px;
  margin: 60px 0;
}

.skills-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 25px;
  margin-top: 30px;
}

.skill-category {
  background: white;
  padding: 30px;
  border-radius: 12px;
  box-shadow: var(--shadow-sm);
  transition: all 0.3s ease;
  border-left: 4px solid var(--accent-color);
}

.skill-category:hover {
  transform: translateX(5px);
  box-shadow: var(--shadow-md);
}

.skill-category h4 {
  color: var(--primary-color);
  margin-bottom: 20px;
  display: flex;
  align-items: center;
  gap: 10px;
  font-size: 1.2rem;
}

.skill-tags {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
}

.skill-tag {
  background: rgba(0, 200, 150, 0.1);
  color: var(--accent-secondary);
  padding: 6px 16px;
  border-radius: 20px;
  font-size: 0.9rem;
  font-weight: 500;
  border: 1px solid rgba(0, 200, 150, 0.3);
}

/* Recent Projects Section */
.projects-showcase {
  margin: 60px 0;
}

.project-card {
  background: white;
  border-radius: var(--border-radius);
  overflow: hidden;
  box-shadow: var(--shadow-sm);
  transition: all 0.3s ease;
  display: flex;
  flex-direction: column;
}

.project-card:hover {
  box-shadow: var(--shadow-lg);
  transform: translateY(-5px);
}

.project-image {
  height: 200px;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  position: relative;
  overflow: hidden;
}

.project-badge {
  position: absolute;
  top: 15px;
  right: 15px;
  background: rgba(255, 255, 255, 0.9);
  padding: 5px 15px;
  border-radius: 20px;
  font-size: 0.8rem;
  font-weight: 600;
  color: var(--primary-color);
}

.project-content {
  padding: 25px;
  flex-grow: 1;
  display: flex;
  flex-direction: column;
}

.project-content h3 {
  color: var(--primary-color);
  margin-bottom: 15px;
  font-size: 1.3rem;
}

.project-meta {
  display: flex;
  gap: 20px;
  margin-bottom: 15px;
  font-size: 0.9rem;
  color: var(--text-light);
}

.project-meta span {
  display: flex;
  align-items: center;
  gap: 5px;
}

/* Call to Action Section */
.cta-section {
  background: linear-gradient(135deg, var(--primary-color) 0%, var(--secondary-color) 100%);
  color: white;
  padding: 60px 40px;
  border-radius: var(--border-radius);
  text-align: center;
  margin: 60px 0;
  position: relative;
  overflow: hidden;
}

.cta-section::before {
  content: '';
  position: absolute;
  top: -50%;
  right: -50%;
  width: 200%;
  height: 200%;
  background: radial-gradient(circle, rgba(255,255,255,0.1) 0%, transparent 70%);
  animation: pulse 4s ease-in-out infinite;
}

@keyframes pulse {
  0%, 100% { transform: scale(0.8); opacity: 0.5; }
  50% { transform: scale(1.2); opacity: 0.8; }
}

.cta-content {
  position: relative;
  z-index: 1;
}

.cta-section h2 {
  color: white;
  margin-bottom: 20px;
  font-size: 2.5rem;
}

.cta-section p {
  font-size: 1.2rem;
  margin-bottom: 30px;
  opacity: 0.95;
}

.cta-buttons {
  display: flex;
  gap: 20px;
  justify-content: center;
  flex-wrap: wrap;
}

/* Contact Card */
.contact-card {
  background: white;
  border-radius: var(--border-radius);
  padding: 40px;
  box-shadow: var(--shadow-md);
  text-align: center;
  max-width: 600px;
  margin: 60px auto;
}

.contact-info {
  display: flex;
  justify-content: center;
  gap: 30px;
  margin-top: 30px;
  flex-wrap: wrap;
}

.contact-item {
  display: flex;
  align-items: center;
  gap: 10px;
  color: var(--text-dark);
  text-decoration: none;
  transition: all 0.3s ease;
}

.contact-item:hover {
  color: var(--accent-color);
  transform: translateY(-2px);
}

/* Responsive Design */
@media (max-width: 768px) {
  .modern-grid {
    grid-template-columns: 1fr;
    gap: 20px;
  }
  
  .cta-section h2 {
    font-size: 2rem;
  }
  
  .contact-info {
    flex-direction: column;
    align-items: center;
  }
}

/* Animation for page load */
.fade-in {
  animation: fadeIn 0.8s ease-in-out;
}

@keyframes fadeIn {
  from { opacity: 0; transform: translateY(20px); }
  to { opacity: 1; transform: translateY(0); }
}
</style>

{% include feature_row id="intro" type="center" %}

<section class="modern-grid fade-in">
  <div class="feature-card">
    <div class="card-header">
      <div class="pattern-dots"></div>
      <div class="card-icon">🛰️</div>
    </div>
    <div class="card-content">
      <h3>Remote Sensing Analysis</h3>
      <p>Expert in satellite imagery processing using ERDAS Imagine, SNAP, and Pix4D for environmental monitoring, agricultural assessment, and land cover classification.</p>
      <a href="/remote-sensing/" class="btn--modern">Explore Projects →</a>
    </div>
  </div>

  <div class="feature-card">
    <div class="card-header">
      <div class="pattern-dots"></div>
      <div class="card-icon">🗺️</div>
    </div>
    <div class="card-content">
      <h3>GIS Solutions</h3>
      <p>Proficient in spatial analysis and cartographic design using ArcGIS Pro, QGIS, and PostGIS for urban planning, environmental assessment, and data visualization.</p>
      <a href="/gis-projects/" class="btn--modern">View Portfolio →</a>
    </div>
  </div>

  <div class="feature-card">
    <div class="card-header">
      <div class="pattern-dots"></div>
      <div class="card-icon">📚</div>
    </div>
    <div class="card-content">
      <h3>Educational Resources</h3>
      <p>Comprehensive learning materials and tutorials developed during MSc studies, including interactive Story Maps and technical documentation.</p>
      <a href="/notes/" class="btn--modern">Browse Resources →</a>
    </div>
  </div>
</section>

<section class="skills-container fade-in">
  <h2 style="text-align: center; color: var(--primary-color); margin-bottom: 10px;">Technical Expertise</h2>
  <p style="text-align: center; color: var(--text-light); margin-bottom: 40px;">Comprehensive skillset in modern geospatial technologies</p>
  
  <div class="skills-grid">
    <div class="skill-category">
      <h4><span>💻</span> GIS Software</h4>
      <div class="skill-tags">
        <span class="skill-tag">ArcGIS Pro</span>
        <span class="skill-tag">QGIS</span>
        <span class="skill-tag">ArcGIS Online</span>
        <span class="skill-tag">PostGIS</span>
        <span class="skill-tag">Story Maps</span>
      </div>
    </div>
    
    <div class="skill-category">
      <h4><span>🛰️</span> Remote Sensing</h4>
      <div class="skill-tags">
        <span class="skill-tag">ERDAS Imagine</span>
        <span class="skill-tag">SNAP</span>
        <span class="skill-tag">Pix4D</span>
        <span class="skill-tag">Copernicus Hub</span>
        <span class="skill-tag">GDAL</span>
      </div>
    </div>
    
    <div class="skill-category">
      <h4><span>⚡</span> Programming</h4>
      <div class="skill-tags">
        <span class="skill-tag">Python</span>
        <span class="skill-tag">SQL</span>
        <span class="skill-tag">Django</span>
        <span class="skill-tag">JavaScript</span>
        <span class="skill-tag">R</span>
      </div>
    </div>
  </div>
</section>

<section class="projects-showcase fade-in">
  <h2 style="text-align: center; color: var(--primary-color); margin-bottom: 40px;">Recent Projects</h2>
  
  <div class="modern-grid">
    <div class="project-card">
      <div class="project-image">
        <div class="pattern-dots"></div>
        <span class="project-badge">🏆 Featured</span>
      </div>
      <div class="project-content">
        <h3>5*S Educational Initiative</h3>
        <div class="project-meta">
          <span>📅 2024</span>
          <span>🏢 Ordnance Survey Ireland</span>
        </div>
        <p>Developed interactive educational content using ArcGIS Online for Junior Certificate students, analyzing Copernicus satellite imagery for environmental education.</p>
        <a href="/portfolio/5s-project/" class="btn--modern" style="margin-top: auto;">Learn More →</a>
      </div>
    </div>
    
    <div class="project-card">
      <div class="project-image" style="background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);">
        <div class="pattern-dots"></div>
        <span class="project-badge">📊 Analysis</span>
      </div>
      <div class="project-content">
        <h3>Dublin Urban Growth Analysis</h3>
        <div class="project-meta">
          <span>📅 2024</span>
          <span>🎓 MSc Thesis</span>
        </div>
        <p>Multi-temporal analysis of urban expansion patterns using Landsat imagery and machine learning classification techniques to support sustainable city planning.</p>
        <a href="/portfolio/dublin-urban-growth/" class="btn--modern" style="margin-top: auto;">View Project →</a>
      </div>
    </div>
    
    <div class="project-card">
      <div class="project-image" style="background: linear-gradient(135deg, #4facfe 0%, #00f2fe 100%);">
        <div class="pattern-dots"></div>
        <span class="project-badge">🌍 Remote Sensing</span>
      </div>
      <div class="project-content">
        <h3>Drought Impact Assessment</h3>
        <div class="project-meta">
          <span>📅 2024</span>
          <span>🛰️ Sentinel-2</span>
        </div>
        <p>Vegetation health monitoring using NDVI time-series analysis to assess drought impacts on agricultural regions in Ireland.</p>
        <a href="/portfolio/heatwave-drought/" class="btn--modern" style="margin-top: auto;">Explore →</a>
      </div>
    </div>
  </div>
</section>

<section class="cta-section fade-in">
  <div class="cta-content">
    <h2>Ready to Collaborate?</h2>
    <p>I'm actively seeking opportunities in GIS and Remote Sensing in Ireland.<br>Let's discuss how I can contribute to your team's success.</p>
    <div class="cta-buttons">
      <a href="mailto:bazenhaileam@gmail.com" class="btn btn--inverse btn--large">📧 Get in Touch</a>
      <a href="/assets/cv/Bazen_Amene_2025_CV.pdf" class="btn btn--primary btn--large">📄 Download CV</a>
    </div>
  </div>
</section>

<div class="contact-card fade-in">
  <h3 style="color: var(--primary-color); margin-bottom: 10px;">Connect With Me</h3>
  <p style="color: var(--text-light);">Based in Dublin, Ireland 🇮🇪 | Available for opportunities</p>
  
  <div class="contact-info">
    <a href="mailto:bazenhaileam@gmail.com" class="contact-item">
      <span>📧</span>
      <span>Email</span>
    </a>
    <a href="https://linkedin.com/in/yourprofile" class="contact-item">
      <span>💼</span>
      <span>LinkedIn</span>
    </a>
    <a href="https://github.com/bazenhaile" class="contact-item">
      <span>🐙</span>
      <span>GitHub</span>
    </a>
  </div>
</div>

<script>
// Add fade-in animation on scroll
document.addEventListener('DOMContentLoaded', function() {
  const observerOptions = {
    threshold: 0.1,
    rootMargin: '0px 0px -50px 0px'
  };

  const observer = new IntersectionObserver(function(entries) {
    entries.forEach(entry => {
      if (entry.isIntersecting) {
        entry.target.style.opacity = '1';
        entry.target.style.transform = 'translateY(0)';
      }
    });
  }, observerOptions);

  document.querySelectorAll('.fade-in').forEach(el => {
    el.style.opacity = '0';
    el.style.transform = 'translateY(20px)';
    el.style.transition = 'opacity 0.6s ease, transform 0.6s ease';
    observer.observe(el);
  });
});
</script>
