# ROT – Development Guide

Version: 1.1

Status: Active Development Preparation

Document Type: Developer Onboarding Guide

---

# 1. Overview

This document explains how developers should approach the ROT project and how the documentation is organized.

ROT is a narrative-driven survival horror game built around exploration, environmental storytelling, and ecological horror.

The project is supported by extensive design documentation that defines every major system of the game.

The purpose of this guide is to help developers quickly understand:

- how the documentation is structured
- which documents are most important
- where to begin implementing the game
- how different systems interact

This document should be the **first file read by anyone beginning development on the project**.

---

# 2. Documentation Structure

All design documentation is located in:

```
docs/
```

The documentation is divided into two major sections.

---

## Franchise Documentation

```
docs/00_franchise/
```

These documents define the overall ROT universe and creative rules.

They include:

- worldbuilding
- creature design philosophy
- visual identity
- environmental storytelling rules
- production strategy

Franchise documentation applies to **all projects set in the ROT universe**, not only this game.

These documents should be consulted when designing new content to ensure consistency with the setting.

---

## Game Documentation

```
docs/01_games/00_rot/
```

This section contains all documentation specific to the ROT game project.

It defines the design and technical structure of the game.

Major sections include:

| Folder | Purpose |
| --- | --- |
| 00_overview | High-level game description |
| 01_game_design | Core design philosophy and gameplay loop |
| 02_core_systems | Gameplay systems |
| 03_enemy_design | Enemy behavior and AI |
| 04_level_design | World layout and exploration |
| 05_progression_balance | Player and enemy balancing |
| 06_engineering | Technical architecture |
| 07_pipelines | Asset production pipelines |
| 08_testing | QA procedures |
| 09_tools | Internal development tools |
| 10_lore | Narrative worldbuilding |
| 11_production | Development planning |

Developers should reference these documents when implementing features.

---

# 3. Key Documents to Read First

New developers should begin with the following documents.

---

## Game Overview

```
docs/01_games/00_rot/00_overview/game_overview.md
```

Provides a high-level description of the game concept and setting.

---

## Gameplay Pillars

```
docs/01_games/00_rot/00_overview/gameplay_pillars.md
```

Defines the core design philosophy that all gameplay systems must support.

---

## Gameplay Loop

```
docs/01_games/00_rot/01_game_design/gameplay_loop.md
```

Explains the fundamental player experience.

Core loop:

```
explore → scavenge → survive → uncover story → progress
```

---

## Systems Overview

```
docs/01_games/00_rot/02_core_systems/systems_overview.md
```

Explains how all gameplay systems interact.

---

## Core Systems Diagram

```
docs/01_games/00_rot/02_core_systems/core_systems_diagram.md
```

Provides a structural overview of the game systems and their dependencies.

---

# 4. Development Priorities

Development should begin by implementing the **core gameplay systems** required for the basic game loop.

Priority order:

1. Player Controller System
2. Interaction System
3. Inventory System
4. Combat System
5. Enemy AI System
6. Rot Exposure System

These systems create the minimal foundation required for a playable prototype.

---

# 5. Vertical Slice

The first major milestone of development is the **vertical slice**.

The vertical slice represents a small but complete section of the game demonstrating all core systems working together.

Details are defined in:

```
docs/01_games/00_rot/11_production/vertical_slice_plan.md
```

The vertical slice should include:

- one playable district
- basic enemy encounters
- exploration mechanics
- inventory and crafting
- Rot exposure system
- narrative collectibles

The purpose of the vertical slice is to validate the game design before full production begins.

---

# 6. Development Principles

The ROT project follows several core development principles.

---

## Consistency

All systems should follow the design philosophy described in the documentation.

---

## Modular Systems

Gameplay systems should be designed to remain modular and easily extendable.

---

## Exploration First

The world should always encourage exploration and discovery.

---

## Environmental Storytelling

Narrative elements should primarily be delivered through environment and collectible documents.

---

# 7. Updating Documentation

Documentation should evolve alongside development.

When modifying systems or adding new features:

- update the relevant design documents
- maintain consistent terminology
- add cross-references where appropriate
- update version numbers for major revisions

Documentation should remain **accurate and useful for development**.

---

# 8. Contributing

All contributors should follow the documentation guidelines defined in:

```
CONTRIBUTING.md
```

These rules define:

- file naming conventions
- markdown formatting
- versioning rules
- documentation structure

---

# 9. Project Status

Current Phase:

```
Preproduction → Vertical Slice Preparation
```

The project has completed the design documentation stage and is preparing for the implementation of the vertical slice.

---

# 10. Purpose of This Document

This guide ensures that developers can quickly understand the structure and goals of the ROT project.

By following the documentation hierarchy and development priorities described here, contributors can begin working on the project without needing extensive onboarding.

---