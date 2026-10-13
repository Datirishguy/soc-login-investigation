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

## Disclaimer

This is an educational project using fictional security log data. It does not represent a real security incident.

## 6. Escalation and Incident Response

If the administrator confirms that the successful login was not theirs, the activity should be treated as a potential account compromise.

Recommended actions:

1. Escalate the alert to the appropriate security team.
2. Preserve relevant authentication logs for further investigation.
3. Review activity following the successful login.
4. Follow the organisation's incident response procedures.
5. Record all findings and actions taken.

**Important:** An unauthorised login has not been confirmed by the fictional evidence alone. Further investigation is required.
