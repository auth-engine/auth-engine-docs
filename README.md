# auth-engine-docs

Canonical documentation for the **AuthEngine** platform, published at
[docs.authengine.org](https://docs.authengine.org). Built with
[MkDocs Material](https://squidfunk.github.io/mkdocs-material/).

> These docs previously lived in `auth-engine-infra`; they now have their own
> repository so the infrastructure repo stays Terraform + Compose only.

## Develop

Requires Python 3.12+.

```bash
cd auth-engine-docs
python -m venv .venv-docs && source .venv-docs/bin/activate
pip install -r requirements-docs.txt

mkdocs serve          # live preview at http://127.0.0.1:8000
```

## Build

```bash
mkdocs build --strict   # static site in ./site
```

## Deploy

Pushed to GitHub Pages via `.github/workflows/docs-deploy.yml`
(`workflow_dispatch`). The custom domain is set by `docs/CNAME`
(`docs.authengine.org`).

## Structure

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

## Related repositories

| Repository | Role |
|------------|------|
| `auth-engine` | FastAPI backend — IAM, OIDC, introspection |
| `auth-engine-dashboard` | Next.js admin dashboard |
| `auth-engine-data` | Roles, permissions & super-admin seeding |
| `auth-engine-infra` | Terraform & Docker Compose |
