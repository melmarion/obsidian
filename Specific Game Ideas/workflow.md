# AI Website Generation Workflow: Optimized Prompts

Based on the transcript, here's the complete prompt system for building modern, animated parallax websites using Google's AI tools.

---

## **WORKFLOW OVERVIEW**

```
Stage 1: NanoBanana (in Google Whisk) → Generate start/end frames
Stage 2: Google Veo 2 (in Google Flow) → Create motion between frames
Stage 3: Conversion → Video to WebP
Stage 4: Firebase Studio → Build parallax website
```

---

## **STAGE 1: NanoBanana Frame Generation Prompts**

### **Starting Frame Prompt Template**

```markdown
# 🎨 Starting Frame Prompt (NanoBanana in Google Whisk)

**Purpose:** Establish visual foundation—lighting, mood, composition, and style that the entire site will follow.

**Prompt Structure:**

A [PRODUCT_TYPE] product photography shot with [LIGHTING_STYLE] lighting, featuring [MAIN_PRODUCT] as the hero focal point. [COMPOSITION_DETAILS]. The scene has [COLOR_PALETTE] with [TEXTURE_DESCRIPTION]. [MOOD_DESCRIPTOR] aesthetic with [DEPTH_ELEMENTS]. Shot with [CAMERA_STYLE] on a [BACKGROUND_TYPE] background. Ultra-modern, clean, premium product photography style with soft shadows and balanced spacing.

---

## **FILL-IN-THE-BLANKS GUIDE:**

**PRODUCT_TYPE:**
- Options: beverage, tech gadget, skincare, fashion accessory, food item, wellness product
- Example: "premium soda can"

**LIGHTING_STYLE:**
- Options: soft diffused, dramatic side-lit, golden hour, studio key light, natural window light, neon accent
- Example: "soft diffused studio lighting with subtle rim highlights"

**MAIN_PRODUCT:**
- Be specific about product + key visual elements
- Example: "a sleek aluminum can with minimalist label design, condensation droplets visible"

**COMPOSITION_DETAILS:**
- Describe arrangement, angle, props
- Example: "Centered in frame at 3/4 angle, surrounded by fresh fruit slices and ice cubes floating in mid-air"

**COLOR_PALETTE:**
- Use 2-3 dominant colors
- Example: "pastel pink and cream tones with pops of vibrant coral"

**TEXTURE_DESCRIPTION:**
- Surface qualities
- Example: "matte product finish contrasting with glossy water droplets and soft fabric backdrop"

**MOOD_DESCRIPTOR:**
- Options: minimalist, playful, luxurious, energetic, serene, bold, sophisticated
- Example: "modern minimalist"

**DEPTH_ELEMENTS:**
- What creates layering?
- Example: "layered depth using foreground fruit elements, mid-ground product, and soft-focus background gradient"

**CAMERA_STYLE:**
- Options: medium format, 50mm prime, macro lens, wide-angle, telephoto
- Example: "medium format camera (Hasselblad style) with shallow depth of field"

**BACKGROUND_TYPE:**
- Options: seamless gradient, textured paper, frosted glass, solid color, abstract geometric
- Example: "soft gradient transitioning from warm cream to cool lavender"

---

## **EXAMPLE PROMPTS (Ready to Use):**

### Example 1: Soda Product
```

A premium beverage product photography shot with soft diffused studio lighting, featuring a sleek aluminum soda can with minimalist modern label design as the hero focal point. Centered in frame at 3/4 angle, surrounded by fresh citrus slices and ice cubes suspended in mid-air with subtle motion blur. The scene has pastel pink, cream, and vibrant coral tones with matte aluminum texture contrasting with glossy water droplets. Modern minimalist aesthetic with layered depth using foreground fruit elements, mid-ground product, and soft-focus background gradient. Shot with medium format camera style on a soft gradient background transitioning from warm cream to cool lavender. Ultra-modern, clean, premium product photography with soft shadows and balanced spacing.

```

### Example 2: Tech Product
```

A sleek technology product photography shot with dramatic side-lighting and neon accent highlights, featuring a matte black wireless earbud case with LED indicator as the hero focal point. Positioned at 45-degree angle on reflective surface, surrounded by floating geometric shapes and light trails. The scene has deep navy, electric blue, and silver metallic tones with brushed metal texture and glass reflections. Bold futuristic aesthetic with layered depth using foreground light particles, mid-ground product, and bokeh background elements. Shot with 50mm prime lens style with ultra-shallow depth of field on a dark gradient background with subtle grid pattern. Ultra-modern, premium tech photography with sharp highlights and moody atmosphere.

```

### Example 3: Wellness Product
```

A natural wellness product photography shot with soft natural window lighting, featuring an organic glass serum bottle with minimalist kraft paper label as the hero focal point. Positioned slightly off-center at eye level, surrounded by fresh botanical elements like eucalyptus leaves and smooth river stones. The scene has earthy sage green, warm beige, and soft white tones with frosted glass texture and natural wood accents. Serene organic aesthetic with layered depth using foreground botanical blur, mid-ground product focus, and soft-focus natural background. Shot with macro lens style capturing fine detail on a textured handmade paper background. Ultra-modern, clean, natural product photography with gentle shadows and organic spacing.

```

---

## **PRO TIPS FOR STARTING FRAMES:**

1. **Reference Image Upload:**
   - Upload 1-2 reference images that match your desired style
   - Tell NanoBanana: "Match the lighting and color tone of this reference"

2. **Consistency Checkers:**
   - ✅ Clean lighting (no harsh shadows)
   - ✅ Balanced spacing (not cluttered)
   - ✅ Clear focal point (product is hero)
   - ✅ Soft modern color tones (not oversaturated)
   - ✅ Professional depth (foreground/background separation)

3. **If Results Are Off:**
   - Too busy? → Add "minimal composition, lots of negative space"
   - Too flat? → Add "layered depth with foreground elements out of focus"
   - Wrong colors? → Be more specific: "exactly #FFB6C1 pink and #F5F5DC cream"
   - Too dark? → Add "bright, high-key lighting with lifted shadows"
```

---

### **Ending Frame Prompt Template**

```markdown
# 🎬 Ending Frame Prompt (NanoBanana in Google Whisk)

**Purpose:** Define the destination state—how the scene should look after motion/transition.

**Prompt Structure:**

[COPY STARTING FRAME PROMPT], but now [TRANSFORMATION_DESCRIPTION]. The [MAIN_PRODUCT] has [POSITION_CHANGE]. [NEW_ELEMENTS_ADDED]. [LIGHTING_EVOLUTION]. Maintain the same [COLOR_PALETTE] and [MOOD_DESCRIPTOR] aesthetic, ensuring visual continuity with the starting frame.

---

## **TRANSFORMATION TYPES:**

**Subtle Motion (for smooth parallax):**
- "slightly rotated 15 degrees clockwise"
- "shifted 20% to the left with increased depth blur on background"
- "zoomed in 1.3x with tighter crop on product label"

**Dynamic Motion (for bold animations):**
- "product exploded into floating ingredient particles"
- "can opened with liquid splash frozen mid-air"
- "transformed into wireframe outline with glowing edges"

**Environmental Change:**
- "background shifted from warm cream to cool blue gradient"
- "lighting changed from soft diffused to dramatic side-lit"
- "foreground elements scattered outward creating radial motion"

---

## **EXAMPLE ENDING FRAME PROMPTS:**

### Example 1: Soda Product (Subtle Parallax)
```

A premium beverage product photography shot with soft diffused studio lighting, featuring a sleek aluminum soda can with minimalist modern label design as the hero focal point. Now rotated 20 degrees counter-clockwise and shifted slightly upward, creating upward motion trajectory. The can has slight motion blur on the edges suggesting movement. Citrus slices and ice cubes have drifted further apart with increased separation, some exiting frame. Background gradient has deepened from cream to richer peachy-coral tone. Maintain the same pastel pink, cream, and coral color palette with modern minimalist aesthetic, ensuring visual continuity with the starting frame. Shot with medium format camera style with slightly wider depth of field to show motion trail.

```

### Example 2: Tech Product (Dynamic)
```

A sleek technology product photography shot with dramatic side-lighting and intensified neon highlights, featuring the matte black wireless earbud case now opened at 90-degree angle revealing the earbuds inside glowing with LED indicators. The case has rotated 45 degrees and shifted to lower-right quadrant. Geometric shapes have scattered outward in radial pattern with motion streaks. Light trails have extended and multiplied creating dynamic energy. Background has shifted from navy to deep purple-blue gradient with increased glow intensity. Maintain the same navy, electric blue, and silver metallic tones with bold futuristic aesthetic, ensuring visual continuity with the starting frame.

```

### Example 3: Wellness Product (Environmental Shift)
```

A natural wellness product photography shot with soft natural lighting now transitioning to golden hour warmth, featuring the organic glass serum bottle slightly tilted 10 degrees with one drop of serum suspended in mid-air below the dropper cap. The bottle has shifted to left-third composition. Botanical elements have gently drifted with soft motion blur showing gentle breeze effect. River stones remain grounded but with added warm glow reflection. Background has evolved from neutral beige to warmer amber-gold tone while maintaining organic texture. Maintain the same sage green, beige, and white color palette with serene organic aesthetic, ensuring visual continuity with the starting frame.

```

---

## **CRITICAL RULES FOR ENDING FRAMES:**

1. **Maintain Visual DNA:**
   - Same lighting quality (just adjusted intensity/direction)
   - Same color family (just shifted hue/saturation)
   - Same composition style (just altered position/scale)

2. **Motion Indicators:**
   - Add these phrases: "with motion blur", "trailing effect", "drift pattern", "momentum trajectory"
   - This helps Veo 2 understand the motion direction

3. **Continuity Anchors:**
   - Always end with: "ensuring visual continuity with the starting frame"
   - Reference specific elements that should remain: "maintaining the same product label visibility"

4. **Test for Smooth Animation:**
   - Starting + Ending frames should be able to transition smoothly
   - Too drastic = jarring animation
   - Too similar = boring static result
   - Sweet spot: 15-30% visual change
```

---

## **STAGE 2: Google Veo 2 Motion Prompt**

```markdown
# 🎬 Motion Generation Prompt (Google Veo 2 in Google Flow)

**Purpose:** Define how the animation should behave between start and end frames.

**Use Mode:** Frame-to-Video in Google Flow

**Base Motion Prompt Template:**

Smooth cinematic [MOTION_TYPE] transition with [PACING_DESCRIPTOR] timing. [ELEMENT_MOTION_1]. [ELEMENT_MOTION_2]. [CAMERA_BEHAVIOR]. Premium product photography motion with [TECHNICAL_SPECS]. [MOOD_MOTION]. No cuts, no jumps, seamless continuous flow.

---

## **MOTION TYPES:**

**Parallax Motion:**
- "multi-layered parallax with foreground moving faster than background"
- "depth-based motion where closer elements drift left while distant elements drift right"

**Rotation:**
- "slow orbital rotation around central axis"
- "gentle tumble with 360-degree reveal"

**Scale:**
- "smooth zoom-in focusing on product detail"
- "pull-back reveal showing full scene context"

**Drift:**
- "floating upward motion with subtle rotation"
- "lateral slide with momentum decay"

---

## **PACING DESCRIPTORS:**
- "slow luxurious" (3-5 second feel)
- "medium steady" (2-3 second feel)
- "quick snappy" (1-2 second feel)
- "variable with ease-in-ease-out"

---

## **ELEMENT MOTION SPECIFICATIONS:**

Format: "[Element] + [motion verb] + [direction] + [speed/quality]"

Examples:
- "Product can rotates clockwise 20 degrees with subtle wobble"
- "Citrus slices drift diagonally outward at varying speeds creating depth"
- "Ice cubes float upward with gentle bobbing motion"
- "Background gradient shifts smoothly from warm to cool tones"
- "Light reflections slide across metallic surface"

---

## **CAMERA BEHAVIORS:**

**Static Camera (for product focus):**
- "Fixed camera position maintaining centered composition"
- "Locked perspective allowing only subject motion"

**Dynamic Camera (for cinematic feel):**
- "Subtle dolly-in movement bringing viewer closer"
- "Slow parallax camera drift revealing depth layers"
- "Gentle crane-up motion adding vertical reveal"

---

## **TECHNICAL SPECS:**

Always include:
- "Consistent lighting throughout transition"
- "Shallow depth of field with smooth focus tracking"
- "Motion blur on moving elements for realism"
- "No strobing or stuttering"
- "Physically accurate momentum and weight"

---

## **MOOD MOTION DESCRIPTORS:**

Match your brand:
- Luxury: "Elegant slow-motion with graceful transitions"
- Energetic: "Dynamic quick pacing with snappy movements"
- Natural: "Organic flowing motion with subtle irregularity"
- Tech: "Precise geometric movements with sharp timing"
- Playful: "Bouncy movements with overshoot and settle"

---

## **COMPLETE EXAMPLE PROMPTS:**

### Example 1: Soda Parallax (Smooth & Premium)
```

Smooth cinematic multi-layered parallax transition with slow luxurious timing. Product can rotates counter-clockwise 20 degrees while drifting upward with gentle float. Citrus slices scatter outward in radial pattern at varying speeds creating depth separation, foreground elements moving faster than background. Ice cubes float and tumble with realistic physics and subtle sparkle reflections. Background gradient shifts smoothly from cream to peachy-coral with soft blur increase. Fixed camera position maintaining centered composition. Premium product photography motion with consistent soft lighting throughout transition, shallow depth of field with smooth focus tracking on product label, motion blur on moving elements for realism, no strobing. Elegant slow-motion with graceful transitions creating luxurious premium feel. No cuts, no jumps, seamless continuous flow.

```

### Example 2: Tech Product (Bold & Dynamic)
```

Smooth cinematic rotation and reveal transition with medium steady timing. Earbud case opens from closed to 90-degree angle in fluid mechanical motion, revealing glowing LED earbuds inside. Case rotates 45 degrees clockwise while shifting to lower-right quadrant. Geometric shapes explode outward in radial burst pattern with sharp motion trails. Light streaks extend and multiply creating energy wave effect. Background shifts from navy to deep purple with pulsing glow intensity increase. Subtle dolly-in camera movement bringing viewer closer to product detail. Premium tech photography motion with dramatic lighting evolution, deep depth of field keeping all elements sharp, crisp motion blur on fast-moving particles, physically accurate geometric trajectories. Dynamic quick pacing with snappy movements creating futuristic high-tech feel. No cuts, no jumps, seamless continuous flow.

```

### Example 3: Wellness Product (Organic & Calm)
```

Smooth cinematic drift transition with slow luxurious timing. Serum bottle tilts gently 10 degrees to the left while single droplet forms and falls in slow motion from dropper. Bottle shifts to left-third composition with smooth lateral slide. Botanical leaves sway and drift with soft breeze effect, creating gentle wave pattern motion. River stones remain grounded with subtle shadow shifts as lighting evolves. Background transitions from neutral beige to warm amber-gold with organic texture fade. Gentle crane-up camera motion adding subtle vertical reveal. Premium natural product photography motion with golden hour lighting evolution, ultra-shallow depth of field with dreamy bokeh on background botanicals, subtle motion blur on drifting elements maintaining organic feel, soft physics with floating quality. Elegant slow-motion with graceful flowing transitions creating serene peaceful atmosphere. No cuts, no jumps, seamless continuous flow.

```

---

## **PRO TIPS FOR MOTION PROMPTS:**

1. **Physics Matters:**
   - Heavy objects (cans): "with weighted momentum"
   - Light objects (leaves): "with floating weightless drift"
   - Liquids: "with fluid dynamics and splash behavior"

2. **Speed Variation Creates Interest:**
   - "Foreground elements move at 1.5x speed of background"
   - "Acceleration in first third, constant motion in middle, deceleration in final third"

3. **Quality Checks After Generation:**
   - ✅ Smooth motion (no stuttering)
   - ✅ Elements don't clip/disappear
   - ✅ Lighting stays consistent
   - ✅ Product remains hero focus
   - ✅ Motion feels intentional (not random)

4. **If Motion Looks Wrong:**
   - Too fast? → Add "slow luxurious timing with ease curves"
   - Too chaotic? → Add "controlled precise movements"
   - Too boring? → Add "dynamic varying speeds creating visual interest"
   - Flickering? → Add "consistent lighting with no strobing"
```

---

## **STAGE 3: Video to WebP Conversion**

````markdown
# 🔄 WebP Conversion Settings (EasyGIF or Similar Tool)

**Purpose:** Convert video to animated WebP format for web performance while maintaining quality and enabling scroll-triggered playback.

---

## **OPTIMAL SETTINGS:**

**Timing:**
- ✅ Start Time: 0:00 (beginning of video)
- ✅ End Time: [Full duration] (entire video length)
- Why: Capture complete animation

**Size:**
- ✅ Dimension: Original (maintain source resolution)
- Why: Preserve quality; we'll optimize with compression

**Frame Rate:**
- ✅ FPS: Closest to native video FPS (typically 24-30fps)
- Recommended: 24fps for smooth motion with reasonable file size
- Don't Max Out: 60fps = huge files with marginal quality gain
- Don't Go Too Low: <20fps = stuttery motion

**Loop:**
- ✅ Forever Loop: CHECKED
- Why: Parallax animations should loop seamlessly for continuous scroll

**Compression:**
- Quality: 85-90% (sweet spot for web)
- Method: Lossy (reduces file size significantly)
- Target: <5MB for fast page load

---

## **FILE SIZE OPTIMIZATION:**

If WebP exceeds 5MB:

**Option 1 - Reduce Duration:**
- Trim to 2-4 seconds (minimum for smooth animation)
- Loop shorter clips feel smoother than long ones

**Option 2 - Scale Resolution:**
- 1920×1080 → 1280×720 (maintains HD feel)
- 1280×720 → 960×540 (still looks sharp on web)

**Option 3 - Lower FPS:**
- 30fps → 24fps (film-like, still smooth)
- 24fps → 20fps (acceptable for slow motion)

**Option 4 - Increase Compression:**
- 90% → 85% → 80% quality
- Test visually: stop when artifacts become noticeable

---

## **QUALITY CHECK:**

Before proceeding to Firebase:
- [ ] Animation plays smoothly (no dropped frames)
- [ ] Colors match original video (no banding)
- [ ] File size <5MB (ideally 2-3MB)
- [ ] Loops seamlessly (no visible "jump" at restart)
- [ ] Product details remain sharp (not pixelated)

---

## **ALTERNATIVE TOOLS:**

If EasyGIF doesn't work:
- **CloudConvert** (web-based, high quality)
- **FFmpeg** (command line, maximum control)
- **Photoshop** (Export → Save for Web → WebP)
- **Online-Convert.com** (simple interface)

---

## **FFMPEG COMMAND (Advanced):**

```bash
ffmpeg -i input.mp4 -vf scale=1280:-1 -vcodec libwebp -lossless 0 -compression_level 6 -q:v 85 -loop 0 -preset default -an -vsync 0 output.webp
````

Breakdown:

- `scale=1280:-1`: Width 1280px, height auto
- `-lossless 0`: Lossy compression (smaller files)
- `-q:v 85`: Quality 85%
- `-loop 0`: Infinite loop
- `-an`: Remove audio track

````

---

## **STAGE 4: Firebase Studio Website Prompt**

```markdown
# 🏗️ Firebase Studio Build Prompt

**Purpose:** Transform design assets into a functional parallax website with clean code, responsive layout, and smooth scroll behavior.

---

## **MASTER PROMPT TEMPLATE:**

Build a modern single-page parallax website for [BRAND_NAME], a [PRODUCT_CATEGORY] brand with [BRAND_PERSONALITY] aesthetic.

**DESIGN SYSTEM:**
- Primary color: [HEX_CODE]
- Secondary color: [HEX_CODE]
- Accent color: [HEX_CODE]
- Typography: [FONT_FAMILY] for headings, [FONT_FAMILY] for body
- Spacing: 8pt grid system with [DENSITY_LEVEL] density

**LAYOUT STRUCTURE:**
[SECTION_1]: [Description]
[SECTION_2]: [Description]
[SECTION_3]: [Description]
[FOOTER]: [Description]

**PARALLAX BEHAVIOR:**
- Scroll speed: [LAYER_SPEEDS]
- Trigger points: [SCROLL_PERCENTAGES]
- Animation style: [MOTION_QUALITY]

**RESPONSIVE DESIGN:**
- Mobile breakpoint: 768px
- Tablet breakpoint: 1024px
- Desktop: 1440px+
- Mobile-first approach with touch-optimized interactions

**TECHNICAL REQUIREMENTS:**
- Smooth scroll with easing
- Lazy loading for media assets
- 60fps animation performance
- Accessibility: WCAG AA compliant
- SEO: Semantic HTML5, meta tags

**ASSETS TO INTEGRATE:**
- Hero animation: [FILE_NAME.webp]
- Product images: [LIST_FILES]
- Background layers: [LIST_FILES]

---

## **FILL-IN-THE-BLANKS GUIDE:**

**BRAND_NAME:**
- Your company/product name
- Example: "Ollie Pop Soda"

**PRODUCT_CATEGORY:**
- Industry/vertical
- Example: "premium organic beverage", "luxury skincare", "AI-powered fitness"

**BRAND_PERSONALITY:**
- Pick 2-3 adjectives
- Options: minimalist, playful, luxurious, bold, serene, futuristic, organic, vibrant
- Example: "minimalist and playful"

**COLOR SPECIFICATIONS:**
```javascript
// Use exact hex codes from your NanoBanana frames
primary: '#FFB6C1',    // Main brand color
secondary: '#F5F5DC',  // Supporting color
accent: '#FF6B7A',     // Highlight/CTA color
neutral: '#2D2D2D',    // Text color
background: '#FFFFFF'  // Base background
````

**TYPOGRAPHY:**

```javascript
// Google Fonts work best in Firebase
headings: 'Inter' | 'Outfit' | 'Space Grotesk' | 'Montserrat'
body: 'Inter' | 'DM Sans' | 'Open Sans' | 'Roboto'

// Example pairing:
headings: { family: 'Outfit', weight: 700 }
body: { family: 'Inter', weight: 400, lineHeight: 1.6 }
```

**SPACING DENSITY:**

- `compact`: High information density (SaaS dashboards)
- `comfortable`: Balanced (most websites)
- `spacious`: Premium feel (luxury brands)

---

## **LAYOUT STRUCTURE TEMPLATES:**

### Template 1: Product Landing Page

```
SECTION 1 - HERO:
Full-screen hero with animated WebP background showing [product] in motion. Headline: "[VALUE_PROP]" with CTA button "Shop Now". Parallax effect: background moves at 0.5x scroll speed, foreground text at 1.2x.

SECTION 2 - FEATURES:
Three-column grid showcasing product benefits. Each column has icon, heading, and description. Icons: [ICON_LIST]. Fade-in animation on scroll (trigger at 70% viewport visibility).

SECTION 3 - PRODUCT SHOWCASE:
Horizontal scrolling carousel with 3 flavor variants. Each card shows product image, flavor name, and key ingredient. Cards scale on hover (1.05x transform). Background: subtle gradient.

SECTION 4 - SOCIAL PROOF:
Testimonial slider with customer quotes and 5-star ratings. Automatic rotation every 5 seconds. Reviews fade in from bottom on scroll.

FOOTER:
Logo, navigation links, social media icons, newsletter signup form. Background color: [PRIMARY_COLOR] at 10% opacity. Sticky contact button in bottom-right corner.
```

### Template 2: Portfolio/Agency Site

```
SECTION 1 - HERO:
Split-screen layout. Left: Bold headline + subheadline. Right: Animated WebP showing creative work in motion. Parallax: text layer moves at 1x, animation layer at 0.8x.

SECTION 2 - SERVICES:
Grid of 6 service cards with hover reveal. Default: icon + title. Hover: description slides up from bottom. Staggered animation (50ms delay between cards).

SECTION 3 - CASE STUDIES:
Vertical stack of full-width project images. Each image has parallax scroll (background at 0.6x, overlay text at 1x). Click opens modal with project details.

SECTION 4 - TEAM:
Circular avatar grid with names and roles. Grayscale by default, color on hover. Tooltip shows bio on click.

FOOTER:
Minimalist footer with contact email and social links. Dark background (#2D2D2D) with white text.
```

### Template 3: SaaS Product Page

```
SECTION 1 - HERO:
Centered headline with animated product demo (WebP) below. Two CTAs: "Start Free Trial" (primary) and "Watch Demo" (secondary). Background: animated gradient shifting between brand colors.

SECTION 2 - FEATURES:
Alternating left-right layout. Odd sections: image left, text right. Even sections: text left, image right. Each section fades in + slides horizontally on scroll.

SECTION 3 - PRICING:
Three-column pricing table. Highlight middle tier with elevated card (translateY: -20px) and accent border. Toggle between monthly/annual billing.

SECTION 4 - FAQ:
Accordion with smooth expand/collapse. Only one question open at a time. Rotate chevron icon on toggle.

FOOTER:
Comprehensive footer with multiple columns: Product, Company, Resources, Legal. Newsletter signup with inline validation.
```

---

## **PARALLAX SPECIFICATIONS:**

```javascript
// Define scroll speeds for each layer
PARALLAX_LAYERS = {
  background: 0.3,    // Slowest (far away)
  midground: 0.6,     // Medium depth
  foreground: 1.0,    // Normal scroll speed
  overlay: 1.3        // Fastest (closest to viewer)
};

// Trigger points (when animations start)
SCROLL_TRIGGERS = {
  hero: 0,            // Immediate
  features: '20%',    // 20% down page
  showcase: '50%',    // Halfway
  social: '70%',      // Near bottom
  footer: '90%'       // Almost end
};

// Animation qualities
MOTION_QUALITY = {
  easing: 'cubic-bezier(0.4, 0.0, 0.2, 1)', // Smooth acceleration
  duration: '0.6s',                          // Comfortable timing
  stagger: '100ms'                           // Delay between elements
};
```

---

## **COMPLETE EXAMPLE PROMPTS:**

### Example 1: Soda Brand (Playful & Premium)

```
Build a modern single-page parallax website for Ollie Pop, a premium organic soda brand with minimalist and playful aesthetic.

DESIGN SYSTEM:
- Primary color: #FFB6C1 (soft pink)
- Secondary color: #F5F5DC (cream)
- Accent color: #FF6B7A (coral)
- Neutral: #2D2D2D (charcoal text)
- Background: #FFFFFF
- Typography: 'Outfit' weight 700 for headings, 'Inter' weight 400 for body with 1.6 line-height
- Spacing: 8pt grid system with comfortable density

LAYOUT STRUCTURE:

HERO SECTION:
Full-screen hero (100vh) with animated WebP background showing soda can rotating with floating fruit. Headline: "Sip Something Extraordinary" (72px, Outfit Bold) with subheadline: "Organic sodas that taste amazing and make you feel great" (24px, Inter Regular). Primary CTA: "Shop Flavors" button (accent color, 16px padding, rounded 8px corners). Parallax: background WebP at 0.5x scroll speed, headline at 1.2x, CTA at 1x creating depth separation.

FEATURES SECTION:
Three-column grid (desktop) / vertical stack (mobile) showcasing benefits. Each column: fruit icon (64px), heading (32px Outfit Semibold), description (18px Inter Regular, gray). Icons: 🍊 "Real Fruit", 🌱 "Organic Ingredients", ✨ "Low Sugar". Fade-in animation from bottom (translateY: 30px to 0) on scroll trigger at 70% viewport visibility. Stagger animation 100ms between columns.

PRODUCT SHOWCASE:
Horizontal scrolling carousel (snap-scroll on mobile) with 3 flavor cards. Each card: product WebP image (400x600px), flavor name (40px Outfit Bold), key ingredient badge (secondary color background, 14px Inter Medium). Cards scale 1.05x on hover with smooth 0.3s transition. Background: subtle vertical gradient from white to light pink (#FFB6C110).

SOCIAL PROOF:
Customer testimonial slider with 5-star ratings. Automatic rotation every 5 seconds with fade transition. 3 testimonials: quote text (24px Inter Regular Italic), customer name (18px Outfit Medium), star icons. Slides fade in from bottom on scroll trigger at 80% viewport.

FOOTER:
Ollie Pop logo (left-aligned), navigation links (About, Shop, Contact), social media icons (Instagram, TikTok, Twitter), newsletter signup form (inline with accent button). Background: primary color at 10% opacity. Sticky "Contact Us" button in bottom-right corner (accent color, 50px circle, message icon).

PARALLAX BEHAVIOR:
- Layer speeds: background 0.3x, midground 0.6x, foreground 1x, overlay 1.3x
- Trigger points: hero immediate, features 20%, showcase 50%, social 70%, footer 90%
- Animation style: Smooth with cubic-bezier(0.4, 0, 0.2, 1) easing, 0.6s duration, 100ms stagger

RESPONSIVE DESIGN:
- Mobile breakpoint: 768px (single column, increased touch targets to 44px minimum)
- Tablet breakpoint: 1024px (two-column grid for features)
- Desktop: 1440px+ (full three-column layout)
- Mobile-first approach with swipe gestures for carousel

TECHNICAL REQUIREMENTS:
- Smooth scroll with 0.8s easing
- Lazy loading for all WebP assets (load when 200px from viewport)
- Target 60fps during parallax scroll (use CSS transforms, not position changes)
- Accessibility: Alt text on images, ARIA labels on buttons, keyboard navigation, WCAG AA color contrast
- SEO: Semantic HTML5 structure, meta description, Open Graph tags, schema markup for product

ASSETS TO INTEGRATE:
- Hero animation: soda-hero-parallax.webp
- Product images: flavor-strawberry.webp, flavor-orange.webp, flavor-lemon.webp
- Background layers: gradient-overlay.png, fruit-pattern.svg
```

### Example 2: Tech SaaS (Bold & Futuristic)

```
Build a modern single-page parallax website for NeuralFlow, an AI-powered workflow automation platform with bold and futuristic aesthetic.

DESIGN SYSTEM:
- Primary color: #0A2E4D (deep navy)
- Secondary color: #1E5A8E (bright blue)
- Accent color: #00D9FF (electric cyan)
- Neutral: #E0E0E0 (light gray text)
- Background: #0D0D0D (near-black)
- Typography: 'Space Grotesk' weight 700 for headings, 'DM Sans' weight 400 for body with 1.5 line-height
- Spacing: 8pt grid system with compact density

LAYOUT STRUCTURE:

HERO SECTION: Asymmetric hero layout. Left 40%: Headline "Skincare from Nature" (64px Newsreader Regular, primary color) + subheadline "Botanically crafted for sensitive skin" (22px Inter Light) + CTA "Discover Products" (accent button with soft rounded 12px corners). Right 60%: Animated WebP showing serum bottle with floating botanicals. Parallax: text at 1x, WebP at 0.7x creating gentle depth. Background: soft watercolor texture (secondary color with 30% opacity).

INGREDIENT SECTION: Full-width image banner showing botanical garden (1920x600px) with text overlay. Headline: "Pure Ingredients, Pure Results" (56px Newsreader, centered, white text with subtle shadow). Three floating cards overlaid on image: each card shows ingredient photo (circular 150px), name (24px Inter Medium), benefit text (16px Inter Light). Cards have frosted glass effect (backdrop-filter: blur(10px), white 80% opacity). Parallax: background image at 0.5x, cards at 1x.

PRODUCT GRID: Four-column grid (responsive to 2-col tablet, 1-col mobile) showing product lineup. Each product card: Image (500x500px with soft shadow), product name (28px Newsreader), price (20px Inter Light), "Add to Cart" button (outline button, primary color). Hover: Image scales 1.03x, button fills with primary color. Cards fade-in and rise on scroll (translateY: 40px to 0) with 120ms stagger.

TESTIMONIAL SECTION: Minimalist layout. Single centered testimonial at a time (fade transition every 7 seconds). Large quote text (32px Newsreader Italic, primary color), customer name (18px Inter Regular), location (14px Inter Light, muted). Background: Subtle organic shapes (blob SVGs) in secondary color at 15% opacity, animated slow float.

SUSTAINABILITY SECTION: Split-screen layout. Left: Image of ingredients being harvested (720x900px tall). Right: Text content (headline "Our Commitment" + 3 value points with leaf icons). Parallax: image scrolls at 0.6x, text at 1x. Value points fade in sequentially on scroll (200ms delay between each).

FOOTER: Dark background (primary color). Four columns: Product (Features, Pricing, Demo), Company (About, Careers, Blog), Resources (Docs, API, Support), Legal (Privacy, Terms). Social icons with accent color on hover. Newsletter signup: inline input with accent button, glow effect on focus.

PARALLAX BEHAVIOR:

- Layer speeds: background 0.2x (slow), content 1x (normal), foreground 1.4x (fast)
- Trigger points: hero immediate, features 15%, pricing 45%, CTA 70%, footer 90%
- Animation style: Sharp with cubic-bezier(0.4, 0, 0.6, 1), 0.4s duration (snappier than usual), 80ms stagger

RESPONSIVE DESIGN:

- Mobile: Single column, stack pricing cards vertically, reduce headline sizes by 40%
- Tablet: Two-column for footer, maintain alternating features
- Desktop: Full layout with maximum 1440px content width (centered)
- Touch: Swipe for pricing comparison on mobile

TECHNICAL REQUIREMENTS:

- Smooth scroll with reduced motion option for accessibility
- Preload hero WebP for instant load
- Use WebGL for particle effects if supported (fallback to CSS)
- Dark mode optimized (already dark, but ensure readability)
- SEO: Technical schema markup, fast initial paint (<1.5s)

ASSETS TO INTEGRATE:

- Hero animation: neural-network-animation.webp
- Feature screenshots: feature-automation.webp, feature-analytics.webp, feature-integrations.webp
- Particle overlay: particles-floating.webp
- Glow effects: accent-glow.png (overlay blend mode)

```

### Example 3: Wellness Brand (Serene & Organic)
```

Build a modern single-page parallax website for Pure Essence, a natural skincare brand with serene and organic aesthetic.

DESIGN SYSTEM:

- Primary color: `#8B9D83` (sage green)
- Secondary color: `#F5F1E8` (warm cream)
- Accent color: `#D4A574` (golden tan)
- Neutral: `#4A4A4A` (warm gray text)
- Background: `#FDFCFA` (off-white)
- Typography: 'Newsreader' weight 400 for headings (serif, elegant), 'Inter' weight 300 for body with 1.8 line-height (airy)
- Spacing: 8pt grid system with spacious density (1.5x normal padding)