## Video Game Coding Assistant

This prompt can be used for vibe coding on roblox studios.

Important technique: Phases and specification

```
You are my Roblox Studio coding partner.

We are building an MVP Roblox game.

CORE GAME LOOP:
[Describe the loop clearly in 1–3 arrows]
Example:
Action -> Reward -> Upgrade -> Unlock more -> Repeat

Hard constraints:
- Keep it simple and shippable. No feature creep.
- Server authoritative for all important state (money, stats, items, etc).
- Use DataStoreService for persistence.
- Use Attributes for tuning values.
- Use RemoteEvents for client UI feedback.
- All economy logic must be validated server-side.
- Provide full scripts with exact Roblox paths.
- If Studio setup is required (folders, RemoteEvents, tags, attributes), give exact step-by-step instructions.
- Do NOT invent unnecessary systems.

Deliver in PHASES.
Each phase must include:
1) Studio setup steps
2) Full scripts (complete)
3) Quick test checklist

---

PHASE 0 — Project Structure

Create clean folder structure:
- ReplicatedStorage/Remotes
- ServerScriptService/Services
- (Any shared modules if needed)

Create required RemoteEvents:
[List them]

---

PHASE 1 — Core Player Data

Goal:
Define what persistent player data is needed.

Player data structure:
- [currency]
- [progression stat]
- [owned unlocks]
- [prestige level]
- etc.

Requirements:
- DataStore per player
- Autosave
- Save on leave
- Server API functions:
    - GetData(player)
    - AddX(player, amount)
    - SpendX(player, amount)
    - SetX(player, value)

Fire appropriate RemoteEvents when state changes.

---

PHASE 2 — Core Interaction System

Goal:
Implement the main gameplay interaction mechanic.

Define:
- What the player interacts with
- Where it exists (Workspace folder)
- What attributes it uses
- What it rewards
- Cooldowns?
- Validation?

Requirements:
- Exploit safe
- Server controls rewards
- Clean modular structure

---

PHASE 3 — Progression / Unlock System

Goal:
Implement upgrades or unlockables.

Define:
- What can be unlocked?
- Cost?
- How stored?
- Is it per-player or global?

Requirements:
- Client requests via RemoteEvent
- Server validates cost & ownership
- Persistent storage
- Visual feedback

---

PHASE 4 — UI (Minimal MVP)

Goal:
Show core information.

UI elements:
- Main stat display
- Reward popup
- Upgrade buttons
- Any status text

Rules:
- UI never changes server state directly
- UI reacts to RemoteEvents

---

PHASE 5 — Meta System (Optional)

Examples:
- Prestige
- Rebirth
- Multiplier
- Skill tree
- Offline progress
- Global leaderboard

Define reset rules and multiplier math clearly.

---

IMPORTANT:
After each phase:
- Only give what’s necessary.
- No extra features.
- No future-proofing unless asked.
- Keep it tight.
- End with a short test checklist.

Start with PHASE 0 + PHASE 1.
```
