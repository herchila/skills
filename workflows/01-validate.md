---
name: validate
description: Go from raw idea to evidence-based decision in days, not months.
---

# Workflow 1: Validate the Idea

**Use when:** You have an idea and want to know if it's worth building before writing a single line of product code.

**Goal:** Produce a go/no-go decision backed by real signals — not gut feeling.

**Duration:** 3–7 days

---

## Skills Involved

```
/trend-researcher → /rapid-prototyper → /feedback-synthesizer → /sprint-prioritizer
```

---

## Step-by-Step

### Step 1 — Research the market (`/trend-researcher`)

Before anything else, validate that the problem exists at scale.

**Invoke:** `/trend-researcher`

**Ask it to:**
- Find demand signals (Reddit, forums, reviews, job boards)
- Map existing competitors and their weaknesses
- Assess market trend: growing, flat, or declining
- Extract customer language (exact phrases people use)

**Output:** Research brief with verdict: Strong / Moderate / Weak opportunity

**Decision gate:** If verdict is Weak and you can't identify a differentiated angle → stop here. Save the time.

---

### Step 2 — Build a smoke test (`/rapid-prototyper`)

Turn the hypothesis into something real that people can react to.

**Invoke:** `/rapid-prototyper`

**Common smoke tests:**
- **Landing page** with email capture and price anchor → tests messaging
- **Wizard of Oz prototype** → looks automated, manually operated → tests willingness to use
- **Clickable mockup** → tests UX assumptions before building

**What to give it:**
- The research brief from Step 1
- Target user, core interaction, success criteria
- Time constraint (2 days max)

**Output:** Live URL or file ready to share

---

### Step 3 — Get it in front of real people

Not a skill — this is founder work.

**Where to share:**
- Personal network (5–10 people who match the target user)
- Relevant Reddit communities (see `/reddit-community-builder`)
- Twitter/X with your build-in-public audience
- Cold DMs to people who match the ICP

**What to collect:**
- Did they sign up / click / engage?
- Qualitative reactions: What confused them? What resonated?
- Would they pay? (If price is shown)

**Minimum signal to continue:** 20+ signups or 5 genuine qualitative conversations

---

### Step 4 — Synthesize the signal (`/feedback-synthesizer`)

Turn raw reactions into structured insights.

**Invoke:** `/feedback-synthesizer`

**Give it:**
- User interview notes or direct quotes
- Email responses
- Conversion data from the landing page

**Output:** Pattern report with top themes, severity scores, and customer language

---

### Step 5 — Decide and plan (`/sprint-prioritizer`)

Make the go/no-go call and — if go — plan the first sprint.

**Invoke:** `/sprint-prioritizer`

**Give it:**
- Research brief (Step 1)
- Feedback synthesis (Step 4)
- Honest assessment of your time/resources

**Output:** Clear recommendation + prioritized build plan for v1

---

## Decision Points

| Signal | Interpretation | Action |
|--------|---------------|--------|
| Strong demand + clear gap | Go | Move to Workflow 2 (Ship v1) |
| Demand exists but angle unclear | Pivot hypothesis | Repeat Steps 1–3 with new angle |
| Weak demand despite good traffic | Messaging problem | Revise copy, re-test |
| No engagement, no interest | No market signal | Abandon or radically rethink |

---

## Example

> **Idea:** A tool that monitors Celery queues and sends Slack alerts when workers stall.
>
> **Step 1 (trend-researcher):** Found 40+ Reddit threads complaining about Flower's limitations. Datadog too complex. Clear gap for lightweight, opinionated monitoring.
>
> **Step 2 (rapid-prototyper):** Built a landing page in 1 hour. Dark theme, Slack mockup, email waitlist.
>
> **Step 3:** Shared in r/Python and r/devops. Got 47 signups in 48 hours.
>
> **Step 4 (feedback-synthesizer):** Top pattern: devs want install-and-forget, not another dashboard.
>
> **Step 5 (sprint-prioritizer):** Go. First sprint: build the core monitoring loop + Slack alert.

---

## Notes

- This workflow is designed to be **cheap** — run it before committing weeks to building
- The landing page from Step 2 becomes your waitlist for Step 3 onwards
- Customer language from Step 4 feeds directly into marketing copy later
