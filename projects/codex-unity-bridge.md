# Codex Unity Bridge

[Back to project index](index.md)

## Summary

Codex Unity Bridge is a private local tooling project for connecting Codex-style automation to a live Unity editor through a guarded bridge. The public portfolio version is a sanitized case study: it describes the architecture, safety model, validation surfaces, and engineering decisions without publishing private source.

Current private evidence reviewed for this case study describes bridge version `0.5.0`, validated through the Phase 6 slice.

## Problem

Unity editor automation is powerful but easy to make unsafe. A useful local bridge has to distinguish between:

- read-only inspection;
- scratch-only validation;
- project writes that require preview and confirmation;
- potentially dangerous operations that should remain gated or deferred.

The goal was to make Unity automation more useful while refusing to treat the editor as an unguarded mutation surface.

## Architecture Shape

The private workspace is organized around:

- a Unity package that owns editor-side inspection, command handling, and loopback HTTP endpoints;
- a Python bridge that can expose CLI and MCP-style access;
- versioned request/response protocol contracts;
- a sandbox Unity project for validation;
- Codex-facing skill/config examples;
- documentation for installation, validation, troubleshooting, threat modeling, and rollout readiness.

## Engineering Highlights

- Capability discovery through a machine-readable command manifest.
- Policy profiles such as `read-only`, `scratch-write`, and `project-write`.
- Dry-run preview and confirmation-token flows for selected mutations.
- Read-only inspection APIs for asset identity, prefab state, reference scans, and project inventory.
- EditMode and PlayMode test execution surfaces with result-file constraints.
- Player build preview/apply flow restricted to scratch output paths.
- Job status reporting for long-running validation/build work.
- Package identity and version alignment checks across Python and Unity package surfaces.

## What This Demonstrates

- Unity editor tooling
- Python and C# bridge design
- Protocol modeling
- Safety-first local automation
- Test/build orchestration
- Developer workflow documentation
- Practical threat modeling

## Validation Status

Private docs record validation from read-only live editor inspection through safe mutation previews, play-mode transitions, EditMode tests, read-only inspection APIs, PlayMode/build surfaces, capability/policy checks, packaging validation, and health diagnostics.

The current public claim is intentionally scoped: this case study shows a validated sandbox/local bridge architecture. It does not claim the bridge is a production-ready public Unity asset, a general-purpose cloud service, or fully installed across every Unity project.

## Public Boundary

The source repo is private. This page does not expose local machine paths, private project data, unpublished config, credentials, or raw validation artifacts.
