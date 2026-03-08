# UI System

## 1. System Overview

The UI System manages all visual interface elements presented to the player.

This includes:

- gameplay HUD
- inventory interface
- interaction prompts
- menus
- boss health indicators
- pause screens
- settings menus

The UI must remain **clear, minimal, and immersive**, supporting the survival horror atmosphere without overwhelming the player.

The system must also remain modular so UI elements can be reused across gameplay states.

---

## 2. UI Design Philosophy

The UI design follows several core principles.

### Minimalism

The interface should display only essential information.

The player should focus primarily on the game world rather than UI elements.

Examples:

- health displayed subtly
- ammo count visible only when weapon is equipped
- interaction prompts appearing contextually

---

### Immersion

UI elements should feel integrated into the game's tone.

The UI aesthetic should reflect the game's atmosphere:

- muted color palettes
- subtle animations
- diegetic design where possible

---

### Readability

Information must be easily readable during stressful gameplay.

Elements should use:

- clear typography
- consistent iconography
- high contrast where needed

---

### Responsiveness

UI elements must react immediately to player input.

Examples include:

- inventory opening instantly
- weapon switching feedback
- interaction confirmation

---

## 3. UI Categories

The UI System contains several categories of interface elements.

---

### Gameplay HUD

Displayed during active gameplay.

Includes:

- health indicator
- stamina indicator (if applicable)
- equipped weapon information
- ammunition count
- interaction prompts

HUD elements should remain unobtrusive.

---

### Inventory Interface

Displays the player’s current items and equipment.

The inventory UI must allow players to:

- view items
- equip weapons
- combine crafting materials
- discard items

Inventory navigation should be fast and intuitive.

---

### Interaction Prompts

Context-sensitive prompts appear when the player approaches interactive objects.

Examples include:

Press key to open door  
Press key to pick up item  
Press key to activate switch

Prompts must disappear when the player moves away from the object.

---

### Menu Interface

Menus allow the player to manage the game state.

Menus include:

- pause menu
- inventory menu
- map screen
- settings menu

Menus pause gameplay when opened.

---

### Boss UI

During boss fights, additional UI elements appear.

Examples include:

- boss health bar
- boss phase indicators
- special mechanic indicators

Boss UI should appear only during boss encounters.

---

### Notification UI

Temporary notifications inform players about events.

Examples include:

Item acquired  
Puzzle solved  
New objective added  

Notifications should fade after a short duration.

---

## 4. HUD Elements

The gameplay HUD contains several components.

---

### Health Indicator

Displays the player's current health.

Health may be represented through:

- health bar
- segmented indicator
- character status indicator

The system should clearly communicate damage.

---

### Weapon Indicator

Displays the currently equipped weapon.

Information includes:

weapon icon  
ammunition count  
reload status

This helps players manage combat resources.

---

### Interaction Indicator

Appears when the player approaches an interactable object.

The indicator includes:

interaction icon  
action text prompt

Example:

Press E to open Door


---

## 5. Inventory UI

The inventory screen allows players to manage their items.

Features include:

item grid display  
item descriptions  
weapon equipment slots  
item discard options

The inventory must clearly show:

- item icons
- item quantity
- item category

Navigation should be optimized for keyboard and controller input.

---

## 6. Menu System

Menus allow players to pause and manage game systems.

Menu options include:

Resume Game  
Inventory  
Map  
Settings  
Exit Game

Menus must be easy to navigate and clearly structured.

---

## 7. Map Interface

The map UI displays explored areas of the game world.

Map features include:

player location marker  
discovered areas  
locked areas  
objective markers

The map updates as the player explores new locations.

---

## 8. Objective Tracking

The UI should provide subtle objective tracking.

Examples include:

current objective text  
optional objective hints  
map markers for major story progression

Objectives should guide the player without removing exploration.

---

## 9. Settings Menu

The settings interface allows players to customize gameplay options.

Settings categories include:

Graphics  
Audio  
Controls  
Gameplay  
Accessibility

Changes should apply immediately when possible.

---

## 10. Accessibility Options

The UI must support accessibility features.

Examples include:

subtitle support  
colorblind-friendly UI options  
adjustable text size  
audio volume customization

Accessibility ensures the game can be played by a wide range of players.

## 11. UI Animation

UI elements should use subtle animations to improve readability and feedback.

Animations should remain minimal to maintain immersion and avoid visual clutter.

Common UI animations include:

Fade In  
Elements appear gradually when triggered.

Fade Out  
Elements disappear smoothly when no longer relevant.

Slide Transitions  
Menus slide into view when opened.

Pulse Effects  
Important notifications briefly pulse to attract attention.

Animations should remain short and responsive.

---

## 12. UI Feedback

The UI must clearly communicate player actions and system responses.

Examples include:

Item Pickup  
Displays a notification showing the acquired item.

Puzzle Interaction  
Displays confirmation when puzzle steps are completed.

Weapon Reload  
Displays visual indication of reload progress.

Error Feedback  
Displays warning messages if an action cannot be performed.

Example:

Inventory Full


Clear feedback prevents player confusion.

---

## 13. UI Layering

UI elements are organized into layers to ensure proper display order.

Typical UI layers include:

Background Layer  
Menu backgrounds and large panels.

Gameplay HUD Layer  
Health, weapon information, and interaction prompts.

Notification Layer  
Temporary messages and alerts.

Overlay Layer  
Pause menus and settings screens.

Debug Layer  
Developer-only UI elements.

Layering ensures important information remains visible.

---

## 14. Input Navigation

The UI must support both keyboard and controller input.

Navigation systems should include:

Directional navigation  
Selection confirmation  
Back navigation

Controller navigation should support:

- analog stick movement
- D-pad navigation
- button selection

Keyboard navigation should support:

- arrow keys
- enter/confirm
- escape/back

UI navigation must remain consistent across all menus.

---

## 15. UI Asset Organization

UI assets must follow consistent naming conventions.

Example naming structure:

ui_category_element_state

Examples:

ui_healthbar_main

ui_inventory_slot

ui_interaction_prompt

ui_boss_healthbar

ui_menu_background


Consistent asset naming simplifies UI development and maintenance.

---

## 16. UI Performance Optimization

UI elements must be optimized to avoid unnecessary rendering overhead.

Optimization strategies include:

UI element pooling  
Reusable UI components.

Limited update frequency  
Non-critical UI elements update less frequently.

Visibility checks  
UI elements render only when needed.

Minimal animation complexity  
Avoid excessive animation layers.

These optimizations ensure smooth gameplay performance.

---

## 17. UI Debugging Tools

Development builds should include tools for testing UI behavior.

Examples include:

UI Visibility Toggle  
Displays or hides specific UI layers.

HUD Debug Mode  
Shows additional gameplay statistics.

Interaction Prompt Viewer  
Displays all active interaction prompts.

Menu Navigation Tester  
Simulates controller and keyboard navigation.

These tools assist developers during testing.

---

## 18. UI System Integration

The UI System interacts with several other systems.

Player Controller  
Displays health, stamina, and weapon information.

Inventory System  
Displays items and equipment.

Combat System  
Shows ammunition count and reload feedback.

Puzzle System  
Displays puzzle notifications and interaction prompts.

Boss System  
Displays boss health bars and encounter UI.

Save System  
Displays save/load notifications.

Audio System  
Plays UI sound effects.

---

## 19. Localization Support

The UI system must support multiple languages.

UI text must be stored separately from code.

Localization features include:

dynamic text scaling  
language selection menu  
external text resource files

This allows the game to support additional languages without modifying UI code.

---

## 20. UI State Persistence

Certain UI states should persist across gameplay sessions.

Examples include:

selected language  
display settings  
control bindings  
accessibility preferences

These settings must be saved using the Save System.

---

## 21. Future UI Expansion

The UI architecture should support future improvements.

Possible expansions include:

dynamic objective tracking systems  
in-game codex or lore viewer  
photo mode interface  
advanced accessibility settings

The UI framework must remain modular to support these additions.

---

## 22. Rot Exposure Interface

The Rot Exposure System requires subtle UI feedback to communicate contamination levels.

The UI must avoid explicit numerical indicators to preserve immersion.

Possible presentation methods include:

Visual Distortion

Screen effects may indicate increasing contamination.

Examples:

- subtle screen warping
- color desaturation
- visual noise
- biological vein-like overlays

These effects gradually intensify as exposure increases.

---

Heartbeat Indicator

A faint heartbeat audio or visual pulse may occur during high exposure.

This reinforces the sense that the player's body is being affected by the Rot.

---

Rot Pulse Indicator

In highly contaminated environments, the UI may display subtle environmental pulsation effects tied to Rot growth nearby.

These effects should feel environmental rather than purely interface-based.

---

## 23. Stealth Awareness Indicators

Stealth gameplay requires subtle feedback for player awareness.

The UI should avoid explicit stealth meters but may provide indirect indicators.

Examples include:

Enemy Awareness Feedback

When enemies become suspicious, subtle indicators may appear such as:

- faint directional markers
- audio cues
- brief UI pulse effects

These indicators warn the player without revealing exact enemy positions.

---

Detection State Feedback

If the player is detected, the UI may briefly display a visual cue.

Examples include:

- screen edge flash
- audio sting
- brief HUD highlight

These cues transition the player into combat awareness.

---

## 24. Archive / Collectibles Interface

The Archive Interface allows players to review collected narrative documents.

The archive system is accessible through the pause menu.

Archive categories include:

Civilian Records  
Emergency Communications  
Halcyon Research Logs  
Researcher Journals  
Environmental Observations  

Each document should display:

- document title
- location where it was discovered
- full readable text

The archive system supports narrative exploration for players interested in the deeper lore of ROT.

---

## 25. Minimal HUD Mode

ROT may support a **minimal HUD mode**.

In this mode:

- health indicators appear only after damage
- ammo count appears only when aiming
- interaction prompts appear only when necessary

This mode increases immersion for players who prefer minimal interface elements.

---

## 26. Environmental UI Integration

Some UI elements may be presented through the game world rather than traditional overlays.

Examples include:

Physical Maps

Players may interact with physical maps placed in safe zones.

Research Terminals

Halcyon computers may display data logs through in-world screens.

Radio Communications

Emergency broadcasts may appear as diegetic audio rather than UI text.

This design reinforces immersion in the world.

---

## 27. Contamination Screen Effects

The UI system may apply screen effects during certain gameplay conditions.

Examples include:

Low Health

- slight vignette
- red color tint

Rot Exposure

- biological distortion
- environmental noise

Severe Injury

- blurred vision
- slowed UI animations

These effects communicate player condition without relying on explicit UI elements.

---

## 28. Design Goals for UI

The UI System must support several goals.

- maintain immersion within the horror atmosphere
- communicate essential gameplay information
- remain minimal and unobtrusive
- integrate naturally with the game world

Players should feel immersed in the environment rather than interacting with a traditional interface.

The UI should support gameplay while remaining mostly invisible during exploration.

---