# ROT – District Layouts

Version: 1.1  
Status: Level Design Specification

---

# 1. Purpose of This Document

This document defines the **internal spatial layout and gameplay structure** of each district in Blackwater Cove.

While `world_map.md` describes the global structure of the town, this document focuses on:

• internal district layouts  
• exploration routes  
• shortcut placement  
• encounter zones  
• puzzle integration  
• safe zone placement  

These layouts guide the **level blockout phase** of development.

The goal is to ensure each district supports:

• exploration-driven gameplay  
• survival tension  
• environmental storytelling  
• clear navigation flow  

---

# 2. District Layout Philosophy

Each district follows several key level design principles.

---

## Exploration Loops

Districts should not be purely linear.

Players should be able to navigate areas through **multiple interconnected paths**.

Typical loop structure includes:

• a primary entry path  
• branching side areas  
• optional exploration zones  
• hidden shortcuts  

This structure encourages players to learn the geography of the environment.

---

## Navigation Landmarks

Each district should contain recognizable visual landmarks that help orient the player.

Examples include:

• water towers  
• lighthouse structures  
• large industrial cranes  
• hospital signage  

These landmarks allow players to navigate without relying on an artificial minimap.

---

## Vertical Level Design

Many districts include vertical traversal elements.

Examples include:

• rooftops  
• staircases  
• elevated walkways  
• ship decks  

Verticality adds tension and improves combat variety.

---

## Rot Exposure Integration

Certain areas contain higher concentrations of Rot biomass.

These locations gradually increase the player’s **Rot exposure level**.

Examples include:

• infected buildings  
• underground chambers  
• dense Rot growth areas  

This system encourages players to move cautiously through heavily corrupted environments.

---

# 3. Residential District Layout

The Residential District is the **first major exploration area** in the game.

This location introduces the core gameplay systems.

The environment should feel familiar and grounded in reality.

---

## Environmental Theme

Suburban coastal neighborhood.

Features include:

• small family homes  
• narrow residential streets  
• backyard fences  
• abandoned vehicles  
• neighborhood parks

Early Rot corruption is visible but not overwhelming.

---

## Major Locations

Key structures include:

Elena’s Childhood Home

Acts as the first safe zone.

Residential Streets

Main exploration routes through the district.

Neighborhood Park

Open environment used for early enemy encounters.

Abandoned Apartment Block

First interior exploration location.

---

## Layout Structure

The residential district is structured as a loose grid.

Example layout:


Apartment Block
|
Park Area
|
Main Street
/
Back Alley Elena's House
|
Roadblock to Downtown


The district gradually opens as the player explores surrounding houses.

---

## Exploration Flow

The player begins at Elena’s house.

Initial exploration includes:

• searching nearby homes  
• discovering supplies  
• encountering early infected enemies  

Exploration eventually leads to a blocked road connecting to downtown.

Players must solve a simple environmental puzzle to unlock access.

---

## Encounter Design

Enemy density remains relatively low in this district.

Primary enemies:

• Rotters  
• Collapsed Rotters

Encounters are designed to introduce:

• stealth mechanics  
• basic combat  
• resource management

---

## Shortcut Placement

Shortcuts allow players to navigate the district more quickly after exploration.

Examples include:

• unlocked alley gates  
• opened backyard fences  
• interior house connections

These shortcuts reduce travel time during later revisits.

---

# 4. Downtown District Layout

Downtown acts as the **central hub of the game world**.

Players revisit this district multiple times.

---

## Environmental Theme

Small coastal town center.

Features include:

• local shops  
• restaurants  
• municipal buildings  
• narrow service alleys  
• clock tower plaza

The environment should feel dense and interconnected.

---

## Major Locations

Clock Tower Square

Central landmark and navigation anchor.

Town Hall

Contains documents describing early outbreak response.

Local Café

Acts as the downtown safe zone.

Grocery Store

Contains resource caches and environmental storytelling.

---

## Layout Structure

Downtown is organized around a central plaza.

Example layout:

```      
                         Town Hall
                            |
Commercial Street — Clock Tower Plaza — Market Street
       |
Café Safe Zone
```


Multiple narrow alleyways connect buildings together.

---

## Exploration Role

Downtown functions as the **central connector for multiple districts**.

District connections include:

Residential District  
Emergency Coordination Center  
Hospital District  
Harbor District

Because of this, players will frequently return to downtown.

---

## Encounter Design

Enemy density increases compared to the residential district.

Enemy types include:

• Rotters  
• Collapsed Rotters  
• early Stalker encounters

Ambush encounters occur in narrow alleyways.

---

## Environmental Storytelling

Downtown shows the **collapse of organized evacuation efforts**.

Examples include:

• overturned military vehicles  
• barricaded storefronts  
• emergency medical stations

Players begin discovering Halcyon-related documents in this area.

---

# 5. Emergency Coordination Center Layout

The Emergency Coordination Center represents the town’s attempt to organize evacuation and containment during the early outbreak.

This district introduces **more complex interior exploration and puzzle systems**.

---

## Environmental Theme

Emergency operations hub built from municipal buildings.

Features include:

• temporary command rooms  
• communication equipment  
• emergency generators  
• refugee shelters  
• barricaded hallways

This area should feel like a **rapidly assembled crisis response center**.

---

## Major Locations

Entrance Lobby

Initial access point containing evacuation notices and emergency broadcasts.

Operations Room

Large command center with planning maps and emergency equipment.

Communications Wing

Contains damaged radio equipment used in puzzle sequences.

Supply Storage

Contains resources and evidence of failed evacuation planning.

Refugee Shelter

Temporary housing area showing the human side of the outbreak.

---

## Layout Structure

The district is primarily interior-based with interconnected rooms.

Example layout:

```
       Entrance Lobby
            |
     Operations Room
   /               \
Comms Wing     Shelter Area
|
Backup Generator Room
```


The player must restore power to activate communication systems.

---

## Gameplay Focus

Key mechanics introduced here:

• multi-room puzzles  
• power restoration systems  
• document discovery  
• environmental storytelling

Players begin uncovering early reports about the Rot phenomenon.

---

## Encounter Design

Enemy encounters remain moderate but more unpredictable.

Primary enemies:

• Rotters  
• Collapsed Rotters  
• occasional Shadow Stalker

Enemies may emerge from previously quiet rooms after puzzles activate power.

---

# 6. Harbor District Layout

The Harbor District represents the **true beginning of heavy Rot corruption**.

This is where the infection becomes clearly visible in the environment.

---

## Environmental Theme

Industrial fishing harbor.

Features include:

• dock platforms  
• cargo warehouses  
• repair garages  
• cranes and mechanical equipment  
• fishing vessels

Rot growth merges with machinery and marine infrastructure.

---

## Major Locations

Dock Platforms

Open combat areas with fishing vessels and loading cranes.

Warehouse Row

Interior exploration spaces containing storage containers and machinery.

Boat Repair Garage

Workshop used for repairing fishing vessels.

Harbor Control Tower

Provides a high vantage point overlooking the harbor.

---

## Layout Structure

The harbor is divided into several interconnected sections.

Example layout:


```
        Dock Platforms
              |
        Warehouse Row
          /        \
Repair Garage    Control Tower
        |
Coastal Path to Aquarium
```


Vertical walkways between cranes and ship decks add traversal variety.

---

## Environmental Hazards

The harbor contains numerous hazards.

Examples include:

• unstable cranes  
• explosive fuel containers  
• electrified water puddles  
• Rot biomass growth blocking pathways

Players can use hazards strategically during combat.

---

## Encounter Design

Enemy density increases significantly.

Primary enemies include:

• Harbor Rotters  
• Shadow Stalkers  
• Hunter Stalkers

The harbor also contains the **Harbor Bloom Guardian boss encounter**.

---

# 7. Rot Aquarium Layout

The Rot Aquarium is one of the game’s major setpiece locations.

This district introduces **marine Rot organisms**.

---

## Environmental Theme

Flooded marine research and aquarium complex.

Features include:

• shattered aquarium tanks  
• submerged hallways  
• flooded maintenance tunnels  
• broken observation decks

Lighting is dim and visibility is reduced due to water damage.

---

## Major Locations

Main Aquarium Hall

Large tank structures with shattered glass.

Marine Research Wing

Rooms containing Halcyon marine experiment data.

Flooded Maintenance Corridor

Partially submerged passageways requiring careful navigation.

Observation Tunnel

Glass tunnel originally used for underwater viewing.

---

## Layout Structure

The aquarium is primarily interior with water-filled corridors.

Example layout:

```
      Entrance Lobby
            |
    Main Aquarium Hall
       /            \
Research Wing   Observation Tunnel
    |
Flooded Maintenance Corridor
```

Some areas require navigating through shallow water.

---

## Gameplay Focus

The aquarium introduces:

• environmental hazards from flooding  
• limited visibility combat  
• marine Rot organisms

The player also discovers evidence linking marine samples to Halcyon research.

---

# 8. Hospital District Layout

The hospital represents the town’s final attempt to treat infected victims.

This district should feel oppressive and tense.

---

## Environmental Theme

Abandoned medical facility.

Features include:

• emergency wards  
• operating theaters  
• quarantine zones  
• damaged medical equipment

Lighting is minimal and corridors are narrow.

---

## Major Locations

Emergency Entrance

Primary entry point into the hospital.

Patient Wards

Rows of abandoned hospital beds.

Surgical Theater

Room containing surgical equipment and failed medical procedures.

Quarantine Wing

Area used to isolate infected individuals.

Hospital Basement

Storage rooms and pharmaceutical supplies.

---

## Layout Structure

The hospital is divided into multiple floors.

Example layout:

```
        Emergency Entrance
                |
            Reception Hall
            /           \
      Patient Wards   Surgical Theater
            |
    Quarantine Wing
            |
    Basement Storage
```


The basement contains puzzle elements tied to backup power systems.

---

## Gameplay Focus

Hospital gameplay emphasizes:

• tense corridor exploration  
• sudden enemy ambushes  
• puzzle-based progression

The hospital also contains many narrative documents describing the outbreak.

---

## Encounter Design

Enemy types include:

• Medical Rotters  
• Collapsed Rotters  
• Shadow Stalkers

Major encounter:

Spliced Medical Mutation boss.

---

# 9. Forest Region Layout

The Forest Region surrounds Blackwater Cove and forms the natural boundary of the playable map.

This district introduces:

• wildlife enemies  
• larger open environments  
• environmental hazards  
• Rot ecological spread

The forest acts as a transition between the urban environment and the Halcyon research facility.

---

## Environmental Theme

Dense coastal forest.

Features include:

• steep terrain  
• narrow hiking trails  
• fallen trees blocking paths  
• abandoned ranger outposts  
• decaying logging infrastructure

Rot corruption spreads through:

• tree root systems  
• fungal growth structures  
• spiral-shaped Rot formations in soil

---

## Major Locations

Forest Entrance Trail

The first access point from the hospital district.

Ranger Cabin

Safe zone used by hikers and forest rangers before the outbreak.

Observation Tower

Elevated vantage point overlooking the town.

Clearing Arena

Open environment used for the Rot Stag mini-boss encounter.

Collapsed Logging Route

Blocked road leading toward the Halcyon research facility.

---

## Layout Structure

The forest uses natural pathways instead of urban road layouts.

Example structure:

```
        Hospital Exit Trail
                |
            Forest Path
            /           \
    Ranger Cabin    Observation Tower
        |
    Clearing Arena
        |
Logging Route to Research Facility
```

Hidden side trails provide optional exploration.

---

## Gameplay Focus

Forest gameplay emphasizes:

• reduced visibility  
• unpredictable enemy attacks  
• environmental hazards

Players begin encountering stronger enemies here.

---

## Encounter Design

Enemy types include:

• Rot Wolves  
• Hunter Stalkers

Mini-boss encounter:

Rot Stag.

The Rot Stag represents the infection of wildlife ecosystems.

---

# 10. Fishing Trawler Graveyard Layout

The Fishing Trawler Graveyard is a coastal setpiece area.

This location contains the wreckage of multiple fishing vessels that attempted to flee the harbor during the outbreak.

The area creates a maze of ships, docks, and metal walkways.

---

## Environmental Theme

Destroyed fishing fleet.

Features include:

• overturned vessels  
• broken cranes  
• rusted hull structures  
• partially submerged ship interiors

Rot growth merges with mechanical ship structures.

---

## Major Locations

Broken Dockyard

Initial access point from the harbor.

Capsized Trawler

Interior exploration area inside an overturned ship.

Ship Bridge

Elevated control deck used as a navigation point.

Submerged Engine Room

Flooded machinery chamber containing puzzle elements.

---

## Layout Structure

The graveyard emphasizes vertical navigation.

Example layout:


Dockyard Entry
|
Capsized Trawler
|
Ship Deck Walkways
/
Bridge Tower Engine Room
|
Cliff Path to Research Facility


Players traverse ship decks and ladders to navigate the area.

---

## Gameplay Focus

Key gameplay elements include:

• vertical traversal  
• narrow combat spaces  
• environmental hazards

Hazards include:

• unstable metal platforms  
• electrified water  
• collapsing walkways

---

## Encounter Design

Enemy types include:

• Harbor Rotters  
• marine-infected Rot organisms

Encounters often occur in tight spaces where mobility is limited.

---

# 11. Halcyon Marine Research Center Layout

The Halcyon facility represents the most technologically advanced location in the game.

This district reveals the truth behind Halcyon’s Rot research.

---

## Environmental Theme

Modern marine research complex.

Features include:

• glass laboratory spaces  
• containment chambers  
• sterile research equipment  
• underground laboratory corridors

Rot growth spreads through laboratory systems and research chambers.

---

## Major Locations

Reception Lobby

Entry point into the research facility.

Marine Research Labs

Rooms used to analyze biological samples.

Rot Containment Wing

Laboratory chambers used to contain infected specimens.

Security Control Room

Safe zone used by Halcyon security personnel.

Underground Research Elevator

Access point to the final area beneath the facility.

---

## Layout Structure

The research center uses multiple interior floors.

Example structure:


Reception Lobby
|
Research Labs
/
Containment Wing Security Control
|
Underground Elevator


Players gradually uncover Halcyon’s research through documents and environmental storytelling.

---

## Gameplay Focus

The facility introduces:

• high Rot contamination zones  
• advanced enemy variants  
• complex puzzle systems

This district also contains the largest number of narrative documents.

---

# 12. Rot Convergence Chamber Layout

The Rot Convergence Chamber lies beneath the research facility.

This location represents the **core biological structure of the Rot ecosystem**.

---

## Environmental Theme

Ancient subterranean Rot biome.

Features include:

• organic cavern systems  
• spiral-shaped Rot structures embedded in stone  
• pulsating biological growth walls  
• Rot tendrils connecting chambers

The environment appears partially ancient and partially biological.

This suggests that the Rot existed beneath the region long before Halcyon discovered it.

---

## Major Locations

Entry Tunnel

Connection between the research facility and the cavern system.

Outer Rot Cavern

Large chamber filled with biological growth.

Central Convergence Chamber

Final arena where the Rot network is strongest.

---

## Layout Structure

Example structure:


Research Elevator Exit
|
Entry Tunnel
|
Outer Rot Cavern
|
Central Convergence Chamber


The central chamber serves as the final boss arena.

---

## Final Encounter

Dr Victor Soren

Soren merged with the Rot in an attempt to understand its structure.

The boss encounter uses:

• multiple combat phases  
• environmental hazards  
• Rot node destruction mechanics

---

# 13. Encounter Density Scaling

Enemy encounters increase in difficulty as the player progresses through districts.

Example scaling:

Early Game

• small enemy groups  
• basic Rotters

Mid Game

• mixed enemy types  
• Stalker encounters

Late Game

• advanced mutations  
• large multi-enemy encounters

Boss encounters appear at major narrative milestones.

---

# 14. District Difficulty Progression

Each district represents a step in gameplay escalation.

Progression order:

Residential District  
Downtown District  
Emergency Coordination Center  
Harbor District  
Rot Aquarium  
Hospital District  
Forest Region  
Fishing Trawler Graveyard  
Halcyon Research Center  
Rot Convergence Chamber

This progression gradually increases:

• enemy difficulty  
• environmental corruption  
• puzzle complexity

---

# 15. Level Design Goals

District layouts should achieve the following design goals.

---

## Believable Environments

Each district must feel like a real place with logical architecture.

---

## Exploration Incentives

Players should be rewarded for thorough exploration through:

• hidden resources  
• lore documents  
• shortcut routes

---

## Environmental Storytelling

The environment should communicate the story without relying heavily on cutscenes.

Examples include:

• abandoned evacuation attempts  
• failed medical treatment areas  
• destroyed harbor infrastructure

---

## Escalating Horror

The world should gradually transition from a recognizable town to a biological ecosystem dominated by the Rot.

Players should feel that the environment itself is slowly transforming around them.

---