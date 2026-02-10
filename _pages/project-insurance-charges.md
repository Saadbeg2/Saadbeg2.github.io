---
layout: single
title: "Predicting Insurance Charges"
permalink: /projects/insurance-charges/
author_profile: false
---

## Overview

**Academic Project.** Completed in a statistics/machine learning course as part of a small team. We analyzed the **Medical Insurance Cost** dataset to evaluate interpretable models for both continuous charge prediction and high-cost risk classification.

Dataset details:
- 1,338 rows
- Predictors: age, sex, bmi, children, smoker, region
- Response: charges

## Decision Tree Regression

We fit decision tree regression models and compared unpruned vs. pruned trees.

- Repeated 80/20 train-test splits
- Cross-validation with `cv.tree`
- Pruning with `prune.tree`

A consistent finding was that **smoker** status acted as the dominant top-level split, with age and BMI contributing additional structure.

## Logistic Regression Classification

To frame classification, we defined:

- `high_cost = 1` for charges in the top 25%
- 75th percentile cutoff for label construction

We then evaluated logistic regression through repeated train/test runs:

- 10 repeated 80/20 splits
- 0.5 probability threshold for class assignment
- Test misclassification around **~7%** on average

## My Contribution

I focused on the logistic regression pipeline:

- Engineering the `high_cost` target from the 75th percentile rule
- Running repeated split evaluation for stability, not single-split reporting
- Summarizing misclassification behavior and predictor interpretability

This approach helped emphasize both predictive quality and model transparency.

<br>
<a href="/projects/" class="project-back-btn">← Back to Projects</a>
