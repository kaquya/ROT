# Player Statistics

This document defines the **baseline player attributes** used throughout ROT.

These statistics determine how the player interacts with:

- enemies
- movement systems
- combat mechanics
- inventory management
- environmental hazards

The values defined here represent **prototype balancing targets**.

These values will be adjusted during testing and gameplay tuning.

---

# Player Design Philosophy

The player character in ROT is **not a super soldier**.

The player is vulnerable and must rely on:

- careful movement
- limited resources
- tactical decision making

Key principles:

• enemies are dangerous  
• mistakes have consequences  
• survival requires planning  
• combat is risky  

These principles help maintain the tension typical of survival horror games.

---

# Core Player Attributes

The player character has several primary attributes.

These attributes define survivability and movement capabilities.

---

## Health

Health represents the player's physical condition.

When health reaches zero, the player dies.

### Base Value

Health: 100

### Health Recovery

Health can be restored using healing items such as:

- bandages
- medical kits
- special treatments

Healing items restore a percentage or fixed amount of health.

---

## Stamina

Stamina represents the player's physical endurance.

Stamina is consumed by actions such as:

- sprinting
- climbing
- heavy melee attacks

### Base Value

Stamina: 100

### Stamina Recovery

Stamina regenerates slowly when the player is not performing exhausting actions.

Low stamina prevents sprinting until recovery occurs.

---

# Movement Statistics

Movement statistics define how the player moves through the environment.

Movement speed influences both exploration and combat survival.

---

## Walking Speed

Default movement speed.

Value:

Walk Speed: 3.0 m/s

---

## Sprint Speed

Used for rapid movement and escaping enemies.

Value:

Sprint Speed: 6.0 m/s

Sprint consumes stamina.

---

## Crouch Speed

Used for stealth movement.

Value:

Crouch Speed: 1.5 m/s

Crouching reduces noise and visibility.

---

## Backward Movement

Moving backward while aiming is slower.

Value:

Backpedal Speed: 2.0 m/s

This prevents players from easily kiting enemies.

---

# Combat Statistics

Combat statistics determine the player's effectiveness during combat.

---

## Melee Damage

Basic melee attacks deal limited damage.

Value:

Base Melee Damage: 15

Melee combat is risky and intended primarily for emergencies.

---

## Critical Hit Multiplier

Weak point attacks deal increased damage.

Example weak points:

- head
- exposed Rot growth

Value:

Critical Damage Multiplier: 2.0x

---

## Aim Stability

Aim stability affects weapon sway while aiming.

Value:

Aim Stability: Medium

Aim stability improves when the player is standing still.

---

# Inventory Capacity

Inventory space is intentionally limited.

Players must carefully decide which items to carry.

---

## Inventory Slots

Base inventory size:

Inventory Slots: 12

Each item occupies one slot unless stackable.

---

## Weapon Carry Limit

Players can carry a limited number of weapons.

Value:

Maximum Equipped Weapons: 3

Example loadout:

- handgun
- shotgun
- melee weapon

---

## Item Stack Limits

Certain items can stack in the same inventory slot.

Example stack limits:

Handgun Ammo: 30  
Shotgun Shells: 10  
Rifle Ammo: 10  
Bandages: 3  
Crafting Materials: 5  

Key items do not stack.

---

# Interaction Statistics

Interaction statistics affect how the player interacts with the environment.

---

## Interaction Range

Defines the maximum distance for interacting with objects.

Value:

Interaction Range: 1.5 meters

---

## Pickup Speed

Defines how quickly the player can collect items.

Pickup actions should be nearly instant to maintain gameplay flow.

---

# Stealth Statistics

Stealth mechanics depend on player movement and visibility.

---

## Noise Generation

Movement generates noise detectable by enemies.

Noise levels:

Walking: Low  
Sprinting: High  
Crouching: Very Low  

---

## Visibility

Player visibility is affected by:

- lighting
- movement speed
- enemy distance

Crouching reduces visibility.

Dark environments improve stealth effectiveness.

---

# Environmental Resistance

Certain environments contain hazards.

Examples:

- toxic gas
- contaminated water
- electrical hazards

Environmental resistance values determine how quickly the player takes damage from hazards.

Base resistance is low, encouraging players to avoid dangerous areas.

---

# Difficulty Scaling

Player statistics may vary depending on difficulty level.

Example adjustments:

Easy Mode

- increased health
- slightly increased stamina regeneration
- more forgiving enemy damage

Hard Mode

- reduced healing effectiveness
- increased enemy damage
- more aggressive enemy behavior

Difficulty adjustments preserve the core gameplay experience while changing survival pressure.

---

# Balancing Notes

The statistics defined in this document are **initial prototype values**.

Balancing will be refined during:

- combat testing
- AI encounter tuning
- playtesting sessions

The goal is to maintain a consistent level of tension while ensuring fair gameplay.

The player should always feel **vulnerable but capable of survival through careful decision making**.

---