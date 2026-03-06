# Inventory System

## 1. System Overview

The Inventory System manages all items carried by the player.

It determines:

- how many items the player can carry
- how items are stored and organized
- how items are used
- how items interact with other systems
- how items are transferred to storage containers

The system is designed to reinforce survival-horror gameplay by limiting resources and forcing players to make strategic decisions about what they carry.

Inventory management is therefore not simply a convenience feature but a **core gameplay mechanic**.

---

## 2. Design Philosophy

The Inventory System follows several core principles.

### Resource Scarcity

Players should rarely feel fully stocked with supplies.

Limited inventory space forces players to prioritize essential resources.

---

### Strategic Planning

Before entering dangerous areas, players must decide which items to bring.

Examples include:

- additional ammunition
- healing supplies
- puzzle key items
- crafting materials

Poor preparation can make encounters significantly more dangerous.

---

### Simplicity and Clarity

The inventory interface should remain simple and easy to navigate.

Players must be able to quickly identify:

- item types
- item quantities
- equipped weapons

This prevents the inventory from interrupting gameplay flow.

---

## 3. Inventory Structure

The player inventory uses a **slot-based system**.

Each item occupies one slot unless the item is stackable.

Example inventory capacity:

12 slots total.

This number may change during balancing.

---

### Slot Allocation

Slots are shared across all item categories.

Examples include:

- weapons
- ammunition
- healing items
- crafting materials
- key items

Because all items share the same space, the player must constantly balance survival resources against progression items.

---

## 4. Item Categories

Items are divided into several categories.

Each category behaves slightly differently within the inventory.

---

### Weapons

Weapons occupy inventory slots and can be equipped by the player.

Examples include:

- handguns
- shotguns
- rifles
- melee weapons

Weapons may require ammunition or durability management depending on their type.

---

### Ammunition

Ammunition is required for firearms.

Examples include:

- handgun rounds
- shotgun shells
- rifle cartridges

Ammunition can stack within inventory slots up to a defined maximum.

---

### Healing Items

Healing items restore the player's health.

Examples include:

- bandages
- medical injections
- chemical stabilizers

Healing items are intentionally rare.

Players must decide carefully when to use them.

---

### Crafting Materials

Crafting materials are used to create useful survival items.

Examples include:

- chemical compounds
- medical alcohol
- mechanical components

Materials occupy inventory slots until they are used in crafting.

---

### Key Items

Key items are required to progress through the game world.

Examples include:

- keys
- access cards
- puzzle components

Key items occupy inventory space until they are used.

This design reinforces tension during exploration.

---

## 5. Item Stacking

Certain item types may stack within a single inventory slot.

Typical stackable items include:

- ammunition
- crafting materials
- small consumables

Example stacking limits:

Handgun Ammo  
Maximum stack: 30 rounds

Shotgun Shells  
Maximum stack: 12 shells

Crafting Materials  
Maximum stack varies depending on material type.

Stack limits will be finalized during gameplay balancing.

---

## 6. Item Acquisition

Items are typically acquired through environmental exploration.

Common sources include:

- containers
- abandoned homes
- industrial facilities
- defeated enemies
- puzzle rewards

When the player collects an item, it is transferred to the inventory if space is available.

If no space is available, the player must either:

- discard an existing item
- transfer items to storage later

---

## 7. Item Usage

Items may be used directly from the inventory.

Examples include:

Healing Items

Restore player health.

Weapon Reloading

Consumes ammunition.

Crafting Materials

Used at crafting stations.

Key Items

Used automatically during relevant interactions.

Some items may trigger animations when used.

---

## 8. Equipped Items

The player may equip certain items for immediate use.

Examples include:

- primary weapon
- secondary weapon
- melee weapon
- quick-use healing item

Equipped items remain stored within the inventory but are accessible without opening the inventory screen.

---

## 9. Inventory Access

The player can open the inventory at most times during gameplay.

Opening the inventory pauses active gameplay in single-player mode.

This allows players to:

- inspect items
- reorganize items
- use items
- combine crafting materials

However, the inventory cannot be accessed during certain states such as:

- cutscenes
- locked puzzle sequences
- certain combat situations

---

## 10. Storage Containers

Storage containers allow the player to store items that cannot be carried in the main inventory.

These containers are typically located in **safe zones** throughout the game world.

Examples include:

- Elena’s house storage chest
- emergency coordination center lockers
- hospital staff lockers
- research facility storage terminals

All storage containers share the same storage pool.

This means that items stored in one location can be retrieved from another storage container later.

---

### Storage Capacity

Storage containers should have a significantly larger capacity than the player inventory.

Example capacity:

50–100 storage slots.

Storage capacity may expand later depending on balancing needs.

---

### Storage Functions

Players may perform several actions when interacting with storage containers.

Deposit Item

Transfers an item from the player inventory into storage.

Withdraw Item

Transfers an item from storage into the player inventory.

Reorganize Storage

Players may reorder stored items for easier management.

---

### Storage Limitations

Items can only be stored when the player is physically interacting with a storage container.

Players cannot access storage remotely.

This maintains exploration tension.

---

## 11. Item Discarding

Players may discard items directly from the inventory.

Discarding permanently removes the item from the player’s possession.

Examples include:

- removing unnecessary crafting materials
- freeing space for important items
- dropping weapons that are no longer needed

Discarded items are typically destroyed and do not remain in the world.

This prevents clutter and memory issues.

---

## 12. Crafting Integration

The Inventory System interacts closely with the Crafting System.

Crafting materials stored in the player inventory can be consumed when crafting items.

Crafting may occur at:

- safe zone workbenches
- medical stations
- specialized crafting tables

When crafting occurs:

1. Required materials are removed from inventory.
2. The crafted item is added to inventory if space exists.

If inventory space is full, the crafting action cannot proceed.

This reinforces inventory planning.

---

## 13. Inventory Reorganization

Players may rearrange items within the inventory.

This allows players to group related items together.

Examples:

- placing ammunition next to weapons
- grouping healing items together
- organizing crafting materials

Item reordering has no gameplay effect but improves usability.

---

## 14. Inventory UI Layout

The inventory screen displays items using a **grid layout**.

Example grid:

[ ] [ ] [ ] [ ]

[ ] [ ] [ ] [ ]

[ ] [ ] [ ] [ ]


Each slot contains one item or stack.

Selecting an item reveals detailed information such as:

- item name
- description
- quantity
- usage options

---

### Item Inspection

Players may inspect items in the inventory to read additional details.

Examples include:

- item descriptions
- lore documents
- key item hints

Inspection may also trigger narrative elements.

---

## 15. Inventory State Management

The inventory system must maintain consistent state across gameplay sessions.

Important states include:

- current item list
- item quantities
- equipped items
- stored items

These values are saved through the Save System.

---

## 16. Save System Integration

When the player saves the game, the following inventory data must be recorded.

Player inventory contents

All item slots and stack quantities.

Equipped items

Currently equipped weapons and quick-use items.

Storage container contents

All items stored in shared storage containers.

Crafting materials

Remaining quantities of crafting resources.

This data ensures that the player’s inventory persists between sessions.

---

## 17. Edge Cases

The system must handle unusual gameplay situations.

Examples include:

Inventory Full

When collecting an item with a full inventory, the player should receive a message indicating that no space is available.

Stack Overflow

If adding items would exceed the stack limit, a new stack should be created if space exists.

Missing Inventory Space During Crafting

Crafting should fail if the resulting item cannot fit in the inventory.

Destroyed Items

Items removed from the world due to scripted events should update inventory correctly.

---

## 18. Debugging Tools

During development, debugging tools should assist with testing inventory behavior.

Examples include:

Inventory state viewer

Displays all current inventory data.

Item spawn commands

Allows developers to spawn test items.

Stack limit testing

Simulates large quantities of items.

These tools help developers quickly diagnose inventory-related issues.

---

## 19. System Dependencies

The Inventory System interacts with several other gameplay systems.

Interaction System

Handles item pickups from the environment.

Crafting System

Consumes materials and creates new items.

Combat System

Uses ammunition and equipped weapons.

UI System

Displays inventory menus and item information.

Save System

Stores inventory data between sessions.

---

## 20. Future Expansion

The inventory system is designed to support additional features in future updates.

Potential future features include:

inventory expansion upgrades  
weapon modification slots  
specialized item containers  
context-sensitive quick item usage  

The modular structure ensures these features can be added without major redesign.

---