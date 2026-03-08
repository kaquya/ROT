# Save Data Format

Project: ROT  
Version: 1.1  
Document Type: Engineering  
Category: Persistence System  
Scope: ROT (Game)  
Status: Core Reference

---

# 1. Overview

This document defines the structure and contents of save files used in ROT.

The Save Data Format determines how player progress, world state, and gameplay data are stored so that the game can be resumed at a later time.

The save system must ensure:

- reliable persistence of player progress  
- consistent restoration of world state  
- compatibility across game updates when possible  
- protection against corrupted or incomplete save data  

Save files store only the minimum information required to reconstruct the game state.

All gameplay logic is reconstructed by the game systems when loading a save.

---

# 2. Save System Goals

The save data format is designed with several goals.

## Reliability

Save files must safely store all critical gameplay information required to resume progress.

The system should minimize the risk of data corruption.

---

## Efficiency

Save files should remain compact and efficient.

Only necessary information should be stored. Static game content should not be duplicated in save files.

---

## Compatibility

Where possible, save files should remain compatible across minor game updates.

Version identifiers are used to track the format of saved data.

---

## Clear Structure

Save data must be organized into well defined sections.

This improves debugging and simplifies future modifications.

---

# 3. Save File Structure

A save file contains several major sections.

Typical save structure:

```
SaveData
├── SaveMetadata
├── PlayerState
├── InventoryState
├── WorldState
├── PuzzleState
├── EnemyState
└── CollectibleState
```


Each section stores a specific type of gameplay information.

---

# 4. Save Metadata

Metadata describes basic information about the save file.

Typical fields include:

- save version
- timestamp
- total playtime
- player progress location
- difficulty mode

Metadata is used by the game to identify and display save files in the load menu.

---

# 5. Player State

Player state stores the current condition of the player character.

Typical data includes:

- player position
- current health
- current stamina
- contamination level
- equipped weapon
- active status effects

This information allows the game to restore the player exactly where they left off.

---

# 6. Inventory State

Inventory state stores the contents of the player's inventory.

Data includes:

- list of items carried
- item quantities
- equipped items
- crafting materials

Item identifiers reference the item database rather than storing full item data.

---

# 7. World State

World state tracks changes that have occurred in the environment.

Examples include:

- unlocked districts
- opened shortcuts
- triggered story events
- environmental changes caused by Rot spread

World state ensures the environment remains consistent across play sessions.

---

# 8. Puzzle State

Puzzle state records the progress of puzzle systems throughout the game.

Examples include:

- completed puzzles
- activated generators
- opened locked mechanisms
- restored power systems

Without this data the game would reset puzzle progress each time the player loads a save.

---

# 9. Enemy State

Enemy state stores information about enemies currently present in the world.

Examples include:

- defeated boss encounters
- unique enemy states
- active enemy spawns

Standard enemies may respawn depending on game design rules, so only certain enemy states need to be saved.

---

# 10. Collectible State

Collectible state tracks which collectibles the player has discovered.

Examples include:

- documents found
- audio recordings unlocked
- narrative fragments collected

This allows the player archive system to remain consistent.

---

# 11. Save Slots

The game may support multiple save slots.

Each slot contains a separate save file with its own progress.

Example structure:

```
Saves
├── Slot_01
├── Slot_02
├── Slot_03
```


Players can load, overwrite, or delete individual save slots.

---

# 12. Autosave System

In addition to manual saves, the game may create automatic saves at key moments.

Examples include:

- entering new districts
- completing major objectives
- before boss encounters

Autosaves reduce the risk of losing significant progress.

---

# 13. Save Versioning

Save files include a version identifier.

Example:

```
SaveVersion: 1.1
```


Versioning allows the game to detect incompatible save files after major updates.

Migration systems may be used to convert older save formats when possible.

---

# 14. Error Handling

The save system should detect corrupted or invalid save files.

Possible safeguards include:

- checksum validation
- backup save files
- autosave redundancy

If corruption is detected, the game may attempt to load the most recent valid save.

---

# 15. Integration with Other Systems

The save system interacts with several gameplay systems.

Examples include:

- Player Stats system
- Inventory system
- Puzzle system
- Collectible tracking system
- World progression system

These systems must provide their state data to the save system when a save operation occurs.

---

# 16. Purpose of This Document

This document defines the structure and behavior of save files used in ROT.

A well designed save data format ensures that player progress remains stable, consistent, and recoverable throughout development and gameplay.

---