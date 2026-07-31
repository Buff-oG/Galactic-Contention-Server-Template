<div align="center">

<img src="Logo/GC_Logo.png" alt="Galactic Contention Logo" width="500"/>

# Galactic Contention Server Template

*Dedicated server configuration template for the mod Galactic Contention, running on Squad.*

[![GitHub release](https://img.shields.io/github/release/Buff-oG/Galactic-Contention-Server-Template.svg?style=flat-square)](https://github.com/Buff-oG/Galactic-Contention-Server-Template/releases)
[![GitHub issues](https://img.shields.io/github/issues/Buff-oG/Galactic-Contention-Server-Template.svg?style=flat-square)](https://github.com/Buff-oG/Galactic-Contention-Server-Template/issues)
[![Last commit](https://img.shields.io/github/last-commit/Buff-oG/Galactic-Contention-Server-Template.svg?style=flat-square)](https://github.com/Buff-oG/Galactic-Contention-Server-Template/commits/main)

</div>

---

## Table of Contents

- [Overview](#overview)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Configuration Reference](#configuration-reference)
  - [Administration](#administration)
  - [Levels & Layers — Reference Lists](#levels--layers--reference-lists)
  - [Standard Rotation](#standard-rotation)
  - [Vote Rotation](#vote-rotation)
  - [Mod-Specific Options](#mod-specific-options)
- [Notable Settings](#notable-settings)
- [Misc](#misc)
- [Support](#support)

---

## Overview

This repository provides a ready-to-deploy `ServerConfig` template for hosting a **Galactic Contention** server on Squad. Every file has been pre-filled with sensible defaults and annotated with inline comments so it can be dropped in and adjusted with minimal guesswork.

Any value written as **`$word`** is a placeholder — replace it with your own value before starting the server.

---

## Prerequisites

- A dedicated Squad server install.
- A valid **OWI hosting license**, obtainable via the [OWI Hosting Discord](https://discord.gg/joinsquad) or [joinsquad.com](https://joinsquad.com).
- The Galactic Contention mod subscribed on Steam Workshop:
  - **Steam Mod ID:** `2428425228`
  - **Workshop URL:** https://steamcommunity.com/sharedfiles/filedetails/?id=2428425228

---

## Installation

1. Download or clone this repository.
2. Copy the entire contents of [ServerConfig/](ServerConfig/) into your server's `ServerConfig` directory:

   ```
   C:\$InstallationFolder\SquadGame\ServerConfig\
   ```

3. Replace every `$word` placeholder with your own values (Steam IDs, server name, etc.).
4. Review the [Configuration Reference](#configuration-reference) below and adjust each file to your needs.
5. Start (or restart) your server.

---

## Configuration Reference

### Administration

| File | Purpose |
|---|---|
| [Server.cfg](ServerConfig/Server.cfg) | Core server identity, rotation mode, queueing, and gameplay flags. |
| [MOTD.cfg](ServerConfig/MOTD.cfg) | Message of the Day shown to connecting players. |
| [ServerMessages.cfg](ServerConfig/ServerMessages.cfg) | Recurring heads-up broadcast messages. |
| [Admins.cfg](ServerConfig/Admins.cfg) | Admin groups, permission levels, and Steam ID assignments. |
| [Rcon.cfg](ServerConfig/Rcon.cfg) | RCON access configuration. |
| [Bans.cfg](ServerConfig/Bans.cfg) | Local ban list. |
| [RemoteAdminListHosts.cfg](ServerConfig/RemoteAdminListHosts.cfg) | Remote admin list source(s). |
| [RemoteBanListHosts.cfg](ServerConfig/RemoteBanListHosts.cfg) | Remote ban list source(s). |

### Levels & Layers — Reference Lists

| File | Purpose |
|---|---|
| [_CompleteLayerList.cfg](ServerConfig/_CompleteLayerList.cfg) | The full list of Galactic Contention layers. Use this as your picking source. |
| [_CompleteLevelIds.cfg](ServerConfig/_CompleteLevelIds.cfg) | The full list of Galactic Contention level IDs. Defaults are recommended. |

### Standard Rotation

Use this set if you want a fixed rotation with **no map voting**.

| File | Purpose |
|---|---|
| [LayerRotation.cfg](ServerConfig/LayerRotation.cfg) | Layers included in the standard rotation. |
| [LevelRotation.cfg](ServerConfig/LevelRotation.cfg) | Levels included in the standard rotation. |
| [_ServerWithStandardRotation.cfg](ServerConfig/_ServerWithStandardRotation.cfg) | Reference `Server.cfg` pre-configured for standard rotation (voting disabled). |

### Vote Rotation

Use this set if you want players to **vote** on the next map/layer.

| File | Purpose |
|---|---|
| [LayerVoting.cfg](ServerConfig/LayerVoting.cfg) | Layer pool offered during map vote. Recommended: large layers (AAS, RAAS, INV, RINV, Insurgency). |
| [LayerVotingLowPlayers.cfg](ServerConfig/LayerVotingLowPlayers.cfg) | Low-population layer pool (Skirmish/Seed-friendly layers). |
| [VoteConfig.cfg](ServerConfig/VoteConfig.cfg) | Vote behavior: options count, durations, skip rules, game-mode weighting, etc. |
| [ExcludedLayers.cfg](ServerConfig/ExcludedLayers.cfg) | Layers hidden from admin layer-change tools. Use to exclude known-broken layers. |
| [ExcludedLevels.cfg](ServerConfig/ExcludedLevels.cfg) | Level IDs excluded from the vote pool. Dev/WIP levels are pre-excluded. |
| [ExcludedFactions.cfg](ServerConfig/ExcludedFactions.cfg) | Factions and battlegroup types excluded from selection. |
| [ExcludedFactionSetups.cfg](ServerConfig/ExcludedFactionSetups.cfg) | Specific FactionSetup IDs excluded from selection. |

### Mod-Specific Options

| File | Purpose |
|---|---|
| [CustomOptions.cfg](ServerConfig/CustomOptions.cfg) | Galactic Contention–specific server settings (seeding behavior, cross-team VOIP, etc.). |
| [License.cfg](ServerConfig/License.cfg) | Hosting license placeholder — see [Prerequisites](#prerequisites). |

---

## Notable Settings

A quick reference for options that materially change gameplay behavior — worth reviewing before going live.

**`Server.cfg`**

| Setting | Description |
|---|---|
| `JoiningPlayerTimeout` | Seconds a queued player has to fully connect before their slot is released back to the queue. |
| `AllowFireteamLayersInRotation` | Includes or excludes Fireteam mission layers from rotation. |
| `AllianceEnabled` | Enables alliance restrictions between factions. |
| `RotationMode=LayerList_Vote` | Rotation mode that presents a vote screen at the end of each match. |

**`CustomOptions.cfg`**

| Setting | Description | Default |
|---|---|---|
| `SeedPlayersThreshold` | Player count required to begin the Pre-Live countdown. | `40` |
| `SeedMinimumPlayersToLive` | Minimum player count to keep the Pre-Live countdown running once triggered. | `42` |
| `SeedMatchLengthSeconds` | Length of the seed match, in seconds. | `21600` |
| `SeedAllKitsAvailable` | Whether all kits are available during seeding. | `1` |
| `SeedInitialTickets` | Starting ticket count for both teams during seeding. | `100` |
| `SeedSecondsBeforeLive` | Countdown length (seconds) before the match goes live. | `60.0` |
| `SeedTargetPlayerCount` | Target player count used for bot-filled seeding. | `40` |
| `CrossVoipGC` | Enables cross-team VOIP. Enemy speaker names are shown for moderation purposes; disabled while dead/knocked, during voting, and on the end screen. | `False` |

**`VoteConfig.cfg`**

| Setting | Description |
|---|---|
| `GameModeSkipRounds` | Per-game-mode cooldown before it can be offered again (e.g. `AAS 0, RAAS 0, Invasion 0, ...`). |
| `GameModeChoices` | Caps how many options of each game mode appear on the vote screen. |
| `SymmetricalMatchUp` | Mirrors team 2's unit choices to match team 1's. |
| `UniqueMap` | Restricts the map vote pool to unique maps with a randomized game mode. |
| `AutoSelectFactions` | Automatically selects factions after the layer vote, per configured rules. |
| `NightTime` | Time window that switches voting to `LayerVotingNight.cfg`, if defined. |

**`Admins.cfg`**

- Admin groups are now `Admin`, `Moderator`, `PTQA`, `Supporters`, and `Famous`.
- The `demo` permission has been split into `demos` (server-side replay recording) and `clientdemos` (client-side replay recording).

---

## Misc

- Any error on maps with a `_DEV` or `_WIP` extension is **not supported** via Discord `#bug-report` or GitHub Issues — these levels/layers exist for test purposes only.
- Make sure files are copied into the correct directory before starting the server.

---

## Support

Questions or issues? [Open an issue](https://github.com/Buff-oG/Galactic-Contention-Server-Template/issues) on this repository.
