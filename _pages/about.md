---
permalink: /
title: "Welcome"
author_profile: true
redirect_from:
  - /about/
  - /about.html
---

<style>
/* CSS Variables for theme support */
:root {
  --about-text-primary: #222;
  --about-text-body: #333;
  --about-bg-card: #ffffff;
  --about-bg-light: #f8f9fa;
  --about-accent: #667eea;
  --about-accent-secondary: #764ba2;
}

/* Dark mode support */
@media (prefers-color-scheme: dark) {
  :root {
    --about-text-primary: #e8e8e8;
    --about-text-body: #d0d0d0;
    --about-bg-card: #2a2a3a;
    --about-bg-light: #1e1e2e;
  }
}

/* Also support class-based dark mode */
.dark-mode, [data-theme="dark"] {
  --about-text-primary: #e8e8e8;
  --about-text-body: #d0d0d0;
  --about-bg-card: #2a2a3a;
  --about-bg-light: #1e1e2e;
}

.hero-section {
  background: linear-gradient(135deg, var(--about-accent) 0%, var(--about-accent-secondary) 100%);
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
  background: var(--about-bg-card);
  border-radius: 12px;
  padding: 1.5rem;
  box-shadow: 0 4px 15px rgba(0,0,0,0.08);
  border-left: 4px solid var(--about-accent);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}
.research-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 8px 25px rgba(0,0,0,0.12);
}
.research-card h3 {
  color: var(--about-accent);
  margin-top: 0;
  font-size: 1.1rem;
}
.research-card p {
  color: var(--about-text-body);
  margin-bottom: 0;
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
  background: var(--about-bg-light);
  padding: 1.2rem;
  border-radius: 10px;
  text-align: center;
  border-bottom: 3px solid var(--about-accent);
}
.stat-box .number {
  font-size: 2rem;
  font-weight: 700;
  color: var(--about-accent);
  display: block;
}
.stat-box .label {
  font-size: 0.85rem;
  color: var(--about-text-body);
  text-transform: uppercase;
  letter-spacing: 0.5px;
}
.news-item {
  padding: 1rem;
  border-left: 3px solid var(--about-accent);
  background: var(--about-bg-light);
  margin-bottom: 1rem;
  border-radius: 0 8px 8px 0;
  color: var(--about-text-body);
}
.news-item .date {
  font-weight: 600;
  color: var(--about-accent);
}
.collab-badge {
  display: inline-block;
  background: linear-gradient(135deg, var(--about-accent), var(--about-accent-secondary));
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
  color: var(--about-accent);
  border-bottom: 2px solid var(--about-accent);
  padding-bottom: 0.5rem;
  margin-top: 2.5rem;
}
</style>

<h2 class="section-title"><i class="fas fa-user"></i> About Me</h2>

<p style="color: var(--about-text-body); line-height: 1.8; text-align: justify;">
Currently, I am a postdoctoral researcher at the <a href="https://grazbci.at/" style="color: var(--about-accent);">Institute of Neural Engineering</a> at Graz University of Technology, working with <a href="https://grazbci.at/" style="color: var(--about-accent);">Prof. Gernot R. Müller-Putz</a>. My research focuses on developing interpretable deep learning frameworks for EEG analysis and Brain-Computer Interfaces.
</p>

<p style="color: var(--about-text-body); line-height: 1.8; text-align: justify;">
From 2020-2025, I was a doctoral researcher at Graz University of Technology, Austria. I worked at the Institute of Neural Engineering in the BCI research group. During my PhD, I developed novel methods for interpretable deep learning in EEG-based brain-computer interfaces, achieving 96.8% subject-independent accuracy while reducing model parameters by more than 50x. I received my Ph.D. (Dr.techn.) from TU Graz in 2025.
</p>

<p style="color: var(--about-text-body); line-height: 1.8; text-align: justify;">
Prior to that, I received my M.Sc. degree in Biomedical Engineering from the Electrical Engineering faculty of Sharif University of Technology, Tehran, Iran (2019), where I developed a hybrid BCI speller achieving 93% classification accuracy. I obtained my B.Sc. degree in Electrical Engineering from Guilan University, Rasht, Iran (2016).
</p>

<h2 class="section-title"><i class="fas fa-microscope"></i> Research Interests</h2>

<p style="color: var(--about-text-body); line-height: 1.8;">
My research interests include interpretable deep learning, brain-computer interfaces, EEG signal processing, cross-subject classification, and real-time neural decoding.
</p>

<h2 class="section-title"><i class="fas fa-newspaper"></i> Recent News</h2>

<div class="news-item">
  <span class="date">2025</span> - Received <strong>Teaching Grant (€15k)</strong> for Joint Online Course from Graz University of Technology with University of Lisbon
</div>
<div class="news-item">
  <span class="date">2024</span> - Awarded <strong>Austrian Marshall Plan Scholarship (€7.5k)</strong> for EU-US research exchange collaboration with UCSD
</div>
<div class="news-item">
  <span class="date">2024</span> - Published interpretable deep learning framework in <strong>Engineering Applications of AI</strong> (IF: 8, Q1)
</div>

<h2 class="section-title"><i class="fas fa-envelope"></i> Contact</h2>

<p style="color: var(--about-text-body);">
I'm always interested in discussing research collaborations, especially in the areas of interpretable AI, EEG signal processing, and brain-computer interfaces.
</p>

<p style="margin-top: 1rem;">
  <a href="mailto:shayanjalilpour@gmail.com" style="display: inline-block; background: linear-gradient(135deg, #667eea, #764ba2); color: white; padding: 0.6rem 1.5rem; border-radius: 25px; text-decoration: none; font-weight: 500;">
    <i class="fas fa-envelope"></i> Get in Touch
  </a>
</p>
