# Animation Pipeline

Project: ROT  
Version: 1.1  
Document Type: Production Pipeline  
Category: Animation  
Scope: ROT (Game)  
Status: Core Reference

---

# 1. Overview

This document defines the animation production pipeline used for ROT.

Animation is responsible for bringing characters, creatures, and interactive objects to life. The pipeline ensures that animations remain consistent with the tone of the game while also supporting gameplay clarity and technical performance.

The animation pipeline connects several disciplines:

- creature design
- character design
- gameplay programming
- enemy AI systems
- audio design

Following a consistent pipeline ensures that animations are readable, technically stable, and integrated smoothly into gameplay systems.

---

# 2. Pipeline Goals

The animation pipeline is designed to support several important goals.

## Gameplay Clarity

Animations must clearly communicate gameplay information to the player.

Examples include:

- attack windups
- damage reactions
- enemy alert behavior
- player interaction states

Readable animations allow players to react appropriately during encounters.

---

## Horror Atmosphere

Movement and animation should reinforce the unsettling tone of the Rot ecosystem.

Creatures should not move like ordinary animals or humans.

Instead they may display:

- unnatural limb motion
- irregular movement rhythms
- twitching biological behavior

These animation traits strengthen the biological horror identity of the game.

---

## Technical Reliability

Animations must remain stable and predictable during gameplay.

Animation systems should avoid:

- clipping issues
- physics conflicts
- desynchronization with gameplay systems

Stable animation behavior ensures responsive gameplay.

---

# 3. Animation Asset Categories

Several categories of animations exist within the game.

---

## Player Animations

Animations used by the player character.

Examples include:

- idle stance
- walking
- sprinting
- crouching
- weapon attacks
- item usage
- interaction animations

Player animations must feel responsive and precise.

---

## Enemy Animations

Enemy creatures require a wide range of animations.

Typical animation sets include:

- idle behavior
- patrol movement
- chase movement
- attack animations
- damage reactions
- death animations

Additional animations may exist for unique enemy types or bosses.

---

## Environmental Animations

Certain environmental elements include animated behavior.

Examples include:

- machinery movement
- environmental hazards
- Rot growth motion
- moving environmental objects

These animations help environments feel alive and reactive.

---

## Cinematic Animations

Narrative events may include cinematic animation sequences.

Examples include:

- story moments
- scripted events
- boss introductions

These animations often use camera control and timing with audio.

---

# 4. Animation Production Stages

Animation assets move through several stages during production.

---

## Animation Planning

Before animation begins, the required animation sets are defined.

This includes identifying:

- required movement states
- attack variations
- interaction animations
- environmental animation needs

Planning ensures that no essential animations are missing.

---

## Rig Preparation

Animation requires a properly prepared rig.

Rigging includes:

- skeletal bone structure
- joint constraints
- deformation controls

Rig design must support the movement style of the character or creature.

Creatures with unusual anatomy may require specialized rigs.

---

## Blocking Stage

Animators first create a rough blocking pass.

Blocking defines:

- major movement poses
- timing of key actions
- basic animation structure

This stage focuses on movement clarity rather than detail.

---

## Refinement Stage

Once blocking is approved, animations are refined.

Refinement includes:

- smoother motion
- improved weight and timing
- detailed secondary motion

This stage brings animations closer to final quality.

---

## Final Polish

The final stage improves animation quality.

Polish may include:

- subtle body movement
- secondary motion
- animation smoothing

Animations must be checked for visual quality and gameplay clarity.

---

# 5. Animation Integration

After production, animations are integrated into the game engine.

Integration includes:

- assigning animations to characters
- linking animations to gameplay states
- configuring animation blending

Animations must work correctly with gameplay systems such as:

- Player Controller System
- Enemy AI System
- Combat System

---

# 6. Animation State Machines

Animations are controlled using animation state machines.

These state machines determine which animation plays based on gameplay conditions.

Examples include:

Player Animation States

- idle
- walk
- sprint
- attack
- interaction

Enemy Animation States

- idle
- patrol
- chase
- attack
- damage reaction

Animation state machines must remain synchronized with gameplay systems.

---

# 7. Animation Timing and Gameplay

Animation timing is closely linked to gameplay mechanics.

Examples include:

- attack windup duration
- dodge timing
- enemy recovery windows

These timings affect game balance and difficulty.

Animation and gameplay systems must be coordinated carefully.

---

# 8. Testing and Iteration

Animations should be tested regularly within gameplay environments.

Testing focuses on:

- animation readability
- interaction with combat mechanics
- movement responsiveness
- collision issues

Animations may require adjustments based on gameplay feedback.

---

# 9. Optimization

Animation performance must be optimized for gameplay stability.

Optimization techniques include:

- limiting unnecessary animation layers
- reducing excessive bone counts
- efficient animation blending

Efficient animation systems prevent performance issues during large encounters.

---

# 10. Integration with Other Systems

Animation interacts with multiple systems within the game.

Examples include:

- Player Controller System
- Enemy AI System
- Combat System
- Audio Gameplay System
- Physics Systems

These systems rely on animation timing and state information.

---

# 11. Purpose of This Document

This document defines the animation production pipeline used in ROT.

By following a structured workflow, the development team ensures that animations remain consistent, readable, and technically stable while supporting the biological horror atmosphere of the game.

---