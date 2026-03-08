# Asset Naming Conventions

Project: ROT  
Version: 1.1  
Document Type: Production Pipeline  
Category: Asset Management  
Scope: ROT (Game)  
Status: Core Reference

---

# 1. Overview

This document defines the naming conventions used for all production assets in ROT.

Consistent naming conventions are essential for maintaining a clean and understandable project structure. Clear asset names allow developers, artists, designers, and engineers to quickly identify the purpose and origin of an asset without needing to inspect it manually.

The rules defined here apply to all asset types, including:

- environment assets
- characters and creatures
- animations
- textures and materials
- audio files
- visual effects
- scripts and data assets

Following these conventions helps prevent confusion and improves long term maintainability of the project.

---

# 2. Naming Philosophy

All asset names should follow several key principles.

## Clarity

The name should clearly describe what the asset represents.

Avoid vague names such as:

- object01
- model_final
- asset_test

Instead, the name should communicate the asset type and purpose.

---

## Consistency

All assets should follow the same structural naming format.

Consistent naming allows teams to quickly search and filter assets in the project.

---

## Brevity

Names should be descriptive but not unnecessarily long.

Avoid including redundant words or unnecessary prefixes.

---

## Stability

Once an asset is integrated into the project, its name should not change unless absolutely necessary.

Frequent renaming can break references in scenes, scripts, or data systems.

---

# 3. General Naming Structure

All assets follow a structured naming format.

Typical structure:

```
[Category][Location][Type][Descriptor][Number]
```

Example:

```
ENV_Harbor_Crate_Wood_01
```

This structure ensures that each asset name communicates useful information.

---

# 4. Category Prefixes

Each asset type begins with a category prefix.

Common prefixes include:

| Prefix | Category |
|------|------|
| ENV | Environment assets |
| CHR | Character assets |
| ENM | Enemy assets |
| PRP | Props |
| VFX | Visual effects |
| SFX | Sound effects |
| MUS | Music |
| UI | User interface |
| MAT | Materials |
| TEX | Textures |
| ANM | Animations |
| SYS | System assets |

These prefixes make it easier to organize assets in large projects.

---

# 5. Environment Asset Naming

Environment assets should include the district or environment where the asset is primarily used.

Structure:

```
ENV_[District][AssetType][Descriptor]_[Number]
```

Examples:

```
ENV_Residential_House_Small_01
ENV_Harbor_Crate_Wood_02
ENV_Forest_Tree_Pine_03
```

This helps level designers quickly locate appropriate assets.

---

# 6. Enemy Asset Naming

Enemy assets should clearly identify the creature type.

Structure:

```
ENM_[CreatureType][AssetType][Descriptor]
```

Examples:

```
ENM_Rotter_Model
ENM_Rotter_Attack_A
ENM_Stalker_Idle
```

Creature type identifiers should match the names defined in the enemy design documentation.

---

# 7. Animation Naming

Animation assets should clearly describe the action performed.

Structure:

```
ANM_[CharacterType]_[Action]`
```

Examples:

```
ANM_Player_Walk
ANM_Player_Sprint
ANM_Rotter_Attack
ANM_Rotter_Death
```

If multiple variations exist, they may be numbered.

Example:

```
ANM_Rotter_Attack_01
ANM_Rotter_Attack_02
```

---

# 8. Texture Naming

Textures should include both the asset type and the texture map type.

Structure:

```
TEX_[AssetName]_[MapType]
```

Examples:

````
TEX_RotWall_BaseColor
TEX_RotWall_Normal
TEX_RotWall_Roughness
```

Common map types include:

- BaseColor
- Normal
- Roughness
- Metallic
- Emissive
- Opacity

---

# 9. Audio Naming

Audio files should describe both the source and the type of sound.

Structure:

```
SFX_[Source]_[Action]
```

Examples:

```
SFX_Door_Open
SFX_Rotter_Growl
SFX_Player_Footstep_Wood
```

Music tracks should use the MUS prefix.

Examples:

```
MUS_BossEncounter
MUS_Tension_Ambient
```

---

# 10. Visual Effects Naming

Visual effects should clearly describe the effect and its purpose.

Structure:

```
VFX_[EffectType]_[Descriptor]
```

Examples:

```
VFX_RotGrowth_Spread
VFX_Impact_Blood
VFX_Fog_Coastal
```

---

# 11. Version and Variant Naming

If multiple versions of an asset exist, they may include a numeric suffix.

Example:

```
ENV_Harbor_Crate_01
ENV_Harbor_Crate_02
```

Variants should represent meaningful differences rather than temporary revisions.

Temporary work files should remain outside the main project asset structure.

---

# 12. Forbidden Naming Practices

The following naming practices should be avoided.

Do not use:

- spaces in asset names
- special characters
- vague identifiers
- temporary names such as "test", "final", or "new"

Example of incorrect naming:

```
crate final model
```


Correct naming:

```
ENV_Harbor_Crate_Wood_01
```

---

# 13. Folder Structure Alignment

Asset names should match the folder structure where possible.

Example structure:

```
Assets/
Environment/
Enemies/
Audio/
Textures/
Animations/
```

Proper folder organization combined with consistent naming makes large projects easier to manage.

---

# 14. Purpose of This Document

This document defines the asset naming conventions used in ROT.

Following consistent naming rules improves project organization, prevents confusion, and allows teams to manage large asset libraries efficiently throughout development.

---