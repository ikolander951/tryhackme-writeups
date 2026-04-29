# Defensive Security Intro

**Path:** Pre-Security / Intro to Cyber Security
**Difficulty:** Info / Easy
**Date completed:** 2026-04 (revisit and confirm)
**Room link:** https://tryhackme.com/room/defensivesecurityintro

---

## What this room teaches

The blue-team counterpart to Offensive Security Intro. You learn what defensive security is (preventing intrusions and detecting them when prevention fails), the major areas a defensive team owns, and the roles inside a SOC. The practical task drops you into a simulated SIEM defending **FakeBank** against an active attack.

## Key takeaways

- The four core areas of defensive security: **monitoring & detection, incident response, threat intelligence, investigation & analysis**.
- A SOC is staffed with distinct roles. The room introduces three:
  - **Bob, SOC Analyst** — front-line monitoring and triage
  - **Aliyah, Incident Responder** — investigates active incidents and shares lessons
  - **Zoe, Security Engineer** — builds and maintains the detection tooling
- A **SIEM** (Security Information and Event Management) is the central console where alerts from across the network land. Splunk is the most common one in industry.

## What was new to me

- The triage workflow for a Tier 1 SOC analyst is more constrained than I expected: see alert → investigate → block source IP → apply rate limit → update WAF rule → close ticket with the flag. Most of the job is repeatable playbooks, not improvisation.
- The clear separation between SOC Analyst (monitors) and Incident Responder (responds) is real — and at large orgs they're different teams. At smaller orgs one person wears both hats. Worth knowing for interviews: ask which model the role you're applying to follows.

## How a SOC analyst would use this

- The FakeBank lab is a tiny version of an actual Tier 1 shift. Alert pops in the SIEM, you open it, you check the source IP, you decide whether to block, escalate, or dismiss.
- The **block source IP → rate limit → WAF rule** progression in the lab maps to a real layered-defense response. You don't just slam the door; you also slow it down (rate limiting) and prevent the same pattern next time (WAF).
- Knowing the SOC roles by name helps when reading job postings. "Tier 1 SOC Analyst" maps to Bob; "DFIR" or "Incident Responder" maps to Aliyah; "Detection Engineer" maps to Zoe.

## Commands / concepts to remember

| Concept | What it means |
|---------|---------------|
| SOC | Security Operations Center — the team and room defending the network |
| SIEM | Central log/alert platform (Splunk, Sentinel, QRadar, Elastic) |
| Tier 1 vs Tier 2 | Tier 1 triages and escalates; Tier 2 takes the harder investigations |
| WAF | Web Application Firewall — filters HTTP traffic based on rules |
| Incident Response | Containment → eradication → recovery → lessons learned |

## Resources

- Room: https://tryhackme.com/room/defensivesecurityintro
- Next steps: Junior Security Analyst Intro (SOC Level 1)
