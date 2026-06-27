# MoleMates 🧪

**See chemistry. Understand everything.**

MoleMates is a visual chemistry learning app — glossy 3D molecules, a tap‑to‑build
molecule lab, smart flashcards, and concept lessons that actually click. This repo
holds the **fully interactive web prototype**: a single, dependency‑free HTML file
that doubles as the clickable spec for the native **SwiftUI / iOS** build.

## ▶️ Live demo

- **App prototype:** open [`index.html`](index.html) in any browser, or visit the
  GitHub Pages build.
- **Concept / landing page:** [seanwirkus.com/molemates.html](https://seanwirkus.com/molemates.html)
- **Atom style guide:** [`style-guide.html`](style-guide.html) — the design system: how every atom looks, derived from real electron counts.
- **Interactive 3D lab:** [`atoms-3d.html`](atoms-3d.html) — glassy WebGL atoms you can rotate, hover, and bond.

No build step, no dependencies — just open the file.

## ✨ What's inside

A complete five‑screen app you can actually use:

| Screen | What it does |
| --- | --- |
| **Home** | Daily goal ring, streak, "continue learning", molecule of the day |
| **Build** | Tap‑to‑build molecule lab — add atoms, bonds auto‑draw, live formula matching (`H₂O`, `C₂H₆O`…), challenge + win states |
| **Cards** | Flip‑and‑grade flashcards for organic functional groups (save, Again / Hard / Got it) |
| **Learn** | Visual concept lessons — bonding, states of matter, periodic trends, the mole, reaction types |
| **Profile** | Stats, achievements, preferences |

## 🍎 The road to iOS

The prototype is written to port cleanly to SwiftUI — the structure is intentional:

| Web prototype | SwiftUI equivalent |
| --- | --- |
| `<section data-screen>` | a `View` (`HomeView`, `BuildView`, …) |
| tab bar + router | `TabView` with a selection binding |
| `APP` state object | `@Observable final class AppModel` |
| `ELEMENTS` / `DECK` / `CONCEPTS` arrays | `struct Element` / `Card` / `Concept` models |
| builder / flashcard logic | `BuilderViewModel` / `StudyViewModel` |

Next stops: native gestures, Core Data progress, and the **App Store**.

## 🛠 Built with

Vanilla **HTML / CSS / JS** — no frameworks. Glossy atoms are layered radial
gradients, bonds are shaded sticks, and everything respects `prefers-reduced-motion`.
Fonts: Fredoka + Inter.

## Embedding

The app supports a transparent‑background embed mode for dropping the phone onto any
surface:

```html
<iframe src="index.html?embed=transparent" scrolling="no"></iframe>
```

---

Built by [Sean Wirkus](https://seanwirkus.com).
