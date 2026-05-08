# TreenAH - World of Warcraft Auction House Add-on

## Summary

TreenAH is a Lua 5.1 World of Warcraft Classic Anniversary addon for auction-house price tracking, scan workflows, local market history, tooltip pricing, tracked lists, slash commands, and SavedVariables-backed data.

## Problem

Auction House decisions are easier when price history is visible in the game client instead of scattered across memory, chat, or external notes. TreenAH keeps local market information close to the normal Auction House workflow.

## Technical Highlights

- Built around WoW Auction House, UI, tooltip, chat, and SavedVariables APIs.
- Separates market data by realm/faction from character-specific tracked-list data.
- Supports scan workflows, recent averages, outlier filtering, tooltip pricing, browse-row pricing, and slash-command price checks.
- Includes user-facing help, options, guardrails, and destructive-action confirmations.

## Architecture Snapshot

The installed addon is organized into focused modules:

- `Core`: lifecycle events, slash commands, chat events, and shared utility helpers.
- `Data`: SavedVariables schema, migrations, price records, name indexing, and tracked-item lists.
- `Systems`: auction scanning, price checks, version checks, cooldowns, and reply behavior.
- `UI`: main Auction House panel, data browser, browse-column display, tooltip injection, options, and help surfaces.

Local evidence shows a meaningful codebase rather than a toy example: 13 source/config files, a multi-module Lua structure, and a large SavedVariables file with real accumulated market data. Raw account data is intentionally not published here.

## What This Demonstrates

- Lua addon development
- Event-driven UI work
- Persistent data modeling
- Platform API integration
- User-facing tool design
- Documentation and QA judgment

## Validation Status

Current evidence includes source inspection and substantial local SavedVariables-based use evidence. A fresh live in-game smoke test should be recorded before making current-client compatibility claims.

## Current Public Boundary

Do not publish raw SavedVariables data, personal account data, or compatibility claims that have not been freshly validated.

## Evidence To Add

- Add screenshots of tooltip pricing, browse-row pricing, scan output, and slash-command output.
- Add setup and usage instructions.
- Record a fresh live smoke test.
