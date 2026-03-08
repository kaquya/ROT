# Bug Reporting

Project: ROT  
Version: 1.1  
Document Type: Testing  
Category: Quality Assurance  
Scope: ROT (Game)  
Status: Core Reference

---

# 1. Overview

This document defines the bug reporting process used during the development of ROT.

A structured bug reporting process ensures that issues discovered during development and testing are documented clearly, prioritized correctly, and resolved efficiently.

The goal of bug reporting is not only to record problems but also to provide developers with enough information to reproduce and fix issues quickly.

This document defines:

- what qualifies as a bug
- how bugs should be reported
- how bug reports should be structured
- how bugs are prioritized and tracked

---

# 2. What is a Bug

A bug is any behavior in the game that differs from the intended design or expected system behavior.

Examples include:

- gameplay systems not functioning correctly
- enemies behaving incorrectly
- puzzles failing to trigger
- visual glitches
- audio issues
- performance problems
- crashes or freezes

A bug may be technical, gameplay-related, or content-related.

---

# 3. What is Not a Bug

Not all issues are bugs.

Examples of issues that are not considered bugs include:

- design feedback or suggestions
- balance concerns
- unclear mechanics
- personal preference feedback

These should be recorded separately as design feedback or improvement suggestions.

---

# 4. Bug Reporting Workflow

The bug reporting process follows a structured workflow.

Step 1  
Issue is discovered during development or testing.

Step 2  
Tester attempts to reproduce the issue.

Step 3  
Bug report is created with detailed information.

Step 4  
The issue is added to the project tracking system.

Step 5  
Developers investigate and resolve the issue.

Step 6  
The bug is retested to confirm the fix.

---

# 5. Bug Report Requirements

A bug report must contain enough information to reproduce the issue.

Every report should include the following fields.

Title  
A short description of the issue.

Example:  
Enemy becomes stuck in patrol loop near hospital corridor.

---

Description  
A clear explanation of the problem.

Example:  
The enemy enters the patrol state but repeatedly walks into a wall and does not transition to another behavior.

---

Reproduction Steps  
Step-by-step instructions describing how to reproduce the bug.

Example:

1. Load hospital district save file  
2. Enter quarantine wing corridor  
3. Approach enemy patrol route  
4. Observe enemy behavior

---

Expected Behavior  
What the system should do.

Example:  
Enemy should navigate the patrol path normally.

---

Actual Behavior  
What actually occurs.

Example:  
Enemy repeatedly walks into a wall and becomes stuck.

---

Environment  
Information about the build or testing environment.

Examples include:

- game version
- platform
- test build identifier

---

Severity  
An estimate of how serious the bug is.

Severity levels are defined later in this document.

---

Attachments  
Screenshots, videos, or logs when possible.

These greatly improve the speed of debugging.

---

# 6. Bug Severity Levels

Bugs should be categorized based on severity.

---

Critical

Critical bugs break the game or prevent progress.

Examples:

- game crashes
- corrupted save files
- progression blockers

These must be fixed immediately.

---

High

High severity bugs significantly impact gameplay.

Examples:

- enemies not attacking
- puzzles failing to trigger
- major visual errors

These should be prioritized for resolution.

---

Medium

Medium severity bugs affect gameplay but do not prevent progress.

Examples:

- animation glitches
- incorrect audio triggers
- minor AI issues

These should be fixed when time allows.

---

Low

Low severity bugs are minor issues.

Examples:

- small visual errors
- minor sound issues
- cosmetic problems

These can be addressed later in development.

---

# 7. Bug Priority

Priority determines when a bug should be fixed.

Priority depends on:

- severity
- gameplay impact
- development schedule

A low severity bug may become high priority if it affects an important gameplay system.

---

# 8. Reproducibility

Bug reports should indicate how consistently the issue occurs.

Possible classifications include:

Always  
Occurs every time.

Often  
Occurs frequently but not always.

Rare  
Occurs occasionally.

Unknown  
Unable to reproduce consistently.

Reproducibility helps developers estimate the complexity of the issue.

---

# 9. Retesting

Once a developer resolves a bug, the issue must be retested.

Retesting verifies that:

- the original issue is fixed
- no new issues were introduced

If the bug persists, the report should be updated and reopened.

---

# 10. Documentation and Tracking

All bugs should be tracked in the project's issue tracking system.

Each bug should have:

- a unique identifier
- status updates
- assigned developer

Tracking allows the team to monitor progress and avoid duplicate reports.

---

# 11. Communication

Clear communication is essential for efficient bug resolution.

Testers should communicate with developers when:

- reproduction steps are unclear
- additional information is required
- the issue cannot be reproduced

Effective collaboration speeds up the debugging process.

---

# 12. Purpose of This Document

This document defines the bug reporting process used during the development of ROT.

By following a consistent reporting structure, the development team can identify, prioritize, and resolve issues efficiently throughout the production cycle.

---