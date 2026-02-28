# Implement Python Vercel Backend Architect

Specialized implementation skill for executing Python Flask + Vercel backend project plans created by `/plan_python_vercel_backend_architect`.

## What Makes This Different

This skill is specifically designed for Python Flask + Vercel serverless projects and includes:

### Flask-Specific Verification
- Ruff linting (`ruff check .`)
- Type checking (`mypy app/`)
- Test suite (`pytest -v`)
- Coverage analysis (`pytest --cov`)
- App startup verification
- Health check endpoint testing

### Architecture Validation
- Uses `python-vercel-backend-architect` agent for expert review
- Validates application factory pattern
- Checks Blueprint organization
- Verifies service layer separation
- Ensures Pydantic validation on all endpoints

### Security Checks
- JWT implementation verified
- CORS configuration validated
- Rate limiting confirmed
- Input validation on all routes
- No hardcoded secrets

### Vercel Optimization
- Entrypoint configuration verified
- Bundle size within limits
- Dependencies minimal
- Connection pooling configured
- Cold start optimization checked

### Standards Enforcement
- Applies `python-vercel-backend-standards.mdc` rules
- Enforces application factory pattern
- Validates type hints throughout
- Checks Pydantic schema usage

## When to Use

Use this skill when:
- Implementing a plan created by `/plan_python_vercel_backend_architect`
- Building a **new** Flask 3+ backend project
- Deploying to Vercel as serverless
- Need architecture validation during implementation
- Want security and testing checks built-in

**Don't use for:**
- Existing/legacy Flask projects (use regular `/implement_plan`)
- Non-Flask Python projects
- Frontend projects (use `/implement_new_project_vercel_nextjs_plan`)
- Quick bug fixes

## How to Use

### Basic Usage

```bash
# In Cursor chat
/implement_python_vercel_backend_architect thoughts/shared/plans/2026-02-14-flask-task-api.md
```

### The Implementation Process

```
1. Verify Setup
   |-- Check it's a Flask + Vercel plan
   |-- Verify Python installation
   |-- Check project structure
   |-- Read plan completely

2. Create Ledger (if needed)
   |-- Extract phases from plan
   |-- Note performance targets
   |-- Track architecture decisions
   |-- Document data model

3. For Each Phase:
   |
   |-- Implement
   |   |-- Follow Flask 3+ patterns
   |   |-- Apply python-vercel-backend-standards rules
   |   |-- Respect architecture decisions
   |
   |-- Verify Code Quality
   |   |-- Ruff linting
   |   |-- mypy type checking
   |   |-- pytest test suite
   |   |-- Coverage check
   |
   |-- Validate Architecture
   |   |-- Consult python-vercel-backend-architect
   |   |-- Verify app structure
   |   |-- Check API design
   |   |-- Confirm security
   |
   |-- Review Code Quality
   |   |-- Spawn task-review-agent
   |   |-- Check for issues
   |   |-- Fix if needed (max 3 iterations)
   |
   |-- Manual Verification
      |-- Test endpoints with curl
      |-- Check error responses
      |-- Verify auth flow
      |-- Confirm with user

4. Final Validation
   |-- Full test suite
   |-- Architecture review
   |-- Security audit
   |-- Deployment readiness check
```

## Execution Modes

### Mode 1: Direct Implementation
**For:** Small plans (3 or fewer phases)

```
User: /implement_python_vercel_backend_architect thoughts/shared/plans/simple-api.md

AI: This plan has 3 phases. I'll implement directly.

Phase 1: Foundation & Setup
[implements directly in main context]
- Ruff passed
- App starts correctly
- Health check works
- Architecture validated
Ready for manual verification...

[continues with phases 2 and 3]
```

### Mode 2: Agent Orchestration
**For:** Larger plans (4+ phases), complex projects

```
User: /implement_python_vercel_backend_architect thoughts/shared/plans/full-api.md

AI: This plan has 5 phases. I'll use agent orchestration.

Creating ledger: thoughts/ledgers/full-api.md
Creating handoffs: thoughts/handoffs/full-api/

----------------------------------------------
Phase 1 of 5: Foundation & Setup
----------------------------------------------

Implementing (implement_task agent)...
Verifying (ruff, mypy, pytest)...
Validating (python-vercel-backend-architect)...
Reviewing (task-review-agent)...

Phase 1 complete
Handoff: thoughts/handoffs/full-api/phase-01-foundation.md

Ready for manual verification. Type 'continue' when ready.
```

## Verification Checklist

After each phase, these checks run automatically:

### Code Quality
```bash
# 1. Linting
ruff check .
# Must pass: No errors

# 2. Type checking
mypy app/
# Should pass: No type errors

# 3. Tests
pytest -v
# Must pass: All tests green

# 4. Coverage
pytest --cov=app
# Check against targets
```

### Architecture Quality
- Consults `python-vercel-backend-architect` agent
- Validates application factory usage
- Checks Blueprint organization
- Verifies service layer pattern
- Confirms Pydantic validation

### Security Quality
- JWT implementation correct
- Passwords hashed properly
- CORS configured for known origins
- Rate limiting active
- No hardcoded secrets

### Manual Quality
- API endpoint testing required
- Auth flow verification
- Error response checking
- User confirmation needed

## Troubleshooting

### Import Errors / Circular Imports

**Problem:** Flask circular import errors

**Solution:**
- Import blueprints after creating them
- Use extensions module for shared instances (db, etc.)
- Avoid importing app in models
- Use local imports in route modules if needed

### Vercel Deployment Fails

**Problem:** App doesn't start on Vercel

**Solution:**
- Verify `app.py` exports `app` instance (not factory)
- Check `pyproject.toml` has `[project.scripts]` section
- Verify all dependencies in requirements.txt
- Check bundle size < 250MB

### Database Connection Errors

**Problem:** Connection errors in serverless

**Solution:**
- Configure connection pooling:
  ```python
  SQLALCHEMY_ENGINE_OPTIONS = {
      "pool_size": 5,
      "max_overflow": 2,
      "pool_recycle": 300,
      "pool_pre_ping": True,
  }
  ```
- Use database provider's connection pooler if available

### Test Database Issues

**Problem:** Tests fail due to database state

**Solution:**
- Use SQLite in-memory for tests: `sqlite:///:memory:`
- Create tables in fixture, drop after
- Rollback session after each test
- Ensure test isolation

## Integration with Other Skills

### Before Implementation
```
1. Plan -> /plan_python_vercel_backend_architect
2. Validate -> Uses python-vercel-backend-architect (included)
3. Implement -> /implement_python_vercel_backend_architect
```

### During Implementation
- Automatically uses `python-vercel-backend-architect` for validation
- Automatically uses `task-review-agent` for code review
- Applies `python-vercel-backend-standards.mdc` rules

### After Implementation
```
1. Deploy -> Vercel (vc deploy --prod)
2. Monitor -> Vercel Dashboard + Error tracking
3. Iterate -> Based on real-world usage
```

## Tips for Success

### 1. Trust the Process
- Let verification run completely
- Don't skip architecture validation
- Fix issues immediately

### 2. Keep Services Clean
- Thin routes, fat services
- Business logic in services
- Routes only validate and respond

### 3. Test Everything
- Write tests alongside code
- Use app factory fixtures
- Test happy paths AND error cases

### 4. Think Serverless
- No local state between requests
- Connection pooling is critical
- Bundle size matters
- Cold starts affect user experience

### 5. Security Always
- Auth on protected routes
- Validate all input
- Hash all passwords
- Secrets in environment

## Support

### Documentation
- Skill: `.cursor/skills/implement_python_vercel_backend_architect/SKILL.md`
- Architect: `.cursor/agents/python-vercel-backend-architect.md`
- Standards: `.cursor/rules/python-vercel-backend-standards.mdc`

### Resources
- Flask Docs: https://flask.palletsprojects.com/
- Vercel Flask: https://vercel.com/docs/frameworks/backend/flask
- Pydantic Docs: https://docs.pydantic.dev/
- SQLAlchemy Docs: https://docs.sqlalchemy.org/

---

**Build with confidence. Deploy with pride.**
