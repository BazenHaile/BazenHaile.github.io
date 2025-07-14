---
layout: single
title: "About"
permalink: /about/
author_profile: true
classes: wide
---

<style>
/* Matching the homepage style */
:root {
  --primary-color: #0a1628;
  --secondary-color: #1e3d59;
  --accent-color: #00a676;
  --text-dark: #2c3e50;
  --text-light: #5a6c7d;
  --bg-light: #f8f9fa;
  --shadow: 0 4px 6px rgba(0,0,0,0.1);
  --shadow-hover: 0 8px 15px rgba(0,0,0,0.2);
}

/* Hero Section */
.about-hero {
  background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
  color: white;
  padding: 60px 40px;
  border-radius: 10px;
  text-align: center;
  margin-bottom: 60px;
  position: relative;
  overflow: hidden;
}

.about-hero::before {
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

.about-hero h1 {
  position: relative;
  z-index: 1;
  font-size: 2.5rem;
  margin-bottom: 20px;
}

.about-hero p {
  position: relative;
  z-index: 1;
  font-size: 1.2rem;
  opacity: 0.95;
  max-width: 800px;
  margin: 0 auto;
}

/* Content Cards */
.about-section {
  background: white;
  border-radius: 10px;
  padding: 40px;
  margin-bottom: 30px;
  box-shadow: var(--shadow);
  border-left: 4px solid var(--accent-color);
  transition: all 0.3s ease;
}

.about-section:hover {
  transform: translateY(-3px);
  box-shadow: var(--shadow-hover);
}

.about-section h2 {
  color: var(--primary-color);
  margin-bottom: 25px;
  font-size: 1.8rem;
  display: flex;
  align-items: center;
  gap: 15px;
}

.about-section h2 .icon {
  font-size: 1.5rem;
}

/* Education & Experience Timeline */
.timeline-item {
  position: relative;
  padding-left: 40px;
  margin-bottom: 30px;
}

.timeline-item::before {
  content: '';
  position: absolute;
  left: 0;
  top: 5px;
  width: 12px;
  height: 12px;
  background: var(--accent-color);
  border-radius: 50%;
  box-shadow: 0 0 0 3px rgba(0, 166, 118, 0.2);
}

.timeline-item::after {
  content: '';
  position: absolute;
  left: 5px;
  top: 20px;
  width: 2px;
  height: calc(100% + 10px);
  background: #e0e0e0;
}

.timeline-item:last-child::after {
  display: none;
}

.timeline-item h3 {
  color: var(--primary-color);
  margin-bottom: 5px;
  font-size: 1.2rem;
}

.timeline-item .meta {
  color: var(--text-light);
  font-size: 0.95rem;
  margin-bottom: 10px;
}

.timeline-item p {
  color: var(--text-dark);
  line-height: 1.6;
}

/* Skills Grid */
.skills-container {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 20px;
  margin-top: 30px;
}

.skill-card {
  background: var(--bg-light);
  padding: 25px;
  border-radius: 8px;
  text-align: center;
  transition: all 0.3s ease;
  border: 2px solid transparent;
}

.skill-card:hover {
  border-color: var(--accent-color);
  transform: translateY(-3px);
}

.skill-card h4 {
  color: var(--primary-color);
  margin-bottom: 15px;
  font-size: 1.1rem;
}

.skill-card ul {
  list-style: none;
  padding: 0;
  margin: 0;
}

.skill-card li {
  color: var(--text-dark);
  padding: 5px 0;
  font-size: 0.95rem;
}

/* CTA Section */
.about-cta {
  background: linear-gradient(135deg, var(--accent-color), #00a676);
  color: white;
  padding: 50px 40px;
  border-radius: 10px;
  text-align: center;
  margin-top: 60px;
}

.about-cta h2 {
  margin-bottom: 20px;
}

.about-cta p {
  font-size: 1.1rem;
  margin-bottom: 30px;
  opacity: 0.95;
}

.btn-group {
  display: flex;
  gap: 20px;
  justify-content: center;
  flex-wrap: wrap;
}

/* Professional Button */
.btn--professional {
  background: white;
  color: var(--accent-color);
  padding: 12px 30px;
  border-radius: 5px;
  text-decoration: none;
  display: inline-block;
  font-weight: 600;
  transition: all 0.3s ease;
  border: 2px solid white;
}

.btn--professional:hover {
  background: transparent;
  color: white;
  transform: translateY(-2px);
}

/* Responsive */
@media (max-width: 768px) {
  .about-hero h1 {
    font-size: 2rem;
  }
  
  .skills-container {
    grid-template-columns: 1fr;
  }
  
  .btn-group {
    flex-direction: column;
    align-items: center;
  }
}
</style>

<div class="about-hero">
  <h1>Hi, I'm Bazen Amene</h1>
  <p>MSc GIS & Remote Sensing graduate from Maynooth University with a passion for transforming spatial data into actionable insights. Based in Dublin, I specialize in environmental monitoring and sustainable development through geospatial technology.</p>
</div>

<div class="about-section">
  <h2><span class="icon">🎓</span> Education</h2>
  
  <div class="timeline-item">
    <h3>MSc GIS and Remote Sensing</h3>
    <p class="meta">Maynooth University, Ireland | 2021</p>
    <p>Specialized in remote sensing applications, spatial analysis, and geospatial data management. Completed additional modules in SQL databases and advanced programming.</p>
  </div>
  
  <div class="timeline-item">
    <h3>BSc Electrical and Computer Engineering</h3>
    <p class="meta">Mekelle University, Ethiopia | 2016</p>
    <p>Built a strong foundation in computer sciences and engineering, with a focus on programming and system design.</p>
  </div>
</div>

<div class="about-section">
  <h2><span class="icon">💼</span> Professional Journey</h2>
  
  <div class="timeline-item">
    <h3>Generative AI Annotator</h3>
    <p class="meta">Covalen | July 2023 - Present</p>
    <p>Enhancing language model performance through data annotation and developing classification guidelines for major social media platforms.</p>
  </div>
  
  <div class="timeline-item">
    <h3>Research Assistant</h3>
    <p class="meta">Maynooth University | 2022</p>
    <p>Advanced the 5*S educational initiative, applying GIS skills and developing educational content for Science Foundation Ireland.</p>
  </div>
  
  <div class="timeline-item">
    <h3>GIS Technician</h3>
    <p class="meta">5*S Project | 2021-2022</p>
    <p>Created interactive educational content using ArcGIS Online, collaborating with Ordnance Survey Ireland, Esri Ireland, and TU Dublin.</p>
  </div>
</div>

<div class="about-section">
  <h2><span class="icon">🛠️</span> Technical Expertise</h2>
  
  <div class="skills-container">
    <div class="skill-card">
      <h4>🗺️ GIS Platforms</h4>
      <ul>
        <li>ArcGIS Pro</li>
        <li>QGIS</li>
        <li>ArcGIS Online</li>
        <li>PostGIS</li>
      </ul>
    </div>
    
    <div class="skill-card">
      <h4>🛰️ Remote Sensing</h4>
      <ul>
        <li>ERDAS Imagine</li>
        <li>SNAP</li>
        <li>Pix4D Mapper</li>
        <li>GDAL/OGR</li>
      </ul>
    </div>
    
    <div class="skill-card">
      <h4>💻 Development</h4>
      <ul>
        <li>Python</li>
        <li>Django</li>
        <li>SQL</li>
        <li>JavaScript</li>
      </ul>
    </div>
  </div>
</div>

<div class="about-section">
  <h2><span class="icon">🏆</span> Recognition</h2>
  <p><strong>Ireland Fellows Programme (2020)</strong> - Selected as one of only five fellows from Ethiopia for this prestigious leadership development programme, demonstrating commitment to professional growth and international collaboration.</p>
</div>

<div class="about-cta">
  <h2>Let's Work Together</h2>
  <p>I'm actively seeking opportunities in Ireland's geospatial sector where I can apply my expertise in GIS and remote sensing to make a meaningful impact.</p>
  
  <div class="btn-group">
    <a href="/portfolio/" class="btn--professional">View My Work</a>
    <a href="/assets/cv/Bazen Amene 2025 CV.pdf" class="btn--professional">Download CV</a>
    <a href="/contact/" class="btn--professional">Get in Touch</a>
  </div>
</div>
