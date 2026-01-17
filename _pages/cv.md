---
layout: archive
title: "Curriculum Vitae"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

<style>
.cv-section {
  margin-bottom: 2.5rem;
}
.cv-section-title {
  display: flex;
  align-items: center;
  gap: 0.5rem;
  color: #667eea;
  border-bottom: 3px solid #667eea;
  padding-bottom: 0.5rem;
  margin-bottom: 1.5rem;
  font-size: 1.4rem;
}
.edu-card {
  background: linear-gradient(145deg, #f8f9fa, #ffffff);
  border-radius: 12px;
  padding: 1.5rem;
  margin-bottom: 1.5rem;
  box-shadow: 0 4px 15px rgba(0,0,0,0.08);
  border-left: 4px solid #667eea;
}
.edu-card h3 {
  color: #333;
  margin: 0 0 0.3rem 0;
  font-size: 1.1rem;
}
.edu-card .institution {
  color: #667eea;
  font-style: italic;
  margin-bottom: 0.5rem;
}
.edu-card .meta {
  display: flex;
  flex-wrap: wrap;
  gap: 1rem;
  font-size: 0.9rem;
  color: #666;
  margin-bottom: 0.5rem;
}
.edu-card .meta span {
  display: flex;
  align-items: center;
  gap: 0.3rem;
}
.edu-card .description {
  color: #555;
  font-size: 0.95rem;
  margin-top: 0.5rem;
  padding-top: 0.5rem;
  border-top: 1px solid #eee;
}
.exp-card {
  background: #fff;
  border-radius: 12px;
  padding: 1.5rem;
  margin-bottom: 1.5rem;
  box-shadow: 0 4px 20px rgba(0,0,0,0.06);
  border: 1px solid #e8e8e8;
  position: relative;
}
.exp-card::before {
  content: '';
  position: absolute;
  left: 0;
  top: 0;
  bottom: 0;
  width: 4px;
  background: linear-gradient(180deg, #667eea, #764ba2);
  border-radius: 4px 0 0 4px;
}
.exp-card h3 {
  color: #333;
  margin: 0 0 0.3rem 0;
}
.exp-card .company {
  color: #667eea;
  font-weight: 500;
}
.exp-card .period {
  color: #888;
  font-size: 0.9rem;
}
.exp-card ul {
  margin-top: 1rem;
  padding-left: 1.2rem;
}
.exp-card li {
  margin-bottom: 0.6rem;
  color: #555;
}
.skills-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 1rem;
}
.skill-category {
  background: linear-gradient(145deg, #f8f9fa, #fff);
  padding: 1.2rem;
  border-radius: 10px;
  box-shadow: 0 3px 10px rgba(0,0,0,0.05);
}
.skill-category h4 {
  color: #667eea;
  margin: 0 0 0.8rem 0;
  font-size: 0.95rem;
  display: flex;
  align-items: center;
  gap: 0.4rem;
}
.skill-tag {
  display: inline-block;
  background: #e8eeff;
  color: #667eea;
  padding: 0.3rem 0.7rem;
  border-radius: 15px;
  font-size: 0.85rem;
  margin: 0.2rem;
}
.award-item {
  display: flex;
  align-items: flex-start;
  gap: 1rem;
  padding: 1rem;
  background: #f8f9fa;
  border-radius: 8px;
  margin-bottom: 0.8rem;
}
.award-year {
  background: linear-gradient(135deg, #667eea, #764ba2);
  color: white;
  padding: 0.4rem 0.8rem;
  border-radius: 6px;
  font-weight: 600;
  font-size: 0.9rem;
  white-space: nowrap;
}
.award-text {
  color: #444;
}
.lang-table {
  width: 100%;
  border-collapse: separate;
  border-spacing: 0;
}
.lang-table th {
  background: linear-gradient(135deg, #667eea, #764ba2);
  color: white;
  padding: 0.8rem 1rem;
  text-align: left;
}
.lang-table th:first-child {
  border-radius: 8px 0 0 0;
}
.lang-table th:last-child {
  border-radius: 0 8px 0 0;
}
.lang-table td {
  padding: 0.8rem 1rem;
  border-bottom: 1px solid #eee;
}
.lang-table tr:last-child td:first-child {
  border-radius: 0 0 0 8px;
}
.lang-table tr:last-child td:last-child {
  border-radius: 0 0 8px 0;
}
.teaching-item {
  padding: 1rem;
  border-left: 3px solid #667eea;
  background: #fafafa;
  margin-bottom: 0.8rem;
  border-radius: 0 8px 8px 0;
}
.teaching-item h4 {
  margin: 0 0 0.3rem 0;
  color: #333;
}
.teaching-item .course {
  color: #667eea;
  font-style: italic;
}
.reference-card {
  background: linear-gradient(145deg, #f8f9fa, #fff);
  padding: 1.5rem;
  border-radius: 12px;
  box-shadow: 0 4px 15px rgba(0,0,0,0.08);
  margin-bottom: 1rem;
}
.reference-card h4 {
  color: #667eea;
  margin: 0 0 0.3rem 0;
}
.reference-card .title {
  color: #666;
  font-size: 0.9rem;
}
.reference-card .email {
  margin-top: 0.5rem;
}
.reference-card .email a {
  color: #667eea;
}
</style>

<div class="cv-section">
  <h2 class="cv-section-title"><i class="fas fa-graduation-cap"></i> Education</h2>

  <div class="edu-card">
    <h3>PhD in Biomedical Engineering</h3>
    <div class="institution">Graz University of Technology - Department of CSBME</div>
    <div class="meta">
      <span><i class="fas fa-calendar"></i> 2020 - Present</span>
      <span><i class="fas fa-map-marker-alt"></i> Graz, Austria</span>
      <span><i class="fas fa-star"></i> GPA: 1.4/5.0</span>
    </div>
    <div class="description">
      <strong>Supervisor:</strong> Prof. Gernot Muller-Putz<br>
      <strong>Dissertation:</strong> Developed interpretable deep learning frameworks for EEG data. Applied statistical analysis, asynchronous decoding, and multi-class classification on brain signals.
    </div>
  </div>

  <div class="edu-card">
    <h3>M.Sc. in Biomedical Engineering</h3>
    <div class="institution">Sharif University of Technology - Department of EE (BME group)</div>
    <div class="meta">
      <span><i class="fas fa-calendar"></i> 2016 - 2019</span>
      <span><i class="fas fa-map-marker-alt"></i> Tehran, Iran</span>
      <span><i class="fas fa-star"></i> GPA: 17.16/20.00</span>
    </div>
    <div class="description">
      <strong>Thesis:</strong> Developed a novel hybrid BCI speller combining RSVP and SSVEP paradigms, achieving 93.06% classification accuracy and 23.41 bit/min information transfer rate (ITR).
    </div>
  </div>

  <div class="edu-card">
    <h3>B.Sc. in Electrical Engineering</h3>
    <div class="institution">Guilan University - Department of EE</div>
    <div class="meta">
      <span><i class="fas fa-calendar"></i> 2011 - 2016</span>
      <span><i class="fas fa-map-marker-alt"></i> Rasht, Iran</span>
    </div>
  </div>
</div>

<div class="cv-section">
  <h2 class="cv-section-title"><i class="fas fa-briefcase"></i> Professional Experience</h2>

  <div class="exp-card">
    <h3>University Assistant (Doctoral Researcher)</h3>
    <div class="company">Graz University of Technology</div>
    <div class="period"><i class="fas fa-calendar"></i> 2020 - Present | <i class="fas fa-map-marker-alt"></i> Graz, Austria</div>
    <ul>
      <li>Conducted EEG-based BCI and AI research, resulting in <strong>three Q1 journal papers</strong> and two conference publications</li>
      <li>Developed an interpretable deep learning framework achieving <strong>96.8% subject-independent accuracy</strong> while reducing model parameters by >50x</li>
      <li>Built a DL pipeline for denoising <strong>500k+ biosignal samples</strong> using Vision Transformer and U-Net architectures (Marshall Plan Scholarship with UCSD)</li>
      <li>Performed statistical analyses across time, frequency, and source domains for neural dynamics characterization</li>
      <li>Developed asynchronous classifier for real-time cognitive state detection optimized for online deployment</li>
      <li>Collaborated with <strong>Daimler Truck AG & FKFS</strong> on decoding distraction events using multimodal data</li>
    </ul>
  </div>

  <div class="exp-card">
    <h3>Signal Processing Engineer & Lab Manager</h3>
    <div class="company">National Brain Mapping Laboratory (NBML)</div>
    <div class="period"><i class="fas fa-calendar"></i> 2018 - 2019 | <i class="fas fa-map-marker-alt"></i> Tehran, Iran</div>
    <ul>
      <li>Supervised a team of 4 specialists in signal processing laboratory</li>
      <li>Designed and analyzed data for <strong>10+ neuroscience research projects</strong></li>
      <li>Developed QA pipelines and statistical protocols for artifact reduction</li>
    </ul>
  </div>
</div>

<div class="cv-section">
  <h2 class="cv-section-title"><i class="fas fa-code"></i> Technical Skills</h2>

  <div class="skills-grid">
    <div class="skill-category">
      <h4><i class="fas fa-terminal"></i> Programming</h4>
      <span class="skill-tag">Python</span>
      <span class="skill-tag">pandas</span>
      <span class="skill-tag">NumPy</span>
      <span class="skill-tag">MATLAB</span>
    </div>
    <div class="skill-category">
      <h4><i class="fas fa-robot"></i> Machine Learning</h4>
      <span class="skill-tag">TensorFlow</span>
      <span class="skill-tag">PyTorch</span>
      <span class="skill-tag">scikit-learn</span>
    </div>
    <div class="skill-category">
      <h4><i class="fas fa-chart-bar"></i> Data Analysis</h4>
      <span class="skill-tag">SPSS</span>
      <span class="skill-tag">Visualization</span>
      <span class="skill-tag">Time-series</span>
    </div>
    <div class="skill-category">
      <h4><i class="fas fa-server"></i> Tools & Platforms</h4>
      <span class="skill-tag">Git</span>
      <span class="skill-tag">HPC Clusters</span>
      <span class="skill-tag">SLURM</span>
    </div>
  </div>
</div>

<div class="cv-section">
  <h2 class="cv-section-title"><i class="fas fa-language"></i> Language Skills</h2>

  <table class="lang-table">
    <tr>
      <th>Language</th>
      <th>Proficiency</th>
    </tr>
    <tr>
      <td><i class="fas fa-globe"></i> English</td>
      <td>Professional (C1)</td>
    </tr>
    <tr>
      <td><i class="fas fa-globe"></i> German</td>
      <td>Elementary (B1)</td>
    </tr>
    <tr>
      <td><i class="fas fa-globe"></i> Persian</td>
      <td>Native</td>
    </tr>
  </table>
</div>

<div class="cv-section">
  <h2 class="cv-section-title"><i class="fas fa-chalkboard-teacher"></i> Teaching Experience</h2>

  <h4 style="color: #667eea; margin-top: 1.5rem;"><i class="fas fa-university"></i> University of Lisbon</h4>
  <div class="teaching-item">
    <h4>Guest Lecturer</h4>
    <div class="course">Non-invasive Brain-Computer Interfaces 1 (KU) - 2025</div>
    <p style="margin: 0.5rem 0 0 0; color: #666;">Received Teaching Grant for joint online course with TUG</p>
  </div>

  <h4 style="color: #667eea; margin-top: 1.5rem;"><i class="fas fa-university"></i> Graz University of Technology</h4>
  <div class="teaching-item">
    <h4>Lecturer</h4>
    <div class="course">Non-invasive Brain-Computer Interfaces 1 (KU) - 2020-2025</div>
    <p style="margin: 0.5rem 0 0 0; color: #666;">Machine learning, statistical analysis, neurophysiological analysis, feature extraction, pattern recognition</p>
  </div>
  <div class="teaching-item">
    <h4>Lecturer</h4>
    <div class="course">Non-invasive Brain-Computer Interfaces 2 (KU) - 2021-2024</div>
    <p style="margin: 0.5rem 0 0 0; color: #666;">Online data processing, classification, BCI task design, EEG instrumentation</p>
  </div>
  <div class="teaching-item">
    <h4>Lecturer</h4>
    <div class="course">Fundamentals of Biomedical Engineering, EEG Laboratory - 2020-2024</div>
  </div>

  <h4 style="color: #667eea; margin-top: 1.5rem;"><i class="fas fa-university"></i> Sharif University of Technology</h4>
  <div class="teaching-item">
    <h4>Head Teaching Assistant</h4>
    <div class="course">Artificial Intelligence - 2018</div>
  </div>
  <div class="teaching-item">
    <h4>Teaching Assistant</h4>
    <div class="course">Tensor Decompositions and Neural Modeling - 2018</div>
  </div>
</div>

<div class="cv-section">
  <h2 class="cv-section-title"><i class="fas fa-hands-helping"></i> Service & Volunteer Work</h2>

  <ul style="list-style: none; padding: 0;">
    <li style="padding: 0.8rem; background: #f8f9fa; border-radius: 8px; margin-bottom: 0.5rem;">
      <strong><i class="fas fa-users" style="color: #667eea;"></i> Mentorship:</strong> Supervised 2 Master's and 2 Bachelor's thesis students (2021 - present)
    </li>
    <li style="padding: 0.8rem; background: #f8f9fa; border-radius: 8px; margin-bottom: 0.5rem;">
      <strong><i class="fas fa-calendar-alt" style="color: #667eea;"></i> Conference Service:</strong> Organizing-committee member, Graz BCI Conference 2024
    </li>
    <li style="padding: 0.8rem; background: #f8f9fa; border-radius: 8px; margin-bottom: 0.5rem;">
      <strong><i class="fas fa-search" style="color: #667eea;"></i> Scientific Review:</strong> IEEE Trans. Biomedical Eng., Scientific Reports, IEEE Trans. NSRE, Frontiers in Human Neuroscience
    </li>
  </ul>
</div>

<div class="cv-section">
  <h2 class="cv-section-title"><i class="fas fa-award"></i> Honors & Awards</h2>

  <div class="award-item">
    <span class="award-year">2025</span>
    <span class="award-text">Teaching Grant for Joint Online Course (15k) - Graz University of Technology</span>
  </div>
  <div class="award-item">
    <span class="award-year">2024</span>
    <span class="award-text">International Communication Funding (2k) - Austrian Research Association</span>
  </div>
  <div class="award-item">
    <span class="award-year">2024</span>
    <span class="award-text">Austrian Marshall Plan Scholarship (7.5k) - EU-US Research Exchange</span>
  </div>
  <div class="award-item">
    <span class="award-year">2020</span>
    <span class="award-text">Full PhD offers from TU Graz, University of Ottawa, and LMU Munich</span>
  </div>
  <div class="award-item">
    <span class="award-year">2017</span>
    <span class="award-text">Research Grant - Iranian Cognitive Science and Technology Council</span>
  </div>
  <div class="award-item">
    <span class="award-year">2016</span>
    <span class="award-text">Ranked 65th in Nationwide M.Sc. Entrance Exam (50,000+ participants)</span>
  </div>
  <div class="award-item">
    <span class="award-year">2011</span>
    <span class="award-text">Top 10% in Iranian University Entrance Exam (285,000 examinees)</span>
  </div>
</div>

<div class="cv-section">
  <h2 class="cv-section-title"><i class="fas fa-user-tie"></i> References</h2>

  <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 1rem;">
    <div class="reference-card">
      <h4>Gernot R. Muller-Putz</h4>
      <div class="title">Full Professor, Head of Institute of Neural Engineering<br>Graz University of Technology, Austria</div>
      <div class="email"><i class="fas fa-envelope"></i> <a href="mailto:gernot.mueller@tugraz.at">gernot.mueller@tugraz.at</a></div>
    </div>
    <div class="reference-card">
      <h4>Sepideh Hajipour Sardouie</h4>
      <div class="title">Assistant Professor, Electrical Engineering Department<br>Sharif University of Technology, Iran</div>
      <div class="email"><i class="fas fa-envelope"></i> <a href="mailto:sepideh.hajipour@sharif.edu">sepideh.hajipour@sharif.edu</a></div>
    </div>
  </div>
</div>

<div class="cv-section">
  <h2 class="cv-section-title"><i class="fas fa-file-alt"></i> Publications</h2>

  <p>See the full list on the <a href="/publications/" style="color: #667eea; font-weight: 500;">Publications page</a> or visit my <a href="https://scholar.google.com/citations?user=2ZODsn0AAAAJ&hl=en" style="color: #667eea; font-weight: 500;">Google Scholar profile</a>.</p>
</div>
