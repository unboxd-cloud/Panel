# Stable State Operations

Unboxd Panel is built for **stable state operations**.

The goal is not to trigger actions endlessly. The goal is to keep systems in a known, declared, observable, governed, and recoverable state.

## Canonical Definition

```text
Stable State = Declared Intent + Verified Observation + Accepted Reconciliation
```

Stable state is not a static snapshot.
Stable state is a governed operating condition.

## Product Position

```text
Unboxd Panel
= Composable Cloud-Native Hybrid Cloud Control Panel
= For Stable State Operations
= Delivered as Solution as a Service
```

## Control Loop

```text
Declare
  -> Observe
  -> Compare
  -> Detect Drift
  -> Decide
  -> Approve
  -> Execute
  -> Reconcile
  -> Audit
  -> Stable State
```

## Rule

Serverless actions, agents, scripts, jobs, and operators are never the source of truth.

They are bounded execution mechanisms used to restore, verify, or transition state.

## Stable State Layers

### 1. Declared State

What should exist.

Examples:

- Tenant exists
- Box is registered
- Cluster is connected
- Service is deployed
- Policy is active
- Identity is valid
- Backup is configured
- Certificate is current

### 2. Observed State

What actually exists now.

Examples:

- Node health
- Workload status
- DNS records
- Certificate expiry
- Deployment revision
- Secret age
- Agent status
- Policy decision result

### 3. Drift

The difference between declared state and observed state.

Examples:

- Service missing
- Replica count changed
- Certificate expiring
- Policy bypass attempted
- Deployment failed
- Node unreachable
- Identity still active after suspension

### 4. Policy

The rule that decides whether a correction is allowed.

Examples:

- Auto-reconcile low-risk drift
- Require approval for production change
- Block unmanaged secret access
- Deny unknown adapter mutation
- Require audit trail before execution

### 5. Execution

The bounded action used to move the system toward stable state.

Examples:

- Kubernetes apply
- Git commit
- Serverless function
- Job
- Webhook
- SSH command
- DNS update
- Secret rotation

### 6. Reconciliation

The verification that the system returned to an accepted state.

Reconciliation is not complete until observation confirms the result.

### 7. Audit

Every transition must be explainable.

Each action must record:

- Requested by
- Approved by
- Protocol used
- Contract used
- Adapter used
- Policy result
- Event emitted
- State before
- State after
- Reconciliation result

## Feature Rule

```text
Feature = Protocol + Contract + Declared State + Observed State + Drift Rule + Policy + Execution + Reconciliation + Audit + UI + Service Operation
```

## Non-Negotiable

Panel must never optimize for action volume.

Panel optimizes for stable state.
