# Asset Naming Conventions

# 1. Overview

The Asset Naming Convention defines how all assets in the ROT project must be named.

Consistent naming is critical for large projects because it:

- prevents asset confusion
- improves searchability
- simplifies debugging
- keeps project structure readable
- allows automation tools to function correctly

Because ROT is a **solo-developed project**, clear naming rules prevent the project from becoming disorganized over time.

All assets must follow the naming standards defined in this document.

---

# 2. Naming Philosophy

Every asset name should immediately communicate three things:

1. What type of asset it is  
2. What the asset represents  
3. What variation it belongs to

A good asset name should allow developers to understand its purpose without opening the file.

Example:

ENV_Wall_Concrete_A

Meaning:

Environment asset → wall → concrete → variation A

---

# 3. Naming Structure

All assets follow a structured naming format.

[Category][Type][Name]_[Variant]

Example:

ENV_Prop_Barrel_A

Breakdown:

ENV → environment asset  
Prop → asset type  
Barrel → object name  
A → variation

---

# 4. Asset Category Prefixes

Every asset begins with a category prefix.

These prefixes indicate the type of asset.

Common prefixes:

ENV Environment assets
CHR Characters
ENM Enemies
WPN Weapons
SFX Sound effects
MUS Music
UI Interface assets
MAT Materials
TEX Textures
ANIM Animations
VFX Visual effects

Example:

ENM_Rotter_Idle

Enemy animation for Rotter idle state.

---

# 5. Environment Asset Naming

Environment assets include buildings, props, and structural pieces.

Format:

ENV_[Type][Object][Variant]

Examples:

ENV_Wall_Concrete_A
ENV_Door_Metal_A
ENV_Floor_Wood_A
ENV_StreetLamp_A
ENV_Window_Broken_A

Types may include:

Wall  
Floor  
Door  
Roof  
Window  
Prop  
Furniture

---

# 6. Character Asset Naming

Character assets follow a similar format.

Format:

CHR_[CharacterName]_[AssetType]

Examples:

CHR_Elena_Model
CHR_Elena_Rig
CHR_Elena_Texture

Enemy characters use the ENM prefix.

---

# 7. Enemy Asset Naming

Enemy assets follow this structure:

ENM_[EnemyType]_[AssetType]

Examples:

ENM_Rotter_Model
ENM_Rotter_Idle
ENM_Rotter_Attack
ENM_Stalker_Run
ENM_Spliced_Death

Enemy asset types may include:

Model  
Rig  
Animation  
Material  
Texture

---

# 8. Animation Naming

Animations must use consistent naming.

Format:

ANIM_[CharacterType]_[Action]

Examples:

ANIM_Player_Walk
ANIM_Player_Run
ANIM_Player_Attack
ANIM_Rotter_Idle
ANIM_Rotter_Attack
ANIM_Stalker_Ambush

Animations must clearly describe the action performed.

---

# 9. Texture Naming

Textures must include their function in the name.

Format:

TEX_[AssetName]_[MapType]

Examples:

TEX_Wall_Concrete_Diffuse
TEX_Wall_Concrete_Normal
TEX_Wall_Concrete_Roughness

Common map types include:

Diffuse  
Normal  
Roughness  
Metallic  
Emissive

---

# 10. Material Naming

Materials should clearly identify the surface they represent.

Format:

MAT_[SurfaceName]

Examples:

MAT_ConcreteWall
MAT_RotGrowth
MAT_RustedMetal
MAT_DirtyGlass

Materials should be reusable across multiple assets when possible.

---

# 11. Weapon Asset Naming

Weapons must follow consistent naming rules to prevent confusion between different weapon types and variations.

Format:

WPN_[WeaponType][WeaponName][Variant]

Examples:

WPN_Handgun_ServiceA_A
WPN_Handgun_ServiceA_B
WPN_Shotgun_Pump_A
WPN_Rifle_Hunting_A
WPN_Knife_Combat_A

Weapon types may include:

Handgun  
Shotgun  
Rifle  
Knife  
Melee

Variants represent visual or mechanical variations of the same weapon type.

---

# 12. Audio Asset Naming

Audio assets must clearly identify their source and behavior.

Format:

SFX_[Category][Object][Action]

Examples:

SFX_Player_Footstep_Concrete
SFX_Player_Footstep_Wood
SFX_Enemy_Rotter_Attack
SFX_Door_Metal_Open
SFX_UI_Menu_Select

Music naming format:

MUS_[TrackName]

Examples:

MUS_ForestAmbience
MUS_CombatTheme
MUS_BossEncounter

Ambient sounds may also follow:

AMB_[Location]_[Type]

Example:

AMB_Forest_Wind
AMB_Harbor_Waves

---

# 13. UI Asset Naming

User interface assets follow a specific naming structure.

Format:

UI_[ElementType]_[Name]

Examples:

UI_Button_Inventory
UI_Icon_Health
UI_Panel_Inventory
UI_Cursor_Default
UI_HUD_HealthBar

UI element types may include:

Button  
Icon  
Panel  
HUD  
Cursor

---

# 14. VFX Asset Naming

Visual effects must follow structured naming rules.

Format:

VFX_[EffectType]_[Name]

Examples:

VFX_RotGrowth_Spread
VFX_Blood_Splatter
VFX_Explosion_Barrel
VFX_Smoke_Factory
VFX_Sparks_Electric

Effect types may include:

Explosion  
Blood  
Smoke  
Fire  
RotGrowth  
Sparks

---

# 15. Prefab Naming

Prefabs represent reusable objects inside the game engine.

Format:

PF_[Category]_[ObjectName]

Examples:

PF_Enemy_Rotter
PF_Enemy_Stalker
PF_Environment_DoorMetal
PF_Prop_Barrel
PF_Weapon_Shotgun

Prefabs should contain all necessary components required for gameplay functionality.

---

# 16. Scene Naming

Scenes must be named clearly to represent the area they contain.

Format:

SCN_[LocationName]

Examples:

SCN_ResidentialDistrict
SCN_Downtown
SCN_PoliceStation
SCN_Harbor
SCN_Hospital
SCN_Forest
SCN_HalcyonFacility
SCN_UndergroundLab

Scenes should correspond to the major districts defined in the Game Design Document.

---

# 17. File Versioning

When assets require revision, version suffixes may be used.

Format:

[AssetName]_v01
[AssetName]_v02

Example:

ENV_Wall_Concrete_A_v02

However, versioning should be used temporarily during development.

Final assets should not include version numbers.

---

# 18. Deprecated Assets

Unused or outdated assets should not remain in production folders.

Deprecated assets should be moved to a dedicated archive folder.

Example folder:

/Archive

Deprecated assets may include:

obsolete models  
unused textures  
old animation versions

Maintaining a clean asset library prevents confusion during development.

---

# 19. Asset Validation

Before an asset is considered production-ready, it must pass validation checks.

Validation includes:

Correct naming format  
Correct folder placement  
Optimized geometry and textures  
Proper scale and orientation  
Working materials and shaders

Assets failing validation must be corrected before integration into the game.

---

# 20. Naming Consistency Enforcement

Naming conventions must be enforced across the entire project.

This prevents issues such as:

duplicate asset names  
incorrect asset references  
difficult debugging

If naming inconsistencies appear, assets must be renamed immediately.

Consistent naming greatly improves project maintainability.

---

# 21. Naming Convention Summary

All assets in the project follow the same structure:

[Category][Type][Name]_[Variant]

Category prefixes include:

ENV – Environment  
CHR – Characters  
ENM – Enemies  
WPN – Weapons  
SFX – Sound effects  
MUS – Music  
UI – Interface elements  
MAT – Materials  
TEX – Textures  
ANIM – Animations  
VFX – Visual effects  
PF – Prefabs  
SCN – Scenes

Maintaining these naming standards ensures the ROT project remains organized and scalable throughout development.

---