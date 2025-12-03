---
name: git-workflow
description: Assist with git operations including commits, branches, PRs, and conflict resolution. Use when user requests git help or when you detect git-related issues.
---

# Git Workflow Skill

Provide assistance with git operations and workflows.

## When to Use

Invoke when:
- User asks for git help
- Merge conflicts detected
- Preparing commits or PRs
- Branch management needed
- Repository state is unclear

## Capabilities

### 1. Commit Assistance
- Analyze staged changes
- Write clear, conventional commit messages
- Format: `<type>: <description>`
- Types: feat, fix, refactor, docs, test, chore, perf
- Check commit message matches repository style

### 2. Branch Management
- Suggest branch naming (feature/, fix/, refactor/)
- Check for unmerged changes
- Identify stale branches
- Recommend cleanup

### 3. Conflict Resolution
- Identify conflict markers
- Explain both sides of conflict
- Suggest resolution strategy
- Help test resolution

### 4. PR Preparation
- Summarize changes since branch point
- Generate PR description
- Suggest reviewers based on file history
- Check for common PR issues:
  - Large diffs (suggest splitting)
  - Missing tests
  - Merge conflicts
  - Failed CI checks

### 5. Repository Analysis
- Understand branching strategy
- Identify main/master branch
- Check remote configuration
- Review recent commit patterns

## Commit Message Guidelines

Structure:
```
<type>(<scope>): <short description>

<detailed description if needed>

<footer: breaking changes, issues closed>
```

Types:
- `feat`: New feature
- `fix`: Bug fix
- `refactor`: Code change that neither fixes a bug nor adds a feature
- `perf`: Performance improvement
- `test`: Adding or updating tests
- `docs`: Documentation only
- `chore`: Maintenance (dependencies, config, etc.)

Rules:
- Imperative mood ("add feature" not "added feature")
- No period at end of subject line
- Max 50 chars for subject
- Wrap body at 72 chars
- Focus on WHY, not WHAT (code shows what)

## Safety

Never:
- Force push to main/master without explicit permission
- Run destructive operations (hard reset, etc.) without confirmation
- Skip commit hooks
- Commit sensitive data (keys, tokens, passwords)
- Amend commits from other developers

Always:
- Check branch before destructive operations
- Verify commits before force push
- Warn about sensitive data in diffs
- Respect repository's git hooks
