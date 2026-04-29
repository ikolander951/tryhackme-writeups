# AI/ML Security Threats

**Path:** AI Security
**Difficulty:** Easy
**Date completed:** 2026-04 (revisit and confirm)
**Room link:** https://tryhackme.com/room/aimlsecuritythreats

---

## What this room teaches

An introduction to the security landscape around AI and machine learning systems. The room walks through the building blocks of AI (models, training data, inference), why LLMs in particular create new attack surfaces, the most common AI-specific threats (prompt injection, data poisoning, model theft, sensitive data disclosure), and what "defensive AI" looks like at a high level.

## Key takeaways

The 7 tasks roughly map to:

1. **Introduction** — why AI security is its own discipline.
2. **The Building Blocks of AI** — training data → model → inference. Each layer is a potential attack surface.
3. **LLMs** — large language models are probabilistic, so the same input can produce different outputs. They can't reliably tell trusted system instructions from untrusted user input — both arrive as natural language.
4. **AI Security Threats** — prompt injection (direct and indirect), data poisoning, sensitive information disclosure, insecure output handling, excessive agency in agentic systems.
5. **Defensive AI** — input validation, output filtering, rate limiting, output isolation, monitoring for anomalous prompts.
6. **Practical** — a live exercise to see one of these threats in action.
7. **Conclusion** — pointers to the rest of the AI Security path.

## What was new to me

- The difference between **direct** prompt injection (the user types something to override the system prompt) and **indirect** prompt injection (malicious instructions are embedded in a webpage, document, or email the model later reads). Indirect injection is the scarier one because the user isn't aware their AI agent has been hijacked by content it processed.
- **Excessive agency** as a vulnerability class — when an LLM is given tools (read email, send email, browse the web) and gets prompt-injected, the consequences leave the screen and become real-world actions. This is why agentic AI systems need stricter guardrails than chat assistants.

## How a SOC analyst would use this

- Detection logic for AI-driven phishing has to shift from "does this email have grammar mistakes?" to behavioral cues — sender history, request patterns, links to look-alike domains. AI now writes flawless phishing in any language.
- A SOC investigating a misbehaving internal AI assistant should look at the inputs the model received (including web pages and documents it ingested) — the compromise might not be in the chat log; it might be in a poisoned source the model trusted.
- MITRE **ATLAS** is the AI-specific equivalent of ATT&CK — worth knowing as the framework you'll cite when filing AI-related incidents.

## Commands / concepts to remember

| Concept | What it means |
|---------|---------------|
| Prompt injection (direct) | User input overrides system instructions |
| Prompt injection (indirect) | Hostile instructions embedded in content the model retrieves |
| Data poisoning | Tampering with training data to bias or backdoor a model |
| Excessive agency | LLM has more tool access than its risk profile justifies |
| OWASP LLM Top 10 | Industry list of LLM-specific vulnerability classes |
| MITRE ATLAS | Threat-modeling framework for AI systems |

## Resources

- Room: https://tryhackme.com/room/aimlsecuritythreats
- OWASP LLM Top 10: https://owasp.org/www-project-top-10-for-large-language-model-applications/
- MITRE ATLAS: https://atlas.mitre.org
