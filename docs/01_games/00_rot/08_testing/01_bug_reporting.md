# Bug Reporting

# 1. Overview

The Bug Reporting system defines how bugs are documented, tracked, and resolved during development.

Clear bug reporting is essential for maintaining development stability and preventing unresolved issues from accumulating.

Because ROT is a solo-developed project, bug reporting must remain:

- simple
- structured
- consistent
- quick to review

Even when working alone, maintaining proper bug documentation prevents issues from being forgotten.

---

# 2. What is a Bug

A bug is any issue where the game behaves differently from the intended design.

Examples include:

Gameplay systems failing  
Enemies behaving incorrectly  
Player becoming stuck in geometry  
Puzzle progression breaking  
Visual glitches  
Audio failing to trigger

Bugs may affect gameplay, performance, visuals, or audio.

---

# 3. Bug Reporting Goals

Bug reporting aims to achieve several goals.

Track issues clearly  
Identify affected systems  
Prioritize fixes  
Prevent repeated bugs  
Improve overall development stability

A well-documented bug report makes fixing the issue significantly easier.

---

# 4. When to Report a Bug

A bug should be reported whenever unexpected behavior occurs.

Examples include:

Game crashes  
Player cannot progress  
Enemy AI behaving incorrectly  
Items not appearing correctly  
UI elements failing to update

If behavior differs from the intended design, it should be recorded.

---

# 5. Bug Report Format

Every bug report should follow a consistent format.

Example bug report structure:

Bug ID:
Short Title:
System:
Severity:
Location:
Description:
Steps to Reproduce:
Expected Result:
Actual Result:
Status:

Each field helps identify and resolve the issue.

---

# 6. Bug ID

Each bug should receive a unique identifier.

Format:

BUG-0001
BUG-0002
BUG-0003

Bug IDs allow quick reference to specific issues.

---

# 7. Bug Title

The bug title should briefly describe the issue.

Example:

Player becomes stuck between wall and crate

The title should summarize the problem clearly.

---

# 8. Affected System

The bug report must specify the affected system.

Examples include:

Player Controller  
Combat System  
Enemy AI  
Inventory System  
Puzzle System  
Save System  
Audio System  
UI System

Identifying the system helps narrow down the cause.

---

# 9. Bug Severity

Each bug must include a severity level.

Severity categories include:

Critical  
Game-breaking issue.

High  
Major gameplay issue.

Medium  
Noticeable but not game-breaking.

Low  
Minor cosmetic issue.

Severity determines the priority of the fix.

---

# 10. Bug Location

The bug location specifies where the bug occurred.

Examples include:

Residential District  
Downtown District  
Police Station  
Harbor District  
Hospital  
Forest  
Halcyon Research Center

If the issue occurs in multiple locations, this should be noted.

---

# 11. Bug Description

The description explains the problem in detail.

It should include:

What happened  
When it happened  
Any unusual circumstances

Example:

Player becomes stuck when moving between a crate and wall inside the Harbor Warehouse.

The description should provide enough context to understand the issue.

---

# 12. Steps to Reproduce

A bug report must include clear steps to reproduce the issue.

Reproduction steps explain exactly how the bug occurred.

Example:

Steps to Reproduce

1. Enter Harbor Warehouse.
2. Walk toward the stacked crates near the entrance.
3. Move between the crate and wall.
4. Attempt to move backward.

Reproduction steps must be detailed enough that the issue can be repeated reliably.

If the bug cannot be reproduced consistently, this should be noted.

---

# 13. Expected Result

The expected result describes how the system should behave according to the design.

Example:

Player should move freely without becoming stuck between objects.

This field defines the intended system behavior.

---

# 14. Actual Result

The actual result describes what actually happened during gameplay.

Example:

Player becomes stuck between the crate and wall and cannot move.

Comparing expected and actual results helps identify the problem.

---

# 15. Bug Status

Each bug must have a status that indicates its current progress.

Common status values include:

Open  
The bug has been reported but not yet addressed.

Investigating  
The developer is analyzing the issue.

In Progress  
A fix is currently being implemented.

Fixed  
The bug has been resolved.

Verified  
The fix has been tested and confirmed.

Closed  
The issue is fully resolved.

Tracking bug status prevents issues from being forgotten.

---

# 16. Bug Tracking Workflow

The bug tracking process follows a simple workflow.

Bug Discovered
↓
Bug Report Created
↓
Severity Assigned
↓
Investigation
↓
Fix Implemented
↓
Verification Testing
↓
Bug Closed

Following this workflow ensures every issue is addressed systematically.

---

# 17. Screenshots and Evidence

Whenever possible, bug reports should include visual evidence.

Examples include:

Screenshots  
Video clips  
Error logs

Visual evidence helps identify the issue more quickly.

Example:

Screenshot showing player stuck between objects.

---

# 18. Temporary Workarounds

Some bugs may have temporary workarounds.

Example:

Reloading the save allows the player to escape the stuck position.

Documenting workarounds can help prevent frustration during testing.

---

# 19. Duplicate Bug Prevention

Before creating a new bug report, existing reports should be reviewed.

Duplicate bug reports create unnecessary confusion.

If the issue has already been reported, additional reports should reference the original bug ID.

Example:

Duplicate of BUG-0012

This helps maintain a clean bug tracking system.

---

# 20. Bug Archive

Once bugs are fixed and verified, they should be moved to an archive list.

Archived bugs remain documented for historical reference.

Archiving bugs allows developers to:

Review past issues  
Prevent repeated problems  
Track development stability over time

---

# 21. Bug Reporting Philosophy

Bug reporting should be consistent and disciplined throughout development.

Key principles include:

Report issues immediately  
Provide detailed reproduction steps  
Categorize severity accurately  
Verify fixes after implementation

Maintaining structured bug reports ensures development remains stable and manageable throughout the project lifecycle.

---