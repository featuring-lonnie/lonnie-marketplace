# Lonnie's Marketplace

Personal Claude Code plugins for productivity and workflow automation.

## Plugins

| Plugin | Description |
|--------|-------------|
| [dev-workflow](https://github.com/featuring-lonnie/dev-workflow) | Developer workflow - Git, PR, code review with Jira/Slack/Confluence |
| [pm-workflow](https://github.com/featuring-lonnie/pm-workflow) | PM workflow - Jira tickets, PRD, release notes, stakeholder updates |
| [de-workflow](https://github.com/featuring-lonnie/de-workflow) | Designer workflow - Figma, design specs, dev handoff |
| [workflow-common](https://github.com/featuring-lonnie/workflow-common) | Common workflow commands - role selection, unified status |
| [workflow-manager](https://github.com/featuring-lonnie/workflow-manager-plugin) | Unified workflow management across Slack, Confluence, Jira, GitHub |

## Installation

### 1. Add Marketplace (First Time Only)

```bash
claude plugin marketplace add featuring-lonnie/lonnie-marketplace
```

### 2. Update Marketplace

```bash
claude plugin marketplace update lonnie-marketplace
```

### 3. Install Plugins

```bash
# Workflow Plugins (Team Collaboration)
claude plugin install dev-workflow@lonnie-marketplace
claude plugin install pm-workflow@lonnie-marketplace
claude plugin install de-workflow@lonnie-marketplace
claude plugin install workflow-common@lonnie-marketplace

# Other Plugins
claude plugin install workflow-manager@lonnie-marketplace
```

### 4. Enable Plugins

Add to `~/.claude/settings.json`:

```json
{
  "enabledPlugins": {
    "dev-workflow@lonnie-marketplace": true,
    "pm-workflow@lonnie-marketplace": true,
    "de-workflow@lonnie-marketplace": true,
    "workflow-common@lonnie-marketplace": true
  }
}
```

### 5. Restart Claude Code

Restart Claude Code to load the new plugins.

## Commands Overview

### dev-workflow (Developer)

| Command | Description |
|---------|-------------|
| `/dev-workflow:init` | Initial setup |
| `/dev-workflow:start` | Start work on Jira ticket + create branch |
| `/dev-workflow:commit` | Gitmoji commit |
| `/dev-workflow:pr` | Create PR |
| `/dev-workflow:review` | Request code review via Slack |
| `/dev-workflow:pr-review` | Perform PR review (P5 format) |
| `/dev-workflow:approve` | Approve PR |
| `/dev-workflow:done` | Merge PR + Jira Done |
| `/dev-workflow:doc` | Create Tech Spec |
| `/dev-workflow:status` | Check status |

### pm-workflow (PM)

| Command | Description |
|---------|-------------|
| `/pm-workflow:init` | Initial setup |
| `/pm-workflow:start` | Start Jira ticket (no git) |
| `/pm-workflow:ticket` | Create/manage tickets |
| `/pm-workflow:track` | Project dashboard |
| `/pm-workflow:prd` | Create PRD document |
| `/pm-workflow:release` | Create release notes |
| `/pm-workflow:update` | Stakeholder update via Slack |
| `/pm-workflow:done` | Complete ticket |
| `/pm-workflow:status` | Check status |

### de-workflow (Designer)

| Command | Description |
|---------|-------------|
| `/de-workflow:init` | Initial setup |
| `/de-workflow:start` | Start design work |
| `/de-workflow:upload` | Add Figma link to ticket |
| `/de-workflow:spec` | Create design spec |
| `/de-workflow:review` | Request design review |
| `/de-workflow:handoff` | Dev handoff |
| `/de-workflow:done` | Complete design |
| `/de-workflow:status` | Check status |

### workflow-common

| Command | Description |
|---------|-------------|
| `/workflow-common:init` | Select role (dev/pm/designer) |
| `/workflow-common:status` | Unified status view |

## Configuration

All workflow plugins share config at `~/.claude/workflow/config.json`.

Run the appropriate init command to configure:
- Developer: `/dev-workflow:init`
- PM: `/pm-workflow:init`
- Designer: `/de-workflow:init`

## Update Plugins

```bash
claude plugin marketplace update lonnie-marketplace
claude plugin install <plugin>@lonnie-marketplace  # reinstall to update
```

## Uninstall

```bash
claude plugin uninstall dev-workflow@lonnie-marketplace
```

## License

MIT
