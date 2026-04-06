Perfect. You want to build a **creative tool, not a game**. The goal is to operationalize our high-level strategic dialogue into a frictionless interface that does the cognitive heavy lifting for the user. It's a **Prompt Design Lab** built on psychological and rhetorical principles.

Here is the prompt to conceptualize and spec this tool.

---

### **Prompt: The Prompt Architect Studio – Spec Designer**

**Your Role:** You are a **Product Strategist for AI Creativity Tools**. You are designing "Prompt Architect Studio," a web app that transforms the abstract art of prompt engineering into a structured, creative, and intuitive process. The philosophy is **"Make the invisible process visible and manipulable."** It’s not a game with points; it's a workshop with levers, templates, and live previews.

**Core User Problem:** People have a goal but lack the **cognitive scaffolding** to bridge the gap between "I want X" and writing the precise, layered prompt that gets X from an AI. They don't know the patterns, the strategic frames, or how to combine them.

**The Solution:** A visual, modular interface where users **build prompts by intention, not by trial and error.** The tool makes expert strategies tangible.

**Key Interface & Functionality Modules to Conceptualize:**

1.  **The "Intention Selector" (The North Star):**
    *   User starts by declaring their **primary goal** via buttons/toggles: `[Persuade]` / `[Explain]` / `[Create]` / `[Analyze]` / `[Role-play]` / `[Refine]`.
    *   This selection loads a tailored set of **Strategy Modules**.

2.  **Strategy Modules (The Tactical Palette):**
    *   Each module is a collapsible pane containing **adjustable levers** for a specific psychological or rhetorical principle.
    *   **Example Module: "Authority & Frame Control"**
        *   *Lever 1 - Role Priming:* Dropdown: `[Cynical Expert]` / `[Empathic Coach]` / `[Tactical Analyst]` / `[Blank Slate]`.
        *   *Lever 2 - Constraint Injection:* Text input: "Given that..." + `[___]`.
        *   *Lever 3 - Output Mandate:* Toggle: `[Must include a metaphor]` / `[Must use bullet points]` / `[Must avoid jargon]`.
    *   **Example Module: "Depth & Evasion Prevention"**
        *   *Lever - Anti-Genericity Guardrails:* Checklist: `[Forbid clichés like "leverage," "shatter"]` / `[Require a counter-argument]` / `[Mandate a real-world example]`.

3.  **The "Linguistic Pattern Injector" (Inspired by *We Should Talk* & Hypnosis):**
    *   A box with pre-written, high-impact **phrase blocks** the user can drag into their prompt structure.
    *   Sections: `Openers That Hook`, `Logical Connectors`, `Subtext & Frame Phrases`, `Closers That Direct Action`.
    *   *Example Phrase Block:* `"Act as if your primary goal is [USER INSERTS GOAL], but you are forbidden from stating it directly."`

4.  **The Live Preview Canvas:**
    *   A central, updating text field that assembles the user's choices from the modules and drag-and-drop phrases into a coherent, well-structured prompt **in real time**.
    *   It shows the "skeleton" being built, allowing for manual tweaking.

5.  **The "Example & Variation Engine":**
    *   Upon generating a prompt, the tool offers **"Apply This Structure To..."**: a dropdown of new topics. Clicking "Business Plan" regenerates the same strategic skeleton applied to that new topic, teaching transferability.

**Your Task: Spec a User Flow.**

I will provide a **user's raw, simple desire** (e.g., "I want to write a scary story," "I need to analyze a business competitor," "I want to learn about quantum physics in a simple way").

You will map out how the tool transforms that desire.

**Design Phase 1: Intention Mapping.**
*   Identify which **primary goal** from the Intention Selector the user would pick.
*   Select **2-3 relevant Strategy Modules** that would be auto-loaded.

**Design Phase 2: Lever Configuration.**
*   For each chosen module, propose **specific, likely settings** a user might choose for their goal.

**Design Phase 3: Pattern Injection.**
*   Suggest 1-2 **specific phrase blocks** from the Linguistic Pattern Injector they might use.

**Design Phase 4: Generate the Final Output.**
*   Assemble the configured levers and phrases into a **final, polished prompt** as it would appear in the Live Preview Canvas.
*   Then, use the Example Engine to show **one variation**—the same prompt structure applied to a completely different topic.

**My Input to Start:**
**User's Raw Desire:** `[I want to write a persuasive email to my boss asking for a raise.]`

**Your Output:**
1.  **Intention & Modules:**
    *   **Selected Goal:** `[Persuade]`
    *   **Loaded Modules:** `[Authority & Frame Control]`, `[Depth & Evasion Prevention]`, `[Tone & Persona Builder]`.
2.  **Configured Levers:**
    *   *Module 1 - Authority & Frame Control:*
        *   Role Priming: `[Tactical Analyst]`
        *   Constraint Injection: `"Given my last two performance reviews..."`
        *   Output Mandate: `[Must include bullet points]`
    *   *Module 2 - Depth & Evasion Prevention:*
        *   Guardrails: `[Require a real-world example]`, `[Forbid generic phrases like "hard worker"]`.
3.  **Injected Pattern:**
    *   Phrase Block Used: `"Structure the argument so the most compelling data point appears as an inevitable conclusion, not a demand."`
4.  **Final Generated Prompt:**
    ```markdown
    Act as a **Tactical Analyst** specializing in corporate negotiation. Your task is to draft a persuasive email. The core argument is to request a raise.

    **Constraints & Context:** The requester's last two performance reviews were positive. The email must be concise and evidence-based.

    **Strategic Mandates:**
    1. Structure the argument so the most compelling data point (e.g., a specific achieved metric) appears as an inevitable conclusion, not a demand.
    2. You are **forbidden** from using generic, valueless phrases like "hard worker" or "dedicated team player." Replace them with specific accomplishments.
    3. The email must include at least one clear, real-world example of a project that delivered measurable value.
    4. The final draft must use bullet points for clarity in the summary of key points.

    Output the full email draft.
    ```
5.  **Applied Variation (Using Same Structure):**
    *   **New Topic:** `[A persuasive email to a landlord requesting a lease renewal without a rent increase.]`
    *   *(You would show the regenerated prompt with the same modules/levers, but context swapped.)*

**Now, design the flow for this user desire.**