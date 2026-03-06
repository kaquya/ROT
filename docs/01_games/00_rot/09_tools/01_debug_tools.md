# Debug Tools

# 1. Overview

Debug tools are utilities used during development to inspect game systems while the game is running.

Unlike editor tools, which operate during level creation, debug tools operate during gameplay.

Debug tools help developers identify problems with:

- gameplay systems
- enemy behavior
- player interactions
- performance issues
- audio events
- puzzle logic

Because ROT is a solo-developed project, debug tools must remain simple but powerful enough to diagnose problems quickly.

---

# 2. Purpose of Debug Tools

Debug tools allow developers to:

inspect system behavior  
visualize hidden game data  
detect incorrect system states  
identify performance bottlenecks

Without debug tools, diagnosing complex gameplay issues becomes extremely difficult.

Debug tools improve development efficiency and reduce troubleshooting time.

---

# 3. Debug Mode

The game should include a special **debug mode** that enables debugging features.

Debug mode may be activated through:

developer key shortcut  
debug build configuration  
developer console command

Example debug activation:

F10 → Toggle Debug Mode

When debug mode is active, additional overlays and information become visible.

---

# 4. Debug Overlay

The debug overlay displays useful information on screen.

Typical debug overlay information includes:

current frame rate  
player position  
active enemies  
system states

Example overlay display:

FPS: 61
Player Position: (34.2, 1.8, -12.5)
Active Enemies: 6
Current District: Hospital

This information helps developers monitor gameplay conditions.

---

# 5. Player Debug Information

Player debug tools display information about the player state.

Example data includes:

player health  
equipped weapon  
current inventory items  
movement speed  
interaction state

Example display:

Player Health: 78
Weapon: Shotgun
Ammo: 6 / 24
Movement State: Running

This helps diagnose gameplay system issues.

---

# 6. Enemy Debug Information

Enemy debug tools display information about enemy behavior.

Example information includes:

enemy type  
current AI state  
target position  
distance to player  
health value

Example display:

Enemy: Rotter
State: Searching
Health: 35
Distance to Player: 12m

Enemy debug tools help verify that AI systems function correctly.

---

# 7. AI State Visualization

AI behavior relies on state machines.

Debug tools should display the current AI state for enemies.

Example states include:

Idle  
Patrol  
Suspicious  
Search  
Chase  
Attack

Displaying the current state allows developers to confirm correct behavior transitions.

---

# 8. Detection Radius Visualization

Enemy perception systems may include detection ranges.

Debug tools can display detection areas visually.

Example:

circle showing enemy sight range  
cone showing enemy field of view

Visualization helps ensure detection ranges are balanced.

---

# 9. Navigation Mesh Visualization

Enemy navigation depends on the navigation mesh.

Debug tools should allow the navigation mesh to be displayed.

Example features include:

walkable areas  
blocked areas  
navigation links

Navigation mesh visualization helps identify pathfinding issues.

---

# 10. Trigger Volume Visualization

Gameplay triggers are often invisible during normal gameplay.

Debug tools should allow trigger volumes to be displayed.

Examples include:

puzzle triggers  
enemy spawn triggers  
cutscene triggers

Visualizing triggers helps detect incorrect trigger placement.

---

# 11. Performance Debugging

Performance debugging tools allow developers to monitor how the game performs during runtime.

These tools display real-time metrics related to system performance.

Typical metrics include:

Frame rate (FPS)  
Frame time  
CPU usage  
Memory usage  
Active enemy count  
Active audio sources

Example debug output:

FPS: 58
Frame Time: 17.2 ms
CPU Usage: 42%
Active Enemies: 7
Memory Usage: 2.4 GB

Monitoring these values helps detect performance problems early.

---

# 12. Frame Time Analysis

Frame time represents how long it takes to render a single frame.

Target frame time:

16.67 ms (for 60 FPS)

If frame time exceeds this value consistently, the game may feel unstable.

Debug tools should allow frame time graphs to be displayed during gameplay.

Example visualization:

Frame Time Graph
|■■■■■■■■■■■■■■■■■■■■|

Frame time spikes often indicate performance bottlenecks.

---

# 13. Audio Debugging

Audio systems can sometimes fail silently.

Audio debug tools should display:

Active audio sources  
Audio event triggers  
Audio channel usage

Example display:

Active Audio Sources: 14
Music Track: MUS_ForestAmbience
Last Triggered Event: EnemyAttack_Rotter

These tools help identify missing or incorrectly triggered sounds.

---

# 14. Event Logging

The game should maintain a runtime event log.

The event log records important system events.

Examples include:

enemy spawn events  
puzzle completion triggers  
player death events  
save/load operations

Example log entry:

[12:45:22] EnemySpawn: Rotter (Downtown)

Event logs help identify the sequence of actions that led to a bug.

---

# 15. Error Logging

Errors encountered during runtime must be logged automatically.

Examples include:

missing asset references  
null object references  
AI pathfinding failures

Example error log:

ERROR: Enemy pathfinding failed (NavMesh missing)

Error logging helps diagnose issues that may not be visible during gameplay.

---

# 16. Debug Console

The debug console allows developers to execute commands during gameplay.

Example console commands:

spawn_enemy rotter
give_weapon shotgun
teleport hospital
toggle_ai

Console commands allow rapid testing of gameplay systems.

The console should only be available in development builds.

---

# 17. Camera Debug Tools

Camera debugging tools allow developers to inspect camera behavior.

Features may include:

free camera movement  
camera position display  
field-of-view adjustments

Example debug display:

Camera Position: (12.4, 2.1, -8.9)
FOV: 75

These tools help diagnose camera issues.

---

# 18. Collision Visualization

Collision debugging tools display collision boundaries.

Example visualization:

Bounding boxes around environment objects  
Collision volumes for enemies  
Player collision capsule

Collision visualization helps detect issues such as:

players getting stuck in geometry  
incorrect collision shapes

---

# 19. Development Shortcuts

Debug tools may include keyboard shortcuts for rapid testing.

Examples include:

F1 → Toggle Debug Overlay
F2 → Toggle AI Debug
F3 → Toggle Navigation Mesh
F4 → Toggle Collision View

Shortcuts allow developers to access debugging tools quickly.

---

# 20. Debug Tool Safety

Debug tools must not affect the final game build.

All debug features must be disabled in release builds.

Examples of debug-only features:

developer console  
debug overlays  
cheat commands  
AI state visualization

Removing debug tools from the final build prevents players from accessing development functionality.

---

# 21. Debugging Philosophy

Debugging tools should prioritize:

clarity  
simplicity  
usefulness

Debug systems should provide enough information to identify issues without overwhelming the developer.

Well-designed debugging tools significantly improve development efficiency.

They allow problems to be diagnosed quickly and accurately during gameplay testing.

---