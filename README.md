# 🧠 Supernatural Body Intelligence

> An interactive biomechanics visualizer that maps modular movement logic to every part of the human body — from finger flexion to spinal rotation. Each body part module tracks joints, range of motion, and muscle groups, feeding real-time data into a unified Central Intelligence core. Pure HTML, CSS & JavaScript. No dependencies.

---

## 🔍 What Is This?

**Supernatural Body Intelligence** is a front-end biomechanics engine built entirely in vanilla HTML, CSS, and JavaScript. It assigns a dedicated code module to every major body part — each storing its own movement data, range of motion values, joint axes, and muscle groups.

When you interact with a body part, all its data flows into a **Central Intelligence core** that aggregates signals across every active module in real time — tracking neural signal estimates, active joints, muscles engaged, total ROM, and total coded movements simultaneously.

Think of it as a living dashboard for the human body.

---

## ✨ Features

- **Modular body-part system** — each part (shoulder, elbow, wrist, hand, spine, hip, knee, ankle, foot) is an independent data module
- **Interactive SVG body map** — click any body part to highlight it and load its movement data
- **Movement arc visualizer** — shows the angle of motion for each selected movement directly on the SVG
- **Central Intelligence panel** — aggregates data from all activated modules and displays live metrics:
  - Neural signals/s
  - Joints active
  - Muscles engaged
  - Total ROM (°)
  - Movements coded
- **Signal bar indicators** — visual activity bars that scale with the number of active modules
- **Zero dependencies** — pure HTML/CSS/JS, no frameworks, no libraries, no build step

---

## 🫀 Body Parts Covered

| Body Part | Movements Coded |
|-----------|----------------|
| Shoulder | 8 |
| Elbow | 5 |
| Wrist | 6 |
| Hand / Fingers | 12 |
| Spine / Torso | 7 |
| Hip | 7 |
| Knee | 5 |
| Ankle | 6 |
| Foot / Toes | 6 |

**Total: 62 coded movements** across 9 body modules.

---

## 🚀 Getting Started

No installation required.

```bash
# Clone the repo
git clone https://github.com/YOUR_USERNAME/supernatural-body-intelligence.git

# Open the file
cd supernatural-body-intelligence
open index.html
```

Or just download `index.html` and open it directly in any modern browser.

---

## 🗂️ Project Structure

```
supernatural-body-intelligence/
│
└── index.html        # Entire project — markup, styles, and logic in one file
```

This is intentionally a single-file project (mini version). Future versions will modularize each body part into its own JS module.

---

## 🧩 How It Works

### Body Part Modules
Each body part is defined as an object in `BODY_PARTS` containing:
- `label` — display name
- `color`, `bg`, `dot` — theming values
- `svgIds` — which SVG elements to highlight
- `center` — coordinates for the movement arc
- `moves[]` — array of movements, each with name, degree range, and axis

### Central Intelligence Core
The `updateIntelligence()` function iterates over all `activePartKeys` (body parts the user has clicked) and computes aggregate metrics — total movements, total ROM, estimated neural signals, and more — then updates the UI in real time.

### Movement Arc
When a movement is selected, `showArc()` calculates an SVG arc path based on the degree value and renders it directly on the body diagram at the part's center coordinates.

---

## 🛠️ Roadmap

- [ ] Expand to full skeletal system (cervical spine, jaw, scapula, etc.)
- [ ] Add muscular layer with origin/insertion data
- [ ] Separate each body part into its own JS module
- [ ] Add nervous system layer (PNS/CNS signal mapping)
- [ ] 3D body model integration
- [ ] Export body intelligence report as JSON/PDF
- [ ] Mobile-responsive layout

---

## 🎨 Design

Built with a dark sci-fi aesthetic using:
- **Fonts:** Syne (headings) + Space Mono (data/labels) via Google Fonts
- **Color system:** Purple (`#7F77DD`), Teal (`#1D9E75`), Coral (`#D85A30`), Amber (`#BA7517`), and more — one accent per body region
- **Background:** Subtle CSS grid overlay for depth

---

## 📄 License

MIT License — free to use, modify, and build on.

---

## 🙌 Author

Built by **[Your Name]** — part of an ongoing project to map and code the full intelligence of the human body.

> *"Every bone. Every muscle. Every nerve. Coded."*
