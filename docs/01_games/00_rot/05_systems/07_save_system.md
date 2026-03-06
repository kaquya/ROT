# Save System

## 1. System Overview

The Save System manages how player progress is recorded and restored in ROT.

The system determines:

- where players can save the game
- when autosaves occur
- what information is stored in save files
- how world state persists across sessions
- how the game recovers after player death

The Save System is intentionally designed to support survival horror gameplay.

Saving progress should feel meaningful and sometimes risky.

Players should feel relief when reaching a safe location where they can record progress.

---

## 2. Design Philosophy

The Save System follows several design principles.

### Tension Through Limited Saves

Players cannot save the game at any moment.

Instead, saving occurs at designated safe locations.

This encourages careful exploration and decision-making.

---

### Fair Progress Protection

Although manual saves are limited, the system prevents excessive progress loss through occasional autosaves.

Autosaves occur at important milestones.

---

### Persistent World State

The world should remain consistent between sessions.

Changes made by the player should remain saved.

Examples include:

- opened shortcuts
- defeated bosses
- solved puzzles
- collected items

---

## 3. Save Points

Save points are specific locations where players can manually save the game.

These locations are typically found in **safe zones**.

Examples include:

- Elena’s house
- emergency coordination center office
- harbor repair garage
- hospital staff break room
- forest ranger cabin
- research facility security room

Save points provide a moment of safety between dangerous exploration segments.

---

## 4. Safe Zones

Save points are usually located in safe zones.

Safe zones provide several functions:

- saving progress
- inventory storage access
- crafting stations
- document review

Enemies cannot enter safe zones.

This allows players to prepare for the next exploration segment.

---

## 5. Manual Save Process

When interacting with a save point, the following occurs.

1. The player activates the save terminal or device.
2. The save interface appears.
3. The player selects a save slot.
4. The current game state is written to the save file.

After saving, the player may continue gameplay.

Manual saves should take only a brief moment to complete.

---

## 6. Autosave System

The game includes limited autosave functionality.

Autosaves occur during important events to prevent excessive progress loss.

Examples include:

- entering a new district
- completing major puzzles
- defeating major bosses
- triggering key story events

Autosaves should never replace manual saving entirely.

They exist to prevent frustration from long progress loss.

---

## 7. Save Slots

The game supports multiple save slots.

Example configuration:

- 5 manual save slots
- 1 autosave slot

Players may maintain separate playthroughs in different slots.

Save slots store independent game progress.

---

## 8. Save Data Contents

Save files must record the current state of the game world.

Core save data includes:

Player Data

- player position
- player health
- player state

Inventory Data

- inventory items
- item quantities
- equipped items

World State

- opened doors
- unlocked shortcuts
- solved puzzles
- destroyed objects

Enemy State

- defeated enemies
- major boss status

Story Progress

- completed story events
- discovered documents

---

## 9. Save File Integrity

Save files must be protected from corruption.

Basic integrity measures include:

- atomic save operations
- file validation checks
- backup autosave slots

These measures ensure that player progress is not lost due to unexpected errors.

---

## 10. Load Process

When loading a saved game, the system restores all saved data.

The following steps occur:

1. Save file is selected.
2. Save data is loaded into memory.
3. Player position and state are restored.
4. Inventory contents are restored.
5. World state changes are applied.
6. Gameplay resumes at the saved location.

Loading should occur quickly to maintain immersion.

---

## 11. Player Death and Recovery

When the player dies, the game restores progress from the most recent save point or autosave checkpoint.

The recovery process follows these steps:

1. Player health reaches zero.
2. Death animation and feedback play.
3. The game displays a death screen.
4. The most recent save state is loaded.
5. The player respawns at the saved location.

The system should clearly communicate the cause of death when possible.

This helps players learn from mistakes.

---

## 12. Checkpoint Behavior

Autosave checkpoints serve as temporary recovery points.

They are typically created during major gameplay events.

Examples include:

- entering a new district
- activating major environmental systems
- defeating a boss
- completing a major puzzle

If the player dies after an autosave, the game restores progress from the autosave slot unless a manual save occurred afterward.

Autosaves should occur silently to avoid interrupting gameplay.

---

## 13. Persistent World State

The Save System ensures that player actions permanently affect the world.

Examples include:

Opened Doors  
Doors that have been unlocked remain unlocked.

Destroyed Objects  
Environmental objects destroyed by the player remain destroyed.

Puzzle Progress  
Solved puzzles remain solved.

Enemy Defeat  
Defeated enemies do not respawn unless specifically scripted.

Boss Defeat  
Major bosses remain defeated permanently.

Persistent world state ensures continuity between gameplay sessions.

---

## 14. Non-Persistent Elements

Certain elements may reset when the game reloads.

Examples include:

Standard Enemy Positions  
Enemies may respawn in specific areas to maintain gameplay challenge.

Consumable Resource Placement  
Some resources may respawn depending on difficulty settings.

Temporary Environmental Effects  
Visual effects or temporary hazards may reset after loading.

These resets help maintain gameplay balance.

---

## 15. Save File Structure

Save files should store structured game data.

Typical save file components include:

PlayerState

- position
- health
- current player state

InventoryState

- item list
- stack quantities
- equipped items

WorldState

- door states
- puzzle states
- shortcut states
- environmental changes

EnemyState

- defeated enemy flags
- boss defeat flags

StoryState

- triggered story events
- discovered documents

SystemSettings

- difficulty level
- playtime

The exact file structure will be defined in the **engineering documentation**.

---

## 16. Save Frequency Guidelines

Saving should occur frequently enough to prevent frustration but not so frequently that tension disappears.

Recommended save distribution:

Safe zones located every major district.

Autosaves triggered at major story events.

Manual saves used for strategic preparation.

Players should never lose excessive progress due to a single mistake.

---

## 17. Edge Cases

The Save System must handle unusual gameplay scenarios.

Examples include:

Saving During Interaction  
If the player attempts to save during an interaction, the system should delay saving until the interaction finishes.

Saving During Combat  
Saving should be disabled while enemies are actively attacking the player.

Interrupted Save Operations  
If saving is interrupted by a system failure, backup recovery should occur.

Invalid Save Data  
The system should detect corrupted save files and prevent loading them.

These safeguards ensure stable gameplay.

---

## 18. Debugging Tools

Development builds should include tools for testing the Save System.

Examples include:

Force Save Command  
Allows developers to manually trigger a save.

Force Load Command  
Allows developers to instantly reload the most recent save.

Save State Viewer  
Displays the current game state being written to save files.

Reset World State  
Allows developers to reset persistent world changes.

These tools assist with debugging and balancing.

---

## 19. System Dependencies

The Save System interacts with several other gameplay systems.

Player Controller

Stores player position and state.

Inventory System

Stores player items and equipment.

World Systems

Stores environmental changes and puzzle states.

Enemy AI System

Tracks defeated enemies and boss encounters.

Story System

Tracks story progression and discovered documents.

UI System

Displays save and load menus.

---

## 20. Future Expansion

The Save System is designed to support future improvements.

Possible expansions include:

additional save slots  
cloud save support  
difficulty-based save restrictions  
chapter-based save checkpoints  

The modular architecture ensures that these features can be added without redesigning the core system.

---