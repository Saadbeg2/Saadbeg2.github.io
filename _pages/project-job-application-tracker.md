---
layout: single
title: "Job Application Accountability Tracker"
permalink: /projects/job-application-tracker/
author_profile: false
---

## Overview

The **Job Application Accountability Tracker** is a full-stack web application I built to manage my job search in one place. It tracks job applications, organizes follow-up tasks, reviews Gmail-detected job updates, syncs clean tracker data to Google Sheets, and sends daily accountability email reports.

The project was built around my real workflow as a new graduate applying to jobs. Instead of being a basic spreadsheet replacement, it combines application tracking, Gmail-assisted review, task management, follow-up logic, and progress reporting into a single local dashboard.

It is currently a **local full-stack application**, with deployment planned.

## Problem

Managing a job search across job boards, Gmail, recruiter emails, spreadsheets, and follow-up reminders can quickly become disorganized.

I needed a system that could answer:
- What jobs did I apply to?
- What stage is each application in?
- Did Gmail receive an update I should review?
- What tasks do I need to complete?
- Which applications need follow-up?
- How can I share progress with family or mentors?

A spreadsheet was useful, but it did not provide Gmail review, task automation, follow-up logic, timezone-safe reporting, or daily accountability emails.

## Tech Stack

### Frontend
- Next.js
- React
- TypeScript
- Custom CSS

### Backend
- Next.js API routes
- TypeScript

### Database
- Prisma ORM
- SQLite

### Integrations
- Gmail API
- Google OAuth
- Google Sheets API

### Email
- SMTP
- Gmail App Password
- Nodemailer

### Tools
- Git
- npm
- Prisma CLI
- Codex-assisted development

## What I Built

### Application Tracker
Built a CRUD system for job applications with fields for company, role, status, date applied, location, job link, source, and notes. Applications are grouped into collapsible status sections such as Interview, Applied, Offer, Rejected, and Withdrawn so active opportunities are easier to scan.

### Task Manager
Built a task system for job-search actions. Tasks are separated into Active and Completed sections, searchable, and can be linked to specific applications through `applicationId`.

### Gmail Review Queue
Integrated Gmail scanning to detect job-related emails. Instead of automatically adding Gmail data to the tracker, the app creates review items that can be approved, edited, ignored, or marked not relevant.

To protect tracker accuracy and reduce privacy risk, the workflow avoids storing raw Gmail bodies, threads, or attachments in the tracker dataset.

### Status Update Matching
Added logic so Gmail-detected status updates can be matched to a specific application. This prevents one company-level update from incorrectly affecting multiple applications from the same company.

### Google Sheets Sync
Integrated Google Sheets syncing so approved application and task data can be shared externally without exposing raw Gmail content.

### Daily Accountability Reports
Built automated email reports that send job-search progress to configured recipients. Reports are timezone-aware and summarize yesterday in `America/Chicago`.

### Follow-Up Task Automation
Built logic to detect stale applications and automatically create follow-up tasks after 10+ days for active Applied or Interview applications. Completing the follow-up task updates the application’s follow-up timestamp and resets the reminder clock.

### UI Design System
Created a custom dark dashboard interface inspired by Linear, Vercel, and Raycast using plain CSS, reusable utility classes, glass cards, subtle borders, dark form inputs, and responsive layouts.

## Challenges

### Gmail Classification
Job emails often come from platforms like LinkedIn, Workday, Indeed, ApplyToJob, and company-specific systems where the sender is not always the actual employer. I handled this by adding platform-specific extraction rules and routing uncertain items into a Review Queue.

### Data Accuracy
The app avoids automatically creating records from Gmail because misclassifications could corrupt tracker data. Manual approval keeps the tracker accurate while still reducing manual work.

### Multiple Applications at the Same Company
The tracker supports multiple roles at the same company, so status updates must be matched to a specific application instead of being applied broadly.

### Timezone Issues
Late-night applications created UTC date bugs. I addressed this by using `America/Chicago` date logic for application dates, dashboard analytics, follow-ups, and daily reports.

### Workflow Design
Follow-up reminders were originally treated like alerts, but I redesigned them as tasks because they represent actions the user needs to take.

## Results / Impact

This project gives me a structured, automated way to manage a real job search. It helps centralize applications, review Gmail updates without losing control of the data, stay on top of follow-ups, sync progress to a shareable Google Sheet, send daily accountability reports, and prioritize active applications over closed ones.

From a technical perspective, it demonstrates full-stack development, real API integrations, Prisma data modeling, workflow automation, email automation, date/timezone handling, and product-driven engineering decisions.

## Future Improvements

- Add Date Completed support for completed tasks if not already implemented
- Add task creation directly from an application
- Create grouped task views by application/interview process
- Deploy with authentication
- Add admin/viewer roles for family or mentor access
- Move from SQLite to hosted Postgres for deployment
- Potentially revisit Job Discovery as an experimental future module

<br>
<a href="/projects/" class="project-back-btn">← Back to Projects</a>
