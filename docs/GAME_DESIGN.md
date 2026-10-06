# VOID STRAIN / 虚空菌株 — Game Design Document v0.1

## 1. High Concept

VOID STRAIN is a compact 2D science-fiction Metroidvania centered on isolation, exploration, biomechanical horror, and mastery of movement.

The player explores Erebus-9, a failed research and extraction world where industrial infrastructure, alien biology, and an adaptive fungal organism have merged into a single hostile ecosystem.

The player begins underpowered, repeatedly encounters inaccessible spaces, acquires new abilities, and returns through old regions with new understanding.

## 2. Player Fantasy

The player should feel like:

- an isolated survivor entering a dead system that is not truly dead;
- a capable but initially limited explorer;
- a hunter whose mobility and combat vocabulary steadily expands;
- an investigator reconstructing events through places rather than exposition.

## 3. Core Pillars

### Exploration

The world is interconnected and readable.

Players should frequently:

- see places they cannot yet reach;
- remember unusual doors, shafts, gaps, or environmental hazards;
- unlock shortcuts;
- return to earlier areas;
- discover optional upgrades through observation and movement mastery.

### Movement

Movement must be responsive before it is realistic.

Priorities:

- low input latency
- strong horizontal control
- forgiving jump behavior
- jump buffering
- coyote time
- readable acceleration/deceleration
- later abilities that meaningfully alter traversal

### Combat

Combat is ranged-first and mobility-oriented.

Enemies should pressure positioning rather than absorb excessive damage.

The player should learn to combine:

- movement
- aiming
- shooting
- dodging
- environmental awareness

### Environmental Storytelling

Story delivery should favor:

- architecture
- machinery
- corpses/remains
- damaged laboratories
- containment failures
- environmental changes
- optional logs

Long mandatory dialogue should be rare.

## 4. Scope

Target first complete release:

- 3–5 hour first playthrough
- 5 major regions
- 5 bosses
- 12–18 normal enemy archetypes
- 6–8 major abilities
- optional upgrades and sequence breaks
- Windows first

## 5. World

Planet / installation: **Erebus-9**

### Region 1 — Crash Cradle / 坠落区

Purpose:

- opening
- tutorialization through environment
- establish industrial ruin and isolation

Visual language:

- cold blue-gray metal
- emergency lighting
- rain / leaking coolant
- broken machinery

Core lessons:

- movement
- jumping
- shooting
- doors
- environmental hazards

### Region 2 — Mycelium Sink / 菌海深层

Purpose:

- first strong organic contrast
- introduce biological infestation and toxic traversal

Visual language:

- fungal growth
- damp caverns
- luminous spores
- purple/green bioluminescence

### Region 3 — Core Furnace / 熔核采掘带

Purpose:

- movement challenge
- industrial escalation

Visual language:

- furnaces
- mining machinery
- heat
- vertical shafts
- moving mechanical hazards

### Region 4 — Null Lab / 零域研究所

Purpose:

- reveal the research program
- merge technology and organism

Visual language:

- sterile white architecture
- broken containment
- holographic systems
- biomechanical experiments

### Region 5 — Celestial Parasite / 天穹寄生塔

Purpose:

- final ascent
- complete fusion of facility and organism
- endgame tests of mastered abilities

Visual language:

- impossible living architecture
- black/red biological structure
- open planetary vistas
- massive pulsating forms

## 6. Player

Working designation: **Vessel-7**

Final identity and narrative details are intentionally unresolved.

### Initial Actions

- run
- jump
- aim/fire energy weapon
- interact with basic world objects

### Candidate Major Abilities

The final list is not locked.

1. Charge Beam
2. Dash
3. Air Dash or upgraded Dash
4. Sphere Form
5. Environmental Protection
6. Phase Shift
7. Advanced Beam upgrade
8. Endgame traversal/combat ability

Every major ability should ideally support at least two of:

- traversal
- combat
- puzzle solving
- secrets
- sequence breaking

## 7. Initial Progression Concept

```text
Crash Cradle
    |
    v
Mycelium Sink
    |
    +------> optional return routes
    |
    v
Core Furnace
    |
    +------> opens major shortcuts
    |
    v
Null Lab
    |
    +------> world-state revelations
    |
    v
Celestial Parasite
```

This is a macro progression only.

The final map should include loops, shortcuts, optional branches, and cross-region connections.

## 8. First Vertical Slice

The first playable milestone should contain approximately 20–30 minutes of content.

Required:

- player controller
- shooting
- damage/death
- one simple enemy
- one environmental hazard
- doors / room transitions
- one ability acquisition
- one locked path demonstrating ability gating
- basic HUD
- save/checkpoint proof of concept

Suggested location:

Crash Cradle.

Suggested first enemy:

**Spore Crawler** — simple ground patrol/contact enemy.

Suggested first upgrade:

**Charge Beam** or **Dash**, depending on which better proves the intended game feel.

## 9. Boss Philosophy

Bosses should test learned mechanics rather than rely on huge health pools.

Each major boss should:

- have a clear spatial identity
- teach readable patterns
- reward movement mastery
- have at least one meaningful phase transition
- connect mechanically or narratively to its region

Candidate early boss:

**Grief Root** — a fungal neural mass rooted into industrial machinery.

## 10. Failure Conditions to Avoid

Do not let the project become:

- content-heavy before movement is fun
- dependent on long lore dumps
- a corridor shooter with token backtracking
- a collection of abilities that only act as colored keys
- excessively large for a first release

## 11. Current Design Status

Locked:

- Godot 4
- 2D
- GDScript
- Metroidvania structure
- science-fiction / biomechanical fungal theme
- compact 3–5 hour target
- five primary regions

Not yet locked:

- protagonist appearance
- exact narrative
- final ability order
- map topology
- final boss roster
- art production method
- pixel art vs high-resolution 2D presentation
