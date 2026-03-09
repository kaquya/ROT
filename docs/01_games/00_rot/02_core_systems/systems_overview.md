# Systems Overview

Project: ROT  
Version: 1.1  
Document Type: Systems  
Category: Core Gameplay Systems  
Scope: Gameplay Architecture  
Status: Core Reference

---

# 1. Overview

This document provides a high level overview of how the core gameplay systems in ROT interact with each other.

While individual systems are defined in their own documents, this file explains how those systems form the complete gameplay architecture.

This document should serve as the **entry point for engineers and system designers** who need to understand how the major gameplay systems connect.

Detailed behavior for each system can be found in their respective documentation files.

---

# 2. Core Gameplay Systems

The following systems form the foundation of the ROT gameplay architecture.

Core systems include:

- Player Controller System
- Combat System
- Stealth System
- Interaction System
- Inventory System
- Crafting System
- Rot Exposure System
- Save System
- UI System
- Audio Gameplay System

These systems work together to support the core gameplay loop:

```
explore → scavenge → survive → uncover story → progress
```


---

# 3. System Interaction Philosophy

The systems in ROT follow several architectural principles.

## Modular Design

Each system should operate as a modular component.

Systems communicate through defined interfaces rather than tightly coupled dependencies.

This allows systems to be modified or expanded without breaking unrelated gameplay features.

---

## Event Driven Communication

Whenever possible, systems communicate using gameplay events.

Examples include:

- player takes damage
- enemy detects player
- item collected
- contamination increased

Event driven communication helps reduce direct dependencies between systems.

---

## Player Centric Architecture

Most gameplay systems ultimately revolve around the player.

The player controller acts as the primary interaction point between gameplay systems and the world.

---

# 4. Player Controller System

Document: `player_controller_system.md`

The player controller manages the player's physical interaction with the game world.

Responsibilities include:

- player movement
- sprinting
- crouching
- climbing
- camera control
- traversal behavior

The player controller acts as the foundation upon which most other gameplay systems operate.

Many systems rely on player state information such as:

- movement speed
- stance
- stamina level
- environmental position

---

# 5. Combat System

Document: `combat_system.md`

The combat system manages all offensive player actions.

Responsibilities include:

- weapon usage
- melee attacks
- ranged attacks
- hit detection
- damage calculation

Combat interacts with several other systems.

Examples:

Combat → Enemy AI  
Enemies react to damage and adjust behavior.

Combat → Stamina System  
Certain actions consume stamina.

Combat → Audio System  
Combat generates sound cues detectable by enemies.

Combat → Rot Exposure  
Certain enemies may cause contamination when attacking.

---

# 6. Stealth System

Document: `stealth_system.md`

The stealth system determines whether enemies detect the player.

Core stealth mechanics include:

- player visibility
- noise generation
- enemy detection ranges

Stealth interacts with several systems.

Examples:

Stealth → Enemy AI  
Enemy detection triggers investigation or pursuit.

Stealth → Player Controller  
Movement speed and stance affect visibility and noise.

Stealth → Audio System  
Sound produced by the player may alert enemies.

---

# 7. Interaction System

Document: `interaction_system.md`

The interaction system allows the player to manipulate objects in the environment.

Examples include:

- opening doors
- activating switches
- collecting items
- interacting with devices

This system connects exploration with puzzle solving and resource acquisition.

Interactions frequently trigger gameplay events used by other systems.

---

# 8. Inventory System

Document: `inventory_system.md`

The inventory system manages the player's collected items.

Responsibilities include:

- item storage
- equipment slots
- item usage
- resource tracking

The inventory system connects to several gameplay systems.

Examples:

Inventory → Crafting System  
Resources stored in the inventory can be used for crafting.

Inventory → Combat System  
Weapons and consumables are accessed through the inventory.

Inventory → UI System  
The inventory interface displays stored items.

---

# 9. Crafting System

Document: `crafting_system.md`

The crafting system allows players to create new items using collected resources.

Examples include:

- healing items
- ammunition
- utility tools

Crafting interacts with:

Crafting → Inventory  
Consumes stored resources.

Crafting → UI System  
Crafting menus allow players to combine items.

Crafting → Resource Economy  
Crafting materials are distributed throughout the world.

---

# 10. Rot Exposure System

Document: `rot_exposure_system.md`

The Rot exposure system tracks the player’s level of biological contamination.

Sources of contamination include:

- Rot biomass environments
- contaminated enemies
- specific environmental hazards

Increasing contamination may cause:

- health degradation
- visual distortions
- environmental hallucinations
- eventual death or mutation

This system reinforces the ecological horror theme of the game.

---

# 11. Save System

Document: `save_system.md`

The save system manages player progress persistence.

Features include:

- manual saves at safe zones
- checkpoint based autosaves
- stored player state

The save system records data from multiple systems, including:

- player stats
- inventory contents
- progression flags
- discovered collectibles

---

# 12. UI System

Document: `ui_system.md`

The UI system displays gameplay information to the player.

UI elements include:

- health indicators
- stamina indicators
- Rot contamination level
- inventory interface
- interaction prompts

The UI system receives information from many other systems and presents it in a readable format.

---

# 13. Audio Gameplay System

Document: `audio_gameplay_system.md`

The gameplay audio system provides auditory feedback for gameplay events.

Examples include:

- enemy audio cues
- environmental ambience
- stealth sound indicators
- combat sound effects

Audio also plays a role in gameplay mechanics.

Enemy AI may detect player generated sound events.

---

# 14. High Level System Interaction

The following simplified structure shows how core systems connect.

```
Player Controller
|
v
Interaction System
|
v
Inventory System -----> Crafting System
|
v
Combat System
|
v
Enemy AI System
|
v
Rot Exposure System

All systems communicate with:
UI System
Audio Gameplay System
Save System
```


This structure allows the player to interact with the world, encounter enemies, manage resources, and experience the effects of the Rot ecosystem.

---

# 15. Related Documents

player_controller_system.md  
combat_system.md  
stealth_system.md  
interaction_system.md  
inventory_system.md  
crafting_system.md  
rot_exposure_system.md  
save_system.md  
ui_system.md  
audio_gameplay_system.md  

---

# 16. Purpose of This Document

This document provides a high level overview of how gameplay systems interact within ROT.

Understanding these relationships helps developers implement features consistently and ensures that new systems integrate smoothly with the existing gameplay architecture.

---

## Related Documents

[Player Controller System](./player_controller_system.md)  
[Combat System](./combat_system.md)  
[Stealth System](./stealth_system.md)  
[Inventory System](./inventory_system.md)  
[Crafting System](./crafting_system.md)  
[Rot Exposure System](./rot_exposure_system.md)  
[Save System](./save_system.md)  
[UI System](./ui_system.md)  
[Audio Gameplay System](./audio_gameplay_system.md)  
[Core Systems Diagram](./core_systems_diagram.md)  

---