---
permalink: /
title: "Welcome"
author_profile: true
redirect_from:
  - /about/
  - /about.html
---

<style>
.hero-section {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  color: white;
  padding: 2rem;
  border-radius: 12px;
  margin-bottom: 2rem;
  box-shadow: 0 10px 40px rgba(102, 126, 234, 0.3);
}
.hero-section h2 {
  color: white;
  margin-top: 0;
}
.research-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 1.5rem;
  margin: 2rem 0;
}
.research-card {
  background: linear-gradient(145deg, #f8f9fa, #ffffff);
  border-radius: 12px;
  padding: 1.5rem;
  box-shadow: 0 4px 15px rgba(0,0,0,0.08);
  border-left: 4px solid #667eea;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}
.research-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 8px 25px rgba(0,0,0,0.12);
}
.research-card h3 {
  color: #667eea;
  margin-top: 0;
  font-size: 1.1rem;
}
.stats-container {
  display: flex;
  flex-wrap: wrap;
  gap: 1rem;
  margin: 2rem 0;
}
.stat-box {
  flex: 1;
  min-width: 140px;
  background: #f8f9fa;
  padding: 1.2rem;
  border-radius: 10px;
  text-align: center;
  border-bottom: 3px solid #667eea;
}
.stat-box .number {
  font-size: 2rem;
  font-weight: 700;
  color: #667eea;
  display: block;
}
.stat-box .label {
  font-size: 0.85rem;
  color: #666;
  text-transform: uppercase;
  letter-spacing: 0.5px;
}
.news-item {
  padding: 1rem;
  border-left: 3px solid #667eea;
  background: #f8f9fa;
  margin-bottom: 1rem;
  border-radius: 0 8px 8px 0;
}
.news-item .date {
  font-weight: 600;
  color: #667eea;
}
.collab-badge {
  display: inline-block;
  background: linear-gradient(135deg, #667eea, #764ba2);
  color: white;
  padding: 0.4rem 1rem;
  border-radius: 20px;
  font-size: 0.85rem;
  margin: 0.3rem;
}
.section-title {
  display: flex;
  align-items: center;
  gap: 0.5rem;
  color: #333;
  border-bottom: 2px solid #667eea;
  padding-bottom: 0.5rem;
  margin-top: 2.5rem;
}
</style>

<div class="hero-section">
  <h2>Shayan Jalilpour</h2>
  <p style="font-size: 1.2rem; margin-bottom: 0.5rem;"><strong>PhD Candidate in Biomedical Engineering</strong></p>
  <p style="opacity: 0.9; margin-bottom: 0;">Graz University of Technology, Austria</p>
  <p style="opacity: 0.9; font-size: 0.95rem;">Developing interpretable deep learning frameworks for EEG analysis and Brain-Computer Interfaces</p>
</div>

<div class="stats-container">
  <div class="stat-box">
    <span class="number">6</span>
    <span class="label">Journal Papers</span>
  </div>
  <div class="stat-box">
    <span class="number">5</span>
    <span class="label">Conferences</span>
  </div>
  <div class="stat-box">
    <span class="number">4</span>
    <span class="label">Q1 Journals</span>
  </div>
  <div class="stat-box">
    <span class="number">5+</span>
    <span class="label">Years Research</span>
  </div>
</div>

<h2 class="section-title"><i class="fas fa-microscope"></i> Research Focus</h2>

<div class="research-grid">
  <div class="research-card">
    <h3><i class="fas fa-brain"></i> Interpretable Deep Learning</h3>
    <p>Developing transparent neural network architectures that provide insights into how models process brain signals, achieving 96.8% accuracy with >50x parameter reduction.</p>
  </div>
  <div class="research-card">
    <h3><i class="fas fa-laptop-medical"></i> Brain-Computer Interfaces</h3>
    <p>Creating systems that decode neural signals for real-time human-machine interaction, including hybrid BCI spellers with 93% accuracy.</p>
  </div>
  <div class="research-card">
    <h3><i class="fas fa-users"></i> Cross-Subject Classification</h3>
    <p>Building robust EEG models that generalize across different individuals without subject-specific calibration.</p>
  </div>
  <div class="research-card">
    <h3><i class="fas fa-clock"></i> Real-time Neural Decoding</h3>
    <p>Developing asynchronous classifiers for cognitive state detection optimized for online deployment in human-machine systems.</p>
  </div>
</div>

<h2 class="section-title"><i class="fas fa-handshake"></i> Collaborations</h2>

<p>Working with leading institutions and industry partners:</p>

<div style="margin: 1rem 0;">
  <span class="collab-badge"><i class="fas fa-university"></i> University of San Diego (UCSD)</span>
  <span class="collab-badge"><i class="fas fa-truck"></i> Daimler Truck AG & FKFS</span>
  <span class="collab-badge"><i class="fas fa-graduation-cap"></i> University of Lisbon</span>
  <span class="collab-badge"><i class="fas fa-award"></i> Marshall Plan Foundation</span>
</div>

<h2 class="section-title"><i class="fas fa-newspaper"></i> Recent News</h2>

<div class="news-item">
  <span class="date">2025</span> - Received <strong>Teaching Grant (15k)</strong> for Joint Online Course from Graz University of Technology with University of Lisbon
</div>
<div class="news-item">
  <span class="date">2024</span> - Awarded <strong>Austrian Marshall Plan Scholarship (7.5k)</strong> for EU-US research exchange collaboration with UCSD
</div>
<div class="news-item">
  <span class="date">2024</span> - <strong>Team Lead - Mirage 91</strong>: Co-led 12-member student team for CYBATHLON 2024 BCI competition
</div>
<div class="news-item">
  <span class="date">2024</span> - Published interpretable deep learning framework in <strong>Engineering Applications of AI</strong> (IF: 8, Q1)
</div>

<h2 class="section-title"><i class="fas fa-chalkboard-teacher"></i> Teaching</h2>

Currently serving as **Lecturer** at Graz University of Technology:

- **Non-invasive Brain-Computer Interfaces 1 & 2** - Machine learning, signal processing, BCI design
- **Fundamentals of Biomedical Engineering** - EEG Laboratory
- **Guest Lecturer** at University of Lisbon (2025)

<h2 class="section-title"><i class="fas fa-envelope"></i> Contact</h2>

I'm always interested in discussing research collaborations, especially in the areas of interpretable AI, EEG signal processing, and brain-computer interfaces.

<p style="margin-top: 1rem;">
  <a href="mailto:shayanjalilpour@gmail.com" style="display: inline-block; background: linear-gradient(135deg, #667eea, #764ba2); color: white; padding: 0.6rem 1.5rem; border-radius: 25px; text-decoration: none; font-weight: 500;">
    <i class="fas fa-envelope"></i> Get in Touch
  </a>
</p>
