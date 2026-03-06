# Player Controller System

## 1. System Overview

The Player Controller is the core gameplay system responsible for translating player input into character movement, camera control, and interaction with the game world.

It acts as the central interface between the player and the game environment.

The controller manages:

- character movement
- camera control
- interaction triggers
- combat actions
- stealth posture
- animation state transitions
- environmental navigation

All other gameplay systems depend on the Player Controller for input and player state information.

Because of this, the Player Controller must remain **modular, predictable, and easy to extend**.

---

## 2. Design Philosophy

The player controller in ROT is designed around three primary goals.

### Grounded Movement

Movement should feel realistic and weighty rather than fast or arcade-like.

The player should feel vulnerable and cautious while navigating infected environments.

This reinforces the survival horror atmosphere.

---

### Readable Player State

The player character should clearly communicate their current state through animation and movement behavior.

Examples:

- walking vs running
- crouching for stealth
- aiming a weapon
- interacting with objects

Enemy AI and other systems rely on these states to respond correctly.

---

### System Integration

The Player Controller acts as the bridge between player input and other gameplay systems.

It interacts directly with:

- Interaction System
- Combat System
- Stealth System
- Inventory System
- Animation System
- Audio System

The controller does not implement the logic of those systems but instead **triggers them through defined interfaces**.

---

## 3. Core Responsibilities

The Player Controller manages several core gameplay responsibilities.

### Movement Control

Handles character locomotion including:

- walking
- running
- crouching
- directional movement
- obstacle navigation

Movement is constrained by environmental collision and terrain.

---

### Camera Control

Controls the player camera including:

- rotation
- zoom distance
- camera collision avoidance
- aim camera adjustments

Camera positioning must ensure the player can clearly observe the environment while maintaining tension.

---

### Interaction Initiation

The controller detects nearby interactable objects and allows the player to trigger interactions.

Interaction logic itself is handled by the Interaction System.

---

### Combat Input

The controller processes combat input such as:

- aiming
- firing weapons
- reloading
- melee actions

These inputs trigger the Combat System.

---

### Stealth Posture

The controller manages stealth-related player posture.

This includes:

- crouching
- movement speed adjustments
- noise generation

Enemy AI uses this information when determining detection behavior.

---

### Animation State

The Player Controller sends movement and posture information to the animation system.

Examples:

- idle
- walking
- running
- crouching
- aiming

Animations must remain synchronized with gameplay states.

---

## 4. Player Movement

Player movement is the most frequently used functionality of the controller.

Movement should feel deliberate and somewhat constrained to maintain tension.

---

### Basic Movement States

The player may move in several different states.

Idle

The player remains stationary.

Walking

The standard movement speed used during exploration.

Running

A faster movement speed used to escape danger.

Running produces more noise and increases enemy detection risk.

Crouching

A slower movement state used for stealth.

Crouching reduces sound and visibility.

---

### Movement Direction

The player can move in all horizontal directions relative to camera orientation.

Movement directions include:

- forward
- backward
- strafe left
- strafe right
- diagonal movement

Movement speed may vary depending on direction and posture.

---

### Movement Speed

Each movement state has a defined speed.

Example values:

Walking  
Moderate speed for exploration.

Running  
Fast movement used for evasion.

Crouching  
Slow movement designed for stealth.

Final movement values will be tuned during playtesting.

---

### Movement Constraints

Movement is limited by environmental factors such as:

- walls and obstacles
- terrain slopes
- narrow passageways
- environmental hazards

The controller must respect collision systems to prevent clipping through geometry.

---

## 5. Camera System

The camera system determines how the player views the world.

Camera behavior plays a major role in creating atmosphere and tension.

---

### Camera Perspective

ROT uses a **third-person over-the-shoulder camera**.

The camera remains positioned slightly behind and above the player character.

This perspective provides:

- situational awareness
- cinematic framing
- clear visibility during combat

---

### Camera Rotation

The player may rotate the camera horizontally and vertically.

Horizontal rotation controls character orientation.

Vertical rotation adjusts the viewing angle.

Vertical rotation limits prevent unnatural camera angles.

---

### Camera Collision

The camera must avoid passing through environmental objects.

When obstacles block the camera path:

- the camera moves closer to the player
- transparency adjustments may occur

This prevents the player from losing visual control in tight spaces.

---

### Aim Camera Mode

When aiming a weapon, the camera shifts into a more focused view.

Changes include:

- slightly zoomed camera position
- tighter camera framing
- increased aiming precision

This helps players target enemy weak points.

---

## 6. Player States

The Player Controller maintains several player states that affect gameplay behavior.

These states are used by multiple systems.

---

### Exploration State

The default gameplay state.

Player actions include:

- movement
- interaction
- exploration

Most of the game occurs in this state.

---

### Combat State

Activated when the player aims or fires a weapon.

Changes include:

- altered camera positioning
- restricted movement speed
- combat animations

---

### Stealth State

Activated when crouching or attempting to avoid enemies.

This state reduces:

- noise generation
- visual exposure

Enemy AI detection is influenced by stealth state.

---

### Interaction State

Triggered when the player interacts with an object.

Examples:

- opening doors
- collecting items
- solving puzzles

During interactions, player movement may be temporarily restricted.

---

## 7. Controller Architecture

The Player Controller should be implemented as a modular system composed of multiple subcomponents.

Example components may include:

Movement Module

Handles character locomotion.

Camera Module

Manages camera positioning and rotation.

Input Module

Processes player input from keyboard, mouse, or controller.

Interaction Module

Detects nearby interactable objects.

State Manager

Tracks player states such as exploration, combat, or stealth.

This modular structure simplifies debugging and future system expansion.

---

## 8. Input Handling

The Player Controller receives input from the Input System and converts it into gameplay actions.

Input may come from:

- keyboard and mouse
- game controller
- future accessibility input methods

The Player Controller should **never read hardware input directly**.  
Instead, it receives normalized input events from the Input System.

This separation ensures that control schemes can be modified without changing gameplay code.

---

### Input Categories

Player input is divided into several functional categories.

Movement Input

Controls character movement direction.

Camera Input

Controls camera rotation and view direction.

Interaction Input

Triggers interactions with objects.

Combat Input

Controls aiming, firing weapons, and melee attacks.

Utility Input

Controls inventory access, map viewing, and other utility actions.

---

### Example Input Mapping

Movement

- Move Forward
- Move Backward
- Strafe Left
- Strafe Right

Camera

- Rotate Camera Horizontal
- Rotate Camera Vertical

Combat

- Aim Weapon
- Fire Weapon
- Reload Weapon
- Melee Strike

Interaction

- Interact
- Pick Up Item

Utility

- Open Inventory
- Open Map
- Pause Game

Final input mapping may vary depending on platform.

---

## 9. Interaction Detection

The Player Controller is responsible for detecting nearby interactive objects.

This is accomplished through a **forward detection system** originating from the player.

Typical implementation methods include:

- raycasting
- sphere detection
- proximity triggers

The system identifies objects that implement the **Interactable Interface**.

---

### Interaction Priority

When multiple interactable objects are nearby, the system must determine which one receives priority.

Priority may be based on:

- distance to player
- camera direction
- interaction type

Example:

A door directly in front of the player should take priority over an item on a nearby shelf.

---

### Interaction Feedback

When an object can be interacted with, the UI System displays a small prompt.

Example prompts:

"Open Door"

"Pick Up Item"

"Activate Switch"

These prompts should only appear when the object is within interaction range.

---

## 10. Animation Integration

The Player Controller sends movement and state information to the animation system.

The animation system determines which animation should play.

Examples of animation triggers include:

- idle
- walking
- running
- crouching
- aiming
- firing
- interacting
- melee attack

Animations must remain synchronized with gameplay states.

---

### Animation State Parameters

Typical parameters sent to the animation system include:

Movement Speed

Determines whether the player is walking or running.

Movement Direction

Controls directional animations.

Crouch State

Indicates stealth posture.

Combat State

Determines combat animations.

Interaction State

Triggers interaction animations.

---

### Animation Transitions

Transitions between animations must remain smooth to avoid visual glitches.

Examples:

- walk to run
- run to crouch
- aim to fire

Transition timing will be refined during animation implementation.

---

## 11. Player State Transitions

The Player Controller maintains a state machine to track player behavior.

State transitions occur when specific inputs or conditions are triggered.

---

### Example State Transitions

Exploration → Combat

Triggered when the player aims or fires a weapon.

Exploration → Stealth

Triggered when the player crouches.

Exploration → Interaction

Triggered when interacting with an object.

Combat → Exploration

Triggered when the player stops aiming.

Stealth → Exploration

Triggered when the player stands up.

---

### State Conflict Prevention

Certain states cannot occur simultaneously.

Examples:

The player cannot reload while interacting with a puzzle.

The player cannot open inventory while performing a melee attack.

State conflict rules ensure consistent gameplay behavior.

---

## 12. Environmental Navigation

The Player Controller must support navigation through complex environments.

This includes interaction with environmental systems such as:

- doors
- ladders
- narrow passages
- climbable obstacles

These interactions are triggered through the Interaction System.

---

### Environmental Movement Adjustments

Certain environments may modify movement behavior.

Examples include:

Water

Movement speed may be reduced.

Steep Terrain

Movement direction may be restricted.

Confined Spaces

Camera distance may be reduced.

These adjustments maintain immersion and realism.

---

## 13. Failure and Edge Cases

The Player Controller must handle unusual gameplay situations.

Examples include:

Player pushed by enemy attacks.

Player trapped in tight spaces.

Player attempting to interact with unreachable objects.

Camera obstruction by environment.

These situations must fail gracefully without breaking gameplay flow.

---

## 14. Debugging Support

The Player Controller should support debugging tools during development.

Debug features may include:

- movement speed display
- player state visualization
- interaction detection visualization
- camera collision debugging

These tools help developers quickly identify system issues.

---

## 15. System Dependencies

The Player Controller interacts with several other gameplay systems.

These dependencies must be clearly defined.

Interaction System

Handles object interactions.

Combat System

Processes weapon usage and combat mechanics.

Stealth System

Determines enemy detection behavior.

Inventory System

Allows item usage and equipment changes.

Animation System

Handles character animation transitions.

Audio System

Triggers movement sounds and player actions.

UI System

Displays prompts and player status information.

---

## 16. Future Expansion

The Player Controller is designed to support future expansion.

Potential future features include:

Advanced movement abilities.

Environmental traversal mechanics.

Character upgrades affecting movement.

Accessibility movement options.

The modular architecture ensures these features can be added without rewriting core controller logic.

---