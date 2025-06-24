---
layout: splash
title: "Portfolio"
permalink: /portfolio/
header:
  overlay_color: "#1e3d59"
  overlay_filter: "0.4"
excerpt: "Geospatial projects showcasing remote sensing analysis, climate monitoring, and interactive visualization"
---

<style>
/* Hero Featured Project */
.hero-project {
  background: linear-gradient(135deg, #ff6b6b 0%, #ee5a24 100%);
  border-radius: 20px;
  padding: 0;
  margin: 40px 0 60px 0;
  overflow: hidden;
  box-shadow: 0 15px 40px rgba(0,0,0,0.2);
}

.hero-content {
  display: grid;
  grid-template-columns: 1fr 1fr;
  min-height: 400px;
  align-items: center;
}

@media (max-width: 768px) {
  .hero-content {
    grid-template-columns: 1fr;
    text-align: center;
  }
}

.hero-text {
  padding: 40px;
  color: white;
}

.hero-text h2 {
  color: white;
  font-size: 2.2em;
  margin-bottom: 15px;
  font-weight: 700;
}

.hero-visual {
  background: rgba(255,255,255,0.1);
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  position: relative;
  min-height: 400px;
  font-size: 4em;
}

.projects-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
  gap: 30px;
  margin: 40px 0;
}

.project-card {
  background: white;
  border-radius: 15px;
  overflow: hidden;
  box-shadow: 0 8px 25px rgba(0,0,0,0.1);
  transition: all 0.3s ease;
}

.project-card:hover {
  transform: translateY(-8px);
  box-shadow: 0 20px 40px rgba(0,0,0,0.2);
}

.project-header {
  height: 180px;
  display: flex;
  align-items: center;
  justify-content: center;
  color: white;
  font-size: 2.5em;
}

.project-content {
  padding: 25px;
}

.project-content h3 {
  color: #1e3d59;
  margin-bottom: 10px;
}

.project-meta {
  color: #666;
  font-size: 0.9em;
  margin-bottom: 15px;
  font-style: italic;
}

.project-description {
  color: #444;
  line-height: 1.6;
  margin-bottom: 20px;
}

.tag {
  display: inline-block;
  background: #f0f2f5;
  color: #1e3d59;
  padding: 4px 12px;
  border-radius: 15px;
  font-size: 0.8em;
  margin: 2px 4px 2px 0;
}

.btn-group {
  margin-top: 15px;
}

.btn-group a {
  margin-right: 10px;
  margin-bottom: 5px;
}
</style>

## Featured Project

<div class="hero-project">
  <div class="hero-content">
    <div class="hero-text">
      <div style="background: rgba(255,255,255,0.2); color: white; padding: 5px 15px; border-radius: 20px; font-size: 0.9em; display: inline-block; margin-bottom: 20px;">🏆 Featured StoryMap</div>
      <h2>A Summer of Heatwaves and Droughts</h2>
      <p style="font-size: 1.1em; line-height: 1.6; margin-bottom: 25px;">Interactive geospatial analysis examining extreme weather patterns using satellite imagery and climate data.</p>
      
      <div style="margin-top: 20px;">
        <a href="https://storymaps.arcgis.com/stories/c17fd354712e43a58c23dbbd8db4f417" target="_blank" class="btn btn--inverse btn--large">🔗 View StoryMap</a>
        <a href="/portfolio/heatwave-drought/" class="btn btn--light btn--large">📋 Project Details</a>
      </div>
    </div>
    
    <div class="hero-visual">
      🌡️🔥
    </div>
  </div>
</div>

## All Projects

<div class="projects-grid">
{% for project in site.portfolio %}
  <div class="project-card">
    <div class="project-header" style="background: {{ project.header_color | default: 'linear-gradient(135deg, #667eea 0%, #764ba2 100%)' }};">
      <span>{{ project.icon | default: '🗺️' }}</span>
    </div>
    <div class="project-content">
      <h3>{{ project.title }}</h3>
      <div class="project-meta">{{ project.category | default: 'GIS Project' }} • {{ project.year | default: '2024' }}</div>
      <div class="project-description">{{ project.excerpt }}</div>
      <div style="margin-bottom: 20px;">
        {% for tag in project.tags %}
          <span class="tag">{{ tag }}</span>
        {% endfor %}
      </div>
      <div class="btn-group">
        <a href="{{ project.url }}" class="btn btn--primary">View Project</a>
        {% if project.external_url %}
          <a href="{{ project.external_url }}" target="_blank" class="btn btn--info">🔗 Live Demo</a>
        {% endif %}
      </div>
    </div>
  </div>
{% endfor %}
</div>

## Project Statistics

<div style="background: #f8f9fa; padding: 30px; border-radius: 15px; margin: 40px 0; text-align: center;">
  <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 20px;">
    <div>
      <h3 style="color: #1e3d59; font-size: 2em; margin-bottom: 5px;">{{ site.portfolio.size }}</h3>
      <p style="color: #666; margin: 0;">Projects Completed</p>
    </div>
    <div>
      <h3 style="color: #1e3d59; font-size: 2em; margin-bottom: 5px;">4+</h3>
      <p style="color: #666; margin: 0;">Technologies Used</p>
    </div>
    <div>
      <h3 style="color: #1e3d59; font-size: 2em; margin-bottom: 5px;">2024</h3>
      <p style="color: #666; margin: 0;">Latest Projects</p>
    </div>
  </div>
</div>

---

## 🚀 **About This Portfolio**

This collection showcases my journey in geospatial technology, from academic research at Maynooth University to professional applications in climate analysis and educational content development. Each project demonstrates practical application of GIS and remote sensing skills using industry-standard tools.

**Want to collaborate?** [Get in touch →](/contact/)
