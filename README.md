# rear-or-front-wheel-




# 🚗 DRIVEWISE Simulation — Rear or Front Wheel Drive Analyzer

[![License](https://img.shields.io/github/license/mach2furkan/rear-or-front-wheel)](LICENSE)
[![Issues](https://img.shields.io/github/issues/mach2furkan/rear-or-front-wheel)](https://github.com/mach2furkan/rear-or-front-wheel/issues)
[![Stars](https://img.shields.io/github/stars/mach2furkan/rear-or-front-wheel)](https://github.com/mach2furkan/rear-or-front-wheel)

Welcome to **Drivewise Simulation** — an interactive tool that visualizes how a sports car behaves in a curve depending on its drivetrain (Rear-Wheel Drive or Front-Wheel Drive). This project combines physics-based calculations with stunning 3D visuals using React Three Fiber and post-processing effects.

---

## 🚀 Live Demo
Coming soon...

---

## 📸 Preview

https://github.com/mach2furkan/rear-or-front-wheel/assets/demo-preview.gif  
<!-- Replace with actual GIF link when available -->

---

## 📦 Project Structure

```
drivewise_simulation/
├── public/
├── src/
│   ├── components/
│   ├── scenes/
│   ├── hooks/
│   └── car-simulation.tsx  ← Post-processing fix applied here
├── package.json
└── README.md
```

---

## 🧰 Tech Stack

- **React** + **TypeScript**
- **Three.js** via [`@react-three/fiber`](https://docs.pmnd.rs/react-three-fiber)
- Post-processing via [`@react-three/postprocessing`](https://github.com/pmndrs/postprocessing)
- Physics Engine: Custom drift, weight transfer, and curve prediction logic

---

## 🛠 Fix: MotionBlur Import Error

### ❌ Problem  
`MotionBlur` was causing an import error from `@react-three/postprocessing`.

### ✅ Solution  
We removed `MotionBlur` and kept the supported `Bloom` effect for smooth visual enhancements.

```tsx
import { EffectComposer, Bloom } from '@react-three/postprocessing'

<EffectComposer>
  <Bloom intensity={1.5} luminanceThreshold={0.3} />
</EffectComposer>
```

---

## 🎮 Features

- 🔄 Toggle between Front-Wheel and Rear-Wheel Drive
- 🧠 Calculates real-time entry angle, optimal speed, and slip behavior
- 🌟 Bloom effect for visual feedback on acceleration & braking zones
- 🧭 Live curve-based driving assistance
- 📉 Physics engine for dynamic simulation

---

## 🧪 How to Run Tests

```bash
# Run type-checks
npm run typecheck

# Run visual simulation in dev mode
npm run dev

# Run automated unit tests (coming soon)
npm run test
```

---

## 🔍 Curve Detection Logic

The simulation uses a combination of:

- Steering angle + IMU input
- GPS-based path prediction
- Radius calculation using:
  \[
  R = \frac{v^2}{g \cdot \mu}
  \]

When a corner is detected, the software dynamically adjusts recommended entry angle and speed based on drivetrain type.

---

## 🗺️ Feature Roadmap

| Feature | Status |
|--------|--------|
| Curve detection using camera input | 🔜 Planned |
| Driver profile adaptation with AI | ⏳ In Progress |
| Advanced HUD visualization | ✅ Completed |
| Audio warnings & alerts | 🔜 Planned |
| Exporting lap data to CSV | ⏳ In Progress |

---

## 🗂️ Repository

🔗 [GitHub Repo → mach2furkan/rear-or-front-wheel](https://github.com/mach2furkan/rear-or-front-wheel)

---

## 🤝 Acknowledgments

- 🌟 [@pmndrs](https://github.com/pmndrs) for the React Three Fiber & Postprocessing ecosystem
- 🧠 Inspiration from GT Racing Sim Physics Docs
- 🎮 Thanks to contributors who tested the simulation across platforms

---

## 🧑‍💻 Contributing

Contributions, ideas, and suggestions are very welcome!  
To contribute:

```bash
# Clone repo
git clone https://github.com/mach2furkan/rear-or-front-wheel

# Install dependencies
cd rear-or-front-wheel
npm install

# Start dev server
npm run dev
```

Please check open issues or suggest a new one!

---

## 📄 License

This project is licensed under the MIT License.  
See [LICENSE](./LICENSE) for more info.

---


