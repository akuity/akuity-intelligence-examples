# Akuity Intelligence Examples

This repository contains operational runbooks and scheduled tasks that demonstrate Akuity Intelligence's capabilities for automated incident response and proactive platform monitoring.

## Scheduled Tasks

Scheduled tasks run automatically at defined intervals to generate reports, detect issues, and maintain platform health. Each task uses a simple frontmatter format with `title` and `schedule` fields.

### Daily Checks
Automated daily monitoring for security, health, and operational hygiene:
- **[expiring-certificates.md](./tasks/checklogs/expiring-certificates.md)** - Check for expiring or failed TLS certificates (8am)
- **[image-vulnerability-report.md](./tasks/checklogs/image-vulnerability-report.md)** - Container image CVE security scan (6am)
- **[platform-integrity-reports.md](./tasks/checklogs/platform-integrity-reports.md)** - Comprehensive daily platform health report (9am)
- **[stuck-resources-cleanup.md](./tasks/checklogs/stuck-resources-cleanup.md)** - Detect orphaned and stuck-in-deletion resources (7am)

### Periodic Checks
Frequent monitoring for GitOps and deployment pipeline health:
- **[argocd-sync-status-report.md](./tasks/checklogs/argocd-sync-status-report.md)** - ArgoCD application sync status (every 6 hours)
- **[kargo-pipeline-health.md](./tasks/checklogs/kargo-pipeline-health.md)** - Kargo promotion pipeline health (every 4 hours)
- **[workload-health-report.md](./tasks/checklogs/workload-health-report.md)** - Workload stability and restart analysis (every 12 hours)

### Weekly Reports
Strategic weekly summaries for planning and optimization:
- **[weekly-incident-summary.md](./tasks/checklogs/weekly-incident-summary.md)** - Weekly incident and operational summary (Mondays 9am)
- **[resource-utilization-report.md](./tasks/checklogs/resource-utilization-report.md)** - Resource utilization and cost optimization (Fridays 5pm)
- **[api-deprecation-report.md](./tasks/checklogs/api-deprecation-report.md)** - Kubernetes API deprecation readiness (Wednesdays 10am)

---

## Runbooks

Runbooks guide Akuity Intelligence's automated incident response when it detects degraded ArgoCD Applications or Kubernetes Namespaces. Each runbook follows a structured approach with symptom identification, root cause analysis, and step-by-step remediation procedures.

## Runbook Categories

### ArgoCD Application Issues
Runbooks for health, sync, and deployment issues surfaced through Argo CD:
- **[argocd-app-degraded.md](./runbooks/argocd/argocd-app-degraded.md)** - Application health degraded with failing resources
- **[argocd-app-out-of-sync.md](./runbooks/argocd/argocd-app-out-of-sync.md)** - Applications showing out-of-sync status
- **[argocd-app-sync-failure.md](./runbooks/argocd/argocd-app-sync-failure.md)** - Sync operations failing or timing out

### Infrastructure & Cluster Issues  
Cluster-level infrastructure problems and resource constraints:
- **[pod-pending-scheduling.md](./runbooks/infra/pod-pending-scheduling.md)** - Pods stuck in pending due to scheduling constraints
- **[pvc-binding-failure.md](./runbooks/infra/pvc-binding-failure.md)** - Persistent volume claim binding failures
- **[time-drift.md](./runbooks/infra/time-drift.md)** - Time synchronization issues between cluster nodes

### Network & Connectivity Issues
Network dataplane and service connectivity diagnostics:
- **[cni-networking.md](./runbooks/networking/cni-networking.md)** - CNI and pod networking problems
- **[service-connectivity.md](./runbooks/networking/service-connectivity.md)** - Service discovery and connectivity failures

### Pod-Level Problems
Per-pod reliability scenarios and runtime issues:
- **[image-pull-failure.md](./runbooks/pod-issues/image-pull-failure.md)** - Container image pull failures and registry issues
- **[pod-evictions.md](./runbooks/pod-issues/pod-evictions.md)** - Pod evictions due to resource pressure
- **[pod-health-issues.md](./runbooks/pod-issues/pod-health-issues.md)** - Pod health check failures and readiness issues

### Security & Access Control
Access control and policy denials that block workloads:
- **[rbac-denials.md](./runbooks/security/rbac-denials.md)** - RBAC permission denials and authorization failures

---

## Tasks

Tasks run automatically at defined intervals to generate reports, detect issues, and maintain platform health. Each task uses a simple frontmatter format with `title` and `schedule` fields.

### ArgoCD
Monitoring for GitOps application health and sync status:
- **[argocd-sync-status-report.md](./tasks/argocd/argocd-sync-status-report.md)** - ArgoCD application sync status (every 6 hours)

### Kargo
Pipeline promotion and stage health monitoring:
- **[kargo-pipeline-health.md](./tasks/kargo/kargo-pipeline-health.md)** - Kargo promotion pipeline health (every 4 hours)

### Platform Health
Comprehensive platform monitoring, resource efficiency, and incident summaries:
- **[platform-integrity-reports.md](./tasks/platform/platform-integrity-reports.md)** - Comprehensive daily platform health report (9am)
- **[resource-utilization-report.md](./tasks/platform/resource-utilization-report.md)** - Resource efficiency and quota analysis (Fridays 5pm)
- **[stuck-resources-cleanup.md](./tasks/platform/stuck-resources-cleanup.md)** - Detect orphaned and stuck-in-deletion resources (7am)
- **[weekly-incident-summary.md](./tasks/platform/weekly-incident-summary.md)** - Weekly incident and operational summary (Mondays 9am)
- **[workload-health-report.md](./tasks/platform/workload-health-report.md)** - Workload stability and restart analysis (every 12 hours)
- **[api-deprecation-report.md](./tasks/platform/api-deprecation-report.md)** - Kubernetes API deprecation readiness (Wednesdays 10am)

### Security
Security posture, vulnerability scanning, and certificate monitoring:
- **[expiring-certificates.md](./tasks/security/expiring-certificates.md)** - Check for expiring or failed TLS certificates (8am)
- **[image-vulnerability-report.md](./tasks/security/image-vulnerability-report.md)** - Container image CVE security scan (6am)
