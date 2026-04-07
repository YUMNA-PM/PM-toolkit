# Experiment 001 — KYC Selfie Capture Optimisation
**Product:** Malaysia Super App  
**Industry:** Travel Tech / Super App  
**Type:** A/B Test  
**Status:** Case 6 — Almost Result (More Data Needed)  
**dmin:** 5 percentage points  
**Baseline:** 52% selfie capture completion rate  

---

## Background

Malaysia Super App is a one-stop travel and lifestyle platform. To activate the digital wallet — the core revenue-generating feature — users must complete KYC verification including a selfie capture step.

Session recordings revealed users were reaching the selfie capture screen and abandoning mid-flow after repeated failed capture attempts and unclear error messages. This was confirmed as the single biggest drop-off point in the entire KYC funnel.

**Why this matters:** Every user who abandons KYC never activates their wallet — meaning they cannot book, spend, or transact. Fixing this one step directly increases revenue-generating users.

---

## Hypothesis

> "We believe that improving the selfie capture UI with real-time guidance — including lighting indicators, face positioning overlays, prominent step completion feedback, and plain English error messages — will increase selfie capture completion rate by at least 5 percentage points, because session recordings show users abandoning after repeated failed attempts caused by poor visual feedback and unclear instructions, not lack of intent."

**Evidence backing this hypothesis:**
- Session recordings confirm users reach the selfie screen and attempt capture
- Drop-off happens MID-flow — intent exists, execution is failing
- Current UI has 4 steps that turn green on completion but indicator is too small to notice
- Error messages are generic — users don't know what went wrong

---

## Experiment Setup

| Parameter | Value |
|-----------|-------|
| Primary metric | Selfie capture completion rate |
| Baseline | 52% |
| dmin | 5pp absolute |
| Alpha | 0.05 |
| Power | 0.80 |
| Sample size | 4,800 per group (9,600 total) |
| Split | 50% control / 50% treatment |
| Test type | Two-tailed |

**Control:** Current selfie capture screen — 4 small steps, generic error messages, minimal guidance

**Treatment:** Improved UI — large step indicators, real-time lighting + positioning guidance, plain English error messages

**Secondary metrics:**
- Per-step completion rate (which of 4 steps causes most drop-off)
- Number of capture attempts per user
- Time to complete selfie capture
- Overall KYC completion rate

---

## Results

| | Control | Treatment | Difference |
|---|---------|-----------|-----------|
| Total users | 4,800 | 4,800 | — |
| Completions | 2,496 | 2,726 | +230 |
| Completion rate | 52.0% | 56.8% | +4.8pp |

---

## Confidence Interval Calculation

| Step | Calculation | Result |
|------|-------------|--------|
| Pooled completion rate | (2,496 + 2,726) / 9,600 | 0.5440 |
| Pooled SE | √(0.5440 × 0.4560 × (1/4800 + 1/4800)) | 0.01018 |
| d hat | 56.8% - 52.0% | 4.8pp |
| Margin of error | 1.96 × 0.01018 | 1.995% |
| Upper bound | 4.8% + 1.995% | 6.795% |
| Lower bound | 4.8% - 1.995% | 2.805% |
| **Confidence interval** | | **[2.805%, 6.795%]** |

---

## Launch Decision

| Check | Question | Answer | Result |
|-------|---------|--------|--------|
| Statistical | Does CI cross zero? | No — both bounds positive | ✅ Significant |
| Practical | Is lower bound above dmin (5%)? | 2.805% < 5% | ❌ Not enough |

**Verdict: Case 6 — The Almost Result. Do not ship yet. Get more data.**

The result is statistically significant — the effect is real and not due to chance. However the lower bound of the confidence interval (2.805pp) falls below the minimum detectable effect of 5pp. In the worst realistic case, the improvement does not justify the engineering cost.

> "It's probably good enough. But probably isn't good enough to ship."

---

## What's Next

1. Run experiment again with 8,000+ users per group to tighten the confidence interval
2. Instrument per-step drop-off to identify which of the 4 steps has highest abandonment
3. Drive more users through KYC via push notifications to users who started but didn't complete
4. If lower bound clears 5pp at larger sample → Case 1 → ship it

---

## Key Learning

Most PMs would see +4.8pp and ship immediately.

A good CRO practitioner checks the confidence interval first — because the lower bound tells you whether you can trust the result at your required threshold.

**Statistical significance** tells you the effect is real.  
**Practical significance** tells you the effect is worth it.  
You need both before you ship.
