---
layout: single
title: "FitPlan Pro v2 — Offline Fitness Tracking PWA"
permalink: /projects/fitplan-pro-v2/
author_profile: false
---

## Overview

**FitPlan Pro v2** is a personal fitness system I built for my own consistency. I use it to turn motivation into discipline through a fixed weekly structure, strict logging rules, and offline-first reliability that I can depend on every day.

## Core Problem

Most fitness tools add options but reduce adherence. FitPlan Pro v2 takes the opposite approach: fewer decisions, stricter constraints, and clear accountability so each day resolves to one outcome, either training was logged correctly or it was not.

## How It Works (High Level)

- Uses a fixed 7-day training cycle with 5 workout days and 2 rest days.
- Starts a week only after Day 1 is logged.
- Enforces one log per day and prevents invalid rest-day logging before week start.
- Tracks streak and weekly completion state from real logs only.
- Surfaces progression trends through simple Chart.js-based views.

## Data & Offline Architecture

The app uses **IndexedDB** for structured persistence and reliability across sessions. State transitions are explicit and constraint-driven so the UI always reflects actual system state.

A **service worker** supports offline-first behavior by caching core assets so logging and review remain available without network access.

## What I Focused On

- Preserving logging integrity through strict weekly rules.
- Keeping state transitions predictable and auditable.
- Reducing decision fatigue with a minimal, disciplined flow.
- Maintaining a calm, mobile-first interface with low friction.

## Current Status

Actively used and continuously iterated as my training routine evolves.

## What I'm refining next

- Tightening weekly state transitions to reduce ambiguity around week rollover and cleanup.
- Improving progress views so trend checks are faster without adding new interaction overhead.
- Hardening validation around log edits and recovery paths to keep history accurate.

Demo/Repo: [Demo/Repo (Coming Soon)](/projects/fitplan-pro-v2/#current-status)

<br>
<a href="/projects/" class="project-back-btn">← Back to Projects</a>
