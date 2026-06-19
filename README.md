# SCRAP LORD: Mech Salvage — Enhanced Edition (Touhou Edition)

A top-down mech salvage shooter with roguelike upgrades and danmaku-inspired bullet mechanics. Built entirely with HTML5 Canvas and procedural Web Audio — no external assets required.

## Overview

You are a SCRAP LORD — a mercenary pilot scavenging the mechanical graveyard of a collapsed civilization. Pilot your mech through endless waves of hostile AI drones, salvage their remains for upgrades, and survive as long as you can. Every run is different. Every upgrade is a tradeoff. Every bullet matters.

SCRAP LORD blends gritty industrial mech combat with subtle Touhou-inspired bullet-hell mechanics: graze incoming fire for bonus points, activate Focus Mode to thread the needle, and face off against bosses that cycle through named attack protocols.

## How to Play

Open `scrap-lord-enhanced.html` in any modern browser. No installation, no dependencies — it just works.

### Controls

| Key | Action |
|-----|--------|
| **WASD** | Move mech |
| **Mouse** | Aim turret |
| **Left Click** | Fire weapons |
| **Right Click** | Vent Reactor (emergency heat dump + shockwave) |
| **Space** | Dash (invulnerability frames) |
| **Shift** | Focus Mode (slow movement, precise hitbox, concentrated fire) |
| **E** | Extend pickup range |

## Core Mechanics

### Heat System
Your mech's reactor generates heat with every shot. If heat reaches maximum, your mech enters emergency shutdown — you're frozen in place for 3 seconds while the reactor cools. Manage your heat with coolant pickups, passive cooling, or vent it manually with Right Click (which also creates a shockwave that damages nearby enemies).

### Dash System
Press Space to dash in your movement direction (or aim direction if stationary). Grants invulnerability frames, allowing you to phase through enemy bullets and collision damage. Has a cooldown that varies by mech type.

### Combo Scoring
Chain kills rapidly to build combo multipliers (x2, x3, x4, x5). Higher combos mean dramatically more points. The combo timer resets after each kill — keep the pressure on.

### Touhou-Inspired Mechanics

**Focus Mode (Hold Shift):** Slows your mech to 40% speed and reveals your precise hitbox dot — the tiny core at your mech's center. Enemy bullets only hurt you if they hit this dot, not the full mech sprite. In Focus Mode, your shots become more concentrated with reduced spread and increased damage, letting you weave through dense bullet patterns while returning accurate fire.

**Grazing System:** When enemy bullets pass within your graze radius (the outer ring visible during Focus Mode) but miss your hitbox, you "graze" them. Each graze grants bonus score and reduces your reactor heat by a small amount, rewarding aggressive positioning near bullet streams. The Graze Amplifier upgrade increases both the detection radius and score multiplier.

**Boss Protocol Cards:** Bosses cycle through named attack patterns (Iron Tempest, Volley Barrage, Reactor Overflow, Graveyard Shift, and more), each announced with an on-screen protocol callout and unique bullet pattern. Phase 2 bosses unlock devastating protocols like Hellfire Rain and Final Judgment that combine multiple pattern types.

## Mech Frames

Choose your starting mech — each has distinct stats that affect your entire run:

| Mech | HP | Speed | Fire Rate | Special |
|------|-----|-------|-----------|---------|
| **JUGGERNAUT** | 200 | 1.5 | 8 frames | Highest hull integrity, balanced firepower |
| **SCOUT** | 100 | 3.5 | 5 frames | Fastest chassis, lowest heat, double dash speed |
| **ARTILLERY** | 120 | 2.0 | 25 frames | Massive burst damage, explosive ordnance, area denial |

## Enemies

Six enemy types escalate across waves:

- **Grunt** — Basic pursuit drone. Easy alone, deadly in numbers.
- **Swarm** — Spawns in groups of 3. Fast and fragile, they overwhelm with numbers.
- **Brute** — Huge, slow, heavily armored. Requires sustained fire or explosive hits.
- **Sentry** — Ranged attacker that fires aimed bullets at you from a distance.
- **Shielded** — Carries a regenerating energy shield that must be broken before hull damage applies.
- **Phantom** — Semi-invisible teleporter that blinks around the battlefield. Appears in later waves.

**Bosses** appear every 5 waves with massive health pools, two phases, and named protocol card attack patterns.

## Upgrades (Roguelike System)

After clearing a wave, choose from 3 randomly rolled upgrades. Every upgrade has both benefits and tradeoffs — there are no pure power-ups:

### Weapons
- **Rotary Autocannon** — Fire Rate +40% / Damage -40%
- **Heavy Cannon** — Damage +120% / Fire Rate -40% / Heat +50%
- **Plasma Spreader** — +2 Projectiles / Damage -50%
- **Rail Gun** — Bullet Speed x2 / Damage +80% / Pierce +1
- **Focus Laser** — Focus DMG +60% / Normal DMG -20%

### Core Systems
- **Overclocked Reactor** — Max Heat +50 / Speed +20% / Cooling -30%
- **Cryo-Vents** — Cooling +100% / Vent Radius +50% / Max Health -30
- **Fusion Core** — All Damage +30% / Heat/Shot -50%
- **Graze Amplifier** — Graze Radius +40% / Graze Score +100%

### Chassis
- **Heavy Plating** — Max Health +100 / Speed -20%
- **Titanium Servos** — Speed +40% / Max Health -40
- **Nano Repair** — Regen 0.05 HP/frame / Max Health -20

### Systems
- **Targeting AI** — Bullet Speed +50% / Damage +20%
- **Reactor Shielding** — Heat/Shot -30% / Cooling +20%
- **Dash Thrusters** — Dash Speed +40% / Dash Cooldown -30%
- **Magnet Lock** — Pickup Range x3 / Score +15%

Upgrade tiers unlock progressively — Tier 2 upgrades appear at wave 3, Tier 3 at wave 6.

## Pickups

Destroyed enemies may drop pickups with magnetic attraction:

- **Health (green)** — Restores hull integrity
- **Scrap (gold)** — Bonus score
- **Coolant (blue)** — Reduces reactor heat
- **Overcharge (orange)** — Large score bonus

## Visual Features

- Procedural particle system (sparks, smoke, expanding rings, thrust trails)
- Screen shake and screen flash on impacts, vents, and boss alerts
- Damage numbers floating from hit targets
- Kill feed ticker in the corner
- CRT scanline overlay and vignette effect
- Minimap in the top-right corner
- Focus Mode hitbox visualization with graze radius ring
- Boss protocol announcement cards with dramatic text callouts

## Audio

All sound effects are generated procedurally using the Web Audio API — no audio files needed:

- Distinct sounds for: shooting, heavy shooting, focus shots, enemy hits, explosions, reactor venting, dash, pickups, wave start, upgrade selection, boss alert, grazing, point-blank hits, protocol shifts, and meltdown shutdown
- Mute toggle supported

## Technical Details

- **Platform:** HTML5 Canvas 2D (single .html file, zero dependencies)
- **Resolution:** 900x640 native
- **Input:** Keyboard + Mouse
- **Audio:** Procedural Web Audio API (oscillators + noise buffers)
- **State Machine:** MENU → MECH_SELECT → PLAYING → UPGRADE → GAMEOVER
- **Performance:** Designed for 60fps on modern browsers

## Credits

Designed and developed as a solo project. Inspired by Vampire Survivors, Enter the Gungeon, Touhou Project, and classic top-down arcade shooters.

## License

Free to play, share, and modify.
