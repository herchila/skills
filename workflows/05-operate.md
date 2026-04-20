---
name: operate
description: Keep a live product healthy — users supported, infrastructure stable, finances clear.
---

# Workflow 5: Operate

**Use when:** The product is live with real users and you need to keep it running reliably without letting operations consume all your building time.

**Goal:** A stable, well-monitored product with supported users and clear financials — with the minimum operational overhead needed.

**Cadence:** Daily lightweight + Weekly review + Monthly deep check

---

## Skills Involved

```
/support-responder + /infrastructure-maintainer → /analytics-reporter → /finance-tracker
```

---

## Daily Operations (~30 min/day)

These should become habits, not projects.

### 1. Support inbox

**Invoke:** `/support-responder` when you need to:
- Respond to a complex or sensitive ticket
- Write a template for a recurring issue
- Handle an angry user or refund request

**Self-service rule:** If the same question comes up 3+ times → write a help doc. Invoke `/support-responder` to write it.

---

### 2. Infrastructure health check (~5 min)

**Every morning, check:**
- Uptime monitor (UptimeRobot / Better Uptime) — any alerts?
- Error tracking (Sentry) — any new errors overnight?
- Failed background jobs — any queue issues?

If something is wrong → invoke `/infrastructure-maintainer`.

---

## Weekly Operations (~1 hour)

### 1. Full infrastructure health check (`/infrastructure-maintainer`)

**Invoke:** `/infrastructure-maintainer`

**Weekly checklist:**
- [ ] Uptime last 7 days
- [ ] Error rate normal?
- [ ] Disk usage within bounds
- [ ] SSL cert expiry > 30 days
- [ ] Any dependency security alerts?

**Output:** Green / Yellow / Red status + action items

---

### 2. Metrics review (`/analytics-reporter`)

**Invoke:** `/analytics-reporter`

**Weekly metrics report — 20 min to fill, 5 min to read:**
- North star metric: up/down/flat vs last week
- What moved? Why?
- One question the data raises for this week

**Output:** Weekly report that feeds into Monday sprint planning (Workflow 3)

---

### 3. Support pattern check

**Every week, scan last week's tickets for patterns:**
- Same error mentioned 3+ times → it's a product bug or a docs gap
- Same question 3+ times → write the help doc
- Recurring complaint → add to product backlog

**Invoke `/support-responder`** to write the help doc.
**Invoke `/sprint-prioritizer`** to add the bug to the backlog.

---

## Monthly Operations (~3 hours)

### 1. Financial review (`/finance-tracker`)

**Invoke:** `/finance-tracker`

**Monthly snapshot:**
- MRR: current, growth rate vs last month
- Churn: how many users left?
- Burn rate: expenses vs revenue
- Runway: months remaining

**Output:** Financial snapshot + updated runway calculation

**Rule:** If runway drops below 6 months → this immediately becomes the top priority. Everything else is secondary.

---

### 2. Infrastructure maintenance (`/infrastructure-maintainer`)

**Invoke:** `/infrastructure-maintainer`

**Monthly tasks:**
- Apply dependency updates (batch minor, patch critical immediately)
- Rotate any secrets that are > 90 days old
- Verify backup restore works (actually restore from backup)
- Review server costs vs. actual usage
- Check for any security advisories

---

### 3. Legal & compliance check (`/legal-compliance-checker`)

**Invoke when:**
- You've added new data collection
- You've expanded to new regions
- New regulations apply to your product
- Privacy policy is > 6 months old

**Monthly quick check:** Is the privacy policy still accurate given what the product does now?

---

## Incident Response

When something breaks in production:

**Step 1 — Triage (< 5 min)**
- What's broken? How many users affected?
- Is it getting worse or stable?
- Is there a quick mitigation (rollback, feature flag)?

**Step 2 — Invoke `/infrastructure-maintainer`**
Give it: what's broken, when it started, any recent changes.
It returns: diagnostic approach + fix.

**Step 3 — Communicate**
- If users are affected: acknowledge it. A short "we're aware and working on it" is better than silence.
- Use `/support-responder` to write the status message.

**Step 4 — Post-mortem**
After fixing: document what happened, why, and how to prevent it.
`/infrastructure-maintainer` writes the post-mortem.

---

## Automate the Routine

As operations grow, automate what runs the same way every time.

**Invoke:** `/workflow-optimizer`

**Good candidates for automation:**
- Weekly metrics email (pull from Stripe + analytics, send to yourself)
- Database backup verification
- Dependency update PR creation
- Recurring support report generation

**Rule:** If you do it manually more than once a week → automate it.

---

## Operations Health Dashboard

| Area | Check | Frequency | Skill |
|------|-------|-----------|-------|
| Support queue | < 24h response | Daily | `/support-responder` |
| Uptime | > 99.5% | Daily (automated) | `/infrastructure-maintainer` |
| Error rate | Baseline or below | Daily (automated) | `/infrastructure-maintainer` |
| MRR | Growing | Weekly | `/finance-tracker` |
| Runway | > 6 months | Monthly | `/finance-tracker` |
| Backups | Verified working | Monthly | `/infrastructure-maintainer` |
| Dependencies | No critical vulns | Monthly | `/infrastructure-maintainer` |
| Privacy policy | Accurate | Quarterly | `/legal-compliance-checker` |

---

## When Operations Needs More Attention

| Signal | Action |
|--------|--------|
| Support volume growing fast | Build self-service docs, fix the root cause product issues |
| Same infrastructure incident repeating | Invoke `/infrastructure-maintainer` for prevention plan |
| Runway below 6 months | Immediate focus: cut expenses, accelerate revenue |
| Can't keep up with operations + building | Automate more, or reduce product scope temporarily |

---

## Notes

- Operations should take < 1 hour/day. If it's more, something is broken — automate or fix the root cause.
- The monthly financial review is non-negotiable. Runway surprises kill companies.
- Support tickets are your cheapest user research. Read them, don't just close them.
