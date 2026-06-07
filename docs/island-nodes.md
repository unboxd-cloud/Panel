# Island Nodes

Island nodes are bounded fabric units with no bleeding edges.

An island node can operate, observe, reconcile, and prove its own local state before participating in a larger fabric.

## Canonical Definition

```text
Island Node = Bounded Fabric Unit With Local Reconciliation
```

An island node is not isolated forever.
It is isolated by default and connected by contract.

## Core Rule

```text
No Bleeding Edges
```

Nothing crosses a node boundary unless it has:

- identity
- protocol
- contract
- bridge
- policy
- event evidence
- reconciliation path
- audit trail

## Why Island Nodes

Large distributed systems become unstable when every part can freely reach every other part.

Island nodes prevent uncontrolled spread of:

- authority
- state
- failure
- secrets
- context
- dependency
- execution
- drift

## Island Node Shape

```text
Island Node
  -> Identity
  -> Metadata
  -> Declared State
  -> Observed State
  -> Local Policy
  -> Local Event Log
  -> Local Reconciliation Loop
  -> Bridge Boundary
  -> Audit Evidence
```

## Boundary Rule

```text
Inside the node: local control.
Across the edge: contract-bound bridge.
Outside the node: no implicit trust.
```

## No Bleeding Edges Means

No implicit mutation.
No unmanaged network path.
No hidden tunnel.
No shared authority by accident.
No state leakage.
No context leakage.
No secret leakage.
No uncontrolled dependency.
No direct control without contract.

## Edge Crossing Model

```text
Island Node A
  -> Bridge
  -> Contract
  -> Policy
  -> CloudEvent
  -> Bridge
  -> Island Node B
```

## Local Stable-State Loop

Every island node must reconcile itself first.

```text
Declare Local State
  -> Observe Local Reality
  -> Detect Local Drift
  -> Evaluate Local Policy
  -> Execute Local Action
  -> Verify Local Result
  -> Emit Evidence
  -> Prove Local Stable State
```

## Fabric Composition

A fabric is composed from island nodes.

```text
Island Node
  + Island Node
  + Island Node
  = Governed Fabric
```

The fabric is not a mesh of uncontrolled edges.
The fabric is a composition of governed islands connected through bridges.

## Panel Role

Panel does not erase island boundaries.

Panel observes and controls island nodes through contracts and bridges.

```text
Panel
  -> Platform Contract
  -> Bridge
  -> Island Node
  -> Local Reconciliation
  -> Stable State
```

## Multipass Fit

Each Multipass Ubuntu VM can be treated as an island node.

```text
multipass VM
  -> Ubuntu
  -> k3s node
  -> Fabric Unit
  -> Island Node
  -> Digital Twin
```

## Kubernetes Fit

Each Kubernetes cluster, namespace, node, or workload can be represented as an island node depending on the boundary required.

```text
Cluster Island
Namespace Island
Workload Island
Tenant Island
Agent Runtime Island
```

## Product Rule

```text
Feature = Island Node + Boundary + Bridge + Contract + Policy + Evidence + Reconciliation + UI
```

## Final Cut

```text
Unboxd Panel composes island nodes into governed fabric without bleeding edges.
```

Stable state is achieved locally first, then composed globally through contract-bound bridges.
