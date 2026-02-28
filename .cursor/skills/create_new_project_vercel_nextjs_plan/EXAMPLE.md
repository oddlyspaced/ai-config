# Example Usage

## Quick Start Example

### Scenario: Building a SaaS Landing Page

**Starting Point:** Fresh Next.js 15 project from `create-next-app`

```bash
npx create-next-app@latest my-saas --typescript --tailwind --app --src-dir=false
cd my-saas
```

### Step 1: Invoke the Skill

In Cursor chat:

```
/create_new_project_vercel_nextjs_plan
```

### Step 2: Respond to Initial Questions

**AI Asks:**
```
I'll help you plan your Next.js + Vercel website. Let me understand what you're building.

Please provide:
1. Project Overview: What type of website?
2. Key Features: Main pages and functionality?
3. Design Requirements: UI/UX considerations?
4. Content Strategy: Static, CMS, or dynamic data?
5. Target Audience: Who and what devices?
```

**You Respond:**
```
1. SaaS landing page for a project management tool
2. Features:
   - Homepage with hero, features, pricing, testimonials
   - /pricing page with three tiers
   - /blog for content marketing (MDX)
   - /docs for product documentation (MDX)
   - Waitlist signup form
   - Contact form
3. Design: Modern, clean, using Tailwind + shadcn/ui, dark mode support
4. Content: MDX files for blog and docs, static content for landing pages
5. Audience: B2B professionals (product managers, developers), desktop and mobile
```

### Step 3: Template Analysis

**AI Analyzes:**
```
I've analyzed your Next.js template. Here's what we're starting with:

Current Setup:
- Next.js version: 15.1.0
- Key dependencies: React 19, Tailwind CSS, TypeScript
- Pre-configured features: App Router, TypeScript, Tailwind
- Directory structure: app/, public/, clean slate

Template Strengths:
- Latest Next.js with App Router
- TypeScript configured
- Tailwind CSS ready

Recommended Additions:
- shadcn/ui for component library
- next-mdx-remote for blog/docs
- Zod for form validation
- React Hook Form for forms
- Vercel Analytics for tracking
```

### Step 4: Architecture Interview

**AI Uses AskQuestion Tool:**

**Question Set 1: Content Structure**
```
How should the blog work?
○ Static posts (all generated at build time)
● ISR posts (rebuild every hour) ← You choose
○ SSR posts (build on each request)

How many blog posts do you plan to have initially?
○ < 10 posts
● 10-50 posts ← You choose
○ 50+ posts

Will you need blog post categories/tags?
● Yes, with dedicated pages ← You choose
○ No, just a list
```

**Question Set 2: Forms & Functionality**
```
Waitlist form - where should data go?
● Vercel Postgres database ← You choose
○ Email service (Resend, SendGrid)
○ Third-party (Mailchimp, ConvertKit)

Should the waitlist form have email verification?
● Yes, send confirmation email ← You choose
○ No, just store the email

Do you need admin panel to view signups?
○ Yes, build custom admin
● No, check database directly ← You choose
○ Use third-party admin (Retool, etc.)
```

**Question Set 3: Performance & SEO**
```
Performance requirements:
● Lighthouse 95+ (strict) ← You choose
○ Lighthouse 90+ (standard)
○ Lighthouse 85+ (relaxed)

SEO priority pages:
☑ Homepage
☑ Pricing
☑ Blog posts
□ Docs (less critical)

Need social sharing images for all pages?
● Yes, OpenGraph for all ← You choose
○ Just homepage and blog
```

**Question Set 4: Deployment**
```
Budget constraints?
● Stay on free tier if possible ← You choose
○ Can use paid features
○ No constraints

Custom domain ready?
○ Yes, I have domain
● Will add later ← You choose
○ Use Vercel subdomain

Analytics needs?
● Vercel Analytics (simple) ← You choose
○ Google Analytics (detailed)
○ Plausible/Fathom (privacy-focused)
```

### Step 5: Architecture Decisions Made

**AI Consults nextjs-vercel-architect Agent:**

```
Using nextjs-vercel-architect to validate architecture...

✅ Data Fetching Strategy Validated:
- Homepage, Pricing: SSG (static)
- Blog posts: ISR with 3600s revalidation
- Docs: SSG (static)
- Waitlist/Contact: Server Actions

✅ Component Architecture Validated:
- Landing pages: Server Components
- Forms: Client Components for interactivity
- Blog/Docs: Server Components with MDX
- Navigation: Shared Component (works in both)

✅ Vercel Optimization Validated:
- 95% of pages static (excellent for free tier)
- Forms use Server Actions (no API routes)
- Edge middleware for redirects
- Estimated function usage: ~100 executions/month (free tier)

✅ SEO Strategy Validated:
- Metadata API for all pages
- Dynamic metadata for blog posts
- Sitemap with priority values
- OpenGraph images automated

✅ Performance Validated:
- next/image for all images
- next/font for typography
- Bundle target: 85kb first load
- Achievable: Lighthouse 95+
```

### Step 6: Plan Created

**AI Creates Plan:**
```
I've created your comprehensive implementation plan at:
thoughts/shared/plans/2026-02-11-saas-landing-page.md

The plan includes:

Phase 1: Foundation & Core Setup (2-3 hours)
- Next.js configuration with security headers
- Tailwind + shadcn/ui setup
- Root layout with fonts and metadata
- Navigation and footer components

Phase 2: Landing Pages (3-4 hours)
- Homepage (hero, features, pricing preview, CTA)
- Pricing page with three tiers
- Shared components (Button, Card, Section)
- Dark mode implementation

Phase 3: Content System (3-4 hours)
- MDX integration for blog and docs
- Blog index and post pages
- Docs navigation and pages
- Syntax highlighting for code
- Reading time calculation

Phase 4: Forms & Functionality (2-3 hours)
- Vercel Postgres setup
- Waitlist form with validation
- Contact form
- Server Actions for submissions
- Email verification flow

Phase 5: Performance, SEO & Deployment (2-3 hours)
- Image optimization audit
- Bundle size optimization
- SEO metadata for all pages
- Sitemap and robots.txt
- OpenGraph images
- Vercel deployment
- Analytics setup

Total Estimate: 12-17 hours

Performance Targets:
- Lighthouse Performance: 95+
- First Load JS: < 85kb
- LCP: < 2.0s
- CLS: < 0.1

Vercel Free Tier Impact:
- ~95% static pages
- ~100 function executions/month
- Should stay within free tier limits

Please review the detailed plan and let me know if any adjustments are needed!
```

### Step 7: Review & Refinement

**You can ask for changes:**
```
User: Can we add a feature comparison table on the pricing page?

AI: Absolutely! I'll update Phase 2 to include:
- Feature comparison table component
- Mobile-responsive table (converts to cards)
- Highlight differences between tiers
- Add pricing FAQ section

Updated plan...
```

**Or proceed:**
```
User: Looks great! Let's implement it.

AI: Perfect! You can now execute the plan with:
/implement_plan thoughts/shared/plans/2026-02-11-saas-landing-page.md

This will implement each phase with automated testing and review loops.
```

## Full Example: Technical Blog

### Starting Point
```bash
npx create-next-app@latest tech-blog --typescript --tailwind --app
cd tech-blog
```

### Invocation
```
/create_new_project_vercel_nextjs_plan
```

### Your Response
```
Type: Technical blog for web development tutorials
Features:
- Blog posts with MDX
- Code syntax highlighting (React, TypeScript, Next.js)
- Tag filtering
- Search functionality
- RSS feed
- Newsletter signup
- Reading time and view counts

Design: Clean, typography-focused, inspired by Medium but faster
Content: MDX files in Git, no CMS
Audience: Web developers, primarily desktop
```

### Result
5-phase plan including:
- MDX setup with syntax highlighting (Shiki)
- Static blog post generation
- Tag pages with ISR
- Client-side search with FlexSearch
- RSS feed generation
- View counts with Vercel KV
- Newsletter integration (Resend)
- Reading time calculation
- SEO optimized (sitemap, metadata)
- Performance targets: 98+ Lighthouse

## Example: E-commerce Store

### Starting Point
```bash
npx create-next-app@latest fashion-store --typescript --tailwind --app
cd fashion-store
```

### Invocation
```
/create_new_project_vercel_nextjs_plan
```

### Your Response
```
Type: Fashion e-commerce store
Features:
- Product catalog with categories
- Product detail pages
- Shopping cart
- Checkout with Stripe
- Order history
- User authentication
- Wishlist
- Product search and filters

Design: Modern, image-heavy, mobile-first
Content: Products from Shopify API
Audience: Fashion consumers, mobile-heavy (70% mobile)
```

### Result
5-phase plan including:
- Shopify integration
- Product listing with ISR (15 min)
- Product detail with ISR (30 min)
- Shopping cart (client state + localStorage)
- Stripe checkout integration
- Auth.js authentication
- User dashboard (SSR)
- Order management
- Image optimization strategy
- Mobile-first responsive design
- Performance targets: 90+ Lighthouse (acceptable for e-commerce)

## Tips for Best Results

### Be Specific
```
❌ "I want a website"
✅ "I want a SaaS landing page with pricing, blog, and waitlist form"
```

### Define Your Content Strategy
```
❌ "Some kind of content"
✅ "MDX blog posts, updating weekly, need categories and search"
```

### Know Your Constraints
```
❌ "Make it good"
✅ "Must stay on free tier, need 95+ Lighthouse, mobile-first"
```

### Clarify Your Stack Preferences
```
❌ "Use whatever"
✅ "I prefer shadcn/ui for components, Zod for validation, no preference on CMS"
```

## What You'll Get

Every plan includes:

1. **Technology Stack** with rationale for each choice
2. **Architecture Decisions** validated by expert agent
3. **5 Detailed Phases** with specific implementation steps
4. **Code Examples** for all major components
5. **Success Criteria** (automated + manual)
6. **Performance Targets** with specific metrics
7. **SEO Strategy** with complete checklist
8. **Vercel Configuration** optimized for your use case
9. **Testing Approach** (unit, integration, E2E)
10. **Deployment Checklist** (pre and post-deployment)

## After Planning

Execute with:
```
/implement_plan thoughts/shared/plans/YYYY-MM-DD-your-project.md
```

This will:
- Break down into manageable tasks
- Implement with quality checks
- Run automated verification
- Track progress to completion
- Ensure standards compliance

---

**Ready to build?** Invoke the skill and let's create something amazing! 🚀
