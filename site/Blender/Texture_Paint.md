# 🎨 Blender Texture Paint Mode Overview

**Texture Paint Mode** lets you paint directly onto your 3D model or its UV map using a brush-based system. It's perfect for adding hand-painted textures, wear, dirt, stylized details, or touch-ups without leaving Blender.

---

## 🧭 Interface Overview

In the **Texture Paint Workspace**, Blender shows:
- **Left Side**: UV/Image Editor (2D texture view)
- **Right Side**: 3D Viewport (paint directly on the model)

You can paint in either view.

---

## 🖌️ Workflow Steps

### 1. **UV Unwrap the Model**
Before painting, your model must be unwrapped.  
Use `Edit Mode` → mark seams → `U` → unwrap.

### 2. **Create an Image Texture**
In the **Shader Editor**:
- Add an **Image Texture** node → click **New**
- Name the texture (e.g., "Body_Paint")
- Set resolution (e.g., 2048x2048 or 4096x4096)
- Set color (optional) → click **OK**
- Connect it to the **Base Color** of the Principled BSDF
- Click the node to **select it** (very important!)

### 3. **Enter Texture Paint Mode**
- Select your object → change to **Texture Paint Mode** (`Ctrl + Tab`)
- If nothing happens, go back to Shader Editor and make sure the Image Texture node is selected!

---

## 🎨 Painting in 3D Viewport

Use your mouse/tablet to paint directly on the 3D model.

### Brush Tools (Left Panel):
- **Draw** – Freehand painting
- **Soften** – Smoothes colors (like blur)
- **Smear** – Smudges colors
- **Clone** – Samples from another part of the texture
- **Fill** – Flood-fill based on UV island
- **Mask** – Restricts paintable area

---

## 🧰 Brush Settings (Top Bar or Sidebar)

- **Radius** – Brush size (`F` to change interactively)
- **Strength** – Opacity/intensity (`Shift + F` to change interactively)
- **Color Picker** – Choose paint color
- **Falloff** – Controls softness of the brush edges
- **Blending Modes** – Mix, Add, Subtract, Multiply, etc.
- **Texture** – Use custom brush textures (dots, patterns, etc.)

---

## 🖼️ Painting in 2D UV/Image Editor

You can also paint directly on the UV map:
- Select the image texture from the dropdown
- Use the same brushes as in 3D mode

---

## 💾 Saving Your Painted Texture

Blender does NOT automatically save painted images!

1. Go to **UV/Image Editor**
2. Select your painted texture
3. Click `Image → Save As`
4. Save it as a `.png` or `.jpeg` file

> 🔥 Tip: Save frequently when painting to avoid losing work!

---

## 🧪 Tips & Best Practices

- **Always Unwrap First**: No UV map = no painting.
- **Use High-Res Textures**: 2048x2048 or higher for detailed work.
- **Save Often**: Blender won’t save textures with `.blend` file unless packed.
- **Use Layers via Masks**: For advanced workflows, use multiple image textures with mix shaders.
- **Use a Graphics Tablet**: More natural brush strokes and pressure sensitivity.
- **Use a Stencil or Texture Brush**: Great for adding fabric patterns, scratches, and decals.

---

## 🧰 Ideal For:

- **Hand-Painted Textures**
- **Stylized Art Styles**
- **Texture Fixing**
- **Adding Dirt/Wear/Rust**
- **Making Custom Normal/Spec Maps**
- **Detail Painting without UV stretching**

---

## 🔑 Hotkeys Summary

| Action                  | Shortcut        |
|-------------------------|-----------------|
| Brush Size              | `F`             |
| Brush Strength          | `Shift + F`     |
| Sample Color            | `S + Left Click`|
| Save Painted Image      | UV/Image Editor → `Image → Save As` |
| Toggle View             | `Z` (switch shading modes to see texture updates) |

