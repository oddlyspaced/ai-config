# Plan Python Vercel Backend Architect

A specialized planning skill for **new Python Flask backend projects deployed on Vercel**. This skill helps you create comprehensive implementation plans optimized for greenfield Flask API applications running as Vercel serverless functions.

## When to Use

Use this skill when:
- Starting a **new** Flask API project from scratch or template
- Planning a backend to be deployed on **Vercel** as serverless
- Want a complete plan covering architecture, data model, API design, and deployment
- Need guidance on Flask + Vercel best practices
- Want to maximize Vercel's free tier

**Don't use this skill for:**
- Existing/legacy Flask projects (use regular `/create_plan` instead)
- Non-Flask Python projects (Django, FastAPI, etc.)
- Frontend projects (use `/create_new_project_vercel_nextjs_plan`)
- Quick feature additions to established apps

## What Makes This Different from `/create_plan`

| Aspect | `/create_plan` | `/plan_python_vercel_backend_architect` |
|--------|---------------|----------------------------------------|
| **Target** | Any project | Flask + Vercel specifically |
| **Focus** | General implementation | API architecture, data model, serverless optimization |
| **Optimizations** | General best practices | Vercel serverless-specific (cold starts, bundling) |
| **Starting Point** | Existing codebase | Fresh Flask project |
| **Guidance** | Framework-agnostic | Flask 3+ patterns (factory, blueprints, services) |

## What You Get

A comprehensive plan that includes:

### 1. **Technology Stack Decisions**
- Flask configuration (factory pattern)
- Database and ORM (SQLAlchemy, Vercel Postgres, Supabase)
- Validation (Pydantic 2+)
- Authentication (JWT, API keys)
- Rate limiting, CORS

### 2. **Architecture Design**
- Application factory pattern
- Blueprint organization by domain
- Service layer for business logic
- Configuration management per environment

### 3. **Data Model**
- Entity relationship design
- SQLAlchemy models with proper types
- Pydantic schemas for request/response
- Migration strategy

### 4. **API Design**
- RESTful endpoint mapping
- Request/response formats
- Error handling patterns
- Pagination and filtering
- API versioning

### 5. **Security**
- Authentication implementation
- Authorization decorators
- CORS configuration
- Rate limiting setup
- Input validation

### 6. **Vercel Deployment**
- Entrypoint configuration
- Cold start optimization
- Bundle size management
- Environment variables
- Monitoring strategy

### 7. **Quality Standards**
- Python type hints
- Ruff linting + mypy type checking
- pytest test strategy
- Coverage targets

## How to Use

### Quick Start

In any Cursor chat:

```
/plan_python_vercel_backend_architect
```

Then follow the interactive prompts to describe your API.

### With Requirements File

If you have a requirements document:

```
/plan_python_vercel_backend_architect requirements.md
```

### Example Session

```
User: /plan_python_vercel_backend_architect

AI: I'll help you plan your Python Flask + Vercel backend API.
    Let me understand what you're building.

    Please provide:
    1. Project Overview: What type of API?
    2. Key Endpoints: Main resources and operations?
    3. Data Requirements: Entities and relationships?
    4. Authentication: JWT, API keys, or OAuth?
    5. External Integrations: Third-party services?

User: I want to build a REST API for a task management app.
      Resources: users, projects, tasks. Tasks belong to projects,
      projects belong to users. JWT auth. Need CRUD for all entities
      plus a dashboard stats endpoint. Vercel Postgres for database.

AI: [Analyzes project needs, asks clarifying questions,
     creates comprehensive plan...]
```

## Output

Your plan will be saved to:
```
thoughts/shared/plans/YYYY-MM-DD-flask-project-name.md
```

## Quality Standards Enforced

Every plan ensures:
- **Application Factory** - Never global app object
- **Blueprints** - Routes organized by domain
- **Type Hints** - Full Python type annotations
- **Pydantic Validation** - All request/response schemas
- **Service Layer** - Business logic separated from routes
- **Serverless-Optimized** - Minimal cold starts and bundle size
- **Security First** - Auth, CORS, rate limiting from day one
- **Testable** - pytest fixtures, >60% coverage target

## Related Resources

### Agents Used by This Skill
- **`python-vercel-backend-architect`** - Validates Flask + Vercel architecture decisions
- **`codebase-locator`** - Maps project structure
- **`codebase-analyzer`** - Understands existing patterns

### Rules Applied
- **`python-vercel-backend-standards.mdc`** - Flask + Vercel coding standards

### Follow-Up Skills
After planning, use:
- **`/implement_python_vercel_backend_architect`** - Execute the plan with quality checks

## Tips for Best Results

1. **Be Specific**: Detail your API resources and operations
2. **Know Your Data Model**: Entities and relationships are crucial
3. **Define Auth Early**: Authentication approach affects everything
4. **Budget Matters**: Specify if you want to stay on Vercel free tier
5. **Know Your Consumers**: Who calls this API (frontend, mobile, services)?

## Support

Questions? Issues?
1. Check the plan output - it includes references and rationale
2. Review Flask docs: https://flask.palletsprojects.com/
3. Review Vercel Flask docs: https://vercel.com/docs/frameworks/backend/flask
4. Ask the AI to explain any recommendation

---

**Built for APIs. Optimized for Vercel. Ready for production.**
