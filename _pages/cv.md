---
layout: archive
title: "Curriculum Vitae"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

## Education

**PhD in Biomedical Engineering** | 2020 - Present
*Graz University of Technology - Department of CSBME* | Graz, Austria
GPA: 1.4/5.0 | Supervisor: Gernot Muller-Putz
*Dissertation: Developed interpretable deep learning frameworks for EEG data. Applied statistical analysis, asynchronous decoding, and multi-class classification on brain signals.*

**M.Sc. in Biomedical Engineering** | 2016 - 2019
*Sharif University of Technology - Department of EE (BME group)* | Tehran, Iran
GPA: 17.16/20.00
*Thesis: Developed a novel hybrid BCI speller combining RSVP and SSVEP paradigms, achieving 93.06% classification accuracy and 23.41 bit/min information transfer rate (ITR), substantially improving performance over prior spellers.*

**B.Sc. in Electrical Engineering** | 2011 - 2016
*Guilan University - Department of EE* | Rasht, Iran

---

## Professional Experience

### University Assistant (Doctoral Researcher)
*Graz University of Technology, Graz, Austria* | 2020 - Present

- Conducted EEG-based BCI and AI research, resulting in three Q1 journal papers and two conference publications
- Developed an interpretable deep learning framework for cross-subject EEG classification, sustaining 96.8% subject-independent accuracy while reducing model parameters by >50x compared with conventional CNNs
- Built a DL pipeline for denoising large-scale biosignal data of 500k+ samples (547 participants, ~100 GB, ~200 hours) using Vision Transformer (ViT) and U-Net architectures, granted access to Vienna cluster service (VCS) GPUs, in collaboration with University of San Diego (UCSD) as part of the Marshall Plan Scholarship
- Performed statistical analyses across time, frequency, and source domains for characterizing neural dynamics of error processing during balance perturbation, resulting in Q1 publication
- Developed an asynchronous classifier for real-time cognitive state detection in human-machine interaction, leveraging advanced feature engineering and optimizing the model for online deployment
- Collaborated with Daimler Truck AG & FKFS on decoding the distraction events by using brain signals + IMU + truck simulator data
- **Team Lead - Mirage 91 (Cybathlon Student Team)**: Co-led a 12-member student team to design and deploy a real-time deep learning framework for the competition; set roadmap/sprints, and mentored students

### Signal Processing Engineer & Lab Manager
*National Brain Mapping Laboratory (NBML), Tehran, Iran* | 2018 - 2019

- Supervised a team of 4 specialists in a signal processing laboratory, and trained new team members in data acquisition and analysis techniques
- Designed and analyzed data for 10+ neuroscience and biomedical engineering research projects from experimental setup to statistical reporting
- Developed QA pipelines and statistical protocols for artifact reduction and reproducibility

---

## Technical Skills

**Programming & Scripting**
Python (pandas, NumPy), MATLAB

**Machine Learning & Data Science**
TensorFlow, PyTorch, scikit-learn

**Data Analysis & Statistics**
SPSS, data visualization, statistical and time-series analysis

**Tools & Platforms**
Git, HPC clusters (Bash & SLURM)

---

## Language Skills

| Language | Proficiency |
|----------|-------------|
| English | Professional (C1) |
| German | Elementary (B1) |
| Persian | Native |

---

## Teaching Experience

### University of Lisbon
- **Guest Lecturer**, *Non-invasive Brain-Computer Interfaces 1 (KU)* (2025)
  - Received a Teaching Grant for joint online course with TUG

### Graz University of Technology
- **Lecturer**, *Non-invasive Brain-Computer Interfaces 1 (KU)* (2020-2025): taught machine learning, statistical analysis, neurophysiological analysis, feature extraction, and pattern recognition
- **Lecturer**, *Non-invasive Brain-Computer Interfaces 2 (KU)* (2021-2024): taught online data processing and classification, BCI task design, and EEG instrumentation
- **Lecturer**, *Fundamentals of Biomedical Engineering, EEG Laboratory* (2020-2024)

### Sharif University of Technology
- **Head Teaching Assistant**, *Artificial Intelligence* (2018)
- **Teaching Assistant**, *Tensor Decompositions and Neural Modeling* (2018)

---

## Mentorship, Service, and Volunteer Work

- **Mentorship**: Supervised 2 Master's and 2 Bachelor's thesis students (2021 - present)
- **Conference Service**: Organizing-committee member, *Graz BCI Conference 2024* (Exhibition, Infrastructure, Poster Sessions)
- **Scientific Review**: *IEEE Transactions on Biomedical Engineering*, *Scientific Reports (Nature Portfolio)*, *IEEE Transactions on Neural Systems and Rehabilitation Engineering*, *Frontiers in Human Neuroscience*, *The Journal of Supercomputing (Elsevier)*
- **Student Team Member**: Part of the TU Graz *Mirage 91* student team competing in the BCI discipline at CYBATHLON 2024
- **Educational Outreach**: Authored educational articles for BrainProducts on the Mirage 91 CYBATHLON journey and BCI+ blog

---

## Honors and Awards

| Year | Award |
|------|-------|
| 2025 | Teaching Grant for Joint Online Course (€15k) issued by Graz University of Technology |
| 2024 | International Communication Funding (€2k) issued by Austrian Research Association |
| 2024 | Austrian Marshall Plan Scholarships (€7.5k) issued by Austrian Marshall Plan Foundation (EU-US research exchange) |
| 2020 | Full fund PhD offers from Graz University of Technology, University of Ottawa, and Ludwig Maximilian University of Munich |
| 2017 | Research grant support from Iranian Cognitive Science and Technology Council (CSTC) |
| 2016 | Ranked 65th in Nationwide M.Sc. Entrance Exam among more than 50,000 participants |
| 2011 | Among the top 10% in approximately 285,000 examinees in the Iranian Nationwide University Entrance Exam |

---

## References

**Gernot R. Muller-Putz**
Full Professor, Head of the Institute of Neural Engineering
Graz University of Technology, Graz, Austria
Email: gernot.mueller@tugraz.at

**Sepideh Hajipour Sardouie**
Assistant Professor, Electrical Engineering Department
Sharif University of Technology, Tehran, Iran
Email: sepideh.hajipour@sharif.edu

---

## Publications

<ul>{% for post in site.publications reversed %}
  {% include archive-single-cv.html %}
{% endfor %}</ul>
