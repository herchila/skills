# Workflows

Five core workflows for solo founders, covering the full product lifecycle — from raw idea to growing, operated product.

Skills are tools. Workflows are how you combine them.

---

## The 5 Workflows

| # | Workflow | When to Use | Duration |
|---|----------|-------------|----------|
| 1 | [**Validate**](01-validate.md) | You have an idea and want to know if it's worth building | 3–7 days |
| 2 | [**Ship v1**](02-ship-v1.md) | Demand is validated, time to build and launch | 2–6 weeks |
| 3 | [**Weekly Sprint**](03-weekly-sprint.md) | Product is live, ongoing development mode | Every week |
| 4 | [**Grow**](04-grow.md) | Core loop works, time to systematically acquire users | Ongoing |
| 5 | [**Operate**](05-operate.md) | Keep a live product healthy with minimal overhead | Ongoing |

---

## How They Connect

```
        ┌─────────────┐
        │  1. Validate │  ← Start here with every new idea
        └──────┬───────┘
               │ Go signal
        ┌──────▼───────┐
        │  2. Ship v1   │  ← Build and launch
        └──────┬───────┘
               │ Product is live
       ┌───────┴────────┐
       │                │
┌──────▼──────┐  ┌──────▼──────┐
│ 3. Weekly   │  │  5. Operate  │  ← Run these in parallel
│   Sprint    │  │              │
└──────┬──────┘  └─────────────┘
       │ Retention works
┌──────▼──────┐
│  4. Grow    │  ← Add once core loop is solid
└─────────────┘
```

---

## Example: Doorman from idea to operation

This is a real example of all 5 workflows applied to **Doorman** — a lightweight monitoring agent for Python/Celery/Redis stacks.

---

### Workflow 1: Validate (Day 1–3)

**The idea:** Devs running Celery can't tell when workers are alive but not processing. Flower doesn't alert. Datadog is overkill.

**`/trend-researcher`**
> Search Reddit (r/Python, r/devops), Celery GitHub issues, Flower reviews.
> Finding: 40+ threads complaining about silent queue stalls. No lightweight solution exists.
> Verdict: **Strong opportunity.**

**`/rapid-prototyper`**
> Build a landing page. Dark theme, terminal mockup, Slack alert simulation, email waitlist.
> Time: 1 hour. Stack: pure HTML + Formspree.

**Share it**
> Post in r/Python and r/devops. DM 10 devs who complained about Flower in recent threads.
> Result: 47 waitlist signups in 48 hours.

**`/feedback-synthesizer`**
> Top pattern from replies: "I don't want a dashboard, I want it to tell me when something's wrong."
> Customer language extracted: "silent failure", "workers look healthy but nothing processes", "zero config".

**`/sprint-prioritizer`**
> Decision: **Go.** First sprint: core monitoring loop + Slack alert. Nothing else.

---

### Workflow 2: Ship v1 (Week 1–3)

**`/sprint-prioritizer`** — v1 scope:
- ✅ Connect to Redis, read queue depth and worker heartbeats
- ✅ Detect stall: 0 tasks processed in configurable window
- ✅ Send Slack alert with queue name, depth, and idle time
- ✅ `pip install doorman-monitor`, one env var, done
- ❌ NOT v1: web dashboard, multiple alert channels, historical data, team features

**`/backend-architect`**
> Architecture: single Python process, polls Redis every 60s, stateless, publishes to Slack webhook.
> No database needed for v1. Config via env vars only.

**`/ai-engineer`**
> Anomaly detection: simple threshold-based first (`tasks_processed_last_N_minutes == 0`).
> No ML needed for v1 — rule-based is faster to ship and easier to explain.

**`/api-tester`**
> Test: Redis connection failure, worker with 0 tasks vs. stalled worker, Slack webhook failure handling.

**`/devops-automator`**
> PyPI publish pipeline via GitHub Actions. CI runs tests on every push. README with `pip install` instructions.

**`/project-shipper`**
> After 2 weeks: "The core works but I want to add metric history before releasing."
> Verdict: **Ship now.** History is v1.1. Email waitlist, post to r/Python.

---

### Workflow 3: Weekly Sprint (Week 4 onwards)

**Monday planning:**

**`/analytics-reporter`**
> Week 1 post-launch: 120 installs, 34 active (ran at least once), 8 sent a Slack alert.
> Key question: Why are 86 installs not running?

**`/feedback-synthesizer`**
> 3 support emails: "I installed it but don't know if it's working."
> Pattern: no feedback when monitoring is healthy → users don't know it's running.

**`/sprint-prioritizer`**
> Sprint goal: "Users know Doorman is running even when everything is fine."
> Must ship: daily "all clear" heartbeat to Slack (opt-in). Nothing else.

**Build:** `/frontend-developer` (CLI flag) + `/content-creator` (update README and docs)

**Friday:** Heartbeat feature ships. Docs updated.

---

### Workflow 4: Grow (Month 2)

**`/analytics-reporter`**
> D7 retention: 61% (users who ran it again after first week). Strong signal.
> Acquisition: almost entirely from the r/Python launch post. No compounding channel yet.

**`/growth-hacker`**
> Funnel diagnosis: retention is solid. Problem is awareness — almost nobody knows this exists.
> Recommendation: content channel (devs search for Celery problems), Reddit ongoing presence.
> Experiment hypothesis: "A blog post titled 'Why Flower won't tell you when your Celery workers stall' will drive qualified organic traffic."

**`/experiment-tracker`**
> Experiment: Publish post, measure signups from organic search in 30 days.
> Success threshold: 20 new installs traceable to search traffic.

**`/content-creator`**
> Writes: "Why Flower won't tell you when your Celery workers stall" — 1,200 words, targets "celery worker monitoring" search intent. Uses exact language from waitlist feedback.

**`/twitter-engager`**
> Thread: "I spent 3 months being paged by users before I realized Flower was lying to me. Here's what I built."
> Includes real numbers: queue depth, idle time, the Slack alert screenshot.

**`/reddit-community-builder`**
> Value-first post in r/Python: shares the problem analysis (not the product).
> In comments, answers "does a tool exist for this?" honestly.

---

### Workflow 5: Operate (Ongoing)

**Daily (10 min):**
- Check Sentry: any errors in the monitoring agent itself?
- Scan support inbox: any install failures or config confusion?

**`/support-responder`** (as needed)
> Wrote 3 help docs in month 1: "How to verify Doorman is running", "Redis connection errors", "Slack webhook setup".
> Each doc was written after the same question appeared twice in support.

**Weekly:**

**`/infrastructure-maintainer`**
> Doorman has no servers (it runs in users' infra). Weekly check: PyPI publish pipeline healthy, GitHub Actions green, no dependency security alerts.

**`/analytics-reporter`**
> Weekly: installs, active users, Slack alerts fired (proxy for "working correctly").

**Monthly:**

**`/finance-tracker`**
> Month 2: 0 revenue (still free). Burn: $12/month (GitHub Actions + domain).
> Runway: personal savings. Decision: launch paid tier at month 3 or extend free beta.

**`/legal-compliance-checker`**
> Doorman doesn't collect user data (privacy-first by design). Verify: PyPI package description matches actual behavior. Privacy policy for website: added.

---

## Workflow vs. Skill

**Skills** are specialists. You invoke them for a specific job.
**Workflows** are sequences. They tell you which skills to use, in what order, and when to move on.

You don't need to follow workflows rigidly — use them as defaults and adapt to your situation.
