---
name: security-audit
description: Comprehensive security audit of code changes. Use when commits include authentication, input handling, database queries, file operations, or API endpoints.
---

# Security Audit Skill

Perform a comprehensive security audit focusing on OWASP Top 10 vulnerabilities.

## When to Use

Automatically invoke when you detect:
- Authentication or authorization code
- User input handling
- Database queries (SQL, NoSQL, ORM)
- File system operations
- API endpoints or request handlers
- Shell command execution
- Cryptographic operations
- Session management
- File uploads
- XML/JSON parsing

## Audit Checklist

### 1. Injection Flaws
- SQL injection: Check parameterized queries, ORM usage
- Command injection: Check shell command construction
- NoSQL injection: Check query object construction
- LDAP injection: Check directory service queries

### 2. Broken Authentication
- Password storage (bcrypt, argon2, not MD5/SHA1)
- Session management (secure, httpOnly, sameSite cookies)
- Token generation (sufficient entropy)
- Multi-factor authentication handling
- Password reset flows

### 3. Sensitive Data Exposure
- Secrets in code or logs
- Unencrypted data transmission
- Inadequate encryption algorithms
- Exposed API keys or credentials
- Sensitive data in URLs or error messages

### 4. XML External Entities (XXE)
- XML parser configuration
- DTD processing disabled
- External entity resolution

### 5. Broken Access Control
- Authorization checks on all protected resources
- Insecure direct object references
- Missing function-level access control
- CORS misconfiguration

### 6. Security Misconfiguration
- Default credentials
- Verbose error messages
- Unnecessary features enabled
- Outdated dependencies

### 7. Cross-Site Scripting (XSS)
- Input validation
- Output encoding/escaping
- Content Security Policy
- DOM-based XSS

### 8. Insecure Deserialization
- Untrusted data deserialization
- Type validation before deserialization

### 9. Using Components with Known Vulnerabilities
- Dependency versions
- Known CVEs

### 10. Insufficient Logging & Monitoring
- Security events logged
- No sensitive data in logs
- Log injection prevention

## Output Format

For each issue found:
- **Severity**: Critical/High/Medium/Low
- **Location**: file:line
- **Issue**: Specific vulnerability description
- **Impact**: What could happen
- **Fix**: Concrete code example or specific action

Be direct. Only report actual vulnerabilities, not theoretical possibilities.
