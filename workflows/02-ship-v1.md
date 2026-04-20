---
name: ship-v1
description: Go from validated idea to a live product users can actually use.
---

# Workflow 2: Ship v1

**Use when:** You've validated demand (Workflow 1) and it's time to build and launch the real product.

**Goal:** A working, deployed product in the hands of real users — not a perfect product, a shipped one.

**Duration:** 2–6 weeks depending on scope

---

## Skills Involved

```
/sprint-prioritizer → /backend-architect + /ui-designer → /frontend-developer → /api-tester → /devops-automator → /project-shipper
```

---

## Step-by-Step

### Step 1 — Scope v1 ruthlessly (`/sprint-prioritizer`)

Before building anything, decide exactly what v1 includes — and explicitly what it doesn't.

**Invoke:** `/sprint-prioritizer`

**Give it:**
- Everything you want to build (full wishlist)
- What you validated in Workflow 1
- Your available time

**Output:** v1 scope with a clear "NOT in v1" list

**Rule:** v1 should be completable in 2 weeks max. If it isn't, cut more.

---

### Step 2 — Design the backend (`/backend-architect`)

Define the data model and API before writing any code.

**Invoke:** `/backend-architect`

**Give it:**
- v1 scope from Step 1
- Core entities and their relationships
- Integration requirements (auth, payments, third-party APIs)
- Your preferred stack (or ask for a recommendation)

**Output:** Database schema + API spec + stack decision

---

### Step 3 — Design the UI (`/ui-designer`)

*Run in parallel with Step 2.*

**Invoke:** `/ui-designer`

**Give it:**
- The screens required for v1 scope
- Any brand direction or references
- Target user and their technical sophistication

**Output:** Design system tokens + screen layout specs

**Skip if:** v1 is a CLI tool, API, or internal tool with no public UI.

---

### Step 4 — Build the frontend (`/frontend-developer`)

Implement the UI from the design spec, wired to the API.

**Invoke:** `/frontend-developer`

**Give it:**
- Design spec from Step 3
- API contracts from Step 2
- Tech stack decided in Step 2

**Output:** Working frontend — all states implemented (loading, error, empty, success)

---

### Step 5 — Test the API (`/api-tester`)

Before deploying, validate the backend behaves correctly.

**Invoke:** `/api-tester`

**Give it:**
- API spec from Step 2
- Auth flow details
- Any business-critical paths (payments, writes, deletes)

**Output:** Integration test suite — at minimum: happy path + auth + top edge cases per endpoint

---

### Step 6 — Deploy (`/devops-automator`)

Get the product live with auto-deploy on push.

**Invoke:** `/devops-automator`

**Give it:**
- Stack details from Step 2
- Hosting preference or budget
- Environment variables needed

**Output:**
- Live URL
- CI/CD pipeline (tests run on every push)
- Basic uptime monitoring
- Database backups configured

---

### Step 7 — Ship it (`/project-shipper`)

When you're in "almost ready" mode too long, use this to push across the finish line.

**Invoke:** `/project-shipper`

**Especially useful when:**
- You keep adding "one more thing" before launching
- The product works but you don't feel ready
- It's been "almost done" for more than a week

**Output:** Ship/no-ship assessment + hard launch date + first 10 people to tell

---

## Parallel Tracks

Some steps can run in parallel to save time:

```
Step 2 (backend-architect)  ─────┐
                                  ├── Step 4 (frontend-developer)
Step 3 (ui-designer)       ─────┘

Step 5 (api-tester) can start as soon as Step 2 is complete
Step 6 (devops-automator) can be set up while Steps 4-5 are running
```

---

## v1 Quality Bar

v1 needs to pass this bar — nothing more:

| Criteria | Required |
|----------|---------|
| Core user flow works end-to-end | ✅ Must have |
| Auth works (if applicable) | ✅ Must have |
| Data doesn't get lost | ✅ Must have |
| No security holes with real user data | ✅ Must have |
| Looks clean (not polished) | ✅ Must have |
| All edge cases handled | ❌ Not for v1 |
| Mobile-optimized | ❌ Unless mobile is core |
| Full test coverage | ❌ Critical paths only |
| Performance under heavy load | ❌ After you have users |

---

## Decision Points

| Situation | Action |
|-----------|--------|
| Scope keeps growing | Return to `/sprint-prioritizer` and cut |
| Technical blocker is slowing everything | Consult `/backend-architect` for alternatives |
| Build is taking too long | Invoke `/project-shipper` — it's probably shippable now |
| UI looks bad | `/ui-designer` for a focused audit, not a full redesign |

---

## After Shipping

Once v1 is live → move to **Workflow 3 (Weekly Sprint)** for ongoing iteration.

---

## Notes

- The order matters: design backend before building frontend — API contracts prevent rework
- `/project-shipper` is not the last step by accident — perfectionism is the #1 reason v1 never ships
- "Soft launch" first: 10 users before 1000. Catch the obvious problems before they're at scale.
