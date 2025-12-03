# Claude Code Personal Configuration

Personal Claude Code plugin with custom preferences, commands, skills, and agents.

## Structure

```
claude/
├── .claude-plugin/
│   ├── plugin.json              # Plugin metadata
│   └── marketplace.json         # Marketplace configuration
├── PREFERENCES.md               # Personal interaction preferences
├── commands/                    # Custom slash commands
│   ├── review.md               # /review - Code review with security focus
│   ├── arch.md                 # /arch - Architecture analysis
│   ├── debug.md                # /debug - Systematic debugging
│   ├── refactor.md             # /refactor - Code refactoring
│   ├── explain.md              # /explain - Code explanation
│   ├── test.md                 # /test - Write tests
│   └── optimize.md             # /optimize - Performance optimization
├── agents/                      # Custom agents
│   └── agent.md                # deep-reviewer - Comprehensive code review
├── skills/                      # Agent skills (auto-invoked)
│   ├── security-audit/         # Security vulnerability scanning
│   ├── dependency-check/       # Dependency security and updates
│   └── git-workflow/           # Git operations assistance
├── hooks/                       # Event handlers
│   └── hooks.json              # Hook configurations (disabled by default)
└── README.md                    # This file
```

## PREFERENCES.md

The `PREFERENCES.md` file defines how Claude Code should interact with you:

- **Direct communication**: No hedging, verify assumptions upfront
- **Minimal changes**: Only what's necessary, no over-engineering
- **Security first**: Watch for OWASP Top 10 vulnerabilities
- **Efficient workflow**: Use parallel operations, specialized tools

This file is your "system prompt" for Claude Code sessions.

## Commands (Slash Commands)

Invoke with `/command-name` in Claude Code:

- `/review` - Comprehensive code review checking security, quality, and best practices
- `/arch` - Analyze codebase architecture and suggest improvements
- `/debug` - Systematically debug issues with reproducible steps
- `/refactor` - Refactor code while preserving behavior
- `/explain` - Detailed explanation of how code works
- `/test` - Write comprehensive tests with edge cases
- `/optimize` - Performance optimization based on actual bottlenecks

## Skills

Skills are automatically invoked by Claude Code when relevant:

- **security-audit** - Triggered when code touches auth, input handling, DB queries, APIs
- **dependency-check** - Triggered when package files are modified
- **git-workflow** - Triggered when git help is needed or conflicts detected

## Agents

Specialized autonomous agents for complex tasks:

- **deep-reviewer** - Thorough code review with security, quality, and maintainability analysis

## Hooks

Event-driven shell commands (currently disabled, enable in `hooks/hooks.json`):

- **lint-on-edit** - Run linter when files are edited
- **test-on-commit** - Remind to run tests before committing
- **security-check** - Alert when dependency files change

## Usage

### In Claude Code CLI

1. Navigate to a directory containing this plugin
2. Claude Code will automatically load the plugin
3. Use slash commands: `/review`, `/debug`, etc.
4. Skills activate automatically when relevant

### Customization

- **Preferences**: Edit `PREFERENCES.md` to adjust interaction style
- **Commands**: Modify `.md` files in `commands/` or add new ones
- **Skills**: Edit `SKILL.md` files in `skills/*/` to adjust triggers
- **Agents**: Customize agents in `agents/`
- **Hooks**: Enable/disable hooks in `hooks/hooks.json`

## MCP (Model Context Protocol)

MCP server configuration is in `.mcp.json`. Add MCP servers for extended functionality:

```json
{
  "mcpServers": {
    "server-name": {
      "command": "command-to-start-server",
      "args": ["arg1", "arg2"]
    }
  }
}
```

---

**Learn more:** https://code.claude.com/docs
