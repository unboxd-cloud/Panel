# Fabric Protocol

Fabric Protocol is the canonical protocol for Island Bridge Architecture.

It defines how bounded islands, governed bridges, digital twins, contracts, policies, events, agents, tools, and reconciliation loops compose into stable-state operations.

## Canonical Definition

```text
Fabric Protocol = Theory + Identity + Island + Bridge + Twin + Contract + State + Event + Policy + Reconciliation + Evidence
```

The protocol exists to make control explicit, bounded, observable, auditable, and composable.

## Core Objective

```text
Stable State
```

Stable state is the only success condition.

```text
Stable State = Declared Intent + Verified Observation + Accepted Reconciliation + Audit Evidence
```

## Protocol Laws

```text
1. Everything begins as theory.
2. Every controlled thing must have identity.
3. Every controlled unit is an island or belongs to an island.
4. Every island has a digital twin.
5. Every edge crossing requires a bridge.
6. Every bridge requires a contract.
7. Every contract is evaluated by policy.
8. Every meaningful transition emits an event.
9. Every execution must be reconciled.
10. Every reconciliation must produce evidence.
11. No bleeding edges.
12. Stable state is local first, then composed globally.
```

## Core Primitives

Fabric Protocol has twelve primitives:

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

Everything else is a runtime, adapter, UI, package, service, or bridge-specific implementation.

## 1. Theory

Theory explains what something is, why it exists, where it belongs, and what makes it valid.

```text
Theory -> Model -> Contract -> Operation -> Evidence
```

No feature is valid without a clear theory.

## 2. Identity

Identity makes control accountable.

Every important object must be identifiable:

```text
Tenant
Profile
Device
Island
Bridge
DigitalTwin
Contract
Policy
Agent
Tool
Model
Event
Operation
Evidence
```

Rule:

```text
No observation without identity.
No action without identity.
No audit without identity.
```

## 3. Island

An island is a bounded fabric unit with local state, local policy, local events, and local reconciliation.

```text
Island = Bounded Fabric Unit + Local Reconciliation
```

Examples:

```text
Ubuntu VM
Server
Kubernetes cluster
Namespace
Tenant
Application
Database
Agent runtime
Tool runtime
Identity domain
Cloud account
Edge location
```

## 4. Bridge

A bridge is the only valid way for state, authority, command, context, or evidence to cross an island boundary.

```text
Bridge = Edge + Protocol + Contract + State Mapping + Policy + Evidence + Reconciliation
```

Rule:

```text
No bridge, no crossing.
```

## 5. Digital Twin

A digital twin is the governed data representation of an island.

```text
DigitalTwin = Identity + Metadata + Declared State + Observed State + Events + Contracts + Policies + Drift + Reconciliation History + Evidence
```

The panel controls the twin.
Reality changes through protocols.
Stable state exists when twin and reality reconcile.

## 6. Contract

The platform holds the contract.

A contract defines allowed control:

```text
who can act
what can be done
which bridge may be used
which protocol is allowed
which tool may execute
which state may change
which policy must evaluate
which evidence must be emitted
which reconciliation proves completion
```

Rule:

```text
No control without contract.
```

## 7. State

State has two required forms:

```text
Declared State = what should exist
Observed State = what reality reports
```

Drift is the explainable difference between them.

```text
Drift = Declared State - Observed State
```

## 8. Event

Events are evidence.

Fabric Protocol uses CloudEvents-compatible event envelopes for important transitions.

Rule:

```text
If it happened, emit an event.
If it changed state, update the twin.
If it crossed an edge, evaluate the bridge contract.
If it changed reality, reconcile stable state.
```

## 9. Policy

Policy decides whether control is allowed.

```text
Policy = Rule that evaluates identity, contract, state, risk, context, and evidence
```

Policy may return:

```text
allow
deny
require_approval
escalate
require_more_evidence
```

## 10. Agent

Agent is operator of tool.

```text
Agent = Contract-bound operator of approved tools
```

The agent may observe, explain, prepare, execute approved tool calls, verify, and report.

The agent may not own authority, bypass policy, mutate state without contract, hide execution, or become the stable core.

## 11. Tool

A tool is a bounded capability.

A tool must define:

```text
identity
purpose
input contract
output contract
protocol
permission boundary
side effects
risk level
event evidence
rollback or reconciliation path
```

Rule:

```text
No tool without contract.
```

## 12. Reconciliation

Reconciliation proves stable state.

```text
Reconciliation = Observe + Compare + Decide + Act + Verify + Audit
```

Execution is not success.
Only verified reconciliation is success.

## No Bleeding Edges

Nothing crosses an island boundary unless it has:

```text
identity
protocol
bridge
contract
policy
event evidence
reconciliation path
audit trail
```

This prevents leakage of:

```text
authority
state
secrets
context
execution
failure
dependency
drift
```

## Time Model

Fabric Protocol treats state as temporal.

```text
Past State     = what was true
Current State  = what is observed now
Declared State = what should be true
Future State   = what is intended after reconciliation
```

Every reconciliation must record the transition from before to after.

## Relationship Model

Islands and twins may relate through explicit relationships:

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
```

Relationships must be represented as governed data, not hidden assumptions.

## Trust Model

Trust is evidence-based.

```text
Trust = Identity + Contract + Policy + Evidence + Reconciliation History
```

Trust can drift.
Trust must be reconciled.

## Knowledge Model

Knowledge is also an island when it affects control.

```text
Knowledge Island = Source + Claim + Evidence + Version + Policy + Reconciliation
```

No agent should act on knowledge that cannot be sourced, versioned, or evaluated.

## Federation Model

Federation is composition without uncontrolled mesh.

```text
Federation = Locally Stable Islands + Governed Bridges + Shared Contract Rules
```

Each island remains bounded.
Global stable state is composed from local stable states and bridge evidence.

## Economic Model

Service delivery must be measurable.

```text
Value = Stable State Outcome + Evidence + Usage + Cost + Accountability
```

The platform should track usage, cost, service obligation, and delivered outcome as data.

## Gaps Model

A gap is a missing link between theory and stable state.

```text
Gap = Missing Theory, Model, Identity, Contract, State, Event, Policy, Bridge, Reconciliation, Evidence, or Maturity
```

Do not build across unexplained gaps.

## Runtime Profile

Fabric Protocol stays lightweight.

Core runtime profile:

```text
Ubuntu
Multipass for local island lab
k3s for lightweight Kubernetes reconciliation
OCI-compatible capability packaging
CloudEvents-compatible evidence
```

Optional systems must stay behind bridges:

```text
Juju
Charmhub
Cloud providers
PaaS platforms
Identity providers
Observability systems
Databases
```

## Feature Formula

A valid feature must have the protocol shape:

```text
Feature = Theory + Identity + Island + Bridge + Twin + Contract + State + Event + Policy + Reconciliation + Evidence + UI
```

## Product Shape

```text
Unboxd Panel
= Stable-State Control Panel
+ Fabric Protocol
+ Island Bridge Architecture
+ Agent Island Protocol
+ Digital Twin Model
+ CloudEvents Evidence
+ OCI-Compatible Capabilities
+ K8s-Native Reconciliation
+ Solution as a Service
```

## Final Cut

```text
Fabric Protocol turns islands, bridges, contracts, twins, events, policies, agents, tools, and reconciliation loops into one stable-state operating system.
```
