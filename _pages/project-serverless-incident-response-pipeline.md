---
layout: single
title: "Serverless Incident Response Pipeline"
permalink: /projects/serverless-incident-response-pipeline/
author_profile: false
---

## Overview

The **Serverless Incident Response Pipeline** is an event-driven AWS workflow that turns real CloudWatch alarm events into tracked incidents. It uses Lambda, CloudWatch Alarms, EventBridge, DynamoDB, SNS, and AWS SAM to model a realistic incident response path without relying on a generic CRUD interface.

The final validated flow is:

**Failure Simulator Lambda → CloudWatch Alarm → EventBridge Rule → Alarm-to-Incident Lambda → DynamoDB → SNS Email Alert**

The project was built for cloud engineering practice, with emphasis on AWS-native event routing, incident persistence, repeatable infrastructure deployment, and least-privilege IAM troubleshooting.

## Problem

Cloud alerts are only useful if they reliably become actionable records and notifications. A CloudWatch alarm can show that something is wrong, but an incident response workflow needs more structure:

- A reliable way to detect a real alarm transition
- Automatic routing from monitoring into response logic
- Persistent incident records for tracking
- Alert delivery to a human operator
- Repeatable deployment through infrastructure as code

This project answers the question:

> How can a real CloudWatch alarm become a durable incident record and an email alert using AWS-native serverless services?

## Architecture / Flow

The pipeline begins with a failure simulator Lambda that intentionally raises an unhandled error. That error increments the Lambda error metric monitored by a CloudWatch alarm. When the alarm enters `ALARM`, EventBridge captures the alarm state change and invokes the alarm-to-incident Lambda.

The alarm-to-incident Lambda parses the CloudWatch alarm event, creates or updates an incident record in DynamoDB, assigns severity and status, and publishes an SNS email alert. The alarm processor uses idempotent handling so repeated alarm events map cleanly to the same incident pattern instead of producing uncontrolled duplicates.

Validated deployed resources:

- Stack name: `sirp-dev`
- DynamoDB table: `sirp-incidents-sam-dev`
- Failure simulator Lambda: `sirp-failure-simulator-sam-dev`
- Alarm processor Lambda: `sirp-alarm-to-incident-sam-dev`
- CloudWatch alarm: `sirp-failure-simulator-errors-sam-dev`
- EventBridge rule: `sirp-failure-simulator-alarm-rule-sam-dev`
- SNS topic: `sirp-incident-alerts-dev`

## AWS Services Used

- AWS Lambda
- DynamoDB
- SNS
- CloudWatch Alarms
- EventBridge
- CloudFormation / AWS SAM
- IAM
- S3 for SAM deployment artifacts
- CloudWatch Logs

## What I Built

### Failure Simulator Lambda

Built a Lambda function that intentionally fails so the pipeline can be validated against a real CloudWatch alarm instead of a manually fabricated event.

### CloudWatch Alarm

Configured a CloudWatch alarm to monitor the simulator Lambda error metric and enter `ALARM` when the function fails.

### EventBridge Routing

Created an EventBridge rule that listens for the specific CloudWatch alarm state change and routes the event to the alarm processor Lambda automatically.

### Alarm-to-Incident Lambda

Built the response Lambda that processes the alarm event, derives incident fields, writes the incident to DynamoDB, and publishes an SNS notification.

### DynamoDB Incident Store

Created a DynamoDB-backed incident table to persist tracked incidents with fields such as alarm name, severity, status, source, and incident ID.

### SNS Email Alerting

Connected the response workflow to an SNS topic so a real email alert is sent when the incident is created.

### SAM / CloudFormation Deployment

Packaged and deployed the system with AWS SAM and CloudFormation, including Lambda functions, IAM permissions, DynamoDB, EventBridge, CloudWatch alarm resources, SNS, and S3-backed deployment artifacts.

## End-to-End Validation

The final end-to-end test validated the full AWS event path:

- Failure simulator Lambda returned `FunctionError: Unhandled`
- CloudWatch alarm entered `ALARM`
- EventBridge invoked the alarm-to-incident Lambda automatically
- DynamoDB stored the incident record
- SNS email alert was received
- SAM/CloudFormation deployment succeeded

Validated DynamoDB incident:

- `id`: `alarm-8a107dc637b96a30`
- `alarmName`: `sirp-failure-simulator-errors-sam-dev`
- `severity`: `HIGH`
- `status`: `OPEN`
- `source`: `cloudwatch`

Local validation also passed:

- `python -m unittest discover -s tests` → 13 tests passed
- `python -m compileall src tests` → passed
- `sam validate --region us-east-1` → valid SAM template

## Screenshot Evidence

Planned screenshots for this page:

- CloudFormation stack showing `UPDATE_COMPLETE`
- CloudFormation outputs
- Lambda functions list
- Failure simulator Lambda invoke result
- CloudWatch alarm in `ALARM`
- EventBridge rule target
- DynamoDB incident item
- SNS email alert
- Terminal output showing validation

## Challenges and Troubleshooting

The most important challenge was getting a real CloudWatch alarm event to drive the workflow instead of shortcutting the system with a manual test payload. That required validating the alarm state transition, EventBridge event pattern, Lambda target invocation, and CloudWatch Logs output together.

IAM was also a key troubleshooting area. The alarm processor needed enough permission to write incidents to DynamoDB and publish to SNS, while the deployment role and generated resources needed to stay scoped to the pipeline instead of using broad permissions by default.

The project also required careful separation between deployment issues and runtime issues. SAM/CloudFormation validation proved the infrastructure template was valid, while Lambda logs, alarm state, EventBridge delivery, and DynamoDB records proved the runtime flow worked.

## Security / IAM Approach

The IAM approach focused on least-privilege learning and practical troubleshooting:

- Lambda execution roles were scoped around the actions each function needed
- The alarm processor required DynamoDB write access and SNS publish access
- CloudWatch Logs permissions supported function-level observability
- EventBridge invocation permissions were tied to the alarm processor target
- SAM/CloudFormation kept infrastructure changes repeatable and reviewable

This was not positioned as production-ready security architecture, but as hands-on practice with AWS permissions, service integrations, and infrastructure-as-code deployment.

## Results / Impact

The finished project demonstrates a realistic AWS-native incident response workflow:

- A real Lambda failure triggered a CloudWatch alarm
- EventBridge routed the alarm event without manual intervention
- DynamoDB stored a durable incident record
- SNS delivered an email alert
- SAM/CloudFormation made the deployment repeatable
- Unit tests, Python compilation, and SAM validation confirmed the local implementation and template health

The result is a practical cloud engineering project that shows event-driven design, serverless AWS integration, incident tracking, alerting, and IAM troubleshooting in one focused system.

## Resume-Ready Bullets

- Built an event-driven AWS incident response pipeline using Lambda, CloudWatch Alarms, EventBridge, DynamoDB, SNS, and AWS SAM.
- Implemented alarm-to-incident processing that converts real CloudWatch alarm events into tracked DynamoDB incidents with severity, status, source, and incident ID fields.
- Deployed repeatable serverless infrastructure with SAM/CloudFormation, including Lambda functions, EventBridge routing, CloudWatch alarm resources, DynamoDB, SNS, IAM roles, and S3 deployment artifacts.
- Validated the full response path from unhandled Lambda failure to CloudWatch `ALARM`, automatic EventBridge invocation, DynamoDB persistence, and SNS email alert delivery.
- Troubleshot least-privilege IAM permissions, CloudWatch Logs, EventBridge targets, and SAM template validation across the end-to-end workflow.

## Future Improvements

- Add a small incident viewer or CLI for listing and updating open incidents
- Add automated incident closure when the CloudWatch alarm returns to `OK`
- Add richer severity mapping based on alarm name, namespace, or environment
- Add structured CloudWatch Logs queries for operational debugging
- Add deployment environments beyond `dev`
- Add screenshots directly to the portfolio page once the evidence images are finalized

## Back to Projects link

<a href="/projects/" class="project-back-btn">← Back to Projects</a>
