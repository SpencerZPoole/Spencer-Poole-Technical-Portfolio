# Foundry V14 Compatibility Contributions

[Back to project index](index.md)

## Summary

This project group covers public compatibility work for existing Foundry VTT modules during the move to Foundry V14. The work is useful portfolio evidence because it combines code changes, live validation, release-shape checks, maintainer-friendly PR writing, and careful attribution to upstream maintainers and prior contributors.

## Public Contributions

| Module | Public PR or release | Work summary |
| --- | --- | --- |
| Quick Status Select | [PR #27](https://github.com/jeremiahverba/qss/pull/27) / [validation release](https://github.com/SpencerZPoole/qss/releases/tag/v2.0.3) | Verified Foundry `14.362`, updated compatibility metadata, replaced regex search filtering with plain-text matching, restored compact visible search behavior, and documented validation. |
| PopOut! | [PR #164](https://github.com/League-of-Foundry-Developers/fvtt-module-popout/pull/164) / [validation release](https://github.com/SpencerZPoole/fvtt-module-popout/releases/tag/v2.24.0) | Verified Foundry `14.362`, updated metadata, included popped-out input focus fix with credit, avoided unsafe HTML assignment for mirrored tooltip/header content, and validated package shape. |
| Popout Resizer | [PR #23](https://github.com/Cardagon/popout-resizer/pull/23) / [validation release](https://github.com/SpencerZPoole/popout-resizer/releases/tag/v1.6.1) | Verified Foundry `14.362`, removed stale max-version cap, added ApplicationV2/sidebar popout handling, guarded repeated renders, and modernized release packaging. |

## What This Demonstrates

- Maintaining compatibility in someone else's codebase.
- Reading existing project style before changing behavior.
- Writing small, reviewable upstream PRs.
- Preserving module IDs, public APIs, and user-facing behavior.
- Crediting existing maintainers and prior contributor work.
- Packaging public fork releases for install testing.
- Running syntax checks, manifest/reference checks, package-shape checks, live Foundry smoke tests, and local security scans.

## Validation Notes

The PR descriptions record local validation against Foundry `14.362` with D35E `3.0.2`. They also document command-level checks such as JavaScript syntax validation, manifest/reference validation, package-shape checks, fork release checks, and local changed-file security scans.

The work is compatibility and contribution work. It does not imply ownership of the upstream modules.
