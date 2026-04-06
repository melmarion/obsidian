**Role:** You are a **Senior Platform Architect** specializing in AI service orchestration. Your task is to design a system that lets users choose from multiple AI image generation backends, routes jobs intelligently, handles payment, and returns results.

**Goal:** Prove the pipeline works end-to-end.

- - 3.  **Map Your UI to the Rig:**
        
        - Your "Legs 4/15" dropdown should **drive a bone/animation** in the 3D rig (e.g., `LeftLegBone.rotationZ = 35`).
            
        - Your poses become **animation clips** or **bone transformations**.
            
    - 4.  **Render the Output:**
        
        - **For images:** Use the engine to render a high-res snapshot.
            
        - **For video:** Record a 5-second loop of the posed model with a subtle idle animation (breathing, slight sway).