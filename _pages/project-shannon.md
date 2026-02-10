---
layout: single
title: "Shannon Coding Multithreaded Encoder"
permalink: /projects/shannon-encoder/
author_profile: false
---

## Overview

**Academic Project.** This project implements Shannon coding with POSIX threads to produce deterministic encoded output from input text while respecting systems-level constraints.

## Approach

- Built a frequency table from input symbols.
- Applied deterministic sorting rules (frequency first, then ASCII tie-break).
- Generated Shannon codes from symbol probabilities.
- Structured processing with pthread-based concurrency while preserving safe data flow and deterministic output order.

## What I Learned

- Thread safety must be planned upfront, not patched later.
- Concurrency logic is only useful when output remains reproducible.
- Small formatting and ordering details can break correctness in systems assignments.

<br>
<a href="/projects/" class="project-back-btn">← Back to Projects</a>
