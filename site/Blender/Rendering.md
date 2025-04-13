# 🖼️ Blender Rendering Mode Overview

**Rendering Mode** is where you create the final output of your 3D scene — images, animations, or previews — using Blender's powerful rendering engines like **Cycles** or **Eevee**.

---

## 🧭 Rendering Workspace Overview

In the **Rendering Workspace**, you'll typically see:

- **Top-Left**: 3D Viewport (set to Rendered view)
- **Bottom**: Timeline (if you're rendering animations)
- **Top-Right**: Outliner
- **Bottom-Right**: Properties panel with full render settings

---

## 🔧 Render Engine Options

You can choose your render engine in:
`Properties Panel → Render Properties (Camera icon)`

### 🧪 1. **Eevee** (Real-time Renderer)
- Fast, great for real-time previews, stylized art, and low-spec PCs
- Supports screen-space reflections, ambient occlusion, bloom, etc.

### 🎥 2. **Cycles** (Path Tracer)
- Physically accurate lighting
- Slower, but delivers photorealistic results
- Supports GPU and CPU rendering

---

## ⚙️ Essential Render Settings

### 📸 Output Properties (Printer icon)
- **Resolution**: Default is 1920x1080
- **Frame Range**: For animation (Start/End frame)
- **Frame Rate**: Usually 24 or 30 fps
- **Output Folder**: Set path for saved files
- **File Format**: PNG, JPEG for images; FFmpeg for videos

### 💡 Render Properties (Camera icon)
- **Samples**: Controls quality (higher = better, slower)
- **Denoising**: Remove grain (especially in Cycles)
- **Light Paths** (Cycles only): Controls reflections, bounces
- **Ambient Occlusion**, **Bloom**, **Depth of Field** (Eevee)

### 🧱 View Layer Properties (Photo icon)
- Control which objects are visible in the render
- Use passes (e.g., Shadow, Diffuse, Z-depth) for compositing

---

## 🚀 Rendering Process

### 🖼️ Render Image
- Shortcut: `F12`
- Menu: `Render` → `Render Image`

### 🎞️ Render Animation
- Shortcut: `Ctrl + F12`
- Menu: `Render` → `Render Animation`
- Blender will render and save each frame (as image sequence or video)

---

## 🎬 Output File Formats

| Format   | Use Case                          |
|----------|-----------------------------------|
| **PNG**  | High-quality image with alpha     |
| **JPEG** | Lightweight images                |
| **EXR**  | HDR images and passes for compositing |
| **FFmpeg** (MP4) | Video animation            |

> 🎯 Tip: For videos, choose **FFmpeg** → Container: `MPEG-4` → Codec: `H.264`

---

## 📦 Compositing After Render (Optional)

- Use **Compositing** workspace to apply filters, glows, color correction
- Enable "Use Nodes" and modify your render output using:
  - **Render Layers**
  - **Glare**, **Color Balance**, **Lens Distortion**, etc.
  - **Composite Output**

---

## 🎯 Ideal For:

- Final frame/animation output
- Game asset previews
- Promotional or cinematic shots
- Stylized or realistic stills
- Exporting to video editing tools

---

## 🧠 Tips & Best Practices

- Use **Render Region** (`Ctrl + B`) to isolate and test part of your scene
- Enable **Denoising** to clean up noisy renders
- Render at lower resolution/sample rate to test quickly
- Bake lighting for better Eevee performance
- Use **Render Layers** to separate objects (good for compositing)
- Use **GPU Rendering** if available (Cycles → Device: GPU Compute)

---

## 🔑 Hotkey Summary

| Action            | Shortcut     |
|-------------------|--------------|
| Render Image      | `F12`        |
| Render Animation  | `Ctrl + F12` |
| Cancel Render     | `Esc`        |
| View Rendered     | `Z` → Rendered or `Shift + Z` |
| Set Render Region | `Ctrl + B`   |
| Clear Region      | `Ctrl + Alt + B` |

