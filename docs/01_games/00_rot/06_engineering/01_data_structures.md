# Data Structures

## 1. Overview

The ROT project uses structured data models to represent all core gameplay information.

Data structures define how information is stored, updated, and transferred between systems.

Key goals of the data structure design include:

- clear ownership of data
- predictable system interaction
- efficient runtime performance
- clean save/load persistence
- extensibility for future features

All major gameplay systems rely on shared data models.

Examples include:

- player state
- enemy state
- inventory items
- puzzle states
- world state

These models act as the backbone of the gameplay architecture.

---

# 2. Player Data Structure

The Player Data Structure stores all information related to the player character.

This includes:

- health
- inventory
- equipped weapons
- player location
- progression flags

Example structure:

PlayerData
{
playerID
health
maxHealth
stamina
position
rotation
inventory
equippedWeapon
progressionFlags
}

### Field Descriptions

playerID  
Unique identifier for the player profile.

health  
Current health value.

maxHealth  
Maximum health capacity.

stamina  
Used for sprinting or physical actions.

position  
Current world position.

rotation  
Player facing direction.

inventory  
Reference to the player's inventory container.

equippedWeapon  
Current weapon in use.

progressionFlags  
Flags tracking story progress.

---

# 3. Inventory Data Structure

The inventory stores all items carried by the player.

Example structure:

InventoryData
{
maxSlots
items[]
}

### Field Descriptions

maxSlots  
Maximum number of item slots available.

items[]  
Array of item objects currently held by the player.

Each item occupies one slot unless it is stackable.

---

# 4. Item Data Structure

Items represent objects that can be carried or used.

Example structure:

ItemData
{
itemID
itemType
name
description
stackSize
quantity
usable
}

### Field Descriptions

itemID  
Unique item identifier.

itemType  
Defines the item category.

Example categories:

- weapon
- ammo
- healing
- crafting
- key item

name  
Display name.

description  
Inventory description text.

stackSize  
Maximum number of items per stack.

quantity  
Current stack quantity.

usable  
Defines whether the item can be used.

---

# 5. Weapon Data Structure

Weapons extend the item structure with additional fields.

Example structure:

WeaponData
{
weaponID
weaponType
damage
fireRate
ammoType
magazineSize
reloadTime
}

### Field Descriptions

weaponID  
Unique identifier.

weaponType  
Example types:

- handgun
- shotgun
- rifle
- melee

damage  
Base damage value.

fireRate  
Time between shots.

ammoType  
Type of ammunition used.

magazineSize  
Maximum rounds before reload.

reloadTime  
Time required to reload.

---

# 6. Enemy Data Structure

Enemy structures store AI state and combat data.

Example structure:

EnemyData
{
enemyID
enemyType
health
maxHealth
position
state
aggressionLevel
}

### Field Descriptions

enemyID  
Unique identifier.

enemyType  
Enemy category.

Examples:

- Rotter
- Stalker
- Spliced
- Boss

health  
Current health.

maxHealth  
Maximum health.

position  
World position.

state  
Current AI state.

aggressionLevel  
Determines enemy behavior intensity.

---

# 7. Enemy AI State Structure

Enemies operate using AI state machines.

Example structure:

EnemyState
{
stateType
target
lastSeenPlayerPosition
awarenessLevel
}

### Field Descriptions

stateType  
Current behavior state.

Examples:

- Idle
- Patrol
- Suspicious
- Attack
- Search

target  
Current target entity.

lastSeenPlayerPosition  
Last recorded player location.

awarenessLevel  
Tracks detection progress.

---

# 8. Puzzle Data Structure

Puzzle state must persist across gameplay sessions.

Example structure:

PuzzleData
{
puzzleID
state
activatedComponents[]
}

### Field Descriptions

puzzleID  
Unique puzzle identifier.

state  
Puzzle progress.

Example states:

- inactive
- in_progress
- completed

activatedComponents  
List of puzzle elements already activated.

---

# 9. Door and Access Data

Doors and locked access points use a structured data model.

Example structure:

DoorData
{
doorID
locked
keyRequired
opened
}

### Field Descriptions

doorID  
Unique door identifier.

locked  
Boolean value.

keyRequired  
ID of key item required.

opened  
Door open/closed state.

---

# 10. World State Data

The world state tracks permanent environmental changes.

Example structure:

WorldState
{
openedDoors[]
solvedPuzzles[]
defeatedBosses[]
destroyedObjects[]
}

This ensures that the world remains consistent after saving and loading.

# 11. Boss Data Structure

Boss enemies extend the standard enemy structure with additional properties.

Example structure:

BossData
{
bossID
bossType
health
maxHealth
currentPhase
arenaID
defeated
}

### Field Descriptions

bossID  
Unique identifier for the boss encounter.

bossType  
Boss classification.

Examples:

- Bloom
- Mutated Host
- Apex Mutation

health  
Current boss health.

maxHealth  
Maximum health.

currentPhase  
Current boss phase.

arenaID  
Reference to the boss arena.

defeated  
Boolean value indicating whether the boss has been defeated.

---

# 12. Boss Phase Structure

Boss encounters use multiple phases.

Example structure:

BossPhase
{
phaseID
healthThreshold
attackSet[]
environmentChanges[]
}

### Field Descriptions

phaseID  
Identifier for the phase.

healthThreshold  
Health value triggering phase transition.

attackSet[]  
List of attacks available during the phase.

environmentChanges[]  
Arena changes triggered during this phase.

---

# 13. Save Data Structure

Save files contain all persistent gameplay data.

Example structure:

SaveData
{
playerData
inventoryData
worldState
puzzleStates[]
enemyStates[]
storyFlags[]
playtime
}

### Field Descriptions

playerData  
Stored player state.

inventoryData  
Stored player inventory.

worldState  
Persistent world changes.

puzzleStates  
Puzzle completion data.

enemyStates  
Enemy defeat flags.

storyFlags  
Narrative progression markers.

playtime  
Total playtime for the save file.

---

# 14. Story Progression Data

Story progression is tracked through flags.

Example structure:

StoryFlag
{
flagID
activated
}

Example flags:

entered_hospital
harbor_bloom_defeated
halcyon_facility_discovered
final_boss_defeated

Story flags control:

- cutscene triggers
- objective updates
- environment changes

---

# 15. Map Exploration Data

Map exploration tracks which areas the player has discovered.

Example structure:

MapData
{
discoveredAreas[]
unlockedShortcuts[]
visitedSafeZones[]
}

### Field Descriptions

discoveredAreas  
List of explored map sections.

unlockedShortcuts  
List of shortcuts opened by the player.

visitedSafeZones  
List of safe zones discovered.

---

# 16. Interaction Object Data

Interactable objects store state information.

Example structure:

InteractableData
{
objectID
interactionType
activated
}

Examples of interaction types:

- door
- switch
- pickup
- puzzle component
- terminal

---

# 17. Event Data Structure

The event system uses structured event messages.

Example structure:

GameEvent
{
eventType
sourceID
targetID
timestamp
}

Example event types:

PLAYER_DAMAGED
ENEMY_KILLED
ITEM_COLLECTED
PUZZLE_COMPLETED
BOSS_DEFEATED

Events allow systems to react to gameplay changes.

---

# 18. Audio Event Data

Audio events trigger sound playback.

Example structure:

AudioEvent
{
soundID
position
volume
category
}

Example categories:

- ambient
- combat
- UI
- enemy
- environment

---

# 19. Configuration Data

Certain gameplay values should be configurable through data files.

Example structure:

GameConfig
{
difficultyLevel
enemyDamageMultiplier
resourceSpawnRate
enemySpawnRate
}

Configuration files allow designers to tune gameplay without modifying code.

---

# 20. Debug Data Structures

Development builds may include debugging data.

Example structure:

DebugData
{
aiDebugEnabled
puzzleDebugEnabled
collisionDebugEnabled
}

Debug flags enable visualization tools for developers.

---

# 21. Data Serialization

All persistent data must support serialization.

Serialization allows data to be saved and loaded from disk.

Recommended formats include:

JSON  
Binary serialization

Example JSON structure:

{
"playerData": {...},
"inventory": {...},
"worldState": {...}
}

Serialization must remain stable across game updates.

---

# 22. Data Ownership Rules

To prevent data corruption, each system must follow ownership rules.

Examples:

Player System  
Owns PlayerData.

Inventory System  
Owns InventoryData.

Enemy AI System  
Owns EnemyData.

Puzzle System  
Owns PuzzleData.

Other systems should not modify this data directly.

---

# 23. Future Data Extensions

The data structure system must support future features.

Possible extensions include:

- weapon modification data
- advanced enemy behavior models
- dynamic world state changes
- procedural encounter data

Data structures should remain flexible to support future development.

---