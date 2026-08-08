# Alert Triage

## Purpose

Alert triage is the process of assessing a security alert, gathering relevant context and evidence, and determining the appropriate response.

The objective is to prioritize investigations accurately while minimizing false positives and unnecessary escalations.

---

## Investigation Process

```text
Alert
  ↓
Initial Review
  ↓
Context Enrichment
  ↓
Evidence Collection
  ↓
Investigation
  ↓
Severity Assessment
  ↓
Decision
  ↓
Reporting
  ↓
Escalation / Closure
```

---

## Initial Review

Before investigating an alert, the analyst should understand what triggered it and establish the initial scope of the investigation.

The analyst should identify:

- Alert source
- Timestamp
- Affected user
- Affected host
- Initial activity
- Relevant processes
- Network activity

The initial review provides the starting point for the investigation.

---

## Context Enrichment

Alert data alone is often insufficient to make an accurate decision.

The analyst should gather additional context about the affected user, asset, and network environment.

### User Context

Relevant information includes:

- Username
- Department
- Role
- Privileges
- Normal activity
- Previous activity

Questions to consider:

- Is this activity expected for this user?
- Does the user normally access this system?
- Is the account privileged?
- Could the account be compromised?

### Asset Context

Relevant information includes:

- Hostname
- IP address
- Operating system
- Asset owner
- Business function
- Criticality
- Environment

Questions to consider:

- Is this a workstation or server?
- Is the system business-critical?
- Is it a production asset?
- Who owns the system?

### Network Context

Relevant information includes:

- Source IP
- Destination IP
- Subnet
- Network segment
- Internal or external communication
- Related systems

Questions to consider:

- Where is the affected system located?
- Is it internet-facing?
- What systems can it communicate with?
- Could this activity indicate lateral movement?

---

## Lookups

Lookups provide additional information that may not be included in the original alert.

Common lookup sources include:

- Asset inventory
- Identity directory
- Network diagrams
- SIEM
- EDR
- Threat intelligence

The purpose of a lookup is to reduce uncertainty and provide additional context during an investigation.

---

## Evidence Collection

After establishing the initial context, the analyst should collect relevant evidence.

Depending on the alert, this may include:

- Event Logs
- Process Tree
- Command Line
- Network Connections
- File information
- Previous alerts
- Security telemetry

Evidence should be relevant to the alert and should support the final investigation decision.

---

## Workbooks

A SOC workbook provides a structured investigation workflow.

Instead of relying entirely on memory, an analyst can follow predefined investigation steps.

A useful workbook should help answer:

1. What happened?
2. Who was involved?
3. Which asset was affected?
4. What additional context is available?
5. What evidence should be collected?
6. What decision should be made?
7. Should the alert be escalated?

Workbooks help make investigations more consistent and reduce the risk of missing important steps.

---

## Severity Assessment

Severity should be determined based on the available evidence and potential impact.

Factors may include:

- Nature of the activity
- Affected asset
- User privileges
- Business impact
- Evidence of compromise
- Potential attacker objectives

A suspicious event affecting a highly privileged account or critical production system may require greater attention than the same activity on a low-risk workstation.

---

## Possible Outcomes

### True Positive

The alert correctly identifies malicious activity.

**Example:**

PowerShell is launched from Microsoft Word with an encoded command and the activity is confirmed to be malicious.

### False Positive

The alert is triggered by activity that does not represent the condition the detection was designed to identify.

**Example:**

A legitimate administrative process unexpectedly triggers a detection rule.

### Benign Positive

The activity appears suspicious but is known to be legitimate and authorized.

**Example:**

A security scanner performs an approved scheduled scan that triggers a detection.

---

## Analyst Principles

- Never investigate an alert without sufficient context.
- Base conclusions on evidence.
- Avoid assumptions.
- Consider the affected user and asset.
- Understand the potential business impact.
- Document important findings.
- Escalate when required.
- Do not close an alert without a justified conclusion.

---

## Analyst Notes

### Why Does This Matter?

An alert without context can be misleading.

For example, a successful login from an unusual location may initially look suspicious. Additional information about the user, VPN usage, affected asset, and expected business activity may completely change the verdict.

Context allows the analyst to distinguish between genuinely suspicious activity and legitimate behavior that only appears unusual.

### Common Mistakes

#### Making a Decision Too Early

Classifying an alert based only on the information contained in the initial alert can lead to incorrect conclusions.

#### Ignoring Asset Criticality

The same activity can have a very different impact depending on whether it occurs on a regular workstation or a critical production server.

#### Ignoring User Context

A suspicious action performed by a standard user may require a different investigation from the same action performed by a privileged administrator.

#### Relying on Assumptions

Suspicious activity should be validated using available evidence rather than assumptions.

### How Would I Verify This?

Use available internal sources to enrich the alert and collect supporting evidence before reaching a conclusion.

Depending on the alert, this may include:

- Identity information
- Asset information
- Network topology
- Previous alerts
- SIEM logs
- EDR telemetry
- Threat intelligence

---

## Professional Reflection

Alert triage is not simply deciding whether an alert is malicious.

It is a structured investigation that combines the initial alert with user, asset, and network context and supporting evidence.

The goal is to make a justified decision based on available evidence and provide enough information for the next stage of the incident response process.
