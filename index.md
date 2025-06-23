---
layout: splash
permalink: /
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: /assets/images/hero-bg.jpg
  actions:
    - label: "View Portfolio"
      url: "/portfolio/"
      btn_class: "btn--primary"
    - label: "Download CV"
      url: "/assets/cv/bazen-haile-cv.pdf"
      btn_class: "btn--inverse"
excerpt: "GIS Analyst & Remote Sensing Specialist passionate about transforming geospatial data into actionable insights for environmental monitoring and sustainable development."

intro: 
  - excerpt: 'I combine technical expertise in geospatial analysis with practical problem-solving skills to support decision-making in environmental management, urban planning, and natural resource monitoring.'

feature_row:
  - image_path: assets/images/remote-sensing-thumbnail.jpg
    alt: "Remote Sensing Projects"
    title: "Remote Sensing Projects"
    excerpt: "Satellite imagery analysis, change detection, and environmental monitoring using Landsat, Sentinel, and commercial datasets."
    url: "/remote-sensing/"
    btn_label: "Explore Projects"
    btn_class: "btn--primary"
  - image_path: assets/images/gis-projects-thumbnail.jpg
    alt: "GIS Projects"
    title: "GIS Analysis & Mapping"
    excerpt: "Spatial analysis, cartographic design, and database management for infrastructure, environmental, and social applications."
    url: "/gis-projects/"
    btn_label: "View Work"
    btn_class: "btn--primary"
  - image_path: assets/images/learning-notes-thumbnail.jpg
    alt: "Learning Notes"
    title: "Learning Resources"
    excerpt: "Visual guides, tutorials, and reference materials for GIS and Remote Sensing concepts, tools, and workflows."
    url: "/notes/"
    btn_label: "Browse Notes"
    btn_class: "btn--primary"

feature_row2:
  - image_path: /assets/images/ireland-focus.jpg
    alt: "Ireland Focus"
    title: "Ireland-Focused Expertise"
    excerpt: 'Experienced with **Irish coordinate systems** (ITM, Irish Grid), **Ordnance Survey Ireland** data, and **EU Copernicus** program datasets. Familiar with environmental challenges and opportunities specific to Ireland.'
    url: "/about/"
    btn_label: "Learn More"
    btn_class: "btn--inverse"

skills_row:
  - title: "🛰️ Remote Sensing"
    excerpt: "Landsat, Sentinel-1/2, MODIS, Google Earth Engine, ENVI, SNAP"
  - title: "🗺️ GIS Software"
    excerpt: "ArcGIS Pro, QGIS, PostGIS, FME, ArcGIS Online"
  - title: "💻 Programming"
    excerpt: "Python (ArcPy, GDAL, Rasterio), R, JavaScript, SQL"
---

{% include feature_row id="intro" type="center" %}

## Featured Work

{% include feature_row %}

{% include feature_row id="feature_row2" type="left" %}

## Technical Skills

{% include feature_row id="skills_row" %}

---

## Recent Updates

<div class="grid__wrapper">
  <div class="grid__item">
    <h4><a href="/portfolio/landsat-change-detection/">🔥 New Project: Forest Change Detection</a></h4>
    <p>Multi-temporal analysis of forest cover changes in County Cork using Landsat time series data.</p>
    <small><i class="fas fa-calendar-alt" aria-hidden="true"></i> Posted: {{ site.time | date: "%B %Y" }}</small>
  </div>
  
  <div class="grid__item">
    <h4><a href="/notes/gis-fundamentals/">📚 Updated: GIS Fundamentals Guide</a></h4>
    <p>Comprehensive visual guide to coordinate systems, projections, and spatial data types.</p>
    <small><i class="fas fa-calendar-alt" aria-hidden="true"></i> Updated: {{ site.time | date: "%B %Y" }}</small>
  </div>
</div>

---

## Connect With Me

Ready to discuss geospatial solutions or opportunities in Ireland? 

[📧 Get in Touch](/contact/){: .btn .btn--primary .btn--large}
[💼 LinkedIn](https://linkedin.com/in/yourprofile){: .btn .btn--inverse}
[🐙 GitHub](https://github.com/bazenhaile){: .btn .btn--inverse}
