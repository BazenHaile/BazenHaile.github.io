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

feature_row:
  - image_path: /assets/images/remote-sensing-thumb.jpg
    alt: "Remote Sensing Projects"
    title: "🛰️ Remote Sensing Projects"
    excerpt: "Satellite imagery analysis, environmental monitoring, and change detection using Landsat, Sentinel, and commercial datasets."
    url: "/remote-sensing/"
    btn_label: "Explore Projects"
    btn_class: "btn--primary"
  - image_path: /assets/images/gis-projects-thumb.jpg
    alt: "GIS Projects"
    title: "🗺️ GIS Analysis & Mapping"
    excerpt: "Spatial analysis, network modeling, and cartographic design for infrastructure and planning applications."
    url: "/gis-projects/"
    btn_label: "View Projects"
    btn_class: "btn--primary"
  - image_path: /assets/images/learning-notes-thumb.jpg
    alt: "Learning Notes"
    title: "📚 Learning Resources"
    excerpt: "Visual tutorials and reference materials for GIS and Remote Sensing concepts, tools, and workflows."
    url: "/notes/"
    btn_label: "Browse Notes"
    btn_class: "btn--primary"

skills_row:
  - title: "🖥️ Software Expertise"
    excerpt: "**ArcGIS Pro** • **QGIS** • **Google Earth Engine** • **ENVI** • **PostGIS**"
  - title: "💻 Programming Skills"
    excerpt: "**Python** • **R** • **JavaScript** • **SQL** • **ArcPy**"
  - title: "🛰️ Data Platforms"
    excerpt: "**Landsat** • **Sentinel** • **MODIS** • **Planet** • **OSI Ireland**"
---

{% include feature_row id="intro" type="center" %}

## Featured Work

{% include feature_row %}

## Technical Skills

{% include feature_row id="skills_row" %}

---

<div style="background: linear-gradient(135deg, #667eea 0%, #764ba2 100%); color: white; padding: 40px; border-radius: 10px; text-align: center; margin: 40px 0;">
  <h2 style="color: white; margin-bottom: 20px;"> Ireland-Focused Expertise</h2>
  <p style="font-size: 1.1em; margin-bottom: 20px;">Experienced with Irish coordinate systems (ITM, Irish Grid), Ordnance Survey Ireland data, and familiar with environmental challenges specific to Ireland.</p>
  <p style="margin-bottom: 30px;">Seeking opportunities with Irish organizations in environmental monitoring, urban planning, and geospatial technology.</p>
  <a href="/about/" class="btn btn--inverse btn--large">Learn More About My Background</a>
</div>

---

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

---

<div style="background: #f8f9fa; padding: 30px; border-radius: 8px; text-align: center;">
  <h2>Let's Connect</h2>
  <p>Interested in geospatial collaboration or have questions about my work?</p>
  
  <div style="margin: 20px 0;">
    <a href="mailto:your.email@example.com" class="btn btn--primary">📧 Email Me</a>
    <a href="https://linkedin.com/in/yourprofile" class="btn btn--info">💼 LinkedIn</a>
    <a href="https://github.com/bazenhaile" class="btn btn--inverse">🐙 GitHub</a>
  </div>
</div>
