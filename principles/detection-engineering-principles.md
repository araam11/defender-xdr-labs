\# Detection Engineering Principles



This document defines the principles used to design all detections

and hunting queries in this repository.



The goal is to maximize \*\*signal quality\*\* while minimizing

\*\*operational noise\*\*.



---



\## Principle 1: Behavior Over Events



Single events are rarely meaningful on their own.



Effective detections focus on:

\- Sequences

\- Patterns

\- Correlation across signals



---



\## Principle 2: Correlation Beats Thresholds



Threshold-only detections are brittle.



Where possible:

\- Combine identity, endpoint, and network signals

\- Use time-bound correlation

\- Avoid static alerting thresholds



---



\## Principle 3: Explainability Is Required



Every detection must answer:

\- Why this behavior is suspicious

\- What benign scenarios may exist

\- How analysts should investigate



Detections that cannot be explained

cannot be trusted.



---



\## Principle 4: Hunting ≠ Alerting



Not every good hunting query

should become an alert.



Hunting queries:

\- Explore hypotheses

\- Support investigation

\- Inform tuning decisions



Alerting requires environment-specific validation.



---



\## Principle 5: Tune, Don’t Rewrite



Well-designed detections should be:

\- Tunable via thresholds

\- Tunable via exclusions

\- Tunable via time windows



Logic should remain stable.



---



\## Principle 6: Risk Escalation Over Noise



Multiple weak signals

are often more meaningful than

a single strong one.



Detection engineering should support

risk-based prioritization.



---



\## Summary



Good detection engineering is not about

finding \*everything\*.



It is about finding the \*\*right things\*\*

at the \*\*right time\*\*

for the \*\*right response\*\*.



