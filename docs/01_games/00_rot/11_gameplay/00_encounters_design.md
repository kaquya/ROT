# ROT – Encounter Design

Version: 1.0  
Status: Gameplay Design

---

# 1. Purpose of Encounter Design

Encounter design defines how enemies are distributed throughout the world of ROT.

Rather than placing enemies randomly, encounters are carefully designed to support:

• exploration tension  
• resource management  
• environmental storytelling  
• pacing progression  

Each district gradually increases difficulty while introducing new enemy behaviors.

The goal is to maintain **survival horror tension without overwhelming the player**.

---

# 2. Encounter Design Principles

Enemy placement must follow several design principles.

---

## Controlled Escalation

Enemy types and group sizes gradually increase as the player progresses.

Example escalation:

```
Residential District → isolated enemies
Downtown → small groups
Emergency Center → ambush encounters
Harbor → aggressive enemies
Hospital → claustrophobic threats
Forest → fast predators
Research Center → elite enemies
Convergence Chamber → boss encounters
```

---

## Environmental Context

Enemy placement should reflect the story of the environment.

Examples:

• infected residents inside homes  
• harbor workers near docks  
• medical staff inside hospital corridors  
• Halcyon researchers within laboratories  

Enemies should appear where they logically belong.

---

## Encounter Variety

Each district should contain different encounter types.

Examples:

• wandering enemies  
• ambush enemies  
• patrol enemies  
• environmental hazard encounters  
• mini-boss fights  

Variety prevents encounters from becoming predictable.

---

## Resource Balance

Encounters must be balanced with available resources.

The player should rarely have enough ammunition to defeat every enemy.

This encourages decisions such as:

• avoiding encounters  
• using stealth  
• conserving ammunition  

---

# 3. Encounter Types

The game uses several encounter formats.

---

## Patrol Encounter

Enemies move through a defined patrol route.

Players may:

• hide  
• ambush  
• sneak past  

Patrol encounters are common in outdoor environments.

---

## Ambush Encounter

Enemies remain hidden until the player enters a trigger zone.

Examples:

• enemies behind doors  
• enemies emerging from Rot growth  
• enemies falling from ceilings  

Ambush encounters create sudden tension.

---

## Horde Encounter

Multiple enemies attack simultaneously.

These encounters typically occur in:

• open spaces  
• plazas  
• large rooms  

The goal is to force players to reposition or retreat.

---

## Environmental Hazard Encounter

Enemies appear in areas containing environmental hazards.

Examples:

• explosive containers  
• electrical traps  
• collapsing structures  

Players may use hazards strategically.

---

## Mini-Boss Encounter

Mini-bosses are stronger enemies guarding key areas.

Mini-bosses may:

• block progression  
• guard valuable resources  
• appear in optional side areas  

---

# 4. District Encounter Distribution

This section defines enemy types and approximate encounter intensity per district.

---

# 4.1 Residential District

Difficulty Level: **Very Low**

This area introduces the player to basic combat and stealth.

Enemy Types:

• Civilian Rotters  
• Collapsed Rotters  

Encounter Design:

Small isolated encounters.

Example placements:

```
Street Corner
1 Rotter

Backyard Path
1 Rotter

Abandoned House
1 Collapsed Rotter (ambush)

Apartment Courtyard
Mini-Boss: Caretaker
```

The player should feel threatened but not overwhelmed.

---

# 4.2 Downtown District

Difficulty Level: **Low**

Downtown introduces small enemy groups.

Enemy Types:

• Civilian Rotters  
• Collapsed Rotters  
• Military Rotters

Encounter Design:

```
Clock Tower Square
3 Rotters

Grocery Store Interior
2 Rotters

Service Alley
1 Collapsed Rotter (ambush)

Town Hall Entrance
Mini-Boss: Checkpoint Enforcer
```

Downtown introduces the idea that **some encounters are dangerous enough to avoid**.

---

# 4.3 Emergency Coordination Center

Difficulty Level: **Moderate**

This district introduces more aggressive enemies.

Enemy Types:

• Rotters  
• Military Rotters  
• Shadow Stalker

Encounter Design:

```
Entrance Hall
2 Rotters

Operations Room
3 Military Rotters

Communication Wing
1 Shadow Stalker

Equipment Storage
2 Rotters (ambush)
```

The Shadow Stalker introduces stealth gameplay.

---

# 4.4 Harbor District

Difficulty Level: **Moderate to High**

The harbor shows the first heavy Rot ecosystem growth.

Enemy Types:

• Harbor Rotters  
• Stalkers  
• Spliced

Encounter Design:

```
Dock Platform
3 Harbor Rotters

Warehouse Interior
2 Rotters + 1 Stalker

Crane Walkway
2 Rotters

Fuel Storage Area
Spliced (mini-boss)

Harbor Crane Platform
Boss: Harbor Bloom Guardian
```

Environmental hazards such as fuel containers are common here.

---

# 4.5 Hospital District

Difficulty Level: **High**

The hospital focuses on claustrophobic combat and stealth.

Enemy Types:

• Medical Rotters  
• Collapsed Rotters  
• Shadow Stalkers  

Encounter Design:

```
Emergency Entrance
2 Rotters

Patient Ward
3 Medical Rotters

Surgical Theater
Mini-Boss: Ward Mother

Quarantine Wing
2 Shadow Stalkers

Basement Morgue
1 Collapsed Rotter (ambush)
```

Lighting conditions make stealth extremely valuable.

---

# 4.6 Forest Region

Difficulty Level: **High**

The forest introduces Rot-infected wildlife.

Enemy Types:

• Rot Wolves  
• Hunter Stalkers  
• Rot Stag (mini-boss)

Encounter Design:

```
Forest Trail
2 Rot Wolves

Observation Tower
1 Hunter Stalker

Campsite
2 Rot Wolves

Forest Clearing
Mini-Boss: Rot Stag
```

The forest emphasizes movement and open-space combat.

---

# 4.7 Halcyon Marine Research Center

Difficulty Level: **Very High**

Enemies here represent advanced Rot mutations.

Enemy Types:

• Stalkers  
• Spliced  
• Experimental Subjects

Encounter Design:

```
Facility Entrance
2 Rotters

Laboratory Wing
2 Stalkers

Containment Chamber
Mini-Boss: Prototype Subject

Security Corridor
3 Rotters + 1 Stalker
```

This district reveals the full consequences of Halcyon experiments.

---

# 4.8 Rot Convergence Chamber

Difficulty Level: **Extreme**

This area represents the core Rot ecosystem beneath the research facility.

Enemy Types:

• Rot Growth Entities  
• Spliced  

Encounter Design:

```
Entry Tunnel
2 Spliced

Outer Cavern
3 Rot Growth Entities

Central Chamber
Final Boss: Dr Victor Soren
```

This area should feel alien compared to the rest of the game.

---

# 5. Dynamic Encounter Changes

As the game progresses, some districts may experience increased enemy presence.

Examples:

Residential District (late game)

• additional Rotters  
• environmental Rot growth  

Downtown District

• new Stalker patrols  

These changes reinforce the spreading Rot ecosystem.

---

# 6. Encounter Balance Goals

Encounter design must support the core survival horror philosophy.

Players should feel:

• vulnerable  
• resource-limited  
• constantly at risk  

However, encounters must also remain fair and readable.

Good encounter design ensures that:

• players can escape dangerous situations  
• stealth remains viable  
• environmental awareness is rewarded  

The goal is to create tension without frustration.

---

# 7. Relationship to Other Systems

Encounter design works closely with several other systems.

Enemy behavior is defined in:

```
enemy_ai_system.md
enemy_design_document.md
```

World structure is defined in:

```
world_map.md
district_layouts.md
```

Combat balance is defined in:

```
enemy_stats.md
player_stats.md
difficulty_balance.md
```

Together, these systems define the full gameplay experience of ROT.

---