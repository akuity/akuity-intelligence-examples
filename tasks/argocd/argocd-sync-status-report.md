---
title: ArgoCD Application Sync Status Report
schedule: "every day at 9am"
---

Generate a comprehensive report on the sync status of all ArgoCD applications.

## Application Sync Overview

- Provide a high-level summary of all applications and their current synchronization status.
- Categorize applications by health status: Healthy, Degraded, Progressing, Missing, and Unknown.

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

## Health Status Details

For Degraded or Progressing applications:

- Identify unhealthy resources
- Brief root cause summary if determinable
- Time in current health state

## Summary Format

Present in Markdown with:

- Quick stats dashboard (unsynced %, degraded %, progress %)
- Priority list of applications requiring attention
- Recommendations for resolving sync issues
