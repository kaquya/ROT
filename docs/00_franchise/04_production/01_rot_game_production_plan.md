# ROT – Game Production Plan

Version: 1.0  
Status: Pre-Production

---

# 1. Purpose of This Document

The ROT Game Production Plan defines how the first ROT game will be developed as a solo project.

While the Game Design Document describes the creative vision of the game, this document translates that vision into a realistic production strategy.

This plan defines:

• development scope  
• production priorities  
• system implementation order  
• asset creation strategy  
• development phases  

The primary goal of this document is to ensure the game remains achievable for a single developer.

---

# 2. Development Philosophy

ROT is designed to be a **focused survival horror experience with controlled scope**.

Solo development requires strict prioritization.

Several design decisions help ensure the project remains manageable:

• limited number of enemy types  
• modular environment assets  
• district-based level design instead of open world  
• simple but effective gameplay systems  
• environmental storytelling instead of expensive cutscenes  

The goal is to create a **high-quality atmospheric game without AAA production complexity**.

---

# 3. Core Production Goals

The first ROT game should aim to deliver:

• a complete survival horror experience  
• a coherent narrative introduction to the Rot phenomenon  
• a memorable and believable location  
• strong environmental storytelling  
• tense survival gameplay

Estimated playtime target:

10–12 hours.

---

# 4. Development Scope

To maintain a realistic scope, the first game will include the following core elements.

---

## 4.1 Environment Scope

The game world consists of **seven major districts** within Blackwater Cove.

Districts:

• Residential District  
• Downtown District  
• Emergency Coordination Center  
• Harbor District  
• Hospital  
• Forest Region  
• Halcyon Marine Research Center

Final Area:

• Rot Convergence Chamber

These districts form a **semi-open interconnected world**.

However, each district loads independently to maintain performance and reduce development complexity.

---

## 4.2 Enemy Scope

Enemy variety is intentionally limited.

Base enemy categories include:

• Rotters  
• Collapsed Rotters  
• Harbor Rotters  
• Medical Rotters  
• Stalkers  
• Rot Wildlife  
• Spliced organisms

Most enemy variants share base models with visual or behavioral differences.

This reduces animation and modeling workload.

---

## 4.3 Boss Scope

The game includes a small number of major encounters.

Planned encounters:

Mini-Bosses

• The Caretaker  
• Rot Stag  
• Ward Mother  
• Prototype Subject

Major Bosses

• Harbor Bloom Guardian  
• Spliced Medical Mutation  
• Dr Victor Soren

Boss encounters emphasize environmental interaction rather than complex mechanics.

---

# 5. Core Gameplay Systems

The following systems must be implemented to support gameplay.

Core systems:

• player movement and interaction  
• combat system  
• enemy AI system  
• inventory management  
• crafting system  
• puzzle interaction system  
• save system  
• environmental triggers

These systems represent the technical backbone of the game.

---

# 6. Asset Production Strategy

Asset production is one of the largest tasks in game development.

To remain manageable, ROT uses several strategies.

---

## 6.1 Modular Environment Assets

Buildings and environment structures are built using modular components.

Examples include:

• wall segments  
• floors and ceilings  
• doors and windows  
• staircases  
• industrial props

These modules can be reused across multiple districts.

---

## 6.2 Shared Texture Libraries

Textures are reused across many assets.

Examples include:

• concrete surfaces  
• wood materials  
• metal structures  
• Rot organic surfaces

Using shared materials reduces both production time and memory usage.

---

## 6.3 Enemy Model Reuse

Enemy models share base skeletons and animation systems.

For example:

Rotter variants may use the same base model with different textures or growth patterns.

This dramatically reduces animation workload.

---

# 7. Development Engine

The project should use a stable modern game engine capable of supporting:

• 3D environments  
• lighting and atmospheric rendering  
• basic AI systems  
• physics interactions  
• cross-platform asset pipelines

Recommended engines include:

• Unreal Engine  
• Unity

The final choice should prioritize development speed and familiarity.

---

# 8. Technical System Priorities

During development, systems should be implemented in a specific order.

Early systems must support later features.

Primary technical systems include:

1. Player Controller
2. Interaction System
3. Enemy AI Framework
4. Combat System
5. Inventory System
6. Crafting System
7. Puzzle Interaction System
8. Save System

These systems create the foundation required for the game world.

---

# 9. Vertical Slice Definition

Before developing the full game, the project must create a **vertical slice**.

A vertical slice is a small but fully functional section of the final game that demonstrates the core gameplay experience.

The vertical slice confirms that the design is achievable before committing to full production.

---

## 9.1 Vertical Slice Location

Recommended vertical slice area:

Residential District

Reasons:

• contained environment  
• introduction to early Rot organisms  
• manageable layout for testing  
• opportunity to test exploration loops

---

## 9.2 Vertical Slice Features

The vertical slice must include:

Core Gameplay Systems

• player movement  
• basic combat  
• enemy AI behavior  
• inventory system  
• item pickups  
• interaction prompts

Environment

• one complete district section  
• environmental storytelling elements  
• lighting and atmosphere

Enemies

• Rotter enemy type  
• basic enemy patrol behavior

Gameplay Flow

• exploration loop  
• item discovery  
• puzzle interaction  
• safe zone functionality

Completing the vertical slice proves that the gameplay experience works.

---

# 10. Development Phases

Development should proceed through several clearly defined phases.

Each phase builds upon the previous one.

---

## Phase 1 — Core Gameplay Prototype

Goal:

Create a playable prototype containing the fundamental systems.

Systems implemented:

• player controller  
• basic enemy AI  
• basic combat  
• interaction system

Environment:

• simple test environment

Outcome:

A functional sandbox demonstrating the core gameplay loop.

---

## Phase 2 — Vertical Slice

Goal:

Create a polished playable section of the game.

Features implemented:

• full environment art for one district  
• functional enemy encounters  
• puzzle systems  
• inventory and crafting systems  
• basic UI

Outcome:

A small but complete representation of the final game experience.

---

## Phase 3 — Core Systems Expansion

Goal:

Stabilize and refine core gameplay systems.

Tasks include:

• combat balancing  
• AI improvements  
• crafting system expansion  
• save system implementation

Outcome:

Stable gameplay systems ready for full content production.

---

## Phase 4 — Environment Production

Goal:

Build the remaining districts of Blackwater Cove.

Tasks include:

• district layout creation  
• environment asset placement  
• lighting and atmosphere setup

Each district should be fully playable before moving to the next.

---

## Phase 5 — Enemy and Boss Implementation

Goal:

Add advanced enemy types and major encounters.

Tasks include:

• implementing mini-boss encounters  
• building boss arenas  
• balancing enemy encounters

Outcome:

Complete enemy ecosystem across all districts.

---

## Phase 6 — Audio and Atmosphere

Goal:

Enhance immersion and tension.

Tasks include:

• ambient sound implementation  
• enemy audio cues  
• environmental audio effects  
• minimal musical score

Outcome:

Atmosphere significantly enhanced.

---

## Phase 7 — Testing and Balancing

Goal:

Refine gameplay experience.

Tasks include:

• bug fixing  
• performance optimization  
• resource balance adjustments  
• enemy difficulty tuning

Outcome:

Stable and polished gameplay.

---

## Phase 8 — Release Preparation

Goal:

Prepare the game for distribution.

Tasks include:

• store page creation  
• promotional materials  
• trailer production  
• final testing

Outcome:

Game ready for release.

---

# 11. Development Timeline Considerations

Solo development timelines can vary significantly depending on available time.

However, a realistic production estimate may resemble:

Core Prototype  
3–4 months

Vertical Slice  
4–6 months

Environment Production  
8–12 months

Polish and Testing  
4–6 months

Estimated total development time:

18–24 months.

This timeline assumes consistent development effort.

---

# 12. Testing Strategy

Testing should occur throughout development rather than only near release.

Testing stages include:

Internal Testing

Frequent testing during system development.

Gameplay Testing

Ensuring combat, exploration, and puzzles feel balanced.

External Testing

Small group of external players providing feedback.

Focus areas include:

• difficulty balance  
• clarity of puzzles  
• exploration flow  
• enemy encounter fairness

---

# 13. Asset Pipeline Workflow

Efficient asset production is essential for solo development.

Recommended workflow:

Concept Sketch → 3D Blockout → Final Model → Texture → Integration into Engine

This pipeline allows environments to be tested early before final art is complete.

---

# 14. Risk Management

Solo development projects face several risks.

Major risks include:

• scope creep  
• asset production overload  
• complex system design

Mitigation strategies include:

• limiting enemy types  
• modular asset design  
• simple gameplay systems

Maintaining strict scope control is critical for completing the project.

---

# 15. Completion Criteria

The game should be considered complete when the following conditions are met:

• all districts are playable  
• all bosses and enemies are implemented  
• gameplay systems are stable  
• performance is optimized  
• the narrative experience is coherent

Only after these conditions are met should the game move toward release.

---