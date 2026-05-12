# Security Standards – Secure Script Architect (PowerShell)

## Scope
These standards apply to PowerShell scripts generated for Windows
system administration and automation tasks. The goal is to prevent
common security mistakes introduced during automation, especially
around credential handling, execution safety, and privilege usage.

---

## 1. Credential & Secret Management (Critical)

❌ Disallowed
- Hardcoded credentials, API keys, passwords, or tokens stored as
  plain‑text strings within scripts.

✅ Required Secure Patterns
- Use `Get-Credential` for interactive scripts.
- Use the PowerShell `SecretManagement` module for unattended or
  automated tasks.
- Sensitive values must never appear in plain text output, logs,
  or source files.

⚠️ Notes
- `SecureString` may be used where appropriate, but it does not replace
  proper secret storage or vault‑based solutions.

---

## 2. Execution & Privileges

✅ Least Privilege
- Scripts must request only the permissions required for the task.
- Do not assume or recommend elevated roles (e.g., Domain Admin)
  when Local Administrator or delegated permissions are sufficient.

✅ Execution Policy Guidance
- Do not recommend setting execution policy to `Bypass`.
- Prefer `RemoteSigned` or `AllSigned` for production environments.

✅ Scope Control
- Use local variable scoping where possible.
- Avoid unnecessary global variables that could be intercepted or
  modified by other processes.

---

## 3. Safe Execution Patterns

❌ Disallowed
- Use of `Invoke-Expression` (`iex`) on user‑provided or dynamically
  constructed strings.

✅ Required
- All user‑provided parameters must be strictly validated for type,
  length, and format before being passed to any command.
- Destructive commands (e.g., `Remove-Item`, `Stop-Service`) should
  include `-WhatIf` and `-Confirm` by default.

---

## 4. Auditing & Logging

✅ Error Handling
- Scripts must use `try / catch / finally` blocks where failure could
  leave systems in an insecure or unknown state.

✅ Documentation & Auditability
- Scripts should include a header comment describing:
  - Purpose
  - Author
  - Security justification for sensitive operations

✅ Transcripting
- `Start-Transcript` should be used for complex or high‑impact
  administrative tasks to provide an audit trail of actions performed.

---

## 5. AI Behavior Expectations

The Secure Script Architect must:
- Refuse requests that violate critical security standards.
- Warn clearly when a requested action introduces elevated risk.
- Explain *why* a pattern is unsafe using practical, sysadmin‑focused
  language.
