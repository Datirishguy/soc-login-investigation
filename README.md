# SOC Investigation: Detecting Suspicious Login Activity

## Project Overview

This project simulates a Security Operations Centre (SOC) investigation into potentially suspicious login activity using fictional Windows security log data.

The aim is to identify repeated failed login attempts, recognise patterns that may indicate a security concern, and document appropriate defensive recommendations.

## Objectives

- Understand basic Windows authentication events.
- Identify repeated failed login attempts.
- Examine timestamps, usernames and source IP addresses.
- Distinguish suspicious patterns from activity that requires further context.
- Produce a clear, evidence-based investigation report.

## Tools and Data

- **Data:** Synthetic Windows-style security events created for this project.
- **Analysis:** Spreadsheet-based analysis initially, with optional Python exercises later.
- **Documentation:** Markdown and GitHub.

No real user accounts, passwords or private organisational logs are used.

## Investigation Plan

1. Review the sample security events.
2. Identify failed login attempts and repeated patterns.
3. Group events by source IP address and target username.
4. Assess the available evidence and its limitations.
5. Write findings and recommend next steps.

## Findings

The review of 12 fictional Windows security events identified:

- **8 failed logins** (Event ID 4625).
- **4 successful logins** (Event ID 4624).
- **3 consecutive failed login attempts** against the `admin` account between 09:04 and 09:06.
- All three failed admin attempts originated from `192.0.2.10`.
- No successful login to the `admin` account appears in the sample data.

The repeated failed attempts against an administrative account warrant further investigation. However, the available evidence does not confirm an attack or account compromise.

See [`investigation.md`](investigation.md) for the detailed investigation report.

## Recommendations

- Review surrounding authentication events for additional suspicious activity.
- Investigate the source IP address and determine whether the activity was expected.
- Check for any successful logins following the failed attempts.
- Preserve relevant logs and escalate the alert if further evidence suggests malicious activity.
- Follow the organisation's incident response procedures.

These are recommended investigative actions, not confirmation that an attack occurred.

## Disclaimer

This is an educational portfolio project using fictional data. The scenarios are simulated and do not represent a real security incident.
