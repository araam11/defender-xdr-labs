\# Defender XDR Labs



This repository contains \*\*sanitized detection and hunting examples\*\*

for Microsoft Defender XDR.



The focus is on \*\*signal quality, reasoning, and attacker behavior\*\* —

not tenant-specific queries or copy-paste detections.



⚠️ No Microsoft-internal content, customer data, or production exports

are included.



---



\## 🎯 Scope



This repository focuses on:

\- Threat hunting with Defender telemetry

\- Correlating endpoint, identity, and network signals

\- Reducing false positives through context

\- Mapping detections to attacker techniques



This repository intentionally avoids:

\- Noisy one-off detections

\- Environment-specific thresholds

\- Tenant identifiers or screenshots



---



\## 📐 Repository Structure



\- \*\*kql/\*\*  

&nbsp; Example hunting queries written for clarity and reasoning



\- \*\*explanations/\*\*  

&nbsp; Why the detection works and what behavior it captures



\- \*\*principles/\*\*  

&nbsp; Detection engineering philosophy and guardrails



---



\## 🧭 Philosophy



> Good detections explain \*behavior\*, not just events.



Every query in this repository:

\- Has a clear threat hypothesis

\- Explains expected false positives

\- Can be tuned without rewriting logic



