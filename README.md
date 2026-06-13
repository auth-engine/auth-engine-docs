# auth-engine-docs

Canonical documentation for **AuthEngine**, published at [docs.authengine.org](https://docs.authengine.org).

**Documentation:** [auth-engine-docs](https://github.com/auth-engine/auth-engine-docs) · published at [docs.authengine.org](https://docs.authengine.org)

| Guide | Link |
|-------|------|
| Quick Start | [quick-start.md](https://docs.authengine.org/quick-start/) |
| OAuth2 / OIDC | [oauth2-oidc-guides.md](https://docs.authengine.org/oauth2-oidc-guides/) |
| API Reference | [api-reference.md](https://docs.authengine.org/api-reference/) |
| Architecture | [architecture.md](https://docs.authengine.org/architecture/) |
| Deployment | [deployment.md](https://docs.authengine.org/deployment/) |
| Security | [security-overview.md](https://docs.authengine.org/security-overview/) |

## What this repository is

MkDocs Material site containing all platform guides. Navigation is explicit in `mkdocs.yml` — new pages must be added to `nav:` manually (no auto-discovery). Built with [MkDocs Material](https://squidfunk.github.io/mkdocs-material/).

## Develop & deploy

Requires Python **3.12+**.

```bash
cd auth-engine-docs
python -m venv .venv-docs && source .venv-docs/bin/activate
pip install -r requirements-docs.txt

mkdocs serve                    # live preview at http://127.0.0.1:8000
mkdocs build --strict           # static site in ./site
```

Deploy to GitHub Pages via `.github/workflows/docs-deploy.yml` (`workflow_dispatch`). Custom domain: `docs/CNAME` → `docs.authengine.org`.

```
docs/
├── index.md                 # Platform overview & URLs
├── quick-start.md           # Run locally
├── deployment.md            # Production on AWS
├── architecture.md          # System design
├── security-overview.md     # Tokens, RBAC, hardening
├── api-reference.md         # REST endpoints
├── oauth2-oidc-guides.md    # Social login & OIDC provider
├── contributing.md
├── security-policy.md
├── about-author.md
├── CNAME                    # docs.authengine.org
└── stylesheets/extra.css
mkdocs.yml                   # Site config & navigation
overrides/                   # Theme overrides
```

## Production

| Host | Role |
|------|------|
| [api.authengine.org](https://api.authengine.org) | API + Swagger |
| [auth.authengine.org](https://auth.authengine.org) | OIDC / login UI |
| [app.authengine.org](https://app.authengine.org) | Admin dashboard |
| [docs.authengine.org](https://docs.authengine.org) | Documentation |

## Contributing

See [Contributing](https://docs.authengine.org/contributing/) or [CONTRIBUTING.md](CONTRIBUTING.md). Report security issues per [Security Policy](https://docs.authengine.org/security-policy/) — not via public issues.

## Related repositories

| Repository | Role |
|------------|------|
| [auth-engine](https://github.com/auth-engine/auth-engine) | FastAPI backend — IAM, OIDC, introspection |
| [auth-engine-dashboard](https://github.com/auth-engine/auth-engine-dashboard) | Next.js admin dashboard |
| [auth-engine-data](https://github.com/auth-engine/auth-engine-data) | Roles, permissions & super-admin seeding |
| [auth-engine-infra](https://github.com/auth-engine/auth-engine-infra) | Terraform & Docker Compose |
| [.github](https://github.com/auth-engine/.github) | Org profile, contributing & security policy |
