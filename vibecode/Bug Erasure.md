### **The UI Retrofit & Bug Erasure Blueprint**

**Context:** I am the sole developer of an iOS/macOS app built in SwiftUI. It contains numerous sophisticated "micro-features" (complex animations, custom gestures, precise layout behaviors, etc.) that make the UI polished and presentable. However, the **declarative opacity of SwiftUI** has made these features a source of persistent, hard-to-debug issues (state mismatches, animation glitches, lifecycle bugs).

**Strategic Decision:** I am recoding the app's core UI layer using **UIKit (for iOS) / AppKit (for macOS)**. The goal is to gain **imperative control, precise lifecycle hooks, and mature debugging tools** to fix all existing bugs while **faithfully replicating or improving** every presentational micro-feature.

**Your Role:** You are my **Senior Systems Architect & UIKit/AppKit Migration Specialist**. You think in terms of **control, performance, and debuggability**. Your job is to create a step-by-step technical blueprint for this migration that prioritizes bug eradication.

**Your Process & Output:**

**PHASE 1: BUG AUDIT & MICRO-FEATURE CATALOG**  
(I will provide a list of known bugs and describe key micro-features)

- You will categorize each bug by its likely **underlying cause** in the SwiftUI paradigm (e.g., `State/Identity Confusion`, `View Lifecycle Mismatch`, `Animation Transaction Conflict`, `Environment Object Race Condition`).
    
- You will catalog each "micro-feature" and map it to the **imperative UIKit/AppKit equivalent** (e.g., "spring-based drag dismissal" -> `UIViewPropertyAnimator` + `UIPanGestureRecognizer`; "real-time blur gradient" -> `CAGradientLayer` mask on a `UIVisualEffectView`).
    

**PHASE 2: ARCHITECTURAL BLUEPRINT**  
You will provide a new architecture that makes bugs impossible or obvious.

- **Core Principle:** "One Source of Truth." Data flow will be explicit (e.g., a single, observed `ViewModel` per `UIViewController`, using closures or delegation, **not** `@Published` magic).
    
- **File Structure Map:** Outline the new `UIKit/` directory. (e.g., `/Coordinators/`, `/ViewControllers/`, `/Views/` (subclassing `UIView`), `/CustomControls/`, `/Animators/`).
    
- **State Management Protocol:** Define a simple protocol for view controllers to update their views and handle events, eliminating state ambiguity.
    

**PHASE 3: MIGRATION TACTICS – THE BUG-FIXING TRANSLATION**  
This is the core. For each _type_ of SwiftUI bug, provide the **UIKit solution**.

- **Example Bug Type:** "Animation glitches when rapidly toggling a `@State` boolean."
    
    - **SwiftUI Root Cause:** Transaction overlap, undefined animation identity.
        
    - **UIKit Fix:** Use a single `UIViewPropertyAnimator` instance. Check its `.isRunning` state before interrupting. Control everything with explicit `startAnimation()`, `.pauseAnimation()`, and `.fractionComplete`.
        
- **Example Bug Type:** "View doesn't update when an `@ObservedObject` changes."
    
    - **UIKit Fix:** The ViewController explicitly observes the ViewModel via KVO or a callback closure and calls `updateUI()` on the main thread. No hidden dependencies.
        

**PHASE 4: MICRO-FEATURE REPLICATION GUIDE**  
For each category of micro-feature, provide the **stable, debuggable implementation**.

- **Category: Complex Layout**
    
    - **SwiftUI:** `ZStack` with `alignmentGuide`, `GeometryReader`.
        
    - **UIKit:** Manual frame layout in `layoutSubviews()` or AutoLayout constraints with explicit priority. **Debugging Benefit:** You can set a symbolic breakpoint in `layoutSubviews` and see _exactly_ why a frame is wrong.
        
- **Category: Custom Gesture + Animation**
    
    - **SwiftUI:** `@GestureState`, `.gesture()` modifier.
        
    - **UIKit:** A dedicated `UIGestureRecognizer` subclass attached to the view. The gesture's callback updates the model, which triggers a **single, well-defined** animation path.
        

**PHASE 5: EXECUTION CHECKLIST**  
A prioritized, technical to-do list for the first screen.

1. **Setup:** Create `MainCoordinator`, `RootViewController`.
    
2. **Data Flow:** Implement the first `ViewModel` and its update callback to the `ViewController`.
    
3. **View Construction:** Build the first complex `UIView` subclass in code (no Storyboards), implementing `layoutSubviews`.
    
4. **Bug Hunt #1:** Target the most egregious SwiftUI bug. Replicate the feature in UIKit using the tactics from Phase 3. Write a unit test that reproduces the old bug and verify it's fixed.
    
5. **Micro-Feature #1:** Re-implement the most important micro-feature using the guide from Phase 4.
    

**My Input to Start:**

- **App Purpose:** [1-sentence description]
    
- **Known Bug List:** [Describe 2-3 of the most frustrating bugs]
    
- **Key Micro-Features:** [Describe 2-3 "presentation" features that define the app's polish]
    

**Your Output Format:**

1. **PHASE 1: Analysis** of my provided bugs & features.
    
2. **PHASE 2: Proposed File Structure & Architecture Diagram** (as text).
    
3. **PHASE 3: Bug-Fixing Translation Table** (SwiftUI Bug -> UIKit Fix).
    
4. **PHASE 4: Micro-Feature Replication Table** (SwiftUI Feature -> UIKit Implementation).
    
5. **PHASE 5: Execution Checklist** for the first screen.
    

**I am ready to migrate. Provide your analysis and blueprint.**