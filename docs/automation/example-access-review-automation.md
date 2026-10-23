# Project 01 (Example): Automating Quarterly Access Reviews with Okta Access Certifications

_This is a filled-out example, included so you can see what "recruiter-ready" actually looks like before you write your own. Delete this file (or move it to a `/examples` folder) once you've built your first real one — don't ship someone else's project as your own._

## The Compliance Gap
Quarterly user access reviews were done manually — pulling access lists, emailing managers, chasing sign-offs in spreadsheets. No consistent evidence trail, and every cycle ate days that could have gone into actual risk work.

## The Scope & Assumptions
All active Okta-managed applications and their assigned users. Assumes Okta is the identity source of truth for in-scope systems — access managed outside Okta (break-glass accounts, local admin) is out of scope and handled through a separate process.

## The Engineering Solution
Built recurring access certification campaigns in Okta Access Certifications, routed to the correct resource owners automatically, with reviewers required to explicitly approve or revoke each access grant instead of a blanket sign-off. Replaced the manual spreadsheet cycle entirely.

## Auditor-Ready Evidence
```
Campaign: Q_Access_Review
Status: Completed
Reviewers: 12
Access grants reviewed: 340
Revoked: 18
Completion time: 15 seconds (system-generated certification report,
vs. ~3 weeks for the prior manual process)
```
_(Replace with your own exported certification report or screenshot when you build your real version.)_

## The Security Impact
Reduced access review turnaround from roughly 3 weeks to same-day, with a clean, timestamped evidence trail an auditor can pull directly instead of reconstructing from email threads. The time recovered went straight into risk management work — this project is what started the shift from GRC analyst to GRC engineer.
