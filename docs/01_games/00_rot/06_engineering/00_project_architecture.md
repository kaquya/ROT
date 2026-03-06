# Project Architecture

## 1. Architecture Overview

The ROT project uses a **modular system architecture** designed for long-term maintainability and scalability.

Each gameplay system is implemented as an independent module with clearly defined responsibilities.

This architecture ensures that:

- systems remain loosely coupled
- new features can be added safely
- debugging remains manageable
- code remains readable for a solo developer

The architecture separates the project into several major layers:

Game Systems  
Core gameplay logic and mechanics.

World Systems  
Environmental logic and level behavior.

Player Systems  
Player control, combat, and inventory.

AI Systems  
Enemy behavior and state logic.

Interface Systems  
UI and player feedback systems.

Infrastructure Systems  
Saving, input handling, and state management.

Each system communicates through controlled interfaces rather than direct dependencies.

---

## 2. Core Architectural Principles

The architecture follows several core engineering principles.

### Modular Design

Each gameplay feature exists as a separate system.

Example systems:

- Player Controller
- Inventory System
- Combat System
- Enemy AI System
- Puzzle System
- Save System

Each module should operate independently whenever possible.

---

### Single Responsibility

Each system has a clearly defined purpose.

Example:

The Inventory System manages items only.

It does not handle UI rendering or player input directly.

---

### Clear Data Ownership

Each system owns its internal data.

Example:

Enemy AI System owns enemy state data.

Other systems may read this data but should not directly modify it.

---

### Event-Based Communication

Systems communicate through events rather than direct function calls.

Example events:

EnemyDetectedPlayer  
PlayerPickedUpItem  
PuzzleSolved  
BossDefeated

Event-driven architecture reduces system coupling.

---

## 3. High-Level System Layout

The project is organized into major gameplay systems.

Game Application
|
|--- Input System
|
|--- Player Systems
| |--- Player Controller
| |--- Combat System
| |--- Inventory System
| |--- Interaction System
|
|--- World Systems
| |--- Puzzle System
| |--- Environmental Systems
|
|--- AI Systems
| |--- Enemy AI
| |--- Boss AI
|
|--- Interface Systems
| |--- UI System
| |--- Audio System
|
|--- Infrastructure
|--- Save System
|--- Game State Manager


Each system operates independently but interacts through defined interfaces.

---

## 4. Game State Management

The Game State Manager controls the overall state of the game.

Typical states include:

Main Menu  
Player navigates menus.

Gameplay  
Player actively explores the world.

Combat  
Triggered during enemy encounters.

Boss Encounter  
Triggered during boss fights.

Paused  
Game paused through menu.

Game Over  
Triggered when the player dies.

The Game State Manager ensures systems behave correctly during each state.

Example:

Combat music activates only during combat state.

---

## 5. Scene Architecture

The game world is divided into scenes.

Each scene represents a major area of the game.

Examples:

Residential District  
Downtown District  
Hospital  
Forest  
Halcyon Facility

Scenes contain:

environment geometry  
enemy spawn points  
puzzle objects  
interactive objects  
audio zones

Scenes should remain modular to allow efficient loading.

---

## 6. Scene Loading Strategy

The project uses controlled scene loading.

Two approaches are used:

Full Scene Loading  
Used when transitioning between major districts.

Subscene Loading  
Used for large areas containing multiple subzones.

Example:

Hospital scene may contain several interior sections loaded dynamically.

This prevents performance issues.

---

## 7. System Update Order

Systems update in a defined sequence during each frame.

Typical order:

1. Input System  
2. Player Controller  
3. Enemy AI System  
4. Combat System  
5. Puzzle System  
6. Physics System  
7. UI System  
8. Audio System  

This ensures consistent gameplay behavior.

---

## 8. Data Flow

Game data flows between systems in controlled ways.

Example interaction:

Player fires weapon.

Combat System calculates damage.

Enemy AI receives damage event.

Enemy state updates.

UI System updates enemy health display.

Audio System plays hit sound.

Event-driven communication ensures clean data flow.

---

## 9. Script Organization

Game scripts should follow a clear directory structure.

Example structure:

/scripts
/player
/combat
/inventory
/ai
/world
/ui
/audio
/systems


Each directory contains scripts related to that specific system.

This improves project navigation.

---

## 10. Error Handling

The architecture must support safe error handling.

Example safeguards:

null reference checks  
invalid state detection  
system initialization validation  

Errors should be logged clearly for debugging.

Robust error handling prevents runtime crashes.

---

## 11. System Initialization Order

When the game starts, systems must initialize in a predictable order.

Improper initialization can cause missing references, broken dependencies, or unstable behavior.

Recommended initialization sequence:

1. Core Infrastructure
   - Logging System
   - Event System
   - Configuration Loader

2. Input System
   - Player input bindings
   - Controller detection

3. Save System
   - Load player profile
   - Load game state

4. Player Systems
   - Player Controller
   - Inventory System
   - Combat System
   - Interaction System

5. World Systems
   - Puzzle System
   - Environmental Systems

6. AI Systems
   - Enemy AI
   - Boss AI

7. Interface Systems
   - UI System
   - Audio System

This ensures that dependent systems always initialize after the systems they rely on.

---

## 12. Dependency Management

Dependencies between systems must remain minimal.

Systems should communicate through defined interfaces or events rather than direct references.

Example of poor dependency:

Combat System directly modifying enemy state.

Example of correct dependency:

Combat System emits a DamageEvent.

Enemy AI System receives the event and updates its internal state.

This approach reduces tight coupling and prevents cascading bugs.

---

## 13. Service Systems

Certain global systems act as shared services used across the game.

Examples include:

Event System  
Manages global gameplay events.

Save System  
Handles persistence and save data.

Input System  
Handles keyboard and controller input.

Audio System  
Manages sound playback.

These services are accessible across systems but must remain lightweight and stable.

---

## 14. Singleton Usage Guidelines

Singletons should be used sparingly.

Singletons are appropriate for systems that must exist only once during the game's lifetime.

Examples:

Game State Manager  
Audio System  
Input System  
Save System

Avoid creating unnecessary singletons for gameplay logic systems.

Gameplay systems should instead be referenced through service interfaces.

---

## 15. Event System

The Event System allows systems to communicate indirectly.

Example event types:

PlayerDamaged
EnemyKilled
ItemCollected
PuzzleSolved
BossDefeated


Events follow this flow:

System emits event → Event System broadcasts → Subscribed systems respond.

This architecture allows systems to react without hard dependencies.

---

## 16. Memory Management Strategy

Efficient memory usage is critical for stable performance.

Key strategies include:

Object Pooling  
Reuse frequently created objects such as bullets or particle effects.

Asset Streaming  
Load large assets only when required.

Lazy Initialization  
Initialize systems only when needed.

Garbage Reduction  
Avoid unnecessary object creation during gameplay loops.

These practices help maintain stable frame rates.

---

## 17. Asset Loading Strategy

Assets must be loaded efficiently to avoid performance spikes.

Two asset loading approaches are recommended.

Preloaded Assets

Essential assets loaded at scene start.

Examples:

player models  
basic UI elements  
common sound effects

Dynamic Loading

Assets loaded when required.

Examples:

boss models  
large environmental props  
rare enemy variants

Dynamic loading helps keep memory usage manageable.

---

## 18. Logging System

A centralized logging system should track system behavior.

Logs help identify issues during development and testing.

Example log categories:

System Initialization  
AI State Changes  
Puzzle Interactions  
Save/Load Operations  
Error Reports

Logs should include timestamps and system identifiers.

Example:

[EnemyAI] Rotter detected palyer
[PuzzleSystem] Power generator activated


This greatly simplifies debugging.

---

## 19. Debug Mode Architecture

Development builds should include debugging features.

Examples include:

System State Inspector  
Displays active systems and states.

AI Debug Visualization  
Shows enemy detection ranges and paths.

Puzzle Debug Mode  
Displays puzzle state variables.

Save Data Viewer  
Displays stored save data structures.

Debug features must be disabled in release builds.

---

## 20. Code Style Guidelines

Consistent coding practices improve maintainability.

Recommended guidelines:

Use descriptive function names.

Avoid overly long functions.

Separate logic and data structures.

Keep system responsibilities clear.

Document complex logic clearly.

Readable code is essential for solo development.

---

## 21. Scalability Considerations

The architecture must support future expansions.

Potential future needs include:

new enemy types  
new weapon systems  
additional puzzle mechanics  
expanded UI systems  
additional districts or environments

Systems should remain flexible enough to support these additions without redesigning core architecture.

---

## 22. Development Workflow

The project architecture supports an iterative development workflow.

Typical development cycle:

1. Implement core system.
2. Test in isolated environment.
3. Integrate with other systems.
4. Validate gameplay behavior.
5. Optimize performance.

Small, incremental changes reduce the risk of introducing major bugs.

---

## 23. Future Architecture Improvements

As development progresses, the architecture may evolve.

Potential improvements include:

advanced event routing  
data-driven configuration systems  
editor tooling for system debugging  
procedural content support

These improvements should be added only when necessary.

Premature complexity should be avoided.

The primary goal of the architecture is stability, clarity, and maintainability for a solo developer project.

---