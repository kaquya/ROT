# Enemy AI System

## 1. System Overview

The Enemy AI System controls how hostile organisms behave in the world of ROT.

The system determines how enemies:

- perceive the player
- react to sound and movement
- patrol environments
- hunt targets
- attack or retreat
- cooperate with nearby organisms

Rather than relying on scripted encounters, the system uses **state-based behavior logic** to allow enemies to react dynamically to player actions.

This approach creates encounters that feel unpredictable and tense.

Enemies are not simply obstacles. They behave as organisms within the Rot ecosystem.

---

## 2. Design Philosophy

Enemy AI behavior follows several core design principles.

### Environmental Awareness

Enemies react to disturbances in their environment.

Examples include:

- player movement
- weapon fire
- broken objects
- environmental hazards

This ensures that exploration always carries risk.

---

### Unpredictability

Enemy behavior should feel organic rather than robotic.

Even familiar enemies may react differently depending on player actions.

This keeps encounters tense and unpredictable.

---

### Ecosystem Behavior

Enemies do not behave like soldiers.

They behave like organisms responding to threats.

Examples include:

- predators stalking prey
- scavengers investigating noise
- groups responding collectively to danger

This reinforces the biological theme of the Rot.

---

## 3. AI State Machine

Enemy behavior is governed by a state machine.

Each enemy exists in one of several possible states.

These states determine the enemy’s actions and transitions.

---

### Core AI States

Idle

The enemy is inactive or wandering slowly.

This state occurs when no disturbances are detected.

---

Patrol

The enemy follows a predefined route or area.

Patrol behavior is common for roaming predators.

---

Suspicious

The enemy has detected a disturbance but has not confirmed the player’s location.

Examples include:

- hearing a noise
- noticing movement in the distance

The enemy investigates the disturbance.

---

Searching

The enemy actively searches for the player after detecting suspicious activity.

During this state the enemy scans nearby areas.

---

Aggressive

The enemy has confirmed the player’s presence and begins attacking.

This state triggers combat behavior.

---

Return

If the player escapes detection, the enemy gradually returns to its patrol area.

---

## 4. Detection Systems

Enemies detect the player using sensory systems.

Two primary detection types exist.

---

### Visual Detection

Enemies can detect the player through line-of-sight.

Factors affecting visual detection include:

Distance

Closer targets are easier to detect.

Lighting

Dark environments make detection harder.

Movement

Running characters are easier to detect than stationary ones.

Posture

Crouching reduces visibility.

---

### Sound Detection

Enemies react to sounds produced by the player.

Examples of noise sources include:

- running
- weapon fire
- melee impacts
- breaking objects
- interacting with machinery

Louder sounds travel further and attract more enemies.

---

## 5. Detection Range

Each enemy type has detection ranges that define how far they can perceive disturbances.

Examples include:

Visual Range

Maximum distance the enemy can see.

Sound Range

Maximum distance the enemy can hear.

Peripheral Vision

Angle of vision around the enemy.

These values vary between enemy types.

For example:

Stalkers may have higher visual awareness.

Rotters may rely more heavily on sound.

---

## 6. Investigation Behavior

When a disturbance is detected, enemies may investigate the source.

Examples include:

approaching the location of a sound  
scanning nearby areas  
checking hiding spots  

If the player remains hidden during investigation, the enemy may eventually abandon the search.

---

## 7. Patrol Behavior

Some enemies patrol specific areas of the environment.

Patrol routes may include:

- corridors
- streets
- rooms
- forest paths

Patrol behavior ensures that the environment remains dynamic rather than static.

Players may observe patrol routes and time their movements accordingly.

---

## 8. Attack Behavior

When an enemy enters the aggressive state, it attempts to attack the player.

Attack patterns vary depending on enemy type.

Examples include:

melee strikes  
lunging attacks  
rapid pursuit  
area attacks  

Enemies may also reposition during combat to maintain pressure.

---

## 9. Target Tracking

When pursuing the player, enemies track the player’s last known location.

If the player breaks line-of-sight, enemies may:

- continue moving toward the last known position
- search nearby areas
- investigate noise disturbances

This prevents enemies from instantly losing the player when hiding behind obstacles.

---

## 10. Movement Behavior

Enemy movement must respect environmental navigation.

Enemies should be able to:

- move around obstacles
- navigate rooms and corridors
- pursue the player through open areas

Navigation systems such as **navigation meshes** are typically used to support this behavior.

Movement speed varies by enemy type.

For example:

Stalkers move quickly and aggressively.

Rotters move slowly but may attack in groups.

---

## 11. Group Behavior

Certain enemy types operate in groups rather than individually.

Group behavior increases combat pressure and prevents the player from easily isolating enemies.

Examples include:

- multiple Rotters responding to nearby combat
- scavenger organisms converging on the same disturbance
- predators coordinating pursuit of the player

When one enemy detects the player, nearby enemies may enter an elevated awareness state.

This may trigger:

- investigation behavior
- group pursuit
- coordinated attacks

The distance at which enemies alert each other varies depending on enemy type.

---

## 12. Ambush Behavior

Some enemy types specialize in ambush tactics.

These enemies remain hidden until the player enters a specific area.

Examples include:

Collapsed Rotters hiding in confined spaces  
Shadow Stalkers waiting in dark rooms  
creatures concealed behind environmental obstacles

Ambush enemies typically remain dormant until triggered.

Once activated, they transition immediately into aggressive behavior.

Ambush behavior increases tension during exploration.

Players must remain cautious when entering unfamiliar areas.

---

## 13. Stealth Interaction

Enemy AI must respond to the player’s stealth behavior.

Stealth mechanics influence detection probability.

Factors that reduce detection include:

- crouching movement
- moving slowly
- remaining in dark environments
- using environmental cover

Factors that increase detection include:

- running
- firing weapons
- interacting with loud machinery
- entering enemy field-of-view

Enemies may also investigate disturbances without fully detecting the player.

This creates opportunities for stealth-based gameplay.

---

## 14. Environmental Navigation

Enemy movement relies on environmental navigation systems.

Typically this is implemented using **navigation meshes**.

Navigation systems allow enemies to:

- move around obstacles
- follow the player through complex environments
- patrol defined areas

Navigation must support both indoor and outdoor environments.

Enemies should also respect environmental barriers such as:

- locked doors
- blocked passages
- environmental hazards

---

## 15. Pathfinding Behavior

Pathfinding determines how enemies reach their target location.

Typical behaviors include:

Direct Pursuit

Enemies attempt to move directly toward the player.

Obstacle Avoidance

Enemies adjust their path when encountering environmental barriers.

Search Patterns

Enemies move through nearby locations while searching for the player.

These behaviors ensure enemies remain believable and functional within complex environments.

---

## 16. Enemy Memory System

Enemies maintain short-term memory of player activity.

This allows enemies to continue searching for the player even after losing direct sight.

Examples include:

remembering the player's last known position  
remembering recent noise sources  
remembering combat disturbances

Memory duration varies by enemy type.

For example:

Stalkers may track the player longer.

Rotters may abandon the search more quickly.

---

## 17. Retreat and Disengagement

Certain enemies may disengage from combat if the player escapes.

Examples include:

the player outruns the enemy  
the player hides successfully  
the enemy loses visual and audio contact

In these cases enemies transition into:

Searching → Return → Idle

This prevents enemies from pursuing the player indefinitely.

---

## 18. Environmental Awareness

Enemies respond to environmental events beyond player actions.

Examples include:

explosions  
falling structures  
environmental hazards  
other creatures moving nearby

These disturbances may trigger investigation behavior.

Environmental awareness helps make the world feel reactive and alive.

---

## 19. Enemy Reaction to Damage

When enemies receive damage, their behavior may change.

Examples include:

entering an aggressive state  
staggering temporarily  
retreating briefly  
calling nearby enemies

Damage reactions vary depending on enemy type and severity of damage.

Weak point hits may produce stronger reactions.

---

## 20. Performance Constraints

Enemy AI must be optimized for stable performance.

Typical encounter sizes should remain limited.

Examples include:

1–3 enemies in confined areas  
1 elite enemy guarding a location  
occasional group encounters

Limiting enemy counts ensures AI systems remain performant on a wide range of hardware.

---

## 21. Debugging Tools

Development builds should include AI debugging tools.

Examples include:

AI state display  
shows the current state of each enemy

detection radius visualization  
displays visual and sound detection ranges

navigation path display  
shows calculated pathfinding routes

These tools allow developers to quickly diagnose AI behavior issues.

---

## 22. System Dependencies

The Enemy AI System interacts with several other gameplay systems.

Player Controller

Provides player position and movement data.

Stealth System

Determines how easily enemies detect the player.

Combat System

Handles enemy attack behavior and damage interactions.

Navigation System

Supports pathfinding through environments.

Audio System

Detects noise events generated by the player.

Animation System

Triggers enemy animations for movement and attacks.

---

## 23. Future Expansion

The AI system is designed to support future gameplay features.

Possible expansions include:

advanced predator behavior  
environment-based hunting patterns  
dynamic ecosystem interactions  
enemy territorial control systems

The modular state-based architecture ensures these features can be added without rewriting the entire AI system.

---