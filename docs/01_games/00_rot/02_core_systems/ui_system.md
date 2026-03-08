# UI System

Project: ROT  
Version: 1.1  
Document Type: Gameplay System  
Category: User Interface  
Scope: ROT (Game)  
Status: Core Reference  

---

# 1. Overview

The UI System defines how information is presented to the player during gameplay.

The user interface in ROT must support gameplay without disrupting immersion. The world and environment should remain the primary focus of the player's attention.

UI elements must therefore be:

- minimal  
- readable  
- context aware  
- consistent with the tone of the game  

The interface should communicate essential gameplay information while remaining visually restrained.

---

# 2. UI Design Philosophy

The design of the UI follows several core principles.

## Minimalism

Only essential information should be visible during gameplay.

The screen should not be filled with persistent interface elements that distract from the environment.

Information should appear when it is needed and disappear when it is no longer relevant.

---

## Immersion

UI elements should feel integrated into the game experience.

The interface should avoid overly stylized or futuristic elements that conflict with the grounded tone of ROT.

Subtle animations, restrained color palettes, and simple iconography help maintain immersion.

---

## Clarity

Despite its minimal design, the interface must communicate information clearly.

Players should quickly understand:

- their current condition  
- available resources  
- interaction opportunities  
- navigation through menus  

Information must remain readable under different lighting conditions and gameplay situations.

---

## Context Awareness

Many interface elements should appear only when relevant.

Examples include:

- interaction prompts appearing near objects  
- inventory information when the inventory is open  
- damage indicators during combat  

Context driven UI prevents unnecessary clutter.

---

# 3. HUD (Heads Up Display)

The HUD displays essential gameplay information during exploration and combat.

HUD elements should remain subtle and occupy minimal screen space.

Possible HUD components include:

- health indicator  
- stamina indicator  
- Rot exposure meter  
- currently equipped item or weapon  
- ammunition count when using firearms  

These elements should be positioned so that they remain visible but do not obstruct the player's view.

HUD elements may fade or become less prominent during calm exploration phases.

---

# 4. Inventory Interface

The inventory interface allows players to manage items, equipment, and resources.

When the inventory is opened, the player should be able to:

- view stored items  
- inspect item descriptions  
- equip weapons or tools  
- rearrange inventory slots  
- discard unnecessary items  

The layout should be clear and easy to navigate.

Information displayed within the inventory includes:

- item icons  
- item names  
- quantities or stack sizes  
- item descriptions  

The inventory screen should allow efficient item management without excessive complexity.

---

# 5. Interaction Prompts

Interaction prompts inform the player when they can interact with objects in the environment.

Prompts should appear when the player approaches an interactable object.

Examples include:

- opening doors  
- picking up items  
- activating devices  
- inspecting objects  

Prompts should be small, readable, and positioned near the center of the player's focus.

They should disappear when the player moves away from the object.

---

# 6. Menu Systems

Menu systems allow players to access settings, saved games, and additional information.

Major menu categories include:

- pause menu  
- options menu  
- save and load screens  
- control configuration  
- accessibility settings  

Menus should be easy to navigate and consistent in visual style.

Menu design should maintain the same restrained aesthetic used throughout the UI.

---

# 7. Feedback and Indicators

The UI should provide feedback for important gameplay events.

Examples include:

- damage indicators when the player is attacked  
- visual cues when stamina is depleted  
- warnings when Rot exposure reaches dangerous levels  
- confirmation messages when saving progress  

Feedback should be immediate and clearly visible.

---

# 8. Accessibility Considerations

The UI should support accessibility options that allow a wider range of players to comfortably experience the game.

Examples include:

- adjustable text size  
- subtitle options  
- color contrast adjustments  
- customizable control bindings  

Accessibility options should not compromise the core design philosophy but should provide flexibility for players.

---

# 9. Integration with Other Systems

The UI System interacts with many gameplay systems.

Examples include:

- Combat System for health and ammunition display  
- Rot Exposure System for contamination indicators  
- Inventory System for item management  
- Interaction System for object prompts  

These integrations ensure that the interface communicates gameplay information effectively.

---

# 10. Purpose of This Document

This document defines the UI philosophy used in ROT.

By following these guidelines, the interface remains clear, immersive, and supportive of the survival horror atmosphere while delivering essential gameplay information to the player.

---