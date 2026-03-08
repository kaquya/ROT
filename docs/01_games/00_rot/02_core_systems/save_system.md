# Save System

Project: ROT  
Version: 1.1  
Document Type: Gameplay System  
Category: Progression / Persistence  
Scope: ROT (Game)  
Status: Core Reference  

---

# 1. Overview

The Save System defines how player progress is stored and restored during gameplay.

Saving in ROT should support the survival horror experience by maintaining tension and consequences while preventing excessive loss of progress.

The system combines **manual save points**, **limited autosaves**, and **checkpoint logic** to balance player safety with meaningful risk.

Saving should never completely remove tension from exploration, but it should ensure that players do not lose large amounts of progress due to unexpected failure.

---

# 2. Save System Philosophy

The save system follows several design principles.

### Controlled Saving

Players should not be able to save anywhere at any time. Saving should occur at specific locations or moments.

### Tension Preservation

Save placement should maintain gameplay tension. Dangerous areas should not allow frequent saving.

### Player Respect

Progress loss should be limited. Players should not be forced to repeat excessive portions of the game.

### Environmental Integration

Save points should exist naturally within the world rather than appearing as abstract menu mechanics.

---

# 3. Save Points

Save points are specific locations where players can manually save their progress.

These locations are usually placed in relatively safe areas.

Examples include:

- research terminals in laboratories  
- field equipment stations  
- safe rooms or shelter areas  
- communication terminals  

Save points should be visually recognizable and consistent across the game.

---

## 3.1 Save Point Behavior

When interacting with a save point:

- the player's current progress is stored
- inventory and equipment states are saved
- world state changes are recorded
- player position is stored

Save points should clearly communicate when the save has successfully completed.

---

# 4. Autosave System

Autosaves occur automatically during key progression moments.

Autosaves help protect player progress when entering new areas or completing important actions.

Autosave triggers may include:

- entering a new district or major location  
- completing a major objective  
- unlocking a new exploration route  
- discovering important narrative milestones  

Autosaves should occur discreetly without interrupting gameplay.

---

# 5. Checkpoint Rules

Checkpoints determine where the player resumes after death or failure.

Checkpoint logic is closely related to the autosave system.

When the player dies or fails, they are returned to the most recent checkpoint.

Checkpoint data may include:

- player location  
- inventory state  
- world state changes  
- objective progression  

Checkpoint placement should ensure that players do not need to repeat large sections of gameplay.

---

# 6. Safe Zones

Certain areas in the game function as safe zones.

Safe zones often contain save points and serve as temporary recovery locations.

Characteristics of safe zones include:

- absence of hostile enemies  
- access to save points  
- opportunities to manage inventory  
- temporary relief from Rot exposure hazards  

Safe zones provide moments of calm within the survival experience.

---

# 7. Save Restrictions

To maintain gameplay tension, certain restrictions apply.

Examples include:

- saving may be disabled during combat encounters  
- saving may be restricted during scripted events  
- saving may require interacting with specific devices  

These restrictions ensure that saving does not trivialize dangerous situations.

---

# 8. World State Persistence

The save system must preserve important world changes.

Examples include:

- opened shortcuts or unlocked doors  
- completed puzzles or activated devices  
- defeated enemies or cleared areas  
- collected items and discovered logs  

Persistent world states help the game feel consistent and reactive to player actions.

---

# 9. Integration with Other Systems

The Save System interacts with several gameplay systems.

Examples include:

- the Inventory System for storing player items  
- the Progression System for tracking exploration progress  
- the Narrative System for recording discovered story elements  
- the Rot Exposure System for saving contamination levels  

These systems ensure that player progress is accurately preserved.

---

# 10. Purpose of This Document

This document defines how player progress is saved in ROT.

The Save System balances player protection with survival horror tension by combining manual save points, autosaves, and checkpoint rules.

Following these guidelines ensures that saving supports the pacing and atmosphere of the game.

---