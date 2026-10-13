# Investigation 01: Repeated Failed Logins

## 1. Summary

This investigation reviews fictional Windows security logs to identify potentially suspicious login activity.

Three failed login attempts were recorded against the `admin` account between 09:04 and 09:06 on 15 September 2026. All three attempts came from the same source IP address: `192.0.2.10`.

This pattern warrants further investigation, but it does not prove an attack occurred.

## 2. Evidence

| Time | Username | Source IP | Event ID | Result |
|---|---|---|---|---|
| 09:04 | admin | 192.0.2.10 | 4625 | Failed |
| 09:05 | admin | 192.0.2.10 | 4625 | Failed |
| 09:06 | admin | 192.0.2.10 | 4625 | Failed |

Event ID 4625 indicates a failed Windows logon attempt.

### Investigation Timeline

- **09:04:** A failed logon attempt was recorded for the `admin` account from `192.0.2.10`.
- **09:05:** A second failed logon attempt was recorded for the same account and source IP.
- **09:06:** A third consecutive failed logon attempt was recorded for the same account and source IP.

**Timeline assessment:** Three consecutive failed logon attempts against an administrative account warrant further investigation. The available events do not establish the cause of the failures.

## 3. Assessment

Repeated failed attempts against an administrative account may indicate incorrect password entry, a misconfigured service, or possible password guessing.

The available data is limited. The cause of the failed attempts cannot be confirmed from these events alone.

## 4. Recommended Next Steps

1. Review nearby login events for additional suspicious activity.
2. Check whether any successful login followed the failed attempts.
3. Investigate the source IP address and determine whether the activity was expected.
4. Review available logon details and failure reasons.
5. Follow the organisation's incident response procedures if further evidence suggests malicious activity.

## 5. Conclusion

The three failed login attempts against the `admin` account should be flagged for further investigation. There is insufficient evidence to confirm a cyber attack or account compromise.

**Status:** Open — further investigation required.

**Priority:** Medium (provisional) — repeated failed logins against an administrative account; severity subject to review of surrounding events and organisational alert criteria.

## Disclaimer

This is an educational project using fictional security log data. It does not represent a real security incident.

## 6. Escalation and Incident Response

If further investigation identifies a successful login to the `admin` account that the account owner does not recognise, the activity should be treated as a potential account compromise.

Recommended actions:

1. Escalate the alert to the appropriate security team.
2. Preserve relevant authentication logs for further investigation.
3. Review activity following the successful login.
4. Follow the organisation's incident response procedures.
5. Record all findings and actions taken.

**Important:** An unauthorised login has not been confirmed by the fictional evidence alone. Further investigation is required.

## 7. Overall Log Review

A review of all 12 fictional log entries identified:

**Scope and limitations:** This assessment is based on 12 fictional Windows security events supplied for the exercise. The available dataset is limited and may not include all relevant authentication activity, host context, or supporting security telemetry. Findings are therefore preliminary and should be validated against additional logs and organisational context before drawing a final conclusion.

- **8 failed logins** (Event ID 4625).
- **4 successful logins** (Event ID 4624).
- **3 failed login attempts** against the `admin` account between 09:04 and 09:06.
- All three failed admin attempts originated from `192.0.2.10`.
- No successful login to the `admin` account appears in the supplied dataset.
- The `jsmith` account recorded successful logins from `192.0.2.10` at 09:01 and 09:12. These events occurred near the failed login activity and should be reviewed to establish whether they were expected.

**Overall assessment:** Repeated failed logins against the `admin` account and additional authentication activity involving `jsmith` were identified from the same source IP address, `192.0.2.10`. The dataset does not establish whether the activity was malicious or whether any account was compromised. Review the surrounding authentication events, validate whether the successful `jsmith` logins were expected, and escalate according to organisational procedures if further evidence supports a security incident.

**Final status:** Open — further investigation required.
