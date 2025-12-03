---
name: dependency-check
description: Check dependencies for updates and security vulnerabilities. Use when package.json, requirements.txt, Cargo.toml, go.mod, or similar files are modified.
---

# Dependency Check Skill

Analyze project dependencies for security vulnerabilities and outdated versions.

## When to Use

Automatically invoke when:
- Dependency files are modified (package.json, requirements.txt, Cargo.toml, go.mod, pom.xml, etc.)
- User explicitly requests dependency audit
- Setting up a new project
- Before major releases

## Check Process

1. **Identify Package Manager**
   - npm/yarn/pnpm (package.json)
   - pip (requirements.txt)
   - cargo (Cargo.toml)
   - go modules (go.mod)
   - maven/gradle (pom.xml/build.gradle)

2. **Security Vulnerabilities**
   - Run appropriate security audit command:
     - npm: `npm audit`
     - yarn: `yarn audit`
     - pip: `pip-audit` or `safety check`
     - cargo: `cargo audit`
     - go: `go list -json -m all | nancy sleuth`
   - Report vulnerabilities with severity and fix recommendations

3. **Outdated Packages**
   - Check for major version updates
   - Identify deprecated packages
   - Note breaking changes in changelogs

4. **License Compliance**
   - Flag incompatible licenses if relevant
   - Note license changes in updates

## Output Format

### Critical Vulnerabilities
- Package name and version
- CVE identifier
- Severity score
- Fix available (version or workaround)

### Recommendations
- Prioritize by severity (critical → high → medium → low)
- Provide update commands
- Note any breaking changes
- Suggest alternative packages if needed

Be specific. Focus on actionable items. Don't report low-severity issues unless explicitly asked.
