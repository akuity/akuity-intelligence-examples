---
title: Over-Provisioned Workloads Report
schedule: "every day at 9am"
supported contexts: argo cd instance, cluster
---

Generate a report identifying over-provisioned workloads where resource requests significantly exceed actual usage, helping optimize cluster resource allocation and reduce costs.

## Resource Usage Analysis

- Query all container resources using the list-container-resources tool
- For each container, compare:
  - CPU request vs actual CPU usage
  - Memory request vs actual memory usage
  - CPU limit vs actual CPU usage
  - Memory limit vs actual memory usage

## Over-Provisioned Detection Criteria

Flag containers as over-provisioned when:
- CPU request is more than 2x the actual CPU usage
- Memory request is more than 2x the actual memory usage
- Resources have been consistently underutilized over the reporting period

## Workload Categories

Group over-provisioned workloads by:
- Severity: Critical (>5x over-provisioned), High (3-5x), Medium (2-3x)
- Namespace
- Workload type (Deployment, StatefulSet, DaemonSet)
- Cluster

## Top Over-Provisioned Workloads

- List the top 20 most over-provisioned containers
- Include for each:
  - Container name and pod name
  - Namespace and cluster
  - Current requests vs actual usage (CPU and memory)
  - Recommended right-sized values
  - Estimated resource savings

## Cost Impact Estimation

- Calculate total wasted resources across all over-provisioned workloads
- Estimate potential savings in terms of:
  - CPU cores that could be reclaimed
  - Memory (GB) that could be reclaimed
- Identify namespaces with highest waste

## Under-Provisioned Detection

Also identify potentially under-provisioned workloads where:
- Actual usage approaches or exceeds limits
- Containers are experiencing OOM kills or CPU throttling
- This helps prevent performance issues while optimizing

## Recommendations

Provide actionable recommendations:
- Specific resource adjustment suggestions per workload
- Priority ranking based on potential savings
- Namespaces that need resource quota review

## Summary Format

Present in Markdown with:
- Executive summary of resource efficiency
- Total potential savings (CPU cores, memory GB)
- Top 10 workloads requiring immediate attention
- Trend comparison with previous report if available
- Quick wins vs long-term optimization opportunities
