# 🎛️ Blender Compositing Mode Overview

**Compositing Mode** in Blender lets you **edit and enhance your rendered images or animations** using nodes — like Photoshop but fully procedural and powerful. It’s great for adding **glow, color correction, depth of field, fog, chromatic aberration**, and more.

---

## 🧭 Workspace Layout

When you switch to the **Compositing** workspace:

- **Main Area**: Node Editor (where you'll connect effects)
- **Top-Right**: Outliner (to access scene elements)
- **Bottom-Right**: Properties panel (to tweak render/composite settings)
- **Image Viewer**: Used to preview your composite output

---

## 🔧 Setup (Start Here)

### Step 1: Enable Nodes
- In the Compositing workspace, check **"Use Nodes"** and **"Backdrop"** in the node editor.

### Step 2: Basic Node Structure
By default, you’ll see:

> 📝 Tip: Add a **Viewer Node** (`Shift + A → Output → Viewer`) and connect it to see real-time preview in the backdrop.

---

## 🧩 Common Nodes and Their Uses

| Node                | Purpose                                         |
|---------------------|-------------------------------------------------|
| **Blur**            | Gaussian or Bokeh blur                         |
| **Glare**           | Add glow, streaks, or fog glow                 |
| **Color Balance**   | Advanced color grading                         |
| **Hue/Saturation**  | Adjust color tones                             |
| **Z Combine**       | Mix images based on depth                      |
| **Alpha Over**      | Overlay images with transparency               |
| **Lens Distortion** | Chromatic aberration / camera effects          |
| **Defocus**         | Simulate camera depth of field (requires Z pass)|
| **ID Mask**         | Isolate objects using render pass IDs          |
| **Mix**             | Blend two image streams                        |
| **Dilate/Erode**    | Expand or shrink masks                         |

---

## 🎨 Popular Effects You Can Do

### 🔥 Glow/Bloom
- Add a **Glare** node (Streaks or Fog Glow)
- Connect from **Render Layers → Glare → Composite**

### 🌈 Color Grading
- Use **Color Balance** or **RGB Curves** node
- Fine-tune shadows, midtones, and highlights

### 🌫️ Depth of Field
- Use **Z-buffer output** from Render Layers
- Add **Defocus** node → connect **Z** input
- Enable “Use Z-buffer” and tweak focus distance

### 🎥 Lens FX
- Add **Lens Distortion** for:
  - **Distort**: Fish-eye or barrel effects
  - **Dispersion**: Chromatic aberration

### 🪞 Render Pass Editing
- Enable extra passes in Render Properties → **Passes**
- You’ll get nodes like:
  - **Diffuse Direct**, **Glossy Indirect**, **Shadow**, etc.
- You can combine, mask, or color correct these independently

---

## 🧠 Pro Tips

- Use **Viewer Node** + `Backdrop` to get live feedback (scroll to zoom)
- Use **File Output Node** to save specific node results (good for VFX)
- Chain multiple nodes for powerful effects (e.g., glare → color balance → vignette)
- Use **Masks** and **ID Masks** to isolate elements or characters
- Use **Cryptomatte** for fast, non-destructive masking of objects/materials

---

## 🧾 Compositing vs Shader Nodes

| Feature              | Compositor       | Shader Editor      |
|----------------------|------------------|--------------------|
| **Purpose**          | Post-processing  | Material creation  |
| **Works on...**      | Rendered output  | Object surface     |
| **Node Types**       | Image FX, masks  | BSDFs, textures    |

---

## 🔑 Hotkeys & Tricks

| Action                  | Shortcut         |
|--------------------------|------------------|
| Add Node                 | `Shift + A`       |
| Delete Node              | `X`               |
| Connect Nodes            | Click-drag output |
| Toggle Backdrop Zoom     | Scroll wheel      |
| Pan in Node Editor       | Middle-click drag |
| Re-center nodes          | `Home`            |
| View node result         | `Ctrl + Shift + Click` on node (with Node Wrangler) |

> ✅ **Enable Node Wrangler Addon** for speed!  
`Edit → Preferences → Add-ons → Search: Node Wrangler → Enable`

---

## 🎯 Ideal For:

- Enhancing realism
- Adding post-effects without modifying 3D scene
- Creating cinematic looks
- Isolating and tweaking render passes
- Preparing final renders for films, games, or web

