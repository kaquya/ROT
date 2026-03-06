# Editor Tools

# 1. Overview

Editor tools are utilities used during development to simplify and accelerate the creation of game content.

These tools exist only inside the development environment and are not included in the final game build.

Editor tools improve development speed by allowing developers to:

- place and modify objects quickly
- configure gameplay systems
- test scenarios rapidly
- visualize game data

Because ROT is a solo-developed project, editor tools must prioritize:

- simplicity
- reliability
- minimal maintenance

Even simple tools can dramatically improve development efficiency.

---

# 2. Purpose of Editor Tools

Editor tools are designed to reduce repetitive tasks.

Examples of repetitive tasks include:

placing large numbers of objects  
configuring enemy spawn points  
testing puzzle triggers  
adjusting lighting settings

Without editor tools, these tasks would take significantly longer.

Editor tools should automate as much manual work as possible.

---

# 3. Types of Editor Tools

Several categories of editor tools may exist.

Level Design Tools

Used to construct environments and place objects.

Enemy Placement Tools

Used to spawn and configure enemies.

Puzzle Configuration Tools

Used to configure puzzle triggers and key items.

Lighting Tools

Used to adjust lighting quickly during development.

Testing Tools

Used to simulate gameplay conditions.

Each category helps improve a specific development workflow.

---

# 4. Level Placement Tools

Level placement tools assist in placing environment objects quickly.

Examples include:

Grid snapping tools  
Object alignment tools  
Batch placement tools

Example workflow:

Select object → choose grid position → place asset.

Level placement tools ensure environments remain aligned with the modular grid system.

---

# 5. Object Spawning Tool

An object spawning tool allows developers to spawn assets quickly inside the scene.

Example uses include:

placing environmental props  
placing enemies  
placing puzzle objects

Example spawn interface:

Spawn Object
Object Type: Enemy
Enemy Type: Rotter
Spawn Location: Selected Position

The tool automatically creates the correct prefab instance.

---

# 6. Enemy Spawn Configuration Tool

Enemy placement can be managed through a spawn configuration tool.

This tool allows developers to:

place enemy spawn points  
select enemy type  
configure spawn conditions

Example configuration:

Spawn Point
Enemy Type: Rotter
Spawn Count: 3
Respawn: Disabled

Spawn tools simplify encounter design.

---

# 7. Puzzle Setup Tool

Puzzle systems may require multiple triggers and objects.

A puzzle setup tool simplifies puzzle configuration.

Example features:

assign key items  
configure puzzle triggers  
define puzzle completion conditions

Example puzzle configuration:

Puzzle: Power Grid Restoration

Required Items:
Fuse A
Fuse B

Completion Result:
Unlock Door

This prevents puzzle logic errors.

---

# 8. Lighting Adjustment Tool

Lighting tools allow developers to quickly adjust environment lighting.

Example features:

adjust brightness  
adjust color temperature  
preview lighting changes in real time

Lighting tools accelerate the environment polish process.

---

# 9. Navigation Visualization Tool

Navigation tools display the navigation mesh used by enemy AI.

This visualization helps ensure that:

enemies can move through environments  
navigation paths are not blocked  
AI movement remains stable

Navigation visualization helps detect level design issues early.

---

# 10. Object Alignment Tools

Alignment tools help ensure assets remain properly placed.

Examples include:

snap to grid  
align to surface  
align rotation

Alignment tools are essential when building modular environments.

They prevent misaligned geometry that can break visual consistency.

---

# 11. Enemy AI Debug Tool

Enemy AI behavior can be complex, so an AI debug tool should be available inside the editor.

The AI debug tool displays real-time information about enemy behavior.

Information displayed may include:

Current AI state  
Target position  
Detection status  
Navigation path

Example debug output:

Enemy: Rotter
State: Chase
Target: Player
Distance: 8.4m

This tool allows developers to quickly verify whether AI logic is functioning correctly.

---

# 12. Enemy Path Visualization

Enemy navigation must be visually inspectable.

The path visualization tool displays the path that an enemy intends to follow.

Example visualization:

Enemy position  
Navigation nodes  
Destination path

This tool helps identify pathfinding issues such as:

blocked navigation routes  
incorrect path selection  
navigation mesh errors

---

# 13. Puzzle Debug Tool

Puzzle systems often involve multiple triggers and objects.

A puzzle debug tool helps visualize puzzle logic.

The tool may display:

active puzzle triggers  
required puzzle items  
puzzle completion state

Example display:

Puzzle: Generator Activation
Trigger A: Active
Trigger B: Inactive
Puzzle State: Incomplete

This allows developers to quickly diagnose puzzle logic errors.

---

# 14. Save State Testing Tool

The save system must be tested regularly.

A save state testing tool allows developers to:

create temporary save points  
reload saves instantly  
test progression logic

Example interface:

Save State
Slot: TestSlot01
Location: Hospital Lobby

This tool allows rapid testing of progression systems.

---

# 15. Encounter Testing Tool

Enemy encounters can be tested using an encounter simulation tool.

The tool allows developers to spawn enemies in controlled conditions.

Example options:

Enemy type  
Enemy count  
Spawn distance

Example interface:

Spawn Enemy Group
Enemy Type: Rotter
Count: 5
Spawn Radius: 10m

This tool helps evaluate combat balance quickly.

---

# 16. Environment Testing Tool

Environment testing tools allow developers to inspect level elements.

Example features include:

collision visualization  
lighting preview  
object bounds display  
trigger volume display

These tools help detect level design issues.

---

# 17. Performance Testing Tool

Performance tools allow developers to monitor game performance inside the editor.

Displayed metrics may include:

frame rate  
CPU usage  
memory usage  
active enemy count

Example display:

FPS: 61
Active Enemies: 7
Draw Calls: 1220
Memory Usage: 2.1GB

Performance tools help detect optimization problems early.

---

# 18. Editor Tool Safety Rules

Editor tools must follow safety guidelines.

Tools should never:

modify save files unintentionally  
delete assets automatically  
alter game progression permanently

Editor tools should only modify temporary development data.

This prevents accidental project corruption.

---

# 19. Tool Access

Editor tools should be accessible through a dedicated development menu.

Example menu structure:

Developer Tools
├── Enemy Tools
├── Puzzle Tools
├── Environment Tools
├── Save Tools
└── Performance Tools

Organizing tools into categories improves usability.

---

# 20. Tool Documentation

All editor tools must be documented clearly.

Documentation should include:

tool purpose  
how to use the tool  
limitations of the tool

Proper documentation ensures tools remain usable throughout development.

---

# 21. Tool Validation

Before editor tools are used regularly, they must be validated.

Validation checks include:

correct functionality  
no unintended side effects  
stable behavior during gameplay testing

Reliable editor tools significantly accelerate development.

---