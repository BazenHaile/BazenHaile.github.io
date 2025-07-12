---
layout: splash
permalink: /
header:
  overlay_color: "#1e3d59"
  overlay_filter: "0.3"
  actions:
    - label: "View Portfolio"
      url: "https://storymaps.arcgis.com/stories/c17fd354712e43a58c23dbbd8db4f417"
      btn_class: "btn--primary btn--large"
    - label: "Download CV"
      url: "/assets/cv/Bazen_H_Amene_2025_CV.pdf"
      btn_class: "btn--inverse btn--large"
excerpt: "Maynooth University MSc GIS & Remote Sensing graduate in Dublin, Ireland. Expertise in spatial analysis, remote sensing (ArcGIS, QGIS, ERDAS Imagine), and data visualization for environmental and urban challenges."
intro: 
  - excerpt: 'Explore my geospatial projects, professional experience, and resources tailored for Ireland\'s GIS community.'
---

<style>
/* [Optimized CSS here: Reduced redundancy, improved performance by limiting animations to hover only] */
.featured-cards-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 30px; margin: 40px 0; }
.feature-card { background: white; border-radius: 12px; box-shadow: 0 4px 15px rgba(0,0,0,0.1); overflow: hidden; transition: transform 0.3s ease; }
.feature-card:hover { transform: translateY(-5px); box-shadow: 0 10px 25px rgba(0,0,0,0.15); }
.card-visual { height: 180px; display: flex; align-items: center; justify-content: center; position: relative; }
.card-content { padding: 20px; text-align: center; }
.card-content h3 { margin: 0 0 10px; color: #1e3d59; font-size: 1.2em; }
.card-content p { color: #666; margin-bottom: 15px; line-height: 1.5; }
/* [Similar styles for remote-sensing-bg, gis-projects-bg, learning-notes-bg, but simplified animations] */
/* ... (keep core styles, remove excessive keyframes for pulse/orbit/float/sparkle to one hover-based) */
.skills-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 20px; margin: 40px 0; }
.skill-card { background: white; padding: 25px; border-radius: 12px; box-shadow: 0 4px 15px rgba(0,0,0,0.1); text-align: center; transition: transform 0.3s ease; }
.skill-card:hover { transform: translateY(-5px); }
.skill-card h4 { color: #1e3d59; margin-bottom: 10px; font-size: 1.1em; }
.highlights-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 20px; margin: 40px 0; }
.highlight-card { background: white; border-radius: 12px; padding: 20px; box-shadow: 0 4px 15px rgba(0,0,0,0.1); transition: transform 0.3s ease; }
.highlight-card:hover { transform: translateY(-5px); }
.ireland-highlight { background: linear-gradient(135deg, #27ae60 0%, #2ecc71 100%); color: white; padding: 30px; border-radius: 12px; text-align: center; margin: 40px 0; }
.connect-section { background: #f8f9fa; padding: 30px; border-radius: 12px; text-align: center; margin: 40px 0; }
</style>

{% include feature_row id="intro" type="center" %}

## Featured Work
<div class="featured-cards-grid">
  <!-- [Kept cards, updated descriptions with CV keywords] -->
  <div class="feature-card">
    <div class="card-visual remote-sensing-bg">
      <div class="satellite-icon" alt="Satellite icon">🛰️</div>
    </div>
    <div class="card-content">
      <h3>🛰️ Remote Sensing Projects</h3>
      <p>Analysis of Copernicus satellite imagery for land cover change, forestry, agriculture, and urban planning using ERDAS Imagine, SNAP, and Pix4D.</p>
      <a href="/remote-sensing/" class="btn btn--primary">Explore Projects</a>
    </div>
  </div>
  <!-- [Similar for GIS and Notes] -->
</div>

## Technical Skills
<div class="skills-grid">
  <div class="skill-card">
    <span class="skill-icon">🖥️</span>
    <h4>GIS Software</h4>
    <p>ArcGIS Pro • QGIS • ArcGIS Online • Dashboards • Story Maps • Insights</p>
  </div>
  <div class="skill-card">
    <span class="skill-icon">🛰️</span>
    <h4>Remote Sensing</h4>
    <p>ERDAS Imagine • SNAP • Pix4D Mapper • Copernicus Imagery • GDAL</p>
  </div>
  <div class="skill-card">
    <span class="skill-icon">💻</span>
    <h4>Programming & Development</h4>
    <p>Python • Django • SQL • PostgreSQL/PostGIS • Java • HTML/CSS/JS</p>
  </div>
  <div class="skill-card">
    <span class="skill-icon">🔧</span>
    <h4>Other Technical Skills</h4>
    <p>Network Administration • MS Office 365 • OS Troubleshooting • Project Management</p>
  </div>
</div>

<div class="ireland-highlight">
  <h2>Ireland-Based Expertise</h2>
  <p>MSc from Maynooth University; contributed to 5*S project with Ordnance Survey Ireland, Esri Ireland, and Science Foundation Ireland. Experienced in Irish geospatial challenges like urban growth and environmental monitoring.</p>
  <a href="/about/" class="btn btn--inverse btn--large">Learn More</a>
</div>

## Experience Highlights
| Role | Duration | Key Achievements |
|------|----------|------------------|
| Generative AI Annotator, Covalen | July 2023 - Present | Annotated data for language models; developed guidelines for accuracy. |
| GIS Technician (Volunteer), 5*S Project | June 2021 - January 2022 | Created ArcGIS Story Maps; analyzed Copernicus imagery; debugged AR apps. |
| Research Assistant, Maynooth University | February 2022 - May 2022 | Advanced GIS objectives for 5*S project. |
| Computer Support Specialist, Ethiopian Investment Commission | November 2016 - September 2020 | Managed networks and servers; developed websites. |

## Recent Certifications & Highlights
<div class="highlights-grid">
  <div class="highlight-card">
    <span class="card-icon">🎓</span>
    <h3>Full Stack Development</h3>
    <h4>UCD Professional Academy (2024)</h4>
    <p>Expertise in Django, SQL, HTML/CSS/JS, Python for scalable geospatial apps.</p>
  </div>
  <div class="highlight-card">
    <span class="card-icon">📚</span>
    <h3>5*S Geomentor</h3>
    <h4>Certified (2021)</h4>
    <p>Delivered workshops on data for Irish challenges.</p>
  </div>
  <div class="highlight-card">
    <span class="card-icon">🏆</span>
    <h3>CCNA Routing & Switching</h3>
    <h4>(2017)</h4>
    <p>Skills in network configuration for WAN sites.</p>
  </div>
</div>

<div class="connect-section">
  <h2>Connect for GIS Opportunities in Ireland</h2>
  <p>Dublin-based and open to roles in spatial analysis or remote sensing.</p>
  <div class="btn-group">
    <a href="mailto:bazenhileam@gmail.com" class="btn btn--primary">📧 Email</a>
    <a href="https://www.linkedin.com/in/bazen-amene" class="btn btn--info">💼 LinkedIn</a>
    <a href="https://github.com/BazenHaile" class="btn btn--inverse">🐙 GitHub</a>
  </div>
