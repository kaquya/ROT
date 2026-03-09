# ROT Documentation

Project: ROT

Documentation Version: 1.1

Status: Active Design Documentation

---

# Overview

This folder contains the **complete design documentation for the ROT project**.

The documentation describes every major aspect of the game and its universe, including:

- franchise worldbuilding
- gameplay systems
- enemy design
- level design
- narrative lore
- engineering architecture
- production planning

The documentation is structured to support **long-term development, system clarity, and collaboration**.

All documents follow a consistent structure to ensure the documentation remains readable and maintainable as the project grows.

---

# Documentation Structure

The documentation is divided into two primary sections:

```
docs/
    00_franchise/
    01_games/
```

---

# Franchise Documentation

Location:

```
docs/00_franchise/
```

This section defines the broader **ROT universe and creative rules** that apply to all ROT projects.

These documents establish the foundation of the franchise, including:

- narrative themes
- visual identity
- creature design philosophy
- environmental storytelling rules
- long-term franchise direction

Subsections include:

```
00_franchise_overview/
01_worldbuilding/
02_visual_direction/
03_creature_design/
04_environment_design/
05_production_strategy/
```

These documents define the **creative identity of the ROT universe**.

---

# ROT Game Documentation

Location:

```
docs/01_games/00_rot/
```

This section contains all documentation specific to the **ROT game project**.

These documents describe the gameplay systems, world design, engineering architecture, narrative structure, and production planning for the game.

---

# Documentation Categories

## Overview

```
00_overview/
```

High level introduction to the game.

Includes:

- game overview
- gameplay pillars
- intended player experience

---

## Game Design

```
01_game_design/
```

Defines the overall design of the game.

Includes:

- game design document
- gameplay loop
- player progression

---

## Core Systems

```
02_core_systems/
```

Documents the main gameplay systems.

Examples include:

- player controller
- combat system
- stealth mechanics
- inventory system
- crafting system
- Rot exposure system
- save system
- UI system
- gameplay audio system

The following files provide entry points for system understanding:

```
systems_overview.md
core_systems_diagram.md
```

---

## Enemy Design

```
03_enemy_design/
```

Defines enemy design philosophy and behavior.

Includes:

- enemy categories
- AI behavior systems
- perception mechanics
- boss encounter structure

---

## Level Design

```
04_level_design/
```

Defines the structure of the game world and exploration systems.

Includes:

- world map
- district design
- encounter design
- puzzle systems
- collectibles
- major setpiece locations
- level design principles

---

## Progression & Balance

```
05_progression_balance/
```

Defines numerical gameplay balance.

Includes:

- player stats
- enemy attributes
- weapons and items
- difficulty scaling
- resource economy
- balance values

---

## Engineering

```
06_engineering/
```

Documents the technical architecture of the game.

Includes:

- project architecture
- core data structures
- game state management
- AI state machines
- input handling
- save data format
- performance strategy

---

## Pipelines

```
07_pipelines/
```

Defines production pipelines for asset creation.

Includes:

- environment pipeline
- enemy pipeline
- animation pipeline
- audio pipeline
- asset naming conventions

---

## Testing

```
08_testing/
```

Defines testing procedures used during development.

Includes:

- test plan
- bug reporting guidelines
- playtesting protocols

---

## Tools

```
09_tools/
```

Documents internal development tools used by the project.

Includes:

- editor tools
- debugging utilities

---

## Lore

```
10_lore/
```

Narrative documentation describing the story and world of ROT.

Includes:

- timeline of Blackwater Cove
- Halcyon Initiative records
- town history
- internal Halcyon factions
- unexplained Rot phenomena
- main character arc
- characters overview

---

## Production

```
11_production/
```

Production planning documents for the game.

Includes:

- implementation plan
- vertical slice plan
- milestone schedule

---

# How to Use This Documentation

If you are new to the project, start with the following documents:

```
01_games/00_rot/00_overview/game_overview.md
01_games/00_rot/00_overview/gameplay_pillars.md
01_games/00_rot/01_game_design/gameplay_loop.md
01_games/00_rot/02_core_systems/systems_overview.md
01_games/00_rot/04_level_design/world_map.md
```

These documents provide a **high-level understanding of the game and its systems**.

More detailed documentation can then be explored depending on the area of development.

---

# Terminology

Canonical terminology used across all ROT documentation is defined in:

```
docs/00_franchise/01_worldbuilding/glossary.md
```

All documents should follow the terminology defined in the glossary.

---

# Development Entry Point

Developers joining the project should begin with:

```
docs/DEVELOPMENT_GUIDE.md
```

This guide explains:

- how the documentation is structured
- which systems should be implemented first
- how development should progress toward the vertical slice

---

# Editing Documentation

When modifying or adding documentation, follow the guidelines defined in:

```
CONTRIBUTING.md
```

These guidelines ensure that documentation remains consistent, readable, and maintainable as the project evolves.

---

# Documentation Philosophy

ROT documentation follows several principles:

**Clarity**

Systems should be explained clearly and without ambiguity.

**Consistency**

Terminology and design philosophy should remain consistent across all documents.

**Modularity**

Each document should focus on a specific system or topic.

**Cross Referencing**

Documents should reference related files where appropriate.

This structure allows the documentation to scale as the project grows.

---

# Status

Documentation Status: Active Design Documentation

Current Version: **1.1**

---