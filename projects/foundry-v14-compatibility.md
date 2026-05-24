# Foundry V14 Compatibility Contributions

[Back to project index](index.md)

## Summary

This project group covers public compatibility and install-flow work for existing Foundry VTT modules during the move to Foundry V14. The work is useful portfolio evidence because it combines small code changes, live validation, release-shape checks, maintainer-friendly PR writing, and careful attribution to upstream maintainers and prior contributors.

These are maintenance contributions, not claims of ownership over the upstream modules.

## Accepted Upstream Contributions

| Module | Public PR | Status | Work summary |
| --- | --- | --- |
| AFK Ready Check | [PR #2](https://github.com/jeremiahverba/afk-ready-check/pull/2) | Merged | Updated the module for Foundry V14, including ApplicationV2 UI work, chat-command registration, socket/user-id handling, player-list badges, package script, README updates, and validation notes. |
| AFK Ready Check | [PR #3](https://github.com/jeremiahverba/afk-ready-check/pull/3) | Merged | Fixed an official Foundry install failure by correcting a manifest download URL that pointed at a missing GitHub release asset, then documented package validation and release-asset alternatives. |
| Quick Status Select | [PR #27](https://github.com/jeremiahverba/qss/pull/27) | Merged | Verified Foundry `14.362`, updated compatibility metadata, replaced regex search filtering with plain-text matching, restored compact visible search behavior, and documented validation. |
| Popout Resizer | [PR #23](https://github.com/Cardagon/popout-resizer/pull/23) | Merged | Verified Foundry `14.362`, removed stale max-version cap, added ApplicationV2/sidebar popout handling, guarded repeated renders, and modernized release packaging. |

## Public Validation Forks

| Module | Fork release or repo | Work summary |
| --- | --- | --- |
| AFK Ready Check | [fork repo](https://github.com/SpencerZPoole/afk-ready-check) | Public V14-compatible fork release and validation surface used before and alongside upstream review. |
| Quick Status Select | [validation release](https://github.com/SpencerZPoole/qss/releases/tag/v2.0.3) | Public validation release for the V14 search-filtering and compatibility work. |
| Popout Resizer | [validation release](https://github.com/SpencerZPoole/popout-resizer/releases/tag/v1.6.1) | Public validation release for the V14 popout compatibility work. |
| PopOut! | [PR #164](https://github.com/League-of-Foundry-Developers/fvtt-module-popout/pull/164) / [validation release](https://github.com/SpencerZPoole/fvtt-module-popout/releases/tag/v2.24.0) | Public pending PR and fork release for V14 validation and popped-out input focus handling. |

## What This Demonstrates

- Maintaining compatibility in someone else's codebase.
- Reading existing project style before changing behavior.
- Writing small, reviewable upstream PRs.
- Diagnosing public install failures and release URL problems.
- Preserving module IDs, public APIs, and user-facing behavior.
- Crediting existing maintainers and prior contributor work.
- Packaging public fork releases for install testing.
- Running syntax checks, manifest/reference checks, package-shape checks, live Foundry smoke tests, and local security scans.

## Validation Notes

The PR descriptions record local validation against Foundry `14.361` or `14.362`, with D35E `3.0.2` where relevant. They also document command-level checks such as JavaScript syntax validation, manifest/reference validation, package-shape checks, fork release checks, release URL checks, and local changed-file security scans.

The work is compatibility and contribution work. It does not imply ownership of the upstream modules.
