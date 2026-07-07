# Project DNA
```yaml
Project DNA

Type:
Engineering Platform

Methodology:
Specification-Driven Development

Architecture:
Hexagonal + Domain-Driven Design

Core Principle:
Engineering Context as a Service

Primary Artifact:
Specifications

Primary Consumer:
Humans and AI Agents

Implementation Priority:
Correctness > Extensibility > Performance

Current Phase:
Architecture Design
```

# Developer Coordination Platform

> The authoritative entry point for the project.

---

# Project Status

**Phase**
Design

**Current Milestone**
Milestone 0 — Specification-Driven Design

**Implementation Status**
No production code.

The project is currently focused on designing a complete and stable specification before implementation begins.

---

# Mission

Developer Coordination Platform is an AI-native Engineering Context Platform.

Its purpose is to continuously collect engineering information from multiple systems (GitHub, Jira, CI/CD, Teams, Confluence, and others), normalize that information into a unified domain model, detect coordination risks, and expose actionable engineering context through multiple interfaces.

The platform is **not** a dashboard.

The dashboard is only one possible client.

The product is the **Engineering Context Engine**.

---

# Vision

Engineering organizations increasingly rely on AI-assisted development.

Current AI tools understand repositories.

They do not understand organizations.

Developer Coordination Platform bridges that gap by becoming the shared source of engineering context for both humans and AI agents.

---

# Guiding Principles

## Domain First

The domain model defines the platform.

External systems never define the domain.

---

## Documentation First

Specifications are the primary source of truth.

Implementation follows specifications.

Documentation is never generated from code.

---

## AI Native

Every specification should be understandable by both humans and AI agents.

The project should be navigable without prior knowledge.

---

## Adapter Architecture

GitHub, Jira, GitLab, Azure DevOps, CI/CD systems, and future integrations are adapters.

They provide data.

They never define business rules.

---

## Stable Core

The Engineering Context Engine should remain independent from:

- UI
- MCP
- REST
- CLI
- Storage implementation
- Third-party services

---

## Evolution Over Perfection

Prefer incremental improvements over premature complexity.

Start simple.

Generalize only when experience justifies it.

---

# Source of Truth

This repository is the canonical specification for the project.

If implementation and documentation disagree:

**The documentation wins until intentionally updated.**

---

# Documentation Map

```
SPEC.md
│
├── Vision
│
├── Domain
│
├── Architecture
│
├── Integrations
│
├── Rules Engine
│
├── APIs
│
├── Security
│
├── Roadmap
│
├── ADRs
│
└── Playbooks
```

Each document has a single responsibility.

Avoid duplicating information across documents.

Cross-reference instead.

---

# Reading Guide

## New Contributor

Read in this order:

1. Vision
2. Goals
3. Glossary
4. Domain
5. Architecture
6. Roadmap

---

## AI Coding Agent

Read in this order:

1. SPEC.md
2. AGENTS.md
3. Domain
4. Architecture
5. Relevant feature specification

Never infer architecture.

Never bypass documented decisions.

---

## Implementer

Before writing code:

1. Understand the domain.
2. Read the relevant specification.
3. Verify existing ADRs.
4. Confirm implementation aligns with the architecture.

---

# Repository Philosophy

This repository is organized around knowledge rather than implementation.

The primary artifact is the specification.

Code is an implementation of the specification.

Documentation should remain valuable even if the implementation is rewritten.

---

# Core Architecture

```
Engineering Systems

GitHub
Jira
CI/CD
Teams
Confluence
...

        │

        ▼

Normalization Layer

        │

        ▼

Engineering Knowledge Graph

        │

        ▼

Coordination Engine

        │

        ▼

Interfaces

REST API
CLI
MCP
Dashboard
Future Integrations
```

The Engineering Knowledge Graph is the core product.

Everything else is an adapter.

---

# Current Milestone

Milestone 0

Goal:

Design the complete specification system before implementation.

Deliverables include:

- Vision
- Goals
- Non-Goals
- Glossary
- Domain Model
- Architecture
- Knowledge Graph
- Integration Contracts
- Rules Engine
- API Contracts
- Security Model
- Roadmap
- ADR Structure
- Playbooks
- AGENTS.md

No production code should be written until these specifications provide a stable architectural foundation.

---

# Decision Log

Important architectural decisions are documented as ADRs.

Specifications should reference ADRs rather than duplicating architectural rationale.

---

# Design Rules

When adding new functionality:

- Extend the domain before extending integrations.
- Prefer composition over special cases.
- Keep adapters isolated.
- Keep business rules inside the Coordination Engine.
- Avoid leaking implementation details into specifications.
- Favor clarity over cleverness.

---

# Long-Term Goal

Create a platform that becomes the shared engineering context layer for both developers and AI agents.

Success is measured by reducing coordination overhead, improving engineering visibility, and enabling AI systems to reason about software development at the organizational level rather than only at the repository level.

---

# Current Next Step

Design the project's ubiquitous language and domain model.

Everything else will be built upon that foundation.
