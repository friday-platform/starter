# Friday Agent Studio & Toolkit — Starter

Get up and running with [Friday Agent Studio & Toolkit (FAST)](https://platform.hellofriday.ai/docs) in under five minutes.

## Prerequisites

- [Docker](https://docs.docker.com/get-docker/) v20.10+ with Docker Compose v2
- An [Anthropic API key](https://console.anthropic.com) for Claude
- A `key.json` service account key file from Friday (for container registry access)

## Quick start

```bash
# 1. Clone this repo
git clone https://github.com/friday-platform/starter.git && cd starter

# 2. Authenticate with the container registry (once per machine)
docker login -u _json_key --password-stdin https://us-west2-docker.pkg.dev < key.json

# 3. Create your .env from the template
cp .env.example .env
# Edit .env and add your ANTHROPIC_API_KEY

# 4. Start it up
docker compose up
```

Wait for the startup banner, then open the Studio at **http://localhost:15200**.

## What's included

| File | Purpose |
|------|---------|
| `docker-compose.yml` | Platform services configuration |
| `.env.example` | All supported environment variables with descriptions |
| `webhook-mappings.yml` | Default webhook payload mappings for GitHub, Bitbucket, and Jira |
| `.gitignore` | Keeps secrets and local data out of version control |

## Next steps

- [Quick start guide](https://platform.hellofriday.ai/docs/getting-started/quickstart) — load a starter space and trigger your first job
- [Documentation](https://platform.hellofriday.ai/docs) — full reference
- [Examples](https://github.com/friday-platform/examples) — starter `workspace.yml` files

## License

Apache 2.0 — see [LICENSE](LICENSE).
