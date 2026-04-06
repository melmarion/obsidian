> Give me a single copy-paste block of commands for Windows: (1) cd's to my Desktop, (2) clones the repo, (3) cd's into the cloned folder, (4) checks out the working branch, (5) installs dependencies, and (6) starts the dev server on port 3000. Separate all commands with semicolons so I can paste it all at once. Use the repo URL and branch name from this conversation. Make sure there is no double && for PowerShell.

ctrl c:
git pull

npx vite --host 0.0.0.0 --port 3000


Here's what's actually wrong — it's not just colors or glow. The entire structure is built wrong for a consumer app:

**The core problem:** The app is organized around _features_ (Dashboard, Review, Compare, Decision) but users think about _people_ (their dating partners). Opening the app should show your partners, not a hero page or a tab bar.

**What kills it:**

1. **5 tabs is overwhelming** — most successful apps have 3 max
2. **Empty hero landing** — beautiful but useless. No one opens a tracker app to stare at a button
3. **Everything is the same visual weight** — nothing pops, nothing recedes
4. **The dark theme is oppressive** — `#0A0A0F` near-black creates eye strain with bright pink
5. **13 sliders at once** in the review form is intimidating
6. **No personality** — it feels like a developer tool, not something you'd show friends
