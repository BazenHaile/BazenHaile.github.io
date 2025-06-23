---
layout: splash
permalink: /
header:
  overlay_color: "#1e3d59"
  overlay_filter: "0.3"
  actions:
    - label: "View Portfolio"
      url: "/portfolio/"
      btn_class: "btn--primary btn--large"
    - label: "Download CV"
      url: "/assets/cv/bazen-haile-cv.pdf"
      btn_class: "btn--inverse btn--large"
excerpt: "GIS Analyst & Remote Sensing Specialist passionate about transforming geospatial data into actionable insights for environmental monitoring and sustainable development."

intro: 
  - excerpt: 'Welcome to my portfolio and learning repository where I showcase projects and share knowledge with the geospatial community.'
---

<style>
.feature-card {
  background: white;
  border-radius: 12px;
  box-shadow: 0 8px 25px rgba(0,0,0,0.1);
  overflow: hidden;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
  margin-bottom: 30px;
}

.feature-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 15px 35px rgba(0,0,0,0.2);
}

.card-visual {
  height: 200px;
  position: relative;
  display: flex;
  align-items: center;
  justify-content: center;
  overflow: hidden;
}

.card-content {
  padding: 25px;
  text-align: center;
}

.card-content h3 {
  margin: 0 0 15px 0;
  color: #1e3d59;
  font-size: 1.3em;
}

.card-content p {
  color: #666;
  margin-bottom: 20px;
  line-height: 1.6;
}

/* Remote Sensing Card */
.remote-sensing-bg {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
}

.satellite-icon {
  width: 80px;
  height: 80px;
  background: rgba(255,255,255,0.2);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 40px;
  animation: orbit 8s linear infinite;
  position: relative;
  z-index: 10;
}

.signal-waves {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}

.wave {
  position: absolute;
  border: 2px solid rgba(255,255,255,0.3);
  border-radius: 50%;
  animation: pulse 3s ease-out infinite;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}

.wave:nth-child(1) { width: 60px; height: 60px; animation-delay: 0s; }
.wave:nth-child(2) { width: 100px; height: 100px; animation-delay: 0.5s; }
.wave:nth-child(3) { width: 140px; height: 140px; animation-delay: 1s; }

@keyframes orbit {
  0% { transform: rotate(0deg) translateX(15px) rotate(0deg); }
  100% { transform: rotate(360deg) translateX(15px) rotate(-360deg); }
}

@keyframes pulse {
  0% { opacity: 1; transform: translate(-50%, -50%) scale(0.8); }
  100% { opacity: 0; transform: translate(-50%, -50%) scale(1.2); }
}

/* GIS Projects Card */
.gis-projects-bg {
  background: linear-gradient(135deg, #11998e 0%, #38ef7d 100%);
}

.map-layers {
  position: absolute;
  width: 100%;
  height: 100%;
  opacity: 0.3;
}

.layer {
  position: absolute;
  border-radius: 8px;
  animation: float 6s ease-in-out infinite;
}

.layer:nth-child(1) {
  width: 120px;
  height: 80px;
  background: rgba(255,255,255,0.4);
  top: 20px;
  left: 20px;
  animation-delay: 0s;
}

.layer:nth-child(2) {
  width: 100px;
  height: 60px;
  background: rgba(255,255,255,0.3);
  top: 40px;
  left: 40px;
  animation-delay: 1s;
}

.layer:nth-child(3) {
  width: 80px;
  height: 50px;
  background: rgba(255,255,255,0.2);
  top: 60px;
  left: 60px;
  animation-delay: 2s;
}

.map-icon {
  font-size: 60px;
  z-index: 10;
  position: relative;
  text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
}

@keyframes float {
  0%, 100% { transform: translateY(0px) rotate(0deg); }
  50% { transform: translateY(-10px) rotate(2deg); }
}

/* Learning Notes Card */
.learning-notes-bg {
  background: linear-gradient(135deg, #ffecd2 0%, #fcb69f 100%);
}

.book-stack {
  position: relative;
  z-index: 10;
}

.book {
  width: 60px;
  height: 8px;
  margin: 3px;
  border-radius: 2px;
  animation: stack 4s ease-in-out infinite;
}

.book:nth-child(1) { background: #ff6b6b; animation-delay: 0s; }
.book:nth-child(2) { background: #4ecdc4; animation-delay: 0.2s; }
.book:nth-child(3) { background: #45b7d1; animation-delay: 0.4s; }
.book:nth-child(4) { background: #96ceb4; animation-delay: 0.6s; }
.book:nth-child(5) { background: #feca57; animation-delay: 0.8s; }

.knowledge-particles {
  position: absolute;
  width: 100%;
  height: 100%;
  top: 0;
  left: 0;
}

.particle {
  position: absolute;
  width: 4px;
  height: 4px;
  background: rgba(255,255,255,0.6);
  border-radius: 50%;
  animation: sparkle 3s ease-in-out infinite;
}

.particle:nth-child(1) { top: 20%; left: 30%; animation-delay: 0s; }
.particle:nth-child(2) { top: 40%; left: 70%; animation-delay: 0.5s; }
.particle:nth-child(3) { top: 60%; left: 20%; animation-delay: 1s; }
.particle:nth-child(4) { top: 80%; left: 80%; animation-delay: 1.5s; }
.particle:nth-child(5) { top: 30%; left: 50%; animation-delay: 2s; }

@keyframes stack {
  0%, 100% { transform: translateX(0px); }
  50% { transform: translateX(5px); }
}

@keyframes sparkle {
  0%, 100% { opacity: 0; transform: scale(0); }
  50% { opacity: 1; transform: scale(1); }
}

.skills-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 20px;
  margin: 40px 0;
}

.skill-card {
  background: white;
  padding: 25px;
  border-radius: 10px;
  text-align: center;
  box-shadow: 0 4px 15px rgba(0,0,0,0.1);
  transition: transform 0.3s ease;
}

.skill-card:hover {
  transform: translateY(-3px);
}

.skill-card h4 {
  color: #1e3d59;
  margin-bottom: 15px;
  font-size: 1.1em;
}

.ireland-highlight {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  color: white;
  padding: 40px;
  border-radius: 15px;
  text-align: center;
  margin: 40px 0;
}

.ireland-highlight h2 {
  color: white;
  margin-bottom: 20px;
}

.connect-section {
  background: #f8f9fa;
  padding: 40px;
  border-radius: 12px;
  text-align: center;
  margin: 40px 0;
}

.btn-group {
  margin: 20px 0;
}

.btn-group a {
  margin: 0 10px;
  display: inline-block;
}
</style>

{% include feature_row id="intro" type="center" %}

## Featured Work

<div class="featured-cards-grid">
  <div class="feature-card">
    <div class="card-visual remote-sensing-bg">
      <div class="signal-waves">
        <div class="wave"></div>
        <div class="wave"></div>
        <div class="wave"></div>
      </div>
      <div class="satellite-icon">🛰️</div>
    </div>
    <div class="card-content">
      <h3>🛰️ Remote Sensing Projects</h3>
      <p>Satellite imagery analysis, environmental monitoring, and change detection using Landsat, Sentinel, and commercial datasets.</p>
      <a href="/remote-sensing/" class="btn btn--primary">Explore Projects</a>
    </div>
  </div>

  <div class="feature-card">
    <div class="card-visual gis-projects-bg">
      <div class="map-layers">
        <div class="layer"></div>
        <div class="layer"></div>
        <div class="layer"></div>
      </div>
      <div class="map-icon">🗺️</div>
    </div>
    <div class="card-content">
      <h3>🗺️ GIS Analysis & Mapping</h3>
      <p>Spatial analysis, network modeling, and cartographic design for infrastructure and planning applications.</p>
      <a href="/gis-projects/" class="btn btn--primary">View Projects</a>
    </div>
  </div>

  <div class="feature-card">
    <div class="card-visual learning-notes-bg">
      <div class="knowledge-particles">
        <div class="particle"></div>
        <div class="particle"></div>
        <div class="particle"></div>
        <div class="particle"></div>
        <div class="particle"></div>
      </div>
      <div class="book-stack">
        <div class="book"></div>
        <div class="book"></div>
        <div class="book"></div>
        <div class="book"></div>
        <div class="book"></div>
      </div>
    </div>
    <div class="card-content">
      <h3>📚 Learning Resources</h3>
      <p>Visual tutorials and reference materials for GIS and Remote Sensing concepts, tools, and workflows.</p>
      <a href="/notes/" class="btn btn--primary">Browse Notes</a>
    </div>
  </div>
</div>

## Technical Skills

<div class="skills-grid">
  <div class="skill-card">
    <h4>🖥️ Software Expertise</h4>
    <p><strong>ArcGIS Pro</strong> • <strong>QGIS</strong> • <strong>Google Earth Engine</strong> • <strong>ENVI</strong> • <strong>PostGIS</strong></p>
  </div>
  
  <div class="skill-card">
    <h4>💻 Programming Skills</h4>
    <p><strong>Python</strong> • <strong>R</strong> • <strong>JavaScript</strong> • <strong>SQL</strong> • <strong>ArcPy</strong></p>
  </div>
  
  <div class="skill-card">
    <h4>🛰️ Data Platforms</h4>
    <p><strong>Landsat</strong> • <strong>Sentinel</strong> • <strong>MODIS</strong> • <strong>Planet</strong> • <strong>OSI Ireland</strong></p>
  </div>
</div>

<div class="ireland-highlight">
  <h2>🇮🇪 Ireland-Focused Expertise</h2>
  <p style="font-size: 1.1em; margin-bottom: 20px;">Experienced with Irish coordinate systems (ITM, Irish Grid), Ordnance Survey Ireland data, and familiar with environmental challenges specific to Ireland.</p>
  <p style="margin-bottom: 30px;">Seeking opportunities with Irish organizations in environmental monitoring, urban planning, and geospatial technology.</p>
  <a href="/about/" class="btn btn--inverse btn--large">Learn More About My Background</a>
</div>

## Recent Highlights

<div class="feature__wrapper">
  <div class="feature__item">
    <div class="archive__item">
      <h3>🔥 Latest Project</h3>
      <h4><a href="/portfolio/forest-change/">Forest Change Detection - County Cork</a></h4>
      <p>Multi-temporal analysis using Landsat time series and Google Earth Engine to monitor forest cover changes.</p>
    </div>
  </div>

  <div class="feature__item">
    <div class="archive__item">
      <h3>📚 New Tutorial</h3>
      <h4><a href="/notes/irish-coordinates/">Irish Coordinate Systems Guide</a></h4>
      <p>Comprehensive reference for ITM and Irish Grid systems with practical transformation examples.</p>
    </div>
  </div>

  <div class="feature__item">
    <div class="archive__item">
      <h3>🐍 Code Update</h3>
      <h4><a href="/notes/python-gis/">Python for GIS Workflows</a></h4>
      <p>Essential Python libraries and automation scripts for geospatial analysis and processing.</p>
    </div>
  </div>
</div>

<div class="connect-section">
  <h2>Let's Connect</h2>
  <p>Interested in geospatial collaboration or have questions about my work?</p>
  
  <div class="btn-group">
    <a href="mailto:your.email@example.com" class="btn btn--primary">📧 Email Me</a>
    <a href="https://linkedin.com/in/yourprofile" class="btn btn--info">💼 LinkedIn</a>
    <a href="https://github.com/bazenhaile" class="btn btn--inverse">🐙 GitHub</a>
  </div>
</div>
