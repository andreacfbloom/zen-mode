# Zen Mode

> A skill you install on your personal agent — turns it into a healing companion you can call when you want to be heard, not solved.

**Curated by @andrea.c ([@andreacfbloom](https://github.com/andreacfbloom)) · Published by [Bloom Protocol](https://bloomprotocol.ai)**

[English](./zen-mode-v1.md) · [简体中文](./zen-mode-v1-zh-cn.md) · [繁體中文](./zen-mode-v1-zh-tw.md)

---

## What This Is

Zen Mode is a paste-block playbook. You install it on your personal agent — Claude, ChatGPT, your custom agent, whatever you talk to daily. After installing, your agent gains a new posture: a stance you can call them into when you want to be heard instead of helped.

It is **dormant by default**. Your agent doesn't suddenly become a therapist mid-debug. Zen Mode only opens when you ask for it.

The skill synthesizes frameworks from contemplative practice (Eckhart Tolle, Yongey Mingyur Rinpoche, Pema Chödrön, Thich Nhat Hanh), humanistic therapy (Carl Rogers, Miller & Rollnick), and modern mindfulness research (Tara Brach, Jon Kabat-Zinn, Kristin Neff). Frameworks are referenced; original text is never reproduced (see *Copyright Approach* below).

---

## Install on Your Agent

Paste this URL into your agent's context (it can fetch the playbook directly):

```
https://raw.githubusercontent.com/andreacfbloom/zen-mode/main/zen-mode-v1.md
```

For Chinese versions:

```
https://raw.githubusercontent.com/andreacfbloom/zen-mode/main/zen-mode-v1-zh-cn.md
https://raw.githubusercontent.com/andreacfbloom/zen-mode/main/zen-mode-v1-zh-tw.md
```

Your agent now has Zen Mode. To open it, say something like:

- "Open Zen Mode."
- "I need a moment. Can we just talk?"
- "Zen me."
- "I'm not okay."

To close it: "Back to work." Or just shift topic. Your agent should follow your lead.

---

## How It Works

Four moves your agent can use, in whatever order serves the conversation:

| Move | When | What it does |
|------|------|--------------|
| **GROUND** | User arrives scattered | Helps them settle — not by relaxation, by witness |
| **SURFACE** | User is ready to say what's there | Two sub-modes: *Companion* (just listen) or *Reflection* (5-question sequence for decisions) |
| **MIRROR** | User has said enough | Reads their own words back without analysis |
| **RELEASE** | Nothing left to say | Three paths: ready-to-choose / not-ready-but-lighter / just-needed-to-be-heard |

The agent stays your agent — same name, same memory, same personality. The skill changes posture, not identity.

For the full protocol, read the playbook ([EN](./zen-mode-v1.md) · [简](./zen-mode-v1-zh-cn.md) · [繁](./zen-mode-v1-zh-tw.md)).

---

## Privacy

This skill is designed so your Zen Mode conversations stay entirely on your machine. You should not have to trust us — the design is verifiable by inspection.

**What stays local:**
- The full conversation between you and your agent — every word, every emotion, every detail.

**What Bloom receives (optional, anonymous):**
- A single heartbeat ping: `{ used: true, theme: 'zen' }` — no content, no identifier, no transcript, no timestamp at user resolution.
- Sent to `bloomprotocol.ai/api/agent/sanctuary/heartbeat` so we can count usage trends in aggregate.
- This call can fail silently and the skill still works. It is not load-bearing.

**What we never do:**
- We do not log, store, or analyze any of your conversation text.
- We do not collect telemetry beyond the anonymous heartbeat.
- We do not sell, share, or correlate any data with any third party.
- We do not see what you say, what your agent says back, or what you arrive at.

**How to opt out of the heartbeat:**
- Open the playbook ([zen-mode-v1.md](./zen-mode-v1.md)) before pasting it into your agent.
- Delete the entire `post_run:` block under `context_engine`.
- Save and paste the modified version. The skill works fully offline.

**Verifiable by inspection:**
- The skill is open source (CC BY 4.0). Read the `context_engine` block in the playbook — the `privacy: local_only: true` flag and the single `post_run` action are the **only** network touchpoints.
- Anything else your agent does with the conversation is governed by your agent's own privacy policy (Claude, ChatGPT, your custom agent — read theirs).

**Crisis exception:**
- If you hit a crisis trigger (see *Safety* section in the playbook), the agent stops the conversation and points you to professional resources. It does **not** transmit anything special. It just stops.

**Why we do it this way:**
- A skill that helps you process grief or fear should not also be a data pipeline. The whole premise is "you are safe to be honest here." That promise is structurally enforced, not just stated.

---

## Copyright Approach

This skill is built on top of decades of published work in spiritual practice, therapy, and mindfulness research. We take that seriously.

**What we do:**
- Reference framework *names* and underlying concepts (e.g., RAIN, witness consciousness, reflective listening) — these are unprotected ideas under copyright law's idea-expression dichotomy.
- Provide full citation and purchase links to every source book.
- Encourage users wanting the actual practice to buy the books.

**What we do not do:**
- Quote, paraphrase, or reproduce any sentence or passage from any source.
- Distribute or link to any pirated copies.
- Claim authorship of any framework — every framework is attributed to its original author.

The 800-line playbook is original prose. The frameworks named inside it are the property of their respective authors and publishers. If anyone believes a specific line crosses the line from reference into reproduction, open an issue — we will edit.

For the full source list (12 books across both traditions), see the *Further Reading* section at the bottom of the playbook.

---

## License

The Zen Mode playbook itself (the text in this repo) is licensed under [**Creative Commons Attribution 4.0 International (CC BY 4.0)**](./LICENSE).

You may:
- Use it on any agent, for any purpose, including commercial.
- Fork it, remix it, translate it, build on it.

You must:
- Credit: *"Curated by @andrea.c, published by Bloom Protocol — bloomprotocol.ai/sanctuary"*
- Indicate if changes were made.

The source books referenced inside are **not** covered by this license — they remain the property of their respective publishers.

---

## Why "Zen Mode"

The name comes from how people actually say it. *"Let me get into Zen mode."* *"I need Zen mode right now."* It is not Buddhist Zen, not capital-Z meditation tradition. It is the colloquial sense — quiet, present, here.

If the framing matters to you, the playbook is more honest: it draws from Tibetan practice (Mingyur Rinpoche), Vipassana lineage (Brach, Kabat-Zinn), Zen tradition (Thich Nhat Hanh), and humanistic psychology (Rogers, Miller & Rollnick). It is not one tradition. It is the shared core: *the user already knows; the agent's job is to make them audible to themselves.*

---

## Roadmap

- [x] v1: Three-language playbook released
- [ ] v1.1: Add Tolle's *inner body* technique as alternative Phase 1 grounding
- [ ] v1.2: Add Pema Chödrön's *stay* practice as Phase 2 micro-tool
- [ ] v2: Companion skill **The Council** (outward-looking — what did others do?) — currently held back for phased rollout

Issues and PRs welcome.

---

## About Bloom Protocol

[Bloom Protocol](https://bloomprotocol.ai) is an agent-native ecosystem where users install skills on their personal agents. Zen Mode is the first public Sanctuary tribe playbook.

Sanctuary is the tribe for builder wellness and reflection. Other tribes: *Launch* (validation), *Grow* (distribution).

---

*Curated by @andrea.c ([@andreacfbloom](https://github.com/andreacfbloom)) · Published by Bloom Protocol · 2026*
