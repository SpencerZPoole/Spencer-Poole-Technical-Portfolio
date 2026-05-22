# Mech Oregon Trail

[Back to project index](index.md)

## Summary

Mech Oregon Trail is a private Unity/C# game-systems project. The public portfolio version is a sanitized engineering case study focused on runtime architecture, systems design, validation discipline, and incremental refactoring rather than lore or unfinished design notes.

The strongest hiring signal is not "I had a game idea." It is the amount of real systems work behind the project: startup flow, save/runtime state, procedural map generation, travel, encounters, UI presentation, combat resources, and inventory architecture.

## Systems In Scope

- Runtime composition and startup bootstrapping.
- Save/load state sanitization and compatibility boundaries.
- Procedural world-map generation and route presentation.
- Travel runtime, resource drain, travel pauses, and arrival handling.
- Encounter flow, combat choices, receipts, fallback content, and presentation models.
- HUD/menu presentation and UI controller boundaries.
- Mech durability, ammo, resources, and inventory state.
- Body-part inventory grid foundation with data-driven layouts and runtime-drawn UI cells.

## Recent Engineering Direction

The current architecture direction separates scene-facing controllers from pure/runtime services. Important seams include:

- runtime services for inventory, travel, encounter, quest, content planning, and validation;
- scene-facing presentation controllers for map, HUD, encounter UI, and inventory UI;
- compatibility shims where legacy scene wiring still matters;
- explicit notes about which large systems should not be split further until tests or shared helpers justify it.

The inventory work is a good example of the project's engineering style. Instead of making one-off art for every possible grid shape, the system moves toward body-region layout data, runtime validation, reusable grid cells, and service-owned mutation rules.

## What This Demonstrates

- Unity/C# runtime architecture
- Incremental refactoring without breaking existing scene/save behavior
- Data-driven UI/system design
- Test extraction and compile validation
- Procedural generation and runtime validation thinking
- Honest separation of compile proof from Unity editor/runtime proof

## Validation Status

Validation varies by slice, and this portfolio keeps that distinction visible. Some Mech Oregon Trail work has real Unity EditMode execution proof; other slices currently have stronger compile/source validation than runtime execution proof. Later project notes specifically avoid treating shell-only `dotnet test` output as authoritative Unity execution evidence when the Unity runner did not produce real test results.

That distinction matters. It shows the project is being handled with engineering honesty instead of claiming every green-looking command proves runtime behavior.

## Public Boundary

The source project is private. This page does not expose local paths, private build folders, raw logs, unreleased assets, save data, or screenshots that have not been reviewed for public use.

## Next Evidence To Add

- Public-safe screenshots or a short video of the world map, travel flow, encounter UI, and inventory panel.
- A concise architecture diagram showing scene controllers versus runtime services.
- A sanitized build/demo note if a public demo is ever intentionally prepared.
