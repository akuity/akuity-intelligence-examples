---
title: Namespace Resource Utilization Report
schedule: "every week on friday at 5pm"
---

Analyze resource utilization patterns across namespaces to identify optimization opportunities.

## Namespace Overview
- List all namespaces with active workloads
- Count of Deployments, StatefulSets, and Pods per namespace
- Total resource requests and limits per namespace

## Resource Utilization Analysis
For each namespace:
- Compare requested resources vs actual usage (if metrics available)
- Identify over-provisioned workloads (requests >> usage)
- Flag under-provisioned workloads at risk of throttling or OOM
- Calculate resource efficiency score

## Workload Right-Sizing Candidates
- List workloads with consistently low CPU utilization (< 20% of requests)
- Identify workloads with memory headroom > 50% of limits
- Flag workloads frequently hitting resource limits

## Quota and Limit Analysis
- Check namespaces with ResourceQuotas defined
- Report quota utilization percentages
- Identify namespaces approaching quota limits
- List LimitRange configurations and their effectiveness

## Resource Efficiency Opportunities
- Identify idle or rarely-used workloads
- Flag development/test workloads running in production configurations

## Cleanup Candidates
- Completed/Failed Jobs older than 7 days
- Orphaned ConfigMaps and Secrets
- Unused PersistentVolumeClaims
- Empty or inactive namespaces

## Summary Format
Present in Markdown with:
- Resource efficiency score by namespace
- Top 10 optimization opportunities
- Recommended actions with priority ranking
