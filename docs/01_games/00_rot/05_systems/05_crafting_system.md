# Crafting System

## 1. System Overview

The Crafting System allows players to create useful survival items using materials collected during exploration.

Crafting provides flexibility in how players manage resources while still preserving the survival horror emphasis on scarcity.

Players cannot craft unlimited supplies.  
Crafting materials are limited and must be discovered through exploration.

The Crafting System allows players to produce:

- healing items
- ammunition
- chemical stabilizers
- environmental tools

Crafting is intended to **supplement exploration**, not replace it.

Players must still search environments to obtain the majority of their supplies.

---

## 2. Design Philosophy

The Crafting System follows several core design principles.

### Simplicity

Crafting recipes should remain easy to understand.

Recipes use only a small number of materials.

This prevents crafting from becoming overly complex.

---

### Resource Scarcity

Crafting materials are intentionally limited.

Players must decide whether to:

- craft items immediately
- save materials for later use

This reinforces the resource economy.

---

### Exploration Integration

Crafting materials are discovered through environmental exploration.

Players who thoroughly explore environments gain a significant survival advantage.

---

### Character Identity

Crafting capabilities reflect the protagonist’s practical survival knowledge.

Elena’s experience working in hazardous environments allows her to improvise basic survival tools.

---

## 3. Crafting Locations

Crafting cannot be performed everywhere.

Players must use designated crafting locations.

Examples include:

- safe zone workbenches
- medical stations
- repair benches
- specialized laboratory equipment

This limitation prevents players from crafting items instantly during combat.

---

## 4. Crafting Materials

Crafting requires materials that the player discovers during exploration.

Examples include:

Chemical Components

Used in ammunition and chemical mixtures.

Medical Supplies

Used to craft healing items.

Mechanical Parts

Used for equipment repairs or advanced crafting.

Biological Samples

Rot-infected materials used for experimental crafting items.

Crafting materials occupy inventory slots until they are used.

---

## 5. Crafting Recipes

Crafting recipes define which materials are required to produce a specific item.

Example recipe structure:

Bandage

Required Materials:

- sterile cloth
- medical alcohol

Result:

- bandage (healing item)

---

Improvised Ammunition

Required Materials:

- chemical compound
- metal fragments

Result:

- handgun ammunition

Recipes are predefined and cannot be modified by the player.

---

## 6. Recipe Discovery

Players do not begin the game with all crafting recipes.

Recipes are discovered through exploration.

Examples include:

- medical notes found in the hospital
- research documents recovered from Halcyon laboratories
- survival manuals left by emergency responders

Once discovered, recipes remain permanently available.

---

## 7. Crafting Process

The crafting process follows several steps.

1. Player opens the crafting interface.

2. The system displays all known recipes.

3. The player selects a recipe.

4. The system checks whether required materials are available.

5. If materials are present, the crafting action completes.

6. Materials are removed from inventory.

7. The crafted item is added to the inventory.

If the inventory is full, crafting cannot proceed.

---

## 8. Crafting Output

Crafting outputs include several categories of items.

Healing Items

Restore player health.

Ammunition

Allows limited recovery of firearm ammunition.

Chemical Compounds

Provide protection from Rot contamination.

Utility Items

Support puzzle solving or environmental interactions.

The exact crafting outputs are defined in the content documentation.

---

## 9. Crafting Interface

The Crafting System provides a dedicated crafting interface accessible at crafting stations.

The interface displays:

- available recipes
- required materials
- current material quantities
- resulting item description

Recipes that cannot be crafted due to missing materials remain visible but appear visually disabled.

This allows players to understand what materials they still need to collect.

---

### Crafting Menu Layout

The crafting menu should include the following sections:

Recipe List

Displays all discovered recipes.

Material Requirements

Shows materials required for the selected recipe.

Inventory Material Count

Displays how many materials the player currently possesses.

Craft Button

Initiates the crafting action when materials are available.

---

### Crafting Feedback

When crafting occurs, players receive immediate feedback.

Examples include:

- crafting sound effects
- short animation
- UI confirmation message
- inventory update

Feedback ensures players clearly understand that crafting succeeded.

---

## 10. Advanced Crafting

Later stages of the game may unlock more advanced crafting options.

Advanced recipes may include:

- enhanced healing items
- improved ammunition
- environmental resistance compounds
- experimental Halcyon chemical mixtures

Advanced crafting requires rare materials typically found in dangerous areas.

---

## 11. Crafting Balance

Crafting must remain carefully balanced to avoid undermining the survival horror experience.

Important balance rules include:

Crafting should never replace exploration.

Materials must remain limited.

Ammunition crafting should be expensive.

Healing items should remain valuable and rare.

Crafting should provide limited flexibility rather than unlimited supplies.

---

## 12. Crafting Failure Conditions

Certain conditions prevent crafting from occurring.

Examples include:

Missing Materials

The player does not possess the required materials.

Inventory Full

The crafted item cannot fit in the inventory.

Unavailable Crafting Station

The player attempts to craft outside designated locations.

In these cases the system should display clear feedback explaining why crafting cannot proceed.

---

## 13. Crafting and Inventory Integration

The Crafting System interacts directly with the Inventory System.

When crafting occurs:

1. required materials are removed from inventory
2. the crafted item is generated
3. the new item is placed into an available inventory slot

If the item cannot fit into the inventory, crafting is prevented.

This ensures players must manage inventory space before crafting.

---

## 14. Crafting Edge Cases

The system must handle unusual gameplay situations.

Examples include:

Player crafting while inventory space becomes unavailable.

Player attempting to craft while in combat.

Player leaving the crafting station during crafting actions.

Crafting interface remaining open after materials are removed.

These cases must resolve safely without breaking the game state.

---

## 15. Crafting Debug Tools

During development, debugging tools assist with crafting system testing.

Examples include:

Material Spawn Commands

Allows developers to add crafting materials to inventory.

Recipe Unlock Commands

Allows developers to unlock all recipes for testing.

Crafting Log Output

Displays crafting actions and material consumption.

These tools help developers test crafting balance and system behavior.

---

## 16. System Dependencies

The Crafting System interacts with several other gameplay systems.

Inventory System

Provides materials and stores crafted items.

Interaction System

Triggers crafting stations when the player interacts with them.

UI System

Displays crafting menus and recipe information.

Audio System

Plays crafting sound effects.

Save System

Stores discovered recipes and material counts.

---

## 17. Future Expansion

The Crafting System is designed to support additional features in future updates.

Possible expansions include:

advanced equipment crafting  
weapon modification crafting  
specialized Rot research crafting  
environmental trap construction  

The modular structure ensures new crafting mechanics can be added without redesigning the core system.

---