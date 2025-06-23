---
layout: single
title: "Remote Sensing Projects"
permalink: /remote-sensing/
classes: wide
header:
  overlay_color: "#2c3e50"
  overlay_image: /assets/images/satellite-header.jpg
  excerpt: "Satellite imagery analysis and environmental monitoring using advanced remote sensing techniques"
---

## 🛰️ Satellite Data Analysis & Environmental Monitoring

<div class="notice--primary">
  <h4>Remote Sensing Expertise</h4>
  <p>Specialized in multi-temporal analysis, land cover classification, and environmental change detection using optical and radar satellite data. Experience with both commercial and open-source platforms for large-scale monitoring projects.</p>
</div>

---

## Featured Projects

### 🌲 Forest Change Detection - County Cork
<div style="display: flex; margin-bottom: 30px;">
  <div style="flex: 1; padding-right: 20px;">
    <img src="/assets/images/forest-change-teaser.jpg" alt="Forest Change Detection" style="width: 100%; border-radius: 8px;">
  </div>
  <div style="flex: 2;">
    <h4>Multi-temporal Analysis of Forest Cover Changes</h4>
    <p><strong>Objective:</strong> Quantify forest cover changes in County Cork over 8-year period using Landsat time series</p>
    <p><strong>Key Results:</strong> Identified 2,847 hectares of forest loss and primary drivers of change</p>
    <p><strong>Tools:</strong> Google Earth Engine, Python, QGIS</p>
    <p><strong>Data:</strong> Landsat 8 OLI, Sentinel-2, OSI Forest Maps</p>
    <p><a href="/portfolio/forest-change-detection/" class="btn btn--primary">View Full Project</a></p>
  </div>
</div>

---

### 🌾 Agricultural Monitoring - Munster Region
<div style="display: flex; margin-bottom: 30px;">
  <div style="flex: 2;">
    <h4>Crop Health Assessment Using Vegetation Indices</h4>
    <p><strong>Objective:</strong> Monitor crop health and predict yield variations across agricultural lands in Munster</p>
    <p><strong>Key Results:</strong> Developed early warning system for crop stress detection</p>
    <p><strong>Tools:</strong> Sentinel-2, NDVI/EVI analysis, R Statistical Analysis</p>
    <p><strong>Data:</strong> Sentinel-2 MSI, Weather stations, Field survey data</p>
    <p><a href="/portfolio/agricultural-monitoring/" class="btn btn--primary">View Full Project</a></p>
  </div>
  <div style="flex: 1; padding-left: 20px;">
    <img src="/assets/images/agriculture-teaser.jpg" alt="Agricultural Monitoring" style="width: 100%; border-radius: 8px;">
  </div>
</div>

---

### 🌊 Coastal Erosion Monitoring - West Coast
<div style="display: flex; margin-bottom: 30px;">
  <div style="flex: 1; padding-right: 20px;">
    <img src="/assets/images/coastal-erosion-teaser.jpg" alt="Coastal Erosion" style="width: 100%; border-radius: 8px;">
  </div>
  <div style="flex: 2;">
    <h4>Multi-sensor Approach to Shoreline Change Detection</h4>
    <p><strong>Objective:</strong> Assess coastal erosion rates along Ireland's Atlantic coastline</p>
    <p><strong>Key Results:</strong> Quantified erosion rates and identified vulnerable areas</p>
    <p><strong>Tools:</strong> Sentinel-1 SAR, Landsat, DSAS (Digital Shoreline Analysis)</p>
    <p><strong>Data:</strong> Multi-temporal satellite imagery, LiDAR, Historical maps</p>
    <p><a href="/portfolio/coastal-erosion/" class="btn btn--primary">View Full Project</a></p>
  </div>
</div>

---

## Technical Capabilities

### 📡 Satellite Platforms & Sensors

| **Platform** | **Sensors** | **Resolution** | **Applications** |
|--------------|-------------|----------------|------------------|
| **Landsat 8/9** | OLI, TIRS | 30m optical, 100m thermal | Land cover, change detection |
| **Sentinel-2** | MSI | 10m-60m multispectral | Vegetation monitoring, agriculture |
| **Sentinel-1** | C-SAR | 5m-40m radar | All-weather monitoring, deformation |
| **MODIS** | Terra/Aqua | 250m-1km | Large-scale phenology, fire detection |
| **Planet Labs** | PlanetScope | 3m optical | High-frequency monitoring |

### 🔬 Analysis Techniques

#### Image Classification
- **Supervised Classification**: Random Forest, SVM, Maximum Likelihood
- **Unsupervised Classification**: K-means, ISODATA clustering
- **Object-Based Classification**: eCognition, OBIA workflows
- **Deep Learning**: CNN, U-Net for semantic segmentation

#### Change Detection Methods
- **Pixel-based**: Image differencing, Change Vector Analysis
- **Object-based**: Multi-temporal object comparison
- **Time Series**: Trend analysis, breakpoint detection
- **Machine Learning**: Ensemble methods for change classification

#### Spectral Analysis
- **Vegetation Indices**: NDVI, EVI, SAVI, LAI estimation
- **Water Indices**: NDWI, MNDWI for water body mapping
- **Soil Indices**: Brightness, wetness, salinity assessment
- **Atmospheric Correction**: DOS, 6S, Sen2Cor processing

---

## Software & Programming

### 🖥️ Primary Platforms
- **Google Earth Engine**: Cloud-based planetary-scale analysis
- **ENVI**: Advanced spectral analysis and classification
- **SNAP**: ESA's Sentinel data processing toolbox
- **ArcGIS Pro**: Integrated image analysis and GIS

### 💻 Programming Languages
```python
# Example: Automated NDVI calculation in Google Earth Engine
import ee

def calculate_ndvi(image):
    """Calculate NDVI for Sentinel-2 imagery"""
    ndvi = image.normalizedDifference(['B8', 'B4']).rename('NDVI')
    return image.addBands(ndvi)

# Apply to image collection
collection = ee.ImageCollection('COPERNICUS/S2_SR') \
               .filterDate('2023-01-01', '2023-12-31') \
               .map(calculate_ndvi)
```

### 📊 Data Processing Libraries
- **Python**: GDAL, Rasterio, Scikit-learn, OpenCV
- **R**: Raster, Rgdal, RandomForest, Satellite package
- **JavaScript**: Google Earth Engine API, Leaflet integration

---

## Methodology Framework

### 1. Project Planning & Data Strategy
- **Requirements Analysis**: Stakeholder consultation and objective definition
- **Data Inventory**: Multi-source data availability and quality assessment
- **Temporal Strategy**: Optimal image selection and time series design
- **Validation Planning**: Ground truth and accuracy assessment protocols

### 2. Pre-processing Workflows
- **Atmospheric Correction**: Surface reflectance conversion
- **Geometric Correction**: Co-registration and orthorectification
- **Cloud Masking**: Quality pixel identification
- **Temporal Compositing**: Multi-image mosaicking and gap-filling

### 3. Analysis Implementation
- **Algorithm Selection**: Method optimization for specific applications
- **Parameter Tuning**: Sensitivity analysis and optimization
- **Scalability Testing**: Processing efficiency for large datasets
- **Quality Control**: Intermediate result validation

### 4. Validation & Accuracy Assessment
- **Reference Data**: Independent validation dataset creation
- **Statistical Metrics**: Overall accuracy, Kappa, F1-score calculation
- **Spatial Validation**: Geographic distribution of errors
- **Temporal Validation**: Multi-date consistency assessment

---

## Applications & Use Cases

### 🌍 Environmental Monitoring
- **Deforestation Tracking**: Real-time forest loss alerts
- **Wetland Mapping**: Seasonal water extent monitoring
- **Land Degradation**: Soil erosion and desertification assessment
- **Carbon Stock**: Biomass estimation for carbon accounting

### 🚜 Agriculture & Food Security
- **Crop Type Mapping**: Seasonal crop identification and monitoring
- **Yield Prediction**: Vegetation index-based yield forecasting
- **Irrigation Monitoring**: Water stress detection and optimization
- **Phenology Tracking**: Growth stage monitoring for precision agriculture

### 🏙️ Urban & Infrastructure
- **Urban Growth**: Expansion pattern analysis and planning support
- **Heat Island Effect**: Surface temperature monitoring
- **Infrastructure Monitoring**: Road and building change detection
- **Disaster Assessment**: Post-event damage mapping

### 🌊 Water Resources
- **Water Quality**: Turbidity and chlorophyll monitoring
- **Flood Mapping**: Inundation extent and frequency analysis
- **Reservoir Monitoring**: Water level and capacity assessment
- **Coastal Dynamics**: Shoreline change and erosion monitoring

---

## Current Research Interests

### 🧠 Machine Learning Applications
- **Deep Learning**: CNN and U-Net for pixel-level classification
- **Time Series Analysis**: LSTM networks for temporal pattern recognition
- **Transfer Learning**: Model adaptation across different geographic regions
- **Ensemble Methods**: Combining multiple algorithms for improved accuracy

### ☁️ Cloud-Native Processing
- **Scalable Workflows**: Distributed processing on cloud platforms
- **Real-time Processing**: Stream processing for continuous monitoring
- **API Development**: Web services for automated analysis
- **Data Fusion**: Multi-sensor integration techniques

### 🌐 Global Monitoring
- **Cross-border Analysis**: Transnational environmental monitoring
- **Climate Change**: Long-term trend analysis and impact assessment
- **Sustainable Development**: SDG indicator monitoring using EO data
- **Disaster Response**: Rapid response mapping and damage assessment

---

## Publications & Presentations

### 📄 Recent Publications
- **"Multi-temporal Forest Change Detection in Ireland"** - *Journal of Environmental Monitoring* (2023)
- **"Agricultural Drought Monitoring Using Satellite Data"** - *Irish Geography* (2023)
- **"Coastal Erosion Assessment Using SAR Interferometry"** - *Remote Sensing Applications* (2022)

### 🎤 Conference Presentations
- **Irish Geospatial Conference 2023**: "Operational Forest Monitoring Using Cloud Computing"
- **EARSeL Symposium 2023**: "Multi-sensor Approach to Coastal Change Detection"
- **ISPRS Congress 2022**: "Machine Learning for Agricultural Land Use Classification"

---

## Collaboration Opportunities

### 🤝 Open to Partnerships
- **Research Institutions**: Joint research proposals and publications
- **Government Agencies**: Operational monitoring system development
- **Private Sector**: Commercial remote sensing applications
- **NGOs**: Environmental conservation and monitoring projects

### 🎓 Training & Education
- **Workshops**: Hands-on remote sensing training
- **Guest Lectures**: University course contributions
- **Online Tutorials**: Educational content development
- **Mentorship**: Student and early-career professional guidance

---

## Contact for Remote Sensing Projects

Interested in satellite-based monitoring solutions or research collaboration?

[📧 Discuss Your Project](mailto:your.email@example.com){: .btn .btn--primary .btn--large}
[📄 Request Detailed CV](/contact/){: .btn .btn--inverse}
