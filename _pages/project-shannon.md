---
layout: single
title: "Shannon Coding Multithreaded Encoder"
permalink: /projects/shannon-encoder/
author_profile: false
---

## Overview

**Academic Project.** This project implements **Shannon coding** using a **multithreaded POSIX threads (pthreads)** design. The goal was to take an input message, build a frequency model, generate Shannon codes, and output a deterministic encoded result while following strict threading and code-quality constraints.

---

## What I Built

A command-line encoder that:

- Parses input text and builds a **symbol frequency table**
- Sorts symbols deterministically (by frequency, then ASCII to break ties)
- Computes **Shannon codes** for each symbol
- Uses **POSIX threads** to separate major steps and improve structure
- Produces a clean encoded output and readable supporting tables

---

## How I Approached It

To keep the implementation safe and predictable under concurrency, I focused on:

- **Thread-safe design:** avoided shared mutable state where possible  
- **No global variables:** passed data via structs and thread arguments  
- **Deterministic output:** stable sorting rules so results don’t vary run-to-run  
- **Clear separation of work:** modeling → code generation → encoding

---

## What This Demonstrates

- Comfort with **low-level systems programming**
- Practical understanding of **threads and synchronization**
- Ability to implement a compression technique from specification
- Writing clean, structured code under real assignment constraints

---

## Tech Stack

- C / C++  
- POSIX Threads (pthreads)

<br>

<a href="/projects/" class="project-back-btn">← Back to Projects</a>
