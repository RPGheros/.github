[Deutsch](README.md) | English

```text
╔══════════════════════════════════════════════════════════════════════════════╗
║  |||||||                                                           |||||||  ║
║  |||||||      .-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-.    |||||||  ║
║  |||||||      |     _____ _          _ _ ____  ____   ____    |    |||||||  ║
║  |||||||      |    / ____| |        | | |  _ \|  _ \ / ___|   |    |||||||  ║
║  |||||||      |   | (___ | |__   ___| | | |_) | |_) | |  _    |    |||||||  ║
║  |||||||      |    \___ \| '_ \ / _ \ | |  _ <|  __/| |_| |   |    |||||||  ║
║  |||||||      |    ____) | | | |  __/ | | |_) | |    \____|   |    |||||||  ║
║  |||||||      |   |_____/|_| |_|\___|_|_|____/|_|               |    |||||||  ║
║  |||||||      '-----------------------------------------------'    |||||||  ║
║  |||||||            \    papyrus scroll // laurel // skulls  /     |||||||  ║
║  |||||||             \______________________________________/       |||||||  ║
║  |||||||                                                           |||||||  ║
║  |||||||      _.._                                 _.._            |||||||  ║
║  |||||||    .'_  _'.   skull      ivy      skull .'_  _'.          |||||||  ║
║  |||||||    |(_)(_)|---/////----<\\>----/////---|(_)(_)|          |||||||  ║
║  |||||||    |  /\  |  //  //      ||      \  \  |  /\  |          |||||||  ║
║  |||||||    |_/  \_| //__//       ||       \__\ |_|  \_|          |||||||  ║
║  |||||||      /||\    /||\        ||        /||\    /||\            |||||||  ║
║  |||||||     /_||_\  /_||_\      /__\      /_||_\  /_||_\           |||||||  ║
╚══════════════════════════════════════════════════════════════════════════════╝
```

# ShellRPG Organisation

> Public top-level overview of the ShellRPG project landscape.
>
> This README contains **public-safe information only**. Private server internals, security mechanisms, operational details, and other owner-only material are intentionally excluded.

## What ShellRPG is

**ShellRPG** is a server-authoritative dark-fantasy RPG ecosystem with four clearly separated artifact roles:

- **ShellRPG-server** — proprietary simulation and authority core
- **ShellRPG-client** — public shell / terminal client
- **ShellRPG-www** — public web client
- **ShellRPG-wiki** — redacted documentation and knowledge layer

At its center is a persistent fantasy world with tick simulation, hybrid combat, world map traversal, factions, crafting, trade, cities, garrisons, sieges, and multilingual output.

## Public repositories and their purpose

## 1. ShellRPG-client
Public terminal client for command input, status display, map awareness, event feedback, and shell-native interaction.

## 2. ShellRPG-www
Public web client for graphical overview, world map, character view, inventory, market panels, and comfort-oriented interactions.

## 3. ShellRPG-wiki
Public and redacted knowledge layer for worldbuilding, systems, usage guides, glossary, and FAQ.

## 4. ShellRPG-server
The server is part of the overall ecosystem but is only described publicly at a high level.

Public-safe summary:
- it is the source of truth
- it resolves world state, combat, visibility, economy, cities, garrisons, and events
- public clients are never authoritative for critical state

## How the repositories connect

The organization is intentionally **not** a loose collection of unrelated repositories. The artifacts are logically coupled:

- `ShellRPG-client` and `ShellRPG-www` talk to the same authoritative core
- `ShellRPG-wiki` documents the world, the usage model, and redacted system views
- changes to state, contracts, or interaction logic typically affect multiple repositories

## Governance model

ShellRPG uses three governance layers:

1. **SERVER-PRIVAT**
2. **CLIENT-PUBLIC**
3. **WIKI-REDACTED**

This separation is a core principle for safety, release discipline, and documentation clarity.

## What visitors should understand here

Visitors should quickly learn:
- what ShellRPG is
- which repositories are public
- what each artifact is meant for
- how public clients and the redacted documentation relate to each other
- that there is a hard boundary between public surfaces and the private server core

## Build and usage model at a high level

Typical public order:
1. make the server available in a suitable environment
2. start either the terminal client or the web client
3. use the wiki as handbook and reference

Detailed build/run steps belong in the artifact-specific READMEs.

## Release and versioning philosophy

ShellRPG uses versioned artifact states.

Project rule:
- **pure build / bug fixes do not automatically increment the version number**
- functional expansions produce new functional revisions

## Public project themes

- terminal RPG UX
- web interface for the same world state
- factions, cities, economy, and tile buildings
- crafting, socketing, enchanting, and soulstone systems
- monsters, biomes, and weapon breadth
- garrisons, militia, generals, and faction pressure
- redacted lore and world documentation

## What this organization README intentionally does not do

It is:
- **not** a full server technical reference
- **not** an anti-cheat specification
- **not** an operator handbook
- **not** a replacement for artifact-level READMEs

It is the **public map of the organization**.

## Google AdSense / ads

GitHub READMEs are not the right place for AdSense integration. GitHub sanitizes rendered markdown and strips styling/script behavior heavily, so README-based ad integration is neither reliable nor appropriate. If monetization is ever relevant, a separately hosted site is the correct surface.

## Recommended reading order

- **New visitors** → start here, then read `ShellRPG-wiki`
- **Players / testers** → `ShellRPG-client` and `ShellRPG-www`
- **Lore readers** → `ShellRPG-wiki`
- **Public-surface contributors** → `ShellRPG-client`, `ShellRPG-www`, and `ShellRPG-wiki`

## FAQ

### Is the server public?
No. It is described publicly only at a high level.

### Are there two clients?
Yes. A terminal client and a web client.

### Is the wiki only about lore?
No. It also contains usage, glossary, FAQ, and redacted system documentation.

### Where do I find build and start steps?
Inside the artifact-specific READMEs.

```text
╔══════════════════════════════════════════════════════════════════════════════╗
║  |||||||    Rome / Greek border • laurel ivy • skull relief • ShellRPG    ║
║  |||||||    Public surface only • no private server internals in README    ║
╚══════════════════════════════════════════════════════════════════════════════╝
```
