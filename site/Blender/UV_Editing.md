# 🗺️ Blender UV Editing Mode Overview

**UV Editing Mode** is where you unwrap your 3D model's surface to a 2D plane so textures can be accurately painted or applied. This is crucial for materials, painting, baking, and exporting to game engines.

---

## 🧭 Interface Overview

When you switch to the **UV Editing Workspace**, Blender splits the screen:
- **Left Side**: 2D UV/Image Editor (where you see and edit the unwrapped UVs).
- **Right Side**: 3D Viewport (where you select and unwrap mesh faces).

---

## 🧩 What Is UV Unwrapping?

UV unwrapping is the process of unfolding a 3D model into a flat 2D surface. Think of it like unfolding a cardboard box into a flat sheet.

- **U** = Horizontal axis on the texture
- **V** = Vertical axis (X & Y for textures)

The result is a UV map, which tells Blender how to project a 2D image (texture) onto your 3D model.

---

## 🔄 UV Editing Workflow

1. **Enter Edit Mode** (`Tab`)
2. **Select Faces/Edges/Verts** to unwrap
3. **Mark Seams**: `Ctrl + E` → Mark Seam  
   - Seams define where the mesh will be "cut" for unwrapping
4. **Unwrap**:
   - Press `U` → choose from:
     - **Unwrap** – General method (best with marked seams)
     - **Smart UV Project** – Auto unwraps for hard-surface objects
     - **Cube/Project from View** – For specific projections
5. **Adjust UVs** in UV Editor:
   - `G` to move
   - `S` to scale
   - `R` to rotate
   - `A` to select all
   - Use **Sync Selection** to link selections between 3D and 2D view

---

## 🛠️ Tools & Features

### In UV/Image Editor (Left Side):
- **UV Sync Selection** (🔗 icon): Toggle to sync 3D Viewport selection with UVs.
- **Image Menu**: Load or create a new image texture for editing/viewing.
- **Live unwrap**: Updates UV map in real-time when mesh changes.
- **UV Channels**: Store multiple UV maps for baking, decals, etc.

### Common UV Options:
- **UV → Pack Islands**: Reorganizes UVs to fill texture space efficiently
- **UV → Average Island Scale**: Makes all UV islands uniform in size
- **UV → Minimize Stretch**: Reduces distortion in UVs
- **UV → Stitch/Pin**: Manually fine-tune seams and pinned UVs

---

## 🧪 Tips & Best Practices

- **Good Seams = Good Unwraps**: Place seams logically along hidden or natural folds.
- **Check Distortion**: Use a checker texture to verify UV spacing and stretching.
- **Use Smart UV Project** for hard-surface objects (buildings, crates).
- **Pack Efficiently**: Use `UV → Pack Islands` before exporting.
- **Pin UVs**: Pin (`P`) important UV points before re-unwrapping to preserve layout.
- **UV Scaling Matters**: Uneven scales result in stretched textures.

---

## 🧰 Ideal For:

- **Texturing with Image Textures**
- **Hand-Painting in Texture Paint Mode**
- **Baking Normals & AO Maps**
- **Exporting to Game Engines (Unity, Godot, Unreal)**
- **Decals, Labels, and Detail Texturing**

---

## 🧱 Useful Hotkeys Summary

| Action                | Shortcut       |
|-----------------------|----------------|
| Unwrap                | `U`            |
| Mark Seam             | `Ctrl + E` → Mark Seam |
| Pin UV Vertex         | `P`            |
| Pack UV Islands       | `Ctrl + P` or `UV → Pack Islands` |
| Move/Scale/Rotate UVs | `G`, `S`, `R`  |
| Sync Selection        | Toggle 🔗 Icon |
