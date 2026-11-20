# BANTAY: Alamat ng Gabi

A lightweight, **zero-asset** browser action game inspired by **Philippine mythology** and **Filipino martial arts**, built in a single self-contained HTML file (`index.html`, ~76 KB).

---

## How to Play

1. Open `index.html` directly in any modern web browser (no server, internet connection, or external files required).
2. Click **LABAN NA! (PLAY)** to start.

### Controls

| Action | Controls |
| --- | --- |
| Move | `W` `A` `S` `D` or Arrow Keys |
| Aim | Mouse cursor |
| Attack / Charge / Guard | Left Mouse Button |
| Switch Weapons | `1`–`5`, `Q` / `E`, Mouse Wheel, or click the weapon bar |
| Dodge Dash | `Space` or `Shift` |
| Pause | `P` or `Esc` |
| Toggle Sound | `M` |

---

## The 5 Weapons

| Slot | Weapon | Filipino Term | Role & Special Mechanic |
| :---: | --- | --- | --- |
| `1` | **Arnis** | *Doblete* (Dual Sticks) | Ultra-fast close-range dual-stick flurry with a 3-hit lunge finisher. |
| `2` | **Slingshot** | *Tirador* | Ranged blessed-stone pellets. Hold click to charge a fast, piercing critical shot. |
| `3` | **Staff** | *Tungkod* | Long sweeping melee reach. Every 3rd strike unleashes a 360° wind shockwave (*Hangin!*). |
| `4` | **Shield** | *Kalasag* | Hold click to raise a directional guard that blocks hits and **reflects** enemy projectiles; tap click for a high-knockback Shield Bash. |
| `5` | **1 Stick** | *Solo Baston* | Heavy *Kamagong* (ironwood) strike with strong stagger/stun and bonus critical damage against stunned foes. |

---

## Stages (Changes Every Level)

Each wave transitions to a new Philippine mythology arena with distinct terrain, lighting, props, and ambient particles:
1. **Kagubatan ng Kawayan** (*Moonlit Bamboo Grove*) — Mossy earth, swaying bamboo clusters with leaves, and golden fireflies.
2. **Barangay sa Tabing-Ilog** (*Torchlit Riverside Village*) — Courtyard arena with an animated moonlit river edge and flickering corner *sulo* (bamboo torches).
3. **Lumang Sementeryo** (*Misty Ancient Ruins*) — Cracked stone flagstones, ancient mossy pillars, and drifting violet mist.
4. **Tuktok ng Bundok** (*Sacred Mountain Shrine*) — Volcanic stone plateau with an etched 8-ray ancient sun motif and glowing spirit braziers.
5. **Lawa ng Bakunawa** (*Blood-Moon Eclipse Lake*) — Dark mirror-water with expanding ripples, obsidian rocks, and an eclipsed blood moon overhead.

---

## Mythical Enemies & Boss

- **Tiyanak** — Fast, agile swarmers that rush in packs.
- **Aswang** — Relentless night stalkers that close distance quickly.
- **Manananggal** — Winged flyers that orbit at medium range and fire cursed bolts.
- **Tikbalang** — Forest spirits that telegraph a line before charging across the arena.
- **Kapre** — Giant tree spirits smoking a glowing cigar ember, firing 3-way ember spreads.
- **Bakunawa (Boss, every 5th wave)** — The moon-eating serpent with a segmented body that darkens the sky (eclipse) and fires radial lunar orb barrages.

### Diwata Blessings (*Biyaya ng Diwata*)

After clearing each wave, choose 1 of 3 blessings:
- **Asin at Bawang** — +18% damage across all weapons
- **Bilis ng Hangin** — +14% movement speed & faster stamina regeneration
- **Biyaya ni Bathala** — +25 Max HP and immediate +45 HP heal
- **Kamay ng Kidlat** — +15% attack speed
- **Lakas ng Buwan** — +15% critical hit chance (2x damage)
- **Matibay na Kalasag** — +30% shield reflect damage & +25% stun duration

---

## Where the Details Come From

All game content was created from general knowledge of **Philippine folklore**, **traditional Filipino martial arts (FMA)**, and original game design — **no external files, images, audio, or web downloads were used**:

- **Philippine Mythology & Folklore:**
  - *Bakunawa* (Visayan/Bicolano moon-eating dragon/serpent associated with eclipses — *Laho*).
  - *Aswang*, *Manananggal*, *Tiyanak*, *Tikbalang*, and *Kapre* (widely known creatures across Tagalog, Visayan, and regional Philippine folklore).
  - *Bathala* (Tagalog supreme deity), *Diwata* (nature/guardian spirits), *Alitaptap* (fireflies), and folk protections such as *Asin at Bawang* (salt and garlic).
- **Filipino Martial Arts & Traditional Gear:**
  - *Arnis / Eskrima / Kali* techniques: *Doblete* (double stick) and *Solo Baston* (single stick, traditionally rattan or *kamagong* ironwood).
  - *Kalasag* (traditional carved wooden war shield used across pre-colonial Philippine warrior cultures).
  - *Tirador* (traditional wooden slingshot) and *Tungkod* (hardwood staff).
  - *Mandirigma* (warrior) and *Putong* (traditional red cloth headband worn by warriors).

---

## Zero-Asset Technical Architecture

To keep storage tiny (**~56 KB**, well under 1 MB):
- **Graphics:** 100% procedural 2D rendering via the HTML5 `<canvas>` API (shapes, gradients, slash arcs, fireflies, particles, and boss segments).
- **Audio:** 100% procedural sound synthesis using the browser's built-in **Web Audio API** (oscillators + filtered noise for wood clacks, elastic twangs, whooshes, blocks, and chimes).
- **Save Data:** High score is stored locally in `localStorage` (`bantay_hi`), taking only a few bytes.
