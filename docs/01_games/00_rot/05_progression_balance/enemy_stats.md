# Enemy Stats

Project: ROT  
Version: 1.1  
Document Type: Gameplay System  
Category: Progression & Balance  
Scope: ROT (Game)  
Status: Core Reference

---

# 1. Overview

This document defines the core statistical attributes used to balance enemies in ROT.

Enemy statistics determine how dangerous a creature is, how it behaves during encounters, and how it interacts with player systems such as combat, stealth, and Rot exposure.

While enemy behavior and abilities are defined in the **Enemy AI System** and **Enemy Design Documents**, this file focuses specifically on the numerical attributes used for balancing.

Enemy stats ensure that encounters remain challenging, fair, and consistent across different stages of the game.

---

# 2. Enemy Stat Design Philosophy

Enemy statistics should support the survival horror identity of ROT.

Enemies are not simply damage targets. They represent biological threats within an evolving ecosystem.

Stat design follows several guiding principles.

### Threat Diversity

Different enemies should feel dangerous in different ways.

Examples include:

- high health enemies that require sustained combat  
- fast enemies that pressure player movement  
- stealth predators that ambush from hidden locations  

Stat differences reinforce these roles.

---

### Escalating Difficulty

Enemy strength gradually increases as the player progresses deeper into Rot-corrupted areas.

Later enemies may have:

- higher health
- stronger attacks
- faster movement
- more complex behaviors

This escalation reflects the evolution of the Rot ecosystem.

---

### Ecological Role

Enemy stats should reflect the biological role of the organism.

For example:

- scavengers are weaker but appear in groups  
- predators are stronger and more aggressive  
- apex mutations are extremely dangerous but rare

---

# 3. Core Enemy Attributes

All enemies share a set of core statistical attributes used for balancing.

---

## Health

Health represents how much damage an enemy can sustain before dying.

Higher health enemies require more resources to defeat.

Health values vary widely depending on enemy type.

Examples:

- small scavengers have low health  
- predators have moderate health  
- bosses and apex mutations have very high health

---

## Attack Damage

Attack damage determines how much health the player loses when hit by an enemy.

Damage values should scale with the enemy’s threat level.

Examples:

- weak enemies deal minor damage  
- aggressive predators deal moderate damage  
- large mutations deal severe damage

Some enemies may also apply additional effects such as contamination.

---

## Movement Speed

Movement speed determines how quickly enemies move through the environment.

Speed strongly affects encounter difficulty.

Examples:

- scavengers may move quickly in groups  
- predators may sprint during chase phases  
- large mutations may move slowly but powerfully

Movement speed also affects how easily players can escape encounters.

---

## Detection Range

Detection range defines how easily enemies detect the player.

This value influences both:

- vision detection distance  
- sound detection sensitivity

Enemies with high detection range can identify the player from farther away.

This stat interacts directly with the **AI Perception System**.

---

## Attack Range

Attack range determines the distance at which an enemy can damage the player.

Examples include:

- melee strikes  
- lunging attacks  
- projectile attacks  
- biological area attacks

Attack range affects how players must position themselves during combat.

---

# 4. Secondary Enemy Attributes

Some enemies may include additional attributes depending on their biological design.

---

## Stagger Resistance

Stagger resistance determines how easily an enemy is interrupted by player attacks.

Low resistance enemies may stagger frequently, while stronger enemies continue attacking even when damaged.

---

## Armor

Certain enemies may possess biological armor.

Armor reduces incoming damage and forces players to target weak points.

Examples include:

- hardened Rot shells  
- thick bone growth structures  
- layered biomass protection

---

## Rot Contamination Output

Some enemies emit Rot contamination during combat.

This may occur through:

- spore attacks  
- toxic biological fluids  
- proximity to Rot biomass

These enemies contribute to the **Rot Exposure System**.

---

# 5. Enemy Scaling

Enemy stats increase as the player progresses through the game world.

Scaling occurs through several methods.

### Regional Scaling

Enemies found in later districts are generally stronger than those in earlier areas.

### Variant Enemies

Some enemy types may have stronger variants that appear later in the game.

### Boss Creatures

Boss enemies possess significantly higher stats and unique mechanics.

---

# 6. Encounter Balance

Enemy statistics must support encounter design.

Encounters should feel tense but manageable.

Balancing factors include:

- enemy health relative to player damage output  
- number of enemies in encounters  
- environmental hazards  
- available player resources

Enemy stats should never force unavoidable damage.

Players should always have options such as:

- stealth avoidance  
- retreat  
- environmental advantage

---

# 7. Integration with Other Systems

Enemy statistics interact with several gameplay systems.

Examples include:

- **Combat System** for damage calculation  
- **Enemy AI System** for behavior patterns  
- **AI Perception System** for detection mechanics  
- **Rot Exposure System** for contamination effects  

Balancing enemy attributes requires coordination with these systems.

---

# 8. Purpose of This Document

This document defines the statistical framework used to balance enemy threats in ROT.

By controlling enemy health, damage, detection ability, and environmental effects, the game ensures that encounters remain tense and unpredictable.

Enemy stats support the broader goal of portraying the Rot ecosystem as a dangerous and evolving biological environment.

---

## Related Documents

enemy_design_document.md
enemy_ai_system.md
combat_system.md
difficulty_balance.md

---