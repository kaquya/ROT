# Enemy Pipeline

# 1. Overview

The Enemy Pipeline defines the complete process used to design, create, implement, and balance enemies in ROT.

Enemies are one of the most complex systems in the game because they involve multiple disciplines:

- design
- art
- animation
- AI programming
- gameplay balance
- audio design

This pipeline ensures that every enemy is created using a consistent and predictable workflow.

For a solo-developed project, this structure is essential to prevent production chaos.

The pipeline covers:

Concept → Design → Modeling → Animation → Implementation → AI Integration → Gameplay Testing.

---

# 2. Enemy Creation Workflow

All enemies follow the same production workflow.

Enemy Concept
↓
Gameplay Design
↓
Creature Modeling
↓
Rigging
↓
Animation Creation
↓
Engine Integration
↓
AI Behavior Implementation
↓
Combat Balancing
↓
Audio Integration
↓
Final Testing

Skipping steps can cause major technical issues later in development.

---

# 3. Enemy Categories

Enemies are organized into several categories.

Each category follows different design rules.

## Rotters

Basic infected enemies.

Characteristics:

- former humans
- slow movement
- limited awareness
- attack in groups

Rotters form the majority of encounters.

---

## Stalkers

Advanced infected predators.

Characteristics:

- stealth movement
- ambush attacks
- intelligent hunting behavior

Stalkers increase tension during exploration.

---

## Spliced

Large mutated infected hosts.

Characteristics:

- fused biological structures
- increased durability
- powerful attacks

Spliced enemies often act as elite encounters.

---

## Wildlife

Animals infected by the Rot.

Examples include:

- Rot Wolves
- Rot Stag
- infected birds

Wildlife enemies behave differently from humanoid enemies.

---

## Boss Creatures

Large, unique enemies with multi-phase encounters.

Bosses are major gameplay events and require custom mechanics.

---

# 4. Enemy Concept Phase

Enemy design begins with conceptual development.

This stage defines:

- enemy appearance
- biological structure
- infection stage
- behavior type
- gameplay role

Concept design must answer several questions:

What threat does this enemy represent?

How does it attack?

How fast is it?

Does it hunt alone or in groups?

Concept sketches should emphasize silhouettes.

Enemies must be recognizable at a distance.

---

# 5. Gameplay Role Definition

Each enemy must serve a gameplay purpose.

Example roles include:

Pressure Enemy  
Forces player movement.

Ambush Enemy  
Attacks unexpectedly.

Tank Enemy  
Absorbs large amounts of damage.

Disruption Enemy  
Interrupts player actions.

Boss Enemy  
Creates large-scale encounters.

Defining enemy roles helps maintain combat variety.

---

# 6. Creature Modeling

After concept approval, enemies move to the modeling stage.

Modeling must follow several rules.

Polygon counts must remain reasonable.

Example targets:

Basic enemies  
10k–20k polygons

Elite enemies  
20k–35k polygons

Boss creatures  
40k–70k polygons

Models must prioritize silhouette and readability.

Overly complex geometry should be avoided.

---

# 7. Rot Mutation Design

Rot infection dramatically alters enemy anatomy.

Mutation characteristics may include:

elongated limbs  
distorted bone structures  
organic growths  
spiral Rot patterns

Mutations should feel organic rather than random.

Enemy shapes should remain readable during combat.

---

# 8. Rigging

Enemies must be rigged for animation.

Rigging must support the enemy's movement style.

Examples:

Humanoid rig  
Used for Rotters.

Quadruped rig  
Used for Rot Wolves.

Custom rigs  
Used for large boss creatures.

Rigging should support all planned animations.

---

# 9. Animation Requirements

Every enemy must include a core animation set.

Basic animation set:

Idle  
Walk  
Run  
Attack  
Damage reaction  
Death

More advanced enemies require additional animations.

Examples:

Ambush animation  
Climbing animation  
Leap attack  
Special ability animation

Animation timing must align with gameplay mechanics.

---

# 10. Engine Integration

After modeling and animation, enemies are imported into the engine.

Integration tasks include:

Importing model  
Importing animations  
Assigning materials  
Setting up animation controller

Enemy prefabs must be created for each enemy type.

Prefab structure:

EnemyPrefab
{
Model
Animator
Collider
HealthComponent
AIController
AudioEmitter
}

This structure ensures consistent enemy behavior across the game.

---

# 11. AI Behavior Integration

Once the enemy model and animations are integrated into the engine, AI behavior must be implemented.

AI behavior controls how enemies:

- detect the player
- navigate the environment
- attack
- react to damage
- disengage or retreat

Each enemy is controlled by an **AI State Machine**.

Typical states include:

Idle  
Patrol  
Suspicious  
Search  
Chase  
Attack  
Stunned  
Dead

These states allow enemies to react dynamically to player actions.

AI behaviors should remain readable and predictable enough for players to understand enemy patterns.

---

# 12. Enemy Navigation

Enemies must be able to navigate environments correctly.

Navigation relies on the engine's navigation system.

Requirements:

Enemies must avoid obstacles  
Enemies must not walk through walls  
Enemies must be able to navigate stairs and slopes

Navigation meshes should be generated for all playable areas.

Some enemies may have special navigation abilities.

Examples:

Stalkers may climb surfaces  
Wildlife may traverse terrain more easily

These special movement behaviors require additional navigation logic.

---

# 13. Enemy Spawn System

Enemies are placed in environments using spawn systems.

Spawn systems control:

Enemy location  
Enemy type  
Spawn conditions  
Maximum active enemies

Enemy spawn placement should follow gameplay design rules.

Enemies should not spawn directly in front of the player unless scripted.

Spawn points may be:

Static spawn points  
Dynamic spawn triggers  
Scripted encounter spawns

Spawn systems must prevent overwhelming the player.

---

# 14. Enemy Combat Integration

Enemy combat behavior must integrate with the Combat System.

Key combat parameters include:

Enemy health  
Damage output  
Attack speed  
Attack range  
Stagger reactions

Enemy attacks must be clearly telegraphed.

Players should be able to recognize attack animations before damage occurs.

Attack telegraphing improves fairness and gameplay clarity.

---

# 15. Weak Point Design

Some enemies include weak points that increase damage when targeted.

Examples include:

Exposed Rot growths  
Head shots  
Unprotected limbs

Weak points reward precision and encourage strategic combat.

Weak point design must remain visually clear.

---

# 16. Enemy Audio Integration

Enemies require audio feedback to communicate behavior.

Enemy audio includes:

Idle sounds  
Movement sounds  
Attack sounds  
Damage reactions  
Death sounds

Audio helps players identify enemy locations and threat levels.

Stalkers may produce subtle sounds to increase tension.

Large enemies may produce heavier footsteps or breathing sounds.

---

# 17. Enemy Visual Feedback

Enemies must provide visual feedback during combat.

Examples include:

Damage reactions  
Stagger animations  
Blood or Rot particle effects  
Weak point exposure

Visual feedback informs the player that their attacks are effective.

Enemies should never feel unresponsive to damage.

---

# 18. Enemy Performance Optimization

Enemies can become performance-heavy if many are active.

Optimization strategies include:

Distance-based AI updates  
Reduced animation updates for distant enemies  
Simplified physics for inactive enemies  
Object pooling for enemy corpses

Example:

Enemy distance > 50m
AI updates reduced

These optimizations reduce CPU load.

---

# 19. Enemy Difficulty Scaling

Enemy difficulty may change depending on game difficulty settings.

Parameters that may change include:

Enemy health  
Enemy damage  
Enemy aggression  
Enemy detection range

Difficulty adjustments should increase tension without creating unfair encounters.

---

# 20. Enemy Testing

Every enemy must undergo gameplay testing.

Testing includes:

Combat balance  
AI behavior correctness  
Animation timing  
Navigation reliability

Enemies must behave consistently in all environments.

Testing should also evaluate how enemies interact with puzzles and level design.

---

# 21. Enemy Encounter Design

Enemies should rarely appear randomly.

Encounters must be intentionally designed.

Encounter design considers:

Enemy placement  
environment layout  
available player resources  
escape routes

Good encounter design creates tension without overwhelming the player.

---

# 22. Enemy Debug Tools

Development builds should include debugging tools.

Examples include:

Enemy AI state viewer  
Pathfinding visualization  
Enemy health display  
Detection radius visualization

These tools help diagnose enemy behavior issues during development.

---

# 23. Enemy Finalization

Before an enemy is considered complete, it must pass final validation.

Final validation includes:

AI behavior stability  
animation consistency  
combat balance  
audio integration  
performance testing

Once validated, the enemy becomes part of the final enemy roster for the game.

Future updates or expansions may introduce additional enemy variants.

---