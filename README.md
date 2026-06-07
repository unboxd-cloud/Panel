# Unboxd Panel

**Unboxd Panel** is the web control surface for operating the Unboxd Cloud fabric.

It is not the core runtime. It is the operator-facing panel that lets a human see, govern, and operate boxes, services, tenants, deployments, events, policies, and drift.

## Ground

- **Box**: the bounded unit that emits, receives, stores, and reconciles events.
- **Fabric**: the operating layer where boxes communicate through explicit protocols.
- **Panel**: the human control surface for observing and governing the fabric.
- **Agent**: an operator of tools, never the unstable core.
- **Drift**: the difference between declared state and observed state.

## Purpose

Panel gives the orchestrator a single place to:

1. See every box and service.
2. Inspect health, drift, events, and deployments.
3. Approve or deny agent actions.
4. Trigger reconciliation.
5. Preserve audit trails.
6. Keep the core stable while the edge expands.

## Non-goals

Panel does not replace Kubernetes, SurrealDB, Git, CI/CD, observability, or identity systems. It composes them behind a clean operator surface.

## Current shape

This repository starts as a minimal, production-oriented shell:

```text
apps/panel        Operator web UI
packages/schema   Shared typed contracts
packages/core     Panel domain model and rules
infra/k8s         Kubernetes deployment manifests
docs              Architecture and operating model
```

## Canonical loop

```text
Declare -> Observe -> Compare -> Approve -> Reconcile -> Audit
```

Panel exists to make that loop visible, safe, and repeatable.
