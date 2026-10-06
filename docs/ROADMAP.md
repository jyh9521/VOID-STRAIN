# VOID STRAIN — Production Roadmap v0.2

## Milestone 0 — Bootstrap

Goal: repository and Godot project can be safely worked on by both the developer and Codex.

- [x] Repository created
- [x] Codex instructions
- [x] Initial GDD
- [x] Lock 2.5D stylized 3D direction
- [ ] Create Godot 4 project
- [ ] Add project folder structure
- [ ] Add input actions
- [ ] Add minimal 3D test scene
- [ ] Confirm headless project validation

## Milestone 1 — 2.5D Movement Prototype

Goal: moving an untextured capsule / placeholder character is already fun.

- [ ] CharacterBody3D player
- [ ] side-scrolling gameplay-plane constraint
- [ ] horizontal movement
- [ ] acceleration/deceleration
- [ ] jump
- [ ] variable jump height
- [ ] coyote time
- [ ] jump buffer
- [ ] wall collision
- [ ] Camera3D behavior
- [ ] controller support

Exit criterion:

The player controller is enjoyable in a graybox 3D test room before combat or final art is added.

## Milestone 2 — Combat Prototype

- [ ] aiming rules
- [ ] energy projectile
- [ ] fire rate
- [ ] enemy health
- [ ] player health
- [ ] hitboxes/hurtboxes
- [ ] knockback / hit reaction
- [ ] simple 3D enemy
- [ ] death and respawn
- [ ] animation-state proof of concept

## Milestone 3 — 2.5D Presentation Proof

Goal: prove that the project looks good before committing to full asset production.

- [ ] one modular sci-fi environment kit
- [ ] side-on camera composition
- [ ] foreground/background depth layers
- [ ] basic lighting pass
- [ ] emissive materials
- [ ] fog / particles / atmospheric VFX
- [ ] one skeletal player placeholder or prototype model

Exit criterion:

A single room should already communicate the intended stylized 3D identity.

## Milestone 4 — Metroidvania Proof

- [ ] reusable room structure
- [ ] transitions
- [ ] doors
- [ ] ability system
- [ ] first ability pickup
- [ ] ability gate
- [ ] persistent progression
- [ ] checkpoint/save prototype
- [ ] map prototype

Exit criterion:

A player can encounter an inaccessible route, acquire an ability elsewhere, return, and use that ability to progress.

## Milestone 5 — Crash Cradle Vertical Slice

Target: 20–30 minutes.

- [ ] graybox map
- [ ] first modular environment art pass
- [ ] final-ish player prototype
- [ ] 2–3 enemy/hazard types
- [ ] one major ability
- [ ] secrets
- [ ] environmental storytelling
- [ ] HUD
- [ ] audio pass
- [ ] lighting/VFX pass
- [ ] one mini-boss or boss encounter

## Milestone 6 — Full Game Production

Build the five-region game around validated systems.

Regions:

1. Crash Cradle
2. Mycelium Sink
3. Core Furnace
4. Null Lab
5. Celestial Parasite

Do not begin full content production until Milestone 5 is fun.

## Milestone 7 — Content Lock

No new major mechanics after this point.

Focus only on:

- missing content
- progression integrity
- balance
- sequence-break handling
- art/audio completion

## Milestone 8 — Polish / Release Candidate

- [ ] full playthrough from new save
- [ ] progression deadlock testing
- [ ] save/load testing
- [ ] controller testing
- [ ] resolution/window testing
- [ ] performance
- [ ] accessibility basics
- [ ] localization readiness
- [ ] Windows export
- [ ] credits/licenses
- [ ] release build smoke test
