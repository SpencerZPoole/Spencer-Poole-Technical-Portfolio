# TreenAH - World of Warcraft Auction House Add-on

[Back to project index](index.md)

Public repo: [SpencerZPoole/TreenAH](https://github.com/SpencerZPoole/TreenAH)

## Summary

TreenAH is a Lua 5.1 World of Warcraft Classic Anniversary Auction House addon for local market-history tracking. It records auction prices from scanned or browsed results, then surfaces that data through tooltips, Auction House browse columns, tracked lists, and `/pc` price checks.

Current public repo version: `1.1.2`

## Problem

Auction House decisions are easier when recent price history is visible in the game client. TreenAH keeps market information close to the normal Auction House workflow instead of spreading it across memory, chat, screenshots, or external notes.

## Technical Highlights

- Built around WoW Auction House, UI, tooltip, chat, and SavedVariables APIs.
- Separates market data by realm/faction from character-specific tracked-list data.
- Supports passive browsing scans, single-item scans, tracked-list scans, fast full scans, and slower page-based full scans.
- Adds optional price data to item tooltips and Auction House browse rows.
- Provides slash-command price checks for local chat, whispers, Battle.net friends, party, raid, guild, and say chat.
- Includes auto-reply controls, channel toggles, cooldown behavior, help windows, options, guardrails, and destructive-action confirmations.

## Repository Shape

The public repo is organized by responsibility:

- `Core/`: startup, event registration, slash commands, chat events, and shared utilities.
- `Data/`: SavedVariables schema, migrations, price records, name indexing, and tracked-item lists.
- `Systems/`: Auction House scanning, price checks, version checks, cooldowns, and reply behavior.
- `UI/`: main panel, data browser, browse-column display, tooltip injection, options, and in-game help.
- `scripts/package-release.ps1`: release zip packaging for the addon folder.

## What This Demonstrates

- Lua addon development
- Event-driven UI work
- Persistent local data modeling
- Platform API integration
- User-facing tool design
- Packaging and installation documentation
- Support-minded troubleshooting notes

## Validation Status

Current public evidence includes source structure, versioned addon metadata, install instructions, slash-command documentation, troubleshooting notes, packaging script, and public repo hygiene.

Private local evidence has shown meaningful real-use data, but raw SavedVariables and account-specific data are intentionally not published. A fresh public screenshot or GIF pass is still needed before making stronger visual/demo claims.

## Public Boundary

Do not publish raw SavedVariables data, account names, character data, private game data, or current-client compatibility claims that have not been freshly validated.

## Next Evidence To Add

- Screenshots of tooltip pricing, browse-row pricing, scan output, and slash-command output.
- A short demo GIF of the normal Auction House workflow.
- A fresh in-game smoke-test note for the current WoW client build.
