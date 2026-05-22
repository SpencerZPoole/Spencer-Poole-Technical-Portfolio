# Foundry Codex Bridge

[Back to project index](index.md)

Public repo: [SpencerZPoole/codex-foundry-bridge](https://github.com/SpencerZPoole/codex-foundry-bridge)

## Summary

Foundry Codex Bridge is a local-first MCP bridge for safely operating a trusted Foundry VTT GM session from Codex. It is not a toy demo. The public release is built around guarded live-world capability: inspect state, preview changes, apply confirmed plans, restart local Foundry when needed, and keep private campaign data behind a trusted GM session gate.

The project direction is "Guarded Power": useful local automation with explicit authentication, authorization, preview, confirmation, backup, and redaction boundaries.

## Problem

AI-assisted GM tooling becomes risky when it can mutate live campaign data without enough context or guardrails. A useful bridge needs to answer practical questions:

- Is the live Foundry session connected and trusted?
- What world, system, module version, and tool registry are actually running?
- Can the assistant inspect enough state to plan safely?
- Can mutating changes be previewed before they touch the world?
- Can high-risk operations require explicit confirmation?
- Can local lifecycle recovery be handled without pretending it is a normal document edit?

## Engineering Highlights

- Shared MCP/daemon tool registry with deterministic capability metadata.
- Localhost-only daemon with token authentication.
- Foundry module connection limited to GM clients and trusted-world authorization.
- Runtime self-checks for bridge readiness, version, registry, and tool metadata.
- Read-only world intelligence for actors, scenes, compendiums, world search, readiness audits, logs, and runtime events.
- Preview/apply transactions for journals, scene prep, top-level document changes, and chat messages.
- Backup-first destructive document operations.
- Guarded local lifecycle restart for relaunching Foundry, joining an explicit world, and restoring bridge readiness.

## Public Release Shape

The public README reports:

- Version: `0.2.13`
- Foundry compatibility target: `14`
- Live validation baseline: Foundry `14.361` with D35E `3.0.2`
- Registered bridge tools: `47`

The repo also includes install guidance, development checks, lifecycle credential setup, a capability manifest, a release audit/roadmap, market-positioning notes, and a safety model.

## What This Demonstrates

- JavaScript/Node tooling
- MCP-style tool design
- Localhost service architecture
- Security-minded workflow design
- Runtime diagnostics and observability
- Preview/confirmation transaction design
- Public release documentation
- Supportability for power-user tooling

## Validation And Boundaries

The public release was prepared with validation and security sweeps before publication. The bridge is intentionally local-first. It should be tested in a disposable Foundry world before being pointed at important data.

Public documentation avoids private campaign details, private world defaults, credentials, raw Foundry data exports, and private GM notes.
