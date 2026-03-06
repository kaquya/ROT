# Interaction System

## 1. System Overview

The Interaction System manages all player interactions with objects and elements within the game world.

It allows the player to:

- collect items
- open doors
- activate mechanisms
- operate environmental systems
- interact with puzzle components
- inspect environmental story elements

The Interaction System acts as a bridge between the **Player Controller** and world objects that can respond to player actions.

Rather than embedding interaction logic directly inside the Player Controller, the system provides a **standardized interface** that any object can implement.

This ensures that interaction behavior remains modular and scalable as the game expands.

---

## 2. Design Philosophy

The Interaction System follows several core design principles.

### Environmental Consistency

Players should quickly understand which objects are interactive.

Common interaction cues include:

- doors
- switches
- control panels
- items on surfaces
- damaged infrastructure

Objects that can be interacted with should follow consistent visual language.

---

### Minimal UI Intrusion

The game should rely primarily on environmental cues rather than excessive UI prompts.

Interaction prompts appear only when the player is within range and facing the object.

---

### Modular Object Behavior

Objects implement interaction behavior independently.

Examples include:

- a door opening
- an item being collected
- a machine activating
- a puzzle element changing state

The Interaction System simply triggers these behaviors.

---

## 3. Interaction Types

Different categories of interactions exist within the game world.

Each type may trigger different gameplay systems.

---

### Item Collection

The player may collect items found in the environment.

Examples:

- ammunition
- crafting materials
- healing items
- key items
- documents

Collected items are transferred to the **Inventory System**.

---

### Environmental Activation

The player may activate environmental objects.

Examples:

- switches
- generators
- elevators
- control panels

These objects often affect the surrounding environment.

---

### Door Interaction

Doors allow the player to move between areas.

Door interactions include:

- opening unlocked doors
- unlocking doors with keys
- unlocking doors with keycards
- blocked doors that cannot be opened

Doors may trigger loading transitions between districts.

---

### Puzzle Interaction

Puzzle elements allow players to manipulate objects to solve environmental challenges.

Examples include:

- rotating mechanisms
- placing objects in slots
- activating multiple switches

Puzzle logic itself is handled by the **Puzzle System**.

---

### Inspection Interaction

Certain environmental objects can be inspected.

Examples include:

- documents
- photographs
- environmental storytelling clues

These interactions reveal narrative information.

---

## 4. Interaction Range

The player must be within a defined distance to interact with an object.

Typical interaction range:

1.5 – 2 meters from the player.

This prevents players from interacting with distant objects unintentionally.

---

### Line-of-Sight Requirement

Some interactions require the player to face the object.

This prevents accidental activation of objects behind the player.

Detection methods may include:

- camera-based raycasting
- forward collision checks

---

## 5. Interaction Prompt System

When the player approaches an interactable object, the UI displays a prompt.

Example prompts:

- "Open Door"
- "Pick Up Item"
- "Activate Generator"
- "Inspect"

Prompts appear only when:

- the player is within interaction range
- the object is visible to the player
- the object is available for interaction

---

### Prompt Behavior

Prompts should be:

- small
- unobtrusive
- clearly readable

They disappear when the player leaves interaction range.

---

## 6. Interaction Interface

All interactable objects must implement a common interface.

Example conceptual interface:

Interact()

Called when the player activates the object.

CanInteract()

Determines whether interaction is currently possible.

GetInteractionPrompt()

Returns the text displayed to the player.

---

### Example Objects Using the Interface

Door

Interact() → opens or unlocks the door.

Item Pickup

Interact() → transfers item to inventory.

Switch

Interact() → activates a mechanism.

Puzzle Component

Interact() → changes puzzle state.

---

## 7. Interaction Priority

When multiple objects are within range, the system determines which one should receive the interaction input.

Priority may be determined by:

- camera direction
- object distance
- object type

Example:

An item directly in front of the player should take priority over a switch behind it.

---

## 8. Interaction Feedback

After a successful interaction, feedback should be provided to the player.

Examples include:

- animation (door opening)
- sound effect
- UI notification
- environmental change

Feedback helps confirm that the interaction occurred successfully.

---

## 9. Interaction Locking

Certain interactions may temporarily lock player movement.

Examples include:

- opening heavy doors
- operating complex machinery
- performing puzzle actions

During these interactions:

- player movement may be disabled
- camera movement may be limited
- interaction animations may play

This prevents gameplay conflicts.

---W

## 10. Inventory-Linked Interactions

Certain interactions depend on items stored in the player's inventory.

These interactions check whether the player possesses a required item before allowing the action.

Examples include:

- unlocking doors with keys
- activating security systems with keycards
- inserting mechanical components into devices
- using puzzle objects in specific locations

When the required item is present, the interaction proceeds normally.

If the required item is missing, the interaction should fail gracefully.

Example feedback:

"This door is locked."

"A keycard is required."

This prevents confusion while maintaining immersion.

---

## 11. Conditional Interactions

Some objects only become interactable after specific conditions are met.

Examples include:

- a generator that must be repaired before activation
- a door that unlocks after solving a puzzle
- a machine that requires power before use

Conditional logic may depend on:

- puzzle completion
- inventory state
- environmental events
- story progression

The Interaction System queries the object's internal state before allowing interaction.

---

## 12. Multi-Step Interactions

Certain environmental systems require multiple interaction steps.

Examples include:

Generator Startup

Step 1 — Insert fuel  
Step 2 — Activate generator switch

Puzzle Mechanism

Step 1 — Place missing component  
Step 2 — Rotate mechanism  
Step 3 — Activate final switch

The interaction system supports these sequences by allowing objects to maintain internal state.

---

## 13. Interaction Cooldowns

Some interactions may include cooldown periods to prevent repeated activation.

Examples include:

- repeatedly activating switches
- triggering environmental mechanisms too quickly
- interacting with objects during animation sequences

Cooldown timers ensure interactions remain stable and prevent unintended gameplay behavior.

---

## 14. Interaction Cancellation

The player may sometimes cancel interactions before completion.

Examples include:

- stepping away from the object
- entering combat
- receiving damage from enemies

When an interaction is cancelled:

- the object returns to its previous state
- the player regains movement control
- any partial progress may be reset depending on the object

This prevents players from becoming stuck during interactions.

---

## 15. Locked Interactions

Certain objects cannot be interacted with until specific conditions are satisfied.

Examples include:

- permanently blocked doors
- broken machines
- inaccessible areas

These objects should still provide feedback to the player.

Example messages:

"The mechanism is damaged."

"The door is blocked from the other side."

This reinforces environmental storytelling.

---

## 16. Interaction State Management

The Interaction System must maintain the current interaction state of the player.

Possible interaction states include:

Idle

The player is not interacting with any object.

Active Interaction

The player is interacting with an object.

Locked Interaction

The player is temporarily unable to initiate interactions.

These states help prevent system conflicts.

Example conflict prevention:

The player cannot interact with a door while reloading a weapon.

---

## 17. Interaction Edge Cases

The system must account for unusual gameplay situations.

Examples include:

Multiple objects occupying the same space

The player may stand between a door and an item.

The system must determine the correct interaction target.

Object destruction

If an object becomes unavailable during interaction, the interaction should terminate safely.

Moving objects

Objects attached to moving platforms must update interaction detection dynamically.

---

## 18. Debugging Tools

During development, debugging tools should assist with interaction testing.

Examples include:

Interaction range visualization

Displays the player's interaction detection radius.

Raycast visualization

Shows the detection ray used to identify interactable objects.

Interaction state display

Shows the player's current interaction state.

These tools help developers diagnose interaction issues quickly.

---

## 19. System Dependencies

The Interaction System interacts with several other gameplay systems.

Player Controller

Provides interaction input and player position.

Inventory System

Handles item collection and item usage.

Puzzle System

Processes puzzle-related interactions.

UI System

Displays interaction prompts and feedback.

Audio System

Plays interaction sound effects.

Animation System

Triggers animations during interactions.

These systems must communicate through clearly defined interfaces.

---

## 20. Future Expansion

The Interaction System is designed to support future gameplay features.

Potential future additions include:

context-sensitive interactions  
advanced environmental manipulation  
multi-object interaction puzzles  
physics-based object interactions  

The modular design ensures that new interaction types can be added without rewriting the core system.

---