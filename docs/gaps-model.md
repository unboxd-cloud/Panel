# Gaps Model

The Gaps Model evaluates whether Island Bridge Architecture is complete enough to build, operate, and govern.

A gap is any missing explanation, model, contract, boundary, evidence path, or reconciliation loop that can cause drift, confusion, leakage, or unstable operation.

## Canonical Definition

```text
Gap = Missing Link Between Theory and Stable State
```

The Gaps Model exists to prevent weak architecture from becoming code.

## Core Rule

```text
Do not build across an unexplained gap.
Define the gap, model it, contract it, then reconcile it.
```

## Gap Stack

```text
Theory Gap
  -> Model Gap
  -> Identity Gap
  -> Contract Gap
  -> State Gap
  -> Event Gap
  -> Policy Gap
  -> Bridge Gap
  -> Reconciliation Gap
  -> Evidence Gap
  -> Maturity Gap
```

## 1. Theory Gap

A theory gap exists when we cannot clearly explain what something is, why it exists, where it belongs, or what makes it valid.

Check:

```text
Can we define it in one sentence?
Can we explain why it exists?
Can we say what it is not?
Can we place it in the architecture?
```

## 2. Model Gap

A model gap exists when the theory has no structured representation.

Check:

```text
Does it have fields?
Does it have relationships?
Does it have lifecycle states?
Does it have boundaries?
Can it become data?
```

## 3. Identity Gap

An identity gap exists when a controlled thing cannot be uniquely identified.

Check:

```text
Who or what is acting?
What is being controlled?
Which tenant owns it?
Which profile is active?
Which device/session is used?
Which island or bridge is involved?
```

## 4. Contract Gap

A contract gap exists when control is possible without a governed agreement.

Check:

```text
Who can request the action?
Who can approve it?
What protocol is allowed?
What tool may execute?
What state may change?
What evidence is required?
```

## 5. State Gap

A state gap exists when declared state and observed state are not both known.

Check:

```text
What should exist?
What actually exists?
How is drift detected?
Who accepts the reconciliation result?
```

## 6. Event Gap

An event gap exists when important transitions are not emitted as evidence.

Check:

```text
Did the transition emit an event?
Is it CloudEvents-compatible?
Can the event update a twin?
Can the event prove audit?
```

## 7. Policy Gap

A policy gap exists when the system can act without explicit decision rules.

Check:

```text
Should this be allowed, denied, approved, escalated, or blocked?
Which risk level applies?
What happens on uncertainty?
```

## 8. Bridge Gap

A bridge gap exists when an edge is crossed without a governed bridge.

Check:

```text
Which edge is being crossed?
Which protocol is used?
Which state is mapped?
Which contract permits it?
Which evidence proves it?
```

## 9. Reconciliation Gap

A reconciliation gap exists when execution happens but verification is missing.

Check:

```text
Did we observe after action?
Did reality match declared state?
Was drift closed?
Was failure handled?
Was stable state proven?
```

## 10. Evidence Gap

An evidence gap exists when an operation cannot be explained later.

Check:

```text
Who requested it?
Who approved it?
What policy evaluated it?
What tool executed it?
What changed?
What event proves it?
What state was reconciled?
```

## 11. Maturity Gap

A maturity gap exists when something works once but is not production-grade.

Check:

```text
Is it observable?
Is it secure?
Is it recoverable?
Is it auditable?
Is it tenant-safe?
Is it profile-safe?
Is it device-safe?
Is it upgradeable?
Is it retireable?
```

## Gap Closure Loop

```text
Find Gap
  -> Name Gap
  -> Define Theory
  -> Build Model
  -> Add Contract
  -> Add Policy
  -> Add Event Evidence
  -> Add Reconciliation
  -> Verify Stable State
  -> Record Maturity Evidence
```

## Product Rule

```text
Feature is not ready if any critical gap remains open.
```

## Final Cut

```text
The Gaps Model protects Island Bridge Architecture from becoming accidental complexity.
It forces every missing theory, boundary, contract, event, policy, and reconciliation loop to be made explicit before build.
```
