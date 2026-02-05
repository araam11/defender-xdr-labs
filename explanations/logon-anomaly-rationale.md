\# Detection Rationale: Suspicious Logon Burst



\## Threat Hypothesis

An attacker attempting credential compromise may generate

multiple failed authentication attempts before eventually

succeeding.



This behavior is commonly observed during:

\- Password spraying

\- Brute-force attempts against a single account

\- Reuse of previously exposed credentials



---



\## Why this detection works



This detection looks for:

\- A high volume of failed logons

\- Followed by at least one successful logon

\- Within a short, bounded time window



The combination is important:

\- Failed logons alone are noisy

\- Successful logons alone are common

\- The sequence of \*\*failures → success\*\* is suspicious



---



\## Expected false positives



Possible benign scenarios include:

\- Users repeatedly mistyping passwords

\- Cached credential issues during password changes

\- Legacy applications retrying authentication



These can be mitigated by:

\- Excluding known service accounts

\- Adjusting the failure threshold

\- Expanding or shrinking the time window



---



\## Why this is a hunting query



This query is intended for:

\- Threat hunting

\- Analyst investigation

\- Detection tuning exercises



It should not be converted into an alert

without environment-specific tuning.



