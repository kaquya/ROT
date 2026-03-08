# Enemy AI System

Project: ROT  
Version: 1.1  
Document Type: Gameplay System  
Category: Enemy AI  
Scope: ROT (Game)  
Status: Core Reference  

---

# 1. Overview

The Enemy AI System defines how creatures perceive the world, react to the player, and behave within the Rot ecosystem.

Enemy behavior in ROT should feel **biologically motivated rather than scripted**. Creatures act according to instinct, environmental conditions, and ecological role.

AI behavior must support the survival horror experience by creating unpredictable but understandable encounters.

Enemies should behave in ways that feel natural for their biological structure and ecological function.

Core AI behavior states include:

- patrol
- chase
- attack
- retreat

Additional states such as investigation or idle behavior may exist depending on creature type.

---

# 2. AI Design Philosophy

Enemy AI follows several design principles.

### Ecological Behavior

Creatures should appear to exist independently of the player. They patrol territories, investigate disturbances, and interact with their environment.

The player enters an ecosystem rather than triggering scripted enemy spawns.

---

### Readable Behavior

Enemy intentions should be communicated through clear visual and audio cues.

Players should be able to interpret:

- when a creature has noticed something
- when it is preparing to attack
- when it is searching for a target
- when it disengages from combat

Readable behavior allows players to react strategically.

---

### Unpredictability

While enemy behavior should be logical, it should not become entirely predictable.

Small variations in behavior patterns help maintain tension.

Examples include:

- different patrol routes
- varied investigation patterns
- unexpected environmental movement

---

# 3. AI Perception

Enemy perception determines how creatures detect the player.

Detection is typically based on two primary senses.

### Visual Detection

Enemies can detect the player when the player enters their line of sight.

Detection speed depends on:

- distance from the player
- lighting conditions
- player movement speed
- player posture

Standing or sprinting in open areas increases detection risk.

---

### Audio Detection

Enemies may react to sound produced by the player.

Common sound triggers include:

- sprinting
- combat actions
- interacting with objects
- environmental noise

Enemies may move toward the source of the sound to investigate.

---

# 4. Patrol Behavior

Patrol behavior represents the default state of many creatures.

During patrol:

- enemies move within a defined territory
- enemies follow environmental paths or wandering patterns
- enemies remain alert for unusual sounds or movement

Patrol routes may vary depending on creature type.

Some enemies patrol predictable paths while others wander irregularly.

Patrol behavior helps make environments feel inhabited.

---

# 5. Chase Behavior

When an enemy confirms the player's presence, it may enter a chase state.

During chase behavior:

- enemies move rapidly toward the player
- enemies attempt to close the distance
- enemies may navigate obstacles or pursue through multiple rooms

The duration and intensity of the chase depends on the creature type.

Some predators may pursue aggressively while others abandon pursuit after losing visual contact.

---

# 6. Attack Behavior

When an enemy reaches the player within attack range, it enters the attack state.

Attack behavior varies depending on the creature.

Common attack patterns include:

- melee strikes
- lunging attacks
- area based biological attacks
- projectile or spore based attacks

Attack animations should clearly indicate when an enemy is preparing to strike.

This allows players to react or attempt to evade.

---

# 7. Retreat Behavior

Not all creatures fight until death.

Some enemies may retreat under certain conditions.

Examples include:

- taking significant damage
- losing sight of the player
- encountering environmental hazards
- returning to a safe territory

Retreat behavior reinforces the idea that creatures are part of a living ecosystem rather than simple combat units.

---

# 8. Investigation Behavior

Enemies may investigate disturbances even when they have not fully detected the player.

Triggers for investigation include:

- unusual sounds
- environmental movement
- partial visual detection

During investigation:

- enemies move toward the disturbance
- enemies search the surrounding area
- enemies may briefly enter an alert state

If no threat is found, the enemy eventually returns to patrol behavior.

---

# 9. Group Behavior

Certain creatures may display group behavior.

Examples include:

- scavengers moving in clusters
- predators coordinating movement
- parasites spreading across environments

Group behavior increases encounter complexity and reinforces ecological realism.

---

# 10. Environmental Interaction

Enemies should interact with the environment in believable ways.

Examples include:

- navigating through structures
- climbing walls or ceilings
- moving through biological growth areas
- disturbing objects while moving

These interactions make creatures feel physically present in the world.

---

# 11. AI State Flow

Enemy AI behavior typically follows a state flow.

Idle / Patrol  
↓  
Suspicious / Investigation  
↓  
Detection  
↓  
Chase  
↓  
Attack  
↓  
Retreat or Return to Patrol

This structure ensures that encounters develop gradually rather than instantly escalating to combat.

---

# 12. Integration with Other Systems

The Enemy AI System interacts with several gameplay systems.

Examples include:

- Stealth System for detection mechanics
- Combat System for attack interactions
- Audio Gameplay System for sound detection
- Level Design for patrol paths and encounter spaces

These integrations allow enemy behavior to respond dynamically to the environment and player actions.

---

# 13. Purpose of This Document

This document defines the behavioral structure of enemy AI in ROT.

By designing enemies as ecological organisms rather than scripted opponents, the game maintains a believable and unsettling ecosystem.

These AI rules ensure that encounters remain tense, readable, and consistent with the biological horror identity of the Rot universe.

---

## Related Documents

ai_state_machine.md
ai_perception_system.md
enemy_design_document.md
combat_system.md
stealth_system.md

---