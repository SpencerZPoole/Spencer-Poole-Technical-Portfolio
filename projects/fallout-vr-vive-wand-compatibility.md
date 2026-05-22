# Fallout 4 VR Vive Wand Compatibility Patch

[Back to project index](index.md)

Public repo: [SpencerZPoole/Vive-Wand-Compatibility-Patch](https://github.com/SpencerZPoole/Vive-Wand-Compatibility-Patch)

## Summary

Case study for a Fallout 4 VR compatibility project focused on restoring practical HTC Vive Wand behavior in a heavily modded VR setup.

Current public package baseline: `Vive Wand Compatibility Patch 2.1.4`

## Problem

Controller behavior in modded Fallout 4 VR can break across input maps, VR controller state, UI layers, profile configuration, script extender plugins, and mod-specific compatibility patches. The goal was to turn confusing player-facing symptoms into a specific, documented, testable fix path.

## What The Patch Does

The public README describes a focused MO2-friendly patch that:

- restores Fallout 4 VR's vanilla OpenVR loader through a manual local file copy by the user;
- keeps controller auto-detection on the normal baseline unless a specific controller-identity regression is being diagnosed;
- makes Virtual Holsters use dominant-hand Grip for holster and unholster;
- ships Virtual Holsters defaults with display spheres and holster-zone haptics off;
- restores right-trackpad touch-drag scrolling in scripted vertical dialogue menus;
- documents recommended Workshop item rotation and distance-speed profile values.

The package does not ship Valve's `openvr_api.dll`. Users copy that file from their own Fallout 4 VR installation.

## Before And After

| Area | Before | After |
| --- | --- | --- |
| OpenVR loader baseline | Modded setup could lose the vanilla OpenVR behavior needed for the target controller path. | User restores the vanilla loader locally from their own Fallout 4 VR install. |
| Virtual Holsters | Vive Wand holster interaction could be awkward or mismatched. | Grip is used for holster/unholster, with display spheres and holster-zone haptics disabled by default. |
| Scripted dialogue menus | Vertical dialogue menu selection could be difficult with Vive Wand trackpad behavior. | Right-trackpad touch-drag moves the highlighted dialogue option; right trigger confirm is left alone. |
| Workshop item handling | Workshop object control needed profile-specific tuning. | README documents recommended rotation and distance-speed values. |

## Package Shape

The public repo includes:

- `README.md`
- `BUILDING.md`
- `RELEASE_MANIFEST_2.1.4.md`
- `SECURITY_REVIEW_NOTES.md`
- `Nexus_FULLDESCRIPTION.txt`
- `Source/`
- `F4SE/`
- `Root/`
- `meta.ini`

The public README lists the release payload, installation flow, expected log strings, and behavior checks.

## Credits

The current README gives major credit to Mr. Dave for the vanilla `openvr_api.dll` restore discovery. This portfolio page frames Spencer's work as compatibility debugging, release/support packaging, validation, documentation, and user-facing integration while preserving that collaborator credit.

## What This Demonstrates

- VR input and controller-behavior troubleshooting
- Runtime/configuration-layer reasoning
- F4SEVR and FO4VRTools-adjacent compatibility work
- Release packaging
- Support-facing documentation
- QA and validation discipline
- Compatibility-scope judgment

## Validation Status

The public README documents expected F4SE log strings for the plugin baseline and user-facing behavior checks for scripted dialogue menus. Claims are scoped to the documented target setup and package version.
