---
title: Daily Platform Integrity Report
schedule: "every day at 9am"
supported contexts: argo cd instance, cluster
---

Generate a comprehensive daily platform health report covering the following areas:

## Incident Summary

- Retrieve all incidents from the past 24 hours
- Group incidents by status (resolved vs unresolved)
- Highlight any recurring patterns or affected applications
- Include incident count and average resolution time

## Resource Health

- Identify resources stuck in deletion state (finalizers blocking cleanup)
- List any resources in unknown or degraded health status
- Check for pods in CrashLoopBackOff or ImagePullBackOff states

## Security Posture

- Summarize container image CVEs by severity (Critical, High, Medium, Low)
- List the top 5 most vulnerable images with their affected workloads
- Note any images without vulnerability scan data

## API Deprecations

- List all deprecated Kubernetes APIs currently in use
- Group by deprecation severity and target removal version
- Identify affected workloads that need migration

## Summary Format

Present findings in a structured Markdown report with:
- Executive summary (1-2 sentences on overall platform health)
- Metrics dashboard (incident count, resource issues, CVE counts)
- Prioritized action items requiring attention
- Trend comparison with previous report if available
