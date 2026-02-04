---
layout: single
title: "Predicting Insurance Charges"
permalink: /projects/insurance-charges/
author_profile: false
---

## Overview

**Academic Project (MATH 4322, Group Project).**  
We explored how well insurance costs can be predicted from demographic and health-related variables using the **Medical Insurance Cost Dataset** (1,338 observations). The work combined:

- **Regression** with a single **Decision Tree** to predict continuous charges
- **Classification** with **Logistic Regression** to identify “high-cost” individuals

---

## Goal

Answer a practical question:

**How accurately can insurance charges be predicted based on age, BMI, smoker status, and other factors?**

Predictors used:
Age, Sex, BMI, Children, Smoker, Region

---

## What We Did

### 1) Decision Tree (Regression)
We trained a regression tree on repeated randomized splits and evaluated performance with test error.

**Approach**
- 10 runs using **80/20 train-test splits**
- Compared **unpruned vs. pruned** trees
- Used cross-validation to select the best subtree size (when pruning helped)

**Key takeaway**
Smoking consistently emerged as the dominant split, with **BMI and age** acting as secondary drivers.

---

### 2) Logistic Regression (Classification)
Because standard logistic regression needs a binary outcome, we engineered:

**high_cost = 1** if charges are in the **top 25%**, else **0**  
(75th percentile cutoff was used)

**Approach**
- 10 runs using the same **80/20 splits** (seeded for consistency)
- Converted predicted probabilities into labels using a **0.5 cutoff**
- Reported average training vs. test misclassification

**Key takeaway**
This model generalized well and highlighted **smoker status** as the strongest predictor, with **age and BMI** also meaningful.

---

## Results Summary

- **Decision Tree:** interpretable structure, moderate predictive accuracy for continuous charges  
- **Logistic Regression:** strong and stable classification performance for identifying high-cost individuals  
- **Most influential driver across both models:** **Smoker status**

---

## Tools & Techniques

- **R / RStudio**
- Train/test splits (repeated evaluation)
- Cross-validation + pruning (Decision Trees)
- Feature engineering (high_cost target)
- Model interpretability and error analysis

<br>

<a href="/projects/" class="project-back-btn">← Back to Projects</a>
