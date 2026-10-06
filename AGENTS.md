# VOID STRAIN — Codex / Coding Agent Instructions

## 1. Project Identity

VOID STRAIN is a **2.5D Metroidvania** made with Godot 4.x and GDScript.

The world is rendered in 3D, but core player traversal is constrained to a side-scrolling gameplay plane.

Primary design pillars:

1. Responsive movement and shooting.
2. Interconnected exploration.
3. Ability gating that changes how old spaces are understood.
4. Strong environmental storytelling with minimal exposition.
5. Compact scope and high polish over content quantity.
6. Stylized 3D presentation with strong atmosphere and readable silhouettes.

Do not expand the project scope without an explicit request.

## 2. Technical Constraints

- Engine: Godot 4.x stable.
- Language: GDScript only unless explicitly requested otherwise.
- Target platform: Windows first.
- Rendering: 3D.
- Gameplay presentation: 2.5D side-scroller.
- Core player body: CharacterBody3D.
- Camera: Camera3D.
- Player gameplay movement is constrained to a defined side-scrolling plane.
- Prefer native Godot systems over third-party frameworks.
- Avoid unnecessary addons.
- Do not introduce C#, C++, GDExtension, or external runtimes without explicit approval.
- Keep systems modular and inspectable in the Godot editor.

## 3. Repository Structure

Use the following structure when applicable:

```text
assets/
  audio/
  fonts/
  materials/
  models/
  textures/
  vfx/

docs/

scenes/
  autoload/
  enemies/
  levels/
  player/
  props/
  ui/

scripts/
  components/
  enemies/
  player/
  systems/
  ui/

tests/
```

Do not create deeply nested folders without a clear reason.

## 4. 2.5D Gameplay Rules

The project is visually 3D but mechanically side-scrolling.

Unless a feature explicitly requires depth movement:

- Player locomotion occurs on X/Y.
- Z movement should be constrained or corrected to the active gameplay plane.
- Enemies intended for the same lane should obey the same gameplay-plane constraint.
- Camera movement should reinforce side-scrolling readability.
- Background and foreground objects may use full 3D depth for composition, parallax, lighting, and atmosphere.
- Do not turn ordinary traversal into free-roaming 3D movement.

Depth may still be used for:

- visual composition
- cinematic camera moves
- foreground/background staging
- boss presentation
- environmental effects
- limited scripted transitions

## 5. Architecture Rules

### Player

The player must not become one monolithic script.

Separate responsibilities when they become non-trivial:

- input
- locomotion
- gameplay-plane constraint
- combat
- health/damage
- abilities
- animation
- interaction
- camera coordination

Prefer composition and small components over large inheritance trees.

### Animation

The player and major enemies are expected to use 3D skeletal animation.

Do not bake gameplay logic into animation clips.

Gameplay state should drive animation, not the other way around.

Use AnimationTree / state-machine-style control where appropriate.

### Abilities

Traversal/combat upgrades must use a consistent ability state/API.

Examples:

- Charge Beam
- Dash
- Air Dash
- Sphere / Compact Form if retained
- Environmental Protection
- Phase Shift

Do not hard-code unrelated ability checks throughout the project.

### Damage

Player, enemies, hazards, and projectiles should converge on a consistent damage/health interface.

Avoid bespoke damage logic for every enemy.

### Enemies

Enemies should share reusable components where sensible:

- health
- hitbox/hurtbox
- patrol/navigation
- contact damage
- projectile firing
- gameplay-plane constraint

Enemy-specific behavior should remain local to the enemy.

### Levels

Rooms and transitions must be reusable.

Avoid room scripts that directly depend on one specific global progression sequence unless required by design.

## 6. Coding Rules

- Use typed GDScript where practical.
- Use descriptive English identifiers.
- Keep functions small and single-purpose.
- Avoid unexplained magic numbers; expose tuning values with `@export` where useful.
- Prefer signals for loosely coupled events.
- Do not use fragile deep node paths.
- Avoid global singletons unless the data is genuinely global.
- Comment intent, not obvious syntax.
- Do not rewrite working systems merely for stylistic preference.

## 7. AI Change Discipline

For every task:

1. Read the relevant existing files before modifying them.
2. Make the smallest coherent change that satisfies the request.
3. Preserve existing behavior unless the task explicitly changes it.
4. Do not opportunistically refactor unrelated code.
5. Report every file created or changed.
6. State any assumptions.
7. Call out editor/manual steps that cannot be completed from code alone.

When a task is ambiguous, prefer the interpretation that changes the least code and scope.

## 8. Validation

After changes, perform the strongest available validation.

At minimum:

- ensure GDScript parses
- check scene/resource paths
- check for missing referenced files
- inspect errors produced by headless Godot if available

When Godot is available from the command line, prefer a headless project check such as:

```bash
godot --headless --path . --quit
```

If a runnable test scene exists, use it when appropriate.

Never claim a change works in-game if it has not actually been executed.

## 9. Git Discipline

- Keep commits focused.
- Do not commit generated caches or editor metadata.
- Do not commit `.godot/`.
- Do not rewrite history unless explicitly requested.
- Avoid large binary assets until they are actually needed.

## 10. Design Authority

The documents under `docs/` define the current intended game design.

If code and design documents conflict:

1. do not silently choose one;
2. identify the conflict;
3. preserve current behavior unless explicitly instructed to change it.

## 11. Scope Guardrails

The initial target is approximately:

- 3–5 hours
- 5 primary regions
- 5 bosses
- 12–18 normal enemy types
- 6–8 major abilities

Do not turn VOID STRAIN into:

- an open-world game
- a procedural roguelike
- a multiplayer game
- a free-roaming 3D exploration game
- a live-service project
- a 15+ hour campaign

unless explicitly directed.
