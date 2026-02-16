# Separation of Duties (RBAC) — Reference Pattern

## Purpose

This reference pattern illustrates a separation-of-duties approach for regulated OpenShift environments by distinguishing:

- Platform governance responsibilities (cluster-scoped)
- Application operations responsibilities (namespace-scoped)

## Context

In many federal environments, governance becomes person-dependent when broad administrative access is granted for convenience. This pattern demonstrates how responsibility boundaries can be reflected in RBAC constructs so that governance is enforceable rather than procedural.

## What This Pattern Enforces

- Platform governance roles that avoid broad cluster-admin usage
- Namespace administration scoped to application responsibilities
- Clear distinction between platform lifecycle responsibilities and application operations

## What This Pattern Does Not Do

- It does not implement a full enterprise RBAC model
- It does not map to any single agency policy
- It does not address identity provider group naming conventions

## Files

- `01-platform-roles.yaml` — illustrative cluster-scoped roles for platform governance
- `02-namespace-roles.yaml` — illustrative namespace-scoped roles for application administration
- `03-bindings.yaml` — example role bindings demonstrating how responsibilities are assigned

## Adaptation Guidance

Organizations should adapt:

- Group names and identity bindings to match institutional IdP structure
- Namespace patterns and workload ownership models
- Review and approval workflows around role changes

The objective is not role completeness, but enforceable responsibility boundaries.
