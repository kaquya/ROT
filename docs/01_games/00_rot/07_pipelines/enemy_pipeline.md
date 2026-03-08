# Enemy Pipeline

Project: ROT  
Version: 1.1  
Document Type: Production Pipeline  
Category: Enemy Production  
Scope: ROT (Game)  
Status: Core Reference

---

# 1. Overview

This document defines the pipeline used to create enemy assets for ROT.

Enemy production includes the full process from concept design to in-game implementation. This pipeline ensures that enemy creatures remain visually consistent with the Rot ecosystem while meeting technical and gameplay requirements.

The pipeline connects multiple disciplines including:

- concept art
- creature design
- 3D modeling
- animation
- gameplay integration
- audio design

Following a consistent pipeline ensures that enemies remain cohesive with the visual identity and biological rules of the Rot universe.

---

# 2. Pipeline Goals

The enemy pipeline is designed to achieve several objectives.

## Biological Consistency

All creatures must follow the biological rules of the Rot ecosystem defined in:

- `rot_ecology.md`
- `creature_design_rules.md`

Enemy designs should appear like plausible biological mutations.

---

## Gameplay Clarity

Enemy designs must communicate behavior clearly.

Players should be able to understand:

- threat level
- attack patterns
- movement behavior

Visual readability is critical for survival gameplay.

---

## Technical Efficiency

Enemy assets must meet performance requirements.

Examples include:

- optimized polygon counts
- efficient skeletal rigs
- manageable animation sets

Enemies should remain performant even during multiple encounters.

---

# 3. Enemy Production Stages

Enemy assets are created through several production phases.

---

# 4. Concept Design

The concept stage defines the visual identity and biological structure of the creature.

Concept artists produce:

- creature silhouettes
- anatomical structure
- mutation features
- ecological role

Concepts must align with:

- Rot mutation rules
- creature ecosystem roles
- environmental context

Approved concepts move to the modeling stage.

---

# 5. Creature Design Review

Before production begins, designs are reviewed to ensure they meet gameplay and narrative goals.

Review criteria include:

- silhouette readability
- animation feasibility
- biological plausibility
- gameplay role clarity

If necessary, concepts are refined before moving forward.

---

# 6. High Resolution Modeling

Artists create a detailed high resolution model of the creature.

This stage focuses on:

- anatomical detail
- Rot corruption patterns
- surface damage and mutation structures

High resolution models are used as the base for creating optimized game assets.

---

# 7. Game Ready Model Creation

The high resolution model is converted into a game ready asset.

This stage includes:

- polygon optimization
- UV mapping
- topology cleanup
- preparation for rigging

The final model must meet engine performance requirements.

---

# 8. Texturing

Textures define the surface appearance of the creature.

Texture maps may include:

- base color
- normal maps
- roughness maps
- biological corruption overlays

Rot organisms often include organic patterns such as:

- infected tissue
- fungal growth
- parasitic structures

Textures should follow the visual rules defined in `rot_visual_design.md`.

---

# 9. Rigging

The creature model receives a skeletal rig that allows animation.

Rigging defines:

- bone structure
- movement constraints
- deformation behavior

Creature rigs must support the movement style defined by the enemy's biological anatomy.

Examples include:

- quadrupedal movement
- crawling motion
- distorted limb structures

---

# 10. Animation

Animations bring the creature to life.

Typical enemy animation sets include:

- idle behavior
- walking and running
- attack animations
- damage reactions
- death animations

Additional animations may include:

- investigation behavior
- environmental interactions

Animations must remain readable and consistent with gameplay timing.

---

# 11. Audio Integration

Enemy audio reinforces creature presence and behavior.

Audio elements include:

- idle sounds
- movement noises
- attack vocalizations
- injury reactions

Audio cues help players identify enemy states before visual contact.

---

# 12. Gameplay Integration

Once the enemy asset is complete, it is integrated into gameplay systems.

Integration includes:

- assigning enemy stats
- connecting AI behavior
- defining attack mechanics
- configuring perception ranges

This step connects the asset with systems such as:

- Enemy AI System
- AI Perception System
- Combat System

---

# 13. Testing and Iteration

Enemies must undergo gameplay testing to ensure they function correctly.

Testing evaluates:

- animation timing
- hit detection accuracy
- AI behavior consistency
- encounter difficulty

Issues discovered during testing may require adjustments to:

- animations
- stats
- AI behavior

---

# 14. Optimization

Final optimization ensures that enemies perform efficiently during gameplay.

Optimization steps include:

- reducing unnecessary geometry
- optimizing animation rigs
- ensuring efficient texture usage

Enemy assets must remain performant even when multiple creatures appear simultaneously.

---

# 15. Integration with Other Systems

Enemy assets interact with multiple gameplay systems.

Examples include:

- Enemy AI System
- Combat System
- AI Perception System
- Audio Gameplay System
- Rot Exposure System

Coordination between these systems ensures enemies behave consistently in the game world.

---

# 16. Purpose of This Document

This document defines the pipeline used to create enemy assets for ROT.

By following a structured production process, the development team ensures that enemies remain visually consistent, technically optimized, and aligned with the ecological horror themes of the game.

---