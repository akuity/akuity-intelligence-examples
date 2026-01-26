---
title: Weekly Incident Summary Report
schedule: "every monday at 9am"
supported contexts: argo cd instance, cluster
---

Generate a weekly summary of all incidents and operational events across the platform.

## Incident Statistics

- Total incidents created in the past 7 days
- Breakdown by status: resolved, unresolved

## Incident Categories

Group incidents by root cause type:

- Application failures (crashes, probe failures)
- Resource issues (OOM, scheduling failures)
- Configuration errors (sync failures, missing secrets)
- Infrastructure problems (networking, storage)
- External dependencies (registry, external services)

## Top Affected Resources

- List applications with the most incidents
- List namespaces with the most incidents
- List clusters with the most incidents

## Resolution Patterns

- Most common resolution actions taken
- Incidents requiring manual intervention vs auto-resolved
- Average number of tool calls per incident resolution

## Recurring Issues

- Identify incidents that occurred multiple times on the same resource
- Flag issues that have not been permanently resolved
- Detect patterns indicating systemic problems

## Trends and Comparisons

- Compare incident volume with previous weeks
- Identify improving or degrading areas
- Highlight successful remediation patterns

## Summary Format

Present in Markdown with:

- Executive summary of operational health
- Key metrics dashboard
- Top 5 issues requiring attention
- Recommendations for reducing incident volume
