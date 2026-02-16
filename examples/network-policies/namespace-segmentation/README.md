# Namespace Segmentation — Baseline Pattern

## Purpose

This pattern establishes a baseline network segmentation posture within a namespace by default-denying ingress traffic.

Default-deny ingress reduces lateral movement risk and forces explicit design of allowed communication pathways.

---

## Context

In many environments, network access is implicitly open within and across namespaces. While convenient, this model undermines isolation boundaries and makes it difficult to demonstrate segmentation intent during assessment.

This baseline pattern is designed to create a clear, enforceable starting point.

---

## What This Pattern Enforces

- Ingress traffic to pods in the namespace is denied by default
- Only explicitly allowed ingress is permitted (added as follow-on policies)
- Follow-on allow policies (such as ingress controller access) are applied explicitly to support Routes and shared platform services.

---

## What This Pattern Does Not Do

- It does not restrict egress traffic (baseline is ingress-focused)
- It does not define application-specific allow rules
- It does not implement service mesh policies
- This baseline set focuses on ingress segmentation. Many logging architectures also require explicit egress policies from workloads to centralized collectors.

This example provides a foundational constraint that organizations can build upon.

---

## Adaptation Guidance

Organizations should consider:

- Whether to also default-deny egress as maturity increases
- Standard allow rules for ingress controllers and monitoring tools
- Namespace labeling conventions to support policy targeting
- Change management and testing procedures to prevent service disruption
- Identify ingress requirements for platform services (ingress controller, monitoring, logging) and encode them explicitly as follow-on allow policies.

A default-deny posture should be rolled out deliberately, beginning with non-production namespaces and expanding as operational confidence increases.
