# ROT – Survival Horror Game

Documentation Version: 1.1

Project Status: Preproduction / Vertical Slice Preparation

---

# Overview

This repository contains the **complete design documentation and development structure for ROT**, a narrative-driven survival horror game set in the coastal town of **Blackwater Cove**.

ROT focuses on **biological horror, ecological mutation, and exploration-driven storytelling**. The world is being consumed by a mysterious biological system known as **the Rot**, which restructures living organisms and environments into new ecological forms.

This repository serves as the **central reference for development**, documenting every major aspect of the project, including:

- gameplay systems
- enemy design
- level design
- narrative lore
- engineering architecture
- production planning

The documentation exists to ensure **design consistency, clear development direction, and long-term maintainability**.

---

# What is ROT?

ROT is a **narrative survival horror game** built around exploration, environmental storytelling, and tactical survival.

Players explore the abandoned coastal town of **Blackwater Cove**, uncovering the truth behind the Rot ecosystem and the research conducted by the mysterious **Halcyon Initiative**.

The game emphasizes:

- survival tension
- ecological horror
- exploration-based progression
- narrative discovery through environment and collectibles

The Rot is not a traditional infection.

Instead, it behaves like a **biological restructuring system**, reorganizing life and environments into a new ecological structure.

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

- abandoned locations
- collectible documents
- environmental clues
- Halcyon research records

Players reconstruct the history of the outbreak by piecing together fragments of information.

---

# Repository Structure

The repository is organized into several main sections.

```
ROT/
│
├─ docs/
├─ game/
├─ CONTRIBUTING.md
├─ DEVELOPMENT_GUIDE.md
└─ README.md
```

---

## docs/

Contains **all design documentation** for the project.

Documentation is divided into two major areas:

```
docs/00_franchise/
docs/01_games/00_rot/
```

---

### Franchise Documentation

Location:

```
docs/00_franchise/
```

Defines the broader **ROT universe and creative rules**.

Topics include:

- franchise vision
- worldbuilding
- Rot ecology
- visual identity
- creature design rules
- environmental storytelling
- franchise production strategy

These documents guide **all projects set in the ROT universe**.

---

### ROT Game Documentation

Location:

```
docs/01_games/00_rot/
```

Contains all **game-specific design documentation**.

| Folder | Description |
| --- | --- |
| 00_overview | High-level overview of the game |
| 01_game_design | Core design documents |
| 02_core_systems | Gameplay systems |
| 03_enemy_design | Enemy design and AI |
| 04_level_design | World and exploration design |
| 05_progression_balance | Balance and progression |
| 06_engineering | Technical architecture |
| 07_pipelines | Asset production pipelines |
| 08_testing | Testing and QA procedures |
| 09_tools | Internal development tools |
| 10_lore | Narrative and world lore |
| 11_production | Production planning |

---

## game/

The `game/` directory will contain the **actual game project and source code**.

Typical contents may include:

```
game/
├─ source/
├─ assets/
├─ configs/
└─ build/
```

This folder will be populated as development progresses.

---

# Documentation Navigation

For a full documentation index see:

```
docs/README.md
```

This file acts as the **table of contents for the entire documentation system**.

---

# Developer Entry Points

If you are new to the project, start with these documents.

### Development Guide

```
DEVELOPMENT_GUIDE.md
```

Provides onboarding information for developers joining the project.

---

### Game Overview

```
docs/01_games/00_rot/00_overview/game_overview.md
```

High-level explanation of the game concept.

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

Main gameplay cycle:

```
explore → scavenge → survive → uncover story → progress
```

---

### Systems Overview

```
docs/01_games/00_rot/02_core_systems/systems_overview.md
```

Explains how gameplay systems interact.

---

### World Map

```
docs/01_games/00_rot/04_level_design/world_map.md
```

Defines the structure of Blackwater Cove.

---

### Timeline

```
docs/01_games/00_rot/10_lore/timeline.md
```

Describes the events leading to the Rot outbreak.

---

# Development Philosophy

ROT follows several core development principles.

### Consistency

All systems follow consistent terminology and design philosophy defined across the documentation.

---

### Modular Systems

Gameplay systems are designed to be modular and expandable.

This allows the project to scale without major architectural changes.

---

### Exploration First

The world should encourage curiosity and reward exploration.

---

### Mystery Over Explanation

Not every aspect of the Rot is meant to be fully understood.

Some mysteries remain intentionally unexplained to reinforce the horror themes.

---

# Versioning

All documentation files include a version identifier.

Current documentation version:

```
ROT Documentation – Version 1.1
```

Version numbers are updated when:

- major structural changes occur
- gameplay systems are redesigned
- documentation architecture changes

Minor edits do not require version updates.

---

# Contributing

When editing or adding documentation:

1. Maintain consistent formatting across documents
2. Follow the established folder structure
3. Avoid duplicating information across multiple files
4. Update version numbers when major revisions occur
5. Add cross-references between related documents

Full contribution rules are defined in:

```
CONTRIBUTING.md
```

---

# License

This repository contains design documentation and development materials for the ROT project.

All content is part of the ROT intellectual property.

Use, reproduction, or distribution of this material outside the project requires permission from the project owner.

---

# Status

Project Status: Preproduction

Next Milestone: **Vertical Slice**

Documentation Version: **1.1**

---