# Data Structures

Project: ROT  
Version: 1.1  
Document Type: Engineering  
Category: Technical Architecture  
Scope: ROT (Game)  
Status: Core Reference

---

# 1. Overview

This document defines the core data structures used to represent game state and gameplay entities in ROT.

Data structures are the underlying models that store information used by gameplay systems such as combat, inventory, AI behavior, and world interaction.

Well designed data models ensure that systems remain modular, predictable, and easy to maintain.

This document focuses on conceptual data models rather than engine specific implementations.

---

# 2. Data Model Design Principles

The data architecture of ROT follows several principles.

## Clarity

Data models should clearly represent the concept they describe.

Each structure should have a specific responsibility and avoid unnecessary complexity.

---

## Modularity

Data structures should be reusable across systems.

For example, an entity health structure may be used by both player characters and enemy creatures.

---

## Data Driven Design

Whenever possible, gameplay behavior should be defined through data rather than hard coded logic.

This allows designers to adjust game balance without modifying code.

Examples include:

- enemy statistics  
- item definitions  
- weapon properties  
- encounter configurations

---

## Separation of State and Behavior

Data structures should store information, while gameplay systems control behavior.

For example:

- an enemy data model stores health and detection range  
- the AI system determines how the enemy behaves

This separation improves maintainability.

---

# 3. Entity Data Model

Most interactive objects in the game world are represented as entities.

Entities include:

- the player  
- enemies  
- interactive objects  
- environmental hazards

### Entity Data Fields

Typical entity information includes:

- unique entity identifier  
- entity type  
- position and orientation  
- current state  
- associated components

Entities may contain modular components representing specific functionality.

---

# 4. Player Data Structure

The player entity contains information related to the player's state and progression.

### Core Player Data

Key data fields include:

- current health  
- maximum health  
- current stamina  
- contamination level  
- contamination tolerance

### Progression Data

Additional information may include:

- inventory contents  
- discovered collectibles  
- unlocked shortcuts  
- completed objectives

This data is used by the save system to restore player progress.

---

# 5. Enemy Data Structure

Enemy entities represent hostile organisms within the Rot ecosystem.

### Core Enemy Data

Important enemy attributes include:

- enemy type identifier  
- health value  
- attack damage  
- movement speed  
- detection range

### Behavioral Data

Additional data may include:

- current AI state  
- patrol route information  
- aggression level  
- target entity

Enemy behavior is controlled by the AI system using this information.

---

# 6. Item Data Structure

Items represent objects the player can collect, use, or interact with.

### Core Item Data

Typical item data fields include:

- item identifier  
- item category  
- item name  
- description text  
- stack limit

### Gameplay Attributes

Some items contain additional gameplay data such as:

- healing amount  
- crafting material value  
- weapon damage values

Items are stored within the player inventory system.

---

# 7. Inventory Data Structure

The inventory stores the items carried by the player.

### Inventory Fields

Typical inventory information includes:

- list of stored items  
- item quantities  
- equipment slots  
- inventory capacity

Inventory limits encourage resource management.

---

# 8. Weapon Data Structure

Weapons are specialized items with combat attributes.

### Weapon Attributes

Common weapon fields include:

- weapon identifier  
- weapon type  
- damage value  
- stamina cost  
- durability (optional)

Additional properties may include attack animations or special effects.

---

# 9. Environmental Object Data

Environmental objects represent interactive structures in the world.

Examples include:

- doors  
- generators  
- puzzle mechanisms  
- destructible objects

### Environmental Object Fields

Typical information includes:

- object identifier  
- interaction type  
- current state  
- required key item (if applicable)

These objects interact with the interaction and puzzle systems.

---

# 10. Save Game Data Structure

The save system stores the persistent game state.

### Saved Data

Important information includes:

- player statistics  
- inventory contents  
- discovered collectibles  
- unlocked shortcuts  
- puzzle completion states

This data allows the player to resume progress from save points.

---

# 11. Event Data

Events represent temporary gameplay occurrences triggered by player actions or system updates.

Examples include:

- enemy detection events  
- puzzle activation events  
- environmental triggers  
- narrative triggers

Event data may include:

- event type  
- triggering entity  
- affected entities  
- timestamp

Event systems allow different gameplay systems to communicate efficiently.

---

# 12. Integration with Other Systems

Data structures are used across multiple systems.

Examples include:

- Combat System uses weapon and enemy data  
- Inventory System manages item data  
- AI System reads enemy behavior data  
- Save System stores player and world data

Consistent data models ensure reliable interaction between systems.

---

# 13. Purpose of This Document

This document defines the key data structures used within ROT.

By maintaining clear and modular data models, the project ensures that gameplay systems remain flexible, maintainable, and scalable throughout development.

These structures provide the foundation for implementing the technical architecture of the game.

---

## Related Documents    

[Project Architecture](./project_architecture.md)  
[Save Data Format](./save_data_format.md)  
[Inventory System](../02_core_systems/inventory_system.md)  
[Player Stats](../05_progression_balance/player_stats.md)   
[Enemy Stats](../05_progression_balance/enemy_stats.md)   
[Enemy AI System](../03_enemy_design/enemy_ai_system.md)   
[AI Perception System](../03_enemy_design/ai_perception_system.md)   
[State Management](./state_management.md)   

---