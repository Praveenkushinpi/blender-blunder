# ✨ Blender Shading Mode Overview

**Shading Mode** in Blender is where you create and manage materials using **nodes**. It’s where you define how your model looks — color, metal, gloss, transparency, bumpiness, and more — by building a **shader graph**.

---

## 🌌 Workspace Overview

When you switch to the **Shading** workspace:

- **Top-Left**: 3D Viewport (to see your model with material applied)
- **Bottom-Left**: Image/UV Editor (optional, for texture viewing)
- **Bottom-Center**: Shader Editor (the node graph)
- **Top-Right**: Outliner
- **Bottom-Right**: Material properties

---

## 🎨 Materials & Shader Basics

### 🎛️ Node System:
- Blender uses a **node-based system** (in the Shader Editor).
- The **Principled BSDF Shader** is the standard, PBR-friendly material (great for game engines too).

### 📦 Key Components:
- **Image Texture Node**: Loads texture files (Base Color, Roughness, Normal, etc.)
- **Principled BSDF**: All-in-one PBR shader
- **Material Output**: Final shader output

---

## ⚙️ Setting Up a Basic Material

### 1. **Select Your Model**
- In Object Mode, select the model.
- Go to the **Material Properties** tab.
- Click **New** to create a material.

### 2. **Shader Editor Setup**
In the Shader Editor:
- You'll see:  
  **[Principled BSDF] → [Material Output]**

### 3. **Add a Texture**
- Press `Shift + A` → Texture → **Image Texture**
- Connect it to **Base Color**
- Load a `.png`, `.jpeg`, or `.exr` texture
- Result: Your model is now textured!

---

## 🪞 PBR Material Node Setup

```plaintext
[Image Texture: Albedo] → Base Color
[Image Texture: Roughness] → Roughness
[Image Texture: Normal Map] → Normal Map → Normal Input
[Image Texture: Metallic] → Metallic
