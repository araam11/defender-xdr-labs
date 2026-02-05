\# Detection Rationale: Lateral Movement Correlation



\## Threat Hypothesis

After initial access, attackers often move laterally to expand access,

escalate privileges, or reach high-value assets.



This frequently involves:

\- Remote authentication

\- Followed by administrative execution methods



---



\## Why this detection works



This detection correlates:

1\. Remote or network-based logons

2\. Followed shortly by execution of known lateral movement tools



The correlation is key:

\- Remote logons alone are common

\- Process execution alone may be benign

\- The \*\*sequence\*\* is suspicious



---



\## Signals used



\### Identity

\- RemoteInteractive and Network logons

\- Source IP and account context



\### Endpoint

\- Process creation events

\- Known lateral movement tooling indicators



---



\## Expected false positives



Possible benign activity includes:

\- IT administrators performing maintenance

\- Automated management tools

\- Patch deployment systems



Mitigations include:

\- Excluding known admin accounts

\- Excluding management subnets

\- Narrowing command-line indicators



---



\## Why this is a hunting query



This query is designed for:

\- Threat hunting

\- Purple team exercises

\- Detection engineering



It should be tuned carefully before alerting.



---



\## Analyst guidance



When investigating hits:

\- Validate account role

\- Check historical device access

\- Review parent processes

\- Correlate with alert timelines



