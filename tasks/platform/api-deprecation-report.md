---
title: API Deprecation Readiness Report
schedule: "every monday at 9am"
supported contexts: argo cd instance, cluster
---

Analyze Kubernetes API deprecations to ensure cluster upgrade readiness.

## Deprecated API Usage Scan

- List all resources using deprecated Kubernetes APIs
- Group by deprecation timeline:
  - Removed in next minor version (critical)
  - Removed in next major version (high)
  - Deprecated but not yet scheduled for removal (medium)
- Include affected resource count per API version

## Impact Analysis

- List of affected resources (name, namespace, kind)
- Owning workloads or ArgoCD applications
- Migration path (replacement API version)
- Estimated effort to migrate

## Cluster Version Context

- Current Kubernetes version of each managed cluster
- Target upgrade version (if known)
- APIs that will break on upgrade

## Migration Progress

- Track resources already migrated to new APIs
- Resources pending migration
- Comparison with previous report

## Risk Assessment

- Clusters at highest risk for upgrade issues
- Applications with most deprecated API usage
- Third-party operators or Helm charts using deprecated APIs

## Summary Format

Present findings in a structured Markdown report with:
- Executive summary
- Critical deprecations requiring immediate action
- Detailed migration checklist
- Timeline recommendations for API updates
