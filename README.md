# ⚔️ Battle-Tested Agent

**16 production-hardened patterns for OpenClaw agents. Every one earned from failure.**

This repo contains the ClawHub-ready skill package for `battle-tested-agent` — a practical reliability layer for agents that operate in the real world.

It focuses on the patterns that stop agents from doing stupid, expensive, or theatrical things:
- write-ahead logging
- anti-hallucination discipline
- ambiguity gates
- compaction survival
- QA gates
- multi-agent handoffs
- recurrence tracking
- self-improvement from real failures

## Why this exists

Most agent systems look smart right up until:
- compaction wipes context
- a cron silently fails
- an agent guesses instead of verifying
- a handoff drops key details
- the system grows governance theater instead of reliability

Battle-Tested Agent is meant to harden that layer.

## What you get

- `SKILL.md` — the full skill definition
- `scripts/audit.sh` — a fast audit script that scores a workspace against the patterns
- `assets/AGENTS-additions.md` — AGENTS.md additions
- `assets/QA-gates.md` — QA guardrails
- `.learnings/` starter templates for learnings, errors, and feature requests

## Quick start

Install from ClawHub:

```bash
clawhub install battle-tested-agent
```

Run the audit:

```bash
bash scripts/audit.sh ~/workspace
```

Example output:

```text
⚔️ Battle-Tested Audit — Score: 10/16

✅ WAL Protocol              ✅ Anti-Hallucination
✅ Ambiguity Gate            ✅ Simple Path First
✅ Unblock Before Shelve     ✅ Agent Verification
❌ Working Buffer            ✅ QA Gates
✅ Decision Logs             ❌ Verify Implementation
✅ Delegation Rules          ❌ Handoff Template
❌ Orchestrator Rule         ✅ Compaction Hardening
❌ Recurrence Tracking       ✅ Self-Improvement
```

## Starting fresh

Copy the templates you want into your workspace:

```bash
cp assets/AGENTS-additions.md ~/workspace/
cp assets/QA-gates.md ~/workspace/QA.md
mkdir -p ~/workspace/.learnings
cp assets/learnings-template.md ~/workspace/.learnings/LEARNINGS.md
cp assets/errors-template.md ~/workspace/.learnings/ERRORS.md
cp assets/features-template.md ~/workspace/.learnings/FEATURE_REQUESTS.md
```

## Pattern tiers

| Tier | Patterns | Best for |
|------|----------|----------|
| 🟢 Starter | 5 | Single agents, first-week setups |
| 🟡 Intermediate | 5 | Daily drivers, heartbeats, reports |
| 🔴 Advanced | 6 | Multi-agent systems, delegation, orchestration |

## Who this is for

This is for people running OpenClaw agents in production-like conditions — not toy demos.

If you care about:
- reliability over vibes
- evidence over narration
- operational clarity over prompt poetry
- fewer repeated failures

this skill is built for you.

## Repository

- GitHub: https://github.com/zurbrick/battle-tested-agent
- ClawHub package: `battle-tested-agent`

## License

MIT
