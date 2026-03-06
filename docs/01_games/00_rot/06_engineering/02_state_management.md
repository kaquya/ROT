# State Management

## 1. Overview

The State Management System controls the global state of the game.

It determines:

- what the player is currently doing
- which gameplay systems are active
- which UI elements are visible
- which audio layers should be playing
- how input is interpreted

The system ensures that gameplay flows smoothly between different modes such as exploration, combat, menus, and cutscenes.

Without structured state management, systems could conflict with one another.

---

# 2. Core State Types

The game operates using several high-level states.

These states represent the major modes of the game.

Examples include:

Main Menu  
Gameplay  
Combat  
Boss Encounter  
Paused  
Cutscene  
Game Over

Each state activates and deactivates specific systems.

---

# 3. State Manager

The **Game State Manager** is responsible for controlling state transitions.

Responsibilities include:

- tracking the current state
- triggering transitions between states
- enabling and disabling systems
- notifying other systems when state changes occur

Example structure:

GameStateManager
{
currentState
previousState
stateStack[]
}

### Field Descriptions

currentState  
Active state.

previousState  
The state that was active before the current state.

stateStack  
Stack of temporary states such as pause menus.

---

# 4. State Transition Rules

State transitions must follow strict rules to avoid invalid transitions.

Example valid transitions:

MainMenu → Gameplay
Gameplay → Combat
Combat → Gameplay
Gameplay → BossEncounter
BossEncounter → Gameplay
Gameplay → Pause
Pause → Gameplay

Invalid transitions must be prevented.

Example:

MainMenu → Combat

The player cannot enter combat from the main menu.

---

# 5. Gameplay State

Gameplay is the primary state where the player explores the world.

Active systems include:

- Player Controller
- Enemy AI
- Puzzle System
- Interaction System
- Inventory System
- Audio System
- UI HUD

During this state the player can:

- explore environments
- interact with objects
- fight enemies
- collect items

---

# 6. Combat State

Combat state activates when enemies actively engage the player.

Additional behaviors include:

- combat music activation
- enemy aggression increase
- UI combat indicators

Combat state is triggered by events such as:

enemy detecting player  
player attacking enemy  
scripted encounters

Combat state ends when all enemies disengage.

---

# 7. Boss Encounter State

Boss encounters represent special gameplay states.

Additional behaviors include:

- boss introduction animation
- boss health bar activation
- arena locking

During boss encounters:

- escape routes are disabled
- boss music activates
- enemy AI uses boss logic

The state ends when the boss is defeated.

---

# 8. Pause State

Pause state occurs when the player opens the pause menu.

During pause state:

- gameplay systems freeze
- physics simulation pauses
- AI updates stop

Active systems include:

- UI System
- Menu Navigation
- Settings

When the pause menu closes, the game returns to the previous state.

---

# 9. Cutscene State

Cutscenes temporarily override player control.

During cutscenes:

- player input is disabled
- camera may be controlled by scripted sequences
- UI elements may be hidden

Cutscenes often occur during:

story events  
boss introductions  
major discoveries

After the cutscene ends, gameplay resumes.

---

# 10. Game Over State

The Game Over state occurs when the player's health reaches zero.

During this state:

- gameplay systems stop
- death animation plays
- UI displays failure message

The player may then choose to:

reload last save  
return to main menu

This state ensures a controlled reset of gameplay.

# 11. State Stack System

Some states temporarily override the current gameplay state without permanently replacing it.

For this purpose the system uses a **state stack**.

The stack allows temporary states such as pause menus or dialogue to overlay gameplay.

Example stack behavior:

Gameplay
↓
PauseMenu

State stack example:

StateStack
[
Gameplay,
PauseMenu
]

When the PauseMenu closes, it is removed from the stack and the system returns to the previous state.

Stack operations include:

Push State  
Adds a temporary state.

Pop State  
Removes the top state.

Peek State  
Reads the currently active state.

---

# 12. Event-Driven State Changes

State transitions are triggered through gameplay events.

Example event triggers:

EnemyDetectedPlayer → Enter Combat State
BossIntroTriggered → Enter Boss Encounter State
PauseButtonPressed → Push Pause State
PlayerHealthZero → Enter Game Over State

The Event System sends signals to the Game State Manager, which then validates and executes the transition.

This keeps state logic centralized and predictable.

---

# 13. Input Routing

The Input System must route input differently depending on the active state.

Example input behavior:

Gameplay State

- movement input active
- combat input active
- interaction input active

Pause State

- gameplay input disabled
- menu navigation enabled

Cutscene State

- player input disabled
- skip cutscene input enabled

Input routing prevents unintended player actions during restricted states.

---

# 14. System Activation Rules

Each system activates only during specific states.

Example:

Player Controller
Active: Gameplay, Combat
Inactive: Pause, Cutscene

Enemy AI
Active: Gameplay, Combat
Inactive: Pause, Menu

UI HUD
Active: Gameplay, Combat, BossEncounter
Inactive: Cutscene, MainMenu

This prevents systems from executing when they should be inactive.

---

# 15. State Persistence

The Save System must record certain state information.

Example saved states:

currentDistrict
playerPosition
storyProgress

Temporary states such as pause menus should not be saved.

Upon loading a save file the game should always return to the **Gameplay State**.

---

# 16. State Conflict Prevention

The State Manager must prevent conflicting states.

Examples of conflicts:

Gameplay and Pause active simultaneously.

Combat and Main Menu active simultaneously.

To prevent this, the State Manager validates transitions before applying them.

Invalid transitions should be rejected.

---

# 17. State Transition Safety

All transitions should follow a consistent pattern.

Typical transition flow:

1. Validate transition
2. Exit current state
3. Initialize new state
4. Notify subscribed systems
5. Activate new state

This ensures clean state changes.

Example pseudocode:

if (StateManager.CanTransition(targetState))
{
ExitState(currentState)
EnterState(targetState)
}

---

# 18. System Notifications

When states change, systems must be notified.

Example notifications:

OnStateEnter(Gameplay)
OnStateExit(Gameplay)
OnStateEnter(Pause)

Systems may respond by enabling or disabling behaviors.

Example:

UI System displays pause menu when Pause State begins.

---

# 19. Debugging State Management

Development builds should include debugging tools for monitoring state behavior.

Examples include:

State Viewer  
Displays the current active state.

State History  
Shows recent state transitions.

Force State Change  
Allows developers to manually change states.

State Conflict Warnings  
Displays alerts when invalid transitions occur.

These tools help identify logic errors during development.

---

# 20. Future State Expansion

The architecture must support additional gameplay states if needed.

Possible future states include:

Dialogue State  
Used during interactive conversations.

Photo Mode State  
Used during screenshot capture.

Multiplayer State  
If cooperative gameplay is added in future projects.

State expansion should not require major changes to the architecture.

The modular state system ensures that new states can be introduced safely.

---