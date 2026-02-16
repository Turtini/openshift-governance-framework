# Privileged Workload Restriction

## Purpose

This example demonstrates how admission policies can restrict privileged workload configurations in regulated OpenShift environments.

Privileged containers and broad host access (hostNetwork, hostPID, hostIPC) significantly expand the attack surface and are commonly restricted by institutional policy.

---

## Context

In many environments, privileged workload approval is handled through manual review or informal exception processes. This pattern illustrates how platform guardrails can enforce baseline constraints consistently at admission time.

---

## What This Pattern Enforces

- Rejects containers configured as `privileged: true`
- Rejects pods requesting host-level namespaces (hostNetwork, hostPID, hostIPC)
- Rejects pods requesting hostPath volumes (optional but commonly restricted)

These constraints reduce high-risk workload deployments that bypass normal isolation boundaries.

---

## What This Pattern Does Not Do

- It does not manage OpenShift SCC (Security Context Constraints) directly
- It does not define exception workflows or break-glass processes
- It does not replace institutional review for legitimate privileged workloads

This example demonstrates baseline restriction guardrails. Organizations should define a documented exception path when privileged access is mission-required.

---

## Adaptation Guidance

Organizations should adapt:

- Namespace scope (cluster-wide vs selected namespaces)
- Exception strategy (allow-list namespaces, service accounts, or labels)
- Enforcement posture (audit vs enforce)
- Alignment with OpenShift SCC and Pod Security expectations

Admission policies should be tested in non-production environments prior to enforcement.
