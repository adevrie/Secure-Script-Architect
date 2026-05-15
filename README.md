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

## Honest Limits

This system does not validate scripts against a live environment.
It does not replace peer review or security tooling.
Prompt enforcement is policy-based, not a formal security boundary.
UI is intentionally minimal.

## Tools Used

Gemini & CoPilot LLMs for prompt iteration and testing.
Google AI Studio (Gemini) for system instruction validation.
Lovable for deployment and public demo.
GitHub for source control and documentation.
Visual Studio Code for editing and iteration.

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

## Live Demo (Work in Progress)

A public-facing demo of the Secure Script Architect is deployed using Lovable
to demonstrate the system prompt and security enforcement behavior.

Live demo:
https://secure-script-architect.lovable.app

The Lovable deployment embeds the system prompt documented in
System_Prompt.md and enforces the security rules defined in
Security_Standards.md. The Lovable-generated repository is treated as
an implementation artifact, while this repository remains the source
of truth for design, iteration, and evaluation.


## Using the Secure Script Architect

Users describe a PowerShell automation task in natural language.
The system may ask clarifying questions before generating a script
to ensure security context is understood.

Unsafe or insecure requests will be refused with an explanation.
