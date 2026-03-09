# Core Systems Diagram

Project: ROT

Version: 1.1

Document Type: System Architecture

Category: Core Systems

Scope: Gameplay Systems

Status: Core Reference

---

# 1. Overview

This document provides a high-level overview of how the core gameplay systems of ROT interact with each other.

While individual documents describe specific systems in detail, this file explains how those systems connect to form the complete gameplay experience.

The diagram presented here acts as a **technical and design reference** for developers working on the project.

Understanding these relationships helps ensure that systems are implemented in a consistent and stable architecture.

---

# 2. Core Gameplay System Structure

At the highest level, ROT’s gameplay architecture can be divided into several layers:

- Input Layer
- Player Systems
- Gameplay Systems
- Enemy Systems
- World Systems
- Interface Systems
- Persistence Systems

These layers interact to create the complete gameplay loop.

---

# 3. High-Level System Flow

The following diagram shows the general flow of gameplay systems.

```
Input System
      ↓
Player Controller System
      ↓
Interaction System
      ↓
Gameplay Systems
      ↓
Enemy Systems
      ↓
World Systems
      ↓
UI & Audio Systems
      ↓
Save System
```

Each layer is described in more detail below.

---

# 4. Input Layer

## Input System

The input system processes player input from devices such as keyboard, mouse, or controller.

Responsibilities include:

- movement input
- camera control
- interaction commands
- combat actions

The input system passes commands to the **Player Controller System**.

---

# 5. Player Layer

## Player Controller System

The player controller handles the player character’s physical movement and traversal.

Key responsibilities include:

- walking and sprinting
- crouching
- climbing and traversal
- camera alignment
- collision handling

The player controller acts as the primary interface between player input and gameplay systems.

---

# 6. Gameplay Systems Layer

Several gameplay systems operate together to support the core gameplay loop.

```
Explore → Scavenge → Survive → Uncover Story → Progress
```

These systems include:

### Interaction System

Allows the player to interact with objects in the environment.

Examples include:

- opening doors
- activating devices
- collecting items
- triggering puzzle elements

---

### Inventory System

The inventory system manages player-owned items.

Features include:

- item storage
- equipment slots
- item usage
- item management

The inventory system connects to crafting and interaction systems.

---

### Crafting System

The crafting system allows the player to create useful items from collected resources.

Examples include:

- crafting survival tools
- creating healing items
- producing temporary equipment

Crafting supports long-term survival and resource management.

---

### Combat System

The combat system defines how players fight enemies.

Core mechanics include:

- weapon usage
- attack timing
- hit detection
- stamina interaction

Combat must remain dangerous and resource-intensive to maintain survival horror tension.

---

### Stealth System

The stealth system allows players to avoid enemies.

Key mechanics include:

- visibility detection
- noise generation
- hiding behavior

Stealth provides an alternative to direct combat.

---

### Rot Exposure System

The Rot exposure system tracks the player’s contamination level when entering infected areas.

Effects include:

- gradual contamination buildup
- environmental hazards
- mutation side effects

This system reinforces environmental danger and encourages careful exploration.

---

# 7. Enemy Systems Layer

Enemy behavior is handled through several connected systems.

```
Enemy AI System
        ↓
AI Perception System
        ↓
AI State Machine
        ↓
Combat Behavior
```

### Enemy AI System

Controls enemy movement and decision-making.

Core behaviors include:

- patrol
- investigate
- chase
- attack
- retreat

---

### AI Perception System

Handles enemy awareness of the player.

Detection methods include:

- vision
- sound
- environmental disturbance

This system integrates closely with the stealth system.

---

### AI State Machine

Defines the state transitions that govern enemy behavior.

Typical states include:

- idle
- patrol
- investigate
- chase
- attack

State transitions allow enemies to respond dynamically to player actions.

---

# 8. World Systems Layer

World systems manage the environment and exploration spaces.

These include:

- level design systems
- puzzle mechanics
- environmental hazards
- contamination zones
- encounter triggers

World systems provide the physical environment where gameplay occurs.

---

# 9. Interface Systems

Interface systems communicate game information to the player.

## UI System

The UI system displays gameplay information.

Examples include:

- health and stamina indicators
- inventory interface
- interaction prompts
- menus

The UI should remain minimal to preserve immersion.

---

## Audio Gameplay System

Audio systems provide environmental feedback.

Examples include:

- enemy audio cues
- ambient environmental sound
- tension-building music

Audio plays an important role in survival horror gameplay.

---

# 10. Persistence Layer

## Save System

The save system stores player progress.

Features include:

- save points
- autosave triggers
- checkpoint systems

Saved data includes:

- player stats
- inventory contents
- progression state
- discovered collectibles

---

# 11. Complete System Interaction Diagram

The following diagram summarizes the relationships between major systems.

```
Input System
      ↓
Player Controller
      ↓
Interaction System
      ↓
Inventory System ↔ Crafting System
      ↓
Combat System ↔ Stealth System
      ↓
Enemy AI System
      ↓
AI Perception System
      ↓
AI State Machine
      ↓
World Systems
      ↓
Rot Exposure System
      ↓
UI System + Audio Gameplay System
      ↓
Save System
```

This architecture ensures that gameplay systems remain modular while still interacting in a coherent structure.

---

# 12. Design Goals

The core system architecture follows several design principles.

### Modular Systems

Each gameplay system should function independently whenever possible.

This allows systems to be modified or expanded without affecting unrelated systems.

---

### Clear System Dependencies

Systems should interact through well-defined interfaces.

Dependencies should remain predictable and documented.

---

### Stability First

Core systems must remain stable before adding additional gameplay complexity.

The architecture defined here supports long-term scalability of the game.

---

# 13. Purpose of This Document

This document provides a structural overview of how ROT’s gameplay systems interact.

It serves as a reference for:

- gameplay programming
- technical design
- system integration
- debugging and troubleshooting

By maintaining a clear understanding of system relationships, the development team can ensure that the game’s architecture remains stable as the project grows.

---

## Related Documents

[Plyer Controller System](./player_controller_system.md)  
[Combat System](./combat_system.md)  
[Stealth System](./stealth_system.md)  
[Inventory System](./inventory_system.md)  
[Crafting System](./crafting_system.md)  
[Interaction System](./interaction_system.md)  
[Rot Exposure System](./rot_exposure_system.md)  
[Enemy AI System](../03_enemy_design/enemy_ai_system.md)     
[AI Perception System](../03_enemy_design/ai_perception_system.md)   
[Audio Gameplay System](./audio_gameplay_system.md)  
[Save System](./save_system.md)  
[Project Architecture](../06_engineering/project_architecture.md)  

---