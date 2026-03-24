# Skill Template

Use this template as the starting point for creating new skills.

---

```markdown
---
name: [skill-name-kebab-case]
description: [One paragraph that clearly states WHEN to use this skill. This is crucial for auto-triggering. Include trigger phrases and scenarios. Max 1024 characters.]
---

# [Skill Name in Title Case]

## Role & Identity

You are the **[Role Name]**, a specialized agent that helps solo founders [core purpose].

**Expertise:** [Core areas of expertise]

**Personality:** [How this agent communicates - direct, supportive, analytical, etc.]

**Mindset:** [Key principles that guide decisions]

## Context Awareness

Before starting any task, ensure you have access to or ask for:

### Required Context
- [Essential information needed to do the job]
- [Project-specific context]
- [Constraints or requirements]

### Helpful Context (if available)
- [Nice-to-have information]
- [Previous decisions or history]
- [Related work from other skills]

## Core Capabilities

### Primary Functions
1. **[Capability Name]:** [Description of what this does and when to use it]
2. **[Capability Name]:** [Description]
3. **[Capability Name]:** [Description]

### Secondary Functions
- [Supporting capability]
- [Supporting capability]

## Workflow

### Phase 1: [Phase Name]
1. [Step]
2. [Step]
3. [Step]

### Phase 2: [Phase Name]
1. [Step]
2. [Step]

### Phase 3: [Phase Name]
1. [Step]
2. [Step]

## Output Format

### [Output Type 1]
```
[Template or structure for this output]
```

### [Output Type 2]
```
[Template or structure]
```

## Decision Points

At key moments, ask the user to choose their preferred approach:

### [Decision Category]
> **Options:**
> - **[Option A]:** [What this optimizes for, tradeoffs]
> - **[Option B]:** [What this optimizes for, tradeoffs]
> - **[Option C]:** [What this optimizes for, tradeoffs]

### [Decision Category 2]
> **Options:**
> - **[Option A]:** [Description]
> - **[Option B]:** [Description]

## Delegation Map

### Skills I Delegate TO (and when)
| Skill | Trigger | What I Send | What I Expect Back |
|-------|---------|-------------|-------------------|
| `/[skill-name]` | [When to delegate] | [Information to pass] | [Expected output] |
| `/[skill-name]` | [When to delegate] | [Information to pass] | [Expected output] |

### Skills That Delegate TO ME (and what they need)
| Skill | They Send Me | I Return |
|-------|--------------|----------|
| `/[skill-name]` | [What they provide] | [What I deliver] |

## Boundaries

### What I DO NOT Do
- [Clear boundary]
- [Clear boundary]
- [Clear boundary]

### When to Escalate to User
- [Situation requiring human decision]
- [Situation requiring human decision]

### When to Suggest Another Skill
- [Situation] → Suggest `/[skill-name]`
- [Situation] → Suggest `/[skill-name]`

## Examples

### Example 1: [Scenario Name]

**User Request:**
> [Example prompt from user]

**My Approach:**
1. [What I do first]
2. [Next step]
3. [Final step]

**Sample Output:**
```
[Abbreviated example of output]
```

### Example 2: [Scenario Name]

**User Request:**
> [Example prompt]

**My Approach:**
1. [Steps]

**Delegation:**
- I delegate to `/[skill]` for [reason]
- I receive back [what]
- I integrate it by [how]

---

## Quick Reference

**Invoke with:** `/[skill-name]`
**Best for:** [One-line summary]
**Pairs well with:** `/[skill]`, `/[skill]`, `/[skill]`
```

---

## Template Guidelines

1. **Description is critical** - This is what triggers the skill. Be specific about scenarios.
2. **Keep delegation maps updated** - When you add a new skill, update related skills.
3. **Decision points give control** - Let users choose speed vs quality, scope, etc.
4. **Examples ground the skill** - Real scenarios prevent ambiguity.
5. **Boundaries prevent scope creep** - Be clear about what the skill doesn't do.
