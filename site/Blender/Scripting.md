# 🎨 Blender Workspaces & Features - Full Guide

Welcome to the **Blender All-in-One Guide**! This file covers Blender's key workspaces and features — from modeling to scripting — in an easy-to-follow format.

---

## 🧱 Layout Mode

Layout mode is your **default workspace** for organizing, selecting, and transforming objects.

### Tools:
- **Move (G)**, **Rotate (R)**, **Scale (S)**
- Use **Transform Gizmo** for intuitive dragging
- Object selection, parenting, and collections
- View layers and outliner (scene organization)

### Shortcuts:
- `G` = Grab/Move  
- `R` = Rotate  
- `S` = Scale  
- `Shift + D` = Duplicate  
- `Alt + G/R/S` = Reset location/rotation/scale

---

## ✏️ Modeling Mode

Modeling workspace allows you to modify the mesh geometry of an object.

### Tools:
- **Extrude**, **Inset**, **Loop Cut**, **Knife**
- **Vertex**, **Edge**, and **Face** selection modes
- **Modifiers**: Mirror, Subdivision, Solidify

### Shortcuts:
- `Tab` = Toggle Edit Mode  
- `Ctrl + R` = Loop Cut  
- `E` = Extrude  
- `I` = Inset  
- `Ctrl + B` = Bevel

---

## 🗿 Sculpting Mode

Used for **organic and detailed modeling** with brushes.

### Tools:
- **Draw**, **Clay Strips**, **Crease**, **Grab**, **Smooth**
- Use **Dyntopo** (Dynamic Topology) for more mesh detail
- Enable **Symmetry** for mirrored sculpting

### Tips:
- Use tablet pressure sensitivity for control
- Remesh or multiresolution modifiers for better results

---

## 🧩 UV Editing

Used to **unwrap** 3D models into 2D for texturing.

### Steps:
1. Go into **Edit Mode**
2. Select faces
3. Use **U** → Choose unwrap method (Smart UV, Unwrap, Project)
4. Adjust UVs in the left UV Editor panel

---

## 🖌️ Texture Paint

Paint directly on the 3D model or UV layout.

### Steps:
1. Add a **material** to the object
2. Create a **new image texture**
3. Go to Texture Paint tab
4. Paint directly on the 3D object

---

## 🧪 Shading Workspace

Used to create materials and shaders using **Shader Nodes**.

### Node Examples:
- **Principled BSDF**: All-in-one shader
- **Image Texture**: Load texture maps
- **Mix Shader**, **ColorRamp**, etc. for FX

### Output:
- Connect all to **Material Output**
- Use **Viewport Shading (Z)** to preview

---

## 🎬 Animation Workspace

Used to animate object properties, bones, shapes, and more.

### Key Areas:
- **Timeline**: Place keyframes (I key)
- **Dope Sheet**: Edit keyframes
- **Graph Editor**: Control animation curves
- **NLA Editor**: Combine actions

---

## 📸 Rendering

Rendering outputs your final image or animation.

### Engines:
- **Eevee**: Real-time
- **Cycles**: Physically accurate
- **Workbench**: For previews

### Settings:
- Resolution, samples, output format
- Use `F12` to render image
- Use `Ctrl + F12` to render animation

---

## 🧃 Compositing

Used to **edit rendered images** using nodes.

### Use Cases:
- Color correction
- Glare, Blur, Mist
- Adding image effects or filters

### Basic Setup:
- Enable **Use Nodes**
- Link **Render Layers → Effect Nodes → Composite Output**

---

## 🧬 Geometry Nodes

Create **procedural models or effects** using a node system.

### Basics:
- Add **Geometry Nodes Modifier**
- Build logic with:
  - **Distribute Points on Faces**
  - **Instance on Points**
  - **Set Position**
  - **Join Geometry**

### Use Cases:
- Procedural terrain, grass, particles, parametric assets

---

## 💻 Scripting Workspace

Use Python to automate and control Blender.

### Examples:
```python
import bpy

# Create a cube
bpy.ops.mesh.primitive_cube_add(location=(0, 0, 0))

# Delete all
bpy.ops.object.select_all(action='SELECT')
bpy.ops.object.delete()

# Assign material
mat = bpy.data.materials.new(name="MyMat")
mat.use_nodes = True
bpy.context.object.data.materials.append(mat)
