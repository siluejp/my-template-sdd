---
name: security-and-hardening
description: Use when a change touches authentication, authorization, secrets, user data, external services, or deployment.
---

# Security and Hardening

## When to Use
- Authentication, authorization, or permissions change.
- User data, secrets, uploads, payments, or external APIs are involved.
- Deployment, CI, logging, or configuration changes may expose data.

## Process
1. Identify assets, trust boundaries, and data flows.
2. Check authorization before data access and state changes.
3. Validate inputs and handle failure paths.
4. Avoid logging secrets or personal data.
5. Record residual risks and required operational controls.

## Verification
- Sensitive data is not committed or logged.
- Access control decisions are explicit and tested where possible.
- Error handling does not leak implementation details.
- External integrations have timeout, retry, and failure behavior considered.

## Red Flags
- Security review happens only after release.
- Examples contain real tokens or personal data.
- Authorization is assumed because the UI hides an action.
