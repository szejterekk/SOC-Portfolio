# SOC Metrics

## Purpose

SOC metrics are measurable indicators used to evaluate the effectiveness and efficiency of a Security Operations Center.

Metrics help security teams identify weaknesses, measure performance, and improve detection and response processes.

Metrics should not be viewed only as performance scores. They should provide useful information that helps the SOC improve its processes and security outcomes.

---

## Why Metrics Matter

A SOC needs measurable objectives to understand whether its processes are working effectively.

Metrics can help identify:

- Slow alert detection
- Slow alert acknowledgement
- Slow incident response
- High false positive rates
- Investigation bottlenecks
- Process inefficiencies
- Areas requiring improvement

A metric becomes useful when it leads to an actionable improvement.

---

## Service Level Agreement (SLA)

A Service Level Agreement defines expected service levels and response requirements.

In a SOC environment, an SLA may define how quickly an alert or incident should be acknowledged, investigated, or responded to depending on its severity.

Example:

```text
Critical Alert
      ↓
Acknowledgement within defined SLA
      ↓
Investigation
      ↓
Response / Escalation
```

SLA requirements can vary depending on:

- Alert severity
- Business impact
- Type of incident
- SOC operating hours
- Organizational requirements

---

## Mean Time to Detect (MTTD)

MTTD measures the average time between an attack or security event occurring and the SOC detecting it.

A lower MTTD generally indicates that threats are being detected more quickly.

### Why MTTD Matters

A long detection time gives an attacker more opportunity to:

- Establish persistence
- Move laterally
- Access additional systems
- Exfiltrate data
- Cause further damage

Reducing MTTD can therefore reduce the amount of time an attacker remains undetected.

---

## Mean Time to Acknowledge (MTTA)

MTTA measures the average time between an alert being generated and the SOC acknowledging it.

Acknowledgement indicates that an analyst or team has recognized the alert and taken ownership of it.

### Why MTTA Matters

A high MTTA may indicate:

- Alert queue overload
- Insufficient staffing
- Poor alert prioritization
- Inefficient workflows
- Unclear ownership

Reducing MTTA helps ensure alerts are reviewed promptly.

--- 

## Mean Time to Respond (MTTR)

MTTR measures the average time required to respond to and resolve a security incident.

The exact definition of MTTR can vary between organizations.

A response may include:

- Investigation
- Containment
- Eradication
- Recovery
- Final documentation

### Why MTTR Matters

A shorter response time can limit the impact of a security incident.

However, reducing response time should not come at the cost of investigation quality.

---

## False Positive Rate

False Positive Rate measures how many alerts are incorrectly identified as malicious or suspicious compared with the total number of alerts investigated.

False Positive Rate = False Positive Alerts / Total Alerts × 100

### Example

If a SOC investigates 100 alerts and 80 are determined to be false positives:

80 / 100 × 100 = 80%

The False Positive Rate is therefore: 80%

### Why False Positives Matter

A high false positive rate can cause:

- Alert fatigue
- Analyst burnout
- Wasted investigation time
- Delayed response to real threats
- Reduced trust in detections

Reducing unnecessary alerts allows analysts to focus on higher-value investigations.

---

## Triage Metrics

Metrics can also be used to evaluate the alert triage process.

Examples include:

- Alert volume
- False Positive Rate
- Mean Time to Acknowledge
- Mean Time to Detect
- Mean Time to Respond
- SLA compliance
- Escalation rate
- Investigation duration

These metrics can help identify weaknesses in the alert handling process.

---

## Improving SOC Metrics

Metrics should be used to identify the cause of a problem rather than simply assigning blame.

### High False Positive Rate

Possible causes:

- Poorly tuned detection rules
- Excessive alerting
- Missing context
- bIncorrect thresholds
- Legitimate activity triggering detections

Possible improvements:

- Tune detection rules
- Adjust thresholds
- Improve alert context
- Add appropriate exclusions
- Review recurring false positives

### High MTTA

Possible causes:

- Large alert queue
- Poor prioritization
- Insufficient staffing
- Unclear alert ownership
- Inefficient workflows

Possible improvements:

- Improve alert prioritization
- Automate repetitive tasks
- Improve escalation procedures
- Review staffing requirements
- Improve alert routing

### High MTTR

Possible causes:

- Complex incidents
- Missing investigation data
- Poor documentation
- Inefficient escalation
- Lack of automation
- Limited analyst experience

Possible improvements:

- Improve investigation workflows
- Create and maintain playbooks
- Improve documentation
- Automate repetitive actions
- Improve collaboration between SOC roles

--- 

## Metrics and the L1 Analyst

An L1 analyst can influence SOC performance metrics through everyday investigation decisions.

Examples include:

- Acknowledging alerts promptly
- Following investigation procedures
- Collecting relevant evidence
- Correctly classifying alerts
- Avoiding unnecessary escalations
- Documenting investigations accurately
- Identifying recurring false positives
- Providing useful feedback about detection quality

The goal should not be to make a metric look better at the expense of investigation quality.

--- 

## Metric Relationships

SOC metrics should be considered together rather than in isolation.

For example:
```text
Improving Detection
        ↓
Lower MTTD
        ↓
More Alerts Detected Earlier
        ↓
Potential Increase in Alert Volume
        ↓
Higher Analyst Workload
        ↓
Potential Increase in MTTA
```
Similarly:
```text
Poor Detection Rules
        ↓
High False Positive Rate
        ↓
Alert Fatigue
        ↓
Lower Analyst Efficiency
        ↓
Potentially Higher MTTA and MTTR
```
A change that improves one metric may negatively affect another.

---

## Important Principle

A good SOC should not optimize a single metric at the expense of overall security effectiveness.

For example, reducing MTTR is not necessarily a positive outcome if analysts are closing incidents too quickly without collecting enough evidence.

Metrics should be interpreted in context and used to identify meaningful improvements.

---

## Analyst Notes

### Why Does This Matter?

SOC metrics provide visibility into how effectively a security team detects, investigates, and responds to threats.

For an L1 analyst, understanding these metrics helps explain how individual investigation decisions can affect the wider SOC operation.

### Common Mistakes

#### Focusing on Speed Alone

Fast investigations are not useful if they result in incorrect classifications or incomplete reports.

#### Ignoring False Positives

A high volume of unnecessary alerts can consume analyst time and reduce the ability to focus on genuine threats.

##### Optimizing One Metric

Improving one metric does not automatically mean that the SOC is performing better overall.

### How Would I Improve a Metric?

Before changing a process, identify why the metric is performing poorly.

A useful improvement process is:
```text
Identify the Problem
        ↓
Analyze the Cause
        ↓
Implement an Improvement
        ↓
Measure the Result
        ↓
Review and Adjust
```

---

## Professional Reflection

SOC metrics provide a way to measure the effectiveness of security operations and identify areas that require improvement.

The most important lesson is that metrics should support better security decisions rather than become goals by themselves.

As an L1 analyst, accurate triage, timely acknowledgement, evidence-based classification, and good documentation can contribute directly to the overall performance of the SOC.
