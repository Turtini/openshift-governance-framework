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

---

# Scoring Guidance

This maturity model is intended to support structured reflection rather than numerical competition.

However, institutions may find it useful to apply a lightweight scoring mechanism to identify dominant characteristics across operating dimensions.

## Scoring Approach

For each level described above, evaluate the degree to which the characteristics are consistently true in your environment.

Use the following qualitative scale:

- 0 — Not present
- 1 — Emerging or inconsistent
- 2 — Implemented but partially enforced
- 3 — Consistently enforced and structurally encoded

Scoring should be applied independently across key governance dimensions:

- RBAC and separation of duties
- Admission policy enforcement
- Network segmentation (ingress and egress)
- Monitoring and audit traceability
- Lifecycle and upgrade governance
- Exception handling and policy encoding

## Interpreting Results

Most institutions will exhibit characteristics across multiple levels simultaneously.

For example:

- Network segmentation may reflect Level 4 maturity
- Admission controls may reflect Level 2 maturity
- Lifecycle governance may reflect Level 3 maturity

The goal is not to "achieve Level 5" universally, but to:

- Identify structural inconsistencies
- Detect areas where governance is procedural rather than encoded
- Prioritize deliberate improvement efforts

## Executive Interpretation

Leadership should view maturity progression as a measure of institutional stability, not technical sophistication.

Higher maturity reflects:

- Reduced operational fragility
- Lower dependency on individual discretion
- Increased authorization durability
- Greater predictability across upgrade cycles

Maturity is achieved when governance intent, technical enforcement, and operational behavior are structurally aligned.

---

## Caution Against False Precision

This model is not a compliance checklist.

It does not replace formal assessment processes, and it should not be used to claim certification status.

Its purpose is diagnostic clarity and structured dialogue across platform engineering, security, and leadership stakeholders.

