# PLAN.md Creation: 2D Side-Scrolling Shooter

## Summary

Create `E:\Cursor Repo\sidescroller\PLAN.md` as the concrete product/design plan for the MVP: a browser-based 2D side-scrolling shooter inspired by `R-Type` and `Gradius`, built with Next.js and PixiJS.

The document will define the game as a focused horizontal shooter with one playable ship, staged enemy waves, powerups, boss encounters, local high scores, and escalating difficulty.

## PLAN.md Content

The file will include these sections:

- **Game Vision**
  - Working title: `2D Side Scrolling Shooter`
  - Genre: horizontal arcade shooter
  - Inspirations: `R-Type` for deliberate enemy patterns and environmental pressure; `Gradius` for powerups, scrolling stages, and readable arcade action
  - MVP target: a polished single-player browser game loop, not a full campaign

- **Player Goal**
  - Survive each scrolling stage
  - Destroy enemy waves and hazards
  - Collect score and powerups
  - Defeat the stage boss
  - Reach the highest possible score across runs

- **Main Loop**
  - Start run from title/menu
  - Enter side-scrolling stage
  - Dodge enemies, bullets, terrain, and hazards
  - Shoot continuously or manually
  - Collect powerups and score items
  - Fight a boss at the end of the stage
  - Win the stage or lose all lives
  - Save local high score and return to menu

- **Inputs and Controls**
  - Keyboard-first controls:
    - Arrow keys or WASD: move ship
    - Space: fire primary weapon
    - Shift: focused slow movement
    - Enter: start/pause/confirm
    - Escape: pause/back
  - Gamepad-ready assumptions:
    - Left stick or D-pad: move
    - Face button: fire
    - Shoulder/trigger: focus movement
  - Mouse/touch are out of scope for MVP unless added later.

- **Win and Fail States**
  - Win: defeat the stage boss and clear the level
  - Fail: lives reach zero
  - Damage model:
    - MVP starts with lives and temporary invulnerability after hit
    - Collision with enemies, bullets, or lethal terrain removes one life
  - Run result screen shows score, kills, stage reached, and high score update.

- **Progression and Difficulty**
  - MVP progression:
    - Stage 1 playable from start
    - Later milestones add more stages
  - Difficulty escalates through:
    - Denser enemy waves
    - Faster bullets
    - More complex movement patterns
    - Environmental obstacles
    - Boss phase changes
  - Powerups:
    - Weapon spread
    - Laser/beam upgrade
    - Missile or option drone
    - Shield
    - Score bonus
  - LocalStorage stores high score and simple settings.

- **Visual Direction**
  - Pixel-art-inspired or crisp 2D arcade sci-fi
  - Side-view spaceship action with strong silhouettes
  - Readable enemy bullets and player shots
  - Layered parallax backgrounds
  - Biome direction:
    - Deep space
    - Mechanical alien structures
    - Planet surface or orbital defense zone
  - Effects:
    - Engine trails
    - Muzzle flashes
    - Explosions
    - Screen shake used lightly
  - Visual priority: clarity first, style second.

- **Stack and Hosting Assumptions**
  - Next.js for app shell, routing, menus, and static hosting
  - PixiJS for browser canvas rendering
  - TypeScript preferred
  - Browser localStorage for saves, high scores, and settings
  - No backend for MVP
  - Next.js API routes only if later needed for AI generation helpers
  - OpenAI features are future-facing, likely for generated stage names, lore, or asset ideation
  - Local Windows development with Node.js
  - Deployable later to Vercel or any static-capable Next.js host

- **Milestone Order**
  - Milestone 1: Project foundation
    - Initialize Next.js app
    - Add PixiJS canvas shell
    - Create game scene lifecycle
  - Milestone 2: Player ship
    - Movement
    - Shooting
    - Hitbox
    - Lives
  - Milestone 3: Core combat
    - Enemy spawning
    - Enemy movement patterns
    - Bullets
    - Collision detection
    - Score
  - Milestone 4: Stage structure
    - Scrolling background
    - Timed enemy waves
    - Basic hazards
    - Stage clear flow
  - Milestone 5: Powerups
    - Weapon upgrades
    - Shield
    - Pickup spawning
  - Milestone 6: Boss encounter
    - Boss health
    - Attack phases
    - Victory condition
  - Milestone 7: Menus and persistence
    - Title screen
    - Pause
    - Game over
    - High score in localStorage
  - Milestone 8: Polish and playtesting
    - Effects
    - Audio hooks
    - Difficulty tuning
    - Playwright visual checks
  - Milestone 9: AI-enhanced features
    - Optional generated mission briefings, stage names, or cosmetic ideas
    - Keep gameplay deterministic for MVP

## Test Plan

- Verify `PLAN.md` exists at the repository root.
- Read through the file to confirm it covers all requested categories:
  - player goal
  - main loop
  - inputs and controls
  - win and fail states
  - progression/difficulty
  - visual direction
  - stack/hosting assumptions
  - milestone order
- No build or automated test is required for this documentation-only change.

## Assumptions

- The game name remains the working name `2D Side Scrolling Shooter` for now.
- The MVP is single-player only.
- The first playable target is one complete stage with one boss.
- The plan should be concrete enough to guide implementation, but not so rigid that later tuning requires rewriting the whole document.
