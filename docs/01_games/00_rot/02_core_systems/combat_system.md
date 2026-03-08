# Combat System

Project: ROT  
Version: 1.1  
Document Type: Gameplay System  
Category: Combat  
Scope: ROT (Game)  
Status: Core Reference  

---

## 1. Overview

The Combat System defines how the player can defend themselves against hostile organisms within the Rot ecosystem.

Combat in ROT is designed to support the survival horror experience rather than dominate it. Encounters should feel dangerous and resource intensive. Players are capable of fighting, but combat is rarely the safest option.

The combat system emphasizes careful decision making, limited resources, and positioning within the environment.

Combat interactions are influenced by several elements:

- weapon availability
- stamina management
- enemy behavior
- environmental positioning

Players must choose carefully when to fight, when to retreat, and when to avoid conflict entirely.

---

## 2. Combat Philosophy

Combat in ROT follows several core design principles.

### Vulnerability

Players should never feel completely safe during combat. Enemies are dangerous and mistakes can quickly lead to defeat.

### Resource Cost

Every combat encounter consumes resources such as ammunition, stamina, or healing items. Players must consider whether the cost of combat is worth the outcome.

### Environmental Awareness

Combat takes place within complex environments. Players should use terrain, obstacles, and positioning to improve their chances of survival.

### Tactical Decision Making

Players must constantly decide whether to fight, avoid, or escape encounters. Combat should never be the only solution.

---

## 3. Weapon Usage

Weapons allow the player to defend themselves against Rot organisms.

Weapons are divided into two general categories.

### Melee Weapons

Melee weapons are used for close range combat.

Characteristics of melee weapons include:

- limited attack range
- moderate stamina cost
- no ammunition requirement
- higher personal risk during combat

Melee combat is often used when ammunition is scarce or when enemies are weak enough to approach safely.

---

### Ranged Weapons

Ranged weapons allow players to attack enemies from a distance.

Characteristics of ranged weapons include:

- limited ammunition
- higher precision requirements
- safer engagement distance
- louder noise that may attract additional threats

Ranged combat provides a safer option but introduces resource management challenges.

---

## 4. Attack Mechanics

Attacks are the primary method of dealing damage to enemies.

### Melee Attacks

Melee attacks are performed with close range weapons.

Melee attacks should feel physical and deliberate.

Typical behavior includes:

- attack wind up before impact
- short recovery time after attack
- stamina consumption per strike

Players must carefully time melee attacks to avoid being exposed to enemy counter attacks.

---

### Ranged Attacks

Ranged attacks are performed using firearms or projectile weapons.

These attacks require the player to aim before firing.

Key elements include:

- aiming control
- projectile or hit scan firing
- ammunition consumption
- recoil or firing delay

Ranged attacks should reward precision but remain limited by ammunition availability.

---

## 5. Hit Detection

Hit detection determines when attacks successfully strike a target.

The system should be reliable and readable to the player.

### Melee Hit Detection

Melee attacks use short range collision detection to determine whether a strike connects with an enemy.

Successful hits should provide clear visual and audio feedback.

---

### Ranged Hit Detection

Ranged attacks use either projectile simulation or hit scan detection.

When a projectile or ray intersects an enemy's hitbox, damage is applied.

Visual feedback such as impact effects or enemy reactions helps communicate successful hits.

---

## 6. Stamina Interaction

Stamina plays an important role in combat.

Physical actions performed during combat consume stamina.

These actions may include:

- melee attacks
- sprinting during combat
- evasive movement
- defensive positioning

If stamina becomes depleted, the player's ability to perform combat actions becomes limited.

This system encourages players to pace their actions and avoid reckless aggression.

---

## 7. Enemy Reaction

Enemies respond to player attacks in ways that reinforce the physical nature of combat.

Examples include:

- stagger reactions when struck
- temporary interruption of enemy actions
- behavioral changes after being damaged

Enemy reactions provide feedback that helps players understand the effectiveness of their attacks.

---

## 8. Combat Risk

Combat situations should always carry risk.

Enemies may:

- attack in groups
- close distance quickly
- retaliate immediately after being struck

Players who engage enemies without preparation may quickly become overwhelmed.

The safest approach is often avoidance or careful positioning.

---

## 9. Integration with Other Systems

The Combat System interacts with several other gameplay systems.

Examples include:

- the stealth system, where players may avoid combat entirely
- the inventory system, which manages weapon and ammunition availability
- the stamina system, which limits physical actions
- the enemy AI system, which determines enemy combat behavior

These interactions ensure that combat is integrated with the overall gameplay experience.

---

## 10. Purpose of This Document

This document defines how combat functions in ROT.

It establishes the rules for weapon usage, attack mechanics, hit detection, and stamina interaction.

By following these principles, combat encounters remain tense, resource driven, and consistent with the survival horror identity of the game.

---

## Related Documents

systems_overview.md
combat_system.md
stealth_system.md
interaction_system.md
player_stats.md
input_system.md

---