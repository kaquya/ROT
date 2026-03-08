# ROT – Survival Horror Game Documentation

Version: 1.1
Status: Active Design Documentation

---

# Overview

This repository contains the **complete design documentation for ROT**, a narrative-driven survival horror game set in the coastal town of **Blackwater Cove**.

ROT focuses on **biological horror, ecological mutation, and exploration-driven storytelling**.
The world is being consumed by a mysterious biological system known as **the Rot**, which restructures living organisms into new ecological forms.

This repository serves as the **central design reference** for the project and documents every major aspect of the game, including:

* gameplay systems
* enemy design
* level design
* narrative lore
* engineering architecture
* production planning

The documentation is intended to support **long-term development and collaboration**.

---

# What is ROT?

ROT is a **narrative survival horror game** built around exploration, environmental storytelling, and tactical survival.

Players explore the abandoned coastal town of **Blackwater Cove**, uncovering the truth behind the Rot ecosystem and the research conducted by the mysterious **Halcyon Initiative**.

The game emphasizes:

* survival tension
* ecological horror
* exploration-based progression
* narrative discovery through environment and collectibles

The Rot is not a traditional infection.

Instead, it behaves like a **biological restructuring system**, reorganizing life and environments into a new ecosystem.

---

# Core Design Pillars

ROT is designed around several core pillars.

### Survival Horror Tension

Resources are limited.
Combat is dangerous.
Players must carefully manage health, stamina, and contamination.

---

### Ecological Horror

The Rot behaves like a living ecosystem.

Creatures, environments, and structures become integrated into a biological network that reshapes the world.

---

### Exploration-Driven Progression

Players progress by exploring the world, discovering new locations, unlocking shortcuts, and uncovering narrative fragments.

The game encourages curiosity and careful observation of the environment.

---

### Environmental Storytelling

The story of Blackwater Cove is discovered through:

* abandoned locations
* collectible documents
* environmental clues
* Halcyon research records

Players reconstruct the history of the outbreak by piecing together fragments of information.

---

# Repository Structure

The repository is organized into two main sections:

```
docs/
```

```
00_franchise/
```

Franchise-level documentation that defines the overall universe and creative rules for the ROT setting.

Includes:

* worldbuilding
* visual identity
* creature design rules
* environment design philosophy
* franchise direction

These documents guide **all projects set in the ROT universe**.

---

```
01_games/
    00_rot/
```

Game-specific documentation for the first ROT project.

This section contains detailed design documentation for every system in the game.

Key categories include:

| Folder                 | Description                        |
| ---------------------- | ---------------------------------- |
| 00_overview            | High-level description of the game |
| 01_game_design         | Core game design documents         |
| 02_core_systems        | Gameplay systems                   |
| 03_enemy_design        | Enemy behavior and design          |
| 04_level_design        | World layout and exploration       |
| 05_progression_balance | Player and enemy balance           |
| 06_engineering         | Technical architecture             |
| 07_pipelines           | Asset production pipelines         |
| 08_testing             | QA and testing procedures          |
| 09_tools               | Internal development tools         |
| 10_lore                | Narrative and world lore           |
| 11_production          | Development planning               |

---

# Key Documents

If you are new to the project, start with these documents.

### Game Overview

```
01_games/00_rot/00_overview/game_overview.md
```

Provides a high-level explanation of the game concept and setting.

---

### Gameplay Pillars

```
01_games/00_rot/00_overview/gameplay_pillars.md
```

Defines the core design philosophy of the game.

---

### Gameplay Loop

```
01_games/00_rot/01_game_design/gameplay_loop.md
```

Explains the main gameplay cycle:

```
explore → scavenge → survive → uncover story → progress
```

---

### Rot Exposure System

```
01_games/00_rot/02_core_systems/rot_exposure_system.md
```

One of the core mechanics of the game.

Defines contamination mechanics and how the Rot affects the player.

---

### World Map

```
01_games/00_rot/04_level_design/world_map.md
```

Describes the structure of Blackwater Cove and its districts.

---

### Timeline

```
01_games/00_rot/10_lore/timeline.md
```

Historical timeline of the outbreak and events surrounding the town.

---

# Development Philosophy

The project follows several design principles.

### Consistency

All systems should follow consistent terminology and design philosophy.

---

### Modular Design

Systems are designed to be modular and expandable.

This allows the game to scale without requiring major rewrites.

---

### Exploration First

The world should encourage curiosity and reward players who investigate their surroundings.

---

### Mystery Over Explanation

Not every aspect of the Rot is meant to be fully understood.

Some mysteries remain intentionally unexplained to reinforce the horror themes.

---

# Versioning

All documents include a **version identifier**.

Current documentation version:

```
ROT Documentation – Version 1.1
```

Version numbers are updated when major structural changes or design revisions occur.

---

# Contributing

When editing or adding documentation:

1. Maintain consistent formatting across documents.
2. Follow the existing folder structure.
3. Avoid duplicating information across multiple files.
4. Update version numbers when major revisions occur.
5. Cross-reference related documents when appropriate.

Documentation should remain **clear, concise, and production-ready**.

---

# License

This repository contains design documentation for the ROT project.

All content is part of the ROT intellectual property.

Use or distribution of this material outside the project requires permission from the project owner.

---

# Status

Project Status: Active Design Development
Documentation Version: 1.1

---
