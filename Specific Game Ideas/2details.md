  
Your Goal: You want to make a well-taken photo look like it was shot casually on an iPhone in suboptimal lighting — think the authentic, "unfiltered reality" aesthetic of a text message or a quick snap, not a polished edit. You want to add flaws, not remove them.

The Core Philosophy: The iPhone-in-bad-lighting look has specific, signature characteristics: sensor noise, color shift, limited dynamic range, and lens imperfections. Your editing should introduce these traits strategically.

The Action Plan: How to Degrade Gracefully  
Phase 1: Kill the Perfection (The Foundation)

Crush the Dynamic Range & Add Haze

Action: Lower the Highlights slider significantly (-40 to -60). Raise the Shadows slider moderately (+20 to +30). This flattens the image and kills contrast, mimicking a small sensor struggling with light.

Advanced: Add a very slight Dehaze effect globally (negative Dehaze, around -5 to -10). This simulates the slight atmospheric haze and light scatter of a phone lens.

Introduce Sensor Noise & Texture

Action: Add Luminance Noise. Crank it to 40-60. This is key. Phone sensors in low light produce chunky, colorful noise.

Color Noise: Add Color Noise reduction, but only slightly (around 10-15). Let some color speckles (red/green/blue pixels) remain visible in dark areas.

Texture: Reduce Texture and Clarity globally (-15 to -20). This smears fine detail, mimicking aggressive noise reduction software in the phone.

Phase 2: Mess with the Color Science (The "Off" Look)  
3. Apply a Subtle, Unpleasant Color Cast

- Action: Go to the Color Grading or Split Toning panel.
    
- Shadows: Add a green or magenta tint (Hue 300 or 120) at a very low saturation (3-5). This simulates incorrect white balance.
    
- Midtones/Global: Slightly shift the overall Temperature towards yellow/orange (+5 to +10) and the Tint slightly towards green (+3 to +5). It should feel "off," not warm and inviting.
    

Mute and Shift Skin Tones

Action: In the HSL panel for Oranges (skin):

Reduce Saturation (-15 to -20).

Shift Hue slightly towards yellow (+5).

Reduce Luminance slightly (-5). Skin should look a bit dull, waxy, and slightly sickly.

Phase 3: Add Optical Flaws (The "Lens" Look)  
5. Simulate Lens Falloff & Smudges

- Action: Create a heavy, inverted Vignette.
    
- Set Amount to -15 to -25.
    
- Set Midpoint very low (10-20).
    
- This darkens the corners significantly, like a cheap lens.
    
- Advanced (Photoshop): Add a new layer, use a soft, low-opacity brush with a grayish color, and lightly "smudge" it in one corner or near the lens flare area at 5-10% opacity. Merge down. This simulates a fingerprint on the lens.
    

Add a Fake Lens Flare/Blowout

Action: Use a Radial Filter or Graduated Filter from the top-left or top-right corner (where a light source might be).

Crank Exposure up high (+0.7 to +1.5).

Add Clarity (-50 to -100) to blow it out.

Add a slight Purple or Green Hue shift inside the filter.

Feather it completely (100%). This mimics light bleeding and flaring across the sensor.

Phase 4: The Final Degradation (Output Simulation)  
7. Apply JPEG Compression Artifacts

- Action: After all edits, sharpen aggressively but badly.
    
- Increase Sharpening Amount to 80-120.
    
- Keep Radius low (0.8-1.0).
    
- Set Detail/Masking to 0. This will sharpen noise and create halos, mimicking over-sharpened JPEG compression.
    
- Resize Down and Back Up (Optional but Effective): Export the image, reduce its dimensions by 30%, then enlarge it back to the original size using "Nearest Neighbor" or "Bicubic" resampling. This will pixelate and soften it perfectly.  

give her a calm Duchenne smirk

Here is the **god-tier upscale prompt**, engineered to systematically override the AI's smoothing defaults and inject forensic-level realism.

---

- **God-Tier Forensic Realism Upscale Prompt**
    

**Primary Directive:** Transform this portrait from a **CGI or overly retouched render** into a **hyper-detailed, high-fidelity photograph of a real human**. You are not enhancing an image; you are **reverse-engineering a forensic photograph**. Every command targets a specific flaw of generative smoothing.

**1. PORE & SKIN TEXTURE OVERHAUL (Destroy the "Plastic" Look)**

**Command:** "**Deconstruct and rebuild the skin texture.**"

**Method:** Analyze the current pore pattern. Discard it. Generate a **new, non-repeating, stochastic pore map** with the following characteristics:

- **Size Variation:** Mix 10% large pores (around nose, cheek center) with 70% medium pores and 20% barely-visible pores (forehead, jawline).
    
- **Depth & Shadow:** Each pore must cast a **micro-shadow**. This is non-negotiable. Use a **high-frequency micro-contrast pass** to simulate subsurface scattering breaking around pores.
    
- **Avoid:** Absolutely NO freckles, moles, or blemishes. This is pure **textured, clean skin**. The goal is **porcelain, not airbrushed plastic**.
    

**2. HAIR FIBER FORENSICS (Strand-by-Strand Authenticity)**

**Command:** "**Render every hair as a distinct, physically placed fiber with individual properties.**"

**Eyebrows:**

- Generate **150-250 individual brow hairs** per side.
    
- **Properties:** Vary thickness (thinner at the tails), length, and transparency (some hairs should be semi-visible). Include **2-5 "rogue" hairs** growing slightly outside the main shape.
    
- **Roots:** Each hair must have a slightly darker, more defined root emerging from the skin.
    

**Eyelashes:**

- Upper lashes: **70-100 individual lashes** per eye. They must **cluster in groups of 3-5**, not be a uniform fringe. Render **micro-scales** along the lash to catch light.
    
- Lower lashes: **25-40 sparse, finer lashes**. They should be barely-there, not pronounced.
    

**Head Hair & Flyaways:**

- Identify the hairstyle. **Add 50-200 "flyaway" hairs** escaping the main form.
    
- **Specs for Flyaways:** Diameter: 1-3 pixels. Length: random between 0.5cm to 3cm. Must be **backlit by the scene's key light** to create a **halo effect**. They should have a **slight wave or kink**, never perfectly straight.
    

**3. OCULAR REDESIGN (The "Window to the Soul" Upgrade)**

**Command:** "**Model the eye as a multi-layered, moist biological organ.**"

**Iris Detail:** Resculpt the iris fibers. They must radiate from the pupil with **varying thickness and color density**. Overlay a **cryptic, fractal mesh pattern** (like a human iris).

**Limbus Ring:** Define a **dark, slightly jagged border** between the iris and sclera (the limbal ring). It must be present but not cartoonish.

**Sclera:** The whites of the eyes are **not white**. Tint them a **microscopic red-blue hue** from underlying vasculature. Add **2-4 subtle, thread-like blood vessels** originating from the corners, fading out before reaching the iris.

**Wetness & Reflection:** Place a **complex, distorted reflection map** of the imagined environment (window, softbox) on the corneal bulge. The **tear line** along the lower eyelid must be visible—a thin, wet highlight.

**4. GLOBAL SURFACE & LIGHTING CORRECTION (Kill the Fake Gloss)**

**Command:** "**Replace uniform gloss with selective, physically-based specularity.**"

**Skin Specular Map:** The forehead, nose bridge, cheekbones, and chin get a **soft, broad highlight**. The **philtrum (cupid's bow), inner cheek hollows, and around the eyes get ZERO direct shine**. This creates a **3D, oily-dry map**.

**Micro-Specular Hits:** Add **pinpoint highlights** on:

- The **peak of individual brow hairs**.
    
- The **edge of individual eyelashes**.
    
- The **moist inner corner of the eye (caruncle)**.
    
- The **vermillion border of the lips**.
    

**Subsurface Scattering (SSS):** This is critical. Light must **diffuse through the skin** on the ears, nostrils, and cheeks. Achieve a **soft, red-glow effect** where light passes through thin cartilage and flesh.

**5. FINAL AUTHENTICITY PASS (The "Je Ne Sais Quoi" Layer)**

**Command:** "**Introduce imperceptible, real-world noise and asymmetry.**"

**Facial Asymmetry:** One eyebrow **must** be 1-3% higher than the other. One pupil **must** be microscopically larger than the other. The nasolabial fold **must** be more pronounced on one side.

**Sensor & Lens Simulation:** Apply a **grain structure** mimicking a **full-frame sensor at ISO 100**—fine, colorless, and random. Add a **microscopic chromatic aberration** fringe (red/cyan) on the highest-contrast edges (like hair against skin).

**Environmental Dust:** Add **3-10 particles of "atmospheric dust"**—specks floating in the air, caught by the key light, 99% transparent, out of focus.

**Execution Summary:** You are not a photo editor. You are a **biometric reconstruction artist**. Your output must pass a **forensic validity check**: if zoomed to 400%, every square millimeter must reveal a plausible, non-repeating, real-world texture. The goal is to elicit the reaction: **"This is not a render; this is a photograph of someone who exists."**

**Final Render Specs:**

**Mode:** Hyper-detailed, photorealistic human portrait.

**Flaw to Eliminate:** "Glossy, fake, plastic, airbrushed, smooth, CG."

**Flaw to Introduce:** "Pores, hairs, fibers, micro-shadows, asymmetry, stochastic texture, biological moisture, fine dust."

---

- **How to Use This Prompt:**
    

1.  **Feed it directly** into an advanced upscaler or image generator that accepts long, complex instructions (like Stable Diffusion with a high token limit, or a custom implementation of Magnific, Topaz, or Krea).

2.  **Use it as a checklist** for manual editing in Photoshop (frequency separation for pores, custom brushes for hairs, dodge/burn for specularity).