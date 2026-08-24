# ♥ Heart · A Living Body of Light

**English** | [中文](README.md)

**A Real-Time Particle Universe — Built Around a Beating Heart**

A crimson energy heart made of 170,000 fluid particles, wrapped in rings of stars on Keplerian orbits.

![WebGL2](https://img.shields.io/badge/API-WebGL2%20%7C%20GLSL%20ES%203.0-blue) ![Fluid](https://img.shields.io/badge/Solver-Navier--Stokes-purple) ![Dependencies](https://img.shields.io/badge/dependencies-zero-brightgreen) ![File](https://img.shields.io/badge/package-single%20file-orange)

---

## What Is This

Not a heart animation.

A **gravitationally-bound universe that happens to be alive**:

- **Center** — crimson plasma driven by a real fluid solver, precisely constrained into the shape of a heart
- **Edge** — a white energy skeleton traces the iconic outline (V-notch included), flowing with every breath, never losing form
- **Around it** — thousands of stars orbiting on inclined elliptical paths: precessing, crossing, pushed by every heartbeat
- **Deep space** — rose and cold-blue nebula haze, with a particle galaxy slowly turning

You can't tell at first glance whether it's particles, fluid, or something alive. That's the point.

---

## Features

### 🌊 A Real Fluid Heart

At its core runs a **Navier-Stokes solver** on atlas-packed 3D textures in WebGL2:

```text
Semi-Lagrangian advection → Force injection → Vorticity confinement → Pressure Poisson (18× Jacobi) → Gradient subtraction
```

A 44³ field, fully solved every frame. The heart doesn't constrain particles — it injects surface currents, membrane pressure, and pulse waves into **the fluid itself**. 176,000 tracer particles are carried by the medium. The shape isn't drawn; it *emerges* from turbulence — like ferrofluid meeting a magnet.

### 💓 An Energy Pulse You Can Feel

A six-phase envelope loop drives everything:

```text
Rest → Systole → Charge (accretion spin-up) → Burst (radial impulse + traveling wave) → Scatter → Regather (underdamped elastic snap)
```

Every beat launches an energy wave from the core. It sweeps through the fluid and across the star field — orbital particles get kicked outward, then gravity pulls them home.

### 🕸 A 3D Outline Skeleton

15,000 highlight particles are **Newton-projected onto the Taubin implicit surface**, forming three families of wireframes:

- **Main ridge** — true front-silhouette solve, so the upper V-notch reads clearly
- **Latitude rings ×5** — horizontal cross-sections that instantly convey volume
- **Meridian ridges ×6** — running over the belly and around the back

Back-side falloff gives the cage real depth.

### 🪐 A Keplerian Particle Galaxy

Thousands of outer stars orbit at **ω ∝ a^(-3/2)**:

| Tier | Behavior |
| ---- | -------- |
| Near | Sparse, fast, bright — tightly coupled to heart energy |
| Mid | Four tilted planetary ring bands + fully randomized inclinations, nodal & apsidal precession |
| Far | Wide ellipses (e ≤ 0.55), uniform spherical distribution wrapping the heart 360° |

Stronger heartbeat → faster star flow. Move the mouse → nearby orbits bend. Click → a shockwave knocks stars off their rails, and gravity reels them back in.

### ✨ Render Pipeline

HDR additive accumulation trails → ¼-res Gaussian bloom chain → ACES tone mapping → shockwave screen-space refraction → chromatic aberration → vignette → film grain

Doppler brightness shift · fake depth-of-field CoC · vorticity-tinted violet glow · GPU electric arcs · velocity-stretched streaks

---

## Controls

| Input | Effect |
| ----- | ------ |
| **Drag** | Orbit the camera (with inertia — flick to spin) |
| **Scroll / pinch** | Zoom [2.6, 6.5] |
| **Move mouse** | Stir the fluid · bend nearby orbits |
| **Click / tap** | Release a shockwave at the cursor |

---

## Run It

No build. No dependencies. No network requests.

```bash
# Just open index.html
# Or serve locally:
python -m http.server 8000
# then visit http://localhost:8000
```

Any browser with **WebGL2** support (Chrome / Edge / Firefox / Safari 16+).

---

## Performance

Four-stage adaptive quality: when FPS drops below threshold, resolution and particle count scale down automatically (grid 420² → 230²). Pauses on hidden tabs, recovers from context loss automatically. Runs smoothly from discrete GPUs to integrated graphics.

---

## Tech Stack

```text
WebGL2 · GLSL ES 3.0 · GPGPU double-buffered MRT
Atlas-packed 3D fields · Semi-Lagrangian advection · Jacobi pressure projection
Vorticity confinement · curl-noise · Analytic Keplerian orbits · Newton surface projection
ACES · Gaussian bloom chain · Feedback trail accumulation
```

**Zero dependencies · Single file · ~2,100 lines · Works offline**

---

*It starts beating the moment you open the page.*
