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
# Clone the repo anywhere
git clone https://github.com/YOUR_USERNAME/skills.git ~/skills-repo

# Copy only the skills you want
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

### Engineering (6 skills)
| Skill | Command | Use When |
|-------|---------|----------|
| Frontend Developer | `/frontend-developer` | Building user interfaces, React/Vue/HTML components |
| Backend Architect | `/backend-architect` | Designing APIs, databases, system architecture |
| Mobile App Builder | `/mobile-app-builder` | Creating iOS/Android apps, React Native, Flutter |
| AI Engineer | `/ai-engineer` | Implementing ML features, LLM integrations, AI pipelines |
| DevOps Automator | `/devops-automator` | CI/CD, deployment, infrastructure, monitoring |
| Rapid Prototyper | `/rapid-prototyper` | Building MVPs fast, validating ideas with working code |

### Product (3 skills)
| Skill | Command | Use When |
|-------|---------|----------|
| Trend Researcher | `/trend-researcher` | Market research, competitor analysis, opportunity validation |
| Feedback Synthesizer | `/feedback-synthesizer` | Processing user feedback, interviews, reviews into insights |
| Sprint Prioritizer | `/sprint-prioritizer` | Deciding what to build next, managing backlog, planning sprints |

### Marketing (7 skills)
| Skill | Command | Use When |
|-------|---------|----------|
| TikTok Strategist | `/tiktok-strategist` | Short-form video strategy, trends, content planning |
| Instagram Curator | `/instagram-curator` | Visual content strategy, reels, stories, feed planning |
| Twitter Engager | `/twitter-engager` | Twitter/X strategy, threads, engagement, building audience |
| Reddit Community Builder | `/reddit-community-builder` | Reddit marketing, community engagement, authentic participation |
| App Store Optimizer | `/app-store-optimizer` | ASO, app store listings, keywords, screenshots |
| Content Creator | `/content-creator` | Blog posts, newsletters, documentation, copywriting |
| Growth Hacker | `/growth-hacker` | Growth experiments, acquisition channels, viral mechanics |

### Design (5 skills)
| Skill | Command | Use When |
|-------|---------|----------|
| UI Designer | `/ui-designer` | Interface design, components, layouts, design systems |
| UX Researcher | `/ux-researcher` | User research, usability testing, journey mapping |
| Brand Guardian | `/brand-guardian` | Brand consistency, voice, visual identity |
| Visual Storyteller | `/visual-storyteller` | Presentations, graphics, visual narratives |
| Whimsy Injector | `/whimsy-injector` | Adding delight, micro-interactions, personality to products |

### Project Management (3 skills)
| Skill | Command | Use When |
|-------|---------|----------|
| Experiment Tracker | `/experiment-tracker` | Tracking A/B tests, experiments, learnings |
| Project Shipper | `/project-shipper` | Pushing projects to completion, unblocking, shipping |
| Studio Producer | `/studio-producer` | Orchestrating multiple projects, resource allocation |

### Studio Operations (5 skills)
| Skill | Command | Use When |
|-------|---------|----------|
| Support Responder | `/support-responder` | Customer support, help docs, ticket responses |
| Analytics Reporter | `/analytics-reporter` | Metrics analysis, dashboards, data insights |
| Infrastructure Maintainer | `/infrastructure-maintainer` | Server maintenance, updates, security patches |
| Legal Compliance Checker | `/legal-compliance-checker` | Privacy policies, terms, GDPR, legal requirements |
| Finance Tracker | `/finance-tracker` | Revenue tracking, expenses, runway, financial planning |

### Testing (5 skills)
| Skill | Command | Use When |
|-------|---------|----------|
| Tool Evaluator | `/tool-evaluator` | Evaluating tools, comparing options, making tech decisions |
| API Tester | `/api-tester` | Testing APIs, edge cases, integration testing |
| Workflow Optimizer | `/workflow-optimizer` | Improving processes, automation, efficiency |
| Performance Benchmarker | `/performance-benchmarker` | Load testing, performance analysis, optimization |
| Test Results Analyzer | `/test-results-analyzer` | Analyzing test results, identifying patterns, QA insights |

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

## Quick Start

1. Install the skills (see Installation above)
2. In Claude Code, type `/rapid-prototyper` to invoke a skill
3. Describe what you need
4. Follow the skill's workflow

## Creating Your Own Skills

Use `TEMPLATE.md` as a starting point for creating new skills.

## Contributing

Contributions welcome! Please read the existing skills for style consistency.

## License

MIT License - see [LICENSE](LICENSE)
