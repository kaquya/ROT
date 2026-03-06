# ROT – Technical Design Document (TDD)

Version: 1.0  
Status: Pre-Implementation

---

# 1. Purpose of This Document

This document defines the **technical architecture of ROT**.

While the Game Design Document describes gameplay and narrative design, the Technical Design Document explains **how the game systems will be implemented in code**.

This document defines:

• system architecture  
• core game systems  
• component responsibilities  
• data flow between systems  
• development constraints for a solo developer

The goal is to provide a clear technical blueprint before development begins.

---

# 2. Technical Philosophy

ROT is designed for **solo development**, which means the technical architecture must prioritize:

• simplicity  
• modular systems  
• maintainability  
• performance stability

Large-scale complex systems should be avoided whenever possible.

Instead, the game should rely on **small, focused systems that interact through clearly defined interfaces**.

---

# 3. Engine Architecture

ROT will be built using a modern game engine capable of supporting:

• 3D environments  
• physics interactions  
• dynamic lighting  
• AI navigation  
• modular scripting systems

Recommended engines include:

Unreal Engine  
or  
Unity

The final implementation details may vary depending on the engine used.

However, the **logical architecture described in this document remains the same**.

---

# 4. High-Level System Architecture

The game is built from several major systems.

These systems interact with one another to produce gameplay.

Core Systems:

Player System  
Enemy AI System  
Combat System  
Inventory System  
Interaction System  
Crafting System  
Puzzle System  
Save System  
Audio System  
Environment System

Each system operates independently but communicates through shared game state.

---

# 5. Game State Management

The game maintains a central game state responsible for tracking:

• player progression  
• discovered items  
• defeated enemies  
• puzzle states  
• district unlocks

Game state must be persistent so that it can be saved and restored through the save system.

Important tracked data includes:

Player Inventory  
Player Health  
Unlocked Districts  
Opened Shortcuts  
Destroyed Rot Structures  
Collected Documents

---

# 6. Core System Responsibilities

Each system has clearly defined responsibilities.

---

## Player System

Responsible for:

• player movement  
• camera control  
• player health  
• player interactions

---

## Enemy AI System

Responsible for:

• enemy movement  
• awareness detection  
• enemy behavior states  
• attack behavior

---

## Combat System

Responsible for:

• weapon usage  
• damage calculation  
• enemy hit reactions  
• weak point detection

---

## Inventory System

Responsible for:

• item storage  
• item usage  
• inventory slot management  
• weapon equipment

---

## Crafting System

Responsible for:

• crafting recipes  
• material usage  
• crafting interface

---

## Interaction System

Responsible for:

• environmental interaction prompts  
• doors and switches  
• item pickups  
• puzzle triggers

---

## Save System

Responsible for:

• saving player state  
• restoring game state  
• managing save files

---

# 7. Data Structures

Several core data structures are required.

---

## Item Data

Items require the following information:

Item ID  
Item Type  
Stack Limit  
Description  
Icon  
Usage Effect

---

## Enemy Data

Enemies require:

Enemy Type  
Health Value  
Damage Value  
Movement Speed  
Detection Range

---

## Weapon Data

Weapons require:

Weapon Type  
Damage Value  
Fire Rate  
Ammo Type  
Reload Time

---

# 8. Player Input System

The player input system converts controller or keyboard input into game actions.

Common input actions include:

Move  
Look  
Interact  
Fire Weapon  
Reload  
Open Inventory  
Use Item

These inputs trigger actions inside the Player System.

---

# 9. Update Loop

Most game systems operate within the engine’s update loop.

Typical update flow:

Input Handling  
Player Movement Update  
Enemy AI Update  
Combat Resolution  
Physics Update  
Animation Update  
Audio Update

This loop repeats continuously during gameplay.

---

# 10. Performance Considerations

Because ROT is developed by a single developer, performance stability must be maintained with simple design choices.

Key strategies include:

Limiting active enemy counts  
Using modular environment assets  
Loading districts separately  
Avoiding extremely complex AI systems

These decisions help ensure the game runs smoothly across mid-range PC hardware.

---

# 11. World Loading Architecture

Blackwater Cove is divided into districts rather than a single open world.

Each district loads independently.

This approach provides several benefits:

• reduced memory usage  
• simpler level management  
• improved performance stability  
• easier testing during development

District transitions occur through controlled entry points such as:

• gates  
• roads  
• interior building transitions

When the player enters a new district, the engine unloads the previous district and loads the new environment.

---

# 12. Enemy AI State Machine

Enemy behavior is implemented using a simple state machine.

Each enemy transitions between several awareness states.

---

## Enemy States

Idle

The enemy remains stationary or wanders within a limited area.

---

Suspicious

The enemy investigates unusual sounds or movement.

The enemy moves toward the source of disturbance.

---

Searching

If the player is not immediately located, the enemy searches the nearby area.

---

Aggressive

The enemy has detected the player and actively attacks.

---

Returning

If the player escapes detection, the enemy returns to its patrol or idle state.

---

## State Transitions

State transitions occur based on triggers such as:

• player entering detection range  
• sound detection events  
• losing line of sight

This system allows enemies to behave dynamically without complex AI algorithms.

---

# 13. Combat Damage Pipeline

Combat damage follows a simple pipeline.

---

## Step 1 – Attack Trigger

A weapon attack is initiated by the player.

The combat system checks:

• weapon type  
• ammunition availability  
• cooldown timers

---

## Step 2 – Hit Detection

The engine detects whether the attack hits an enemy.

This may use:

• raycasts for firearms  
• collision detection for melee

---

## Step 3 – Weak Point Check

If the hit location matches an enemy weak point:

Damage multiplier is applied.

Weak points include:

• exposed Rot growth  
• head  
• unstable limbs

---

## Step 4 – Damage Application

Enemy health is reduced based on:

Weapon damage value  
Weak point multiplier  
Enemy resistance

---

## Step 5 – Reaction

The enemy responds with:

• hit animation  
• stagger effect  
• death state if health reaches zero

---

# 14. Inventory Architecture

The inventory system is based on a slot model.

Example configuration:

12 inventory slots.

Each item occupies one slot unless stackable.

Stackable items include:

• ammunition  
• crafting materials

Non-stackable items include:

• weapons  
• key items

---

## Inventory Operations

Add Item

Checks for available slot or stack space.

Remove Item

Reduces item stack or clears slot.

Use Item

Triggers the item’s effect.

Move Item

Allows reorganization of inventory slots.

---

# 15. Crafting System Architecture

Crafting uses recipe-based logic.

Each recipe defines:

• required materials  
• quantity of each material  
• resulting crafted item

Example structure:

Recipe ID  
Required Materials  
Result Item  
Crafting Location

Crafting is restricted to safe zones or designated workbenches.

---

# 16. Puzzle System Architecture

Puzzle interactions are built using trigger-based systems.

Puzzle components include:

Puzzle Trigger  
Puzzle State  
Puzzle Outcome

Example puzzles:

Power restoration

• activate multiple switches  
• restore electricity to area

Access systems

• keycard reader unlocks door

Environmental puzzles

• destroy Rot growth blocking path

Puzzle states are stored in the game state to ensure persistence after saving.

---

# 17. Save System Architecture

The save system stores persistent game data.

Saved data includes:

• player inventory  
• player health  
• district progression  
• puzzle states  
• destroyed Rot structures  
• collected documents

Save files should remain lightweight to ensure fast loading.

---

## Save Trigger

Saving occurs at designated save points located in safe zones.

When saving:

The current game state is serialized into a save file.

---

## Load Process

When loading a save file:

The game restores:

• player location  
• inventory contents  
• puzzle states  
• world progression

---

# 18. Debugging Tools

During development, several debugging tools should be implemented.

These tools dramatically speed up development.

Recommended tools include:

Debug Console

Allows developers to run commands such as:

• spawn enemy  
• teleport player  
• give item

Enemy Debug View

Displays enemy awareness states and detection ranges.

Inventory Debug Tools

Allows adding or removing items quickly.

---

# 19. Logging System

A logging system helps track runtime events.

Examples of logged events:

Enemy detection events  
Combat damage calculations  
Puzzle activation triggers  
Save system operations

Logs should be written in a clear structured format.

---

# 20. Technical Design Goals

The architecture of ROT should prioritize:

• simplicity  
• stability  
• maintainability  
• modular systems

Avoiding overly complex systems ensures the game remains achievable for a solo developer.

The goal is not technical complexity.

The goal is **a stable foundation that supports the survival horror experience**.

---