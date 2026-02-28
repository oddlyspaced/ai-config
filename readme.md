# AI Config

Personal Cursor configuration with skills, agents, and rules for structured planning and implementation workflows.

## Installation

### Option 1: Global (Recommended)

Install once, available in all projects:

```bash
cd /Users/hardik/Projects/ai-config

# Copy everything to global Cursor config
cp -r .cursor/* ~/.cursor/

# Verify
ls -la ~/.cursor/
# Should see: skills/, agents/, rules/
```

### Option 2: Project-Specific

Install in individual projects:

```bash
cd /Users/hardik/Projects/ai-config

# Copy to your project
cp -r .cursor/* /path/to/your-project/.cursor/
```

### Post-Installation

Create required folders in each project where you'll use the skills:

```bash
cd /path/to/your-project
mkdir -p thoughts/shared/plans thoughts/shared/specs thoughts/shared/handoffs thoughts/ledgers
```

Open your project in Cursor and type `/` in chat -- you should see the available skills.

---

## Quick Start

### 1. Create a Plan

In Cursor chat:

```
/create_plan
```

Or with a file reference:

```
/create_plan thoughts/tickets/feature-123.md
```

What happens:
1. AI asks what you're building
2. Spawns agents to research your codebase
3. Asks clarifying questions
4. Creates detailed plan at `thoughts/shared/plans/YYYY-MM-DD-description.md`

### 2. Implement the Plan

```
/implement_plan thoughts/shared/plans/YYYY-MM-DD-description.md
```

What happens:
1. Reads the plan and creates continuity ledger
2. For each task:
   - `implement_task` agent implements the work
   - `task-review-agent` reviews the code
   - Fixes issues if needed (max 3 iterations)
   - Creates handoff document
3. Moves to next task after approval
4. Survives context compaction (handoffs persist on disk)

Two modes:
- **Direct** (1-3 tasks): Implements in main context
- **Agent Orchestration** (4+ tasks): Agents handle each task

---

## What's Included

### Skills (8)

| Skill | Description |
|-------|-------------|
| `/create_plan` | Create detailed implementation plans through interactive research |
| `/implement_plan` | Execute plans with task tracking and review loops |
| `/implement_task` | Sub-skill used by implement_plan for individual tasks |
| `/create_new_project_vercel_nextjs_plan` | Plan greenfield Next.js + Vercel web apps |
| `/implement_new_project_vercel_nextjs_plan` | Execute Next.js + Vercel plans with architecture validation |
| `/plan_python_vercel_backend_architect` | Plan Python Flask + Vercel backend APIs |
| `/implement_python_vercel_backend_architect` | Execute Python Flask + Vercel backend plans |
| `/debug_plan` | Systematic debugging through structured investigation |

### Agents (8)

Planning & exploration:
- **`codebase-locator`** - Find files and components related to features
- **`codebase-analyzer`** - Deep dive into implementation details
- **`codebase-pattern-finder`** - Find similar implementations and patterns

Architecture specialists:
- **`nextjs-vercel-architect`** - Next.js + Vercel architecture validation and optimization
- **`python-vercel-backend-architect`** - Python Flask + Vercel backend architecture validation

Quality & validation:
- **`validate-agent`** - Validate plans against best practices
- **`review-agent`** - Review entire implementation (plan vs reality)
- **`task-review-agent`** - Review individual task implementations

### Rules (3)

| Rule | Applies To |
|------|-----------|
| `react-native-standards.mdc` | `**/*.tsx`, `**/*.ts`, `**/*.swift`, `**/*.kt` |
| `nextjs-vercel-standards.mdc` | `**/*.tsx`, `**/*.ts`, `**/*.jsx`, `**/*.js`, `next.config.*`, `middleware.ts` |
| `python-vercel-backend-standards.mdc` | Python Flask + Vercel backend projects |

---

## Workflow

### The Full Cycle

```
Feature Request
      |
  /create_plan  --> Research --> Questions --> Plan Document
      |
/implement_plan --> Task 1 --> Review --> Fix --> Approved
                    Task 2 --> Review --> Fix --> Approved
                    Task 3 --> Review --> Fix --> Approved
                    ...
      |
   Feature Done
```

### Example: Planning Phase

```
You: /create_plan

AI: I'll help you create a detailed implementation plan.
    What are you building?

You: Add biometric authentication to the login screen

AI: [Spawns codebase research agents...]
    I found the current auth implementation at src/auth/...

    Questions:
    - Should we support both Face ID and Touch ID?
    - What happens if biometric auth fails?
    - Should we keep password login as fallback?

You: [Answer questions...]

AI: [Creates detailed plan with phases, code examples, success criteria]
    Plan created at: thoughts/shared/plans/2026-02-11-biometric-auth.md
```

### Example: Implementation Phase

```
You: /implement_plan thoughts/shared/plans/2026-02-11-biometric-auth.md

AI: I'll use agent orchestration for this plan (5 tasks).

    Creating continuity ledger: thoughts/ledgers/biometric-auth.md
    Setting up handoffs: thoughts/shared/handoffs/biometric-auth/

    ─────────────────────────────────────
    Task 1 of 5: Create biometric auth module
    ─────────────────────────────────────

    Implementing...
    [Spawns implement_task agent]
    [Creates handoff: task-01-biometric-module.md]

    Reviewing (iteration 1)...
    [Spawns task-review-agent]
    [Review: APPROVED]

    Task 1 approved. Moving to Task 2...

    [Continues for all 5 tasks...]
```

### Behind the Scenes

**During `/create_plan`:**
1. `codebase-locator` finds relevant files
2. `codebase-analyzer` understands current implementation
3. `codebase-pattern-finder` finds similar patterns
4. AI asks clarifying questions
5. Creates detailed plan with phases, code examples, and success criteria

**During `/implement_plan`:**
1. Creates continuity ledger and handoff directory
2. For each task: Implement -> Review -> Fix (if needed) -> Approve -> Next
3. Each task creates a handoff document that persists on disk
4. Ledger tracks progress across sessions

### Generated Artifacts

```
thoughts/
├── shared/
│   ├── plans/
│   │   └── 2026-02-11-push-notifications.md
│   └── handoffs/
│       └── push-notifications/
│           ├── task-01-ios-apns-setup.md
│           ├── task-02-android-fcm-setup.md
│           └── ...
└── ledgers/
    └── push-notifications.md
```

---

## Next.js + Vercel Projects

For greenfield Next.js websites deployed on Vercel:

### Plan

```
/create_new_project_vercel_nextjs_plan
```

What happens:
1. Analyzes your Next.js template structure
2. Uses `nextjs-vercel-architect` agent for validation
3. Deep requirements interview (content, UX, performance, SEO)
4. Creates comprehensive 5-phase plan optimized for Vercel

### Implement

```
/implement_new_project_vercel_nextjs_plan thoughts/shared/plans/2026-02-11-nextjs-project.md
```

Additional checks beyond the standard workflow:
- TypeScript strict mode (`npx tsc --noEmit`)
- ESLint verification (`npm run lint`)
- Build verification (`npm run build`)
- Lighthouse audit (90+ required)
- Core Web Vitals check
- Bundle size verification (< 100kb)
- SEO completeness check
- Vercel deployment readiness

See `.cursor/skills/create_new_project_vercel_nextjs_plan/README.md` for detailed usage.

---

## Python Flask + Vercel Backend

For greenfield Python Flask APIs deployed on Vercel:

### Plan

```
/plan_python_vercel_backend_architect
```

### Implement

```
/implement_python_vercel_backend_architect thoughts/shared/plans/YYYY-MM-DD-project.md
```

See `.cursor/skills/plan_python_vercel_backend_architect/README.md` for detailed usage.

---

## Debugging

For systematic bug investigation:

```
/debug_plan
```

Walks through structured investigation, root cause analysis, and fix planning.

---

## Tips

### Better Plans
- Provide ticket files or detailed descriptions
- Answer questions thoroughly
- Mention constraints upfront (deadlines, platform differences)

### Smooth Implementation
- Trust the process -- let agents do their work
- Read handoffs if you need to resume (`thoughts/shared/handoffs/`)
- Check the ledger for current state (`thoughts/ledgers/`)

### Context Limits
If context clears mid-implementation, just run the same command again:
```
/implement_plan thoughts/shared/plans/YYYY-MM-DD-description.md
```
AI reads the ledger and handoffs, continues from where it stopped.

---

## Troubleshooting

### Skill not showing up
1. Check file structure: `ls -la ~/.cursor/skills/create_plan/` (should contain `SKILL.md`)
2. Restart Cursor completely
3. Check frontmatter in SKILL.md has `description:` field

### Agents not working
1. Verify agents exist: `ls -la ~/.cursor/agents/`
2. Check agent files have proper YAML frontmatter with `name:` and `description:`

### Folder not found errors
```bash
mkdir -p thoughts/shared/plans thoughts/shared/specs thoughts/shared/handoffs thoughts/ledgers
```

### Review keeps rejecting
After 3 iterations, you'll be asked to continue with issues, fix manually, or skip task.

---

## Folder Structure

```
ai-config/
├── readme.md
└── .cursor/
    ├── skills/
    │   ├── create_plan/
    │   ├── create_new_project_vercel_nextjs_plan/
    │   ├── implement_plan/
    │   ├── implement_new_project_vercel_nextjs_plan/
    │   ├── implement_task/
    │   ├── plan_python_vercel_backend_architect/
    │   ├── implement_python_vercel_backend_architect/
    │   └── debug_plan/
    ├── agents/
    │   ├── codebase-locator.md
    │   ├── codebase-analyzer.md
    │   ├── codebase-pattern-finder.md
    │   ├── nextjs-vercel-architect.md
    │   ├── python-vercel-backend-architect.md
    │   ├── validate-agent.md
    │   ├── review-agent.md
    │   └── task-review-agent.md
    └── rules/
        ├── react-native-standards.mdc
        ├── nextjs-vercel-standards.mdc
        └── python-vercel-backend-standards.mdc
```

---

## Updating

To get latest changes after pulling this repo:

```bash
cd /Users/hardik/Projects/ai-config

# Reinstall globally
cp -r .cursor/* ~/.cursor/

# Or to a specific project
cp -r .cursor/* /path/to/your-project/.cursor/
```

## Adding Custom Rules

Create additional rules following this pattern:

```markdown
---
description: Your custom standards
globs: ["**/*.tsx", "**/*.ts"]
alwaysApply: false
---

# Your Standards

Your conventions and patterns here...
```
