# Create New Project Vercel Next.js Plan

A specialized planning skill for **new Next.js projects deployed on Vercel**. This skill helps you create comprehensive implementation plans optimized for greenfield Next.js 15+ applications.

## When to Use

Use this skill when:
- ✅ Starting a **new** Next.js project from scratch or template
- ✅ Planning a website to be deployed on **Vercel**
- ✅ Want a complete plan covering architecture, performance, SEO, and deployment
- ✅ Need guidance on Next.js 15+ App Router best practices
- ✅ Want to maximize Vercel's free tier

**Don't use this skill for:**
- ❌ Existing/legacy projects (use regular `/create_plan` instead)
- ❌ Non-Next.js projects
- ❌ Quick feature additions to established apps

## What Makes This Different from `/create_plan`

| Aspect | `/create_plan` | `/create_new_project_vercel_nextjs_plan` |
|--------|---------------|------------------------------------------|
| **Target** | Any project | Next.js + Vercel specifically |
| **Focus** | General implementation | Architecture, performance, SEO, deployment |
| **Optimizations** | General best practices | Vercel-specific optimizations |
| **Starting Point** | Existing codebase | Fresh Next.js template |
| **Guidance** | Framework-agnostic | Next.js 15+ App Router patterns |

## What You Get

A comprehensive plan that includes:

### 1. **Technology Stack Decisions**
- Next.js configuration
- Styling framework (Tailwind, component libraries)
- Database and ORM (if needed)
- Authentication solution (if needed)
- CMS integration (if needed)
- Analytics setup

### 2. **Architecture Design**
- Server vs Client Component boundaries
- Data fetching strategy (SSG/ISR/SSR)
- Caching and revalidation approach
- API routes vs Server Actions
- Edge runtime usage

### 3. **Performance Optimization**
- Image optimization strategy
- Font loading strategy
- Code splitting approach
- Bundle size targets
- Core Web Vitals goals

### 4. **SEO Strategy**
- Metadata configuration
- Sitemap generation
- OpenGraph and Twitter Cards
- Structured data (JSON-LD)
- robots.txt setup

### 5. **Vercel Deployment**
- Free tier optimization tactics
- Environment variables setup
- Domain configuration
- Build optimization
- Monitoring strategy

### 6. **Quality Standards**
- TypeScript strict mode
- Accessibility (WCAG AA)
- Testing strategy
- ESLint/Prettier setup

## How to Use

### Quick Start

In any Cursor chat:

```
/create_new_project_vercel_nextjs_plan
```

Then follow the interactive prompts to describe your project.

### With Requirements File

If you have a requirements document:

```
/create_new_project_vercel_nextjs_plan requirements.md
```

### Example Session

```
User: /create_new_project_vercel_nextjs_plan

AI: I'll help you plan your Next.js + Vercel website. Let me understand what you're building.

Please provide:
1. Project Overview: What type of website?
2. Key Features: Main pages and functionality?
3. Design Requirements: UI/UX considerations?
4. Content Strategy: Static, CMS, or dynamic data?
5. Target Audience: Who and what devices?

User: I want to build a SaaS landing page with a blog, pricing page, 
      waitlist form, and documentation. Design should be modern with 
      Tailwind. Content will be MDX for blog and docs. Target is B2B 
      developers on desktop and mobile.

AI: [Analyzes your Next.js template, asks clarifying questions, 
     creates comprehensive plan...]
```

## What the Skill Does

### Step 1: Template Analysis
- Reads your `package.json` and `next.config.js`
- Maps your current directory structure
- Identifies pre-configured features
- Recommends additions

### Step 2: Architecture Decisions
- Uses `nextjs-vercel-architect` agent for validation
- Determines data fetching strategy per page
- Plans component architecture
- Designs caching strategy

### Step 3: Deep Requirements Interview
- Asks detailed questions using `AskQuestion` tool
- Covers content, UX, data, performance, SEO, deployment
- Continues until zero ambiguity
- Documents all decisions with rationale

### Step 4: Vercel Optimization
- Maximizes static generation
- Plans Edge runtime usage
- Optimizes for free tier
- Configures deployment settings

### Step 5: Plan Writing
- Creates detailed 5-phase plan:
  1. **Foundation & Core Setup** - Config, design system, layouts
  2. **Content Architecture** - Content modeling, routes, pages
  3. **Features & Functionality** - Interactive components, APIs
  4. **Performance & Polish** - Optimization, accessibility, analytics
  5. **Deployment & Launch** - Vercel setup, domain, monitoring

### Step 6: Review & Iteration
- Presents draft plan for feedback
- Iterates based on your input
- Finalizes when you're satisfied

## Output

Your plan will be saved to:
```
thoughts/shared/plans/YYYY-MM-DD-nextjs-project-name.md
```

## Quality Standards Enforced

Every plan ensures:
- ✅ **App Router Only** - No Pages Router
- ✅ **Server Components by Default** - Client only when needed
- ✅ **TypeScript Strict** - Full type safety
- ✅ **Performance First** - < 100kb first load JS
- ✅ **Static When Possible** - Minimize Vercel costs
- ✅ **SEO Native** - Metadata on all pages
- ✅ **Accessibility Required** - WCAG AA compliance
- ✅ **Cost-Effective** - Optimized for free tier

## Related Resources

### Agents Used by This Skill
- **`nextjs-vercel-architect`** - Validates Next.js + Vercel architecture decisions
- **`codebase-locator`** - Maps template structure
- **`codebase-analyzer`** - Understands existing patterns

### Rules Applied
- **`nextjs-vercel-standards.mdc`** - Next.js 15 + Vercel coding standards

### Follow-Up Skills
After planning, use:
- **`/implement_plan`** - Execute the plan with task tracking

## Examples

### SaaS Landing Page

```
/create_new_project_vercel_nextjs_plan

Type: SaaS Landing Page
Features: Hero, Features, Pricing, Testimonials, Waitlist Form, Blog
Design: Modern, Tailwind, Dark Mode
Content: MDX for blog
Target: B2B professionals, mobile + desktop

Result: 5-phase plan with:
- Static pages (SSG)
- Blog with ISR
- Waitlist form with Server Actions
- Email integration
- Vercel Analytics
- SEO optimized
```

### E-commerce Store

```
/create_new_project_vercel_nextjs_plan

Type: E-commerce
Features: Product catalog, product pages, cart, checkout, order tracking
Design: Tailwind + shadcn/ui
Content: Products from Shopify API
Target: General consumers, mobile-first

Result: 5-phase plan with:
- Product listing (SSG)
- Product detail pages (ISR)
- Cart (client state)
- Checkout (Stripe integration)
- Order API routes
- Performance optimized
```

### Technical Blog

```
/create_new_project_vercel_nextjs_plan

Type: Developer Blog
Features: Blog posts, tags, search, RSS, code highlighting
Design: Minimal, great typography
Content: MDX with frontmatter
Target: Developers, primarily desktop

Result: 5-phase plan with:
- MDX setup with plugins
- Static blog generation
- Tag pages (SSG)
- Search with FlexSearch
- RSS feed generation
- Code syntax highlighting
- Reading time calculation
```

## Tips for Best Results

1. **Be Specific**: The more details you provide, the better the plan
2. **Know Your Content Strategy**: Static vs dynamic is crucial for optimization
3. **Define Your MVP**: Start with core features, plan future phases
4. **Consider Your Skills**: Mention if you're new to Next.js for more guidance
5. **Budget Matters**: Specify if you want to stay on free tier

## Troubleshooting

### "I don't have a Next.js template yet"

Run this first:
```bash
npx create-next-app@latest my-app
cd my-app
```

Then invoke the skill.

### "The plan is too complex"

Ask the AI to:
- Simplify the phasing
- Focus on MVP first
- Remove optional features

### "I need to change technologies mid-planning"

Just tell the AI:
- "Actually, let's use X instead of Y"
- The AI will re-research and update the plan

### "Where's my plan?"

Check:
```
thoughts/shared/plans/YYYY-MM-DD-nextjs-project-name.md
```

## Contributing

Found a pattern that should be included? Update:
- Skill: `.cursor/skills/create_new_project_vercel_nextjs_plan/SKILL.md`
- Agent: `.cursor/agents/nextjs-vercel-architect.md`
- Rules: `.cursor/rules/nextjs-vercel-standards.mdc`

## Support

Questions? Issues?
1. Check the plan output - it includes references and rationale
2. Review Next.js 15 docs: https://nextjs.org/docs
3. Review Vercel docs: https://vercel.com/docs
4. Ask the AI to explain any recommendation

---

**Built for quality. Optimized for Vercel. Ready for production.**
