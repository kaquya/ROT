# ROT Exposure System

Version: 1.0  
Status: Core Gameplay System

---

# 1. Purpose of the Rot Exposure System

The **Rot Exposure System** is the primary signature mechanic of ROT.

While the Rot infects the environment and enemies, the player is **not immune to its influence**.

As the player interacts with contaminated environments, enemies, and Rot growth, **Rot contamination slowly accumulates**.

This contamination affects:

- perception
- enemy behavior
- environmental stability
- player psychological state

The Rot Exposure System introduces a **progressive tension mechanic** that blends gameplay with narrative themes.

The system reinforces the idea that **survival comes at a cost**.

---

# 2. Design Goals

The Rot Exposure system exists to achieve several gameplay goals.

### Psychological Horror Integration

Exposure causes visual and audio distortions that increase tension.

### Risk-Based Exploration

Highly contaminated areas provide valuable resources but increase Rot exposure.

### Narrative Integration

Elena’s gradual exposure connects the gameplay experience with the narrative of Rot influence.

### Dynamic Gameplay Variation

Exposure changes how enemies behave and how the environment reacts to the player.

---

# 3. Rot Exposure Meter

The player has a hidden or semi-visible **Rot Exposure Meter**.

Exposure increases when interacting with Rot contamination.

### Exposure Range


0 → 100 Rot Exposure


Example UI display:

- subtle UI indicator
- pulse effect around screen edges
- audio heartbeat cues

At high exposure levels the UI may begin to distort.

---

# 4. Exposure Sources

Exposure increases when the player encounters Rot-infected elements.

---

## Rot Growth

Environmental Rot structures slowly contaminate the player.

Examples:

- Rot walls
- Rot tendrils
- infected structures

Exposure Rate:


+2 exposure per second when near heavy growth


---

## Enemy Attacks

Certain enemies transfer Rot contamination when they damage the player.

Example values:


Rotter hit: +5 exposure
Stalker hit: +10 exposure
Spliced hit: +15 exposure
Boss attack: +20 exposure


---

## Rot Pools

Some areas contain concentrated Rot biomass.

Entering these zones rapidly increases exposure.

Example:


+10 exposure per second


These areas are typically high-risk/high-reward locations.

---

## Environmental Events

Major Rot environments may cause spikes in exposure.

Examples:

- Rot storms
- Rot bloom pulses
- boss arena corruption

These events may temporarily overwhelm the player.

---

# 5. Exposure Stages

Rot exposure affects the player in escalating stages.

---

# Stage 0 – Clean (0–20)

The player is unaffected.

Environment appears normal.

Enemy behavior remains unchanged.

---

# Stage 1 – Contamination (21–40)

Early symptoms appear.

Visual Effects:

- slight screen distortion
- subtle environmental pulsing
- faint Rot whispers

Gameplay Effects:

- enemies slightly more sensitive to sound
- minor aim instability

Narrative Notes:

This stage reflects early neurological influence.

---

# Stage 2 – Infection (41–60)

The Rot begins altering the player's perception.

Visual Effects:

- environmental flickers
- shadow distortions
- distant hallucination shapes

Audio Effects:

- whispers
- distorted environmental sounds

Gameplay Effects:

- enemies detect player slightly faster
- hallucination enemies may appear briefly
- false environmental audio cues

Narrative Notes:

The Rot is interfering with the player's sensory processing.

---

# Stage 3 – Rot Influence (61–80)

The player becomes heavily affected.

Visual Effects:

- stronger hallucinations
- temporary environment shifts
- Rot growth appearing in areas that are not actually infected

Gameplay Effects:

- enemies actively track the player more aggressively
- hallucination enemies appear more frequently
- stamina regeneration reduced

Narrative Notes:

The Rot begins overriding the player’s biological systems.

---

# Stage 4 – Critical Exposure (81–100)

Severe contamination occurs.

Effects include:

- severe screen distortion
- disorienting audio hallucinations
- unpredictable environmental events

Gameplay Effects:

- enemies become highly aggressive
- player aim stability heavily reduced
- stamina regeneration severely slowed

If exposure reaches 100:

The player experiences **Rot Collapse**.

---

# 6. Rot Collapse

When Rot exposure reaches maximum level:

The player experiences temporary biological failure.

Effects:

- loss of control
- screen blackout
- severe hallucination sequence

After collapse:

The player wakes in the **nearest safe zone**.

Exposure resets to a lower level.

This mechanic prevents permanent punishment while reinforcing the danger of contamination.

---

# 7. Exposure Reduction

Exposure does not permanently increase.

Players can reduce contamination.

---

## Safe Zones

Rot exposure slowly decreases inside safe zones.

Example reduction rate:


-5 exposure per minute


Safe zones include:

- Elena’s house
- ranger cabin
- hospital staff room
- research facility security room

---

## Medical Treatments

Special consumables can reduce exposure.

Example item:


Anti-Rot Stabilizer


Effect:


-30 Rot Exposure


These items are rare and valuable.

---

## Environmental Purification

Some puzzle events temporarily reduce exposure.

Examples:

- activating purification systems
- burning Rot biomass
- restoring environmental power systems

These events reinforce environmental storytelling.

---

# 8. Enemy Interaction with Exposure

Certain enemies react differently to contaminated players.

Examples:

Stalkers:


High exposure increases detection radius


Spliced:


Attracted to heavily contaminated players


Boss entities:


More aggressive attack patterns


This creates dynamic combat situations.

---

# 9. Hallucination Events

At higher exposure levels the player may experience hallucinations.

Examples include:

- enemies appearing where none exist
- doors briefly changing location
- fake Rot growth
- shadow figures watching the player

Hallucinations should be **rare but unsettling**.

They should never fully remove player control.

---

# 10. Narrative Integration

The Rot Exposure system reflects Elena’s biological interaction with the Rot.

Throughout the story, players may discover:

- Elena appears unusually resistant to Rot contamination
- Halcyon may have studied Rot-human compatibility
- Daniel may have been exposed before the outbreak

These hints build narrative mystery.

---

# 11. Technical Implementation Overview

The exposure system tracks a single variable:


rotExposureValue


This value updates continuously.

Example pseudo logic:


if nearRotGrowth:
rotExposureValue += exposureRate

if hitByEnemy:
rotExposureValue += enemyExposureValue

if inSafeZone:
rotExposureValue -= recoveryRate


The exposure value determines which stage is active.

Each stage activates visual and gameplay modifiers.

---

# 12. Design Balance Notes

The Rot Exposure System must create tension without overwhelming the player.

Design rules:

- exposure should increase slowly during normal exploration
- high exposure should feel dangerous but manageable
- players should have multiple ways to recover
- hallucinations should remain rare and impactful

Proper balancing will occur during playtesting.

---

# 13. Future Expansion Possibilities

Later games in the ROT franchise may expand the system.

Possible additions include:

- Rot mutations affecting player abilities
- permanent exposure consequences
- different Rot strains

For the first game, the system focuses on **psychological influence and environmental tension**.

---