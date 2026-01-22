# Railway Skill for Claude Code

A Claude Code skill for managing Railway deployments via CLI.

## Features

- **Status checks** - View project, environment, service, and deployment info
- **Health checks** - Verify your deployment is responding
- **Logs** - View deploy/build logs with natural language filters ("errors", "last hour")
- **Deploy** - Deploy with automatic health verification
- **Variables** - View/set env vars (sensitive values auto-redacted)
- **Project switching** - Quick switch between Railway projects
- **Database access** - Connect to database shells

## Installation

```bash
npx add-skill mshumer/claude-skill-railway
```

Or manually copy the `railway` folder to your Claude Code skills directory:

```bash
# Personal (all projects)
cp -r railway ~/.claude/skills/

# Or project-specific
cp -r railway /path/to/project/.claude/skills/
```

## Prerequisites

1. Install Railway CLI: `npm install -g @railway/cli`
2. Login: `railway login`
3. Link a project: `railway link`

## Usage

```
/railway              # Status check (default)
/railway status       # Project info + last deployment
/railway health       # Check if deployment is responding
/railway logs         # Recent logs
/railway logs errors  # Error logs only
/railway logs 1h      # Logs from last hour
/railway deploy       # Deploy + verify
/railway redeploy     # Redeploy without rebuild
/railway vars         # List environment variables
/railway switch <name> # Switch to different project
/railway db           # Connect to database shell
/railway link         # List and link a project
```

## License

MIT
