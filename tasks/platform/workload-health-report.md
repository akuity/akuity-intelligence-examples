---
title: Workload Health and Restart Report
schedule: "every 12 hours"
---

Analyze workload stability and identify frequently restarting containers across all managed clusters.

## Container Restart Analysis
- List all containers with restart count > 3 in the past 24 hours
- Group restarts by reason:
  - OOMKilled (memory issues)
  - Error/CrashLoopBackOff (application failures)
  - Evicted (resource pressure)
  - Preempted (priority-based eviction)
- For each high-restart workload, include:
  - Workload type, name, and namespace
  - Container name and restart count
  - Last restart reason and time
  - Current resource requests/limits
  - Current CPU/Memory usage (from resource columns)

## Pod Health Status
- List all pods currently in non-Ready state
- Identify pods failing readiness or liveness probes
- Check for pods stuck in Pending, ContainerCreating, or Terminating states
- Flag pods with high restart counts (> 10 total restarts)

## Workload Availability
- Calculate availability percentage for Deployments and StatefulSets
- Identify workloads with fewer ready replicas than desired
- List workloads with pending rollouts or stuck updates

## Trend Analysis
- Compare restart counts with previous report period
- Highlight workloads with increasing restart frequency
- Identify patterns (time-based, event-correlated)

## Summary Format
Present in Markdown with:
- Stability score (percentage of healthy pods)
- Top 10 most unstable workloads
- Recommended actions for investigation
- Resource adjustment suggestions for OOMKilled containers
