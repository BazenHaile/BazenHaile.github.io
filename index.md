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
excerpt: "MSc GIS & Remote Sensing graduate from Maynooth University with expertise in spatial analysis, satellite imagery processing, and geospatial technology applications for environmental monitoring and sustainable development."

intro: 
  - excerpt: 'Welcome to my portfolio and learning repository where I showcase projects from my MSc studies and professional work, sharing knowledge with the geospatial community.'
---

<style>
.featured-cards-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 30px;
  margin: 40px 0;
}

@media (max-width: 768px) {
  .featured-cards-grid {
    grid-template-columns: 1fr;
  }
}

.feature-card {
  background: white;
  border-radius: 12px;
  box-shadow: 0 8px 25px rgba(0,0,0,0.1);
  overflow: hidden;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
  margin-bottom: 0;
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
  gap: 25px;
  margin: 40px 0;
}

.skill-card {
  background: white;
  padding: 30px 25px;
  border-radius: 15px;
  text-align: center;
  box-shadow: 0 8px 25px rgba(0,0,0,0.1);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
  position: relative;
  overflow: hidden;
}

.skill-card:hover {
  transform: translateY(-8px);
  box-shadow: 0 15px 35px rgba(0,0,0,0.2);
}

.skill-card::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 4px;
  transition: height 0.3s ease;
}

.skill-card:hover::before {
  height: 8px;
}

.skill-card:nth-child(1)::before {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
}

.skill-card:nth-child(2)::before {
  background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
}

.skill-card:nth-child(3)::before {
  background: linear-gradient(135deg, #4facfe 0%, #00f2fe 100%);
}

.skill-card h4 {
  color: #1e3d59;
  margin-bottom: 15px;
  font-size: 1.2em;
  font-weight: 600;
}

.skill-card .skill-icon {
  font-size: 2.5em;
  margin-bottom: 15px;
  display: block;
  animation: bounce 2s ease-in-out infinite;
}

.skill-card:nth-child(1) .skill-icon { animation-delay: 0s; }
.skill-card:nth-child(2) .skill-icon { animation-delay: 0.3s; }
.skill-card:nth-child(3) .skill-icon { animation-delay: 0.6s; }

@keyframes bounce {
  0%, 20%, 50%, 80%, 100% { transform: translateY(0); }
  40% { transform: translateY(-10px); }
  60% { transform: translateY(-5px); }
}

.highlights-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 25px;
  margin: 40px 0;
}

.highlight-card {
  background: white;
  border-radius: 15px;
  padding: 25px;
  box-shadow: 0 8px 25px rgba(0,0,0,0.1);
  transition: all 0.3s ease;
  position: relative;
  overflow: hidden;
}

.highlight-card:hover {
  transform: translateY(-5px) scale(1.02);
  box-shadow: 0 15px 35px rgba(0,0,0,0.2);
}

.highlight-card::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 5px;
}

.highlight-card:nth-child(1)::before {
  background: linear-gradient(135deg, #ff6b6b 0%, #ee5a24 100%);
}

.highlight-card:nth-child(2)::before {
  background: linear-gradient(135deg, #a55eea 0%, #8e44ad 100%);
}

.highlight-card:nth-child(3)::before {
  background: linear-gradient(135deg, #26de81 0%, #20bf6b 100%);
}

.highlight-card .card-icon {
  font-size: 2em;
  margin-bottom: 10px;
  display: inline-block;
  animation: rotate 4s ease-in-out infinite;
}

.highlight-card:nth-child(1) .card-icon { animation-delay: 0s; }
.highlight-card:nth-child(2) .card-icon { animation-delay: 1s; }
.highlight-card:nth-child(3) .card-icon { animation-delay: 2s; }

@keyframes rotate {
  0%, 100% { transform: rotate(0deg); }
  25% { transform: rotate(5deg); }
  75% { transform: rotate(-5deg); }
}

.highlight-card h3 {
  color: #1e3d59;
  margin: 0 0 10px 0;
  font-size: 1.1em;
  font-weight: 600;
}

.highlight-card h4 {
  margin: 0 0 15px 0;
  font-size: 1em;
}

.highlight-card h4 a {
  color: #2c5aa0;
  text-decoration: none;
  transition: color 0.3s ease;
}

.highlight-card h4 a:hover {
  color: #1e3d59;
}

.highlight-card p {
  color: #666;
  line-height: 1.6;
  margin: 0;
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
      <p>Satellite imagery analysis using ERDAS Imagine, SNAP, and Pix4D for land cover monitoring, and agricultural planning.</p>
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
      <p>Spatial analysis and cartographic design using ArcGIS Pro, QGIS, and PostGIS for educational content and research applications.</p>
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
      <p>Educational materials and tutorials developed during MSc studies and the 5*S project, including Story Maps and interactive content.</p>
      <a href="/notes/" class="btn btn--primary">Browse Notes</a>
    </div>
  </div>
</div>

## Technical Skills

<div class="skills-grid">
  <div class="skill-card">
    <span class="skill-icon">🖥️</span>
    <h4>GIS Software</h4>
    <p><strong>ArcGIS Pro</strong> • <strong>QGIS</strong> • <strong>ArcGIS Online</strong> • <strong>ArcGIS Dashboards</strong> • <strong>Story Maps</strong></p>
  </div>
  
  <div class="skill-card">
    <span class="skill-icon">🛰️</span>
    <h4>Remote Sensing</h4>
    <p><strong>ERDAS Imagine</strong> • <strong>SNAP</strong> • <strong>Pix4D Mapper</strong> • <strong>Copernicus Imagery</strong> • <strong>GDAL</strong></p>
  </div>
  
  <div class="skill-card">
    <span class="skill-icon">💻</span>
    <h4>Programming & Development</h4>
    <p><strong>Python</strong> • <strong>Django</strong> • <strong>JavaScript</strong> • <strong>SQL</strong> • <strong>PostgreSQL/PostGIS</strong></p>
  </div>
</div>

<div class="ireland-highlight">
  <h2>🇮🇪 Ireland-Based Experience</h2>
  <p style="font-size: 1.1em; margin-bottom: 20px;">MSc graduate from Maynooth University with hands-on experience working on Irish geospatial projects including the 5*S educational initiative with Ordnance Survey Ireland.</p>
  <p style="margin-bottom: 30px;">Contributed to Science Foundation Ireland-funded projects and collaborated with Esri Ireland and Society of Chartered Surveyors Ireland.</p>
  <a href="/about/" class="btn btn--inverse btn--large">Learn More About My Background</a>
</div>

## Recent Highlights

<div class="highlights-grid">
  <div class="highlight-card">
    <span class="card-icon">🎓</span>
    <h3>Latest Achievement</h3>
    <h4><a href="/portfolio/5s-project/">5*S Educational Project</a></h4>
    <p>Developed interactive educational content using ArcGIS Online for Junior Cert students, analyzing Copernicus satellite imagery.</p>
  </div>

  <div class="highlight-card">
    <span class="card-icon">📚</span>
    <h3>New Certification</h3>
    <h4><a href="/notes/gdal-mastery/">GDAL Tools Mastery</a></h4>
    <p>Completed intensive hands-on course with Spatial Thoughts covering GDAL & OGR command-line workflows and automation.</p>
  </div>

  <div class="highlight-card">
    <span class="card-icon">🏆</span>
    <h3>Recognition</h3>
    <h4><a href="/about/">Ireland Fellows Programme</a></h4>
    <p>Selected as one of five fellows from Ethiopia in 2020 for this prestigious leadership development programme.</p>
  </div>
</div>

<div class="connect-section">
  <h2>Let's Connect</h2>
  <p>Based in Dublin and interested in geospatial collaboration or career opportunities in Ireland?</p>
  
  <div class="btn-group">
    <a href="mailto:bazenhaileam@gmail.com" class="btn btn--primary">📧 Email Me</a>
    <a href="https://linkedin.com/in/yourprofile" class="btn btn--info">💼 LinkedIn</a>
    <a href="https://github.com/bazenhaile" class="btn btn--inverse">🐙 GitHub</a>
  </div>
</div>
