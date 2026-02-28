# Implement Next.js + Vercel Project Plan

Specialized implementation skill for executing Next.js + Vercel project plans created by `/create_new_project_vercel_nextjs_plan`.

## What Makes This Different

This skill is specifically designed for Next.js 15+ projects and includes:

### Next.js-Specific Verification
- ✅ TypeScript strict mode checking (`npx tsc --noEmit`)
- ✅ ESLint verification (`npm run lint`)
- ✅ Next.js build validation (`npm run build`)
- ✅ Bundle size analysis
- ✅ Route optimization checking (static vs dynamic)
- ✅ Development server verification

### Architecture Validation
- ✅ Uses `nextjs-vercel-architect` agent for expert review
- ✅ Validates data fetching strategy (SSG/ISR/SSR)
- ✅ Checks Server vs Client Component boundaries
- ✅ Verifies caching and revalidation setup
- ✅ Ensures Vercel optimization best practices

### Performance Checks
- ✅ Lighthouse audits (90+ required)
- ✅ Core Web Vitals monitoring (LCP, FID, CLS)
- ✅ Bundle size budget enforcement (< 100kb first load)
- ✅ Image optimization verification (next/image)
- ✅ Font optimization verification (next/font)

### SEO Verification
- ✅ Metadata API usage check
- ✅ Sitemap generation verification
- ✅ OpenGraph tags validation
- ✅ robots.txt configuration
- ✅ Structured data validation (if applicable)

### Standards Enforcement
- ✅ Applies `nextjs-vercel-standards.mdc` rules
- ✅ Enforces App Router patterns (no Pages Router)
- ✅ Validates Server Component defaults
- ✅ Checks TypeScript strict mode compliance
- ✅ Verifies accessibility standards (WCAG AA)

## When to Use

Use this skill when:
- ✅ Implementing a plan created by `/create_new_project_vercel_nextjs_plan`
- ✅ Building a **new** Next.js 15+ project
- ✅ Deploying to Vercel
- ✅ Need architecture validation during implementation
- ✅ Want performance and SEO checks built-in

**Don't use for:**
- ❌ Existing/legacy Next.js projects (use regular `/implement_plan`)
- ❌ Pages Router projects
- ❌ Non-Next.js projects
- ❌ Quick bug fixes (use regular `/implement_plan`)

## How to Use

### Basic Usage

```bash
# In Cursor chat
/implement_new_project_vercel_nextjs_plan thoughts/shared/plans/2026-02-11-nextjs-saas-landing.md
```

### The Implementation Process

```
1. Verify Setup
   ├─ Check it's a Next.js + Vercel plan
   ├─ Verify Next.js installation
   ├─ Check App Router structure
   └─ Read plan completely

2. Create Ledger (if needed)
   ├─ Extract phases from plan
   ├─ Note performance targets
   ├─ Track architecture decisions
   └─ Document technology stack

3. For Each Phase:
   │
   ├─ Implement
   │  ├─ Follow Next.js 15 patterns
   │  ├─ Apply standards rules
   │  └─ Respect architecture decisions
   │
   ├─ Verify Build
   │  ├─ TypeScript check
   │  ├─ ESLint check
   │  ├─ Next.js build
   │  └─ Bundle size check
   │
   ├─ Validate Architecture
   │  ├─ Consult nextjs-vercel-architect
   │  ├─ Verify data fetching strategy
   │  ├─ Check component boundaries
   │  └─ Confirm optimizations
   │
   ├─ Review Code Quality
   │  ├─ Spawn task-review-agent
   │  ├─ Check for issues
   │  └─ Fix if needed (max 3 iterations)
   │
   └─ Manual Verification
      ├─ Test in browser
      ├─ Check responsiveness
      ├─ Verify functionality
      └─ Confirm with user

4. Final Validation
   ├─ Run Lighthouse audit
   ├─ Check Core Web Vitals
   ├─ Final architecture review
   ├─ SEO verification
   └─ Deployment readiness check
```

## Execution Modes

### Mode 1: Direct Implementation
**For:** Small plans (3 or fewer phases)

```
User: /implement_new_project_vercel_nextjs_plan thoughts/shared/plans/simple-site.md

AI: This plan has 3 phases. I'll implement directly.

Phase 1: Foundation & Core Setup
[implements directly in main context]
✓ TypeScript check passed
✓ Build successful
✓ Architecture validated
Ready for manual verification...

[continues with phases 2 and 3]
```

**Benefits:**
- Faster for small projects
- Single context, easier to follow
- Direct communication

### Mode 2: Agent Orchestration
**For:** Larger plans (4+ phases), complex projects

```
User: /implement_new_project_vercel_nextjs_plan thoughts/shared/plans/full-saas-site.md

AI: This plan has 5 phases. I'll use agent orchestration.

Creating ledger: thoughts/ledgers/full-saas-site.md
Creating handoff directory: thoughts/handoffs/full-saas-site/

────────────────────────────────────────────────
Phase 1 of 5: Foundation & Core Setup
────────────────────────────────────────────────

📝 Implementing...
[spawns implement_task agent]

🔨 Building...
[npm run build]

🏗️ Validating architecture...
[spawns nextjs-vercel-architect]

🔍 Reviewing code...
[spawns task-review-agent]

✅ Phase 1 complete
Handoff: thoughts/handoffs/full-saas-site/phase-01-foundation.md

Ready for manual verification. Type 'continue' when ready.
```

**Benefits:**
- Compaction-resistant (handoffs persist)
- Each phase fresh context
- Automatic quality checks
- Detailed progress tracking

## Verification Checklist

After each phase, these checks run automatically:

### Build Quality
```bash
# 1. TypeScript
npx tsc --noEmit
# Must pass: No errors

# 2. Linting
npm run lint
# Must pass: No errors or warnings

# 3. Build
npm run build
# Must succeed with optimization
```

### Architecture Quality
- Consults `nextjs-vercel-architect` agent
- Validates data fetching strategy
- Checks component boundaries
- Verifies performance impact

### Code Quality
- Spawns `task-review-agent`
- Checks for issues (MUST_FIX, SHOULD_FIX, NIT)
- Requires fixes before proceeding
- Max 3 fix iterations

### Manual Quality
- Browser testing required
- Responsive design check
- Functionality verification
- User confirmation needed

## Example Session

### Small Project (Direct Mode)

```
User: /implement_new_project_vercel_nextjs_plan thoughts/shared/plans/2026-02-11-portfolio.md

AI: Analyzing plan...
✓ Next.js 15.1.0 detected
✓ App Router structure found  
✓ 3 phases identified

Creating ledger: thoughts/ledgers/portfolio.md

Starting direct implementation...

─────────────────────────────────────
Phase 1: Foundation & Core Setup
─────────────────────────────────────

Implementing:
- next.config.mjs updated
- tailwind.config.ts configured
- RootLayout created with fonts
- Header and Footer components

Verifying...
✓ TypeScript check passed
✓ ESLint passed
✓ Build successful (First Load: 72 KB)

Architecture validation...
✓ Server Components used correctly
✓ Fonts optimized with next/font
✓ Metadata API configured
Status: ✅ APPROVED

Manual verification needed:
- Check design system renders
- Verify responsive layout
- Test navigation

Ready to continue? Type 'yes' or review code first.

User: yes

[continues with phases 2 and 3...]

─────────────────────────────────────
All Phases Complete
─────────────────────────────────────

Final verification...

Build Report:
- Status: ✅ SUCCESS
- First Load JS: 82 KB
- Static pages: 5
- Bundle within budget ✓

Lighthouse Scores:
- Performance: 96/100 ✓
- Accessibility: 100/100 ✓
- Best Practices: 100/100 ✓
- SEO: 100/100 ✓

Architecture Review:
- Data fetching: ✅ APPROVED
- Components: ✅ APPROVED
- Performance: ✅ APPROVED
- Vercel optimization: ✅ APPROVED

Status: ✅ PRODUCTION READY

Next steps:
1. Deploy to Vercel: `vercel`
2. Add environment variables
3. Configure custom domain
4. Enable analytics

Your portfolio is ready to launch! 🚀
```

### Large Project (Orchestration Mode)

```
User: /implement_new_project_vercel_nextjs_plan thoughts/shared/plans/2026-02-11-saas-platform.md

AI: Analyzing plan...
✓ Next.js 15.1.0 with App Router
✓ 5 phases with multiple features
✓ Performance targets: 90+ Lighthouse

Using agent orchestration mode for quality.

Setup:
- Ledger: thoughts/ledgers/saas-platform.md
- Handoffs: thoughts/handoffs/saas-platform/

────────────────────────────────────────────────
Phase 1 of 5: Foundation & Core Setup
────────────────────────────────────────────────

📝 Implementing (implement_task agent)...
[Agent works in isolated context]
[Creates: thoughts/handoffs/saas-platform/phase-01-foundation.md]

🔨 Building Next.js...
$ npm run build
✓ Success (First Load: 78 KB)

🏗️ Architecture validation (nextjs-vercel-architect)...
Checking:
- RootLayout pattern ✓
- Font optimization ✓
- Metadata API ✓
- Component structure ✓
- Performance budget ✓

Result: ✅ APPROVED

🔍 Code review (task-review-agent)...
Checking:
- TypeScript types ✓
- Component patterns ✓
- Error handling ✓
- Standards compliance ✓

Result: ✅ APPROVED (no issues)

✅ Phase 1 Complete
Handoff saved: thoughts/handoffs/saas-platform/phase-01-foundation.md

Manual verification:
- [ ] Design system renders correctly
- [ ] Responsive on all devices
- [ ] Fonts load without flash
- [ ] Navigation functional

Type 'continue' when ready for Phase 2.

User: continue

────────────────────────────────────────────────
Phase 2 of 5: Content Architecture
────────────────────────────────────────────────

📝 Implementing...
[Reading previous handoff for context]
[Implementing pages and routing]
[Creates: thoughts/handoffs/saas-platform/phase-02-content.md]

🔨 Building...
$ npm run build

Route Analysis:
┌ ○ /                          5.2 KB    85 KB
├ ○ /about                     1.8 KB    82 KB  
├ ○ /pricing                   2.1 KB    83 KB
├ ● /blog                      1.5 KB    81 KB
└ ƒ /blog/[slug]              3.2 KB    88 KB

○ Static ✓
● SSG ✓
ƒ ISR (1h revalidation) ✓

Bundle within budget ✓

🏗️ Architecture validation...
Checking data fetching strategy...
- Homepage: SSG ✓ (correct choice)
- Blog posts: ISR with 3600s ✓ (matches plan)
- generateStaticParams used ✓
- Metadata API for dynamic pages ✓

Result: ✅ APPROVED

🔍 Code review...
Found 2 issues:

Iteration 1:
1. [SHOULD_FIX] app/blog/[slug]/page.tsx:12
   Consider adding error boundary for post not found
   
2. [NIT] app/blog/page.tsx:8
   Add loading skeleton component

🔧 Fixing (iteration 2)...
[implement_task agent addresses feedback]
[Updates handoff]

🔍 Re-reviewing...
Result: ✅ APPROVED (all issues addressed)

✅ Phase 2 Complete after 2 iterations
Handoff: thoughts/handoffs/saas-platform/phase-02-content.md

Manual verification:
- [ ] All pages load correctly
- [ ] Blog posts render with metadata
- [ ] Links work properly
- [ ] Responsive on mobile

Type 'continue' when ready for Phase 3.

[continues through phases 3, 4, and 5...]

────────────────────────────────────────────────
All Phases Complete - Final Validation
────────────────────────────────────────────────

Running comprehensive checks...

Build Report:
============
✓ TypeScript: 0 errors
✓ ESLint: 0 warnings
✓ Build: SUCCESS (42.3s)
✓ First Load JS: 94 KB (target: < 100 KB)
✓ Static Routes: 12
✓ ISR Routes: 8
✓ Dynamic Routes: 2

Lighthouse Audit:
================
Homepage:
- Performance: 94/100 ✓
- Accessibility: 100/100 ✓
- Best Practices: 100/100 ✓
- SEO: 100/100 ✓

Blog Post:
- Performance: 92/100 ✓
- Accessibility: 100/100 ✓
- Best Practices: 100/100 ✓
- SEO: 100/100 ✓

Core Web Vitals:
- LCP: 1.8s ✓ (target: < 2.5s)
- FID: 45ms ✓ (target: < 100ms)  
- CLS: 0.05 ✓ (target: < 0.1)

Architecture Review:
===================
Final validation by nextjs-vercel-architect...

✅ Data Fetching Strategy: APPROVED
   - 85% static pages (excellent for free tier)
   - ISR configured appropriately
   - No unnecessary dynamic rendering

✅ Component Architecture: APPROVED
   - Server Components: 38 files
   - Client Components: 9 files (justified)
   - Proper boundaries maintained

✅ Performance: APPROVED
   - Bundle size within budget
   - Images optimized (AVIF fallback)
   - Fonts optimized (next/font)
   - No performance anti-patterns

✅ Vercel Optimization: APPROVED
   - Free tier maximized
   - Edge middleware for auth
   - Caching strategy correct
   - Estimated usage: ~150 function executions/month

✅ SEO: APPROVED
   - Metadata on all pages
   - Sitemap generated
   - OpenGraph tags present
   - robots.txt configured

Overall Status: ✅ PRODUCTION READY

Implementation Summary:
======================
- Phases completed: 5/5
- Total handoffs: 5
- Review iterations: 7 (avg 1.4 per phase)
- Issues found: 12
- Issues fixed: 12
- Time: ~3 hours

Your SaaS platform is ready to deploy! 🎉

Next Steps:
===========

Deployment Checklist:
- [ ] Add environment variables to Vercel
- [ ] Configure custom domain  
- [ ] Set up Vercel Analytics
- [ ] Configure error tracking (Sentry)
- [ ] Test on Vercel preview deployment
- [ ] Deploy to production

Post-Launch:
- [ ] Submit sitemap to Google Search Console
- [ ] Monitor Core Web Vitals in Search Console
- [ ] Watch Vercel Analytics daily
- [ ] Monitor error rates
- [ ] Gather user feedback

Monitoring:
- Vercel Dashboard: usage, errors, performance
- Google Search Console: SEO, indexing
- Lighthouse CI: ongoing performance checks

Deploy command:
$ vercel --prod

Congratulations! 🚀
```

## Configuration

### Required Directory Structure

```bash
thoughts/
├── shared/
│   └── plans/              # Plans from create_new_project_vercel_nextjs_plan
├── ledgers/                # Continuity ledgers
└── handoffs/               # Phase handoffs (orchestration mode)
    └── <session-name>/
        ├── phase-01-*.md
        ├── phase-02-*.md
        └── ...
```

### Environment Check

Before implementation, ensure:

```bash
# Next.js installed
npm list next

# TypeScript configured  
cat tsconfig.json

# ESLint configured
cat .eslintrc.json

# App Router present
ls -la app/
```

## Troubleshooting

### "This doesn't look like a Next.js + Vercel plan"

**Problem:** Skill detected plan wasn't created for Next.js + Vercel

**Solution:**
- Use regular `/implement_plan` for other projects
- Or specify it's a Next.js project and continue
- Verify plan has Next.js-specific content

### Build Fails with TypeScript Errors

**Problem:** `npx tsc --noEmit` returns errors

**Solution:**
- Fix errors immediately (never use `any`)
- Check for Server Component using client hooks
- Verify async params are awaited
- Ensure 'use client' on interactive components

### Bundle Size Exceeds Budget

**Problem:** First Load JS > 100kb

**Solution:**
```bash
# Analyze bundle
npx @next/bundle-analyzer

# Common fixes:
# 1. Dynamic import heavy components
# 2. Remove unused dependencies
# 3. Check for duplicate packages
# 4. Minimize client-side JS
```

### Lighthouse Score Too Low

**Problem:** Performance < 90

**Solution:**
- Check LCP (hero image optimized?)
- Check CLS (layout shifts?)
- Check TBT (blocking JavaScript?)
- Verify next/image used
- Verify next/font used
- Minimize client components

### Architecture Validation Failed

**Problem:** nextjs-vercel-architect finds issues

**Solution:**
- Read specific concerns carefully
- Understand the recommendation
- Implement suggested fix
- Re-validate architecture
- Ask architect agent for clarification if needed

## Advanced Usage

### Custom Verification Scripts

Add to `package.json`:

```json
{
  "scripts": {
    "verify": "npm run type-check && npm run lint && npm run build",
    "type-check": "tsc --noEmit",
    "lint": "next lint",
    "build": "next build",
    "analyze": "ANALYZE=true next build"
  }
}
```

### Performance Monitoring

```bash
# During implementation
npm run build | tee build-output.txt

# Check specific pages
curl http://localhost:3000 | grep -o '<link.*' | wc -l

# Bundle analysis
ANALYZE=true npm run build
```

### SEO Verification

```bash
# Check sitemap
curl http://localhost:3000/sitemap.xml

# Check robots.txt
curl http://localhost:3000/robots.txt

# Check metadata (view source)
curl http://localhost:3000 | grep -i 'meta'
```

## Integration with Other Skills

### Before Implementation

```
1. Plan → /create_new_project_vercel_nextjs_plan
2. Validate → Use nextjs-vercel-architect (included in this skill)
3. Implement → /implement_new_project_vercel_nextjs_plan
```

### During Implementation

- Automatically uses `nextjs-vercel-architect` for validation
- Automatically uses `task-review-agent` for code review
- Applies `nextjs-vercel-standards.mdc` rules

### After Implementation

```
1. Deploy → Vercel
2. Monitor → Vercel Analytics + Search Console
3. Iterate → Based on real-world data
```

## Tips for Success

### 1. Trust the Process
- Let verification run completely
- Don't skip architecture validation
- Fix issues immediately

### 2. Watch Bundle Size
- Check after each phase
- Dynamic import when needed
- Remove unused deps

### 3. Test Responsively
- Mobile, tablet, desktop
- Check all breakpoints
- Verify touch interactions

### 4. Performance First
- Images via next/image
- Fonts via next/font
- Minimal client JS
- Server Components default

### 5. SEO Always
- Metadata on every page
- Meaningful descriptions
- OpenGraph images
- Structured data

## Support

### Documentation
- Skill: `.cursor/skills/implement_new_project_vercel_nextjs_plan/SKILL.md`
- Architect: `.cursor/agents/nextjs-vercel-architect.md`
- Standards: `.cursor/rules/nextjs-vercel-standards.mdc`

### Resources
- Next.js Docs: https://nextjs.org/docs
- Vercel Docs: https://vercel.com/docs
- Lighthouse: https://developers.google.com/web/tools/lighthouse

---

**Build with confidence. Deploy with pride. 🚀**
