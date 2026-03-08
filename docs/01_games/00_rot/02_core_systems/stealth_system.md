# Stealth System

Project: ROT  
Version: 1.1  
Document Type: Gameplay System  
Category: Stealth  
Scope: ROT (Game)  
Status: Core Reference  

---

## 1. Overview

The Stealth System defines how players can avoid detection by hostile organisms within the Rot ecosystem.

Stealth is a core survival strategy in ROT. Combat is dangerous and resource intensive, so players are often encouraged to avoid enemies rather than confront them directly.

Stealth gameplay is built around three primary elements:

- visibility
- noise
- enemy detection

Players who move carefully, remain hidden, and control the sounds they produce can navigate hostile areas without triggering combat encounters.

---

## 2. Stealth Philosophy

Stealth in ROT should feel grounded and intuitive.

Players should understand why they were detected or why they remained hidden. Environmental conditions, player movement, and sound all contribute to stealth outcomes.

The system should reward patience and observation.

Stealth is not intended to make the player invisible. Instead, it allows the player to reduce the chance of being noticed.

Mistakes should increase tension but still allow opportunities to recover if the player reacts quickly.

---

## 3. Visibility

Visibility determines how easily enemies can see the player.

Several factors influence player visibility.

### Lighting Conditions

Dark environments make the player harder to detect. Brightly lit areas increase the chance of enemy detection.

Light sources such as lamps, emergency lighting, or daylight may expose the player if they move through illuminated areas.

Players may need to navigate shadows or avoid open spaces to remain unseen.

---

### Player Posture

The player's stance influences how visible they are.

- standing posture produces the highest visibility  
- crouching reduces the player's visible profile  
- moving slowly while crouched improves stealth effectiveness  

Crouching is the primary stealth movement mode.

---

### Environmental Cover

Environmental objects can block enemy line of sight.

Examples of useful cover include:

- furniture
- walls
- structural debris
- large environmental objects

Players should use these elements to remain hidden while observing enemy behavior.

---

## 4. Noise

Noise represents the sound produced by player movement and actions.

Many enemies rely heavily on sound to locate potential targets.

### Movement Noise

Different movement types produce different noise levels.

- sprinting produces loud noise and attracts attention  
- walking produces moderate noise  
- crouched movement produces minimal noise  

Players should adjust their movement speed depending on nearby threats.

---

### Environmental Noise

Certain environmental interactions may produce sound.

Examples include:

- stepping on loose debris  
- knocking objects over  
- opening doors quickly  

These sounds may alert nearby enemies.

Players must remain aware of their surroundings to avoid creating unnecessary noise.

---

### Combat Noise

Weapons and combat actions produce significant noise.

Examples include:

- firearm discharge  
- melee impacts  
- environmental destruction during combat  

These sounds may attract additional enemies to the area.

---

## 5. Enemy Detection

Enemy detection is determined by how creatures interpret visibility and noise.

Enemies evaluate their surroundings using two primary detection methods.

### Visual Detection

Enemies detect the player when they have a clear line of sight.

Detection speed depends on:

- distance between enemy and player  
- lighting conditions  
- player movement speed  
- player posture  

Moving quickly in bright areas increases the chance of visual detection.

---

### Audio Detection

Enemies may investigate sounds produced by the player.

When a sound is detected, enemies may:

- move toward the source of the sound  
- search the surrounding area  
- enter an alert state  

Audio detection creates tension because enemies may approach even if they have not seen the player.

---

## 6. Enemy Awareness States

Enemies transition between different awareness states depending on the information they receive.

Typical states include:

### Passive State

Enemies patrol or idle without awareness of the player.

### Suspicious State

Enemies investigate unusual sounds or visual disturbances.

### Alert State

Enemies have detected the player and actively pursue or attack.

These states help communicate enemy behavior to the player.

---

## 7. Player Stealth Strategies

Players can use several strategies to remain undetected.

Examples include:

- moving slowly through shadowed environments  
- crouching to reduce visibility and noise  
- using environmental cover to block line of sight  
- observing enemy patrol patterns before moving  
- avoiding unnecessary environmental interactions  

Successful stealth requires careful observation and patience.

---

## 8. Integration with Other Systems

The Stealth System interacts with several gameplay systems.

Examples include:

- Player Controller System for movement and crouching  
- Combat System for encounters triggered by detection  
- Enemy AI System for detection and pursuit behavior  
- Environmental Design for lighting and cover placement  

These interactions ensure that stealth is integrated into the overall gameplay experience.

---

## 9. Purpose of This Document

This document defines the stealth mechanics used in ROT.

It establishes how visibility, noise, and enemy detection interact to create stealth gameplay.

Following these guidelines ensures that stealth encounters remain tense, readable, and consistent with the survival horror identity of the game.

---