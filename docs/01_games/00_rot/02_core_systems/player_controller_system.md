# Player Controller System

Project: ROT  
Version: 1.1  
Document Type: Gameplay System  
Category: Player Systems  
Scope: ROT (Game)  
Status: Core Reference  

---

## 1. Overview

The Player Controller System defines how the player moves and physically interacts with the environment.

Movement in ROT should feel grounded, responsive, and consistent with the survival horror tone of the game. Players are not highly agile action heroes. Movement should communicate weight, vulnerability, and physical effort.

Traversal is designed to support exploration while maintaining tension. Players should always feel aware of their surroundings when navigating environments affected by the Rot.

---

## 2. Movement

Basic movement allows the player to walk through environments while exploring buildings, streets, and natural terrain.

Movement should feel deliberate and controlled rather than fast or exaggerated.

Key characteristics of player movement include:

- moderate walking speed
- slight inertia when starting or stopping
- responsive directional control
- clear visual feedback from animations

Movement should support careful observation of the environment while maintaining immersion.

---

## 3. Sprinting

Sprinting allows the player to temporarily increase movement speed in order to escape danger or move quickly through safe areas.

However, sprinting should come with limitations to maintain survival tension.

### Sprint Behavior

- sprinting increases player movement speed
- sprinting consumes stamina
- sprinting produces louder movement noise
- sprinting reduces the player's ability to react quickly to threats

Players should not be able to sprint indefinitely.

### Design Purpose

Sprinting introduces a risk decision.

Players must choose when it is worth using stamina and potentially attracting attention in order to escape a dangerous situation.

---

## 4. Crouching

Crouching allows the player to move more quietly and remain less visible to enemies.

This mechanic supports stealth gameplay and careful navigation of dangerous areas.

### Crouch Behavior

- crouched movement is slower than walking
- crouched movement produces less noise
- crouching lowers the player's profile behind objects
- crouching improves stealth effectiveness

Crouching should feel deliberate and controlled, encouraging players to move carefully through hostile environments.

---

## 5. Climbing

Climbing allows players to traverse certain environmental obstacles and reach elevated areas.

Climbing is used to support exploration and environmental navigation.

Examples of climbable objects include:

- ladders
- short ledges
- broken structures
- maintenance access points

Climbing actions should be clearly readable and supported by environmental cues so players understand where traversal is possible.

---

## 6. Traversal Behavior

Traversal refers to how the player moves through the environment beyond basic walking.

Traversal systems should encourage exploration while maintaining immersion.

Traversal elements may include:

- stepping over small obstacles
- navigating narrow passages
- moving through damaged buildings
- crossing unstable terrain

Traversal actions should feel grounded in the physical world of the game.

---

## 7. Environmental Interaction

Movement should naturally integrate with the environment.

Examples include:

- pushing open doors
- stepping through debris
- moving around environmental hazards
- navigating tight interior spaces

These interactions help reinforce the sense that the player is physically present within the environment.

---

## 8. Movement Limitations

Movement should reflect the vulnerability of the player.

The player is not capable of extreme agility or unrealistic movement.

Examples of limitations include:

- no exaggerated jumping mechanics
- limited climbing ability
- restricted stamina for sprinting
- slower movement in hazardous environments

These limitations reinforce the survival horror atmosphere.

---

## 9. Integration with Other Systems

The Player Controller System interacts with several other gameplay systems.

Examples include:

- stealth system, where movement noise affects enemy detection
- stamina systems affecting sprint duration
- environmental hazards that restrict movement
- combat systems that influence player positioning

These interactions ensure that movement is an important part of survival decision making.

---

## 10. Purpose of This Document

This document defines the movement and traversal rules for the player in ROT.

By establishing consistent movement behavior, the Player Controller System ensures that exploration, stealth, and survival mechanics work together to support the overall gameplay experience.

---