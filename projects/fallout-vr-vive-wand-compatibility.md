# Fallout 4 VR Vive Wand Compatibility Patch

## Summary

Public-safe case study for a Fallout 4 VR compatibility project focused on restoring practical HTC Vive Wand behavior in a heavily modded VR setup.

## Problem

Controller behavior in modded Fallout 4 VR can break across input maps, VR controller state, UI layers, profile configuration, and mod-specific compatibility patches. The goal was to turn confusing player-facing symptoms into a specific, documented, testable fix path.

## Technical Highlights

- Investigated behavior across Mod Organizer 2 profile configuration, Fallout 4 VR control maps, OpenVR loader behavior, FO4VRTools/F4SEVR concepts, Virtual Holsters settings, and Scaleform/GFx menu behavior.
- Focused on player-facing control quality and regression avoidance rather than broad remapping.
- Produced release notes, troubleshooting guidance, package checks, and validation notes.
- Preserved public/private boundaries around community QA and accessibility-sensitive context.

## Current Public-Safe Package Shape

The current local package evidence reviewed for this portfolio is `Vive Wand Compatibility Patch 2.1.4`. Its README describes a focused MO2-friendly patch that:

- restores Fallout 4 VR's vanilla OpenVR loader through a manual local file copy by the user;
- makes Virtual Holsters use dominant-hand Grip for holster and unholster;
- ships Virtual Holsters defaults with display spheres and holster-zone haptics off;
- restores right-trackpad touch-drag scrolling in scripted vertical dialogue menus;
- documents recommended Workshop item rotation and distance speed profile values.

The package intentionally does not ship Valve's `openvr_api.dll`; it documents where the user must copy that file from their own Fallout 4 VR installation.

## Credit Boundary

The current 2.1.4 README gives major credit to Mr. Dave for the vanilla `openvr_api.dll` restore discovery. This portfolio page frames the project as compatibility debugging, release/support packaging, QA, and documentation work while preserving that collaborator credit.

## What This Demonstrates

- Compatibility debugging
- Runtime and configuration-layer reasoning
- Release packaging
- Support-facing documentation
- QA and validation discipline
- User-centered troubleshooting

## Validation Status

Current evidence includes the local 2.1.4 package README, metadata, included file shape, and validation instructions. Public wording should stay scoped to verified behavior and should avoid broad compatibility claims.

## Current Public Boundary

Do not disclose private accessibility details, raw support context, private tester information, or unsupported install claims.

## Evidence To Add

- Add a public-safe architecture/diagnostic diagram.
- Add a concise before/after behavior table.
- Link public release materials only after reviewing the exact public page and files.
