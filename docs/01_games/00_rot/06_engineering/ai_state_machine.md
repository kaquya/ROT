# AI State Machine

Project: ROT  
Version: 1.1  
Document Type: Engineering  
Category: AI Architecture  
Scope: ROT (Game)  
Status: Core Reference

---

# 1. Overview

This document defines the AI state machine architecture used by enemy creatures in ROT.

The AI state machine controls how enemies transition between behaviors such as patrolling, investigating disturbances, chasing the player, and attacking.

Rather than relying on scripted sequences, enemy behavior is driven by state transitions triggered by perception events, environmental conditions, and internal logic.

The goal is to create enemies that feel reactive and biologically motivated while remaining predictable enough for players to learn and adapt.

This document focuses on the **state transition logic**, while detailed behavior descriptions are defined in:

- `enemy_ai_system.md`
- `ai_perception_system.md`

---

# 2. AI State Machine Philosophy

The AI state machine follows several key design principles.

## Clear Behavioral States

Each enemy behavior must exist in a clearly defined state.

This improves debugging and ensures that enemies cannot perform conflicting actions.

---

## Event Driven Transitions

State changes occur in response to events rather than constant polling.

Examples include:

- detecting the player
- hearing a sound
- losing visual contact
- taking damage

Event driven transitions improve performance and create more natural behavior.

---

## Predictable Structure

While enemies may behave unpredictably within a state, the structure of state transitions should remain consistent.

Players should learn how enemies escalate from suspicion to combat.

---

# 3. Core AI States

Most enemy types use a shared set of core states.

Different creatures may extend or modify this structure depending on their biological role.

Core states include:

- Idle  
- Patrol  
- Investigation  
- Alert  
- Chase  
- Attack  
- Search  
- Retreat  

---

# 4. Idle State

The idle state represents passive enemy behavior when no threats are detected.

Typical behaviors include:

- standing in place
- performing ambient animations
- observing the environment

Idle enemies may transition to patrol behavior after a short time.

---

# 5. Patrol State

During patrol, enemies move through a defined territory.

Patrol paths may include:

- predefined routes
- randomized wandering
- territory loops

While patrolling, enemies actively monitor the environment for unusual stimuli.

Possible transitions from patrol include:

- investigation
- alert state

---

# 6. Investigation State

The investigation state occurs when an enemy detects suspicious activity.

Triggers may include:

- unusual sounds
- partial visual detection
- environmental disturbances

During investigation:

- the enemy moves toward the disturbance
- the enemy searches the surrounding area
- the enemy becomes more alert

If no threat is confirmed, the enemy eventually returns to patrol.

---

# 7. Alert State

The alert state occurs when the enemy strongly suspects the presence of the player.

This state represents a brief escalation before full pursuit.

Typical behaviors include:

- focusing attention toward the player location
- preparing for chase
- emitting warning vocalizations

Alert may transition into chase if the player is confirmed.

---

# 8. Chase State

During the chase state, the enemy actively pursues the player.

Chase behavior may include:

- rapid movement
- pathfinding through complex environments
- obstacle navigation

The enemy remains in chase until one of the following occurs:

- the player enters attack range
- the enemy loses sight of the player
- the enemy is interrupted

---

# 9. Attack State

The attack state occurs when the player is within the enemy's attack range.

Attack behavior varies by creature but may include:

- melee strikes
- lunging attacks
- biological projectile attacks
- area based attacks

Enemies may briefly return to chase if the player escapes attack range.

---

# 10. Search State

The search state occurs when the enemy loses track of the player during pursuit.

During search:

- the enemy investigates nearby locations
- the enemy checks hiding spots
- the enemy listens for further sound cues

If the player is not rediscovered, the enemy eventually returns to patrol.

---

# 11. Retreat State

Some enemies may retreat under specific conditions.

Triggers for retreat may include:

- severe damage
- environmental hazards
- territorial limits
- biological survival behavior

Retreating enemies disengage from combat and attempt to reach a safe location.

Not all enemies support this state.

---

# 12. State Transition Diagram

Typical AI state flow:

Idle  
↓  
Patrol  
↓  
Investigation  
↓  
Alert  
↓  
Chase  
↓  
Attack  

If the player escapes:

Attack → Chase → Search → Patrol

Optional transitions:

Attack → Retreat  
Investigation → Patrol

This flow ensures encounters escalate gradually.

---

# 13. State Interruptions

Certain events may interrupt the current state.

Examples include:

- taking damage
- environmental hazards
- new perception events

Interruptions may force transitions such as:

- Patrol → Alert
- Attack → Chase
- Chase → Search

Interrupt rules help prevent enemies from becoming stuck in incorrect states.

---

# 14. Enemy Variants

Different enemies may modify the base state machine.

Examples include:

Scavenger enemies

- simpler state transitions
- short investigation periods

Predator enemies

- aggressive chase behavior
- extended search states

Apex mutations

- complex multi-phase behaviors
- additional special states

---

# 15. Debugging and Visualization

Development tools should allow visualization of AI states.

Useful debugging features include:

- displaying current AI state above enemies
- showing perception ranges
- highlighting patrol routes
- logging state transitions

These tools assist in balancing and troubleshooting AI behavior.

---

# 16. Integration with Other Systems

The AI state machine interacts with several systems.

Examples include:

- AI Perception System for detection events
- Enemy AI System for behavior execution
- Combat System for attack actions
- Navigation System for pathfinding

Together these systems create reactive and believable enemy behavior.

---

# 17. Purpose of This Document

This document defines the AI state transition architecture used by enemy creatures in ROT.

A clear state machine structure ensures that enemy behavior remains predictable, maintainable, and scalable as new enemy types are introduced.

This system forms the foundation for enemy behavior across the game.

---

## Related Documents

[Enemy AI System](../03_enemy_design/enemy_ai_system.md)  
[AI Perception System](../03_enemy_design/ai_perception_system.md)  
[State Management](./state_management.md)  

---