# SOC Investigation: Detecting Suspicious Login Activity

## Project Overview

This project simulates a Security Operations Centre (SOC) investigation into potentially suspicious login activity using fictional Windows security log data.

The aim is to identify repeated failed login attempts, recognise patterns that may indicate a security concern, assess the available evidence, and document appropriate defensive recommendations.

## Objectives

- Understand basic Windows authentication events.
- Identify repeated failed login attempts.
- Examine timestamps, usernames, and source IP addresses.
- Distinguish suspicious patterns from activity requiring further context.
- Produce a clear, evidence-based investigation report.

## Tools and Data

- **Data:** Synthetic Windows-style security events created for this project.
- **Analysis:** Spreadsheet-based review of authentication events.
- **Documentation:** Markdown and GitHub.

No real user accounts, passwords, or private organisational logs are used.

## Investigation Process

1. Review the sample security events.
2. Identify failed login attempts and repeated patterns.
3. Group events by source IP address and target username.
4. Assess the evidence and its limitations.
5. Document findings and recommend next steps.

## Key Findings

The review of 12 fictional Windows security events identified:

- **8 failed logins** (Event ID 4625).
- **4 successful logins** (Event ID 4624).
- **3 consecutive failed login attempts** against the `admin` account between 09:04 and 09:06.
- All three failed admin attempts originated from `192.0.2.10`.
- No successful login to the `admin` account appears in the supplied dataset.
- The `jsmith` account recorded successful logins from `192.0.2.10` at 09:01 and 09:12. These events require further review to determine whether they were expected.

The repeated failed attempts against an administrative account warrant further investigation. The available evidence does not confirm an attack or account compromise.

## Skills Demonstrated

- Windows authentication event analysis.
- Identification of repeated failed logins.
- Basic event timeline analysis.
- Review of usernames, timestamps, and source IP addresses.
- Evidence-based incident assessment.
- Security documentation and defensive recommendations.

## Recommendations

- Review surrounding authentication events for additional suspicious activity.
- Investigate the source IP address and establish whether the activity was expected.
- Validate the successful `jsmith` logins against the available context.
- Preserve relevant logs and escalate if further evidence suggests malicious activity.
- Follow the organisation's incident response procedures.

These are recommended investigative actions, not confirmation that an attack occurred.

## Investigation Report

See [`investigation.md`](investigation.md) for the detailed investigation, evidence, timeline, assessment, and recommended response actions.

## Disclaimer

This is an educational portfolio project using fictional data. The scenario is simulated and does not represent a real security incident.
