---
title: ArgoCD Application Sync Status Report
schedule: "every 6 hours"
---

Generate a comprehensive report on the sync status of all ArgoCD applications.

## Application Sync Overview
- List all ArgoCD applications and their current sync status (Synced, OutOfSync, Unknown)
- Group applications by health status (Healthy, Degraded, Progressing, Missing, Unknown)
- Calculate sync compliance rate (percentage of applications in Synced state)

## Out-of-Sync Applications
For each OutOfSync application:
- Application name and namespace
- Target cluster and destination namespace
- Duration since last successful sync
- Number of resources with drift
- Brief summary of detected drift (resource types affected)

## Failed Syncs
- Check recent application events or sync history to find failures (past 24 hours)
- List applications with recent sync failures
- Include error messages and failure reasons
- Identify recurring sync failures (same error multiple times)

## Sync Operation History
- Count of sync operations in the past 24 hours
- Success vs failure rate
- Average sync duration
- Applications with unusually long sync times

## Health Status Details
For Degraded or Progressing applications:
- Identify unhealthy resources
- Brief root cause summary if determinable
- Time in current health state

## Summary Format
Present in Markdown with:
- Quick stats dashboard (total apps, synced %, healthy %)
- Priority list of applications requiring attention
- Recommendations for resolving sync issues
