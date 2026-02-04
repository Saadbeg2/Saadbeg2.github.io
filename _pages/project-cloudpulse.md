---
layout: single
title: "CloudPulse — Multi-Region AWS Infrastructure Monitoring"
permalink: /projects/cloudpulse/
author_profile: false
---

## Overview

**CloudPulse** is a React-based AWS infrastructure monitoring dashboard designed to provide **centralized visibility across multi-region cloud environments**. The project focuses on aggregating cost, performance, security, and network signals into a single interface to better understand how distributed AWS systems behave at scale.

This project was built as a **capstone-style system**, emphasizing architecture, data integration, and real-world cloud constraints rather than UI polish alone.

---

## Problem Statement

Monitoring AWS infrastructure across multiple regions often requires switching between services such as CloudWatch, Cost Explorer, EC2, and networking dashboards. This fragmentation makes it difficult to:

- Understand cross-region cost trends
- Correlate performance and network behavior
- Identify security-relevant access patterns
- Maintain operational awareness as infrastructure scales

CloudPulse was designed to answer a simple question:

> *How can I view cost, performance, network, and security signals for a multi-region AWS deployment from a single place?*

---

## Scope & Constraints

- Read-only AWS access
- Real-time data pulled directly from AWS APIs
- No centralized backend (client-side aggregation)
- Multi-region infrastructure with mixed networking patterns:
  - Transit Gateway
  - VPC Peering

These constraints intentionally mirror common early-stage and internal tooling environments.

---

## Architecture Overview

CloudPulse uses a **frontend-driven architecture** built on React and the AWS SDK:

- **React 18** handles UI state, data orchestration, and rendering
- **AWS SDK for JavaScript** integrates directly with AWS APIs
- **Chart.js** visualizes cost, performance, and network trends

### AWS Services Integrated
- **CloudWatch** — EC2, Transit Gateway, and network metrics
- **Cost Explorer** — daily and cumulative regional cost data
- **EC2** — instance discovery and status monitoring
- **S3** — access pattern monitoring for sensitive buckets
- **Transit Gateway & VPC Peering** — network traffic visibility

---

## Key Design Decisions

### 1. Multi-Region First
The system treats regions as first-class entities, allowing real-time switching and comparison across **7 AWS regions**, including North America and Asia-Pacific.

### 2. Client-Side Aggregation
To avoid backend complexity, CloudPulse aggregates AWS API responses in the frontend. This highlights:
- API rate limits
- Data freshness tradeoffs
- Cost Explorer latency constraints

### 3. Read-Only Security Model
IAM permissions are scoped strictly to monitoring actions, reinforcing least-privilege access and reducing operational risk.

---

## Monitoring Capabilities

### Cost Visibility
- Daily and cumulative cost tracking
- Region-level breakdowns
- 7-day historical trend analysis

### Performance Monitoring
- EC2 CPU and network utilization
- Multi-instance support (bastion + private instances)
- Historical performance trends

### Network Observability
- Transit Gateway traffic (BytesIn / BytesOut)
- VPC peering connection visibility
- Cross-region connectivity awareness

### Security Awareness
- S3 access monitoring for sensitive resources
- Request pattern visibility
- Recent access source tracking

---

## What This Project Demonstrates

- **Multi-region AWS architecture understanding**
- **Direct AWS API integration**
- **Cost, security, and performance tradeoff awareness**
- **Designing under real cloud constraints**
- **Frontend systems orchestration without a backend**

This project prioritizes **engineering judgment** over feature quantity.

---

## What I’d Improve Next

- Backend aggregation layer for historical data retention
- Alerting for cost spikes and performance thresholds
- IAM scoping per service and region
- Multi-account AWS support
- Persistent storage for long-term trend analysis

---

## Tech Stack

- React 18  
- AWS SDK (JavaScript)  
- Chart.js  
- CloudWatch, Cost Explorer, EC2, S3, Transit Gateway  
- CSS3 (custom styling)

---

<a href="/projects/" class="project-back-btn">← Back to Projects</a>
