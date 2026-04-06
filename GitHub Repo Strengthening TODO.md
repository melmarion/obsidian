# GitHub Repo Strengthening TODO

## Core Rule For Next Codex Session

Do not drift into random feature work.

For each repo, Codex must first make the repo **stronger** by applying the relevant audit lenses from these notes:

- [[vibecode/Code Quality Audit Master Prompt]]
- [[vibecode/Hostile Code Audit]]
- [[vibecode/Vibe-Code Security Architect]]
- [[vibecode/App Brand Identity Audit Prompt]]
- [[UX/Prompts/Senior Interaction Designer specializing in micro-interaction audits]]
- [[Ai Prompt Context/1. How to format content]]
- [[Ai Prompt Context/2. Presentation Style Guide]]

## Session Operating Sequence

For each repo, Codex should do this exact sequence:

1. Read the repo before proposing changes.
2. Classify the repo:
   - native app
   - frontend product
   - backend/service
   - research/prompt system
   - prototype / artifact repo
3. Apply the right strengthening lens:
   - all repos: `Code Quality Audit Master Prompt`
   - anything with auth, API, payments, user data, or external services: `Hostile Code Audit` + `Vibe-Code Security Architect`
   - apps with onboarding, interface friction, weak polish, or retention problems: `Senior Interaction Designer specializing in micro-interaction audits`
   - consumer-facing app repos with fuzzy identity: `App Brand Identity Audit Prompt`
4. Produce:
   - top risks
   - strongest leverage fixes
   - concrete code or repo changes
   - a tighter README / framing when needed
5. Prefer changes that raise:
   - reliability
   - debuggability
   - security
   - UX polish
   - product identity
6. Only after strengthening the repo should Codex do optional expansion work.

## Deliverable Standard Per Repo

Codex should leave each repo with some combination of:

- cleaner architecture
- better guardrails
- improved README or operator instructions
- stronger UX polish
- security hardening
- missing tests or validation
- a sharper product story if the app feels generic

## Repo Sweep Checklist

- [ ] `/Users/infiniteupside/Journal`
- [ ] `/Users/infiniteupside/LinkedinGen`
- [ ] `/Users/infiniteupside/Luna`
- [ ] `/Users/infiniteupside/Neural-Drift`
- [ ] `/Users/infiniteupside/Obluda`
- [ ] `/Users/infiniteupside/Persuasion-Max`
- [ ] `/Users/infiniteupside/Reality-Distortion`
- [ ] `/Users/infiniteupside/SSMDateTracker-iOS`
- [ ] `/Users/infiniteupside/SignFlow`
- [ ] `/Users/infiniteupside/SoloFinance`
- [ ] `/Users/infiniteupside/UX`
- [ ] `/Users/infiniteupside/WeighIt`
- [ ] `/Users/infiniteupside/build-repos`
- [ ] `/Users/infiniteupside/carnivore-tracker`
- [ ] `/Users/infiniteupside/charisma-training-game`
- [ ] `/Users/infiniteupside/cloud-gossip-v6`
- [ ] `/Users/infiniteupside/coastal-compass`
- [ ] `/Users/infiniteupside/date-pilot`
- [ ] `/Users/infiniteupside/dead-internet`
- [ ] `/Users/infiniteupside/erikson`
- [ ] `/Users/infiniteupside/field-protocol`
- [ ] `/Users/infiniteupside/figma-design-library`
- [ ] `/Users/infiniteupside/forecast-ios`
- [ ] `/Users/infiniteupside/jeju-island`
- [ ] `/Users/infiniteupside/jeju-island-life`
- [ ] `/Users/infiniteupside/kitsune-no-michi`
- [ ] `/Users/infiniteupside/late`
- [ ] `/Users/infiniteupside/lumina`
- [ ] `/Users/infiniteupside/mcp-rover`
- [ ] `/Users/infiniteupside/melmarion.github.io`
- [ ] `/Users/infiniteupside/paired`
- [ ] `/Users/infiniteupside/paws-and-presence`
- [ ] `/Users/infiniteupside/petsitting`
- [ ] `/Users/infiniteupside/read-the-room-ios`
- [ ] `/Users/infiniteupside/sign-language-app`
- [ ] `/Users/infiniteupside/sign-language-app-ref`
- [ ] `/Users/infiniteupside/slop-ops-mvp`
- [ ] `/Users/infiniteupside/social-pilot`
- [ ] `/Users/infiniteupside/somnium-ios`
- [ ] `/Users/infiniteupside/still-waters`
- [ ] `/Users/infiniteupside/stillness`
- [ ] `/Users/infiniteupside/sway-v5`
- [ ] `/Users/infiniteupside/visual-scene`

## First Repos To Hit

- [ ] `/Users/infiniteupside/read-the-room-ios`
- [ ] `/Users/infiniteupside/SignFlow`
- [ ] `/Users/infiniteupside/SoloFinance`
- [ ] `/Users/infiniteupside/Luna`
- [ ] `/Users/infiniteupside/date-pilot`
- [ ] `/Users/infiniteupside/social-pilot`
- [ ] `/Users/infiniteupside/Journal`

## Non-Negotiable Instruction To Codex

If a repo feels half-finished, generic, brittle, or "vibe-coded," do not just add more features.

First:

- tighten the structure
- harden the risky edges
- raise the visual and interaction quality
- sharpen the repo's identity and README
- remove the most embarrassing weak spots

Then continue.
