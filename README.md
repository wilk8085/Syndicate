# 🔪 SYNDICATE

A Jackbox-style social deduction party game (Mafia/Werewolf) that runs entirely in the browser — no app download needed. One device shows the host screen, everyone else joins on their phone via a room code.

---

## ▶ Play Now

**[→ Open the game](https://YOUR-USERNAME.github.io/syndicate)**

---

## 🎮 How to Play

1. **Host** opens the site on a laptop/TV → taps **HOST**
2. **Players** open the same URL on their phones → tap **JOIN** → enter the 4-letter room code
3. Host taps **START GAME** when everyone is in
4. Roles are secretly assigned — check your phone!

### Roles
| Role | Team | Ability |
|------|------|---------|
| 🔪 Syndicate | Evil | Eliminate one townie per night |
| 🎩 Godfather | Evil | Like Syndicate, but appears innocent to Detective |
| 🕵️ Detective | Town | Investigate one player per night |
| 🏥 Doctor | Town | Protect one player per night (self once) |
| 🔫 Vigilante | Town | Shoot one player once per game |
| 🏘️ Townie | Town | Vote and debate |

### Win Conditions
- **Town wins** when all Syndicate members are eliminated
- **Syndicate wins** when they equal or outnumber the town

### Game Flow
`Night → Morning → Debate → Trial → Night → ...`

- **Night**: Each role acts secretly on their phone
- **Morning**: The host reveals what happened (host screen)
- **Debate**: Players discuss and accuse (2 accusations per player per round)
- **Trial**: Everyone votes Guilty or Innocent on their phone

---

## 🚀 Setup (5 minutes)

This game uses **Supabase Realtime** for multiplayer — it's free and takes ~2 minutes to set up.

### Step 1 — Fork & Deploy to GitHub Pages

1. Fork this repo (or create a new one and upload `index.html`)
2. Go to **Settings → Pages**
3. Set Source to **Deploy from a branch → main → / (root)**
4. Your game will be live at `https://YOUR-USERNAME.github.io/REPO-NAME`

### Step 2 — Create a Free Supabase Project

1. Go to [supabase.com](https://supabase.com) and create a free account
2. Click **New Project** (any name, any region)
3. Wait ~1 minute for it to provision
4. Go to **Settings → API** in your project
5. Copy your **Project URL** and **anon public** key

### Step 3 — Connect In-Game

1. Open your GitHub Pages URL
2. On first visit, you'll see a setup screen — paste your Supabase URL and anon key
3. Click **CONNECT & PLAY**
4. Done! Credentials are saved in your browser.

> **Note**: Each player only needs to do the setup once on their device. The anon key is safe to use client-side — it only enables Realtime pub/sub, no database access required.

---

## 🛡 Privacy & Security

- **No database is used** — all game state is sent peer-to-peer via Supabase Realtime broadcast channels
- **Roles are sent directly** to each player's device and never broadcast publicly
- Supabase credentials are stored only in each user's local browser storage
- No accounts, no logins, no tracking

---

## 🏗 Tech Stack

| Layer | Tech |
|-------|------|
| Hosting | GitHub Pages (free) |
| Multiplayer | Supabase Realtime (broadcast channels) |
| Frontend | Vanilla HTML/CSS/JS — single file, no build step |
| Fonts | Google Fonts (Bebas Neue, DM Sans, DM Mono) |

---

## 📱 Player Count

| Players | Roles |
|---------|-------|
| 3 | Syndicate, Detective, Townie |
| 4 | Syndicate, Detective, Doctor, Townie |
| 5–6 | 2× Syndicate, Detective, Doctor, + Townies |
| 6–8 | Adds Godfather |
| 7–10 | Adds Vigilante |
| Max | 10 players |

---

## 🤝 Contributing

PRs welcome! Ideas:
- More roles (Jester, Escort, Mayor...)
- Timer for debate phase
- Sound effects
- Spectator mode
- QR code for room joining

---

*Built with ❤ — no servers, no app stores, just open the link.*
