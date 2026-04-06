## PART 1: CORE PIPELINE & RENDER SETTINGS

### Render Path / Post-Stack

**Approach:**

- **Unity:** URP with **Custom Renderer Feature** (Full-screen pass + per-object screen shaders)
    
- **Unreal:** Deferred Renderer with **Post Process Volume + Custom Depth/Stencil for screens**
    
- **Godot:** Forward+ with **Environment + Viewport-to-Texture CRT screens**
    

**Key Rule:**  
Global post is intentionally _flat and cold_. All visual authority comes from **localized emissive systems**, not cinematic grading.

---

### Global Volume Profile Settings

**Tonemapping**

- Mode: **Neutral / Linear**
    
- White Point: **Lowered** (≈ 0.85)
    
- Contrast: **-10%**
    
- Purpose: Suppress modern HDR punch; preserve institutional dullness.
    

**Color Grading (Lift / Gamma / Gain)**  
(Converted from the Replication Formula)

- **Lift:**
    
    - R: -0.02
        
    - G: 0.00
        
    - B: +0.04
        
- **Gamma:**
    
    - R: -0.03
        
    - G: -0.01
        
    - B: +0.05
        
- **Gain:**
    
    - R: -0.05
        
    - G: -0.03
        
    - B: +0.02
        

**Saturation:** 0.40 global cap  
**Purpose:** Enforces _Cold-State Chromatic Minimalism_.

**Vignette**

- Intensity: 0.35
    
- Smoothness: 0.6
    
- Color: **Cold Cyan (#0b1a24)**
    
- Purpose: Tunnel vision, command isolation.
    

**Film Grain**

- Type: Monochrome
    
- Intensity: 0.15
    
- Response: Midtones only
    

---

## PART 2: MATERIAL & SHADER SYSTEMS

### World Material Philosophy

**Rule Zero:**

> No material is allowed to look emotionally expressive.

- Use **Desaturated PBR** only
    
- Hard clamp albedo saturation at **≤ 0.45**
    
- Metallic values biased upward (0.4–0.7) even for plastics
    
- Roughness slightly elevated (0.55–0.8) to kill specular beauty
    

**Global Cold Bias Shader Function**

- Add a shared shader function that shifts **ambient + indirect light** toward blue:
    
    `ambientColor = lerp(ambientColor, ambientColor * float3(0.85, 0.95, 1.15), 0.6);`
    
- Apply to all non-UI materials.
    

---

### CRT Screen Shader (Critical System)

**Architecture**

- UI → RenderTexture / Viewport
    
- CRT Shader applied to **screen mesh only**
    
- Uses **Custom Depth/Stencil** so global post does not affect it
    

---

#### CRT Shader: Pseudo-Code Logic

**Inputs**

- `ScreenTex` (RenderTexture)
    
- `Time`
    
- `Intensity` (per-screen parameter)
    

---

**1. Scanlines**

`float scan = sin(UV.y * ScreenHeight * 1.5); scan = smoothstep(0.2, 0.8, scan); color *= lerp(0.85, 1.0, scan);`

---

**2. Chromatic Aberration**

`float2 offset = float2(1.0 / ScreenWidth, 0);  float r = tex(ScreenTex, UV + offset).r; float g = tex(ScreenTex, UV).g; float b = tex(ScreenTex, UV - offset).b;  color = float3(r, g, b);`

---

**3. Gaussian Blur (Soft Authority)**

- Small radius blur (1–1.5 px)
    
- Applied _before_ bloom
    
- Prevents modern razor-sharp UI
    

---

**4. Phosphor Bloom / Command Glow**

`float luminance = dot(color, float3(0.299, 0.587, 0.114)); float glow = saturate(luminance - 0.6);  color += glow * float3(0.6, 0.8, 1.0) * Intensity;`

---

**5. Flicker (Sub-Perceptual)**

`float flicker = sin(Time * 120.0) * 0.02; color *= (1.0 + flicker);`

---

**Output**

- Emissive-only contribution
    
- No real-time shadows
    
- Screen _lights the scene_, not the other way around
    

---

## PART 3: CAMERA & FRAMING RIGS

### Camera Behavior

**Rig Type**

- First-person
    
- Camera is **rig-mounted**, not head-mounted
    
- Micro-motion is _mechanical_, not organic
    

**Procedural Motion**

- Vertical bob: minimal
    
- Slight **inertial lag** on pitch/yaw (0.08–0.12s)
    
- Feels like mass + restraint
    

**FOV**

- **65–70°**
    
- Never widen for speed or spectacle
    

**Rotation**

- No acceleration curves
    
- Linear response
    
- Optional snap-turns (45° / 90°) for menus or critical systems
    

**Rule:**  
The camera never expresses curiosity—only compliance.

---

## PART 4: UI / UX AS A WORLD SYSTEM

### Diegetic UI Philosophy

UI exists **inside power structures**, not for player comfort.

---

### Fonts

- **Monospaced only**
    
- Bitmap or pixel-snapped
    
- Examples:
    
    - OCR-B
        
    - Share Tech Mono
        
    - IBM Plex Mono (bitmap export)
        
- No sub-pixel AA
    

---

### Color Palette (Canonical)

- **Active / Confirmed:** `#8fd3ff`
    
- **Inactive / System Idle:** `#3a506b`
    
- **Warnings / Errors:** `#ffaa00`
    
- **Critical / Override:** `#ff3b30`
    
- **Background UI Black:** `#0b0f14`
    

---

### Animation Principles

- No easing curves
    
- Instant state changes or **hard linear wipes**
    
- CRT-style horizontal refresh wipes for:
    
    - Scene changes
        
    - Authority handovers
        
- Blinking allowed only at **1–2 Hz**, never smooth pulsing
    

---

## PART 5: CONTENT CREATION GUIDELINES

### Asset Priority Order

**1. Foreground Props (Highest Fidelity)**

- Hands
    
- Switches
    
- Knobs
    
- Levers
    
- Screens
    
- Must show:
    
    - Wear
        
    - Oil
        
    - Finger grime
        
    - Manufacturing tolerances
        

**2. Midground Interfaces**

- Consoles
    
- Panels
    
- Racks
    

**3. Background World (Suppressed)**

- Low detail
    
- Fog-dominated
    
- Reduced contrast
    
- Often silhouette-only
    

---

### Lighting Scenario

**Primary Light**

- Screens
    
- LEDs
    
- Status indicators
    
- Color-biased blue/cyan
    

**Ambient**

- Near black
    
- Values < 0.05 intensity
    

**Prohibitions**

- ❌ Warm global lights
    
- ❌ Hero rim lighting
    
- ❌ Cinematic key/fill setups
    

**Rule:**  
If a light doesn’t communicate function, it doesn’t exist.

---

### Baking Policy

- **No baked lighting**
    
- Everything real-time
    
- Shadows are sharp, unforgiving, and often incomplete
    
- Creates a sense of surveillance infrastructure
    

---

## PART 6: AUDIO DESIGN COROLLARY

### UI Sounds

- Short
    
- Dry
    
- Mid-frequency (1–3 kHz)
    
- Slight distortion
    
- No reverb
    
- Think: military surplus hardware
    

---

### Ambience

- Continuous low hum
    
- HVAC drones
    
- Electrical noise
    
- No silence, no music
    
- Silence would imply freedom
    

---

### Voice

- Always filtered:
    
    - Walkie-talkie
        
    - Intercom
        
    - CRT speaker emulation
        
- Narrow bandwidth
    
- Slight latency
    
- Authority speaks _through systems_, never directly
    

---

## FINAL DIRECTIVE

This style is not about nostalgia or cyberpunk aesthetics.  
It is about **operational power**, **emotional suppression**, and **interface dominance**.

If a feature feels expressive, cinematic, or “cool,” it is probably wrong.  
If it feels procedural, cold, and inevitable—you are doing it correctly.

You are a **Real-Time Graphics Engineer**. Your expertise is translating visual art direction into actionable, optimized settings for a modern game engine (Unreal Engine 5).

I have a visual style defined by four pillars:
1.  **Instrumental Totalitarian Framing** (First-person, interface-locked, hands foregrounded).
2.  **Cold-State Chromatic Minimalism** (Steel blues, muted ambers, dead blacks, aggressive desaturation).
3.  **CRT Command Glow** (CRT bloom, scanlines, phosphor glow on screens only).
4.  **Liminal Power Displacement** (Static cameras, symmetrical UI, emblematic imagery).

**Your Task:** Design the **complete graphics pipeline** to achieve this style in-engine.

**Output this SPECIFIC technical document:**

**A. Post-Process Volume Settings (Exact Values)**
*   **Color Grading (Lift/Gamma/Gain):**
    *   Lift: (R, G, B) - e.g., "Shift shadows toward blue: (0.95, 1.0, 1.05)"
    *   Gamma: (R, G, B) - e.g., "Desaturate midtones by reducing G & B relative to R"
    *   Gain: (R, G, B) - e.g., "Ensure highlights are cold, not white"
*   **Global Saturation:** -40
*   **Tonemapping:** "Neutral with a lowered white clip point to 0.8"
*   **Vignette:** "Intensity 0.4, with a cold cyan tint."

**B. Lighting & Atmosphere Setup**
*   **Fog:** "Exponential Height Fog with dense, cold blue (Hex #2a3b54) density."
*   **Sky Atmosphere:** "Disabled. World should feel like an interior or endless void."
*   **Global Illumination:** "Lumen enabled, but with **Ambient Light** biased to blue (Temperature: 12000K)."
*   **Rule:** "No warm point lights. All practical lights are cold LEDs (Hex #6f8fa3)."

**C. The "CRT Screen" Material (Shader Graph Recipe)**
This is the most important asset. Describe the node network:
1.  **Input:** `Emissive Texture` (the screen's content).
2.  **Node 1:** `Blur` node (Radius 1.2) to soften.
3.  **Node 2:** `Scanline` pattern (1px lines, tiled) blended with `Overlay`.
4.  **Node 3:** `Chromatic Aberration` node (shift R +0.005, B -0.005).
5.  **Node 4:** `Bloom Threshold` set very low (0.1) so the screen bleeds glow.
6.  **Output:** Plug final result into `Emissive Color` at high intensity (5.0).

**D. World Material Master (Parent Material)**
*   **Base Color:** "Plug a `Desaturation` node (0.6) between texture and base color."
*   **Specular:** "Keep low (0.2) and metallic (0.1) to avoid plastic shine."
*   **Rule:** "All environment materials inherit from this to enforce global desaturation."

**E. Camera & Player Controller Specs**
*   **FOV:** 70 degrees (narrow for tunnel vision).
*   **Motion Blur:** Per-object motion blur enabled, but camera motion blur disabled (to keep interfaces crisp during head movement).
*   **Depth of Field:** "Set to a fixed focus on the player's hands/foreground interface. The distant world is permanently blurred."

**F. First-Person Hands Model Requirements**
*   "Model must have **highly detailed knuckles, wrist seams, and glove texturing**."
*   "Rig must allow for **precise, mechanical finger movements** (button presses, lever flips) not fluid natural motion."
*   "Shader on hands should have a slight **subsurface scattering** value to mimic skin under cold light, but keep it subtle."

**Now, generate the complete technical brief.**