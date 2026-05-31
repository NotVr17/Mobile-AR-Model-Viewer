# 📱 Mobile AR Viewer for Dynamic 3D Model Iterations

## 📌 Project Overview
Complex, iterative 3D models—such as topology optimizations and structural meshes—lose critical spatial context when reviewed on 2D monitors. This mobile Augmented Reality application bridges that gap, allowing engineers to anchor sequences of high-poly STL files in physical space and dynamically simulate their structural evolution at real-world scale.

**Tech Stack:** Unity 6, AR Foundation (ARCore), C#, Android

## ⚙️ Core Architecture & Features

* **Custom Runtime STL Parsing:** Engineered a bespoke C# `STLLoader` that bypasses Unity Editor dependencies. It reads raw binary/ASCII STL files directly from Android's `persistentDataPath`, dynamically decoding vertex and triangle arrays into Unity Mesh objects at runtime.
* **Environmental Anchoring:** Utilizes `ARPlaneManager` and `ARRaycastManager` to detect valid horizontal/vertical planes. A single screen tap casts a ray into AR world-space, setting the initial model anchor origin.
* **State-Machine Playback Controller:** A robust `UIManager` state machine governs all iteration playback logic (play, pause, step, speed adjustment), ensuring the AR scene and UI overlay remain in strict sync without dropping frames on high-poly geometry.
* **Dual-Touch Manipulation:** Implemented pinch-to-zoom and swipe-to-rotate input systems for fluid, hands-on spatial inspection.

## 🚀 Installation & Usage

1. Download the `launcher-release.apk` from the repository files.
2. Install the APK on an ARCore-compatible Android device.
3. Open the app, slowly pan your camera to map the floor or desk, and tap the grid to anchor the 3D model.
4. Use the UI controls at the bottom to play, pause, or step through the iteration sequence.

## 👥 The Team
* Vansh Rathi 
* Arnav Sharma 
* Medha Kohli 

*Future implementations will include real-time cloud/local file uploading and grouped iteration rendering for direct spatial comparison.*
