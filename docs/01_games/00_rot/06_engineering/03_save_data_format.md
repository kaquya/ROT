# Save Data Format

## 1. Overview

The Save Data Format defines how game progress is stored on disk.

The save system must support:

- persistent player progression
- world state persistence
- safe save/load operations
- future compatibility
- protection against corrupted save data

Save files contain all information required to restore the game to a previous state.

This includes:

- player position
- inventory
- world changes
- puzzle completion
- enemy defeat states
- story progression

The save format must remain stable across game updates.

---

# 2. Save File Structure

A save file is composed of several structured data sections.

Example save file layout:

SaveData
{
SaveHeader
PlayerData
InventoryData
WorldState
PuzzleState
EnemyState
StoryState
MapState
GameSettings
}

Each section stores a different category of gameplay data.

---

# 3. Save Header

The save header contains metadata about the save file.

Example structure:

SaveHeader
{
saveVersion
timestamp
playtime
saveSlot
}

### Field Descriptions

saveVersion  
Version of the save file format.

timestamp  
Date and time when the save was created.

playtime  
Total playtime of the save file.

saveSlot  
Save slot index.

This metadata allows the game to validate save compatibility.

---

# 4. Player Data Section

The PlayerData section stores the player’s current state.

Example structure:

PlayerData
{
position
rotation
health
stamina
equippedWeapon
}

### Field Descriptions

position  
Current player world coordinates.

rotation  
Player facing direction.

health  
Current health value.

stamina  
Current stamina value.

equippedWeapon  
Currently equipped weapon ID.

---

# 5. Inventory Data Section

The InventoryData section stores all player items.

Example structure:

InventoryData
{
maxSlots
items[]
}

Example item entry:

ItemEntry
{
itemID
quantity
}

This section restores the player's inventory exactly as it was during the save.

---

# 6. World State Section

The WorldState section stores environmental changes.

Example structure:

WorldState
{
openedDoors[]
destroyedObjects[]
activatedSystems[]
}

Examples:

openedDoors  
Doors unlocked by the player.

destroyedObjects  
Breakable objects removed from the world.

activatedSystems  
Environmental systems such as generators or elevators.

---

# 7. Puzzle State Section

Puzzle progress must be preserved.

Example structure:

PuzzleState
{
puzzleID
state
}

Example states:

inactive  
in_progress  
completed

This ensures solved puzzles remain solved after loading.

---

# 8. Enemy State Section

Enemy states track defeated enemies and boss encounters.

Example structure:

EnemyState
{
defeatedEnemies[]
defeatedBosses[]
}

Example values:

defeatedEnemies = [rotter_102, stalker_12]
defeatedBosses = [harbor_bloom]

Standard enemies may respawn depending on gameplay rules.

Bosses must never respawn.

---

# 9. Story State Section

StoryState tracks narrative progression.

Example structure:

StoryState
{
activeObjective
storyFlags[]
}

Example story flags:

entered_downtown
hospital_discovered
halcyon_research_found
final_boss_defeated

These flags control story events and cutscene triggers.

---

# 10. Map State Section

Map exploration progress must be saved.

Example structure:

MapState
{
discoveredAreas[]
unlockedShortcuts[]
visitedSafeZones[]
}

This ensures the player’s map progress remains accurate after loading.

---

# 11. Serialization Format

Game data must be converted into a storable format before writing to disk.

This process is called **serialization**.

Two formats are supported:

### JSON Serialization

JSON is useful during development.

Advantages:

- human readable
- easy debugging
- simple testing
- flexible structure

Example JSON save structure:

{
"playerData": {...},
"inventoryData": {...},
"worldState": {...},
"storyState": {...}
}

JSON saves are useful for debugging and testing systems.

---

### Binary Serialization

Binary serialization is recommended for release builds.

Advantages:

- smaller file size
- faster read/write speeds
- harder for players to modify

Binary save files are more efficient for production environments.

---

# 12. Save Slot System

The game supports multiple save slots.

Example structure:

SaveSlots
{
slot1
slot2
slot3
}

Each slot contains an independent SaveData structure.

Players may create, overwrite, or delete save slots.

The UI must display information for each slot:

- playtime
- save timestamp
- location name

---

# 13. Autosave System

The game also supports automatic saving.

Autosaves occur at specific moments such as:

- entering a new district
- defeating a boss
- completing major puzzles
- reaching checkpoints

Autosave files use a dedicated save slot.

Example:

autosave_slot

Autosaves should occur silently to avoid interrupting gameplay.

---

# 14. Save Frequency Rules

Save operations should follow specific rules.

Recommended behavior:

Manual saves  
Allowed only at safe zones.

Autosaves  
Triggered by major progression events.

Combat restriction  
Saving should not occur during active combat.

These restrictions maintain tension while preventing frustration.

---

# 15. Corruption Detection

Save files must include integrity checks to detect corruption.

Example fields:

SaveIntegrity
{
checksum
saveVersion
}

If corruption is detected:

- the game should warn the player
- loading should be prevented
- backup recovery should be attempted

This protects player progress.

---

# 16. Backup Save Files

The system should automatically create backup save files.

Example structure:

slot1.save
slot1_backup.save

If the primary save fails to load, the backup can be restored.

Backups help prevent progress loss.

---

# 17. Version Compatibility

Save files must remain compatible with future game updates.

Each save includes a version number.

Example:

saveVersion = 1.0.0

When loading older save files:

- migration logic may update data structures
- missing fields may be initialized with default values

This allows older saves to remain usable.

---

# 18. Save File Location

Save files should be stored in a platform-appropriate directory.

Example structure:

/ROT/Saves/
slot1.save
slot2.save
autosave.save

This directory must be accessible for read/write operations.

---

# 19. Save File Size Management

Save files should remain small to ensure fast loading.

Recommended guidelines:

- avoid storing redundant data
- store only essential world state
- compress large data sections when necessary

Efficient save files improve loading performance.

---

# 20. Save Debug Tools

Development builds should include tools for inspecting save data.

Examples include:

Save Inspector  
Displays current save file contents.

Force Save Command  
Creates a save immediately.

Force Load Command  
Loads a specific save slot.

Reset Save Data  
Clears all save files for testing.

These tools assist with debugging during development.

---

# 21. Future Save Features

The save system architecture should support additional features.

Possible future improvements include:

Steam Cloud saves  
multiple player profiles  
cross-device save synchronization  
chapter-based save checkpoints  

The save format must remain flexible enough to support these features.

---