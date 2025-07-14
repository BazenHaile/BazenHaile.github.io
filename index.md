---
layout: splash
permalink: /
header:
  overlay_color: "#0a1628"
  overlay_filter: "0.6"
  overlay_image: "/assets/images/ireland-satellite.jpg"
  actions:
    - label: "View Portfolio"
      url: "/portfolio/"
      btn_class: "btn--primary btn--large"
    - label: "Download CV"
      url: "/assets/cv/Bazen Amene 2025 CV.pdf"
      btn_class: "btn--inverse btn--large"
excerpt: "MSc GIS & Remote Sensing graduate from Maynooth University specializing in spatial analysis, satellite imagery processing, and geospatial solutions for environmental monitoring and sustainable development."

intro: 
  - excerpt: 'Transforming spatial data into actionable insights for a sustainable future. Based in Dublin, Ireland 🇮🇪'
---

<style>
/* Professional Color Scheme */
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

/* Clean Card Grid */
.feature-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
  gap: 30px;
  margin: 60px 0;
}

.feature-card {
  background: white;
  border-radius: 10px;
  box-shadow: var(--shadow);
  overflow: hidden;
  transition: all 0.3s ease;
  border: 1px solid #e0e0e0;
}

.feature-card:hover {
  transform: translateY(-5px);
  box-shadow: var(--shadow-hover);
  border-color: var(--accent-color);
}

.card-header {
  height: 200px;
  background: linear-gradient(135deg, var(--secondary-color), var(--primary-color));
  display: flex;
  align-items: center;
  justify-content: center;
  position: relative;
  overflow: hidden;
}

.card-icon {
  font-size: 4rem;
  color: rgba(255, 255, 255, 0.9);
  z-index: 1;
}

.card-content {
  padding: 30px;
}

.card-content h3 {
  color: var(--primary-color);
  margin-bottom: 15px;
  font-size: 1.4rem;
  font-weight: 600;
}

.card-content p {
  color: var(--text-light);
  line-height: 1.6;
  margin-bottom: 20px;
}

/* Skills Section */
.skills-section {
  background: var(--bg-light);
  padding: 60px 20px;
  margin: 60px -20px;
}

.skills-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 30px;
  max-width: 1200px;
  margin: 0 auto;
}

.skill-category {
  background: white;
  padding: 30px;
  border-radius: 8px;
  box-shadow: var(--shadow);
  border-left: 4px solid var(--accent-color);
}

.skill-category h4 {
  color: var(--primary-color);
  margin-bottom: 20px;
  font-size: 1.2rem;
  display: flex;
  align-items: center;
  gap: 10px;
}

.skill-list {
  list-style: none;
  padding: 0;
  margin: 0;
}

.skill-list li {
  padding: 8px 0;
  color: var(--text-dark);
  display: flex;
  align-items: center;
  gap: 10px;
}

.skill-list li:before {
  content: "▸";
  color: var(--accent-color);
  font-weight: bold;
}

/* Highlights Section */
.highlights-section {
  margin: 60px 0;
}

.highlight-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 25px;
}

.highlight-card {
  background: white;
  border-radius: 8px;
  padding: 30px;
  box-shadow: var(--shadow);
  transition: all 0.3s ease;
  border-top: 3px solid var(--accent-color);
}

.highlight-card:hover {
  transform: translateY(-3px);
  box-shadow: var(--shadow-hover);
}

.highlight-card h3 {
  color: var(--primary-color);
  margin-bottom: 10px;
  font-size: 1.1rem;
}

.highlight-card .meta {
  color: var(--text-light);
  font-size: 0.9rem;
  margin-bottom: 15px;
}

/* CTA Section */
.cta-section {
  background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
  color: white;
  padding: 60px 40px;
  border-radius: 10px;
  text-align: center;
  margin: 60px 0;
}

.cta-section h2 {
  margin-bottom: 20px;
  font-size: 2.2rem;
}

.cta-section p {
  font-size: 1.1rem;
  margin-bottom: 30px;
  opacity: 0.9;
}

.btn-group {
  display: flex;
  gap: 20px;
  justify-content: center;
  flex-wrap: wrap;
}

/* Professional Button Styles */
.btn--professional {
  background: var(--accent-color);
  color: white;
  padding: 12px 30px;
  border-radius: 5px;
  text-decoration: none;
  display: inline-block;
  font-weight: 500;
  transition: all 0.3s ease;
  border: 2px solid var(--accent-color);
}

.btn--professional:hover {
  background: transparent;
  color: var(--accent-color);
  transform: translateY(-2px);
}

/* Responsive Design */
@media (max-width: 768px) {
  .feature-grid,
  .skills-grid,
  .highlight-grid {
    grid-template-columns: 1fr;
    gap: 20px;
  }
  
  .cta-section h2 {
    font-size: 1.8rem;
  }
  
  .btn-group {
    flex-direction: column;
    align-items: center;
  }
}
</style>

{% include feature_row id="intro" type="center" %}

<section class="feature-grid">
  <div class="feature-card">
    <div class="card-header">
      <div class="card-icon">🛰️</div>
    </div>
    <div class="card-content">
      <h3>Remote Sensing Analysis</h3>
      <p>Expert in satellite imagery processing using ERDAS Imagine, SNAP, and Pix4D for environmental monitoring, agricultural assessment, and land cover classification.</p>
      <a href="/remote-sensing/" class="btn--professional">View Projects</a>
    </div>
  </div>

  <div class="feature-card">
    <div class="card-header">
      <div class="card-icon">🗺️</div>
    </div>
    <div class="card-content">
      <h3>GIS Solutions</h3>
      <p>Proficient in spatial analysis and cartographic design using ArcGIS Pro, QGIS, and PostGIS for urban planning, environmental assessment, and data visualization.</p>
      <a href="/gis-projects/" class="btn--professional">View Projects</a>
    </div>
  </div>

  <div class="feature-card">
    <div class="card-header">
      <div class="card-icon">📊</div>
    </div>
    <div class="card-content">
      <h3>Educational Resources</h3>
      <p>Comprehensive learning materials and tutorials developed during MSc studies and professional projects, including interactive Story Maps and technical documentation.</p>
      <a href="/notes/" class="btn--professional">Browse Resources</a>
    </div>
  </div>
</section>

<section class="skills-section">
  <h2 style="text-align: center; color: var(--primary-color); margin-bottom: 40px;">Technical Expertise</h2>
  
  <div class="skills-grid">
    <div class="skill-category">
      <h4><span>💻</span> GIS Software</h4>
      <ul class="skill-list">
        <li>ArcGIS Pro & ArcGIS Online</li>
        <li>QGIS</li>
        <li>PostGIS & PostgreSQL</li>
        <li>ArcGIS StoryMaps</li>
        <li>ArcGIS Dashboards</li>
      </ul>
    </div>
    
    <div class="skill-category">
      <h4><span>🛰️</span> Remote Sensing</h4>
      <ul class="skill-list">
        <li>ERDAS Imagine</li>
        <li>SNAP (Sentinel Application Platform)</li>
        <li>Pix4D Mapper</li>
        <li>Google Earth Engine</li>
        <li>GDAL/OGR</li>
      </ul>
    </div>
    
    <div class="skill-category">
      <h4><span>⚡</span> Programming & Analysis</h4>
      <ul class="skill-list">
        <li>Python (GeoPandas, Rasterio)</li>
        <li>R for Spatial Statistics</li>
        <li>SQL & Spatial SQL</li>
        <li>JavaScript for Web Mapping</li>
        <li>Django for GIS Applications</li>
      </ul>
    </div>
  </div>
</section>

<section class="highlights-section">
  <h2 style="text-align: center; color: var(--primary-color); margin-bottom: 40px;">Recent Achievements</h2>
  
  <div class="highlight-grid">
    <div class="highlight-card">
      <h3>🎓 5*S Educational Initiative</h3>
      <p class="meta">2024 | Ordnance Survey Ireland</p>
      <p>Developed interactive GIS educational content for Junior Certificate students, integrating Copernicus satellite imagery analysis with curriculum requirements.</p>
      <a href="/portfolio/5s-project/" style="color: var(--accent-color); text-decoration: none; font-weight: 500;">Learn more →</a>
    </div>
    
    <div class="highlight-card">
      <h3>📊 Dublin Urban Growth Analysis</h3>
      <p class="meta">2024 | MSc Thesis Project</p>
      <p>Multi-temporal analysis of urban expansion patterns using Landsat and Sentinel imagery, supporting sustainable city planning initiatives.</p>
      <a href="/portfolio/dublin-urban-growth/" style="color: var(--accent-color); text-decoration: none; font-weight: 500;">View project →</a>
    </div>
    
    <div class="highlight-card">
      <h3>🏆 Ireland Fellows Programme</h3>
      <p class="meta">2020 | Leadership Excellence</p>
      <p>Selected as one of five fellows from Ethiopia for this prestigious programme, demonstrating leadership potential and commitment to sustainable development.</p>
      <a href="/about/" style="color: var(--accent-color); text-decoration: none; font-weight: 500;">Read more →</a>
    </div>
  </div>
</section>

<section class="cta-section">
  <h2>Ready to Collaborate?</h2>
  <p>I'm actively seeking opportunities in GIS and Remote Sensing in Ireland.<br>Let's discuss how I can contribute to your organization's spatial data initiatives.</p>
  <div class="btn-group">
    <a href="/contact/" class="btn btn--inverse btn--large">Get in Touch</a>
    <a href="/assets/cv/Bazen Amene 2025 CV.pdf" class="btn btn--primary btn--large">Download CV</a>
  </div>
</section>
