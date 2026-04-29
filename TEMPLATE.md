# [Room Name]

**Path:** [Path name, e.g. Cyber Security 101]
**Difficulty:** [Easy / Medium / Hard]
**Date completed:** YYYY-MM-DD
**Room link:** https://tryhackme.com/room/[room-slug]

---

## What this room teaches

_1-2 sentences in your own words. What is the topic? What skill does it build?_

Example: "Linux Fundamentals 1 introduces the Linux command line: navigating the filesystem with `pwd`, `ls`, `cd`, and reading files with `cat`. Foundational for any analyst who'll work in a SOC, since most logs and tools live on Linux."

---

## Key tasks walkthrough

### Task 1: [Title]

_What did the task ask? What command/answer did you provide? Why?_

```bash
# Commands you actually ran
pwd
ls -la
```

### Task 2: [Title]

_Repeat for each major task. Skip trivial ones._

---

## What was new to me

_The 1-2 things you didn't know going in. Be specific — "permissions" is too vague; "the difference between `chmod 755` and `chmod 644` and when to use each" is a writeup-worthy nugget._

- Concept 1: ...
- Concept 2: ...

---

## How a SOC analyst would use this

_The most important section. Connect this room to real-world Tier 1 SOC work. Examples:_

- "When investigating a Linux host alert, I'd `cd /var/log` and `grep` through `auth.log` for failed login attempts — exactly the navigation pattern this room drills."
- "Understanding file permissions matters because malware often modifies `/etc/passwd` or drops payloads in world-writable directories like `/tmp`. Detecting that requires knowing what 'normal' permissions look like."

---

## Commands / tools to remember

| Command | What it does |
|---------|--------------|
| `pwd` | Print working directory |
| `grep -r 'pattern' .` | Recursive text search |

---

## Resources

- Room: https://tryhackme.com/room/[room-slug]
- Related: [Any related rooms, MITRE techniques, blog posts]
