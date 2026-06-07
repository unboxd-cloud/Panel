# Fabric Protocol Gap Register

This register identifies the current gaps in Fabric Protocol, Island Bridge Architecture, Agent Island Protocol, and Unboxd Panel.

A gap is not a failure. A gap is an unclosed edge between theory and stable state.

## Gap Definition

```text
Gap = Missing Link Between Theory and Stable State
```

## Evaluation Rule

```text
Do not build across an unexplained gap.
Name the gap.
Model the gap.
Contract the gap.
Reconcile the gap.
```

## Current Gap Summary

```text
G01 Canonical Meta Model Gap
G02 Time Model Gap
G03 Relationship Model Gap
G04 Trust Model Gap
G05 Federation Model Gap
G06 Knowledge Model Gap
G07 Economic Model Gap
G08 Runtime Boundary Gap
G09 Schema / Data Contract Gap
G10 Event Taxonomy Gap
G11 Policy Decision Model Gap
G12 Reconciliation Status Model Gap
G13 Maturity Evidence Gap
G14 Panel Surface Model Gap
G15 Build Path Gap
```

---

## G01: Canonical Meta Model Gap

### Problem

Fabric Protocol has many primitives, but no single canonical meta model that makes them all data.

Current primitives:

```text
Theory
Identity
Island
Bridge
DigitalTwin
Contract
State
Event
Policy
Agent
Tool
Reconciliation
```

### Risk

Without a meta model, each feature may create its own data structure, causing drift between docs, API, database, UI, and runtime.

### Needed Model

```text
Entity
  -> Identity
  -> Metadata
  -> Type
  -> State
  -> Relationships
  -> Events
  -> Contracts
  -> Policies
  -> Evidence
```

### Closure

Create `docs/canonical-meta-model.md` and later derive schemas from it.

---

## G02: Time Model Gap

### Problem

State is defined, but time is not yet first-class.

### Risk

Reconciliation cannot be proven without before/after state, event ordering, and temporal validity.

### Needed Model

```text
Past State
Current State
Declared State
Observed State
Future State
Effective Time
Observed Time
Reconciled Time
```

### Closure

Create `docs/time-model.md`.

---

## G03: Relationship Model Gap

### Problem

Islands and bridges exist, but their relationships are not formalized.

### Risk

Ownership, dependency, delegation, and trust may become implicit bleeding edges.

### Needed Relationships

```text
contains
depends_on
owns
delegates_to
trusts
observes
controls
executes
reconciles_with
provides_evidence_for
```

### Closure

Create `docs/relationship-model.md`.

---

## G04: Trust Model Gap

### Problem

Identity, contract, and policy exist, but trust is still implicit.

### Risk

A system may be allowed to act without trust evidence, or trust may remain static when behavior changes.

### Needed Model

```text
Trust = Identity + Contract + Policy + Evidence + Reconciliation History
```

Trust must drift and reconcile like state.

### Closure

Create `docs/trust-model.md`.

---

## G05: Federation Model Gap

### Problem

Island Bridge Architecture avoids uncontrolled mesh, but federation is not yet defined.

### Risk

Many islands may connect without a clear governance model for cooperation.

### Needed Model

```text
Federation = Locally Stable Islands + Governed Bridges + Shared Contract Rules
```

### Closure

Create `docs/federation-model.md`.

---

## G06: Knowledge Model Gap

### Problem

Agents can reason, but knowledge is not yet a governed island.

### Risk

Agents may act on unsourced, stale, or unverified knowledge.

### Needed Model

```text
Knowledge Island = Source + Claim + Evidence + Version + Policy + Reconciliation
```

### Closure

Create `docs/knowledge-model.md`.

---

## G07: Economic Model Gap

### Problem

Solution as a Service exists, but value, cost, usage, and accountability are not modeled.

### Risk

The product may deliver operations without measurable service value.

### Needed Model

```text
Value = Stable State Outcome + Evidence + Usage + Cost + Accountability
```

### Closure

Create `docs/economic-model.md`.

---

## G08: Runtime Boundary Gap

### Problem

Ubuntu, Multipass, k3s, OCI, CloudEvents are named, but runtime boundaries are not formalized.

### Risk

Runtime choices may leak into the protocol core.

### Needed Boundary

```text
Protocol Core != Runtime Implementation
```

Core remains stable. Runtime sits behind bridges.

### Closure

Create `docs/runtime-boundary.md`.

---

## G09: Schema / Data Contract Gap

### Problem

No machine-readable schema exists yet for Fabric Protocol primitives.

### Risk

Docs cannot become APIs, database tables, CRDs, events, or UI forms consistently.

### Needed Artifacts

```text
schemas/fabric/entity.schema.json
schemas/fabric/island.schema.json
schemas/fabric/bridge.schema.json
schemas/fabric/twin.schema.json
schemas/fabric/contract.schema.json
schemas/fabric/event.schema.json
schemas/fabric/policy.schema.json
```

### Closure

Create schema package after Canonical Meta Model.

---

## G10: Event Taxonomy Gap

### Problem

CloudEvents is selected as envelope, but event types are not defined.

### Risk

Evidence stream becomes inconsistent and non-queryable.

### Needed Taxonomy

```text
island.declared
island.observed
island.drift.detected
bridge.crossing.requested
contract.evaluated
policy.allowed
policy.denied
agent.tool.requested
agent.tool.executed
reconciliation.started
reconciliation.completed
stable_state.proven
```

### Closure

Create `docs/event-taxonomy.md`.

---

## G11: Policy Decision Model Gap

### Problem

Policy outcomes exist, but decision records are not formalized.

### Risk

Approvals, denials, escalations, and uncertainty cannot be audited consistently.

### Needed Model

```text
PolicyDecision
  id
  subject
  action
  resource
  context
  result
  reason
  evidence
  timestamp
```

### Closure

Create `docs/policy-decision-model.md`.

---

## G12: Reconciliation Status Model Gap

### Problem

Reconciliation is defined as a loop, but status states are missing.

### Risk

The panel cannot show reliable operational truth.

### Needed States

```text
unknown
observing
in_sync
drift_detected
policy_pending
approval_pending
executing
verifying
reconciled
failed
escalated
suspended
```

### Closure

Create `docs/reconciliation-status-model.md`.

---

## G13: Maturity Evidence Gap

### Problem

Maturity is named, but evidence levels are not defined.

### Risk

The platform cannot distinguish prototype, usable, governed, and production-grade capabilities.

### Needed Levels

```text
L0 undefined
L1 described
L2 modeled
L3 contracted
L4 observable
L5 reconcilable
L6 governed
L7 production-grade
```

### Closure

Create `docs/maturity-evidence-model.md`.

---

## G14: Panel Surface Model Gap

### Problem

The panel is defined as control surface, but primary surfaces are not modeled.

### Risk

UI can drift into random screens instead of protocol-backed controls.

### Needed Surfaces

```text
Islands
Bridges
Twins
Contracts
Events
Policies
Agents
Tools
Drift
Reconciliation
Evidence
Maturity
```

### Closure

Create `docs/panel-surface-model.md`.

---

## G15: Build Path Gap

### Problem

The docs now define the theory and protocol, but the implementation path is not sequenced.

### Risk

Build may start with UI before schema, or runtime before protocol contracts.

### Needed Build Order

```text
1. Canonical Meta Model
2. Schemas
3. Event Taxonomy
4. Reconciliation Status Model
5. Minimal API
6. Minimal State Store
7. Local Multipass/k3s Lab
8. Panel UI
9. Agent Tool Bridge
10. Maturity Evidence
```

### Closure

Create `docs/build-order.md`.

---

## Priority Order

```text
P0 Canonical Meta Model
P0 Schema / Data Contract
P0 Event Taxonomy
P0 Reconciliation Status Model
P1 Time Model
P1 Relationship Model
P1 Runtime Boundary
P1 Policy Decision Model
P2 Trust Model
P2 Federation Model
P2 Knowledge Model
P2 Economic Model
P2 Maturity Evidence
P3 Panel Surface Model
P3 Build Path
```

## Final Cut

```text
The Fabric Protocol is strong enough to proceed, but not yet strong enough to code blindly.
The next closure point is the Canonical Meta Model.
```
