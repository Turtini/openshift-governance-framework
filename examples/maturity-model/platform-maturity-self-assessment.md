# Platform Maturity Self-Assessment

This assessment framework is designed to help institutions identify observable characteristics of their current OpenShift operating model.

It is not a scoring mechanism. It is a structural reflection tool.

---

## Level 1 — Reactive Deployment

### Characteristics

- Platform deployed primarily for application hosting
- Governance enforced through ticket review or informal process
- Broad administrative access granted for operational convenience
- Minimal namespace segmentation
- Monitoring focused primarily on availability

### Symptoms

- Configuration drift over time
- Access reviews performed manually or inconsistently
- Upgrade cycles are disruptive
- Audit preparation is event-driven rather than continuous

---

## Level 2 — Procedural Governance

### Characteristics

- Documented governance intent exists
- Role separation discussed but not consistently enforced technically
- Some network policies implemented
- Admission controls applied inconsistently
- Monitoring and logging centralized but not tightly integrated into governance

### Symptoms

- Security posture depends heavily on key personnel
- Governance boundaries occasionally bypassed for expediency
- Exceptions handled manually without structural encoding
- Authorization maintained, but brittle

---

## Level 3 — Enforced Governance

### Characteristics

- RBAC reflects documented responsibility boundaries
- Admission policies encode baseline guardrails
- Namespace labeling standardized
- Default-deny ingress posture implemented
- Monitoring captures governance-relevant events

### Symptoms

- Reduced configuration drift
- Clear ownership of workloads
- Exceptions documented and traceable
- Upgrade cadence aligned to vendor lifecycle

At this level, governance becomes structural rather than discretionary.

---

## Level 4 — Operationalized Authorization

### Characteristics

- Default-deny ingress and egress segmentation enforced
- Policy definitions version-controlled
- Role and policy changes subject to review workflows
- Monitoring integrated with compliance and reporting processes
- Governance posture resilient to personnel transitions

### Symptoms

- Audit preparation requires minimal retrospective reconstruction
- Platform upgrades executed predictably
- Security posture observable in system behavior
- Institutional knowledge encoded in configuration

Authorization durability becomes sustainable.

---

## Level 5 — Institutional Coherence

### Characteristics

- Governance, monitoring, and lifecycle management operate as a unified system
- Policy exceptions encoded structurally rather than granted informally
- Configuration managed declaratively across environments
- Platform metrics inform governance decisions
- Continuous improvement driven by measurable signals

### Symptoms

- Governance changes propagate predictably
- Authorization posture stable across upgrade cycles
- Platform operations transparent to leadership
- Institutional continuity independent of individual operators

At this level, the platform is not merely compliant. It is structurally aligned with mission durability.
