# screenkit

Screen1 Claude Code Kit

This repository is a Claude Code / Cursor workspace that bundles the `screenkit` plugin defined in `.claude-plugin/marketplace.json`, along with a curated set of local skills, agents, commands, and hooks to streamline screen recording and video‑editing workflows.

## Contents

- `.claude-plugin/marketplace.json` – declares the `screenkit` plugin:
  - **Name**: `screenkit` (`name` field)
  - **Owner**: `Duc Nguyen <ducit.dev@gmail.com>`
  - **Description**: “Screenkit is a collection of skills, workflows, and productivity tools for screen recording and video editing.”
  - **Version**: `1.0.1`
  - **Source**: `https://github.com/dinhduc2402/screenkit.git`
  - **Plugin description**: “Core skills library: TDD, debugging, collaboration patterns, and proven techniques”
- `skills/` – local skill definitions (debugging, test‑driven development, frontend/backend/full‑stack patterns, QA, Git worktrees, webapp testing, writing skills, and more).
- `commands/` – high‑level commands such as `brainstorm`, `write-plan`, and `execute-plan` that wrap the Superpowers skills.
- `agents/` – specialized agents like `code-reviewer` for structured code and architecture review.
- `hooks/` – automation hooks (for example, `session-start.sh`) used to set up the environment at key lifecycle events.
- `settings.local.json` – workspace‑local permission settings for shell and MCP tools.

## Usage

Open this folder as a project in an editor that supports Claude Code workspaces (for example, Cursor or the Claude Code desktop app). The `.claude-plugin/marketplace.json` file and the `skills/`, `commands/`, `agents/`, and `hooks/` directories provide the configuration that such tools use to load the bundled plugins and workflows.

Refer to the documentation for your specific editor or Claude Code integration for details on how it discovers `.claude-plugin` manifests and exposes skills, commands, and agents in the UI.

## Installation

**Note:** Installation may differ slightly by platform. The examples below assume Claude Code or a compatible environment with plugin marketplace commands.

### Claude Code (via Plugin Marketplace)

Register the Screenkit marketplace:

```bash
/plugin marketplace add dinhduc2402/screenkit
```

Then install the plugin from this marketplace:

```bash
/plugin install screenkit@screenkit-marketplace
```

### Verify Installation

Check that commands appear:

```bash
/help
```

You should see entries similar to:

```bash
# /screenkit:brainstorm   - Interactive design refinement
# /screenkit:write-plan   - Create implementation plan
# /screenkit:execute-plan - Execute plan in batches
```

## Customization

- **Skills**: Add or adapt skill definitions under `skills/` to match your technology stack or team practices.
- **Commands**: Update files in `commands/` to change how high‑level workflows (brainstorming, planning, execution) are invoked.
- **Agents**: Tune agent behavior in `agents/` (for example, `code-reviewer.md`) to adjust review depth, style, or standards.
- **Hooks**: Modify scripts in `hooks/` to customize what happens when sessions start or other events fire.
- **Permissions**: Edit `settings.local.json` if you need to expand or tighten which shell commands or MCP tools are allowed.

## License

See `LICENSE` for licensing details.
