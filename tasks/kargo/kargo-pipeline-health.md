---
title: Kargo Promotion Pipeline Health Check
schedule: "every 4 hours"
---

Monitor the health and status of Kargo promotion pipelines across all projects.

## Project Overview
- List all Kargo projects with their current status
- Count of active stages, warehouses, and pending promotions per project

## Warehouse Status
- Check all Warehouses for recent refresh status and errors
- Identify Warehouses that haven't produced new Freight in expected intervals
- List any Warehouses with scan/refresh errors

## Stage Health
For each Stage:
- Current Freight version deployed
- Time since last successful promotion
- Any pending or in-progress promotions
- Health status of the Stage

## Promotion Analysis
- Retrieve promotion history from the past 24 hours
- Group by status: Succeeded, Failed, Running, Pending
- For failed promotions, include:
  - Stage name and target Freight
  - Failure reason and error messages
  - Time of failure

## Pipeline Flow Assessment
- Identify bottlenecks where Freight is waiting for promotion
- Detect stages that are significantly behind their upstream sources
- Flag any stages with auto-promotion disabled that have pending Freight

## Summary Format
Present in Markdown with:
- Pipeline health score per project
- Count of successful vs failed promotions (last 24h)
- Stages requiring manual intervention
- Recommendations for pipeline optimization
