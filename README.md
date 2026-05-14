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

## Status
Project 1 (Draft) – Prompt engineering and grounding phase
``


## Current Status

Project 1 implementation ongoing.

- Security standards defined and documented
- System prompt iterated and validated
- Prompt behavior tested against safe, risky, and unsafe scenarios
- Secure Script Architect deployed as a public demo using Lovable

This project focuses on prompt engineering, grounding, and evaluation rather
than full automation or production deployment.

Here is my Loveable DEMO URL:
