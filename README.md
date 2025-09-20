```markdown
# 🏌️‍♂️ MiniGolf (CloneFest 2025 Project)

A web-based **3D MiniGolf game** built with [Three.js](https://threejs.org/) and [Vite](https://vitejs.dev/).  
This project is part of **CloneFest 2025 — Reimagining a C-based Minigolf Classic**, where the goal is to port a minigolf experience into the browser with interactive physics, gameplay, and user-friendly controls.

Deployed on **Vercel** → [🎮 Play Now](https://mini-golf-eta.vercel.app/)
---

---

## 🎮 Use Case: Loading Page Game

This project can also be adapted as a **fun offline/loading screen game** 🔄  
(similar to the **Chrome dinosaur game** or simple **Flappy Bird clones**).  

👉 It can run in the background while:  
- A website/app is loading heavy content  
- Users are offline or facing slow internet  
- As an **Easter Egg mini-game** to keep users engaged 🎉  

---

## ✨ Features

- **3D Scene & Rendering**
  - Interactive 3D golf courses rendered in Three.js.
  - Multiple `.glb` holes (`hole1.glb`, `hole2.glb`, `hole3.glb`) loaded dynamically.
  - Ambient + directional lighting for realistic shading.

- **Golf Ball Physics**
  - Realistic physics: gravity, friction, velocity, restitution (bounce).
  - Triangle-level collision detection (no wall clipping).
  - Special handling for **loops** (level 3): reduced friction + uphill assist for smoother climbs.

- **Player Interaction**
  - **Drag-to-Aim**: Click near the ball (within its diameter) to start aiming.
  - **Shot Power**: Visualized by a cylinder that changes color (green → yellow → red) and thickness.
  - **Opposite Direction Launch**: Pull back and release to shoot forward.
  - Configurable shot strength and drag tolerance.

- **Camera System**
  - Smooth ball-following camera.
  - OrbitControls: rotate, zoom, pan.
  - Prevents camera from clipping into the ground.

- **Gameplay & UI**
  - Single HUD counter (top-left) showing **Level** and **Strokes**.
  - After each hole, popup shows: *“You took X strokes”*.
  - Win detection: reaching `hole_end` triggers level completion.
  - Lose condition: falling out of bounds resets ball to start.

---
## 📌 Additional Future Enhancements

### 1. Music System
- *Music Toggle Button*: A circular music control button in the bottom-right corner that lets you:
  - Play/pause background music
  - Mute/unmute the audio
  - Shows a speaker icon (🔊) when music is playing
  - Changes to a muted speaker (🔇) when music is off
  - Has a smooth hover effect with a color change

### 2. Control Panel (Left Side)
A vertical panel on the left side with these interactive buttons:

1. *Reset Ball (🔄)*
   - Resets the ball to its starting position
   - Has an orange background
   - Has a smooth scale animation when clicked

2. *Reset Camera (📹)*
   - Resets the camera to its default position
   - Has a blue background
   - Also has a click animation

3. *Level Select (🎯)*
   - Opens a prompt to choose a level
   - Shows available levels (e.g., "Choose your challenge! Level 1-2")
   - Has a purple background
   - Includes input validation

4. *Fullscreen Toggle (⛶)*
   - Toggles between fullscreen and windowed mode
   - Has a green background
   - Works with the browser's fullscreen API

5. *Help (❓)*
   - Displays game controls and instructions
   - Has a red background
   - Shows a popup with game information

### 3. HDRI Background System
- *Dynamic Background*: 
  - Loads high-dynamic-range images for realistic lighting
  - Affects both the skybox and environment reflections
  - Has a fallback to original lighting if loading fails
  - Includes loading progress tracking
  - Currently disabled but can be re-enabled

### 4. Visual Feedback
- *Button Effects*:
  - Scale animation on hover (buttons grow slightly larger)
  - Click animation (buttons press down)
  - Smooth transitions for all animations
  - Shadow effects for depth

### 5. Game State Display
- *Strokes Counter* (Top-left)
  - Shows the current number of strokes
  - Updates in real-time
  - Has a semi-transparent black background

- *Level Display* (Top-right)
  - Shows the current level number
  - Matches the style of the strokes counter

## 📂 Project Structure

```

MiniGolf/
├── public/
│   └── assets/
│       ├── hole1.glb        # Level 1 course
│       ├── hole2.glb        # Level 2 course
│       └── hole3.glb        # Level 3 with 360° loop
├── src/
│   ├── main.js              # Core game logic
│   └── style.css            # Styling
├── index.html               # Entry point
├── package.json
├── vite.config.js
└── README.md

````

---

## ⚙️ Installation & Setup

### 1. Clone the repository
```sh
git clone https://github.com/TheClazer/MiniGolf.git
cd MiniGolf
````

### 2. Install dependencies

```sh
npm install
```

### 3. Start development server

```sh
npm run dev
```

Open the shown URL (usually `http://localhost:5173/`).

### 4. Build for production

```sh
npm run build
```

### 5. Preview production build

```sh
npm run preview
```

---

## 🕹️ Controls

* **Left Mouse Button + Drag near ball** → Aim and set power

  * Pull further = stronger shot.
  * Cylinder indicator shows color (green → yellow → red) and thickness.
* **Release Mouse Button** → Shoot the ball.
* **Mouse Scroll** → Zoom camera.
* **Right Click + Drag** → Rotate camera.
* **Shift + Drag** → Pan camera.

---

## ✅ Requirements Implemented

* Multi-level support (`hole1`, `hole2`, `hole3`).
* Advanced physics with friction, bounce, gravity.
* Stroke counter with clean UI overlay.
* Hole detection (with high-speed capture fix).
* Loop climbing mechanics.
* Camera follow system with OrbitControls.

---

## 📌  Future Enhancements
  🎶 Add sound effects & background music

  📱 Mobile/touchscreen support

  🏆 Leaderboard & scoring system

---

## 🛠 Tech Stack

* **Three.js** – 3D rendering
* **Vite** – Dev server & bundler
* **JavaScript (ES Modules)** – Core logic

---

## 👨‍💻 Author

## 👨‍💻 Author

Built by [TheClazer](https://github.com/TheClazer),  
[Ashitha0409](https://github.com/Ashitha0409),  
[has066](https://github.com/hash066),  
[ayushranjan28](https://github.com/ayushranjan28)  
for CloneFest 2025.


```
```
