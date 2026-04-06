**Goal:** Transform my photo into a **1990s arcade cabinet/Doom-style** visual: gritty, low-res, with CRT screen artifacts and a constrained, vibrant color palette.

**Core Aesthetic Pillars:**

- **Color Palette:** **16-bit constrained**. Dominated by neon-edged **reds, cyans, deep purples, and acidic yellows** against near-black shadows.
    
- **Contrast:** **Extreme, with crushed blacks**. Almost no midtones. Use **posterization** to reduce color bands.
    
- **Texture & Detail:** **Heavy pixelation** (nearest-neighbor scaling) and **visible scanlines**. Add **chromatic aberration** (red/cyan channel shift) and **bloom** on light sources.
    
- **Lighting:** Light appears as **flat, emissive shapes**, not gradients. Harsh, directional, and unrealistic.
    

**Directive:** Do not simply apply a filter. **Remap the image's fundamental components** (light, shadow, color, detail) to match the technical limitations and artistic style of 90s arcade hardware.

**Process:**

**Phase 1: Foundation – Pixel & Palette**

1. **Downscale & Repixel:** Reduce image dimensions to **320px width** using **Nearest Neighbor** interpolation. Then upscale back to original size by **400% using Nearest Neighbor**. This creates hard, blocky pixels.
    
2. **Posterize & Crush:** Apply **Posterization** to 4-6 levels. Use **Levels** or **Curves** to **crush blacks** (input black point to ~50) and **clip whites** (input white point to ~200).
    

**Phase 2: Color – 16-Bit Remapping**  
3. **Color Remap:** Use a **Gradient Map** with this specific gradient:  
`#000000` (Pure Black) → `#6B00B3` (Deep Purple) → `#FF004D` (Neon Red) → `#00E6FF` (Cyan) → `#FFFF00` (Acid Yellow) → `#FFFFFF` (White).  
Adjust opacity to 30-50% and set blend mode to **Color**.  
4. **Selective Saturation:** **Desaturate** everything except reds and cyans. Boost **Red Saturation +50**, **Cyan Saturation +40**.

**Phase 3: CRT Screen Effects – The "Cabinet" Feel**  
5. **Scanlines:** Create a new layer with a **1px black line, 1px transparent line** pattern. Set blend mode to **Multiply** at 15% opacity.  
6. **Chromatic Aberration:** Duplicate layer twice. On the top copy, **disable Red channel**, nudge layer 2px right. On the copy below, **disable Blue & Green channels**, nudge layer 2px left. Set both to **Lighten** at 70% opacity.  
7. **Bloom:** Duplicate layer, apply **Gaussian Blur** (radius 15px), set to **Screen** blend mode at 40% opacity. Mask to only bright areas.

**Output Format:**

1. **Phase Summary:** List the 3 phases you'll execute.
    
2. **Key Settings:** Provide the exact values for: Posterization Levels, Gradient Map colors, Pixel Scaling %.
    
3. **Final Check:** Does it look like a screenshot from a 90s arcade shooter? (YES/NO)
    

**My Photo:** [Describe subject/lighting]