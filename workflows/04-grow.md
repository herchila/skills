---
name: grow
description: Systematically acquire users and improve retention through experiments and content.
---

# Workflow 4: Grow

**Use when:** The product is live, the core loop works, and it's time to deliberately grow — more users, better retention, or higher revenue.

**Goal:** Find the acquisition channels and retention levers that work, double down on them, and build compounding growth systems.

**Prerequisite:** Don't run this workflow until you have at least 10–20 users who actively use the product. Growth tactics on a broken product accelerate churn, not growth.

---

## Skills Involved

```
/analytics-reporter → /growth-hacker → /content-creator + social skills → /experiment-tracker → /feedback-synthesizer
```

---

## Phase 1: Diagnose Before Scaling

**Don't invest in acquisition until you understand retention.**

### Step 1 — Find the leak (`/analytics-reporter`)

**Invoke:** `/analytics-reporter`

**Analyze the full funnel:**
```
Awareness → Acquisition → Activation → Retention → Revenue → Referral
```

For each stage: what's the conversion rate? Where's the biggest drop?

**Output:** Funnel map with the single biggest drop-off identified

---

### Step 2 — Growth audit (`/growth-hacker`)

**Invoke:** `/growth-hacker`

**Give it:**
- Funnel analysis from Step 1
- Current channels (organic, word of mouth, anything)
- Any previous experiment results

**Output:**
- Diagnosis: where's the constraint? (activation, retention, or acquisition)
- Top 3 experiment hypotheses
- Channel recommendations based on where your users already are

**Rule:** If retention is the problem, fix it before investing in acquisition. Acquiring users into a leaky product is burning money.

---

## Phase 2: Run Experiments

### Step 3 — Design experiments (`/experiment-tracker`)

**Invoke:** `/experiment-tracker`

For each hypothesis from Step 2:

**Output per experiment:**
- Hypothesis with specific metric
- Control vs. treatment
- Success threshold (defined before running)
- Duration and minimum sample

**Run 1–2 experiments at a time** — more creates confounds and dilutes focus.

---

### Step 4 — Build what the experiment needs

Experiments often need something built:

| Experiment Type | Skills Needed |
|----------------|---------------|
| Landing page variant | `/rapid-prototyper` + `/content-creator` |
| Onboarding flow change | `/frontend-developer` + `/ui-designer` |
| Email sequence | `/content-creator` |
| In-app feature | `/frontend-developer` |
| Referral mechanism | `/backend-architect` + `/frontend-developer` |

---

### Step 5 — Analyze results (`/feedback-synthesizer` + `/experiment-tracker`)

**After experiment completes:**

1. Record results in `/experiment-tracker`
2. If qualitative feedback was collected → `/feedback-synthesizer`
3. Declare: Win / Loss / Inconclusive
4. Extract the learning: what does this tell us about our users?

**Repeat Steps 3–5** until a winning channel or lever is identified.

---

## Phase 3: Build Compounding Channels

Once experiments identify what works, build durable systems.

### Content (compounding over time)

**Invoke:** `/content-creator`

Build content that drives organic discovery:
- Blog posts targeting search intent your users have
- Case studies with specific outcomes
- Documentation that ranks for problems you solve

**Platform-specific content:**

| Channel | Skill |
|---------|-------|
| Twitter/X threads | `/twitter-engager` |
| TikTok / Reels | `/tiktok-strategist` |
| Instagram | `/instagram-curator` |
| Reddit | `/reddit-community-builder` |
| App Store | `/app-store-optimizer` |

---

### Referral / Viral loops

**Invoke:** `/growth-hacker`

Design a referral mechanism that:
- Triggers at the moment of highest user satisfaction
- Rewards both sides
- Makes sharing feel natural, not transactional

---

## Cadence

| Frequency | Activity |
|-----------|----------|
| Weekly | Review experiment metrics, update `/experiment-tracker` |
| Bi-weekly | New experiment starts |
| Monthly | Channel performance review with `/analytics-reporter` |
| Quarterly | Growth strategy review — double down or pivot channels |

---

## Growth Stage Checklist

**Before investing in acquisition:**
- [ ] Activation rate > 30% (users experience value in first session)
- [ ] D7 retention > 20% (users come back after a week)
- [ ] At least 5 users who use it without being prompted
- [ ] You understand why those 5 use it

**Early-stage growth focus (0→100 users):**
- Manual, unscalable acquisition (personal outreach, community participation)
- Fix every activation friction point
- Talk to every churned user

**Mid-stage growth focus (100→1k users):**
- 1–2 scalable channels identified and working
- Referral/word-of-mouth loop designed
- Content strategy started

---

## Decision Points

| Situation | Action |
|-----------|--------|
| Retention below 15% D7 | Stop acquisition investment. Fix retention first. |
| One channel working clearly | Double down. Don't diversify yet. |
| No experiment is winning | Question the channel, not the execution. Try a different channel. |
| Strong retention, weak acquisition | It's a distribution problem. Run more acquisition experiments. |
| Strong acquisition, high churn | Acquisition is attracting wrong users. Fix targeting or product. |

---

## Notes

- Growth is a system, not a campaign. The goal is channels that compound.
- Every failed experiment is a learning. Log it in `/experiment-tracker` so you don't repeat it.
- The fastest growth lever at early stage is almost always retained users telling friends. Optimize for that first.
