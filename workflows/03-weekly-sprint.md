---
name: weekly-sprint
description: Run a focused, productive week — from Monday planning to Friday shipping.
---

# Workflow 3: Weekly Sprint

**Use when:** The product is live and you're in ongoing development mode — building, learning, iterating every week.

**Goal:** Ship one meaningful thing per week, grounded in user feedback and business metrics.

**Cadence:** Every week, repeated

---

## Skills Involved

```
/analytics-reporter + /feedback-synthesizer → /sprint-prioritizer → [build skills] → /project-shipper
```

---

## Weekly Rhythm

```
Monday       Tuesday–Thursday     Friday
────────      ─────────────────    ──────────
Plan          Build                Review + Ship
```

---

## Monday: Plan (2–3 hours)

### 1. Review what happened last week (`/analytics-reporter`)

Before planning, understand the current state.

**Invoke:** `/analytics-reporter`

**Review:**
- North star metric: up, down, flat?
- Any unexpected drops or spikes?
- Any new data from the week?

**Output:** 10-minute metrics read. One key question the data raises.

---

### 2. Process incoming feedback (`/feedback-synthesizer`)

**Invoke:** `/feedback-synthesizer`

**Feed it:**
- Support tickets from last week
- User replies, emails, DMs
- App reviews (if mobile)
- Any interviews conducted

**Output:** Top themes with severity — what's causing friction for real users right now?

---

### 3. Set the sprint (`/sprint-prioritizer`)

**Invoke:** `/sprint-prioritizer`

**Give it:**
- Metrics summary from analytics-reporter
- Feedback synthesis
- Anything carried over from last week
- Your honest time estimate for the week

**Output:**
- Sprint goal (one sentence)
- Must-ship list (2–3 tasks max)
- Explicit "NOT this week" list
- Minimum viable sprint (if everything breaks, this one thing ships)

---

## Tuesday–Thursday: Build

Use the appropriate skill for each task in the sprint.

| Task Type | Skill |
|-----------|-------|
| New UI screen | `/frontend-developer` + `/ui-designer` |
| New API endpoint | `/backend-architect` → `/api-tester` |
| AI feature | `/ai-engineer` |
| Copy or docs update | `/content-creator` |
| Bug fix | `/frontend-developer` or `/backend-architect` |
| Automation | `/workflow-optimizer` |
| Performance issue | `/performance-benchmarker` |

**Rules while building:**
- Work from the sprint plan — don't add scope mid-week
- If a new urgent thing appears → add to next sprint backlog, not this one
- If a task is taking 3x longer than expected → flag it to `/project-shipper`

---

## Friday: Review + Ship (1–2 hours)

### 1. Ship what's done (`/project-shipper`)

If something is "almost done" and you're hesitating → invoke `/project-shipper`.

**It will tell you:** Ship now, ship a scoped-down version, or identify the one real blocker.

---

### 2. Weekly review (no skill needed — 20 min)

Answer these 4 questions in writing:

1. **What shipped?** (specific, not "worked on X")
2. **What did we learn?** (from data, users, or building)
3. **What slowed us down?** (to address next week)
4. **What's the plan for next week?** (rough — sprint-prioritizer will refine Monday)

---

## Sprint Health Signals

| Signal | What It Means | Action |
|--------|--------------|--------|
| Shipped the must-haves | Healthy sprint | Continue |
| Scope crept mid-week | Process issue | Be stricter with "NOT this week" list |
| Same item in backlog 3 weeks | Blocker or avoidance | Resolve or deliberately kill it |
| Nothing shipped | Estimation issue or morale | Shrink scope next sprint |
| Feedback and metrics not reviewed | Flying blind | Never skip Monday planning |

---

## Monthly Supplement

Once a month (suggest: first Monday), extend the planning session with:

- **Finance review** (`/finance-tracker`): MRR growth, burn rate, runway update
- **Experiment review** (`/experiment-tracker`): What did we learn from experiments this month?
- **Portfolio check** (if multiple products, `/studio-producer`): Is time allocation still right?

---

## Connecting to Other Workflows

- **If metrics show a retention problem** → run a mini Workflow 1 (validate the fix) before building
- **If scope has grown to a major release** → run Workflow 2 (ship v1) scoped around that release
- **If a new growth channel is being explored** → run Workflow 4 (grow) in parallel

---

## Notes

- The review in steps 1–2 is not optional. Skipping it means building based on assumption, not signal.
- The "NOT this week" list is as important as the sprint plan. Write it down.
- Friday review takes 20 minutes and saves hours of confusion on Monday.
