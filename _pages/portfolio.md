# Portfolio Pages Structure

## Main Portfolio Landing Page (_pages/portfolio.md)
---
layout: collection
title: "Portfolio"
permalink: /portfolio/
collection: portfolio
entries_layout: grid
classes: wide
header:
  overlay_color: "#1e3d59"
  overlay_image: /assets/images/portfolio-header.jpg
  excerpt: "Explore my GIS and Remote Sensing projects showcasing environmental monitoring, spatial analysis, and data visualization capabilities."
---

## Featured Projects

<div class="feature__wrapper">
  <div class="feature__item--left">
    <div class="archive__item">
      <div class="archive__item-teaser">
        <img src="/assets/images/featured-project-1.jpg" alt="Featured Project">
      </div>
      <div class="archive__item-body">
        <h2 class="archive__item-title">🔥 Forest Change Detection Ireland</h2>
        <div class="archive__item-excerpt">
          <p>Multi-temporal analysis of forest cover changes across Irish counties using Landsat time series data and Google Earth Engine.</p>
          <p><strong>Skills:</strong> Remote Sensing, Time Series Analysis, Change Detection</p>
        </div>
        <p><a href="/portfolio/forest-change-detection/" class="btn btn--primary">View Project</a></p>
      </div>
    </div>
  </div>
</div>

---

## Project Categories

### 🛰️ Remote Sensing Projects
[View All Remote Sensing Projects](/remote-sensing/){: .btn .btn--primary}

### 🗺️ GIS Analysis & Mapping  
[View All GIS Projects](/gis-projects/){: .btn .btn--success}

### 📊 Data Visualization
[View Visualization Projects](/data-viz/){: .btn .btn--info}

---

## Remote Sensing Projects Page (_pages/remote-sensing.md)
---
layout: single
title: "Remote Sensing Projects"
permalink: /remote-sensing/
classes: wide
header:
  overlay_color: "#2c3e50"
  overlay_image: /assets/images/satellite-header.jpg
---

## Satellite Data Analysis & Environmental Monitoring

<div class="grid__wrapper">
{% for post in site.portfolio %}
  {% if post.categories contains "remote-sensing" %}
  <div class="grid__item">
    <div class="archive__item">
      <div class="archive__item-teaser">
        <img src="{{ post.header.teaser }}" alt="{{ post.title }}">
      </div>
      <div class="archive__item-body">
        <h2 class="archive__item-title">
          <a href="{{ post.url }}">{{ post.title }}</a>
        </h2>
        <div class="archive__item-excerpt">
          {{ post.excerpt | markdownify }}
          <p><strong>{{ post.software }}</strong> | {{ post.data_source }}</p>
        </div>
      </div>
    </div>
  </div>
  {% endif %}
{% endfor %}
</div>

---

## GIS Projects Page (_pages/gis-projects.md)
---
layout: single
title: "GIS Analysis & Mapping"
permalink: /gis-projects/
classes: wide
header:
  overlay_color: "#27ae60"
  overlay_image: /assets/images/gis-header.jpg
---

## Spatial Analysis & Cartographic Design

<div class="grid__wrapper">
{% for post in site.portfolio %}
  {% if post.categories contains "gis" %}
  <div class="grid__item">
    <div class="archive__item">
      <div class="archive__item-teaser">
        <img src="{{ post.header.teaser }}" alt="{{ post.title }}">
      </div>
      <div class="archive__item-body">
        <h2 class="archive__item-title">
          <a href="{{ post.url }}">{{ post.title }}</a>
        </h2>
        <div class="archive__item-excerpt">
          {{ post.excerpt | markdownify }}
          <p><strong>{{ post.software }}</strong> | {{ post.analysis_type }}</p>
        </div>
      </div>
    </div>
  </div>
  {% endif %}
{% endfor %}
</div>

---

## Sample Project Template (_portfolio/forest-change-detection.md)
---
title: "Forest Cover Change Detection - County Cork"
excerpt: "Multi-temporal analysis of forest cover changes using Landsat time series data and machine learning classification"
categories: ["remote-sensing", "environmental"]
software: "Google Earth Engine, Python, QGIS"
data_source: "Landsat 8 OLI, Sentinel-2"
skills: ["Time Series Analysis", "Change Detection", "Machine Learning", "JavaScript"]
header:
  image: /assets/images/forest-change-header.jpg
  teaser: /assets/images/forest-change-teaser.jpg
gallery:
  - url: /assets/images/forest-before-2015.jpg
    image_path: /assets/images/forest-before-2015.jpg
    alt: "Forest cover 2015"
    title: "Forest Cover - 2015"
  - url: /assets/images/forest-after-2023.jpg
    image_path: /assets/images/forest-after-2023.jpg
    alt: "Forest cover 2023"
    title: "Forest Cover - 2023"
  - url: /assets/images/change-map.jpg
    image_path: /assets/images/change-map.jpg
    alt: "Change detection results"
    title: "Detected Changes"
---

## Project Overview

This project analyzes forest cover changes in County Cork, Ireland, over an 8-year period (2015-2023) using Landsat 8 satellite imagery. The analysis identifies areas of deforestation, afforestation, and forest management activities to support sustainable forest management decisions.

### Objectives
- **Quantify** forest cover changes over time
- **Identify** hotspots of deforestation/afforestation
- **Assess** the effectiveness of forest protection policies
- **Provide** actionable insights for local forest management

---

## Methodology

### 1. Data Acquisition & Preprocessing
```javascript
// Google Earth Engine code snippet
var ireland = ee.FeatureCollection("users/username/ireland_counties")
                .filter(ee.Filter.eq('NAME_1', 'Cork'));

var landsat = ee.ImageCollection('LANDSAT/LC08/C02/T1_L2')
                .filterBounds(ireland)
                .filterDate('2015-01-01', '2023-12-31')
                .filter(ee.Filter.lt('CLOUD_COVER', 20));
```

**Data Sources:**
- **Landsat 8 OLI** Surface Reflectance (30m resolution)
- **Sentinel-2** MSI for validation (10m resolution)
- **OSI Forest Cover Map** for training data
- **EPA Ireland** protected areas boundaries

### 2. Image Classification
Applied **Random Forest** classifier with spectral indices:
- **NDVI** (Normalized Difference Vegetation Index)
- **EVI** (Enhanced Vegetation Index)
- **NDMI** (Normalized Difference Moisture Index)
- **Textural features** from GLCM analysis

### 3. Change Detection Algorithm
Implemented **pixel-based change detection** using:
- Pre-classification comparison
- Change vector analysis
- Post-classification comparison
- Confidence thresholding (>85%)

---

## Key Results

{% include gallery caption="Forest cover changes from 2015 to 2023 in County Cork" %}

### Quantitative Findings
- **Total forest loss**: 2,847 hectares (3.2% of total forest area)
- **Forest gain**: 1,234 hectares (new plantations)
- **Net forest change**: -1,613 hectares
- **Primary drivers**: Urban expansion (45%), agriculture conversion (35%), forest management (20%)

### Spatial Patterns
- **Highest loss rates**: Near Cork city and major towns
- **Conservation success**: National parks showed <0.5% loss
- **Afforestation hotspots**: Marginal agricultural lands in upland areas

---

## Technical Implementation

### Processing Workflow
```python
# Python pseudocode for change detection
import ee
import numpy as np

def classify_forest_cover(image, training_data):
    """Random Forest classification for forest/non-forest"""
    bands = ['B2', 'B3', 'B4', 'B5', 'B6', 'B7']
    indices = calculate_indices(image)
    
    classifier = ee.Classifier.smileRandomForest(100) \
                   .train(training_data, 'landcover', bands + indices)
    
    return image.classify(classifier)

def detect_changes(image1, image2, threshold=0.85):
    """Pixel-based change detection"""
    change_magnitude = image1.subtract(image2).abs()
    return change_magnitude.gt(threshold)
```

### Validation & Accuracy Assessment
- **Overall accuracy**: 91.3%
- **Producer's accuracy (forest)**: 88.7%
- **User's accuracy (forest)**: 93.1%
- **Kappa coefficient**: 0.89

**Validation methods:**
- Independent test dataset (30% of reference points)
- Visual interpretation of high-resolution imagery
- Field verification (limited sample)

---

## Practical Applications

### For Forest Management
- **Monitoring compliance** with forest licenses
- **Early detection** of illegal logging
- **Planning reforestation** in optimal locations
- **Assessing fire damage** and recovery

### For Policy Making
- **Evidence-based** forest protection policies
- **Impact assessment** of development projects
- **Carbon stock** estimation for climate reporting
- **Biodiversity conservation** planning

### For Stakeholders
- **Landowners**: Sustainable management guidance
- **Government**: Regulatory compliance monitoring
- **NGOs**: Conservation priority identification
- **Researchers**: Long-term trend analysis

---

## Interactive Results

<div style="background: #f8f9fa; padding: 20px; border-radius: 8px; margin: 20px 0;">
  <h4>🌍 Interactive Map</h4>
  <p><strong>Note:</strong> Interactive map would be embedded here showing:</p>
  <ul>
    <li>Before/after imagery slider</li>
    <li>Change detection results overlay</li>
    <li>Clickable areas for detailed information</li>
    <li>Legend and data sources</li>
  </ul>
  <p><a href="/assets/maps/forest-change-interactive.html" class="btn btn--primary">View Full Interactive Map</a></p>
</div>

---

## Code & Data Access

### Repository Links
- **📁 GitHub Repository**: [Forest-Change-Detection-Cork](https://github.com/bazenhaile/forest-change-cork)
- **🌍 Google Earth Engine**: [Public GEE Script](https://code.earthengine.google.com/your-script-id)
- **📊 Data Portal**: [Processing Results](https://drive.google.com/folder/your-data-folder)

### Reproducibility
All code is documented and includes:
- Step-by-step processing scripts
- Parameter files and configurations
- Sample datasets for testing
- Detailed README with setup instructions

---

## Future Enhancements

### Technical Improvements
- **Deep learning** classification using CNN/U-Net
- **Multi-sensor fusion** (optical + SAR data)
- **Real-time monitoring** system development
- **Automated reporting** pipeline

### Expanded Analysis
- **Species-level** forest classification
- **Carbon stock** estimation
- **Fire risk** assessment modeling
- **Climate change** impact projections

---

## Project Impact

> *"This analysis provided crucial data for updating our county forest management plan. The spatial precision and temporal coverage exceeded our expectations."*
> 
> **— Forest Service Representative, Cork County Council**

### Recognition
- **Presented** at Irish Geospatial Conference 2023
- **Published** in Journal of Environmental Monitoring (pending)
- **Featured** in EPA Ireland quarterly newsletter

---

## Contact & Collaboration

Interested in similar analysis for your area or organization? I'm open to:
- **Consulting projects** for forest monitoring
- **Research collaborations** on environmental change detection
- **Training workshops** on remote sensing techniques
- **Data sharing** partnerships

**Get in touch**: [your.email@example.com](mailto:your.email@example.com)
