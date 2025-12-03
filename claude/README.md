# Claude Code Configuration

This directory contains Claude Code configuration optimized for ML/AI research and development work.

## Setup

To use this configuration, symlink or copy it to your home directory:

```bash
# Option 1: Symlink (recommended - keeps config in dotfiles)
ln -s ~/dotfiles/claude ~/.claude

# Option 2: Copy
cp -r ~/dotfiles/claude ~/.claude
```

## Structure

```
claude/
├── .claude-plugin/
│   └── plugin.json           # Plugin metadata
├── CLAUDE.md                 # Core preferences and working style
├── commands/                 # Custom slash commands
│   ├── quick-experiment.md   # Set up experiment with tracking
│   ├── paper-notes.md        # Generate paper notes template
│   ├── check-reproducibility.md  # Check reproducibility
│   └── ml-code-review.md     # ML-specific code review
├── skills/                   # Specialized agent skills
│   ├── research-paper/       # Deep paper analysis
│   ├── ml-systems-design/    # System architecture design
│   ├── experiment-design/    # Rigorous experiment planning
│   └── literature-synthesis/ # Multi-paper synthesis
└── agents/                   # Custom agents (add as needed)
```

## Configuration Philosophy

This configuration emphasizes:
- **Direct, precise communication** - No hedging, explicit assumptions
- **Depth over breadth** - Thorough analysis
- **Empirical rigor** - Evidence-based reasoning
- **Systems thinking** - Scalability and maintainability
- **Reproducibility** - Versioning, logging, seeds

## Skills

### research-paper
Analyze ML/AI papers with Gwern-level depth. Examines methodology, results, limitations, and reproducibility.

### ml-systems-design
Design ML systems considering scale, reliability, and operational concerns. Covers data pipelines, training infrastructure, and serving.

### experiment-design
Plan rigorous experiments with proper controls, baselines, and statistical validity. Includes ablation studies and reproducibility.

### literature-synthesis
Synthesize research across multiple papers. Identify patterns, gaps, and trajectories in the literature.

## Commands

### /quick-experiment
Set up a minimal but rigorous experiment with tracking, reproducibility, and monitoring.

### /paper-notes
Generate structured notes template for ML/AI papers with all key sections.

### /check-reproducibility
Audit codebase for reproducibility issues (seeds, versions, documentation).

### /ml-code-review
ML-specific code review checking correctness, numerical stability, and best practices.

## Customization

### CLAUDE.md
Core preferences file loaded in every session. Edit to adjust communication style, technical standards, and workflow preferences.

### Adding Commands
Create `commands/your-command.md` with:
```markdown
---
description: Brief description for command list
---

# Command Title

Instructions for Claude...
```

### Adding Skills
Create `skills/your-skill/SKILL.md` with:
```markdown
---
name: skill-name
description: When to use this skill
---

# Skill instructions...
```

## References

Configuration influenced by:
- Gwern (depth, documentation)
- TheZvi (explicit reasoning)
- davidad (formal rigor)
- Jeremy Howard (practical ML)
- Chris Lattner (systems design)

---

**Documentation**: https://code.claude.com/docs
