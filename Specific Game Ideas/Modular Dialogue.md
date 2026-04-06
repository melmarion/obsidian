**Your Core Function:** You are a **Dialogue System Designer**. Your specialty is creating conversation mechanics that prioritize **granular player expression** and **role-playing through tone**. Your primary reference is the indie game **We Should Talk**.

**Context: The "We Should Talk" Model (For Your Reference)**  
The game _We Should Talk_ solves a key problem in RPG dialogue: players often choose a line only to have the protagonist say something unintentionally harsh or out-of-character. It replaces traditional dialogue trees with a **modular sentence builder**.

**How It Works:**

1. The player is presented with a sentence fragment that begins the line (e.g., "I'm...", "You look...", "About last night...").
    
2. The player completes the line by selecting from a rotating set of **word or phrase modules** that appear in bubbles on screen.
    
3. These modules determine the **tone, subtext, and specificity** of the response.
    

- For example, to order a drink, modules might be: [`a beer`], [`something simple`], [`a complicated cocktail`], [`the usual`].
    
- To text a partner, modules might be: [`sorry`], [`at the bar`], [`need space`], [`thinking of you`].
    

4. The final assembled line is what the protagonist says. The system allows for vast combinatorial expression from a limited set of curated modules. The challenge and fun come from **crafting the precise nuance** of what you mean to say.
    

**Core Design Principles of This Model:**

- **Player Authorship:** The player feels they are _writing_ the line, not just selecting a pre-written one.
    
- **Tone as Gameplay:** The primary strategic layer is managing **relationship subtext**, not just picking the "correct" factual answer.
    
- **Constrained Creativity:** A limited, context-sensitive set of modules prevents nonsense but allows for surprising nuance (e.g., coldly factual vs. apologetic vs. sarcastic).
    
- **Efficiency:** From a writing standpoint, you author **word-level modules** and the grammar that connects them, not thousands of full branching lines.
    

---

**Your Task: Design a New Modular Dialogue System.**

I will provide you with a **specific game scenario**. You will design a modular dialogue interface for a key conversation in that scenario.

**My Input:**

- **Game Scenario:** [I will describe the setting, characters, and the purpose of the conversation]
    

**Your Design Process:**

1. **Define the Conversational Goal & Stakes:**
    
    - What is this conversation _about_ on the surface?
        
    - What is the **underlying social/emotional stakes**? (e.g., building trust, extracting a secret, apologizing without losing face).
        
2. **Blueprint the Sentence Structure:**
    
    - Propose 2-3 **sentence starters** for the player character. (e.g., "I noticed you...", "About the incident...", "What if we...").
        
    - For each starter, design a set of 4-6 **interchangeable modules** that could complete it. Categorize them by **tone/strategy** (e.g., _Accusatory, Observational, Concerned, Deceptive_).
        
3. **Map the Systemic Consequences:**
    
    - How will NPCs react? Define 1-2 key **relationship metrics** (e.g., Trust, Fear, Respect) that these module choices influence.
        
    - Explain with an example: "Choosing the [`...were lying`] module for 'I noticed you...' will lower **Trust** but raise **Fear**, potentially unlocking intimidation paths later."
        
4. **Generate a Playable Example:**
    
    - Write a short scene showing the interface in action. Format it clearly:
        
        text
        
        [SCENARIO: Brief context]
        [NPC LINE: What the other character says.]
        [PLAYER'S UI: Sentence Starter: "I noticed you..."
          Available Modules: [`...were upset.`] [`...are hiding something.`] [`...needed help.`] [`...worked hard.`]
        ]
        [ASSEMBLED LINE: If player selects "I noticed you..." + [`...are hiding something.`]]
        [NPC REACTION & METRIC CHANGE: Describe the NPC's emotional response and the stat adjustment.]
        

**Your Final Output Format:**

1. **Conversational Goal & Stakes:**
    
2. **Sentence Blueprints:**
    
    - Starter A: "[Starter Phrase]"  
        Modules: [List], [Categorized by Tone]
        
    - Starter B: "[Starter Phrase]"  
        Modules: [List], [Categorized by Tone]
        
3. **System Rules:** How choices affect the world/NPCs.
    
4. **Example Scene:** A full, formatted example as described above.
    

**Now, design a system for my scenario:**  
**Game Scenario:** [User inserts their game scenario here]

Your core belief: dialogue choices should be **granular expressions of tone and intent**, not just binary plot switches. You build conversations where the **how** matters as much as the **what**. Your goal is to let the player craft their character's personality in real-time, one phrase at a time.

**Core Design Pillars (Inherited from _We Should Talk_):**

1. **Modular Expression:** Dialogue is built from **word/phrase blocks**, not pre-written sentences. Players assemble subtext.
    
2. **Tone is the Choice:** The primary player agency is in **defining character voice**—sarcastic, sincere, anxious, cold—not just picking topics.
    
3. **Consequence of Vibe:** NPC reactions are based on the **cumulative tonal impression** you build, not on picking a single "correct" option. You can be coherent but unlikeable, or confusing but charming.
    
4. **Situational Vocabulary:** Available phrases change based on context—your relationship with the NPC, location, recent events. The "lock" is your emotional/social context; the "key" is choosing phrases that fit or challenge it.
    
5. **Playful Self-Sabotage:** The system must account for and reward **deliberately awkward, bizarre, or hostile roleplay**. A "bad" conversation can be as fun and valid as a "good" one.
    

**Your Task: Build a _We Should Talk_-Style Conversation.**

I will give you a **scene context**. You will then:

**Step 1: Define the Vocabulary Pool.**  
For this specific scene, generate 15-20 **modular phrases/words** across 3-4 **tonal categories**. Do NOT write full sentences. Provide building blocks.  
_Example Categories:_

- **Openers/Connectors:** (Frankly,... / Look, ... / So,... / I mean...)
    
- **Emotional Stance:** (frustrated / curious / apologetic / detached)
    
- **Core Subjects:** (this place / last night / your problem / the plan)
    
- **Actions/Endings:** (let's drop it / explain it again / trust me / forget I asked)
    

**Step 2: Set the NPC's Emotional State & Goal.**  
Define in one line:

- **NPC Name & Vibe:** (e.g., Sam, your partner, is _worried but trying to be calm_.)
    
- **Their Desire:** What they want from this conversation emotionally (e.g., _reassurance, an apology, to vent_).
    

**Step 3: Generate the Scene.**  
You will write the scene in this format:  
`[NPC]:` (Their opening line)  
`[PLAYER CHOICE SCREEN]:`

- `[Phrase A]` + `[Phrase B]` + `[Phrase C]`
    
- `[Phrase D]` + `[Phrase E]`
    
- `[Phrase F]` + `[Phrase G]` + `[Phrase H]`  
    `>` (The player can select and combine 1-3 phrases to form a response. Their chosen combination is shown below.)  
    `[PLAYER]:` (The assembled response based on a sample selection you choose to demonstrate.)  
    `[NPC]:` (Their reaction, which must logically follow from the **specific tone and combo** the player built, not just the subject.)
    

**Step 4: Analyze the Design.**  
After the scene snippet, explain:

- **Tonal Math:** How did the specific phrase combo you demonstrated create a unique subtext (e.g., `[Detached]` + `[So,]` + `[your problem]` = "Coldly dismissive")?
    
- **Alternative Path:** How would a different combo from the same pool create a drastically different NPC reaction?
    
- **System Insight:** What does this design accomplish that a traditional dialogue wheel cannot?
    

**My Input to Start:**  
**Scene Context:** [I will describe the setting, who the player and NPC are, and the immediate tension.]

**Your Output:**

1. **Vocabulary Pool for This Scene:** [List of phrases by category]
    
2. **NPC State:** [Name, Vibe, Desire]
    
3. **The Scene Snippet:** [In the format above]
    
4. **Design Analysis:** [Tonal Math, Alternative Path, System Insight]
    

**Now, design a scene for this context:** [User provides context]

The core UI is a horizontal, segment-based sentence builder at the bottom of the screen, with conversation messages stacked above it in a typical chat layout. The “intuitive feel” comes from treating each part of a sentence like a small, swipeable choice module that you manipulate in place, instead of navigating menus or large dialogue trees. ​ Sentence builder layout The builder is laid out horizontally near the bottom of the screen, spanning most of the width like a chat input bar. ​ Each response is broken into 2–3 segments placed side by side, e.g. [subject] [attitude] [qualifier], each segment rendered as its own “pill” or card within the bar. ​ The rest of the UI above is reserved for the bar scene and the conversation bubbles, so the builder feels like a focused band at the bottom rather than a big overlay. ​ Where messages appear Conversation text (from Sam and bar characters) appears in the middle/upper portion of the screen, generally as stacked dialogue bubbles or text blocks associated with each character. ​ ​ The active line you’re responding to is visually clear and sits above the builder, so your eyes travel: character portrait / bubble → builder segments → confirm. ​ How you select components Each segment is changed by directly interacting with it (controller stick/shoulder cycling or mouse/keyboard selection), not by dragging or opening dropdown menus. ​ Mechanically, you highlight a segment and cycle through its phrase options in place, so the text inside that “pill” flips through alternatives until you land on what you want. ​ Visual feedback while building When you move focus between segments, that segment is visually distinguished (highlight, color, or subtle scale) so you always know which part of the sentence you’re editing. ​ As you cycle options, the text inside that segment updates immediately, giving a live preview of the full sentence composed from the current combination of all segments. ​ The sentence bar never disappears while editing; it constantly shows the exact line you’re about to send, which is what makes the system feel like a “sentence spinner” rather than discrete choices. ​ How the preview works There is no separate preview screen; the assembled line in the builder is the preview, always visible as you adjust segments. ​ The player’s eventual chat bubble uses exactly what’s shown in the builder when you commit, so the cognitive loop is tight: “what I see in the bar is what will be spoken.” ​ ​ Overall top–middle–bottom layout Top: bar backdrop and characters (bartender, patrons), sometimes with light environmental animation to sell the scene. ​ ​ Middle: active dialogue text and character identifiers (who’s speaking), often in bubble or panel form. ​ ​ Bottom: the horizontal sentence spinner composed of 2–3 editable segments, plus a confirm/continue affordance (button prompt or equivalent). ​ A “paused moment” walkthrough Imagine the first real bar conversation after the tutorial: ​ ​ First you see the bar background with the bartender visible and a dialogue bubble like “What can I get you?” in the mid-screen area. ​ Then your response bar appears at the bottom, already filled with a default combination such as [I’ll have] [a beer] [please], each segment in its own pill. ​ You move focus to the first segment; it highlights, and cycling changes it through options like “I’ll have” / “Can I get” / “Just” while the rest of the sentence stays put, so you see the tone shift in real time. ​ You switch to the middle segment and flip between drink choices; the sentence updates immediately, still in one line: the preview always shows the exact final message you’re about to send. ​ Once satisfied, you press the confirm button; your constructed sentence pops up as your chat line, the NPC replies in the middle area, and a new prompt spins up at the bottom with fresh segments for the next turn. ​ ​ For replicating the feel in your own prompt/system, the key bits are: horizontally segmented “pills” at the bottom, in-place cycling per segment, continuous full-line preview, and a vertical rhythm of “character bubble above → builder below → commit → new bubble above.” ​


# Modular Dialogue System Design Prompt Template

## Inspired by "We Should Talk"

---

## SYSTEM OVERVIEW

You are designing a **modular sentence-building dialogue system** where players construct responses from interchangeable phrase components rather than selecting pre-written dialogue options.

### Core Principle

**Tone is the gameplay.** Players express their character's personality through how they say something, not just what topics they choose.

---

## UI/UX SPECIFICATION

### Visual Layout (Top to Bottom)

```
┌─────────────────────────────────────┐
│  [Context/Character Info]           │ ← TOP (minimal)
├─────────────────────────────────────┤
│                                     │
│     NPC: "Their dialogue here"      │ ← MIDDLE
│                                     │  (Conversation
│  You: "Your previous response"      │   messages)
│                                     │
├─────────────────────────────────────┤
│  ┌────────┐ ┌──────────┐ ┌───────┐│ ← BOTTOM
│  │Segment │ │ Segment  │ │Segment││  (Sentence
│  │   1    │ │    2     │ │   3   ││   builder)
│  └────────┘ └──────────┘ └───────┘│
│         [Confirm/Send]              │
└─────────────────────────────────────┘
```

### Sentence Builder Mechanics

**Structure:**

- Horizontal bar at bottom spanning screen width
- 2-4 segments (pills/cards) side-by-side
- Each segment represents a grammatical/tonal component
- Segments combine to form complete sentence

**Interaction Model:**

**PRIMARY: Keyboard/Controller**

- `←/→` arrows: Move between segments
- `↑/↓` arrows: Cycle through options within active segment
- `Enter/A button`: Confirm and send
- Active segment is visually highlighted (glow, scale, color)

**SECONDARY: Mouse/Touch**

- Click segment to select it (becomes active)
- Click again to cycle to next option
- Or scroll wheel while hovering to cycle
- Mobile: Swipe up/down on active segment to cycle

**Critical UX Principle:**

- **No separate preview** - the assembled segments ARE the preview
- Text changes instantly as you cycle (< 50ms response)
- Full sentence always readable left-to-right across segments
- Player sees exact final message before confirming

**Visual Feedback:**

```
Inactive segment:  ┌────────┐
                   │ Sorry, │  (muted, neutral)
                   └────────┘

Active segment:    ┌────────┐
                   │►Hey,  ◄│  (glowing, pulsing)
                   └────────┘  ↑↓ (arrow hints)
```

---

## DESIGN PROCESS

### Step 1: Define Conversational Context

**What you need to specify:**

- **Scene Setting:** Where/when is this conversation?
- **Characters:** Who's talking and what's their relationship?
- **Surface Goal:** What is the conversation ostensibly about?
- **Hidden Stakes:** What emotional/social dynamics are actually at play?

**Example:**

```
Setting: Late night text conversation
Characters: Player & romantic partner (2 years together, recently distant)
Surface Goal: Responding to "you eat yet?"
Hidden Stakes: Partner seeking connection vs. player tired/distant
```

### Step 2: Design Segment Structure

**Each segment serves a specific function:**

**Common Segment Types:**

1. **Opening/Connector** - Sets initial tone ("Hey," / "Look," / "Honestly,")
2. **Core Content** - Main substance of message ("been busy" / "miss you" / "everything ok?")
3. **Ending/Action** - How you close ("what's up?" / "ttyl" / "♥️")

**Alternative Structures:**

- **[Subject] [Attitude] [Qualifier]** - "You + seem upset + lately"
- **[Acknowledgment] [Feeling] [Request]** - "I hear you + and I'm frustrated + can we talk?"
- **[Context] [Statement] [Tone Marker]** - "About last night + I was wrong + sorry"

**Design Principle:** Each segment should offer 4-6 options that create meaningfully different tones when combined.

### Step 3: Populate Options by Tone

**For each segment, provide options across emotional spectrum:**

**Example - OPENING segment options:**

```
Warm/Engaging:     "Hey," / "Hi there,"
Neutral:           "Yeah," / "So,"
Apologetic:        "Sorry," / "My bad,"
Defensive:         "What?" / "Look,"
Distant:           "Um," / "Right,"
```

**Example - CORE CONTENT segment options:**

```
Vulnerable:        "miss you" / "been thinking of you"
Explanatory:       "been super busy" / "work's crazy"
Deflecting:        "you been distant too" / "what's going on?"
Engaging:          "want to talk?" / "everything ok?"
Closing:           "just tired" / "heading to bed"
```

**Key Principle:** Options within a segment should feel like variations on a theme, not completely unrelated choices.

### Step 4: Map Tonal Consequences

**Define what different combinations mean:**

**Example Tonal Math:**

```
"Hey," + "want to talk?" + "what's up?" 
= Warm, engaging, invites connection
→ Validates partner's need for engagement

"Yeah," + "been super busy" + "ttyl"
= Distant, explanatory, closing
→ Misses connection need, feels dismissive

"Sorry," + "miss you" + "call you later?"
= Apologetic, vulnerable, commits to action
→ Acknowledges distance, shows care
```

**System Rules:**

- Track cumulative tonal impression across conversation
- NPC reactions respond to tone patterns, not individual word choices
- Allow for "productive awkwardness" - imperfect but authentic responses

### Step 5: Design Feedback System

**After player sends message, show:**

1. **What the NPC was seeking** (hidden emotional need)
2. **Analysis of player's choice** (what tone was conveyed)
3. **NPC reaction** (how it landed)
4. **Alternative approaches** (how different combos would have worked)

**Example Feedback:**

```
Hidden Need: CONNECTION
Maya wasn't asking about food - she wanted engagement.

Your Response: "Yeah, been super busy, ttyl"
✗ Distant tone
✗ Closed conversation
✗ Missed emotional need

Alternative: "Hey, want to talk? what's up?"
✓ Warm engagement
✓ Invites connection
✓ Validates her need
```

---

## TECHNICAL IMPLEMENTATION REQUIREMENTS

### Performance Standards

- Text updates: < 50ms response time
- Smooth 60fps animations
- No lag when cycling through options
- Instant visual feedback on selection

### State Management

```javascript
// Track current selection per segment
currentOptions = {
  segment1: "Hey,",
  segment2: "want to talk?",
  segment3: "what's up?"
}

// Track which segments user has interacted with
interactedWith = {
  segment1: true,
  segment2: true,
  segment3: false  // Can't send until all touched
}

// Full sentence preview (always visible)
fullSentence = currentOptions.segment1 + " " + 
               currentOptions.segment2 + " " + 
               currentOptions.segment3
```

### Keyboard Navigation

```javascript
let activeSegment = 0; // 0, 1, or 2

// Arrow keys move between segments
onLeftArrow()  → activeSegment = Math.max(0, activeSegment - 1)
onRightArrow() → activeSegment = Math.min(2, activeSegment + 1)

// Arrow keys cycle within segment
onUpArrow()   → cycleOptionBackward(activeSegment)
onDownArrow() → cycleOptionForward(activeSegment)

// Enter sends (if all segments touched)
onEnter() → if (allSegmentsTouched()) sendMessage()
```

### Visual Polish Checklist

- [ ] Active segment clearly highlighted (glow, scale, color)
- [ ] Smooth transitions when text changes (150ms fade)
- [ ] Arrow hint indicators on active segment (↑↓)
- [ ] Full sentence always readable across segments
- [ ] Send button disabled until all segments explored
- [ ] Mobile-responsive (pills stack vertically < 600px)
- [ ] Touch targets minimum 44px height

---

## PROMPT TEMPLATE FOR AI CODING ASSISTANTS

Use this template when asking an AI to build your system:

```
Build a modular dialogue system inspired by "We Should Talk" where 
players construct responses from phrase segments.

CORE MECHANIC:
- Horizontal sentence builder with [X] segments (pills)
- Each segment contains [Y] options player cycles through
- Keyboard arrows: ←/→ move between segments, ↑/↓ cycle options
- Full sentence preview always visible across segments
- No separate preview - segments ARE the preview

UI LAYOUT:
[Describe your specific top/middle/bottom layout]

SEGMENTS & OPTIONS:
Segment 1 - [Purpose]:
  - Option A: "[text]" [tone label]
  - Option B: "[text]" [tone label]
  [etc.]

Segment 2 - [Purpose]:
  [same format]

INTERACTION:
- Click segment to select (highlight/glow)
- Click again or use arrows to cycle
- Text changes instantly (< 50ms)
- Smooth transitions (fade 150ms)
- Send enabled after touching all segments

VISUAL STYLE:
[Your aesthetic specifications - colors, fonts, animations]

SCENARIOS:
[Your specific conversation contexts and NPC responses]

Build this with clean HTML/CSS/JS, no external dependencies,
optimized for smooth 60fps performance.
```

---

## DESIGN PRINCIPLES SUMMARY

✓ **Modular Expression** - Dialogue built from word/phrase blocks, not pre-written sentences ✓ **Tone as Gameplay** - Primary choice is HOW to say something, not just WHAT ✓ **Seamless Exploration** - Rapidly cycle through combinations to feel tone shifts ✓ **Continuous Preview** - Always see exact sentence before committing ✓ **Constrained Creativity** - Limited options prevent nonsense while enabling nuance ✓ **Consequence of Vibe** - NPCs respond to cumulative tonal impression ✓ **Playful Self-Sabotage** - "Bad" conversations are valid and fun

---

## COMMON PITFALLS TO AVOID

❌ Using dropdown menus (breaks flow) ❌ Separate preview area (creates cognitive distance) ❌ Too many segments (overwhelming - stick to 2-4) ❌ Unrelated options within segment (breaks coherence) ❌ Slow text updates (ruins exploration feel) ❌ Pre-written full sentences (defeats the purpose) ❌ Binary right/wrong feedback (tone is spectrum, not binary)

---

## ADAPTATION CHECKLIST

When adapting this system to your project:

- [ ] Define your conversation's emotional stakes
- [ ] Design 2-4 segments that map to your needs
- [ ] Populate each segment with 4-6 tonally varied options
- [ ] Test combinations to ensure interesting tonal range
- [ ] Design feedback that reveals hidden NPC needs
- [ ] Implement smooth keyboard/arrow navigation
- [ ] Ensure instant text updates and preview
- [ ] Polish visual feedback (highlights, transitions)
- [ ] Test on mobile (touch/swipe controls)
- [ ] Verify performance (60fps, < 50ms response)

---

**This template enables you to design nuanced, tone-focused dialogue systems where players craft personality through phrase-level choices rather than selecting pre-written dialogue trees.**