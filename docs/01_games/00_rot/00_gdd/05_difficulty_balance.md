# ROT – Difficulty Balance

Version: 1.0  
Status: Balancing Design

---

# 1. Purpose of This Document

This document defines the principles and systems for **difficulty scaling** in ROT. The goal is to ensure that the player's experience remains challenging yet fair across different difficulty levels.

Difficulty balance takes into account:

- **Enemy statistics** (Health, Damage, Speed)
- **Player capabilities** (Health, Stamina, Weapon Usage)
- **Combat pacing** (Enemy density, AI behavior)
- **Environmental factors** (Hazards, resource availability)

The ultimate aim is to maintain consistent tension and meaningful choices, regardless of the difficulty setting.

---

# 2. Difficulty Levels

ROT features multiple difficulty settings that scale the game experience from relatively accessible to highly challenging. These include:

- **Easy**  
- **Normal**  
- **Hard**  
- **Nightmare** (Unlockable, intended for expert players)

Each difficulty level affects:

- Enemy behavior (aggression, intelligence, evasion)
- Player health and stamina
- Enemy health and damage output
- Availability and distribution of resources

---

## 2.1. Easy Mode

**Target Audience:** Players who want to enjoy the narrative and exploration without excessive combat stress.

### Adjustments:

- **Player Health:** +25% health.
- **Player Stamina:** +20% stamina regeneration.
- **Enemy Health:** -20% health.
- **Enemy Damage:** -15% damage.
- **Enemy AI:** Reduced aggressiveness, slower reaction time.
- **Resources:** Increased frequency of health items and ammunition in the environment.
- **Combat Focus:** More forgiving mechanics. Combat encounters are less punishing.

**Result:** Easy Mode allows players to focus on story and exploration, making it a good choice for those who are new to survival horror or want a relaxed experience.

---

## 2.2. Normal Mode

**Target Audience:** Players who want a balanced challenge with moderate difficulty.

### Adjustments:

- **Player Health:** Standard health (no adjustments).
- **Player Stamina:** Standard stamina regeneration.
- **Enemy Health:** Standard health (baseline for enemies).
- **Enemy Damage:** Standard damage (no adjustments).
- **Enemy AI:** Standard aggression, normal reaction time.
- **Resources:** Normal frequency of health items and ammunition.
- **Combat Focus:** Balanced gameplay with moderate difficulty.

**Result:** Normal Mode represents the default experience, providing a fair challenge where the player needs to manage resources effectively without extreme combat difficulty.

---

## 2.3. Hard Mode

**Target Audience:** Experienced players seeking a more challenging experience with greater stakes.

### Adjustments:

- **Player Health:** -20% health.
- **Player Stamina:** -15% stamina regeneration.
- **Enemy Health:** +20% health.
- **Enemy Damage:** +30% damage.
- **Enemy AI:** Increased aggression, faster reaction times, and more intelligent combat strategies.
- **Resources:** Reduced availability of healing items and ammunition. Health items and crafting materials are scarcer.
- **Combat Focus:** Combat requires more tactical decision-making, and the player must rely heavily on stealth and resource management.

**Result:** Hard Mode offers a more intense challenge, making combat encounters more punishing. Players will need to be strategic in both combat and resource management.

---

## 2.4. Nightmare Mode

**Target Audience:** Expert players who want to face the toughest challenges with minimal room for error.

### Adjustments:

- **Player Health:** -40% health.
- **Player Stamina:** -30% stamina regeneration.
- **Enemy Health:** +40% health.
- **Enemy Damage:** +50% damage.
- **Enemy AI:** Maximum aggression, enemies will attack relentlessly and intelligently, making them highly dangerous.
- **Resources:** Very few healing items or ammunition. Crafting materials are rare.
- **Combat Focus:** Every encounter is lethal, requiring perfect timing and expert planning. Stealth and resource management are essential.

**Result:** Nightmare Mode offers the hardest challenge, where the player is forced to use every available tool to survive. Combat is brutal, and even the slightest mistake can lead to death.

---

# 3. Dynamic Difficulty Adjustment

While the game provides fixed difficulty settings, **dynamic difficulty adjustments (DDA)** are also implemented to maintain a smooth experience for players.

### Adjustments Based on:

- **Player Progression:** If a player consistently fails a specific encounter, the game may reduce enemy damage or increase resource availability for that segment. This ensures that players are not excessively punished for difficulty spikes.
- **In-Game Behavior:** If a player shows signs of struggling (e.g., dying multiple times in a row), the game may automatically make slight adjustments to make the encounter more manageable.
- **AI Behavior Modulation:** Some enemy behavior may be slightly toned down if the player is having difficulty surviving. For example, enemies may hesitate longer before attacking or miss certain attacks.

---

# 4. Resource Management & Economy

The resource economy is one of the key aspects of balancing the difficulty in ROT.

- **Easy Mode:** More abundant resources to ensure players feel empowered.
- **Normal Mode:** A balanced resource economy, encouraging smart management.
- **Hard Mode:** Resource scarcity forces players to be strategic in every encounter.
- **Nightmare Mode:** Resources are very limited, and the player must explore and scavenge for anything that could help.

---

# 5. Enemy Scaling

As players progress through the game, the enemies will scale in difficulty. The following methods are used to adjust enemy challenges:

- **Enemy Health Scaling:** As the player advances, enemies will become tougher and more resilient to damage.
- **Enemy Damage Scaling:** Higher-tier enemies deal more damage, forcing the player to consider their combat options carefully.
- **Enemy Spawn Density:** Certain areas will see more enemies appear as the player advances, increasing pressure during exploration and combat encounters.
- **Special Enemies:** Elite and boss-type enemies become more prominent as the player reaches later stages of the game.

---

# 6. Balancing Notes

These difficulty adjustments and balancing methods are **subject to change** during:

- **Playtesting sessions**
- **Combat feedback** from the community
- **Internal team reviews**

The aim is to maintain **fairness, challenge, and player agency** while ensuring that the game remains an enjoyable experience for all difficulty levels.

Balancing will continue throughout the development cycle to refine the player experience.

---