# Alert Triage

## Purpose

Alert triage is the process of determining whether an alert represents malicious activity and deciding what actions should be taken.

The objective is to prioritize investigations while minimizing unnecessary escalations.

---

# Investigation Process

```text
Alert

↓

Understand what happened

↓

Collect context

↓

Gather evidence

↓

Determine severity

↓

Make a decision

↓

Document findings

↓

Escalate if required
```

---

# Possible Outcomes

## True Positive

The alert correctly identifies malicious activity.

Example

PowerShell launched from Microsoft Word with an encoded command.

---

## False Positive

Legitimate activity incorrectly classified as malicious.

Example

Administrator executed an approved maintenance script.

---

## Benign Positive

Activity appears suspicious but is expected and authorized.

Example

Security scanner performing scheduled scans.

---

# Information Required

Before making a decision an analyst should identify:

- affected user
- affected host
- source of the alert
- timestamp
- executed process
- parent process
- network activity
- previous alerts

---

# Analyst Principles

- Never investigate an alert without context.
- Every conclusion should be evidence-based.
- Avoid assumptions.
- Record every important finding.
- Escalate only when justified.

---

# Professional Reflection

Alert triage is not about deciding quickly.

It is about making the correct decision using available evidence while reducing the risk of false positives and missed incidents.

# After Triage

Once the alert has been classified:

- document investigation
- write report
- escalate if necessary
- communicate with relevant teams

Alert triage is not complete until the findings are documented.

---

# Investigation Context

Alert data alone is often insufficient to make an accurate decision.

An analyst should enrich the alert with additional context before reaching a verdict.

## User Context

Investigate:

- Username
- Department
- Role
- Privileges
- Normal activity
- Previous activity

Questions:

- Is this activity expected for this user?
- Does the user normally access this system?
- Is the account privileged?
- Could the account be compromised?

---

## Asset Context

Investigate:

- Hostname
- IP address
- Operating system
- Asset owner
- Business function
- Criticality
- Environment

Questions:

- Is this a workstation or server?
- Is the system business-critical?
- Is it a production asset?
- Who owns the system?

---

## Network Context

Investigate:

- Source IP
- Destination IP
- Subnet
- Network segment
- Internal or external communication
- Related systems

Questions:

- Where is the affected system located?
- Is it internet-facing?
- What systems can it communicate with?
- Could this activity indicate lateral movement?

---

# Lookups

Lookups provide additional information that is not always included in the original alert.

Useful lookup sources may include:

- Asset inventory
- Identity directory
- Network diagrams
- SIEM
- EDR
- Threat intelligence

The purpose of a lookup is to reduce uncertainty during an investigation.

---

# Workbooks

A SOC workbook provides a structured investigation workflow.

Instead of relying on memory, an analyst can follow predefined investigation steps.

A useful workbook should help answer:

1. What happened?
2. Who was involved?
3. Which asset was affected?
4. What additional context is available?
5. What evidence should be collected?
6. What decision should be made?
7. Should the alert be escalated?

---

# Analyst Notes

### Why does this matter?

An alert without context can be misleading.

For example, a successful login from an unusual location may initially look suspicious. Additional information about the user, asset, VPN usage or expected business activity may completely change the verdict.

### Common Mistake

Making a decision based only on the information contained in the alert.

### How would I verify this?

Use available internal sources to enrich the alert before deciding whether it is malicious.

### Additional Evidence

- Identity information
- Asset information
- Network topology
- Previous alerts
- SIEM logs
- EDR telemetry
- Threat intelligence

---

# Professional Reflection

A SOC analyst needs to understand the affected user, asset and network context before determining whether activity is suspicious.

Workbooks can make this process consistent and reduce the chance of missing important investigation steps.
