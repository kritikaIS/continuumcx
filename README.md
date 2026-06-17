# ContinuumCX

**Stop making customers repeat themselves — and prove it with a score.**

ContinuumCX is an AI layer that follows a customer's issue across every channel they use — chat, email, voice — merges it into one living context, and scores how seamless that journey actually was, in real time, with the AI explaining *why* the score moved.

Built for **TeXpedition VIT** · Theme 02: *How can we use AI to deliver seamless customer experiences across channels while defining clear measures of success?*

---

## The problem

A customer explains their issue on chat. No reply. They explain it again on email. They get transferred. They explain it a third time on a call — now angry. Every channel treats the conversation as brand new, and nobody has a number that proves whether that's actually been fixed.

## How it works

**1. Detect** — the moment a customer switches from chat to email to phone, the system recognizes it's the same issue, not a fresh conversation.

**2. Merge** — an LLM folds everything already said into one running summary, instantly available to whoever picks up next, bot or human. No "can you repeat that for me?"

**3. Score & Rescue** — every touch updates a live **Seamlessness Score** built from real friction signals: repeat-asks, channel switches, response latency, sentiment trend. When the score crosses a friction threshold, the system auto-escalates with the full merged thread attached, so the next agent resolves in one touch instead of starting from zero.

## Why this is different

Most "AI customer support" tools optimize for response speed inside a single channel. ContinuumCX optimizes for **continuity across channels during an already-active complaint**, and turns "seamless experience" from a slide claim into a transparent, live, explainable metric.

## Metrics nobody else is measuring

| Metric | What it tells you |
|---|---|
| **Seamlessness Score** | Live 0–100 read on how friction-free a customer's cross-channel journey actually was |
| **Repeat-Ask Count** | How many times a customer had to re-explain themselves across channels |
| **Continuity Recovery Rate** | How much the score rebounds after an auto-rescue — proof the intervention worked, not just logged |
| **Time-to-Merged-Context** | How fast a new channel touch gets full prior context, versus starting cold |

## Proof, not a promise

Demo scenario, same customer, same 3 touches:

| | Without ContinuumCX | With ContinuumCX |
|---|---|---|
| Repeat-asks | 2 | 0 |
| Total handle time | 38 min | 19 min |
| Final Seamlessness Score | 31 | 88 |

## Try the prototype

The prototype is a single, dependency-free HTML file — no build step, no server.

```bash
# clone the repo, then just open the file in any browser
open continuumcx-prototype.html
```

Walk through the 5-step scenario using the **Next →** / **← Back** controls:
1. Customer opens on chat
2. No reply → switches to email, repeats the issue
3. Switches to a call, repeats again → score crosses threshold → auto-rescue fires
4. Agent resolves in one touch using the merged context
5. Before/after impact summary

## Tech stack

**Prototype:** HTML / CSS / vanilla JS — interactive walkthrough of the channel rail, memory thread, and live scoring engine.

**Production architecture (proposed):**
- Claude API — context merging across channels and natural-language score explanations
- Vector store — persistent cross-channel memory per customer
- Lightweight scoring model — combines conversational + behavioral friction signals
- React dashboard — live score monitoring and rescue alerts for CX teams

## Repo structure

```
continuumcx/
├── continuumcx-prototype.html   # interactive prototype, open directly in browser
└── README.md
```

## Team

[Add your team name / members here]

## License

[Add license, e.g. MIT — or remove this section if not needed for the hackathon]
