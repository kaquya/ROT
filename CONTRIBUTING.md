# Contributing Guide

Project: ROT
Documentation Version: 1.1
Scope: Documentation Repository
Status: Active Guidelines

---

# 1. Overview

This document defines the guidelines for contributing to the ROT documentation repository.

The goal of these rules is to maintain:

* consistent structure
* clear formatting
* reliable cross-referencing
* long-term maintainability

All contributors should follow these guidelines when creating or editing documentation.

---

# 2. Repository Structure

All documentation is located inside the `docs/` directory.

The repository is organized into two primary sections:

```
docs/
    00_franchise/
    01_games/
```

### Franchise Documentation

```
docs/00_franchise/
```

Contains documentation that defines the overall ROT universe, including:

* worldbuilding
* visual identity
* creature design
* environment design
* franchise direction

These documents apply to **all ROT projects**.

---

### Game Documentation

```
docs/01_games/00_rot/
```

Contains documentation specific to the ROT game project.

These documents include:

* gameplay systems
* level design
* enemy design
* engineering architecture
* production planning
* narrative lore

---

# 3. File Naming Rules

All file names must follow these conventions.

### Use lowercase

All file names must be lowercase.

Example:

```
combat_system.md
enemy_ai_system.md
rot_exposure_system.md
```

---

### Use underscores instead of spaces

Example:

```
player_controller_system.md
inventory_system.md
world_map.md
```

Do not use:

```
Player Controller System.md
inventory system.md
```

---

### Use descriptive names

File names should clearly describe the system or concept they document.

Example:

```
puzzle_system.md
enemy_ai_system.md
audio_gameplay_system.md
```

Avoid vague names such as:

```
systems.md
notes.md
design.md
```

---

# 4. Document Header Standard

All documents must begin with a standard header.

Example:

```
Project: ROT
Version: 1.1
Document Type: System / Design / Lore / Engineering / Production
Category: folder classification
Status: Draft / Core Reference / Complete
```

Example:

```
Project: ROT
Version: 1.1
Document Type: System
Category: Core Gameplay Systems
Status: Core Reference
```

This header ensures documents remain consistent across the repository.

---

# 5. Formatting Rules

Documentation should follow a consistent formatting style.

### Headings

Use markdown headings in hierarchical order.

Example:

```
# Main Title
## Section
### Subsection
```

Avoid skipping heading levels.

---

### Lists

Use bullet lists for grouped concepts.

Example:

```
- combat mechanics
- enemy behavior
- exploration systems
```

---

### Code blocks

Use code blocks for diagrams or structural examples.

Example:

```
explore → scavenge → survive → uncover story → progress
```

---

### Section spacing

Maintain clear spacing between sections to improve readability.

---

# 6. Cross References

When a document references another system or concept, include a **Related Documents** section.

Example:

```
## Related Documents

combat_system.md  
enemy_ai_system.md  
ai_perception_system.md
```

Cross references help maintain connections between documentation files.

---

# 7. Versioning Rules

All documents use the same documentation version number.

Current version:

```
ROT Documentation – Version 1.1
```

The version number should only change when:

* major structural changes occur
* gameplay systems are significantly redesigned
* documentation architecture is reorganized

Minor edits do not require version updates.

---

# 8. Writing Style Guidelines

Documentation should follow a clear and direct writing style.

Guidelines include:

* use simple and precise language
* avoid unnecessary repetition
* prefer short paragraphs
* describe systems objectively

Do not use em dashes in documentation.

Use standard sentence punctuation instead.

---

# 9. System Documentation Guidelines

When documenting gameplay systems, include the following sections whenever applicable:

* Overview
* Purpose
* System behavior
* Integration with other systems
* Gameplay impact

This ensures system documentation remains consistent across the project.

---

# 10. Lore Documentation Guidelines

Narrative documents should focus on world consistency rather than gameplay mechanics.

Lore documentation should support:

* environmental storytelling
* collectible documents
* narrative context for locations

Avoid explaining every mystery in the lore.

Some ambiguity should remain to support the horror themes of ROT.

---

# 11. Editing Existing Documents

When modifying an existing document:

1. Preserve the original structure when possible.
2. Avoid duplicating information that exists in other documents.
3. Update cross references if related documents change.
4. Ensure terminology matches the glossary definitions.

---

# 12. Adding New Documents

When adding a new document:

1. Place the file in the correct folder category.
2. Follow the file naming rules.
3. Use the standard document header.
4. Add cross references where appropriate.

If the document introduces new terminology, update the glossary.

---

# 13. Purpose of This Document

This guide ensures that the ROT documentation remains organized, consistent, and easy to maintain as the project grows.

Following these guidelines helps maintain a professional and scalable documentation system for the ROT project.

---