# ROT – Development Milestones

Version: 1.0  
Status: Active Development Roadmap

---

# 1. Purpose of This Document

This document converts the ROT Game Design Document and Production Plan into a structured development roadmap.

Each milestone represents a major step in the development process.

Milestones help maintain focus, prevent scope creep, and ensure the project progresses toward a complete playable game.

Each milestone should be completed before moving to the next stage.

---

# 2. Milestone Structure

Milestones are grouped into development phases.

Each milestone contains:

• objectives  
• systems to implement  
• expected outcome  

The milestones move the project from early technical foundations to final release.

---

# 3. Phase 1 – Core Gameplay Foundations

This phase builds the basic gameplay systems required for any playable experience.

No environment art or story content should be prioritized yet.

The focus is on **mechanical functionality**.

---

## M1 – Player Controller

Objective:

Implement the basic player movement and camera system.

Systems:

• player movement  
• sprinting  
• crouching  
• camera control  
• collision detection

Outcome:

The player can freely move within a 3D environment.

---

## M2 – Interaction System

Objective:

Allow the player to interact with objects in the environment.

Systems:

• interaction prompts  
• object inspection  
• item pickup  
• door interaction  
• simple switches

Outcome:

The player can interact with the environment and collect items.

---

## M3 – Inventory System

Objective:

Create the player inventory system.

Systems:

• inventory slots  
• item storage  
• item usage  
• equipping weapons  
• stackable items

Outcome:

The player can collect, manage, and use items.

---

## M4 – Enemy Framework

Objective:

Create the base enemy AI framework.

Systems:

• enemy movement  
• awareness states  
• patrol behavior  
• detection via sight and sound

Outcome:

Enemies can detect and pursue the player.

---

## M5 – Combat System

Objective:

Implement the combat mechanics.

Systems:

• weapon firing  
• ammunition system  
• enemy damage reactions  
• player damage system  
• weak point detection

Outcome:

The player can fight enemies.

---

# 4. Phase 2 – Core Survival Systems

This phase introduces the systems that define survival gameplay.

---

## M6 – Health and Healing

Objective:

Implement player health and healing mechanics.

Systems:

• health pool  
• healing items  
• damage feedback  
• death state

Outcome:

The player must manage health to survive encounters.

---

## M7 – Crafting System

Objective:

Allow players to create items using materials.

Systems:

• crafting recipes  
• material inventory  
• crafting interface

Outcome:

Players can craft survival items.

---

## M8 – Save System

Objective:

Implement safe zones and saving.

Systems:

• manual save points  
• save data structure  
• game state persistence

Outcome:

Players can save progress in safe zones.

---

## M9 – Puzzle Interaction System

Objective:

Implement environmental puzzle mechanics.

Systems:

• power restoration systems  
• mechanical puzzle triggers  
• environmental state changes

Outcome:

Players can solve environmental puzzles to progress.

---

# 5. Phase 3 – Vertical Slice

This phase builds the first complete playable section of the game.

---

## M10 – Residential District Blockout

Objective:

Create a rough layout of the Residential District.

Tasks:

• basic geometry layout  
• exploration routes  
• safe zone placement

Outcome:

A navigable level layout.

---

## M11 – Vertical Slice Enemy Encounters

Objective:

Populate the vertical slice with enemies.

Tasks:

• Rotter enemy encounters  
• patrol routes  
• ambush encounters

Outcome:

The district contains functional gameplay encounters.

---

## M12 – Vertical Slice Gameplay Loop

Objective:

Create a complete exploration loop.

Tasks:

• key item discovery  
• puzzle interaction  
• enemy encounters  
• return to safe zone

Outcome:

A fully playable vertical slice of the game.

---

# 6. Phase 4 – Full Environment Production

After the vertical slice is completed and validated, full production of the remaining districts begins.

Each district should follow a consistent workflow:

1. Level blockout
2. Gameplay implementation
3. Enemy placement
4. Environment art
5. Lighting and atmosphere

Districts should be completed one at a time to maintain development focus.

---

## M13 – Downtown District

Objective:

Create the central hub district connecting the town.

Tasks:

• layout design  
• exploration routes  
• shortcut systems  
• enemy encounter placement

Outcome:

Downtown becomes the central navigation hub for the game.

---

## M14 – Emergency Coordination Center

Objective:

Implement the emergency command facility.

Tasks:

• interior environment design  
• environmental storytelling elements  
• puzzle systems involving communication equipment

Outcome:

Players learn how the town attempted to respond to the outbreak.

---

## M15 – Harbor District

Objective:

Build the harbor environment where Rot contamination first escalates.

Tasks:

• dock structures  
• warehouses  
• environmental hazards  
• Rot biomass structures

Outcome:

The harbor becomes the first heavily corrupted district.

---

## M16 – Hospital District

Objective:

Create the medical facility where early treatment attempts occurred.

Tasks:

• hospital corridors and wards  
• quarantine zones  
• medical equipment environments

Outcome:

The hospital reveals the medical response to the Rot infection.

---

## M17 – Forest Region

Objective:

Implement the forest ecosystem surrounding Blackwater Cove.

Tasks:

• forest terrain generation  
• wildlife enemy encounters  
• exploration paths

Outcome:

The forest introduces Rot wildlife and new environmental hazards.

---

## M18 – Halcyon Marine Research Center

Objective:

Build the research facility where Halcyon studied the Rot.

Tasks:

• research laboratories  
• restricted underground sections  
• environmental storytelling about Halcyon experiments

Outcome:

The research center reveals the deeper origin of the outbreak.

---

## M19 – Rot Convergence Chamber

Objective:

Create the final area beneath the research center.

Tasks:

• Rot biomass environment  
• organic environmental structures  
• final boss arena

Outcome:

The game reaches its final narrative climax.

---

# 7. Phase 5 – Boss and Mini-Boss Implementation

This phase adds major encounters throughout the game.

---

## M20 – Mini-Boss Encounters

Tasks:

• implement The Caretaker encounter  
• implement Rot Stag encounter  
• implement Ward Mother encounter  
• implement Prototype Subject encounter

Outcome:

Mini-bosses introduce major difficulty spikes.

---

## M21 – Major Boss Encounters

Tasks:

• Harbor Bloom Guardian encounter  
• Spliced Medical Mutation encounter  
• Dr Victor Soren final encounter

Outcome:

Major narrative and gameplay climax moments.

---

# 8. Phase 6 – Audio and Atmosphere

Atmosphere is essential for survival horror.

---

## M22 – Ambient Sound Systems

Tasks:

• environmental soundscapes for each district  
• wind, water, forest ambience

Outcome:

Exploration becomes more immersive.

---

## M23 – Enemy Audio

Tasks:

• Rotter movement sounds  
• Stalker detection audio  
• boss creature sound design

Outcome:

Players receive audio cues about nearby threats.

---

## M24 – Music System

Tasks:

• boss encounter music  
• atmospheric ambient music  
• tension-building sound design

Outcome:

Music enhances dramatic moments without dominating gameplay.

---

# 9. Phase 7 – Testing and Optimization

This phase ensures the game runs smoothly and feels balanced.

---

## M25 – Gameplay Balance

Tasks:

• enemy difficulty adjustments  
• ammunition balance  
• healing item distribution

Outcome:

The survival experience feels fair but tense.

---

## M26 – Bug Fixing

Tasks:

• fix gameplay bugs  
• resolve collision issues  
• repair AI behavior problems

Outcome:

Stable gameplay.

---

## M27 – Performance Optimization

Tasks:

• lighting optimization  
• asset performance improvements  
• enemy count balancing

Outcome:

Stable frame rates on target hardware.

---

# 10. Phase 8 – Release Preparation

The final phase prepares the game for distribution.

---

## M28 – External Testing

Tasks:

• invite external testers  
• gather feedback  
• refine gameplay flow

Outcome:

Fresh perspectives improve the final experience.

---

## M29 – Final Polish

Tasks:

• visual improvements  
• UI polish  
• audio adjustments

Outcome:

The game reaches release quality.

---

## M30 – Release Preparation

Tasks:

• prepare Steam store page  
• build release version  
• finalize marketing materials

Outcome:

ROT is ready for launch.

---

# 11. Development Completion

The game should only release when the following are complete:

• all districts are playable  
• all enemies and bosses are implemented  
• gameplay systems are stable  
• performance is optimized  
• narrative flow is complete

Completing all milestones means the game is production-ready.

---