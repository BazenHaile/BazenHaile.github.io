---
layout: single
title: "Contact"
permalink: /contact/
author_profile: true
classes: wide
breadcrumbs: false
---

<style>
/* Hide the page title */
.page__title {
  display: none;
}

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
.contact-hero {
  background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
  color: white;
  padding: 60px 40px;
  border-radius: 10px;
  text-align: center;
  margin-bottom: 60px;
  position: relative;
  overflow: hidden;
}

.contact-hero::before {
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

.contact-hero h1 {
  position: relative;
  z-index: 1;
  font-size: 2.5rem;
  margin-bottom: 20px;
}

.contact-hero p {
  position: relative;
  z-index: 1;
  font-size: 1.2rem;
  opacity: 0.95;
  max-width: 600px;
  margin: 0 auto;
}

/* Contact Cards Grid */
.contact-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 30px;
  margin-bottom: 60px;
}

.contact-card {
  background: white;
  border-radius: 10px;
  padding: 40px 30px;
  text-align: center;
  box-shadow: var(--shadow);
  transition: all 0.3s ease;
  border-top: 4px solid var(--accent-color);
}

.contact-card:hover {
  transform: translateY(-5px);
  box-shadow: var(--shadow-hover);
}

.contact-card .icon {
  font-size: 3rem;
  margin-bottom: 20px;
  display: block;
}

.contact-card h3 {
  color: var(--primary-color);
  margin-bottom: 15px;
  font-size: 1.3rem;
}

.contact-card p {
  color: var(--text-light);
  margin-bottom: 20px;
  line-height: 1.6;
}

.contact-card a {
  color: var(--accent-color);
  text-decoration: none;
  font-weight: 600;
  transition: all 0.3s ease;
}

.contact-card a:hover {
  color: var(--primary-color);
}

/* Info Section */
.info-section {
  background: var(--bg-light);
  padding: 60px 40px;
  margin: 60px -40px;
  text-align: center;
}

.info-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 40px;
  max-width: 1000px;
  margin: 40px auto 0;
}

.info-item {
  text-align: center;
}

.info-item h4 {
  color: var(--primary-color);
  margin-bottom: 10px;
  font-size: 1.2rem;
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 10px;
}

.info-item p {
  color: var(--text-dark);
  line-height: 1.6;
}

/* CTA Section */
.contact-cta {
  background: white;
  border-radius: 10px;
  padding: 50px 40px;
  text-align: center;
  box-shadow: var(--shadow);
  border: 2px solid var(--accent-color);
}

.contact-cta h2 {
  color: var(--primary-color);
  margin-bottom: 20px;
}

.contact-cta p {
  color: var(--text-light);
  font-size: 1.1rem;
  margin-bottom: 30px;
}

/* Button Styles */
.btn--professional {
  background: var(--accent-color);
  color: white;
  padding: 12px 30px;
  border-radius: 5px;
  text-decoration: none;
  display: inline-block;
  font-weight: 600;
  transition: all 0.3s ease;
  border: 2px solid var(--accent-color);
}

.btn--professional:hover {
  background: transparent;
  color: var(--accent-color);
  transform: translateY(-2px);
}

.btn--outline {
  background: transparent;
  color: var(--accent-color);
  padding: 12px 30px;
  border-radius: 5px;
  text-decoration: none;
  display: inline-block;
  font-weight: 600;
  transition: all 0.3s ease;
  border: 2px solid var(--accent-color);
}

.btn--outline:hover {
  background: var(--accent-color);
  color: white;
  transform: translateY(-2px);
}

/* Response Time Table */
.response-table {
  background: white;
  border-radius: 10px;
  padding: 40px;
  margin-top: 40px;
  box-shadow: var(--shadow);
}

.response-table table {
  width: 100%;
  border-collapse: collapse;
}

.response-table th {
  background: var(--bg-light);
  color: var(--primary-color);
  padding: 15px;
  text-align: left;
  font-weight: 600;
}

.response-table td {
  padding: 15px;
  border-bottom: 1px solid #e0e0e0;
  color: var(--text-dark);
}

.response-table tr:last-child td {
  border-bottom: none;
}

/* Responsive */
@media (max-width: 768px) {
  .contact-hero h1 {
    font-size: 2rem;
  }
  
  .contact-grid,
  .info-grid {
    grid-template-columns: 1fr;
  }
  
  .info-section {
    margin: 40px -20px;
    padding: 40px 20px;
  }
}
</style>

<div class="contact-hero">
  <h1>Let's Connect</h1>
  <p>I'm always interested in discussing geospatial projects, collaboration opportunities, and sharing knowledge with the GIS community.</p>
</div>

<div class="contact-grid">
  <div class="contact-card">
    <span class="icon">📧</span>
    <h3>Email</h3>
    <p>For professional inquiries and project discussions</p>
    <a href="mailto:bazenhaileam@gmail.com">bazenhaileam@gmail.com</a>
  </div>
  
  <div class="contact-card">
    <span class="icon">💼</span>
    <h3>LinkedIn</h3>
    <p>Connect for professional networking</p>
    <a href="https://linkedin.com/in/bazen-amene" target="_blank">View Profile</a>
  </div>
  
  <div class="contact-card">
    <span class="icon">🐙</span>
    <h3>GitHub</h3>
    <p>Explore my code and projects</p>
    <a href="https://github.com/bazenhaile" target="_blank">@bazenhaile</a>
  </div>
</div>

<section class="info-section">
  <h2 style="color: var(--primary-color); margin-bottom: 20px;">Collaboration Opportunities</h2>
  <p style="color: var(--text-light); font-size: 1.1rem; margin-bottom: 40px;">I'm particularly interested in projects that leverage geospatial technology for positive impact</p>
  
  <div class="info-grid">
    <div class="info-item">
      <h4><span>🌍</span> Environmental Monitoring</h4>
      <p>Satellite imagery analysis for tracking environmental changes, climate impact assessment, and conservation planning</p>
    </div>
    
    <div class="info-item">
      <h4><span>🏙️</span> Urban Planning</h4>
      <p>Smart city initiatives, urban growth analysis, and sustainable development planning using GIS</p>
    </div>
    
    <div class="info-item">
      <h4><span>🎓</span> Education & Research</h4>
      <p>Developing educational content, research collaboration, and knowledge sharing in geospatial technologies</p>
    </div>
  </div>
</section>

<div class="contact-cta">
  <h2>Ready to Start a Project?</h2>
  <p>Whether you need GIS expertise, remote sensing analysis, or spatial data solutions, I'm here to help bring your ideas to life.</p>
  
  <div style="display: flex; gap: 20px; justify-content: center; flex-wrap: wrap;">
    <a href="mailto:bazenhaileam@gmail.com?subject=Project%20Inquiry" class="btn--professional">Send Email</a>
    <a href="/assets/cv/Bazen Amene 2025 CV.pdf" class="btn--outline">Download CV</a>
  </div>
</div>

<div class="response-table">
  <h3 style="color: var(--primary-color); margin-bottom: 20px;">Response Times</h3>
  <table>
    <tr>
      <th>Contact Method</th>
      <th>Typical Response</th>
    </tr>
    <tr>
      <td>Email (General)</td>
      <td>Within 24 hours</td>
    </tr>
    <tr>
      <td>Email (Urgent)</td>
      <td>Within 4-6 hours</td>
    </tr>
    <tr>
      <td>LinkedIn Messages</td>
      <td>Within 48 hours</td>
    </tr>
    <tr>
      <td>GitHub Issues</td>
      <td>Within 1 week</td>
    </tr>
  </table>
</div>

<div style="text-align: center; margin-top: 60px;">
  <p style="color: var(--text-light); font-style: italic;">
    📍 Based in Dublin, Ireland | Available for opportunities across Ireland and EU
  </p>
</div>
