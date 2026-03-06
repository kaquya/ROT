# Stealth System

## 1. System Overview

The Stealth System governs how the player avoids detection by hostile organisms.

Stealth allows players to bypass enemies, conserve resources, and explore dangerous environments without direct combat.

The system determines:

- how visible the player is to enemies
- how much noise the player produces
- how enemies react to stealth movement
- how environmental factors influence detection

Stealth is not intended to make the player invisible.

Instead, it reduces the probability of enemy detection and creates opportunities to avoid combat.

This supports the survival horror gameplay philosophy where **avoidance is often safer than confrontation**.

---

## 2. Design Philosophy

The Stealth System follows several core principles.

### Risk and Reward

Stealth offers advantages but is not completely safe.

Enemies may still detect careless players.

Players must balance speed and caution.

---

### Environmental Awareness

The environment plays a major role in stealth gameplay.

Factors such as lighting, obstacles, and noise influence detection.

Players are encouraged to observe their surroundings carefully.

---

### Player Agency

Stealth mechanics should feel predictable and understandable.

Players must clearly understand why they were detected.

Detection events should always feel fair.

---

## 3. Stealth Factors

Enemy detection is influenced by several key factors.

### Visibility

How easy the player is to see.

Factors affecting visibility include:

- lighting conditions
- player posture
- distance from enemies
- movement speed

---

### Sound

How much noise the player generates.

Factors affecting sound include:

- walking or running
- interacting with objects
- weapon fire
- environmental interactions

Loud actions increase the risk of detection.

---

### Distance

The distance between the player and enemy greatly affects detection.

Closer proximity increases detection probability.

---

### Enemy Awareness

Different enemy types have different detection capabilities.

Examples:

- Stalkers have strong visual awareness.
- Rotters rely more heavily on sound.

---

## 4. Player Posture

The player can adjust posture to influence stealth effectiveness.

---

### Standing

Default posture.

Standing characters are easier to see and hear.

Movement speed is normal.

---

### Crouching

Stealth posture.

Crouching reduces:

- visibility
- movement noise

Movement speed is slower.

Enemies detect crouching players less easily.

---

### Running

Running increases speed but generates significant noise.

Running players are easier to detect.

Running should primarily be used to escape enemies rather than avoid them.

---

## 5. Lighting Influence

Lighting conditions affect how easily enemies can see the player.

Dark environments reduce visibility.

Bright environments increase visibility.

The system may evaluate lighting intensity around the player.

Example lighting categories:

Bright Light  
Player is easily visible.

Moderate Light  
Visibility is moderate.

Darkness  
Player visibility is reduced.

Lighting influence is combined with enemy visual detection.

---

## 6. Environmental Cover

Objects in the environment may provide visual cover.

Examples include:

- walls
- furniture
- large machinery
- vegetation

Enemies cannot see the player if line-of-sight is blocked.

Cover objects allow players to avoid detection even at close range.

---

## 7. Noise Generation

Player actions produce noise events that enemies may detect.

Examples include:

walking footsteps  
running footsteps  
weapon fire  
melee impacts  
interacting with objects  
breaking environmental objects

Each noise event has an associated **noise radius**.

Enemies within that radius may react to the sound.

---

## 8. Noise Propagation

Noise travels outward from the source.

The system determines which enemies are within hearing range.

Factors influencing noise propagation include:

- sound intensity
- distance
- environmental obstacles

Certain surfaces may produce louder footsteps.

Example:

Metal floors may amplify footstep sounds.

---

## 9. Noise Feedback

Players should receive subtle feedback about noise generation.

Examples include:

- louder footstep audio when running
- environmental sound cues
- enemy reactions to noise

Players learn to control their movement to avoid attracting attention.

---

## 10. Detection Threshold

Enemies require a certain level of suspicion before entering combat.

Detection typically follows several stages:

Unaware  
Enemy has detected nothing unusual.

Suspicious  
Enemy hears or sees something unusual.

Investigating  
Enemy searches the area.

Detected  
Enemy confirms the player's presence and attacks.

Stealth gameplay primarily occurs during the **suspicious and investigation stages**.

---

## 11. Stealth Modifiers

Several modifiers influence how effectively the player can remain hidden.

These modifiers adjust the probability that enemies detect the player.

Examples include:

Movement Modifier

Walking generates moderate noise.  
Crouching generates minimal noise.  
Running generates significant noise.

Lighting Modifier

Dark environments reduce visibility.  
Bright environments increase visibility.

Distance Modifier

Enemies detect nearby players more easily.

Enemy Type Modifier

Different enemy species possess different sensory abilities.

These modifiers combine to produce the final detection result.

---

## 12. Enemy Investigation Behavior

When enemies detect suspicious activity, they enter an investigation phase.

During this phase enemies may:

- move toward the disturbance
- scan the surrounding area
- pause and observe nearby movement

If the player remains hidden during the investigation phase, enemies eventually abandon the search.

If additional disturbances occur, enemies may escalate into aggressive behavior.

Investigation behavior creates tension without immediately forcing combat.

---

## 13. Stealth Escape Mechanics

Players may escape detection by breaking enemy awareness.

Common escape strategies include:

breaking line-of-sight  
moving into darkness  
hiding behind environmental cover  
creating distractions  

If enemies lose visual contact with the player, they move toward the player's **last known location**.

If the player remains hidden long enough, enemies eventually disengage.

This mechanic allows stealth recovery after detection.

---

## 14. Environmental Stealth Tools

The environment may provide tools that help players avoid detection.

Examples include:

Noise Distractions

Players may create noise to draw enemies away from their path.

Examples:

- throwing objects
- activating machinery
- triggering alarms

Environmental Hazards

Players may trigger environmental events that distract or damage enemies.

Examples:

- collapsing structures
- electrical systems
- explosive containers

These tools provide alternative solutions to dangerous encounters.

---

## 15. Stealth Failure

Stealth fails when enemies confirm the player's presence.

Triggers may include:

direct line-of-sight detection  
multiple noise events  
combat engagement  

When stealth fails, enemies transition into the **aggressive state**.

Combat systems then take control of the encounter.

Players may still escape combat by retreating and hiding.

---

## 16. Edge Cases

The Stealth System must handle unusual situations gracefully.

Examples include:

Multiple enemies detecting the player simultaneously.

Enemies losing sight of the player in crowded environments.

Player hiding near moving environmental objects.

Rapid state transitions between stealth and combat.

These situations must not cause erratic enemy behavior.

---

## 17. Debugging Tools

Development builds should include stealth debugging features.

Examples include:

Visibility meters  
Displays how visible the player currently is.

Noise radius visualization  
Displays the range of generated noise events.

Enemy detection indicators  
Shows when enemies begin detecting the player.

These tools help developers balance stealth gameplay.

---

## 18. System Dependencies

The Stealth System interacts with several other gameplay systems.

Player Controller

Provides player posture and movement speed data.

Enemy AI System

Uses stealth information to determine detection behavior.

Audio System

Handles sound generation and propagation.

Environment System

Provides lighting information and environmental cover.

Combat System

Handles transitions from stealth to combat.

---

## 19. Future Expansion

The stealth system is designed to support future gameplay features.

Possible additions include:

specialized stealth equipment  
environmental camouflage mechanics  
advanced distraction tools  
enemy scent tracking systems  

The modular design allows new stealth mechanics to be integrated without rewriting core systems.

---