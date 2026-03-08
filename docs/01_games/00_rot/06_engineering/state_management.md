# State Management

Project: ROT  
Version: 1.1  
Document Type: Engineering  
Category: Technical Architecture  
Scope: ROT (Game)  
Status: Core Reference

---

# 1. Overview

This document defines the architecture used to manage game state in ROT.

Game state management controls how the game tracks progression, system behavior, and world conditions during gameplay.

A clear state management structure ensures that gameplay systems remain synchronized and predictable. It also enables reliable saving, loading, and transitions between different gameplay situations.

This document describes how different game states are organized and how systems interact with them.

---

# 2. State Management Philosophy

Game state management in ROT follows several design principles.

## Centralized State Control

Core game state information should be managed by a central system rather than distributed randomly across systems.

This ensures consistency and reduces errors.

---

## Predictable Transitions

Game states should change through clearly defined transitions.

Unexpected or uncontrolled state changes can lead to inconsistent gameplay behavior.

---

## System Independence

Individual systems should respond to game state changes rather than directly controlling them.

This prevents tightly coupled systems.

---

## Persistence Support

Game state must support saving and loading.

Important gameplay information must be stored in a format that allows reliable restoration of player progress.

---

# 3. Core Game States

The game operates through several high level states.

These states determine what systems are active and how player interaction functions.

---

## Main Menu State

The main menu state represents the initial interface before gameplay begins.

Features include:

- starting a new game  
- loading a saved game  
- accessing settings  
- viewing credits

Gameplay systems are inactive during this state.

---

## Gameplay State

The gameplay state represents the normal play experience.

During this state the following systems are active:

- player movement  
- enemy AI behavior  
- combat systems  
- exploration systems  
- puzzle interactions  
- audio and visual systems

Most gameplay occurs in this state.

---

## Pause State

The pause state temporarily suspends gameplay.

During pause:

- player movement is disabled  
- enemy AI stops updating  
- timers are suspended

Players can access menus such as:

- inventory  
- settings  
- game controls

---

## Cutscene State

The cutscene state is used for scripted narrative sequences.

During this state:

- player input may be limited or disabled  
- camera control may be overridden  
- scripted animations and events occur

Cutscenes communicate key narrative moments.

---

## Loading State

The loading state occurs when transitioning between areas or loading saved data.

During loading:

- gameplay systems are temporarily inactive  
- assets and world data are prepared

The loading state ensures smooth transitions between environments.

---

# 4. World State

In addition to global game states, the game also tracks world state information.

World state describes the condition of the game world and environment.

Examples include:

- which districts have been unlocked  
- completed puzzle states  
- enemy spawn conditions  
- environmental changes caused by Rot spread

World state information ensures that player actions persist throughout the game.

---

# 5. Player State

The player entity maintains several internal states.

Examples include:

- normal movement state  
- sprinting state  
- crouching state  
- combat state  
- interaction state

These states control player behavior and animation.

---

# 6. Enemy State

Enemies also operate through defined behavior states.

Examples include:

- idle or patrol  
- investigation  
- detection  
- chase  
- attack  
- retreat

These states are controlled by the Enemy AI System.

---

# 7. Event Driven State Changes

State transitions are typically triggered through events.

Examples include:

- entering a new area  
- activating a puzzle mechanism  
- triggering a narrative event  
- enemy detection of the player

Event driven transitions help ensure that systems respond consistently.

---

# 8. Save and Load Integration

State management must support the save system.

Important state data stored in save files includes:

- player statistics  
- inventory contents  
- puzzle completion states  
- district progression  
- discovered collectibles

Loading a save file restores the game state exactly as it was when the player saved.

---

# 9. Debug and Development Tools

Development tools may allow developers to inspect or modify game states during testing.

Examples include:

- forcing state transitions  
- viewing system state values  
- debugging AI states

These tools assist with testing and balancing.

---

# 10. Integration with Other Systems

State management interacts with multiple gameplay systems.

Examples include:

- Save System for persistence  
- Enemy AI System for behavior states  
- Player Controller System for movement states  
- Puzzle System for progression tracking

These systems rely on consistent state information to function correctly.

---

# 11. Purpose of This Document

This document defines how game state is organized and managed within ROT.

A well structured state management system ensures that gameplay systems remain synchronized, stable, and maintainable throughout development.

Clear state architecture also supports reliable saving, loading, and progression tracking.

---