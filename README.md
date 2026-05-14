Note: This is a Week 1 Draft. Core security logic and deployment structure are operational; UI refinement and deeper evaluation are planned for Week 2

# Secure Script Architect – PowerShell Edition

## Overview
The Secure Script Architect is a prompt‑driven tool designed to help Windows system administrators
generate secure PowerShell automation scripts. The focus of this project is preventing common
security mistakes such as hardcoded credentials, unsafe command execution, and overly broad privilege use.

## Problem
PowerShell is extremely powerful in Windows environments, but automation scripts are often written
quickly and can introduce serious security risks. Hardcoded credentials, unsafe execution patterns,
and poor error handling are common issues.

## Solution
This project provides a guided, security‑first prompt interface that helps sysadmins design PowerShell
scripts while enforcing secure coding standards and explaining why certain patterns are unsafe.

## Key Security Principles
- No hardcoded credentials or secrets
- Avoid unsafe patterns such as Invoke‑Expression on user input
- Prefer Get‑Credential, PowerShell SecretManagement, or environment variables
- Explicit warnings and refusals for insecure requests

## Project Progress (Week 1)

This project is currently in active development as part of a two-week
prompt-engineering assignment.

Completed so far:
- Defined explicit PowerShell security standards
- Designed and iterated on a system prompt enforcing those standards
- Tested prompt behavior across multiple environments
  (chat-based testing and Google AI Studio)
- Created an initial public deployment using Lovable

Current focus:
- Evaluating consistency of prompt behavior in a deployed environment
- Refining clarification questions and refusal explanations
- Preparing for additional iteration and polish in the second project week

This project intentionally prioritizes prompt engineering, grounding,
and evaluation over full automation or production-ready tooling.

## Using the Secure Script Architect

Users describe a PowerShell automation task in natural language.
The system may ask clarifying questions before generating a script
to ensure security context is understood.

Unsafe or insecure requests will be refused with an explanation.
