---
layout: single
title: "FitPlan Pro v2 — Offline Fitness Tracking PWA"
permalink: /projects/fitplan-pro-v2/
author_profile: false
---

## Overview

**FitPlan Pro v2** is a mobile-first, offline-first fitness tracking web app built for daily execution and measurable progress. It is designed to run fully on-device with no backend, no accounts, and no cloud dependency.

## Core Problem

Many fitness tools optimize for flexibility and novelty, which often weakens consistency. FitPlan Pro v2 is built to enforce a clear weekly structure so the user can answer one question each day: did I show up and move forward?

## How It Works (High Level)

- Uses a fixed 7-day training cycle with 5 workout days and 2 rest days.
- Starts a week only after Day 1 is logged.
- Enforces one log per day and prevents invalid rest-day logging before week start.
- Tracks streak and weekly completion state from real log history.
- Surfaces training trends through simple Chart.js-based visuals.

## Data & Offline Architecture

The app uses **IndexedDB** for structured persistence and local reliability across sessions. State transitions are constraint-driven so UI reflects real system state instead of loose flags.

A **service worker** supports offline-first behavior by caching core assets so the app remains usable without network access.

## What I Focused On

- Constraint-first business rules to preserve logging integrity.
- Explicit state transitions for predictable weekly behavior.
- Low-friction UI flow with minimal controls.
- Mobile-first layout and calm, distraction-free interaction.

## Current Status

In progress and actively evolving.

Demo/Repo: [Demo/Repo (Coming Soon)](/projects/fitplan-pro-v2/#current-status)

<br>
<a href="/projects/" class="project-back-btn">← Back to Projects</a>
