# Input System

## 1. Overview

The Input System is responsible for capturing and processing player input.

It converts raw input signals from devices into gameplay actions.

Supported input devices include:

- keyboard
- mouse
- game controllers

The input system must support:

- real-time gameplay input
- menu navigation
- input rebinding
- input buffering
- state-based input routing

Input must remain responsive and predictable during all gameplay situations.

---

# 2. Input Architecture

The input system converts **physical inputs** into **game actions**.

Example pipeline:

Input Device
↓
Input Mapping
↓
Action Events
↓
Gameplay Systems

Example:

Keyboard Key W
↓
MoveForward Action
↓
Player Controller Movement

This abstraction allows different devices to trigger the same actions.

---

# 3. Input Action Mapping

All inputs are mapped to actions.

Example structure:

InputAction
{
actionName
primaryBinding
secondaryBinding
}

Example mappings:

MoveForward → W / LeftStickUp
MoveBackward → S / LeftStickDown
Interact → E / ControllerButtonX
Attack → MouseLeft / ControllerTrigger
Reload → R / ControllerButtonY

Using action mapping allows easy rebinding.

---

# 4. Input Categories

Input actions are grouped into categories.

---

## Movement Inputs

Used to control player movement.

Examples:

MoveForward  
MoveBackward  
MoveLeft  
MoveRight  
Sprint

---

## Combat Inputs

Used during combat.

Examples:

Attack  
Aim  
Reload  
SwitchWeapon

---

## Interaction Inputs

Used for interacting with the world.

Examples:

Interact  
UseItem  
PickUpItem

---

## Menu Inputs

Used when navigating UI.

Examples:

MenuConfirm  
MenuBack  
MenuNavigateUp  
MenuNavigateDown

---

# 5. Input Contexts

Input behavior changes depending on the game state.

Contexts ensure that inputs perform appropriate actions.

Example contexts:

Gameplay Context  
Menu Context  
Cutscene Context

---

## Gameplay Context

Active during normal gameplay.

Active inputs include:

movement  
combat  
interaction

---

## Menu Context

Active when menus are open.

Gameplay input is disabled.

Active inputs include:

menu navigation  
menu confirmation  
menu back

---

## Cutscene Context

Active during cinematic sequences.

Most player inputs are disabled.

Possible active inputs:

skip cutscene

---

# 6. Input Buffering

Input buffering stores player inputs for a short time.

This helps ensure responsive controls during rapid gameplay.

Example:

Player presses attack slightly before animation finishes.

Buffered input triggers the attack immediately after recovery.

Example buffer structure:

InputBuffer
{
action
timestamp
}

Buffered inputs expire after a short duration.

---

# 7. Input Polling

Input must be checked every frame.

Typical process:

Read device inputs

Convert to actions

Send actions to systems

Polling frequency must match the game's frame rate.

---

# 8. Controller Support

The system must support modern game controllers.

Controller inputs include:

analog stick movement  
trigger inputs  
face buttons  
shoulder buttons

Controller mappings must match console-style layouts.

Example:

LeftStick → Movement
RightStick → Camera
RT → Attack
LT → Aim

---

# 9. Analog Input Handling

Analog sticks allow continuous input values.

Example range:

-1.0 to 1.0

Used for:

movement speed  
camera rotation  
aim precision

Dead zones must be applied to prevent unintended movement.

Example:

deadZone = 0.15

Values inside the dead zone are ignored.

---

# 10. Input Sensitivity

Certain inputs require adjustable sensitivity.

Examples:

mouse look sensitivity  
controller camera sensitivity

Players should be able to modify these settings through the options menu.

Sensitivity settings must be stored in player preferences.

---

# 11. Input Rebinding

The Input System must allow players to rebind controls.

Rebinding allows players to customize which physical inputs trigger gameplay actions.

Example:

Attack → MouseLeft (default)
Attack → ControllerRT

After rebinding:

Attack → MouseRight

Rebinding must support:

- keyboard keys
- mouse buttons
- controller buttons

Each action may have multiple bindings.

Example:

Interact
Primary: E
Secondary: ControllerButtonX

Rebinding settings must be saved in the player settings file.

---

# 12. Input Priority Rules

When multiple systems receive input simultaneously, priority rules determine which system processes the input.

Example priority order:

1. System Menus
2. Pause Menu
3. UI Navigation
4. Gameplay Systems

Example scenario:

Player presses "Escape".

If the game is in gameplay state → open pause menu.

If already in pause menu → close pause menu.

Gameplay input should never override menu input.

---

# 13. Input Locking

Some gameplay situations temporarily disable input.

Examples include:

- cutscenes
- player death
- scripted story sequences
- boss introductions

Input locking prevents unintended player actions.

Example structure:

InputLock
{
movementLocked
combatLocked
interactionLocked
}

This allows certain inputs to remain active while others are disabled.

---

# 14. Input Cooldowns

Some actions require cooldown timers to prevent excessive input spam.

Examples include:

- interaction actions
- weapon switching
- item usage

Example cooldown structure:

InputCooldown
{
action
cooldownTime
currentTimer
}

Cooldowns ensure consistent gameplay pacing.

---

# 15. Input Conflict Prevention

The system must prevent conflicting inputs.

Example conflict:

Player attempts to interact and attack simultaneously.

Resolution rules determine which action takes priority.

Typical priority:

Interaction > Attack

If the player is interacting with an object, attack input should be ignored.

---

# 16. Input Debugging Tools

Development builds should include input debugging tools.

Examples include:

Input Viewer  
Displays currently pressed inputs.

Input Mapping Inspector  
Shows which actions are bound to which inputs.

Input Event Logger  
Logs input events in real time.

Controller Debug Mode  
Displays analog stick values and trigger pressure.

These tools help diagnose control issues during development.

---

# 17. Input System Integration

The Input System interacts with multiple gameplay systems.

Player Controller  
Receives movement and camera input.

Combat System  
Receives attack and weapon input.

Interaction System  
Receives interaction commands.

UI System  
Receives menu navigation input.

State Management  
Controls which input contexts are active.

Audio System  
Triggers UI and interaction sounds.

Input routing must follow state rules to avoid conflicts.

---

# 18. Accessibility Input Features

The input system must support accessibility features.

Examples include:

toggle sprint instead of hold  
toggle aim instead of hold  
remappable controls  
adjustable input sensitivity

Accessibility improves usability for different players.

---

# 19. Input Persistence

Input settings must persist between sessions.

Settings to store include:

- key bindings
- controller mappings
- sensitivity values

These values are saved in the player's configuration file.

Example configuration:

InputConfig
{
mouseSensitivity
controllerSensitivity
keyBindings[]
}

---

# 20. Future Input Expansion

The Input System must support future input devices and features.

Possible expansions include:

Steam Deck support  
advanced controller layouts  
gyro aiming  
adaptive triggers  
custom macro bindings

The system architecture must remain flexible to support additional input features.

---