---
title: Stuck and Orphaned Resources Detection
schedule: "every day at 7am"
---

Identify resources that are stuck in deletion or potentially orphaned across all managed clusters.

## Stuck in Deletion
- Identify resources with a deletionTimestamp that have been pending deletion for more than 1 hour
- For each stuck resource, include:
  - Resource type, name, and namespace
  - Deletion timestamp and duration stuck
  - Finalizers preventing deletion
  - Owner references (if any)
- Group by cluster and namespace

## Orphaned Resources Analysis
- Identify ConfigMaps and Secrets not referenced by any workload
- Find PersistentVolumeClaims in Released or Failed state
- Detect Services with no backing endpoints for extended periods
- List completed or failed Jobs older than 7 days

## Namespace Cleanup Candidates
- Identify namespaces with no running workloads
- List namespaces in Terminating state for more than 10 minutes
- Flag empty namespaces (no resources except default ServiceAccount)

## Resource Cleanup Recommendations
For each category:
- Estimated resources that could be safely cleaned up
- Potential resource savings (if applicable)
- Risk assessment for cleanup actions

## Summary Format
Present in Markdown with:
- Count of stuck resources by type
- Prioritized cleanup recommendations
- Commands or actions needed (note: require approval for any deletions)
