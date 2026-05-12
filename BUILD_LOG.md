# Build Log – Secure Script Architect

## System Prompt v1
Initial system prompt defining the Secure Script Architect role,
focused on PowerShell automation and secure coding practices.

Key rules enforced:
- No hardcoded credentials
- Avoid unsafe execution methods
- Explain security tradeoffs
- Refuse insecure requests

## Early Testing
Initial tests included:
- Safe automation tasks (service restarts, system queries)
- Unsafe requests involving inline credentials
- Ambiguous administrative actions

Observed issues:
- Some ambiguous cases required clearer refusal language

Next steps:
- Iterate on refusal explanations
- Improve clarity of allowed vs disallowed patterns
