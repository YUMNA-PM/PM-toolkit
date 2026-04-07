# PM Toolkit

A public collection of frameworks, agents, and case studies built while developing skills in AI-augmented product management, CRO, and experimentation.

Everything here is practical — built from real product problems, documented clearly, and designed to be reused.

---

## Who this is for

PMs and product consultants who want to:
- Run proper A/B tests and make confident launch decisions
- Use AI agents to accelerate discovery, strategy, and execution
- See real worked examples, not just theory

---

## What's inside

### CRO & Experimentation

Frameworks and case studies for running rigorous experiments.

| File | What it covers |
|------|---------------|
| `cro/experiments/exp-001-kyc-selfie-capture.md` | Full A/B test on KYC selfie capture drop-off in a Malaysia super app — hypothesis, setup, results, CI calculation, Case 6 verdict |
| `cro/reference/ab-testing-complete-guide.md` | The complete A/B testing flow — before, during, after — with formulas and KYC worked examples throughout |
| `cro/reference/6-launch-cases.md` | Every possible experiment outcome with plain English names, worked examples, and decision rules |

---

### Discovery Agents

Reusable AI prompt templates for synthesising user research in minutes.

| File | What it covers |
|------|---------------|
| `discovery/base-discovery-agent.md` | Core synthesis agent — works for any industry. Produces themes, JTBD, HMW statements, hypothesis backlog |
| `discovery/travel-lens.md` | Industry context layer for travel tech clients |
| `discovery/retail-lens.md` | Industry context layer for retail clients |
| `discovery/ecommerce-lens.md` | Industry context layer for ecommerce clients |

**How to use:**
1. Copy `base-discovery-agent.md`
2. Copy the relevant industry lens below it
3. Paste your raw interview notes at the bottom
4. Send to Claude — get full synthesis in minutes

---

### Prototypes

Clickable prototypes built from real product briefs. Each one was built in under 60 minutes.

| Prototype | Product | Built in | Live Link |
|-----------|---------|----------|-----------|
| Revoo — Electric Scooter App | Karachi, Pakistan | 60 min | [View prototype](https://yumna-pm.github.io/PM-toolkit/prototypes/revoo-scooter-app/index.html) |

---

### SQL Query Library

Reusable product analytics queries. Focus on metrics PMs actually use — no academic SQL.

| Query | What it does |
|-------|-------------|
| Coming soon | — |

---

## Case Studies

Full end-to-end product work documented publicly. Each case study covers discovery, strategy, prototype, execution, and experimentation.

| # | Product | Industry | Focus |
|---|---------|----------|-------|
| 001 | Malaysia Super App | Travel Tech | KYC funnel CRO — selfie capture optimisation |
| 002 | Coming soon | — | — |

---

## The A/B Testing Framework

Every experiment I run follows this flow:

```
BEFORE
1. Identify problem (backed by data)
2. Write hypothesis + set dmin
3. Calculate baseline metric
4. Check baseline stability
5. Calculate sample size needed

RUN
1. Split 50/50 — wait for full sample
2. Never peek or stop early

AFTER
1. Calculate completion rate per group
2. Calculate pooled rate
3. Calculate pooled SE
4. Calculate d hat
5. Calculate margin of error
6. Calculate confidence interval
7. Check statistical significance (lower bound > 0?)
8. Check practical significance (lower bound > dmin?)
9. Match to one of the 6 launch cases
```

**The 6 Launch Cases:**
- Case 1 — Dream Result → Ship it
- Case 2 — Boring Result → Don't ship
- Case 3 — Frustrating Result → Don't ship
- Case 4 — Scary Result → Get more data
- Case 5 — Tempting Result → Get more data
- Case 6 — Almost Result → Get more data

Full details with worked examples in `cro/reference/6-launch-cases.md`

---

## Tools I use

| Tool | What for |
|------|---------|
| Claude (Anthropic) | Discovery synthesis, strategy docs, prototyping, experiment design |
| Notion | Portfolio and case study documentation |
| SQLiteOnline | SQL practice and product analytics queries |
| GitHub | Agent templates, query library, and worked examples |

---

## Work in progress

This repo is actively being built. New case studies, agents, and SQL queries are added weekly.

Current focus:
- [ ] Travel tech CRO case study
- [ ] SQL product analytics query library
- [ ] Prototype #1 — vibe coding challenge
- [ ] Experiment #2 — new product, new industry

---

## Connect

Open to consulting work in CRO, experimentation, and AI-assisted product management.

Linkedin : https://www.linkedin.com/in/yumna-m-92a275157/
Notion Portoflio : https://www.notion.so/Hi-I-m-Yumna-I-m-an-Associate-Product-manager-2b5470cc0fb9805d9150d3386990a811

---

*Built in public. Everything documented as it's learned.*
