# Paradox Tap

A polished, single-file mobile web game built for **one-thumb** play.

Tap the glowing core to score points, but every tap increases **Instability**. Let Instability hit 100 and your timeline collapses.

## How to Play

- **Tap** the big circular button:
  - **+1 score** (or more with multipliers)
  - **+6 Instability**
- **Instability drains automatically** over time.
- **Hold** your finger down:
  - Instability drains **faster**
  - **No score** is gained while holding
- **Rhythm Bonus:** if your last taps are consistently timed (±100ms), you get:
  - **2x score**
  - A stronger **glow** effect
- **Paradox Events:** when Instability is high (>70), short chaotic effects can trigger:
  - screen shake
  - button shifts
  - temporary 2x scoring
  - reverse tap mode (tap reduces Instability)

## Run Locally

Just open the file:

- Open `index.html` directly in your browser, or
- Serve it locally:

```bash
# from the repo folder
python3 -m http.server 8000
# then open:
# http://localhost:8000
```

## Deploy to GitHub Pages

1. Go to **Settings → Pages**
2. Under **Build and deployment**:
   - **Source:** Deploy from a branch
   - **Branch:** `main`
   - **Folder:** `/ (root)`
3. Save.

Your game will be available at:
`https://themaxscriptguy.github.io/Paradox_Tap/`

## Tech Notes

- Single file: **all HTML/CSS/JS in `index.html`**
- Works offline (no external assets/libraries)
- Mobile optimized (portrait layout, touch + mouse support)
- Uses `requestAnimationFrame` for the game loop
- High score saved via `localStorage`
