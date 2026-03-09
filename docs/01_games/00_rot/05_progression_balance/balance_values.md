# Balance Values

Project: ROT

Version: 1.1

Document Type: Balance Reference

Category: Gameplay Balance

Scope: Player, Enemies, Resources

Status: Early Tuning Reference

---

# 1. Overview

This document defines the baseline numerical values used for balancing gameplay systems in ROT.

While other documents describe the design philosophy of progression and difficulty, this file provides the **initial numerical values used during development and testing**.

These values serve as **starting points for iteration** and will likely change during playtesting and balancing phases.

Systems covered include:

- player attributes
- enemy attributes
- stamina costs
- Rot contamination values
- resource distribution

All values should remain **consistent with the survival horror design philosophy of the game**.

---

# 2. Player Attributes

The player’s survivability is intentionally limited to reinforce survival tension.

| Attribute | Base Value | Notes |
| --- | --- | --- |
| Health | 100 | Maximum player health |
| Stamina | 100 | Used for sprinting and combat |
| Rot Tolerance | 50 | Maximum safe contamination level |
| Inventory Slots | 12 | Base carrying capacity |
| Movement Speed | 4.5 m/s | Default walking speed |
| Sprint Speed | 6.5 m/s | Sprinting movement |

---

# 3. Stamina Costs

Stamina is consumed by movement and combat actions.

| Action | Stamina Cost |
| --- | --- |
| Sprinting | 10 per second |
| Melee Attack | 15 |
| Heavy Attack | 30 |
| Dodge / Quick Movement | 20 |
| Climbing / Traversal | 10 |

Stamina regeneration begins **1.5 seconds after the last stamina-consuming action**.

Stamina regeneration rate:

```
20 stamina per second
```

---

# 4. Rot Exposure

Rot exposure measures the player’s contamination level when entering infected areas.

| Condition | Exposure Rate |
| --- | --- |
| Low contamination area | +1 per second |
| Moderate contamination | +3 per second |
| High contamination zone | +6 per second |
| Convergence zone | +10 per second |

Contamination thresholds:

| Level | Effect |
| --- | --- |
| 0–20 | Safe |
| 20–40 | Minor visual effects |
| 40–50 | Severe contamination effects |
| 50+ | Critical mutation risk |

Exposure slowly decreases when leaving contaminated environments.

Decay rate:

```
2 per second in safe areas
```

---

# 5. Player Damage Values

Basic combat damage values.

| Weapon Type | Damage |
| --- | --- |
| Light Melee | 20 |
| Heavy Melee | 40 |
| Improvised Weapon | 15 |
| Firearm (if implemented) | 50 |

These values ensure most enemies cannot be defeated without careful resource management.

---

# 6. Enemy Base Attributes

Enemy difficulty increases as the player progresses through districts.

### Rotter (Basic Enemy)

| Attribute | Value |
| --- | --- |
| Health | 40 |
| Attack Damage | 10 |
| Movement Speed | 3.8 m/s |
| Detection Range | 12 m |

---

### Collapsed Rotter

| Attribute | Value |
| --- | --- |
| Health | 70 |
| Attack Damage | 18 |
| Movement Speed | 4.2 m/s |
| Detection Range | 14 m |

Collapsed Rotters are more aggressive and attack in confined spaces.

---

### Stalker Variant

| Attribute | Value |
| --- | --- |
| Health | 60 |
| Attack Damage | 15 |
| Movement Speed | 5.0 m/s |
| Detection Range | 18 m |

Stalkers rely on stealth and ambush behavior.

---

# 7. Enemy Damage Against Player

Enemy attacks should remain dangerous but survivable.

| Enemy Type | Damage |
| --- | --- |
| Rotter | 10 |
| Collapsed Rotter | 18 |
| Stalker | 15 |
| Boss Attacks | 30–50 |

Two or three enemy hits should be enough to seriously threaten the player.

---

# 8. Healing Items

Healing items restore limited health.

| Item | Effect |
| --- | --- |
| Basic Medical Kit | +40 health |
| Emergency Injection | +25 health |
| Full Recovery Kit | +100 health |

Healing items are intentionally scarce.

---

# 9. Crafting Resources

Crafting resources are distributed across the world.

Example resource categories:

| Resource | Usage |
| --- | --- |
| Scrap Metal | crafting tools |
| Chemical Compounds | healing items |
| Organic Samples | Rot research items |
| Fabric | crafting supplies |

Crafting recipes should require **multiple components** to prevent excessive crafting.

---

# 10. Resource Distribution

Resource availability is intentionally limited.

Example resource density:

| Area Type | Resource Frequency |
| --- | --- |
| Residential | Medium |
| Downtown | Medium |
| Harbor | Low |
| Hospital | Medium |
| Forest | Low |
| Research Facility | Rare |

Players should feel pressure to manage resources carefully.

---

# 11. Difficulty Scaling

Enemy difficulty increases across districts.

Example scaling:

| Stage | Enemy Health | Enemy Damage |
| --- | --- | --- |
| Early Game | 100% | 100% |
| Mid Game | 120% | 115% |
| Late Game | 150% | 130% |

This scaling helps maintain tension throughout the game.

---

# 12. Balancing Philosophy

Balance in ROT should support survival horror gameplay.

Key principles include:

### Limited Resources

Players should never feel overpowered.

---

### Dangerous Combat

Enemies should pose a real threat.

---

### Exploration Rewards

Players who explore thoroughly should find additional resources.

---

### Gradual Difficulty Increase

Enemy strength and environmental danger increase as the player approaches the center of the Rot outbreak.

---

# 13. Future Adjustments

These values represent early balance targets.

During development the values will be refined through:

- internal playtesting
- difficulty analysis
- encounter tuning
- player feedback

Balancing should remain flexible throughout development.

---

## Related Documents

[Player Stats](./player_stats.md)   
[Enemy Stats](./enemy_stats.md)   
[Difficulty Balance](./difficulty_balance.md)   
[Resource Economy](./resource_economy.md)   
[Weapons and Items](./weapons_items.md)   
[Combat System](../02_core_systems/combat_system.md)  
[Rot Exposure System](../02_core_systems/rot_exposure_system.md)  

---