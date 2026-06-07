# Bridge Framework

Bridge Framework is the lightweight adapter framework for Unboxd Panel.

It connects external systems, protocols, tools, runtimes, and fabric units to the platform without making them part of the core.

## Canonical Definition

```text
Bridge = Minimal governed adapter across an edge
```

A bridge exists only where two bounded systems need to exchange state, events, commands, or evidence.

## Core Rule

```text
Do not expand the core.
Add a bridge.
```

The bridge must be small, explicit, observable, policy-bound, and reconcilable.

## Position

```text
Platform holds the contract.
Panel exposes the control.
Fabric provides the building block.
Bridge connects edges.
Agent operates tools.
Stable state is the objective.
```

## Bridge Stack

```text
Edge
  -> Protocol
  -> Contract
  -> Adapter
  -> Event
  -> State Mapping
  -> Policy Check
  -> Reconciliation
  -> Evidence
```

## What a Bridge Does

A bridge may:

- connect a protocol
- translate a request
- map external state to twin state
- emit CloudEvents
- invoke approved tools
- report observed state
- reconcile drift
- produce audit evidence

A bridge may not:

- hold the platform contract
- own authority
- bypass policy
- mutate state without contract
- become a second control plane
- hide execution
- increase the core surface area

## Bridge Types

```text
Kubernetes Bridge
Git Bridge
SSH Bridge
HTTP Bridge
OCI Bridge
CloudEvents Bridge
Identity Bridge
DNS Bridge
Observability Bridge
Database Bridge
Agent Tool Bridge
Multipass Bridge
Juju Bridge
Charmhub Bridge
Cloud Provider Bridge
PaaS Bridge
```

## Bridge Lifecycle

```text
Draft
  -> Registered
  -> Contracted
  -> Approved
  -> Active
  -> Observed
  -> Reconciled
  -> Suspended
  -> Retired
```

## Stable-State Loop

```text
Observe Edge
  -> Map State
  -> Compare Twin
  -> Detect Drift
  -> Evaluate Policy
  -> Execute Through Bridge
  -> Verify Result
  -> Emit Evidence
  -> Reconcile Stable State
```

## Feature Rule

```text
Feature = Bridge + Edge + Protocol + Contract + State Mapping + Policy + Reconciliation + Evidence + UI
```

## Minimal Surface Rule

A bridge is valid only if it reduces system complexity.

```text
If the bridge adds more control-plane confusion than it removes, reject it.
```

## Final Cut

```text
Bridge Framework keeps the core small while allowing the platform to compose with many systems.
```
