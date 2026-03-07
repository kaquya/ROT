# Vertical Slice Specification

This document defines the **Vertical Slice** of ROT.

The vertical slice is a **small, fully playable section of the game** that demonstrates all core gameplay systems working together.

The goal is not to build the full game, but to validate:

- player movement
- combat systems
- enemy AI
- exploration
- inventory
- puzzles
- environmental storytelling

The vertical slice should be **polished enough to represent the final gameplay experience** on a smaller scale.

---

# Vertical Slice Goals

The vertical slice must demonstrate the core gameplay loop:

```
Explore
↓
Encounter Enemy
↓
Fight / Stealth / Escape
↓
Collect Resources
↓
Solve Puzzle
↓
Unlock Shortcut
↓
Reach Safe Zone
```

All major gameplay systems should be functional.

The vertical slice will act as the **foundation for the rest of development**.

---

# Location

The vertical slice takes place in the **Residential District of Blackwater Cove**.

This area represents the **start of the game** and introduces players to the core mechanics.

The district should feel like a believable abandoned neighborhood.

Environment features:

- small suburban houses
- narrow streets
- alleyways
- backyard paths
- environmental destruction
- early Rot corruption

---

# Map Scope

The map should remain **small and manageable** while still providing exploration.

Approximate scope:

Area size: Small district section  
Estimated playtime: 20–30 minutes  

Map elements:

- 3 enterable houses
- 1 safe house
- 1 courtyard encounter area
- 1 alley shortcut
- 1 locked gate puzzle
- 1 mini-boss encounter

The map should contain **multiple paths** that reconnect through shortcuts.

---

# Core Gameplay Systems Included

The vertical slice must implement the following systems.

---

## Player Controller

Movement states:

- walking
- sprinting
- crouching
- aiming

Camera control must function properly.

---

## Interaction System

Players must be able to interact with:

- doors
- items
- puzzle objects
- containers

Interaction prompts should be visible.

---

## Inventory System

The player should have a functioning inventory.

Features required:

- item pickup
- item stacking
- weapon slots
- inventory UI

---

## Combat System

Combat must support:

- handgun weapon
- melee attack
- enemy damage
- player damage
- weak point damage

Enemies must react to attacks.

---

## Enemy AI

The following enemies should appear in the vertical slice.

Rotter × 5

Shadow Stalker × 1

Mini Boss (Caretaker) × 1

Enemies must support:

- idle state
- detection
- chasing
- attacking
- returning to patrol

---

## Stealth System

Players must be able to avoid enemies by:

- crouching
- staying out of sight
- minimizing noise

Enemies must respond to sound and sight.

---

## Puzzle System

The vertical slice includes a simple puzzle.

Example puzzle:

Power Fuse Puzzle

Steps:

1. Find a fuse inside a house
2. Insert fuse into electrical box
3. Restore power to open the district gate

This puzzle introduces environmental problem solving.

---

## Save System

The vertical slice must contain a safe zone.

Safe house functions:

- save progress
- access inventory
- access storage

This introduces the **safe room concept**.

---

# Weapons Available

Only a small selection of weapons is needed.

Weapons included in the vertical slice:

Handgun (M9 Pistol)

Combat Knife

Shotgun ammunition may appear as a teaser item but the weapon itself is not yet usable.

---

# Items and Resources

The slice should include a limited set of resources.

Examples:

Handgun Ammo

Bandage

Alcohol

Cloth

Fuse (key item)

Items should be placed in believable locations such as:

- kitchen drawers
- storage cabinets
- garages
- abandoned vehicles

---

# Environmental Storytelling

The vertical slice should include early signs of the outbreak.

Examples:

- overturned furniture
- abandoned evacuation vehicles
- blood trails
- broken barricades
- Rot growth beginning to appear on surfaces

Players should begin to understand that the town collapsed rapidly.

---

# Mini Boss Encounter

The vertical slice includes a mini boss encounter.

Mini Boss: **Caretaker**

Location: Apartment courtyard.

The Caretaker is a heavily mutated Rot creature formed from multiple infected residents.

Encounter design:

- enclosed courtyard arena
- environmental obstacles
- limited movement space

The boss should demonstrate:

- enemy durability
- multi-hit combat
- threat escalation

---

# Completion Objective

The vertical slice ends when the player unlocks the **Residential District Gate** leading toward Downtown.

Completing the slice should feel like the **end of a small self-contained chapter**.

---

# Systems Validation

The vertical slice should confirm that the following systems work correctly together:

- player movement
- combat
- AI behavior
- inventory management
- puzzle interaction
- safe zone functionality

If the vertical slice is successful, development can safely proceed to larger districts.

---

# Future Expansion

Once the vertical slice is complete, development can expand the world to include:

- Downtown District
- Police Station
- Harbor District
- Hospital
- Forest Region
- Halcyon Research Center
- Underground Facility

The vertical slice serves as the **foundation for all future level development**.

---