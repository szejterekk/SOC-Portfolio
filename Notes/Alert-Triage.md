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
