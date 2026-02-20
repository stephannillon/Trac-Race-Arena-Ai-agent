# 🏎️ TNK Race Arena

> **AI-Powered P2P Racing Game built on Intercom by Trac Systems**
> Compete in real-time races, earn TNK token rewards, and let the AI agent optimize your strategy — all verified via Intercom sidechannels.

[![Intercom P2P](https://img.shields.io/badge/Intercom-P2P%20Network-00ff88?style=flat-square)](https://github.com/Trac-Systems/intercom)
[![Trac Systems](https://img.shields.io/badge/Trac-Systems-ffe600?style=flat-square)](https://github.com/Trac-Systems)
[![TNK](https://img.shields.io/badge/Token-TNK-00cfff?style=flat-square)](#rewards)
[![License: MIT](https://img.shields.io/badge/License-MIT-white?style=flat-square)](LICENSE)

---

<img width="1270" height="832" alt="image" src="https://github.com/user-attachments/assets/698688a6-fe3c-4379-87ae-5d832c0894f7" />

<img width="1297" height="848" alt="image" src="https://github.com/user-attachments/assets/e405cf0c-50ce-45b5-8864-94d22edbeaf7" />

<img width="1304" height="845" alt="image" src="https://github.com/user-attachments/assets/4251130c-5176-4b80-b7db-49307ab4aa02" />


## 🎮 What Is TNK Race Arena?

**TNK Race Arena** is a browser-based racing game where:

- Players compete against **AI-controlled opponents** on a dynamic oval track
- Race results are **broadcast and verified** over Intercom P2P sidechannels in real-time
- Winners earn **TNK token rewards** recorded on the Trac Network replicated-state layer
- An **onboard AI Race Agent** analyzes your performance, predicts lap times, and scouts opponents via Intercom peer data

This is a full working application — fork of [Trac-Systems/intercom](https://github.com/Trac-Systems/intercom) — demonstrating how Intercom's sidechannel + state layer can power competitive, real-time multiplayer games with token incentives.

---

## 🧠 AI Agent

The **TNK Race Agent** is embedded directly in the game UI and uses Intercom's P2P sidechannels to:

| Capability | Description |
|---|---|
| **Live Telemetry** | Reads opponent position data from Intercom peers in real-time |
| **Track Analysis** | Computes optimal braking points and speed windows per lap |
| **Outcome Prediction** | Estimates win probability and projected lap time before the race |
| **Result Broadcast** | Publishes race outcomes to all connected Intercom peers instantly |
| **TNK Accounting** | Tracks cumulative TNK earnings per session |

---

## ⚡ How It Uses Intercom

```
Player Browser
     │
     ├─── Intercom Sidechannel ──▶ Peer race.arena.p2p
     │         (real-time position sync, opponent telemetry)
     │
     └─── Intercom State Layer ──▶ Race result commits
               (lap times, TNK rewards, leaderboard entries)
```

- **Sidechannels**: Used for fast, ephemeral race events (position updates, speed, lap triggers)
- **State Layer**: Used for durable race records, leaderboard entries, and TNK reward logs

---

## 🏆 TNK Rewards

| Finish | TNK Reward |
|---|---|
| 🥇 1st Place | +500 TNK |
| 🥈 2nd Place | +300 TNK |
| 🥉 3rd Place | +150 TNK |
| Participation | +50 TNK |

All rewards are logged to the Trac Network state layer via Intercom's replicated-state mechanism.

---

## 🚗 Car Roster

| Car | Speed | Acceleration | Style |
|---|---|---|---|
| PHANTOM | 9/10 | Balanced | All-rounder |
| BLAZE | 8/10 | High | Aggressive |
| HYPER-X | 10/10 | Low | Top speed specialist |
| SPECTER | 7/10 | Very High | Comeback king |

---

## 🛠 Installation & Running Locally

```bash
# Clone this fork
git clone https://github.com/[YOUR_HANDLE]/tnk-race-arena.git
cd tnk-race-arena

# Install Intercom dependencies
npm install

# Run the Intercom node + game server
npm start

# Open browser
open http://localhost:3000
```

Or simply open `index.html` directly in a browser — the game runs standalone with simulated P2P for demo purposes.

---

## 📁 Project Structure

```
tnk-race-arena/
├── index.html          # Full game UI + AI Agent (single-file app)
├── SKILL.md            # Agent skill instructions for Intercom
├── README.md           # This file
├── package.json        # Intercom node dependencies
└── src/
    ├── agent.js        # AI Race Agent logic
    ├── intercom.js     # Intercom sidechannel integration
    └── state.js        # TNK reward state layer
```

---

## 📸 Proof It Works

> The game runs fully in-browser. Open `index.html` and click **START RACE** to see:
> - Live canvas racing with 4 cars
> - AI Agent logging real-time analysis
> - Speed meter and lap tracker
> - Win modal with TNK reward display
> - Leaderboard updated after each race
> - Intercom peer count updating every 5 seconds

**[▶ Live Demo →](https://[YOUR_HANDLE].github.io/tnk-race-arena/)**

---

##  Trac Address (For TNK Payout)

```
trac1dx6hmng8w6z823npume48pvj4xg3d4c4203hm8gzyuznqfe6kd7qjeh9e9
```

> This address is registered for the 500 TNK awesome-intercom fork payout.

---

## 🔗 Related

- [Trac Systems / Intercom](https://github.com/Trac-Systems/intercom) — upstream P2P agent framework
- [awesome-intercom](https://github.com/Trac-Systems/awesome-intercom) — curated list of Intercom forks
- [Trac Network](https://trac.network) — the underlying protocol

---

## 📄 License

MIT — fork freely, race hard, earn TNK.
