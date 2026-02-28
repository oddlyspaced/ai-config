# Plan Python Vercel Backend Architect - Summary

## What Was Created

This comprehensive skill package includes **three interconnected components** designed to ensure the highest quality Python Flask + Vercel backend projects:

### 1. The Skill: `/plan_python_vercel_backend_architect`

**File:** `.cursor/skills/plan_python_vercel_backend_architect/SKILL.md`

**Purpose:** Interactive planning skill specialized for greenfield Python Flask API projects deployed on Vercel as serverless functions.

**What it does:**
- Analyzes your Flask project structure (or starts fresh)
- Conducts deep requirements interviews for API design
- Makes architecture decisions with expert validation
- Creates comprehensive 5-phase implementation plans
- Optimizes for cold starts, bundle size, and Vercel free tier
- Enforces quality standards from the start

**Key Features:**
- **Project-Aware**: Understands your starting point (Vercel template, fresh project)
- **Interactive**: Asks detailed questions about API design, data model, auth
- **Expert Validation**: Uses `python-vercel-backend-architect` agent for architecture review
- **Comprehensive**: Covers architecture, data model, API design, security, deployment
- **Vercel-Optimized**: Minimizes cold starts, optimizes bundle size, free tier usage
- **Quality-Focused**: Enforces best practices for Flask 3+, Pydantic 2+, SQLAlchemy 2+

**Output:** A detailed plan saved to `thoughts/shared/plans/YYYY-MM-DD-flask-project-name.md` with:
- Technology stack with rationale
- Data model and entity relationships
- Complete API endpoint mapping
- 5 implementation phases
- Success criteria (automated + manual)
- Performance budgets
- Security checklist
- Deployment strategy
- Testing approach

### 2. The Agent: `python-vercel-backend-architect`

**File:** `.cursor/agents/python-vercel-backend-architect.md`

**Purpose:** Specialized validation agent for Python Flask + Vercel architecture decisions.

**Expertise:**
- Flask application factory and Blueprint patterns
- Python backend best practices (type hints, service layer)
- Vercel serverless deployment optimizations
- Database strategy for serverless (connection pooling)
- API design patterns (REST, validation, error handling)
- Security (auth, CORS, rate limiting)

**What it validates:**
- **Application Structure**: Factory pattern, Blueprint organization, service layer
- **Data Layer**: ORM configuration, connection pooling, schema design
- **API Design**: RESTful conventions, validation, error format
- **Security**: Auth, CORS, rate limiting, input sanitization
- **Vercel Optimization**: Bundle size, cold starts, execution time
- **Testing**: pytest setup, fixture design, coverage

### 3. The Rules: `python-vercel-backend-standards.mdc`

**File:** `.cursor/rules/python-vercel-backend-standards.mdc`

**Purpose:** Comprehensive coding standards for Python Flask + Vercel backend development.

**Applies to:** `**/*.py`, `**/pyproject.toml`, `**/requirements.txt`, `**/vercel.json`

**Covers Major Topics:**

#### Core Principles (7)
1. **Application Factory** - Always use `create_app()` pattern
2. **Blueprints** - Organize routes by domain
3. **Type Hints** - Full Python type annotations
4. **Pydantic Validation** - All input/output validated
5. **Service Layer** - Business logic separated from routes
6. **Serverless-Aware** - Optimized for Vercel
7. **Security First** - Auth, validation, CORS built-in

#### Detailed Coverage
- Project Structure conventions
- Python coding conventions (types, imports, constants)
- Flask patterns (factory, config, blueprints, routes)
- Pydantic schemas (request/response/common)
- SQLAlchemy models (base mixin, relationships)
- Service layer patterns
- Authentication (JWT, decorators)
- Error handling (standardized JSON errors)
- Testing (pytest fixtures, test patterns)
- Vercel deployment (pyproject.toml, env vars, checklist)
- Performance best practices
- Security checklist
- Linting (Ruff + mypy)
- Anti-patterns to avoid

## How They Work Together

```
User invokes: /plan_python_vercel_backend_architect
                         ↓
                Skill activates
                         ↓
        Analyzes Flask project structure
                         ↓
        Spawns python-vercel-backend-architect agent
                         ↓
   Agent validates architecture decisions
   (using knowledge from standards rules)
                         ↓
        Creates comprehensive plan
        (enforcing standards rules)
                         ↓
   Plan includes specific code examples
   (following standards patterns)
                         ↓
   Output: Production-ready implementation plan
```

## Quality Standards Enforced

Every plan created with this skill ensures:

### Architecture
- Application Factory pattern
- Blueprint-based route organization
- Service layer for business logic
- Clean configuration management

### Data Layer
- SQLAlchemy 2+ with proper types
- Pydantic 2+ for validation
- Connection pooling for serverless
- Database migration strategy

### Security
- JWT/API key authentication
- CORS configured for known origins
- Rate limiting on all endpoints
- Input validation on all requests
- Secrets in environment variables

### Performance
- Cold start < 2s target
- Simple CRUD < 200ms
- Bundle size < 50MB
- Efficient database queries

### Testing
- pytest with app factory fixtures
- API endpoint tests
- Service layer tests
- >60% coverage target

### Deployment
- Vercel entrypoint configured
- Environment variables documented
- Health check endpoints
- Monitoring strategy

## File Locations

All created files are in your Cursor configuration:

```
.cursor/
├── skills/
│   └── plan_python_vercel_backend_architect/
│       ├── SKILL.md          # Main skill implementation
│       ├── README.md         # Usage documentation
│       └── SUMMARY.md        # This file
├── agents/
│   └── python-vercel-backend-architect.md  # Architecture validation agent
└── rules/
    └── python-vercel-backend-standards.mdc # Coding standards
```

## Next Steps After Planning

Once you have your plan:

```
/implement_python_vercel_backend_architect thoughts/shared/plans/YYYY-MM-DD-flask-project-name.md
```

---

**Built for APIs. Optimized for Vercel. Ready for production.**
