# Player Stats

Project: ROT  
Version: 1.1  
Document Type: Gameplay System  
Category: Progression & Balance  
Scope: ROT (Game)  
Status: Core Reference

---

# 1. Overview

This document defines the core player statistics used in ROT.

Player stats represent the physical condition of the character and determine how the player survives encounters within the Rot ecosystem.

These values influence combat survivability, mobility, and resistance to environmental contamination.

The core player stats include:

- Health  
- Stamina  
- Contamination Tolerance  

These systems interact with other gameplay systems such as combat, traversal, and Rot exposure.

---

# 2. Player Stats Design Philosophy

Player statistics are designed to support the survival horror identity of the game.

## Vulnerability

The player should never feel overly powerful. Health and stamina values are intentionally limited to maintain tension during encounters.

## Resource Management

Players must constantly manage their physical condition. Sprinting, fighting, and navigating dangerous areas all consume resources.

## Environmental Pressure

The Rot ecosystem directly affects player survival through contamination exposure.

This system ensures that the environment itself becomes a threat.

---

# 3. Health

Health represents the player's physical condition and ability to survive damage.

When health reaches zero, the player dies and reloads from the most recent save point.

## Damage Sources

Health can be reduced by several threats including:

- enemy attacks  
- environmental hazards  
- Rot biological attacks  
- falling damage  

## Healing

Health can be restored using medical supplies found throughout the world.

Examples include:

- bandages  
- medical kits  
- emergency treatment supplies  

Healing items are intentionally limited to maintain survival tension.

## Health Feedback

The game should communicate low health through multiple feedback methods.

Examples include:

- visual screen effects  
- character breathing sounds  
- reduced movement confidence  

These cues warn the player before death occurs.

---

# 4. Stamina

Stamina represents the player's physical endurance.

It determines how long the player can perform strenuous actions.

## Stamina Consumption

Stamina is consumed by actions such as:

- sprinting  
- heavy melee attacks  
- certain traversal movements  

When stamina is depleted, the player becomes temporarily exhausted.

## Stamina Recovery

Stamina gradually regenerates when the player stops performing strenuous actions.

Recovery speed may vary depending on the player's current condition.

## Gameplay Impact

Stamina management is critical during enemy encounters.

Players must decide when to sprint, fight, or retreat.

Poor stamina management can leave the player vulnerable to attack.

---

# 5. Contamination Tolerance

Contamination tolerance represents the player's resistance to Rot exposure.

This stat determines how quickly the player is affected by Rot contamination within infected environments.

## Exposure Sources

Rot exposure may occur through:

- heavily contaminated environments  
- Rot biomass structures  
- biological attacks from infected creatures  
- airborne spores or toxins  

## Tolerance Function

Higher tolerance allows the player to survive longer within contaminated areas before negative effects occur.

Lower tolerance causes contamination effects to appear more quickly.

## Interaction with Rot Exposure System

Contamination tolerance interacts directly with the Rot Exposure System.

As exposure increases, the player may experience:

- visual distortions  
- physical weakness  
- biological symptoms  

Managing exposure becomes a key survival mechanic in later areas.

---

# 6. Stat Balancing Philosophy

Player stats should remain carefully balanced throughout the game.

The player should feel capable of surviving encounters but never completely safe.

Balancing goals include:

- maintaining survival tension  
- rewarding careful play  
- preventing players from ignoring environmental dangers  

Stat adjustments may occur through equipment upgrades or narrative progression.

---

# 7. Integration with Other Systems

Player stats interact with several gameplay systems.

Examples include:

- Combat System for damage and stamina use  
- Rot Exposure System for contamination mechanics  
- Inventory System for healing items  
- Level Design for environmental hazards  

These interactions ensure player survival depends on multiple interconnected systems.

---

# 8. Purpose of This Document

This document defines the core player statistics used in ROT.

Health, stamina, and contamination tolerance form the foundation of the player's survival capabilities.

These systems reinforce the survival horror design of the game by limiting player power and emphasizing careful resource management.

---

## Related Documents

[Combat System](../02_core_systems/combat_system.md)  
[Rot Exposure System](../02_core_systems/rot_exposure_system.md)  
[Inventory System](../02_core_systems/inventory_system.md)  
[UI System](../02_core_systems/ui_system.md)  

---