# Plugin structure overview

```
my-first-plugin/
├── .claude-plugin/
│   └── plugin.json           # Plugin metadata
├── commands/                 # Custom slash commands (optional)
│   └── hello.md
├── agents/                   # Custom agents (optional)
│   └── helper.md
├── skills/                   # Agent Skills (optional)
│   └── my-skill/
│       └── SKILL.md
└── hooks/                    # Event handlers (optional)
    └── hooks.json
```

---

**Source:** https://code.claude.com/docs/en/plugins
