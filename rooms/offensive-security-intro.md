# Offensive Security Intro

**Path:** Pre-Security / Intro to Cyber Security
**Difficulty:** Easy
**Date completed:** 2026-04 (revisit and confirm)
**Room link:** https://tryhackme.com/room/offensivesecurityintro

---

## What this room teaches

A friendly first taste of what "hacking" actually looks like. You hack a fake website in a sandboxed lab, learn the difference between offensive and defensive security, and get exposed to the basic offensive toolkit (browser dev tools, scripting, common web flaws). It's designed to make the rest of the path feel less intimidating.

## Key takeaways

- **Offensive security** = thinking like an attacker. Penetration testers, red teams, and bug bounty hunters live here. Their job is to find weaknesses before real attackers do.
- The room walks you through navigating a vulnerable web app and finding hidden content — the same instinct that web pentesters use every day.
- Offensive work isn't lawless — it's contractually scoped. Without written authorization, the same actions are illegal.

## What was new to me

- Most "hacking" at the entry level is patient enumeration, not flashy exploits. You browse the site, view source, poke at URLs, look for things developers thought they hid. That's it for the first 80% of a real engagement.
- Browser developer tools are a legitimate offensive recon tool. View Source, Network tab, and JavaScript debugger surface paths and parameters that aren't linked from the homepage.

## How a SOC analyst would use this

- Defenders need to understand the attacker's methodology to detect it. If you don't know that recon is the first stage of an attack, you'll miss the slow, low-noise enumeration that precedes the actual breach.
- The **cyber kill chain** (recon → weaponization → delivery → exploitation → installation → C2 → actions on objectives) starts with what this room demonstrates. SOC alerts at the recon stage are the cheapest to investigate and the most valuable to catch.
- Knowing what a web exploit looks like from the attacker's side makes log analysis more intuitive — you stop seeing requests as opaque strings and start reading them as someone's intent.

## Commands / concepts to remember

| Concept | What it means |
|---------|---------------|
| Offensive security | Authorized adversary simulation — pentest, red team, bug bounty |
| Reconnaissance | Information gathering before attacking; passive (no contact) or active (probing) |
| Browser dev tools | View Source, Network tab, Console — first-line offensive recon |
| Scope | The legal boundary of what an offensive engagement is allowed to test |

## Resources

- Room: https://tryhackme.com/room/offensivesecurityintro
- Related: Defensive Security Intro (the blue-team counterpart, also completed)
