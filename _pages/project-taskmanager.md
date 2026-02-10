---
layout: single
title: "TaskManager — Priority + Calendar Workflow"
permalink: /projects/taskmanager/
author_profile: false
---

## Overview

**TaskManager** is a personal system I built for my own workload management and prioritization habits. I use it to keep pressure visible, force clear next actions, and stay consistent when task volume increases.

## What It Does

- Supports priority levels including **Extremely High**.
- Separates tasks into active and completed views.
- Provides sorting controls for faster daily triage.
- Allows per-task priority edits without re-creating items.
- Applies configurable escalation rules from Settings.
- Persists task state reliably with localStorage.

## Calendar Workflow

When a task reaches extremely high urgency, it can be routed into a focused calendar flow:

- Select urgent tasks on the calendar page.
- Assign date, start time, and duration.
- Generate a standards-based **.ics** file.
- Import manually into a preferred calendar app.

## UX Notes

- Mobile-first layout for quick capture and review.
- Show more/less behavior for long task text.
- Extremely high tasks are grouped for fast visibility.
- Interaction model emphasizes clarity and low friction over customization.

## Status

Actively used and continuously iterated as my workflow changes.

## What I'm refining next

- Simplifying mobile task scanning so high-priority queues are faster to review.
- Tightening escalation edge-case handling so rule behavior remains predictable under heavy churn.
- Tuning priority rule defaults based on real usage patterns without expanding scope.

<br>
<a href="/projects/" class="project-back-btn">← Back to Projects</a>
