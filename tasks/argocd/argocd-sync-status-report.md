---
title: ArgoCD Application Sync Status Report
schedule: "every day at 9am"
supported contexts: argo cd application
---

Generate a comprehensive report on the sync status of the specified ArgoCD application.

## Application Overview

- Provide a summary of the application and its current synchronization status.
- Report its health status: Healthy, Degraded, Progressing, Missing, or Unknown.

## Sync Status

If the application is OutOfSync:

- Target cluster and destination namespace
- Duration since last successful sync
- Number of resources with drift
- Brief summary of detected drift (resource types affected)

## Sync History

- Check recent application events or sync history to find failures (past 24 hours)
- Include error messages and failure reasons if any
- Identify recurring sync failures

## Health Status Details

If the application is Degraded or Progressing:

- Identify unhealthy resources
- Brief root cause summary if determinable
- Time in current health state

## Summary Format

Present in Markdown with:
- Current Health and Sync Status
- Summary of any issues (drift, sync failures, unhealthy resources)
- Recommendations for resolving issues
