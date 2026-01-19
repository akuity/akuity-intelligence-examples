---
title: Expiring Certificates Check
schedule: "every day at 8am"
---

Generate a summary of all expiring certificates.

## Expiring Certificates

- List all Certificate resources (e.g. cert-manager.io/Certificate)
- Check the status fields of Certificate, CertificateRequest, and Order objects
- Identify certificates in any of these states:
  - Expiring within 21 days (warning)
  - Expiring within 7 days (critical)
  - Already expired
  - Failed or stalled renewal (e.g., ACME challenges failing, issuer not ready)
- For each problematic certificate, include:
  - Certificate name and namespace
  - Expiration date and time remaining
  - Current status and any error messages
  - Associated Secret name

## Summary Format

Present in Markdown with:

- Executive summary of expiring certificates
- Group findings by severity (critical, warning, informational)
- Alert for immediate action required
