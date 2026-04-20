# Skills

Claude Code skills for solo founders who want to operate like a full team.

## What is this?

A collection of 34 specialized AI agents that cover the full spectrum of running a startup: engineering, product, marketing, design, project management, operations, and testing.

Each skill is a detailed prompt that transforms Claude into a focused expert for a specific role.

## Installation

### Option 1: Install all skills (recommended)

```bash
# Clone into Claude Code's skills directory
git clone https://github.com/YOUR_USERNAME/skills.git ~/.claude/skills/solo-founder
```

After cloning, all skills are immediately available. Type `/rapid-prototyper` in Claude Code to use it.

### Option 2: Install specific skills only

```bash
# 1. Clone the repo anywhere
git clone https://github.com/YOUR_USERNAME/skills.git ~/skills-repo

# 2. Copy only the skills you want
cp -r ~/skills-repo/agents/engineering/rapid-prototyper ~/.claude/skills/
cp -r ~/skills-repo/agents/product/sprint-prioritizer ~/.claude/skills/
```

### Option 3: Install for a specific project

Add skills to your project's `.claude/skills/` directory:

```bash
# From your project root
mkdir -p .claude/skills
cp -r ~/skills-repo/agents/engineering/rapid-prototyper .claude/skills/
```

Project-level skills are only available when working in that project.

### Verify installation

In Claude Code, type `/` and you should see the installed skills in the autocomplete menu. Or just type the full command like `/rapid-prototyper` to invoke it directly.

### Updating skills

```bash
cd ~/.claude/skills/solo-founder
git pull
```

## Available Skills

See [SKILLS.md](SKILLS.md) for the full list of 34 skills organized by category.

## Workflows

Five pre-built workflows that chain skills together for the most common founder scenarios:

| Workflow | When to Use |
|----------|-------------|
| [1. Validate](workflows/01-validate.md) | New idea — is it worth building? |
| [2. Ship v1](workflows/02-ship-v1.md) | Validated demand — build and launch |
| [3. Weekly Sprint](workflows/03-weekly-sprint.md) | Ongoing development cadence |
| [4. Grow](workflows/04-grow.md) | Systematically acquire and retain users |
| [5. Operate](workflows/05-operate.md) | Keep a live product healthy |

See [workflows/README.md](workflows/README.md) for the full guide.

## Quick Start

1. Install the skills (see Installation above)
2. In Claude Code, type `/rapid-prototyper` to invoke a skill
3. Describe what you need
4. Follow the skill's workflow

## Skill Structure

Each skill follows this structure:

```
agents/
└── [category]/
    └── [skill-name]/
        ├── SKILL.md      # Main instructions (required)
        ├── references/   # Additional docs (optional)
        └── examples/     # Example outputs (optional)
```

## Core Concepts

### Skills Know Each Other

Skills are designed to work together. Each skill knows when to delegate to another:

- `/rapid-prototyper` → delegates to `/ui-designer` for polish
- `/trend-researcher` → feeds insights to `/sprint-prioritizer`
- `/content-creator` → checks with `/brand-guardian` for consistency

### User Controls the Workflow

Skills ask you to make decisions at key moments:

- Speed vs Quality
- Scope (minimal vs comprehensive)
- When to involve other skills

### Built for Solo Founders

Every skill is optimized for the constraints of building alone:

- Pragmatic over perfect
- Ship fast, learn, iterate
- Automate what you can, focus on what matters

## Creating Your Own Skills

Use `TEMPLATE.md` as a starting point for creating new skills.

## Contributing

Contributions welcome! Please read the existing skills for style consistency.

## License

MIT License - see [LICENSE](LICENSE)
