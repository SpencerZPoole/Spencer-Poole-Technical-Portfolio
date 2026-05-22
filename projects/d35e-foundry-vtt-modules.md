# D35E Foundry VTT Modules

[Back to project index](index.md)

## Summary

This project family contains public Foundry VTT module work for the D35E system. The strongest current examples are two release-ready modules:

- [D35E Piecemeal Armor And Called Shots](https://github.com/SpencerZPoole/d35e-piecemeal-armor-called-shots)
- [D35E Scent Sense](https://github.com/SpencerZPoole/d35e-scent-sense)

Both projects show practical JavaScript module development, Foundry V14 compatibility work, D35E integration, user-facing documentation, validation tooling, and careful legal/content boundaries.

## Featured Modules

| Module | Current status | What it does |
| --- | --- | --- |
| [D35E Piecemeal Armor And Called Shots](https://github.com/SpencerZPoole/d35e-piecemeal-armor-called-shots) | Public `v1.0.0` release | Adds optional piecemeal armor workflows, called-shot selection in D35E attack dialogs, configurable profiles, GM-confirmed outcomes, and release packaging. |
| [D35E Scent Sense](https://github.com/SpencerZPoole/d35e-scent-sense) | Public `v1.0.0` release | Adds conservative SRD Scent support: range detection, owner/GM range rings, detection state, odor context, scent trails, diagnostics, and stable public API docs. |

## Screenshots

The Piecemeal Armor / Called Shots module includes screenshots from the release repository:

![Native D35E attack dialog with Called Shot dropdown](https://raw.githubusercontent.com/SpencerZPoole/d35e-piecemeal-armor-called-shots/main/docs/assets/native-called-shot-dropdown.png)

![Piecemeal armor sync dialog](https://raw.githubusercontent.com/SpencerZPoole/d35e-piecemeal-armor-called-shots/main/docs/assets/piecemeal-armor-sync.png)

![Called-shot profile editor](https://raw.githubusercontent.com/SpencerZPoole/d35e-piecemeal-armor-called-shots/main/docs/assets/profile-editor.png)

## Engineering Highlights

- Foundry VTT module manifests, scripts, styles, templates, localization, and release workflows.
- D35E system integration without editing upstream system files.
- Public APIs exposed under `game.d35ePiecemealCalledShots` and `game.d35eScentSense`.
- Runtime behavior split into focused modules for future maintenance.
- User guides, release process docs, architecture notes, legal notes, and public-surface checks.
- Validation tooling for manifests, script syntax, localization coverage, package shape, and public repository hygiene.

## Release And Compatibility Evidence

Piecemeal Armor / Called Shots:

- Public release: [v1.0.0](https://github.com/SpencerZPoole/d35e-piecemeal-armor-called-shots/releases/tag/v1.0.0)
- Verified compatibility noted in the public README: Foundry VTT `14.362`, D35E `3.0.2`
- Includes screenshots, user guide, release workflow, module manifest, package build script, and validation tools.

D35E Scent Sense:

- Public release: [v1.0.0](https://github.com/SpencerZPoole/d35e-scent-sense/releases/tag/v1.0.0)
- Verified compatibility noted in the public README: Foundry VTT `14.361`, D35E `3.0.2`
- Includes API reference, architecture docs, RAW coverage matrix, release audit, release process, and validation tooling.

## What This Demonstrates

- JavaScript application development in an existing platform
- API and data-contract design
- UI integration inside a complex host application
- Compatibility testing against current platform versions
- Release packaging and GitHub release workflows
- Public documentation for users and maintainers
- License-aware documentation for tabletop-related tooling
