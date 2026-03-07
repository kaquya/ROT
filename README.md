# ROT

ROT is a survival horror game currently in pre-production.

This repository contains the **complete design, technical, and production documentation** for the project.  
The documentation is structured to support **solo development**, clear system architecture, and a smooth transition into implementation.

The project is currently in the **documentation and vertical slice preparation phase**.

---

# Repository Structure

The repository is divided into several documentation sections.  
Each section focuses on a specific aspect of the project.


```
ROT
│
├── docs
│   ├── 00_franchise
│   │   ├── 03_art_worldbuilding
│   │   │   ├── 00_art_direction_bible.md
│   │   │   ├── 01_rot_visual_design.md
│   │   │   ├── 02_creature_design_rules.md
│   │   │   ├── 03_architecture_environment.md
│   │   │   ├── 04_environmental_storytelling.md
│   │   ├── 04_production
│   │   │   ├── 00_franchise_roadmap.md
│   │   │   ├── 01_rot_game_production_plan.md
│   │   │   └── 02_development_milestones.md
│   │   ├── 00_franchise_bible.md
│   │   └── 01_gameplay_systems.md
│   └── 01_games
│       └── 00_rot
│           ├── 00_gdd
│           │   ├── 00_game_design_document.md
│           │   ├── 01_gameplay_flow.md
│           │   ├── 02_weapons_and_items.md
│           │   ├── 03_enemy_stats.md
│           │   └── 04_player_stats.md
│           ├── 01_technical_design
│           │   └── 00_technical_design_document.md
│           ├── 02_level_design
│           │   ├── 00_world_map.md
│           │   ├── 01_district_layouts.md
│           │   ├── 02_puzzle_design.md
│           │   └── 03_vertical_slice_spec.md
│           ├── 03_enemy_design
│           │   └── 00_enemy_design_document.md
│           ├── 04_implementation_plan
│           │   └── 00_implementation_plan.md
│           ├── 05_systems
│           │   ├── 00_player_controller.md
│           │   ├── 01_interaction_system.md
│           │   ├── 02_inventory_system.md
│           │   ├── 03_combat_system.md
│           │   ├── 04_enemy_ai_system.md
│           │   ├── 05_crafting_system.md
│           │   ├── 06_stealth_system.md
│           │   ├── 07_save_system.md
│           │   ├── 08_puzzle_system.md
│           │   ├── 09_boss_system.md
│           │   ├── 10_audio_system.md
│           │   └── 11_ui_system.md
│           ├── 06_engineering
│           │   ├── 00_project_architecture.md
│           │   ├── 01_data_structures.md
│           │   ├── 02_state_management.md
│           │   ├── 03_save_data_format.md
│           │   ├── 04_ai_state_machine.md
│           │   ├── 05_input_system.md
│           │   └── 06_performance_strategy.md
│           ├── 07_pipelines
│           │   ├── 00_environment_pipeline.md
│           │   ├── 01_enemy_pipeline.md
│           │   ├── 02_animation_pipeline.md
│           │   ├── 03_audio_pipeline.md
│           │   └── 04_asset_naming_conventions
│           ├── 08_testing
│           │   ├── 00_test_plan.md
│           │   ├── 01_bug_reporting.md
│           │   └── 02_playtest_protocol.md
│           ├── 09_tools
│           │   ├── 00_editor_tools.md
│           │   └── 01_debug_tools.md
│           └── 10_lore
│               ├── 00_timeline.md
│               ├── 01_halcyon_records.md
│               ├── 02_blackwater_history.md
│               └── 03_collectibles.md
└── game
└── README.md
```


The **game folder** will later contain the actual source code and game assets.

---

# Franchise Documentation

Location:


docs/franchise


These files define the **overall ROT universe** and gameplay philosophy.

### franchise_bible.md

Defines the foundation of the ROT universe.

Includes:

- the Rot phenomenon
- enemy ecosystem
- franchise themes
- narrative philosophy
- recurring symbolism
- long-term narrative arc

---

### gameplay_systems.md

Defines gameplay systems shared across ROT games.

Includes:

- combat philosophy
- inventory system design
- crafting systems
- stealth mechanics
- enemy AI concepts
- resource economy

---

# Art and Worldbuilding

Location:


docs/art_worldbuilding


Defines the visual direction and environmental storytelling of the game.

### art_direction_bible.md

Defines the overall visual style.

Includes:

- tone
- lighting
- environmental decay
- atmosphere

---

### rot_visual_design.md

Defines how the Rot organism visually appears.

Includes:

- mutation structures
- growth patterns
- color palette
- environmental infection

---

### creature_design_rules.md

Rules for designing Rot-infected enemies.

Includes:

- mutation principles
- anatomy distortion
- silhouette design
- behavior traits

---

### architecture_environment.md

Defines environment design.

Includes:

- building styles
- decay and destruction
- Rot corruption stages

---

### environmental_storytelling.md

Defines how the world communicates story.

Includes:

- abandoned environments
- civilian traces
- disaster storytelling
- Rot takeover progression

---

# Production Documentation

Location:


docs/production


Defines the development roadmap and project planning.

### franchise_roadmap.md

Long-term plans for the ROT franchise.

Includes:

- potential future games
- narrative expansion
- world progression

---

### rot_game_production_plan.md

Production planning for the first game.

Includes:

- development phases
- vertical slice planning
- milestone structure

---

### development_milestones.md

Defines development stages.

Includes:

- prototype
- vertical slice
- alpha
- beta
- release

---

# Game Documentation

Location:


docs/games/rot


Contains all documentation specific to the first ROT game.

---

# Game Design

Location:


docs/games/rot/gdd


### game_design_document.md

Main design document.

Includes:

- story structure
- characters
- districts
- enemy encounters
- boss fights
- gameplay progression

---

# Technical Design

Location:


docs/games/rot/technical_design


### technical_design_document.md

Defines system architecture.

Includes:

- engine systems
- system dependencies
- runtime architecture

---

# Level Design

Location:


docs/games/rot/level_design


### world_map.md

Defines the global map structure of Blackwater Cove.

---

### district_layouts.md

Defines layouts for each district.

Includes:

- exploration routes
- enemy placement philosophy
- shortcuts and loops

---

### puzzle_design.md

Defines puzzle structure.

Includes:

- puzzle types
- progression gating
- puzzle integration

---

# Enemy Design

Location:


docs/games/rot/enemy_design


### enemy_design_document.md

Defines enemy types and behaviors.

Includes:

- Rotters
- Stalkers
- Spliced
- wildlife mutations
- boss entities

---

# Gameplay Systems

Location:


docs/games/rot/systems


Core gameplay system documentation.

Includes:

- player_controller.md
- interaction_system.md
- inventory_system.md
- combat_system.md
- enemy_ai_system.md
- stealth_system.md
- crafting_system.md
- save_system.md
- puzzle_system.md
- boss_system.md
- ui_system.md
- audio_system.md

These documents define the **mechanics that power gameplay**.

---

# Engineering

Location:


docs/games/rot/engineering


Defines internal software architecture.

Includes:

- project_architecture.md
- data_structures.md
- state_management.md
- save_data_format.md
- ai_state_machine.md
- input_system.md
- performance_strategy.md

---

# Pipelines

Location:


docs/games/rot/pipelines


Defines asset production workflows.

Includes:

- environment_pipeline.md
- enemy_pipeline.md
- animation_pipeline.md
- audio_pipeline.md
- asset_naming_conventions.md

---

# Testing

Location:


docs/games/rot/testing


Includes:

- test_plan.md
- bug_reporting.md
- playtest_protocol.md

---

# Tools

Location:


docs/games/rot/tools


Includes:

- editor_tools.md
- debug_tools.md

---

# Lore

Location:


docs/games/rot/lore


Includes narrative background and world history.

### timeline.md

Chronological history of the ROT universe.

---

### halcyon_records.md

Recovered Halcyon research documents.

---

### blackwater_history.md

History of Blackwater Cove before the outbreak.

---

# Game Implementation

Location:


game


This folder will contain the **actual game project and source code** once development begins.

---

# Development Status

Current phase:

**Documentation Complete**

Next step:

**Vertical Slice Prototype**

Systems to implement first:

1. Player Controller
2. Camera System
3. Interaction System
4. Inventory System
5. Combat Prototype
6. Enemy AI Prototype
7. First Test Level

---

# License

To be determined.

---