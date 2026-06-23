---
layout: single
title: "Serverless Incident Response Pipeline"
permalink: /projects/serverless-incident-response-pipeline/
author_profile: false
---

## Overview

The **Serverless Incident Response Pipeline** is a validated AWS serverless incident response workflow that turns real CloudWatch alarm events into DynamoDB incident records and SNS email alerts.

This was not just a manually invoked Lambda demo. A real Lambda failure triggered a CloudWatch alarm, EventBridge invoked the response Lambda automatically, DynamoDB stored the incident, and SNS delivered an email alert.

> **Validated architecture flow**
>
> Failure Simulator Lambda → CloudWatch Alarm → EventBridge Rule → Alarm-to-Incident Lambda → DynamoDB → SNS Email Alert

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

- Created a Lambda function that intentionally raises an unhandled error.
- Used the failure to validate the pipeline against a real CloudWatch alarm transition.

### CloudWatch Alarm

- Monitored the simulator Lambda error metric.
- Confirmed the alarm entered `ALARM` after the failed invocation.

### EventBridge Routing

- Created an EventBridge rule for the CloudWatch alarm state change.
- Routed matching alarm events to the alarm-to-incident Lambda automatically.

### Alarm-to-Incident Lambda

- Parsed the CloudWatch alarm event.
- Derived incident fields such as ID, alarm name, severity, status, and source.
- Wrote the incident to DynamoDB and published the SNS alert.

### DynamoDB Incident Store

- Created a DynamoDB-backed incident table.
- Persisted incident records for tracking instead of treating alerts as transient messages.

### SNS Email Alerting

- Connected the response workflow to an SNS topic.
- Confirmed a real email alert was received when the incident was created.

### SAM / CloudFormation Deployment

- Packaged and deployed the system with AWS SAM and CloudFormation.
- Included Lambda functions, IAM permissions, DynamoDB, EventBridge, CloudWatch alarm resources, SNS, and S3-backed deployment artifacts.

## End-to-End Validation

The final test validated the complete AWS event path from simulated Lambda failure to persisted incident and email alert. This confirmed that the response workflow was driven by a real CloudWatch alarm transition and automatic EventBridge routing, not just a local unit test or manually invoked processor Lambda.

## Validation Evidence

This project was validated with a real deployed AWS event flow rather than only local tests or manual Lambda invocation.

Confirmed validation results:

- Failure simulator Lambda returned `FunctionError: Unhandled`
- CloudWatch alarm entered `ALARM`
- EventBridge invoked the alarm-to-incident Lambda automatically
- DynamoDB stored an incident record with:
  - `id`: `alarm-8a107dc637b96a30`
  - `alarmName`: `sirp-failure-simulator-errors-sam-dev`
  - `severity`: `HIGH`
  - `status`: `OPEN`
  - `source`: `cloudwatch`
- SNS email alert was received
- SAM/CloudFormation deployment succeeded
- `python -m unittest discover -s tests` passed with 13 tests
- `python -m compileall src tests` passed
- `sam validate --region us-east-1` returned a valid SAM template

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

- Built a serverless AWS incident response pipeline that converts CloudWatch alarm events into DynamoDB incident records and SNS email alerts.
- Deployed repeatable infrastructure with AWS SAM/CloudFormation, including Lambda, DynamoDB, SNS, CloudWatch Alarms, EventBridge, IAM, and CloudWatch Logs.
- Validated the full event flow by triggering a Lambda failure, confirming CloudWatch alarm activation, EventBridge routing, DynamoDB persistence, and SNS email delivery.
- Implemented alarm-to-incident processing logic with local validation through 13 passing unit tests, Python compile checks, and SAM template validation.
- Troubleshot IAM permissions across Lambda, EventBridge, DynamoDB, SNS, CloudWatch Logs, and CloudWatch Alarms.

## Future Improvements

- Add a small incident viewer or CLI for listing and updating open incidents
- Add automated incident closure when the CloudWatch alarm returns to `OK`
- Add richer severity mapping based on alarm name, namespace, or environment
- Add structured CloudWatch Logs queries for operational debugging
- Add deployment environments beyond `dev`

## Back to Projects link

<a href="/projects/" class="project-back-btn">← Back to Projects</a>
