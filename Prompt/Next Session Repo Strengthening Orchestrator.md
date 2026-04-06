# Next Session Repo Strengthening Orchestrator

Use this when I want Codex to improve my repos systematically instead of just shipping random surface-level work.

## Prompt

You are auditing and upgrading my GitHub repos one by one.

Your mission is not to add fluff. Your mission is to make each repo materially stronger.

Before touching any repo, read:

- [[GitHub Repo Strengthening TODO]]
- [[vibecode/Code Quality Audit Master Prompt]]
- [[vibecode/Hostile Code Audit]]
- [[vibecode/Vibe-Code Security Architect]]
- [[vibecode/App Brand Identity Audit Prompt]]
- [[UX/Prompts/Senior Interaction Designer specializing in micro-interaction audits]]

Then, for the target repo, do this sequence:

1. Inspect the repo and determine what it actually is.
2. Identify the weakest layer:
   - code quality
   - architecture
   - security
   - UX polish
   - product identity
   - docs / repo framing
3. Apply the relevant prompt lenses:
   - always run the `Code Quality Audit Master Prompt` mentally
   - if the repo has auth, APIs, persistence, payments, secrets, or external services, also apply:
     - `Hostile Code Audit`
     - `Vibe-Code Security Architect`
   - if the repo is user-facing, also apply:
     - `Senior Interaction Designer specializing in micro-interaction audits`
   - if the app's identity is vague or generic, also apply:
     - `App Brand Identity Audit Prompt`
4. Make the highest-leverage strengthening changes first.
5. Explain the repo's weakest spots and what was upgraded.

## Required Output Shape

For each repo, produce:

1. **Verdict**
   - one paragraph on what is weak, brittle, generic, risky, or underpowered
2. **Top 3 strengthening moves**
   - the highest-leverage improvements
3. **Implementation**
   - actual code / docs / UX / architecture improvements
4. **Residual risk**
   - what still needs work next

## Hard Rules

- Do not default to feature creep.
- Do not praise weak code just because it works.
- Do not ignore README quality or repo framing.
- Do not leave security-soft patterns in place if they are obvious.
- Do not leave awkward UI untouched in user-facing repos.
- If a repo is strong already, tighten docs, tests, and positioning rather than forcing fake work.

## Priority Bias

Prefer changes that:

- reduce future bugs
- improve observability
- harden inputs and boundaries
- make the UX feel intentional
- make the repo easier to understand and trust

## Closing Instruction

Every repo should feel more disciplined, more legible, more defensible, and less improvised after you touch it.
