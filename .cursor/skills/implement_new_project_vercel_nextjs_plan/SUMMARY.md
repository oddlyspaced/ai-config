# Implement Next.js + Vercel Project Plan - Summary

## What Was Created

A specialized implementation skill for executing Next.js 15+ and Vercel project plans with comprehensive quality assurance and validation.

## The Complete Next.js + Vercel Workflow

```
┌──────────────────────────────────────────────────────────────────┐
│                    PLANNING PHASE                                │
│  /create_new_project_vercel_nextjs_plan                          │
│                                                                   │
│  ├─ Template Analysis                                            │
│  ├─ Requirements Interview                                       │
│  ├─ Architecture Decisions (nextjs-vercel-architect)             │
│  └─ Comprehensive 5-Phase Plan                                   │
│                                                                   │
│  Output: thoughts/shared/plans/YYYY-MM-DD-project.md             │
└──────────────────────────────────────────────────────────────────┘
                               ↓
┌──────────────────────────────────────────────────────────────────┐
│                 IMPLEMENTATION PHASE                              │
│  /implement_new_project_vercel_nextjs_plan      ← NEW SKILL!     │
│                                                                   │
│  For Each Phase:                                                 │
│  ┌────────────────────────────────────────────────────────┐     │
│  │ 1. IMPLEMENT                                           │     │
│  │    ├─ Follow Next.js 15 patterns                      │     │
│  │    ├─ Apply nextjs-vercel-standards.mdc rules         │     │
│  │    └─ Respect architecture decisions                  │     │
│  └────────────────────────────────────────────────────────┘     │
│                          ↓                                       │
│  ┌────────────────────────────────────────────────────────┐     │
│  │ 2. VERIFY BUILD                                        │     │
│  │    ├─ TypeScript check (npx tsc --noEmit)             │     │
│  │    ├─ ESLint check (npm run lint)                     │     │
│  │    ├─ Next.js build (npm run build)                   │     │
│  │    ├─ Bundle size analysis                            │     │
│  │    └─ Route optimization check                        │     │
│  └────────────────────────────────────────────────────────┘     │
│                          ↓                                       │
│  ┌────────────────────────────────────────────────────────┐     │
│  │ 3. VALIDATE ARCHITECTURE                               │     │
│  │    Uses: nextjs-vercel-architect agent                 │     │
│  │    ├─ Data fetching strategy (SSG/ISR/SSR)            │     │
│  │    ├─ Server vs Client Component boundaries           │     │
│  │    ├─ Performance impact                              │     │
│  │    ├─ Vercel optimization                             │     │
│  │    └─ SEO implementation                              │     │
│  └────────────────────────────────────────────────────────┘     │
│                          ↓                                       │
│  ┌────────────────────────────────────────────────────────┐     │
│  │ 4. REVIEW CODE QUALITY                                 │     │
│  │    Uses: task-review-agent                             │     │
│  │    ├─ TypeScript types                                │     │
│  │    ├─ Component patterns                              │     │
│  │    ├─ Error handling                                  │     │
│  │    └─ Standards compliance                            │     │
│  └────────────────────────────────────────────────────────┘     │
│                          ↓                                       │
│  ┌────────────────────────────────────────────────────────┐     │
│  │ 5. FIX ISSUES (if needed, max 3 iterations)           │     │
│  │    ├─ Address review comments                         │     │
│  │    ├─ Fix architecture issues                         │     │
│  │    └─ Re-validate                                     │     │
│  └────────────────────────────────────────────────────────┘     │
│                          ↓                                       │
│  ┌────────────────────────────────────────────────────────┐     │
│  │ 6. MANUAL VERIFICATION                                 │     │
│  │    ├─ Browser testing                                  │     │
│  │    ├─ Responsive design check                         │     │
│  │    ├─ Functionality verification                      │     │
│  │    └─ User confirmation                               │     │
│  └────────────────────────────────────────────────────────┘     │
│                                                                   │
│  Progress Tracking:                                              │
│  ├─ Ledger: thoughts/ledgers/project.md                          │
│  └─ Handoffs: thoughts/handoffs/project/phase-NN-*.md            │
└──────────────────────────────────────────────────────────────────┘
                               ↓
┌──────────────────────────────────────────────────────────────────┐
│                   FINAL VALIDATION PHASE                          │
│                                                                   │
│  ├─ Lighthouse Audit (90+ required on all metrics)               │
│  ├─ Core Web Vitals Check (LCP < 2.5s, FID < 100ms, CLS < 0.1)  │
│  ├─ Bundle Size Verification (< 100kb first load)                │
│  ├─ SEO Completeness (metadata, sitemap, OpenGraph)              │
│  ├─ Vercel Deployment Readiness                                  │
│  └─ Final Architecture Review                                    │
│                                                                   │
│  Status: ✅ PRODUCTION READY                                      │
└──────────────────────────────────────────────────────────────────┘
                               ↓
┌──────────────────────────────────────────────────────────────────┐
│                     DEPLOYMENT PHASE                              │
│                                                                   │
│  ├─ Deploy to Vercel (vercel --prod)                             │
│  ├─ Configure custom domain                                      │
│  ├─ Set up environment variables                                 │
│  ├─ Enable analytics and monitoring                              │
│  └─ Verify production deployment                                 │
└──────────────────────────────────────────────────────────────────┘
```

## File Overview

### Skill Implementation (1,036 lines)
**Location:** `.cursor/skills/implement_new_project_vercel_nextjs_plan/SKILL.md`

**Key Features:**
- ✅ **Next.js-Specific Verification** - TypeScript, ESLint, build checks
- ✅ **Architecture Validation** - Uses nextjs-vercel-architect agent
- ✅ **Performance Checks** - Lighthouse, Core Web Vitals, bundle size
- ✅ **SEO Verification** - Metadata, sitemap, OpenGraph validation
- ✅ **Quality Enforcement** - Applies nextjs-vercel-standards.mdc rules
- ✅ **Two Execution Modes** - Direct (1-3 phases) or Orchestration (4+ phases)

**What It Does:**

#### Phase-by-Phase Implementation
Each phase goes through a rigorous process:
1. **Implement** - Following Next.js 15 best practices
2. **Verify** - TypeScript, ESLint, build, bundle size
3. **Validate** - Architecture review by expert agent
4. **Review** - Code quality check by review agent
5. **Fix** - Address issues (up to 3 iterations)
6. **Confirm** - Manual verification by user

#### Specialized Checks
- **TypeScript Strict Mode** - `npx tsc --noEmit` must pass
- **ESLint** - `npm run lint` must pass with no warnings
- **Next.js Build** - `npm run build` must succeed with optimizations
- **Bundle Analysis** - First load JS must be < 100kb
- **Route Optimization** - Verifies static vs dynamic rendering
- **Development Server** - No console errors or hydration warnings

#### Architecture Validation
After each phase, consults `nextjs-vercel-architect` agent to validate:
- Data fetching strategy (SSG/ISR/SSR decisions)
- Server vs Client Component boundaries
- Performance impact of changes
- Vercel optimization implementation
- SEO completeness

#### Final Validation
After all phases complete:
- **Lighthouse Audit** - All metrics 90+ required
- **Core Web Vitals** - LCP, FID, CLS must pass
- **Bundle Size** - Within budget from plan
- **SEO Check** - All metadata, sitemaps, OpenGraph
- **Vercel Ready** - Deployment configuration verified

### Documentation (744 lines)
**Location:** `.cursor/skills/implement_new_project_vercel_nextjs_plan/README.md`

**Comprehensive guide covering:**
- What makes this skill different
- When to use vs regular implementation
- Execution modes (Direct vs Orchestration)
- Verification checklist
- Phase-by-phase guide
- Example sessions
- Troubleshooting
- Advanced usage
- Integration with other skills

## Key Differences from Regular `/implement_plan`

| Aspect | `/implement_plan` | `/implement_new_project_vercel_nextjs_plan` |
|--------|------------------|---------------------------------------------|
| **Target** | Any project | Next.js 15+ with Vercel only |
| **Verification** | Generic tests | TypeScript, ESLint, Next.js build |
| **Architecture** | General patterns | nextjs-vercel-architect validation |
| **Performance** | Optional checks | Lighthouse, Core Web Vitals, bundle size |
| **SEO** | Not included | Comprehensive SEO verification |
| **Standards** | Framework-agnostic | nextjs-vercel-standards.mdc enforced |
| **Optimization** | General | Vercel-specific (SSG/ISR/Edge) |

## What It Validates

### 1. Next.js Build Quality
```bash
# TypeScript
npx tsc --noEmit
# Must pass: 0 errors

# ESLint
npm run lint
# Must pass: 0 errors, 0 warnings

# Next.js Build
npm run build
# Must succeed with:
# - Proper route indicators (○ ● ƒ)
# - Bundle size within budget
# - No warnings
```

### 2. Architecture Quality
Via `nextjs-vercel-architect` agent:
- ✅ Data fetching strategy correct (SSG/ISR/SSR)
- ✅ Component boundaries proper (Server/Client)
- ✅ Caching and revalidation configured
- ✅ Performance impact acceptable
- ✅ Vercel optimizations in place

### 3. Performance Quality
- ✅ Lighthouse Performance: 90+
- ✅ Lighthouse Accessibility: 100
- ✅ Lighthouse Best Practices: 100
- ✅ Lighthouse SEO: 100
- ✅ First Load JS: < 100kb
- ✅ LCP (Largest Contentful Paint): < 2.5s
- ✅ FID (First Input Delay): < 100ms
- ✅ CLS (Cumulative Layout Shift): < 0.1

### 4. SEO Quality
- ✅ Metadata API used on all pages
- ✅ Dynamic metadata for blog/dynamic pages
- ✅ Sitemap generated and accessible
- ✅ robots.txt configured
- ✅ OpenGraph tags on all pages
- ✅ Twitter Cards configured
- ✅ Structured data added (if applicable)

### 5. Code Quality
Via `task-review-agent`:
- ✅ TypeScript types proper (no `any`)
- ✅ Component patterns correct
- ✅ Error handling present
- ✅ Loading states implemented
- ✅ Standards compliance verified

### 6. Vercel Optimization
- ✅ Static generation maximized
- ✅ ISR configured appropriately
- ✅ Edge runtime used where beneficial
- ✅ Caching strategy correct
- ✅ Free tier optimized
- ✅ Environment variables documented

## Execution Modes

### Direct Implementation (1-3 Phases)
```
User: /implement_new_project_vercel_nextjs_plan thoughts/shared/plans/simple-site.md

AI: Plan has 3 phases. Using direct implementation.

Phase 1: Foundation & Core Setup
[implements in main context]
✓ TypeScript passed
✓ Build successful (78 KB)
✓ Architecture validated
Ready for manual verification...

[continues with phases 2 and 3]

All phases complete!
✅ PRODUCTION READY
```

**Benefits:**
- Faster for small projects
- Single context
- Direct communication

### Agent Orchestration (4+ Phases)
```
User: /implement_new_project_vercel_nextjs_plan thoughts/shared/plans/full-site.md

AI: Plan has 5 phases. Using agent orchestration.

Creating ledger: thoughts/ledgers/full-site.md
Creating handoffs: thoughts/handoffs/full-site/

─────────────────────────────────────
Phase 1 of 5: Foundation & Core Setup
─────────────────────────────────────

📝 Implementing (implement_task agent)...
🔨 Building (npm run build)...
🏗️ Validating (nextjs-vercel-architect)...
🔍 Reviewing (task-review-agent)...

✅ Phase 1 complete
Handoff: thoughts/handoffs/full-site/phase-01-foundation.md

Ready for manual verification. Type 'continue' when ready.

[continues with phases 2-5]
```

**Benefits:**
- Compaction-resistant
- Fresh context per phase
- Automatic quality loops
- Detailed progress tracking

## Integration with Planning Skill

```
Step 1: Plan
───────────
/create_new_project_vercel_nextjs_plan

├─ Analyzes template
├─ Requirements interview
├─ Architecture decisions (nextjs-vercel-architect)
├─ Creates 5-phase plan
└─ Output: thoughts/shared/plans/YYYY-MM-DD-project.md

Step 2: Implement (This Skill!)
────────────────────────────────
/implement_new_project_vercel_nextjs_plan thoughts/shared/plans/YYYY-MM-DD-project.md

For each phase:
├─ Implement with Next.js 15 patterns
├─ Verify with TypeScript/ESLint/Build
├─ Validate with nextjs-vercel-architect
├─ Review with task-review-agent
├─ Fix issues (max 3 iterations)
└─ Manual verification

Final validation:
├─ Lighthouse audit
├─ Core Web Vitals
├─ Bundle size check
├─ SEO verification
└─ Vercel deployment readiness

Step 3: Deploy
──────────────
vercel --prod

├─ Environment variables
├─ Custom domain
├─ Analytics setup
└─ Monitoring
```

## Quality Standards Enforced

Every implementation ensures:

### Build Standards
- ✅ TypeScript compiles with no errors
- ✅ ESLint passes with no warnings
- ✅ Next.js builds successfully
- ✅ No console errors in production

### Architecture Standards
- ✅ App Router only (no Pages Router)
- ✅ Server Components by default
- ✅ Client Components minimal and justified
- ✅ Proper data fetching strategy
- ✅ Correct caching configuration

### Performance Standards
- ✅ Lighthouse scores 90+ on all metrics
- ✅ First Load JS < 100kb
- ✅ Core Web Vitals pass
- ✅ Images optimized (next/image)
- ✅ Fonts optimized (next/font)

### SEO Standards
- ✅ Metadata on every page
- ✅ Sitemap generated
- ✅ OpenGraph tags present
- ✅ Social sharing configured
- ✅ Structured data (when applicable)

### Code Standards
- ✅ TypeScript strict mode
- ✅ No `any` types
- ✅ Proper error handling
- ✅ Loading states present
- ✅ Follows nextjs-vercel-standards.mdc

### Vercel Standards
- ✅ Static generation maximized (free tier)
- ✅ Edge runtime where appropriate
- ✅ Proper caching strategy
- ✅ Environment variables documented
- ✅ Deployment configuration correct

## Success Metrics

After implementation, you get:

### Build Report
```
Next.js Build Report
===================
Status: ✅ SUCCESS
First Load JS: 94 KB (target: < 100 KB)
Static Routes: 12
ISR Routes: 8
Bundle within budget: ✓
```

### Performance Report
```
Lighthouse Scores
================
Performance: 94/100 ✓
Accessibility: 100/100 ✓
Best Practices: 100/100 ✓
SEO: 100/100 ✓

Core Web Vitals:
LCP: 1.8s ✓
FID: 45ms ✓
CLS: 0.05 ✓
```

### Architecture Report
```
Architecture Review
==================
Data Fetching: ✅ APPROVED
Component Architecture: ✅ APPROVED
Performance: ✅ APPROVED
Vercel Optimization: ✅ APPROVED
SEO: ✅ APPROVED

Status: ✅ PRODUCTION READY
```

## Files Created During Implementation

```
thoughts/
├── ledgers/
│   └── project-name.md          # Continuity ledger
│       ├─ Goal and tech stack
│       ├─ Performance targets
│       ├─ Architecture decisions
│       └─ Progress tracking
│
└── handoffs/
    └── project-name/
        ├── phase-01-foundation.md     # Phase 1 handoff
        ├── phase-02-content.md        # Phase 2 handoff
        ├── phase-03-features.md       # Phase 3 handoff
        ├── phase-04-performance.md    # Phase 4 handoff
        └── phase-05-deployment.md     # Phase 5 handoff
        
Each handoff contains:
├─ Phase summary
├─ Files modified
├─ Architecture validation results
├─ Review history
├─ Issues found and fixed
└─ Manual verification items
```

## Common Use Cases

### SaaS Landing Page (3 phases)
```
Direct Mode:
- Phase 1: Foundation (30 min)
- Phase 2: Landing pages (45 min)
- Phase 3: Forms and deployment (30 min)

Total: ~2 hours
Result: Production-ready landing page
```

### Full SaaS Platform (5 phases)
```
Orchestration Mode:
- Phase 1: Foundation (45 min)
- Phase 2: Content architecture (1 hour)
- Phase 3: Features & functionality (2 hours)
- Phase 4: Performance & polish (1 hour)
- Phase 5: Deployment & launch (45 min)

Total: ~5.5 hours
Result: Complete SaaS platform
```

### E-commerce Store (5 phases)
```
Orchestration Mode:
- Phase 1: Foundation (45 min)
- Phase 2: Product catalog (1.5 hours)
- Phase 3: Shopping cart & checkout (2 hours)
- Phase 4: User accounts (1 hour)
- Phase 5: Optimization & deployment (1 hour)

Total: ~6 hours
Result: Full e-commerce site
```

## Why This Skill?

### Without This Skill
```
❌ Manual verification of Next.js patterns
❌ Easy to miss performance issues
❌ No architecture validation
❌ SEO often forgotten
❌ Bundle size grows unchecked
❌ Vercel optimization missed
❌ Technical debt accumulates
❌ No systematic quality checks
```

### With This Skill
```
✅ Automatic Next.js build verification
✅ Performance checked every phase
✅ Architecture validated by expert agent
✅ SEO verified comprehensively
✅ Bundle size enforced strictly
✅ Vercel optimizations built-in
✅ Quality enforced from day one
✅ Production-ready guarantee
```

## Integration Points

### Uses These Agents
- **`nextjs-vercel-architect`** - Architecture validation
- **`task-review-agent`** - Code quality review
- **`implement_task`** - Phase implementation (orchestration mode)

### Applies These Rules
- **`nextjs-vercel-standards.mdc`** - Next.js 15 coding standards

### Reads These Plans
- **From:** `thoughts/shared/plans/YYYY-MM-DD-nextjs-*.md`
- **Created by:** `/create_new_project_vercel_nextjs_plan`

### Creates These Artifacts
- **Ledger:** `thoughts/ledgers/project-name.md`
- **Handoffs:** `thoughts/handoffs/project-name/phase-NN-*.md`
- **Build reports**
- **Performance reports**
- **Architecture reviews**

## The Complete Toolchain

```
Planning:
/create_new_project_vercel_nextjs_plan
├─ Template analysis
├─ Requirements gathering
├─ Architecture decisions
└─ Comprehensive plan

           ↓

Implementation: (This Skill!)
/implement_new_project_vercel_nextjs_plan
├─ Phase-by-phase execution
├─ Build verification
├─ Architecture validation
├─ Code review
├─ Fix loops
└─ Final validation

           ↓

Deployment:
vercel --prod
├─ Environment setup
├─ Domain configuration
├─ Analytics enabling
└─ Monitoring setup
```

## What You Get

### Immediately
- ✅ Next.js 15 project built correctly
- ✅ App Router patterns enforced
- ✅ Performance targets met
- ✅ SEO fully configured
- ✅ Vercel optimized
- ✅ Production-ready code

### Long Term
- ✅ Maintainable codebase
- ✅ Scalable architecture
- ✅ Low Vercel costs
- ✅ Great Core Web Vitals
- ✅ Strong SEO foundation
- ✅ Quality standards established

## Quick Reference

### Invocation
```bash
/implement_new_project_vercel_nextjs_plan thoughts/shared/plans/YYYY-MM-DD-project.md
```

### Prerequisites
- Next.js 15+ project
- Plan from `/create_new_project_vercel_nextjs_plan`
- TypeScript configured
- App Router structure

### Output
- Ledger with progress tracking
- Handoffs for each phase (orchestration mode)
- Build reports
- Performance reports
- Architecture validation
- Production-ready application

### Success Criteria
- ✅ All phases complete
- ✅ All automated checks pass
- ✅ All architecture validations pass
- ✅ All code reviews pass
- ✅ All manual verifications confirmed
- ✅ Final validation complete
- ✅ Status: PRODUCTION READY

## Support

### Documentation
- **Skill Details:** `.cursor/skills/implement_new_project_vercel_nextjs_plan/SKILL.md`
- **Usage Guide:** `.cursor/skills/implement_new_project_vercel_nextjs_plan/README.md`
- **Architect Agent:** `.cursor/agents/nextjs-vercel-architect.md`
- **Coding Standards:** `.cursor/rules/nextjs-vercel-standards.mdc`

### Related Skills
- **Planning:** `/create_new_project_vercel_nextjs_plan`
- **General Implementation:** `/implement_plan`
- **Task Implementation:** `/implement_task`

---

**Build with confidence. Ship with quality. Scale with Vercel. 🚀**
