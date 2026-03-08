# Environment Pipeline

Project: ROT  
Version: 1.1  
Document Type: Production Pipeline  
Category: Environment Art  
Scope: ROT (Game)  
Status: Core Reference

---

# 1. Overview

This document defines the environment asset pipeline used for ROT.

The pipeline describes the complete process for creating, importing, and integrating environment assets into the game world.

Environment assets include:

- buildings
- terrain elements
- vegetation
- props
- environmental structures
- Rot biomass growth

A consistent pipeline ensures that assets remain visually consistent, technically optimized, and easy to integrate into the level design workflow.

---

# 2. Pipeline Goals

The environment pipeline is designed to achieve several goals.

## Consistency

All assets must follow the same visual and technical standards.

This ensures environments feel cohesive and believable.

## Efficiency

The pipeline should allow artists to produce assets quickly while minimizing rework.

Clear steps reduce confusion during asset production.

## Optimization

Environment assets must meet performance requirements.

Polygon budgets, texture sizes, and collision meshes should follow defined guidelines.

## Collaboration

The pipeline should allow environment artists, level designers, and engineers to work together efficiently.

---

# 3. Environment Asset Categories

Environment assets are divided into several major categories.

## Structural Assets

Large structures that define the environment.

Examples include:

- buildings
- bridges
- docks
- towers
- industrial structures

These assets form the backbone of each district.

---

## Modular Assets

Reusable structural components used to build larger environments.

Examples include:

- walls
- floors
- staircases
- door frames
- windows

Modular assets allow level designers to assemble environments efficiently.

---

## Props

Smaller environmental objects that add detail and storytelling.

Examples include:

- furniture
- tools
- crates
- vehicles
- debris

Props help environments feel lived in.

---

## Natural Assets

Natural elements found throughout the environment.

Examples include:

- trees
- rocks
- terrain elements
- vegetation

These assets are especially important in the forest region.

---

## Rot Biomass Assets

Organic structures created by the Rot ecosystem.

Examples include:

- Rot growth clusters
- biological tendrils
- infected surfaces
- pulsating biomass structures

These assets visually represent environmental corruption.

---

# 4. Asset Creation Workflow

Environment assets are created through several production stages.

---

## Concept Stage

Concept artists create visual references for new environments and asset types.

Concept work defines:

- overall shape
- scale
- visual style
- Rot corruption level

Concepts guide asset modeling.

---

## Blockout Stage

Initial blockout models are created to establish scale and layout.

Blockout models use simple geometry and minimal detail.

These models are used by level designers to test environment layouts.

---

## High Resolution Modeling

Artists create detailed versions of assets using 3D modeling software.

High resolution models include:

- detailed surface structure
- Rot growth patterns
- realistic environmental damage

These models define the final visual quality.

---

## Game Ready Model Creation

High resolution assets are converted into optimized game models.

This step includes:

- reducing polygon counts
- creating level of detail models
- preparing UV layouts

Game ready models must meet technical performance requirements.

---

## Texture Creation

Textures are created to define surface appearance.

Examples include:

- base color maps
- normal maps
- roughness maps
- Rot corruption overlays

Textures must follow consistent visual standards.

---

## Asset Import

Finished assets are imported into the game engine.

During import, artists configure:

- materials
- collision meshes
- level of detail settings

Assets must be tested for proper scaling and alignment.

---

# 5. Level of Detail (LOD)

Many environment assets require multiple levels of detail.

LOD models reduce visual complexity at greater distances.

Typical LOD structure includes:

- LOD0: full detail model
- LOD1: reduced geometry
- LOD2: simplified model

LOD transitions improve performance in large environments.

---

# 6. Collision Setup

Environment assets must include collision meshes.

Collision defines how the player and enemies interact with objects.

Examples include:

- walls blocking movement
- floors supporting traversal
- props preventing or allowing passage

Collision meshes should remain simple to avoid unnecessary performance costs.

---

# 7. Asset Naming Conventions

Consistent naming conventions improve project organization.

Example naming structure:

```
ENV_[District][AssetType][Name]
```

Examples:

- ENV_Harbor_Crate_01
- ENV_Forest_Tree_Pine_02
- ENV_Downtown_Building_Shop01

Clear naming prevents confusion when managing large asset libraries.

---

# 8. Asset Validation

Before assets are integrated into the game world, they should be validated.

Validation checks include:

- correct scale
- optimized polygon count
- proper collision setup
- correct material assignment

Assets that fail validation should be corrected before integration.

---

# 9. Integration with Level Design

Environment assets are used by level designers to construct playable environments.

Designers assemble modular assets to create:

- buildings
- interior spaces
- navigation paths
- environmental storytelling locations

Close collaboration between artists and level designers ensures environments remain visually coherent.

---

# 10. Pipeline Tools

Several tools may assist the environment pipeline.

Examples include:

- 3D modeling software
- texture creation tools
- asset validation scripts
- engine level editing tools

These tools help maintain efficiency during asset production.

---

# 11. Purpose of This Document

This document defines the pipeline used to create environment assets for ROT.

A clear pipeline ensures that assets remain visually consistent, technically optimized, and easy to integrate into the game world.

Following this workflow helps maintain production efficiency throughout development.

---