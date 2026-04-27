# Architecture Systems

Each file in this folder documents a specific system, component, or Architecture Decision Record (ADR).

## System file structure

```
## Purpose

What this system does and why it exists.

## Boundaries

What is in scope and out of scope for this system.

## Key components

- Component A — role
- Component B — role

## Interfaces

How other systems interact with this one (APIs, events, files).

## Decisions

Links to relevant ADRs: [ADR-001](adr-001-<slug>.md)

## Diagram

See: [diagram](../04-diagrams/<slug>.md)
```

## ADR file structure

```
## Status

Proposed | Accepted | Deprecated | Superseded by [ADR-NNN](adr-NNN-<slug>.md)

## Context

What situation forced this decision.

## Decision

What we decided.

## Consequences

What becomes easier, what becomes harder.
```

## Naming

- Systems: `<system-slug>.md`
- ADRs: `adr-<NNN>-<slug>.md` — keep NNN zero-padded to three digits
