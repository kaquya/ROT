# Interaction System

Project: ROT  
Version: 1.1  
Document Type: Gameplay System  
Category: Interaction  
Scope: ROT (Game)  
Status: Core Reference  

---

## 1. Overview

The Interaction System defines how the player interacts with objects, structures, and devices within the game world.

Interaction is a core part of exploration and environmental storytelling in ROT. Players must frequently examine objects, open pathways, manipulate equipment, and use items in order to progress through the environment.

Interactions should feel natural and grounded in the physical world. Objects should behave in ways that reflect their real world function and condition.

The interaction system connects the player to the environment and enables gameplay elements such as exploration, puzzle solving, and progression.

---

## 2. Interaction Philosophy

Interactions in ROT follow several design principles.

### Clarity

Players should easily understand which objects can be interacted with. Visual cues, lighting, or contextual prompts should guide attention without overwhelming the environment.

### Contextual Behavior

Objects should behave logically based on their type and condition. For example, damaged doors may open slowly or require effort, while electronic devices may require power before functioning.

### Environmental Integration

Interactions should feel like part of the world rather than isolated gameplay mechanics. Objects should appear as functional parts of the environment.

### Minimal Interface

Interaction prompts should remain subtle so that the player focuses on the environment rather than the interface.

---

## 3. Interaction Types

The system supports several types of player interactions.

### Object Interaction

Players can examine or manipulate objects within the environment.

Examples include:

- picking up items  
- inspecting documents  
- moving small objects  
- collecting resources  

Object interactions often support scavenging and narrative discovery.

---

### Door Interaction

Doors and access points allow players to move between spaces.

Door interactions may include:

- opening or closing doors  
- unlocking doors with keys or tools  
- forcing open damaged doors  
- sliding or mechanical door systems  

Door behavior should reflect the condition of the structure and the environment.

---

### Item Usage

Players may use items directly from their inventory.

Item interactions include:

- using medical supplies  
- activating tools  
- applying equipment upgrades  
- unlocking barriers with keys or tools  

Items should always have a clear purpose tied to survival or progression.

---

### Device Activation

Certain environments contain devices that the player can activate or manipulate.

Examples include:

- power switches  
- generators  
- control panels  
- research equipment  

Device interactions may influence environmental systems such as lighting, locked areas, or machinery.

---

## 4. Interaction Prompts

When the player approaches an interactable object, the system may display a contextual prompt.

Prompts should remain minimal and unobtrusive.

Typical prompt behavior includes:

- appearing only when the player is within interaction range  
- disappearing when the player moves away  
- updating based on the type of interaction available  

The interface should support player awareness without breaking immersion.

---

## 5. Interaction Conditions

Some interactions require specific conditions before they can be performed.

Examples include:

- possessing the correct key or item  
- restoring power to a device  
- clearing environmental obstacles  
- completing earlier exploration steps  

These conditions help structure progression and encourage exploration.

---

## 6. Environmental Interaction Feedback

Interactions should provide clear feedback to the player.

Feedback may include:

- sound effects when interacting with objects  
- animation changes for doors or devices  
- visual indicators when systems activate  
- character movement responses when manipulating objects  

Feedback helps the player understand that their actions are affecting the environment.

---

## 7. Interaction Limitations

Not every object in the environment should be interactive.

Limiting interactions helps maintain environmental realism and prevents unnecessary player confusion.

Objects chosen for interaction should serve one of the following purposes:

- progression  
- survival  
- narrative discovery  
- environmental navigation  

This ensures that interactions remain meaningful.

---

## 8. Integration with Other Systems

The Interaction System connects to several other gameplay systems.

Examples include:

- the Inventory System for item usage  
- the Level Design System for environmental progression  
- the Puzzle System for environmental challenges  
- the Narrative System for document and log discovery  

These connections ensure that interactions support both gameplay and storytelling.

---

## 9. Purpose of This Document

This document defines how players interact with the world in ROT.

By establishing clear interaction rules, the system ensures that objects, doors, items, and devices function consistently across all environments.

These guidelines support exploration, narrative discovery, and environmental immersion.

---

## Related Documents

[Systems Overview](./systems_overview.md)  
[Inventory System](./inventory_system.md)  
[Puzzle System](./puzzle_system.md)  
[Collectibles Design](../04_level_design/collectibles_design.md)  

---