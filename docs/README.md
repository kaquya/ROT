# ROT Documentation

Project: ROT
Documentation Version: 1.1
Status: Active Design Documentation

---

# Overview

This folder contains the complete design documentation for the ROT project.

The documentation describes every major aspect of the game and its universe, including:

* franchise worldbuilding
* gameplay systems
* enemy design
* level design
* narrative lore
* engineering architecture
* production planning

The documentation is organized to support **long-term development, system clarity, and collaboration**.

All files follow a consistent structure to ensure the documentation remains readable and maintainable as the project grows.

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

This section defines the broader ROT universe and creative rules that apply to all ROT projects.

These documents establish the foundation of the franchise, including:

* narrative themes
* visual identity
* creature design philosophy
* environmental storytelling rules
* long-term franchise direction

Subsections include:

```
00_franchise_overview/
01_worldbuilding/
02_visual_direction/
03_creature_design/
04_environment_design/
05_production_strategy/
```

---

# ROT Game Documentation

Location:

```
docs/01_games/00_rot/
```

This section contains all documentation specific to the ROT game project.

These documents describe the gameplay systems, world design, engineering architecture, and narrative structure of the game.

---

# Documentation Categories

## Overview

```
00_overview/
```

High level introduction to the game.

Includes:

* game overview
* gameplay pillars
* intended player experience

---

## Game Design

```
01_game_design/
```

Defines the overall design of the game.

Includes:

* core design document
* gameplay loop
* player progression

---

## Core Systems

```
02_core_systems/
```

Documents the main gameplay systems.

Examples include:

* player controller
* combat system
* stealth mechanics
* inventory system
* crafting system
* Rot exposure mechanics
* save system
* UI systems
* gameplay audio

The `systems_overview.md` file provides a high level explanation of how these systems interact.

---

## Enemy Design

```
03_enemy_design/
```

Defines enemy design philosophy and behavior.

Includes:

* enemy categories
* AI behavior systems
* perception mechanics
* boss encounter structure

---

## Level Design

```
04_level_design/
```

Defines the structure of the game world and exploration systems.

Includes:

* world map
* district design
* encounter design
* puzzle systems
* collectibles
* major setpiece locations

---

## Progression & Balance

```
05_progression_balance/
```

Defines numerical gameplay balance.

Includes:

* player stats
* enemy attributes
* weapons and items
* difficulty scaling
* resource economy

---

## Engineering

```
06_engineering/
```

Documents the technical architecture of the game.

Includes:

* project architecture
* core data structures
* game state management
* AI state machines
* input handling
* save data format
* performance strategy

---

## Pipelines

```
07_pipelines/
```

Defines production pipelines for asset creation.

Includes:

* environment pipeline
* enemy pipeline
* animation pipeline
* audio pipeline
* asset naming conventions

---

## Testing

```
08_testing/
```

Defines testing procedures used during development.

Includes:

* test plan
* bug reporting guidelines
* playtesting protocols

---

## Tools

```
09_tools/
```

Documents internal development tools used by the project.

Includes:

* editor tools
* debugging utilities

---

## Lore

```
10_lore/
```

Narrative documentation describing the story and world of ROT.

Includes:

* timeline of Blackwater Cove
* Halcyon Initiative records
* town history
* internal Halcyon factions
* unexplained Rot phenomena
* main character arc

---

## Production

```
11_production/
```

Production planning documents for the game.

Includes:

* implementation plan
* vertical slice plan
* milestone schedule

---

# How to Use This Documentation

If you are new to the project, start with the following documents:

```
00_overview/game_overview.md
00_overview/gameplay_pillars.md
01_game_design/gameplay_loop.md
02_core_systems/systems_overview.md
04_level_design/world_map.md
```

These files provide a high level understanding of the game and its core systems.

More detailed documents can then be explored depending on the area of development.

---

# Terminology

Canonical terminology used across all ROT documentation is defined in:

```
docs/00_franchise/01_worldbuilding/glossary.md
```

All documentation should follow the definitions provided in the glossary.

---

# Editing Documentation

When modifying or adding documentation, follow the guidelines defined in:

```
CONTRIBUTING.md
```

These guidelines ensure that the documentation remains consistent and easy to maintain as the project evolves.

---