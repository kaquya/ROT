# AI State Machine

## 1. Overview

Enemy behavior in ROT is controlled through a **Finite State Machine (FSM)**.

A state machine organizes enemy behavior into clearly defined states and transitions.

Each enemy can exist in only **one state at a time**, but may transition between states based on:

- player detection
- damage received
- environmental triggers
- scripted events

The AI State Machine ensures that enemy behavior remains predictable, testable, and maintainable.

This approach is ideal for a solo-developed project because it keeps logic simple and debuggable.

---

# 2. State Machine Architecture

Each enemy instance contains its own state machine.

Example structure:

EnemyAI
{
currentState
previousState
target
awarenessLevel
}

The state machine continuously updates every frame.

State transitions occur when specific conditions are met.

---

# 3. Core AI States

All enemy types share several common states.

These states define baseline behavior.

---

## Idle State

The enemy remains inactive.

Typical behavior:

- standing still
- performing idle animations
- minimal awareness of environment

The enemy may transition to other states if stimuli are detected.

Possible transitions:

Idle → Patrol  
Idle → Suspicious

---

## Patrol State

The enemy moves between predefined patrol points.

Behavior includes:

- walking along a route
- scanning the environment
- listening for sounds

Possible transitions:

Patrol → Suspicious  
Patrol → Attack

---

## Suspicious State

Triggered when the enemy detects something unusual.

Examples include:

- hearing a noise
- seeing brief player movement
- discovering a dead enemy

Behavior includes:

- investigating the area
- moving toward the sound source
- increased awareness

Possible transitions:

Suspicious → Search  
Suspicious → Attack  
Suspicious → Idle

---

## Search State

The enemy actively searches for the player.

Behavior includes:

- moving toward the last known player position
- scanning the surrounding area
- increased alertness

Possible transitions:

Search → Attack  
Search → Patrol

---

## Attack State

The enemy engages the player.

Behavior includes:

- moving toward the player
- performing attacks
- coordinating with nearby enemies

Possible transitions:

Attack → Search  
Attack → Idle (if player escapes)

---

## Stunned State

Triggered when the enemy receives heavy damage.

Behavior includes:

- temporary immobilization
- vulnerability to additional damage

Possible transitions:

Stunned → Attack  
Stunned → Idle

---

# 4. Boss AI States

Boss enemies use additional states beyond standard enemies.

Examples include:

Intro State  
Plays boss introduction sequence.

Phase Transition  
Triggers new boss phase.

Special Ability  
Boss performs unique attacks.

Enrage State  
Boss behavior becomes more aggressive.

Boss states follow the same state machine logic but include additional scripted behavior.

---

# 5. State Transition Conditions

Transitions occur when conditions are met.

Examples include:

if playerDetected → Attack
if noiseDetected → Suspicious
if health < threshold → Enrage
if playerLost → Search

Transitions must always follow valid state rules.

Invalid transitions must be prevented.

---

# 6. AI Perception System

Enemy perception drives most state transitions.

Perception uses two primary senses.

---

## Vision

Enemies detect the player using a vision cone.

Vision detection depends on:

- player position
- enemy facing direction
- distance
- lighting conditions

Example structure:

VisionCone
{
angle
range
}

Players outside the cone remain undetected.

---

## Hearing

Enemies detect sound events.

Examples include:

- gunshots
- running footsteps
- object collisions

Example sound event:

SoundEvent
{
position
intensity
}

Enemies within hearing range react to the sound.

---

# 7. Awareness Level

Enemies track an awareness meter representing how close they are to detecting the player.

Example structure:

Awareness
{
value
threshold
}

Stages:

Low Awareness  
Enemy notices minor disturbances.

Medium Awareness  
Enemy becomes suspicious.

High Awareness  
Enemy enters combat state.

This system prevents instant detection.

---

# 8. Target Tracking

Once the player is detected, the enemy stores the player's last known position.

Example structure:

TargetData
{
targetID
lastKnownPosition
}

If the player escapes, enemies move toward the last known location.

If the player is not rediscovered, enemies eventually return to patrol.

---

# 9. Group AI Behavior

Some enemies coordinate behavior.

Group AI allows enemies to:

- alert nearby enemies
- converge on player position
- attack from multiple angles

Example communication event:

EnemyAlert
{
sourceEnemy
alertRadius
}

Enemies within the radius receive the alert.

---

# 10. State Update Loop

Enemy AI runs an update loop every frame.

Example update sequence:

Process perception

Update awareness

Evaluate transitions

Execute current state behavior

Apply movement or attacks

This loop ensures enemies respond dynamically to player actions.

---

# 11. Pathfinding System

Enemy movement is controlled through a pathfinding system.

The system allows enemies to navigate around obstacles and follow the player through the environment.

Recommended approach:

Navigation Mesh (NavMesh)

A navigation mesh defines walkable areas of the level.

Enemies can:

- follow paths
- avoid obstacles
- navigate complex environments
- chase the player

Example path request:

PathRequest
{
startPosition
targetPosition
}

The navigation system returns a path composed of movement nodes.

Enemies follow these nodes until the target is reached or the target position changes.

---

# 12. Movement Behavior

Enemy movement speed depends on the current state.

Example movement rules:

Idle State  
No movement.

Patrol State  
Slow walking speed.

Suspicious State  
Moderate movement speed.

Search State  
Moderate movement with scanning behavior.

Attack State  
Fast pursuit movement.

Movement speed should be configurable for each enemy type.

Example configuration:

EnemyMovementConfig
{
patrolSpeed
chaseSpeed
searchSpeed
}

---

# 13. Combat Decision Logic

During combat, enemies must choose between different attack behaviors.

Decision logic may include:

distance to player  
line of sight  
cooldown timers  
current phase (for bosses)

Example decision structure:

if distance < meleeRange → performMeleeAttack
if distance > meleeRange → moveTowardPlayer
if attackCooldownActive → reposition

This logic ensures enemies behave strategically rather than randomly.

---

# 14. Stealth Detection

Stealth detection uses both vision and sound systems.

Enemies gradually detect the player rather than instantly reacting.

Example stealth detection stages:

Undetected  
Enemy unaware of player.

Suspicious  
Enemy heard something or saw movement.

Searching  
Enemy actively investigating.

Alerted  
Enemy has detected the player.

The Awareness System manages these transitions.

Stealth allows players to:

- bypass encounters
- perform surprise attacks
- avoid wasting resources

---

# 15. Attack Execution

When attacking, enemies execute predefined attack actions.

Attack execution includes:

- attack animation
- damage calculation
- hit detection
- recovery time

Example attack structure:

AttackAction
{
attackType
damage
range
cooldown
}

Examples of attack types:

- melee strike
- grab attack
- leap attack
- ranged projectile (rare enemies)

---

# 16. Boss AI Extensions

Boss AI uses an extended state machine.

Boss-specific states include:

Intro State  
Boss introduction animation.

Phase State  
Boss uses abilities specific to the current phase.

Special Attack State  
Boss executes unique scripted abilities.

Enrage State  
Boss becomes more aggressive after health threshold.

Boss AI may also control environmental elements within the arena.

Example:

- spawning enemies
- activating hazards
- destroying structures

---

# 17. AI Cooldowns

Enemy abilities should use cooldown timers.

Cooldowns prevent enemies from spamming attacks.

Example cooldown structure:

AbilityCooldown
{
abilityID
cooldownDuration
currentTimer
}

Cooldown timers ensure predictable and fair combat behavior.

---

# 18. Performance Optimization

AI systems must be optimized to avoid performance issues.

Recommended strategies include:

AI Update Throttling  
Some AI calculations occur less frequently.

Distance-Based Activation  
Enemies far from the player become inactive.

Sleep States  
Enemies outside active areas stop updating.

Group AI Batching  
Nearby enemies share perception updates.

These optimizations reduce CPU usage.

---

# 19. AI Debugging Tools

Development builds should include AI debugging tools.

Examples include:

AI State Viewer  
Displays the current state of each enemy.

Vision Cone Visualizer  
Shows enemy vision detection ranges.

Pathfinding Debug Lines  
Displays navigation paths.

Awareness Meter Viewer  
Displays enemy awareness levels.

Enemy Target Display  
Shows which target an enemy is tracking.

These tools help developers diagnose AI behavior problems.

---

# 20. AI System Integration

The AI system interacts with several other gameplay systems.

Player Controller  
AI tracks player position and actions.

Combat System  
AI attacks and receives damage.

Audio System  
AI reacts to sound events.

Puzzle System  
AI may guard puzzle areas.

State Management  
AI may change behavior based on game state.

UI System  
Debug UI may display AI state information.

---

# 21. AI Configuration Data

Enemy behavior should be configurable through data rather than hardcoded logic.

Example configuration file:

EnemyConfig
{
detectionRange
visionAngle
patrolSpeed
chaseSpeed
attackDamage
}

Data-driven AI allows easy balancing and adjustments.

---

# 22. Future AI Expansion

The AI architecture should support future improvements.

Possible expansions include:

advanced squad coordination  
dynamic enemy behaviors  
adaptive difficulty AI  
procedural enemy encounters

The AI system should remain modular to support these features.

---