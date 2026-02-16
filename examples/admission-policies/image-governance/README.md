# Image Governance — Approved Registry Enforcement

## Purpose

This example demonstrates how admission policies can enforce container image provenance requirements in regulated OpenShift environments.

Restricting workload deployment to approved registries reduces supply chain risk and aligns with federal compliance expectations related to software integrity and source validation.

---

## Context

In many environments, image source validation is handled informally through code review or ticket-based oversight. This pattern illustrates how enforcement can be encoded directly into the platform using admission controls.

---

## What This Pattern Enforces

- Workloads must reference container images from defined, approved registries
- Image pulls from unauthorized external registries are rejected
- Enforcement occurs at admission time, not post-deployment

---

## What This Pattern Does Not Do

- It does not manage image scanning workflows
- It does not define registry mirroring strategies
- It does not enforce signature verification

This example focuses specifically on registry source restriction.

---

## Adaptation Guidance

Organizations should adapt:

- Approved registry domains
- Namespace scope of enforcement
- Exception handling processes
- Change management around policy updates

Policy enforcement should be coordinated with platform engineering, security, and application teams to ensure operational alignment.
