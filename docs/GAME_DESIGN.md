# VOID STRAIN / 虚空菌株 — Game Design Document v0.2

## 1. High Concept

VOID STRAIN is a compact **2.5D science-fiction Metroidvania** centered on isolation, exploration, biomechanical horror, and mastery of movement.

The game uses stylized 3D characters and environments while keeping core traversal constrained to a side-scrolling plane.

The player explores Erebus-9, a failed research and extraction world where industrial infrastructure, alien biology, and an adaptive fungal organism have merged into a single hostile ecosystem.

The player begins underpowered, repeatedly encounters inaccessible spaces, acquires new abilities, and returns through old regions with new understanding.

## 2. Player Fantasy

The player should feel like:

- an isolated survivor entering a dead system that is not truly dead;
- a capable but initially limited explorer;
- a hunter whose mobility and combat vocabulary steadily expands;
- an investigator reconstructing events through places rather than exposition.

## 3. Visual Direction

### Rendering Style

- stylized 3D
- 2.5D side-scrolling gameplay
- strong silhouettes
- readable combat staging
- atmospheric lighting
- emissive accents
- fog, particles, dust, spores, heat haze, and environmental VFX
- detailed environments without photorealistic asset demands

### Production Principle

The project should avoid AAA realism.

Asset quality should come primarily from:

- silhouette
- lighting
- material contrast
- modular environment construction
- camera composition
- VFX
- coherent color direction

rather than ultra-dense geometry or expensive texture detail.

## 4. Core Pillars

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
- bodies/remains
- damaged laboratories
- containment failures
- environmental changes
- optional logs

Long mandatory dialogue should be rare.

## 5. Scope

Target first complete release:

- 3–5 hour first playthrough
- 5 major regions
- 5 bosses
- 12–18 normal enemy archetypes
- 6–8 major abilities
- optional upgrades and sequence breaks
- Windows first

## 6. World

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
- layered 3D wreckage behind and in front of the gameplay plane

### Region 2 — Mycelium Sink / 菌海深层

Purpose:

- first strong organic contrast
- introduce biological infestation and toxic traversal

Visual language:

- fungal growth
- damp caverns
- luminous spores
- purple/green bioluminescence
- large background fungal structures and deep parallax

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
- large-scale machinery crossing visual depth layers

### Region 4 — Null Lab / 零域研究所

Purpose:

- reveal the research program
- merge technology and organism

Visual language:

- sterile white architecture
- broken containment
- holographic systems
- biomechanical experiments
- glass, emissive panels, and controlled depth staging

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
- dramatic 3D boss and environment presentation

## 7. Player

Working designation: **Vessel-7**

Final identity and narrative details are intentionally unresolved.

### Presentation

- 3D skeletal character
- slim and agile silhouette
- integrated arm weapon
- strongly readable side profile
- animation optimized for side-on gameplay readability

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
4. Compact traversal form or equivalent
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

## 8. 2.5D Gameplay Rule

Normal gameplay takes place on a side-scrolling plane.

The player may visually exist in full 3D, but normal movement is constrained to the gameplay plane.

Depth is primarily used for:

- composition
- lighting
- foreground/background staging
- parallax
- VFX
- large boss presentation
- short cinematic camera moves

Free-roaming 3D exploration is outside current scope.

## 9. Initial Progression Concept

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

## 10. First Vertical Slice

The first playable milestone should contain approximately 20–30 minutes of content.

Required:

- 3D player controller constrained to 2.5D plane
- shooting
- damage/death
- one simple enemy
- one environmental hazard
- doors / room transitions
- one ability acquisition
- one locked path demonstrating ability gating
- basic HUD
- save/checkpoint proof of concept
- one lighting / VFX mood pass proving the visual direction

Suggested location:

Crash Cradle.

Suggested first enemy:

**Spore Crawler** — simple ground patrol/contact enemy.

Suggested first upgrade:

**Charge Beam** or **Dash**, depending on which better proves the intended game feel.

## 11. Boss Philosophy

Bosses should test learned mechanics rather than rely on huge health pools.

Each major boss should:

- have a clear spatial identity
- teach readable patterns
- reward movement mastery
- have at least one meaningful phase transition
- connect mechanically or narratively to its region
- take advantage of 3D scale and presentation without sacrificing gameplay readability

Candidate early boss:

**Grief Root** — a fungal neural mass rooted into industrial machinery.

## 12. Failure Conditions to Avoid

Do not let the project become:

- content-heavy before movement is fun
- dependent on long lore dumps
- a corridor shooter with token backtracking
- a collection of abilities that only act as colored keys
- excessively large for a first release
- visually ambitious enough to require AAA production values
- a free-roaming 3D game

## 13. Current Design Status

Locked:

- Godot 4
- stylized 3D rendering
- 2.5D side-scrolling gameplay
- GDScript
- Metroidvania structure
- science-fiction / biomechanical fungal theme
- compact 3–5 hour target
- five primary regions

Not yet locked:

- protagonist final appearance
- exact narrative
- final ability order
- map topology
- final boss roster
- exact 3D asset production pipeline
- camera focal length / framing
- environment modular kit specifications
