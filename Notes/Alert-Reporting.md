# Alert Reporting

## Purpose

Alert reporting documents the investigation and provides enough context for another analyst to continue the case without repeating the same work.

A good report should explain not only *what happened*, but also *why the analyst reached a specific conclusion*.

---

# Report Objectives

- Preserve investigation results
- Support L2 analysts
- Create long-term documentation
- Improve investigation quality

---

# The Five Ws

## Who

Who performed the activity?

Examples:
- User
- Service Account
- Administrator

---

## What

What happened?

Examples:
- PowerShell executed
- File downloaded
- Login attempt
- Registry modified

---

## When

When did the activity occur?

Include:

- Date
- Time
- Timezone

---

## Where

Where did it happen?

Examples:

- Hostname
- IP Address
- URL
- Process
- File Path

---

## Why

Explain your conclusion using evidence.

Never write:

"I think it is malicious."

Instead:

"The activity matches malicious behavior because PowerShell was launched by WINWORD.EXE using an encoded command."

---

# Good Report Principles

- Clear
- Concise
- Evidence-based
- Professional
- Easy to continue by another analyst

---

# Professional Reflection

Writing reports is part of the investigation itself.

If another analyst cannot understand what happened by reading the report, the report is incomplete.
