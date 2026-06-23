# auth-engine-docs

Official documentation site for **AuthEngine**, built with MkDocs Material and published at [docs.authengine.org](https://docs.authengine.org).

Covers local development, production deployment (K3s + Rancher + Helm), API reference, OAuth/OIDC integration, architecture, and security.

## Documentation index

| Section | Pages |
|---------|-------|
| **Getting started** | [Quick Start](https://docs.authengine.org/quick-start/) · [Deployment](https://docs.authengine.org/deployment/) |
| **Platform** | [Architecture](https://docs.authengine.org/architecture/) · [Security](https://docs.authengine.org/security-overview/) |
| **Integration** | [API Reference](https://docs.authengine.org/api-reference/) · [OAuth2 / OIDC](https://docs.authengine.org/oauth2-oidc-guides/) |
| **Community** | [Contributing](https://docs.authengine.org/contributing/) · [Security Policy](https://docs.authengine.org/security-policy/) |

## Development

Edit and preview locally:

```bash
cd auth-engine-docs
python -m venv .venv-docs && source .venv-docs/bin/activate
pip install -r requirements-docs.txt
mkdocs serve                  # http://127.0.0.1:8000
```

Deploy to GitHub Pages: run workflow **docs-deploy** (`workflow_dispatch`).

## Production

Platform deployment (not the docs site itself):

| Path | Guide |
|------|-------|
| Local VM + Cloudflare Tunnel | [Deployment — local VM](https://docs.authengine.org/deployment/#local-vm-laptop--cloudflare-tunnel) |
| AWS EC2 or any cloud VM | [Deployment — cloud VM](https://docs.authengine.org/deployment/#cloud-vm-aws-or-any-provider) |

Docs site hosting: GitHub Pages → `docs.authengine.org` (deploy via the **docs-deploy** workflow in this repo).

## Related repositories

[auth-engine](https://github.com/auth-engine/auth-engine) · [auth-engine-dashboard](https://github.com/auth-engine/auth-engine-dashboard) · [auth-engine-data](https://github.com/auth-engine/auth-engine-data) · [auth-engine-infra](https://github.com/auth-engine/auth-engine-infra)
