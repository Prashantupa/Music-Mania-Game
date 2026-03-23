# Music-Mania-Game

## 1. Game Overview

**Music Mania** is a mobile-first arcade game built entirely in a single HTML file (~3800 lines) using pure HTML, CSS, and JavaScript. It features a neon/cyberpunk aesthetic, five unique game levels, and an anime card-collection reward system.

## 2. Universal UI & Visual Design

* 
**Theme:** Neon/Cyberpunk against a near-black (`#0B0B0F`) background.


* 
**Palette:** Purple (`#7861FF`), Cyan (`#2EE6FF`), Green (`#39FF6E`), Pink (`#FF61C7`), and Yellow (`#FFE040`).


* 
**Typography:** **Orbitron** for headings/scores and **Exo 2** for body text (loaded via Google Fonts).


* 
**Fixed Layout Elements:** * **Progress Bar:** Pinned to the top; shows current level score vs. target (e.g., 47/200 pts); fills with a neon gradient.


* 
**Instruction Hint Pill:** Pinned at the bottom center; provides level-specific gameplay tips.





---

## 3. Level Structure & Mechanics

Each level has a specific point target to trigger a level-up.

| Level | Mode | Target | Key Mechanic |
| --- | --- | --- | --- |
| **1** | **Note Match Puzzle** | 100 pts | Match 3+ same-colored notes (horizontal/vertical/diagonal) on a $6 \times 7$ grid.

 |
| **2** | **Snake Note Hunt** | 200 pts | Guide a snake to collect falling notes. Snake grows on collection (cap 11).

 |
| **3** | **Music Dash Runner** | 300 pts | 3-lane runner. Swipe to change lanes; tap to jump over speakers or spike barriers.

 |
| **4** | **Rhythm Tap** | 400 pts | 4-lane rhythm game. Tap when notes reach the hit bar (Perfect = +40 pts).

 |
| **5** | **Note Defense** | 500 pts | Tap enemies (Small, Medium, Large) to defend a central speaker tower (5 HP).

 |

---

## 4. Systems & Logic

### Progression & Scoring

* 
**Score Flow:** All points are funneled through `addLevelScore(pts)`, which updates the progress bar and checks if `currentLevelScore >= levelTargetPoints`.


* 
**Level Completion:** Triggers a confetti celebration screen, awards a card, and increments the level.



### Card Collection System

* 
**Rewards:** Eight anime cards (e.g., Naruto, Kakashi, Luffy) unlock at specific levels.


* 
**Rarity:** Cards range from "Rare" to "Legendary" with associated theme colors.



### Technical Implementation

* 
**No Dependencies:** No external libraries or frameworks.


* 
**Audio:** Uses the **Web Audio API** (oscillators only) to synthesize all game sounds.


* 
**Graphics:** Rendered via **HTML Canvas 2D API** and inline SVG.


* 
**Persistence:** High scores and collected cards are saved via `localStorage`.
