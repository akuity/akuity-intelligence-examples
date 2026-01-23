# Akuity Intelligence Examples

This repository contains operational runbooks and scheduled tasks that demonstrate Akuity Intelligence's capabilities for automated incident response and proactive platform monitoring.

---

## Runbooks

Runbooks guide Akuity Intelligence's automated incident response when it detects degraded ArgoCD Applications or Kubernetes Namespaces. Each runbook follows a structured approach with symptom identification, root cause analysis, and step-by-step remediation procedures.

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

Tasks run automatically at defined intervals to generate reports, detect issues, and maintain platform health.

### ArgoCD
Monitoring for GitOps application health and sync status:
- **[argocd-sync-status-report.md](./tasks/argocd/argocd-sync-status-report.md)** - ArgoCD application sync status

### Kargo
Pipeline promotion and stage health monitoring:
- **[kargo-pipeline-health.md](./tasks/kargo/kargo-pipeline-health.md)** - Kargo promotion pipeline health

### Platform Health
Comprehensive platform monitoring, resource efficiency, and incident summaries:
- **[platform-integrity-report.md](./tasks/platform/platform-integrity-report.md)** - Comprehensive platform health report
- **[weekly-incident-summary.md](./tasks/platform/weekly-incident-summary.md)** - Weekly incident and operational summary
- **[api-deprecation-report.md](./tasks/platform/api-deprecation-report.md)** - Kubernetes API deprecation readiness

### Security
Security posture, vulnerability scanning, and certificate monitoring:
- **[expiring-certificates.md](./tasks/security/expiring-certificates.md)** - Check for expiring or failed TLS certificates
- **[image-vulnerability-report.md](./tasks/security/image-vulnerability-report.md)** - Container image CVE security scan