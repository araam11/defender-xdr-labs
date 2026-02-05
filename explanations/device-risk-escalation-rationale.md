\# Detection Rationale: Device Risk Escalation



\## Threat Hypothesis

Compromised devices often exhibit \*\*multiple weak signals\*\*

before generating a high-confidence alert.



Individually, these signals may be benign.

Collectively, they indicate elevated risk.



---



\## Why this detection works



This detection escalates device risk when:

\- Suspicious process execution is observed

\- Authentication failures increase

\- Unusual remote connectivity occurs



No single signal is sufficient on its own.

The combination is meaningful.



---



\## Signals used



\### Endpoint

\- Suspicious or abuse-prone binaries

\- Encoded PowerShell usage



\### Identity

\- Repeated authentication failures



\### Network

\- Remote management protocol usage



---



\## Expected false positives



Potential benign causes include:

\- Administrative scripting

\- Automated management tools

\- Remote troubleshooting sessions



Mitigation strategies:

\- Exclude known admin devices

\- Tune thresholds per environment

\- Limit remote port scope



---



\## Why this is a hunting query



This query supports:

\- Risk-based triage

\- Threat hunting

\- SOC prioritization



It should not be converted into an alert

without environment-specific tuning.



---



\## Analyst guidance



When this detection triggers:

\- Review device timeline

\- Check user behavior history

\- Correlate with existing alerts

\- Consider tagging device for triage



