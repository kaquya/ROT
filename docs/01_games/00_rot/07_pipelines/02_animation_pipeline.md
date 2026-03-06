# Animation Pipeline

# 1. Overview

The Animation Pipeline defines the process used to create, import, and integrate animations in ROT.

Animation affects several core systems:

- player movement
- combat responsiveness
- enemy behavior
- environmental interactions
- cinematic sequences

Because ROT is a solo-developed project, the animation pipeline must prioritize:

- efficiency
- reuse of animation assets
- simple animation systems
- predictable integration with gameplay systems

This pipeline ensures animations remain consistent across the entire project.

---

# 2. Animation Production Workflow

All animations follow a standardized production workflow.

Animation Planning
↓
Rig Preparation
↓
Animation Creation
↓
Animation Export
↓
Engine Import
↓
Animation Controller Setup
↓
Gameplay Integration
↓
Testing and Adjustment

Skipping steps in this pipeline can cause animation errors and gameplay inconsistencies.

---

# 3. Animation Categories

Animations are divided into several categories.

Each category serves a specific gameplay function.

Player Animations

Used for player movement, combat, and interactions.

Enemy Animations

Used for enemy locomotion, attacks, and behaviors.

Environmental Animations

Used for objects such as doors, machinery, and environmental events.

Cinematic Animations

Used for scripted story sequences and cutscenes.

---

# 4. Rigging Standards

All animated characters must use properly constructed rigs.

Rigging ensures characters deform correctly during animation.

Rig requirements include:

Consistent bone hierarchy  
Correct joint orientation  
Proper skin weighting  
Stable root bone for movement

Character rigs must also support:

weapon holding  
attack animations  
damage reactions

---

# 5. Root Motion vs In-Place Animation

Two main animation approaches exist.

Root Motion

Movement is driven directly by the animation.

Example:

A lunge attack moves the enemy forward based on animation motion.

In-Place Animation

Movement is controlled by code while the animation plays in place.

Example:

Walking animations loop while the character moves via controller logic.

ROT primarily uses **in-place animation** for gameplay consistency.

Root motion may be used for specific attacks or cinematic moments.

---

# 6. Animation Naming Conventions

Animations must follow strict naming rules.

Format:

ANIM_[CharacterType]_[Action]

Examples:

ANIM_Player_Walk  
ANIM_Player_Run  
ANIM_Player_Attack  
ANIM_Rotter_Attack  
ANIM_Stalker_Ambush  
ANIM_Boss_Phase2_Attack

Consistent naming simplifies debugging and organization.

---

# 7. Animation Export Settings

Animations are created in external software such as Blender.

Export settings must follow strict guidelines.

Export format:

FBX

Export rules:

Apply transforms before export  
Bake animation into keyframes  
Ensure correct scale  
Include only required bones

Incorrect export settings can break animation playback.

---

# 8. Engine Animation Import

Once exported, animations are imported into the engine.

Import process includes:

assigning skeleton  
configuring animation loops  
setting root motion settings  
verifying animation playback

Animations must be tested immediately after import to verify correctness.

---

# 9. Animation Controllers

Characters use animation controllers to manage animation transitions.

Animation controllers are state-based systems.

Example player controller:

Idle
Walk
Run
Attack
Reload
Interact
Damage
Death

Transitions occur based on gameplay input or AI state.

---

# 10. Animation Blending

Animation blending ensures smooth transitions between animations.

Example transitions include:

Idle → Walk  
Walk → Run  
Run → Stop

Blending prevents characters from snapping between poses.

Blend times should be short enough to maintain responsiveness.

Typical blend duration:

0.1 – 0.25 seconds

Long blend times may cause sluggish controls.

---

# 11. Combat Animation Timing

Combat animations must align precisely with gameplay mechanics.

Each attack animation contains several phases.

Wind-Up Phase  
The enemy or player prepares the attack.

Strike Phase  
The actual hit occurs.

Recovery Phase  
The attacker returns to neutral stance.

Only the **Strike Phase** should apply damage.

This ensures players can visually anticipate attacks.

Example timing:

Wind-Up: 0.4s  
Strike: 0.1s  
Recovery: 0.5s

This structure keeps combat readable and fair.

---

# 12. Animation Events

Animation events trigger gameplay actions at specific frames.

Examples include:

Attack damage triggers  
Footstep sounds  
Weapon reload completion  
Door interaction completion

Example animation event:

Frame 23 → TriggerDamage()

Events allow animations and gameplay systems to remain synchronized.

Without events, gameplay logic may feel disconnected from animation.

---

# 13. Enemy Animation Behavior

Enemy animations must clearly communicate behavior.

Key animation principles:

Enemies should telegraph attacks clearly  
Movement animations should indicate speed and threat level  
Damage reactions should provide feedback to the player

Examples:

Rotters

Slow, unsteady walking animation  
Wide arm swings during attacks

Stalkers

Low crouched movement  
Quick lunging attacks

Spliced

Heavy, slow movement  
Large sweeping attack animations

These animation styles help differentiate enemy types visually.

---

# 14. Hit Reaction Animations

Enemies must react to damage.

Hit reactions provide visual confirmation that the player's attacks are effective.

Examples:

Small hit reaction  
Stagger animation  
Knockdown animation

Not every hit should interrupt the enemy.

Stronger enemies may ignore weaker attacks.

Balancing hit reactions helps maintain combat tension.

---

# 15. Death Animations

Enemies must include death animations.

Death animations provide visual closure for combat encounters.

Examples:

Forward collapse  
Backward fall  
Heavy creature collapse

Enemy bodies may remain in the environment for a short time.

To preserve performance, enemy corpses may despawn after a set duration.

Example despawn time:

30 seconds

Object pooling may also be used for corpses.

---

# 16. Environmental Animations

Environmental objects may contain animations.

Examples include:

Doors opening  
Elevators moving  
Machinery operating  
Environmental destruction

These animations are usually triggered through the **Interaction System**.

Environmental animations must not block gameplay flow.

Example:

Door opening animations should complete quickly enough to avoid frustrating players.

---

# 17. Animation Performance Optimization

Animations must remain efficient.

Optimization strategies include:

Limiting bone counts in rigs  
Reducing animation update rates for distant characters  
Using simplified animation sets for distant enemies

Example:

Enemies beyond 40 meters may use simplified animation updates.

This reduces CPU workload.

---

# 18. Animation LOD

Animation systems may also use Level of Detail.

Animation LOD reduces animation complexity for distant characters.

Example levels:

LOD0  
Full animation system

LOD1  
Reduced animation blending

LOD2  
Minimal animation updates

This technique significantly improves performance in large encounters.

---

# 19. Animation Debugging Tools

Development builds should include animation debugging tools.

Examples include:

Animation state viewer  
Animation event tracker  
Skeleton visualization  
Animation timeline preview

These tools help diagnose animation errors.

Example debug view:

Current State: Enemy_Attack
Blend Time: 0.12s
Animation Time: 0.65

Debug tools greatly improve troubleshooting speed.

---

# 20. Animation Testing

Animations must undergo thorough testing.

Testing includes:

Movement responsiveness  
Combat timing  
Animation transitions  
Enemy attack telegraphing

Animations should always feel responsive and readable.

Players must be able to understand enemy behavior through animation alone.

---

# 21. Animation Finalization

Before animations are finalized, they must pass validation checks.

Final validation includes:

Correct animation import  
Proper animation controller integration  
Correct event timing  
Stable transitions between animation states

Once validated, animations become part of the final animation library for the project.

Future updates may expand the animation library with additional actions or enemy types.

---