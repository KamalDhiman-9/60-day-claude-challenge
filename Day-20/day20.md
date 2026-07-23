# Day 20 — Face Puzzle Game 🧩

## Overview
Today I built a **fully self-contained Face Puzzle Game** using only vanilla HTML, CSS, and JavaScript — no frameworks, no external libraries. The app captures a live selfie from the user's webcam, slices it into a scrambled grid puzzle, and challenges the player to reassemble their own face against the clock.

Live in a single `.html` file — open it in any modern browser and play.

## Features Built
- 📷 **Webcam capture** via `getUserMedia()`, with a live preview and a "Take Photo" button
- 🎚️ **Selectable difficulty** — 3×3, 4×4, or 5×5 grids
- 🔀 **Randomized, guaranteed-solvable puzzle scrambling**
- 🖱️📱 **Drag-and-drop with full mouse *and* touch support** — swap-on-drop, snap-to-grid
- 🎨 **Visual feedback** — coloured border while dragging, green border when a piece is correctly placed
- ⏱️ **Live timer** (mm:ss.t) and **move counter**
- 🏆 **Win detection** with a results overlay showing final time, moves, and difficulty
- 💾 **Persistent leaderboard** — top 5 best times saved to `localStorage` (date, time, moves, difficulty)
- 🔁 Retake Photo / Play Again / New Photo controls
- 📱 Fully responsive layout for desktop and mobile

## Tech Stack
- **HTML5** — `<video>` + `<canvas>` for camera capture and image slicing
- **CSS3** — custom properties, gradients, flexbox/grid layout, responsive design
- **Vanilla JavaScript** — MediaDevices API, Canvas API, Pointer/Touch events, `localStorage`
- Zero external dependencies — the entire app is one portable `.html` file

## How It Works
1. On load, the browser requests camera permission and streams video into a `<video>` element.
2. Clicking **Take Photo** draws the current video frame onto a `<canvas>`, mirrored to match the preview, and exports it as a data URL.
3. The captured image is used as a shared CSS `background-image` across a grid of absolutely-positioned `<div>` "piece" elements, each showing a different `background-position` slice.
4. Piece positions are shuffled with a Fisher–Yates shuffle (re-rolled if it lands on the identity/solved order).
5. Dragging a piece and dropping it near another cell swaps the two pieces' positions and snaps both to the grid — this works identically for `mousedown/mousemove/mouseup` and `touchstart/touchmove/touchend`.
6. After every swap, the app checks whether every piece's current index matches its correct index. If so, the timer stops and the win overlay appears.
7. The final time is compared against the saved leaderboard in `localStorage`, and the top 5 fastest runs (with date, time, moves, and difficulty) are kept and displayed.

## Screenshots
> Add your screenshots below (drag them into this folder and reference them here):
- `screenshot-camera.png` — camera capture screen
- `screenshot-puzzle.png` — puzzle mid-play with a piece being dragged
- `screenshot-win.png` — win overlay with leaderboard

```md
![Camera capture](./screenshot-camera.png)
![Puzzle gameplay](./screenshot-puzzle.png)
![Win screen](./screenshot-win.png)
```

## Key Learnings
- **`getUserMedia()` error handling matters** — permission denial, no camera found, and camera-in-use all need distinct, user-friendly messages rather than a silent failure.
- **Mirroring the canvas capture** to match a CSS-mirrored `<video>` preview requires manually flipping the drawing context (`ctx.translate` + `ctx.scale(-1,1)`), not just relying on CSS.
- **Unifying mouse and touch input** is much cleaner when pointer-down/move/up logic is written once and simply fed different coordinate sources (`clientX/clientY` from either event type).
- **Guaranteeing a solvable shuffle** is trivial for a *free swap* puzzle (unlike a classic 15-puzzle with a blank tile and parity constraints) — since any two pieces can be swapped directly, every permutation except the identity is a valid, solvable scramble.
- **`localStorage` as a lightweight leaderboard** is a good pattern for small local-only game data — just remember to wrap reads/writes in try/catch since storage can be unavailable (private browsing, quota limits).
- Building responsive drag targets that "snap" to a grid is mostly a rounding problem: converting a pixel drop position into the nearest `(row, col)` and clamping to grid bounds.

## Files in This Folder
- `day20.md` — this write-up
- `face-puzzle.html` — the complete, working game (single file)
- Screenshots (see above)

## Try It
Open `face-puzzle.html` in any modern browser over `https://` or `localhost` (camera access requires a secure context), allow camera permission, and play!
