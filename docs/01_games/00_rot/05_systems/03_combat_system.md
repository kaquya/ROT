# Combat System

## 1. System Overview

The Combat System governs all offensive and defensive player actions against hostile organisms in ROT.

Combat is designed to support the core survival horror experience by emphasizing:

- danger
- limited resources
- tactical decision making
- environmental awareness

Players are capable of defending themselves, but they are rarely strong enough to eliminate every enemy they encounter.

Because of this, combat is only one option available to the player.

The player may choose to:

- fight enemies
- evade encounters
- retreat
- use environmental hazards

The Combat System must support these choices without forcing constant combat.

---

## 2. Combat Design Philosophy

Combat in ROT follows several key principles.

### Resource Scarcity

Weapons and ammunition are intentionally limited.

Players should not feel comfortable engaging every enemy.

Ammunition conservation is a critical part of survival.

---

### Vulnerability

The player character is not a trained soldier.

Enemies can overwhelm the player if approached recklessly.

Combat encounters should always feel tense.

---

### Precision Over Volume

Combat rewards careful aiming and observation rather than excessive firing.

Enemy weak points encourage precision.

---

### Environmental Awareness

Players may use environmental hazards to defeat enemies without spending ammunition.

Examples include:

- explosive containers
- electrical hazards
- unstable machinery

These options reward situational awareness.

---

## 3. Combat States

The player can enter several combat-related states.

These states affect movement behavior, camera positioning, and animation.

---

### Exploration State

The default gameplay state.

Player movement and interaction occur normally.

Combat actions are not active.

---

### Aim State

Triggered when the player aims a weapon.

Changes include:

- reduced movement speed
- adjusted camera positioning
- weapon aiming animations

---

### Attack State

Triggered when the player fires a weapon or performs a melee attack.

During this state:

- attack animations play
- weapon effects trigger
- damage calculations occur

---

### Reload State

Triggered when the player reloads a firearm.

During reload:

- the player cannot fire the weapon
- reload animation plays
- ammunition is transferred from inventory

---

## 4. Weapon Categories

Weapons are divided into several general categories.

This document defines how each category behaves.

Specific weapons will be defined in content documentation.

---

### Handguns

Handguns are the most common firearm type.

Characteristics:

- moderate damage
- high accuracy
- relatively common ammunition
- moderate reload speed

Handguns serve as the player's primary defensive weapon.

---

### Shotguns

Shotguns are powerful close-range weapons.

Characteristics:

- high damage
- wide spread pattern
- slow reload speed
- limited ammunition

Shotguns are effective against larger enemies or groups.

---

### Rifles

Rifles are precision weapons designed for long-range combat.

Characteristics:

- very high damage
- high accuracy
- slow firing rate
- rare ammunition

Rifles are ideal for targeting enemy weak points.

---

### Melee Weapons

Melee weapons are used when enemies approach at close range.

Characteristics:

- no ammunition required
- limited range
- moderate damage
- risk of counterattack

Melee attacks can also be used to stagger enemies.

---

### Improvised Weapons

Improvised weapons may appear throughout the environment.

Examples include:

- pipes
- tools
- heavy objects

These weapons are generally weaker but useful in emergencies.

---

## 5. Weapon Handling

Weapon handling affects how quickly and accurately the player can attack.

Key factors include:

- recoil
- reload speed
- firing rate
- weapon sway

These factors vary depending on weapon category.

---

### Recoil

Recoil affects aim stability after firing.

Higher recoil weapons require players to re-adjust aim between shots.

---

### Reload Speed

Reload speed determines how quickly a weapon can fire again after its magazine is empty.

Some weapons may reload one round at a time.

---

### Weapon Sway

When aiming, the weapon may drift slightly due to player movement or fatigue.

This encourages careful shot timing.

---

## 6. Ammunition Usage

Firearms require ammunition stored in the Inventory System.

Each weapon type uses a specific ammunition category.

Examples include:

- handgun rounds
- shotgun shells
- rifle cartridges

When the player fires a weapon:

1. ammunition is removed from the inventory stack
2. weapon firing animation plays
3. projectile or hit detection occurs

If no ammunition is available, the weapon cannot fire.

---

## 7. Hit Detection

Combat relies on hit detection to determine whether an attack connects with a target.

Two primary detection methods are used.

---

### Hitscan Detection

Used for most firearms.

The game instantly determines whether a shot hits a target along the firing line.

Advantages include:

- precise hit detection
- efficient performance
- consistent results

---

### Collision Detection

Used for melee attacks.

The weapon's attack arc checks for collision with enemy hitboxes.

If a hit is detected, damage is applied.

---

## 8. Damage System

When a successful hit occurs, damage is applied to the target.

Damage calculations consider several factors.

These include:

- weapon damage value
- enemy defense
- weak point modifiers
- environmental modifiers

Final damage values are determined through balancing during development.

---

## 9. Weak Point System

Many enemies possess exposed biological structures that function as weak points.

Examples include:

- exposed Rot growth nodes
- mutated limbs
- unstable tissue structures

Targeting these areas increases damage significantly.

Weak points encourage players to observe enemy anatomy carefully before attacking.

---

## 10. Enemy Stagger

Certain attacks may temporarily stagger enemies.

Stagger effects interrupt enemy actions and create opportunities for escape or follow-up attacks.

Examples include:

- shotgun blasts at close range
- melee strikes to unstable limbs
- critical hits on weak points

Stagger duration varies by enemy type.

---

## 11. Environmental Combat

The Combat System supports interactions with environmental hazards that can damage enemies.

These hazards allow players to conserve ammunition and create tactical advantages.

Examples include:

Explosive Objects  
Containers such as fuel barrels may detonate when shot.

Electrical Hazards  
Damaged wiring or power systems may shock enemies when activated.

Mechanical Hazards  
Heavy machinery or collapsing structures may damage nearby enemies.

Environmental combat is triggered through the Interaction System or by weapon fire.

These hazards should provide strong feedback to the player through visual and audio cues.

---

## 12. Enemy Pressure

Combat encounters are designed to create pressure rather than large-scale battles.

Typical encounters include:

- one to three enemies in confined spaces
- a single elite enemy guarding a key area
- ambush predators in dark environments

Enemy pressure increases as the player progresses deeper into infected zones.

Encounters should remain tense but manageable.

---

## 13. Player Damage and Health

The player has a limited health pool.

Damage may occur from:

- enemy attacks
- environmental hazards
- boss encounters

Health is restored using healing items stored in the Inventory System.

Examples include:

- bandages
- medical injections
- chemical stabilizers

If the player’s health reaches zero, the character dies and the Save System reloads the most recent save point.

---

## 14. Damage Feedback

When the player takes damage, the system should provide clear feedback.

Examples include:

Visual Effects  
Screen distortion, blood splatter, or damage indicators.

Audio Feedback  
Pain sounds or impact audio.

Animation Response  
The character briefly reacts to damage.

These cues help players understand when they are in danger.

---

## 15. Combat Difficulty Scaling

Combat difficulty may vary depending on the selected difficulty level.

Higher difficulties may include:

- reduced ammunition availability
- increased enemy damage
- faster enemy reaction times

Lower difficulties may include:

- increased resource availability
- reduced enemy aggression

Enemy mechanics remain consistent across difficulties to ensure fairness.

---

## 16. Animation Integration

The Combat System interacts closely with the Animation System.

Combat-related animations include:

- aiming weapons
- firing weapons
- reloading
- melee attacks
- damage reactions

Animations must remain synchronized with gameplay actions.

For example:

A weapon should not fire until the firing animation reaches the correct frame.

---

## 17. Audio Integration

Combat actions trigger audio events managed by the Audio System.

Examples include:

Weapon firing sounds  
Reload sounds  
Enemy impact sounds  
Environmental explosions

Audio cues help players understand the intensity and direction of combat encounters.

---

## 18. Edge Cases

The Combat System must handle unusual gameplay situations.

Examples include:

Player attempting to fire without ammunition  
Player attempting to reload without spare ammo  
Enemies leaving the attack range mid-animation  
Player firing during interaction sequences

These situations must resolve without breaking gameplay flow.

---

## 19. Debugging Tools

Development builds should include debugging tools for testing combat behavior.

Examples include:

Damage visualization  
Displays damage values applied to enemies.

Hitbox visualization  
Displays enemy collision areas and weak points.

Weapon stat overrides  
Allows developers to test different weapon parameters.

These tools assist with balancing and debugging.

---

## 20. System Dependencies

The Combat System interacts with several other gameplay systems.

Player Controller  
Processes combat input and player state.

Inventory System  
Manages ammunition and weapon equipment.

Enemy AI System  
Handles enemy behavior and reactions.

Animation System  
Controls combat-related animations.

Audio System  
Triggers combat sound effects.

UI System  
Displays ammunition counts and combat indicators.

---

## 21. Future Expansion

The Combat System is designed to support additional combat features in future updates.

Possible expansions include:

weapon modification systems  
advanced enemy weak point mechanics  
environmental trap systems  
specialized combat abilities

The modular architecture ensures new features can be added without redesigning the core system.

---