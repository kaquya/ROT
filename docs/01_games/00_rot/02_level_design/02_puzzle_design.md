# ROT – Puzzle Design

Version: 1.0  
Status: Gameplay Design

---

# 1. Purpose of This Document

This document defines the design principles and structure of puzzles used throughout ROT.

Puzzles are an important part of the exploration gameplay loop and are used to:

• unlock new areas  
• control player progression  
• reinforce environmental storytelling  
• encourage exploration of the world

Unlike abstract puzzle games, puzzles in ROT should always feel **grounded in the physical environment**.

Players should feel like they are interacting with real systems within the world.

---

# 2. Puzzle Design Philosophy

Puzzle design in ROT follows several guiding principles.

---

## Environmental Logic

Puzzles must make sense within the environment.

Examples include:

• restoring electrical power  
• repairing mechanical equipment  
• unlocking security systems  
• removing Rot growth blocking pathways

The player should understand the problem through observation.

---

## Exploration Driven Solutions

Puzzle solutions often require exploration of nearby areas.

Players may need to:

• locate missing components  
• find access cards  
• activate multiple switches in different locations

This encourages players to explore the environment thoroughly.

---

## Minimal Abstraction

Puzzles should avoid abstract mechanics such as symbol matching or mathematical puzzles.

The focus should remain on **environmental interaction**.

---

# 3. Puzzle Categories

Several puzzle categories appear throughout the game.

These categories repeat across districts to create familiarity while still offering variation.

---

# 3.1 Infrastructure Restoration

Many locations contain damaged infrastructure that must be restored.

Examples include:

• restoring electrical power  
• repairing water pumps  
• activating emergency generators

Typical puzzle flow:

1. discover damaged system
2. locate missing component
3. restore functionality

---

# 3.2 Access Control Systems

Restricted areas often require access credentials.

Examples include:

• security keycards  
• mechanical keys  
• electronic access terminals

These puzzles encourage players to search nearby areas for required items.

---

# 3.3 Environmental Manipulation

Some puzzles require manipulating the environment itself.

Examples include:

• moving heavy objects  
• activating machinery  
• opening blocked pathways

These puzzles create new exploration routes.

---

# 3.4 Rot Obstruction Removal

As the Rot spreads, organic growth structures block many areas.

Players must destroy or disable these obstacles.

Examples include:

• destroying Rot growth nodes  
• neutralizing spore sacs  
• clearing biomass clusters

Removing these structures often reduces nearby enemy activity.

---

# 4. Puzzle Difficulty Curve

Puzzle complexity increases gradually as the game progresses.

Early Game

Simple environmental puzzles introducing basic mechanics.

Mid Game

Multi-step puzzles requiring exploration across districts.

Late Game

Complex puzzles integrated with Rot ecosystem mechanics.

Despite this progression, puzzles should remain readable and logical.

---

# 5. Puzzle Feedback

When a puzzle is solved, the game should clearly communicate the result.

Examples include:

• power restoring to nearby buildings  
• locked doors opening  
• Rot growth collapsing

Clear feedback helps players understand the consequences of their actions.

---

# 6. Optional Puzzle Content

Some puzzles are optional and reward exploration.

Optional puzzles may unlock:

• hidden supply caches  
• rare crafting materials  
• narrative documents

These puzzles encourage curious players to explore thoroughly.

---

# 7. District Puzzle Implementation

Each district introduces specific puzzle mechanics that reflect its environment.

---

## Residential District

The Residential District introduces the player to basic puzzle interactions.

Examples include:

• unlocking blocked gates  
• restoring power to a residential street  
• locating house keys

These puzzles are simple and serve as tutorials for later mechanics.

---

## Downtown District

Downtown puzzles involve interacting with municipal infrastructure.

Examples include:

• activating emergency generators  
• unlocking municipal buildings  
• restoring power to the clock tower square

Downtown puzzles often open shortcuts connecting different parts of the town.

---

## Emergency Coordination Center

Puzzles in this district focus on communication and emergency systems.

Examples include:

• repairing radio transmitters  
• activating emergency control panels  
• restoring power to the operations room

These puzzles reveal how the town attempted to coordinate evacuation.

---

## Harbor District

The harbor introduces environmental hazard puzzles.

Examples include:

• activating dock cranes to move cargo containers  
• opening shipping gates  
• destroying Rot growth blocking dock pathways

These puzzles often involve interacting with industrial machinery.

---

## Hospital District

Hospital puzzles focus on medical infrastructure.

Examples include:

• locating patient records to unlock quarantine wards  
• restoring backup power to surgical theaters  
• unlocking restricted medical storage rooms

These puzzles reveal attempts to treat the Rot infection.

---

## Forest Region

Forest puzzles rely on natural environmental obstacles.

Examples include:

• clearing fallen trees blocking paths  
• activating ranger station generators  
• locating trail keys to open ranger buildings

These puzzles emphasize exploration in outdoor environments.

---

## Halcyon Research Center

Research facility puzzles involve advanced technology.

Examples include:

• unlocking laboratory security systems  
• activating containment protocols  
• restoring power to research equipment

These puzzles reveal the scientific investigation of the Rot organism.

---

# 8. Rot Ecosystem Puzzle Mechanics

As the game progresses, puzzles begin interacting directly with the Rot ecosystem.

---

## Rot Growth Nodes

Rot nodes act as biological control centers for nearby growth structures.

Destroying these nodes may:

• open blocked pathways  
• weaken nearby enemies  
• slow Rot spread

---

## Spore Chambers

Some areas become filled with airborne Rot spores.

Players must locate and destroy spore sacs to clear the environment.

Until cleared, these areas damage the player over time.

---

## Biomass Clusters

Large organic growth clusters block corridors and buildings.

Players must locate weak points to destroy these structures.

These encounters combine puzzle solving with combat.

---

# 9. Puzzle Encounter Integration

Puzzles often occur alongside enemy encounters.

Examples include:

• solving generator puzzles while enemies patrol nearby  
• restoring power in dark environments where enemies hide  
• clearing Rot nodes while under attack

This integration increases tension during puzzle sequences.

---

# 10. Puzzle System Implementation

Puzzles are implemented using simple trigger-based systems.

Each puzzle includes three components.

Puzzle Trigger

The object or system the player interacts with.

Puzzle State

Tracks whether the puzzle is incomplete, active, or solved.

Puzzle Outcome

The environmental change that occurs after solving the puzzle.

Puzzle states must be saved in the game state so that progress is preserved.

---

# 11. Puzzle Design Goals

Puzzle design should support the core gameplay loop.

Puzzles must:

• encourage exploration  
• reinforce environmental storytelling  
• control player progression  
• integrate with combat encounters

Puzzles should never feel disconnected from the world.

The player should feel like they are **repairing or interacting with real systems inside the environment**.

---