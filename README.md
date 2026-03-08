# ROT – Survival Horror Game Documentation

Documentation Version: 1.1
Project Status: Active Design Development

---

# Overview

This repository contains the complete design documentation for **ROT**, a narrative-driven survival horror game set in the coastal town of **Blackwater Cove**.

ROT focuses on **biological horror, ecological mutation, and exploration-driven storytelling**. The world is being consumed by a mysterious biological system known as **the Rot**, which restructures living organisms and environments into new ecological forms.

This repository serves as the central design reference for the project and documents every major aspect of the game, including:

* gameplay systems
* enemy design
* level design
* narrative lore
* engineering architecture
* production planning

The documentation is intended to support **long-term development, design consistency, and collaboration**.

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

Instead, it behaves like a **biological restructuring system**, reorganizing life and environments into a new ecological ecosystem.

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

The repository is organized into two main sections.

## Documentation

All design documentation is located in:

```
docs/
```

The documentation is divided into two primary areas:

* **Franchise documentation** defining the ROT universe
* **Game-specific documentation** for the ROT project

---

## Franchise Documentation

Location:

```
docs/00_franchise/
```

Franchise-level documentation defines the broader ROT universe and creative rules used across all projects set within the ROT setting.

Topics include:

* franchise vision
* worldbuilding
* Rot ecology
* visual identity
* creature design rules
* environmental storytelling
* franchise production strategy

---

## ROT Game Documentation

Location:

```
docs/01_games/00_rot/
```

Game-specific documentation describes every system used in the ROT project.

Key documentation areas include:

| Folder                 | Description                     |
| ---------------------- | ------------------------------- |
| 00_overview            | High level overview of the game |
| 01_game_design         | Core game design documents      |
| 02_core_systems        | Gameplay systems                |
| 03_enemy_design        | Enemy design and AI             |
| 04_level_design        | World and exploration design    |
| 05_progression_balance | Player and enemy balancing      |
| 06_engineering         | Technical architecture          |
| 07_pipelines           | Asset production pipelines      |
| 08_testing             | Testing and QA procedures       |
| 09_tools               | Internal development tools      |
| 10_lore                | Narrative and world lore        |
| 11_production          | Production planning             |

---

# Documentation Navigation

For a complete index of all documentation files see:

```
docs/README.md
```

This file acts as the **table of contents for the entire documentation system**.

---

# Key Documents

If you are new to the project, start with the following documents.

### Game Overview

```
docs/01_games/00_rot/00_overview/game_overview.md
```

Provides a high-level explanation of the game concept and setting.

---

### Gameplay Pillars

```
docs/01_games/00_rot/00_overview/gameplay_pillars.md
```

Defines the core design philosophy of the game.

---

### Gameplay Loop

```
docs/01_games/00_rot/01_game_design/gameplay_loop.md
```

Explains the main gameplay cycle:

```
explore → scavenge → survive → uncover story → progress
```

---

### Systems Overview

```
docs/01_games/00_rot/02_core_systems/systems_overview.md
```

Provides a high level explanation of how the gameplay systems interact.

---

### World Map

```
docs/01_games/00_rot/04_level_design/world_map.md
```

Defines the structure of Blackwater Cove and its districts.

---

### Timeline

```
docs/01_games/00_rot/10_lore/timeline.md
```

Explains the historical events leading to the Rot outbreak.

---

# Development Philosophy

ROT follows several core development principles.

### Consistency

All systems follow consistent terminology and design philosophy defined across the documentation.

---

### Modular Systems

Gameplay systems are designed to be modular and expandable.

This allows the project to grow without requiring large architectural rewrites.

---

### Exploration First

The world design encourages curiosity and rewards players who investigate their surroundings.

---

### Mystery Over Explanation

Not every aspect of the Rot is meant to be fully understood.

Some mysteries remain intentionally unexplained to reinforce the horror themes of the game.

---

# Versioning

All documentation files include a version identifier.

Current documentation version:

```
ROT Documentation – Version 1.1
```

Version numbers are updated when:

* major structural changes occur
* gameplay systems are redesigned
* documentation architecture changes

Minor edits do not require version updates.

---

# Contributing

When editing or adding documentation:

1. Maintain consistent formatting across all documents.
2. Follow the established folder structure.
3. Avoid duplicating information across multiple files.
4. Update version numbers when major revisions occur.
5. Add cross-references between related documents when appropriate.

Full contribution rules are defined in:

```
CONTRIBUTING.md
```

---

# License

This repository contains design documentation for the ROT project.

All content is part of the ROT intellectual property.

Use, reproduction, or distribution of this material outside the project requires permission from the project owner.

---

# Status

Project Status: Active Design Development
Documentation Version: 1.1

---