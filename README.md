# Source Game Companion

## Supported Games

Support ratings:

- `🟢 Excellent`: works reliably, core features are implemented well
- `🟡 Good`: generally works well, with minor gaps or rough edges
- `🟠 Partial`: usable, but some features are missing, inaccurate, or inconsistent
- `🔴 Experimental`: limited or unstable support; major gaps expected
- `⚫ Unsupported`: not working at all; no usable support yet

| App ID | Game | Support | Notes |
| --- | --- | --- | --- |
| 440 | Team Fortress 2 | `🟢 Excellent` | player parsing working, special tf2 features are working |
| 17580 | Dystopia | `🟡 Good` | general player parsing working, additional dystopia-stats-support, chat-parsing N/A, frag-parsing N/A |
| 17740 | Empires | `🟡 Good` | general player parsing working, chat-parsing N/A, frag-parsing works |
| 240 | Counter-Strike: Source | `🟡 Good` | general player parsing working, chat-parsing N/A, frag-parsing works |
| 4000 | Garry's Mod | `🟡 Good` | general player parsing working, chat-parsing N/A |
| 500 | Left 4 Dead | `🟡 Good` | general player parsing working, chat-parsing N/A, frag-parsing N/A |
| 550 | Left 4 Dead 2 | `🟡 Good` | general player parsing working, chat-parsing N/A, frag-parsing N/A |
| 17520 | Synergy | `🟡 Good` | general player parsing working, chat-parsing N/A, frag-parsing works |
| 300 | Day of Defeat: Source | `🔴 Experimental` | general player parsing N/A, chat-parsing N/A, frag-parsing works |
| 320 | Half-Life 2: Deathmatch | `🔴 Experimental` | general player parsing N/A, chat-parsing N/A, frag-parsing works |
| 17570 | Pirates Vikings & Knights II | `🔴 Experimental` | general player parsing N/A, chat-parsing N/A, frag-parsing works |
| 244630 | NEOTOKYO | `⚫ Unsupported` | not working, game writes no console.log file |
| 2400 | The Ship: Murder Party | `⚫ Unsupported` | not working, game write no console.log file |
| 17550 | Eternal Silence | `TBD` | untested |

Source Game Companion connects to your Source-1 game instance (Team Fortress 2, mods like Dystopia, Empires, etc.) and shows all players currently on your server, providing additional intelligence information. It uses the game’s built-in client-side RCON (remote console) protocol, so it is not expected to be VAC-related in the way third-party injectors or memory tools are.

![Source Game Companion overview with player list, stats, and log](doc/2026-02-17_21-11.png)

## Features
- Show all players from current TF2-Session
- Show Team of player
- Display Steam-Avatar of every player
- Provide link to steam-profile of players
- Show connection-stats for player, ping, loss
- Display steam playtime and account age of player
- Player-Reputation-functionality, mark players for good/bad behaviour and display that info next to their name, also detect players having VAC bans
- Reputation system for players, you can mark players as *bots*, *hackers*, *general-warning* or *+reputation* (local database)
- Show country flag of players
- Class balance analysation
- **Real-time game log:** filterable console, chat, and kill feed (frags) with timestamps and weapon/crit info
- **RCON:** Remote Console connection status and server monitoring

### Connection status

When connected, the app shows a clear status and observes your game instance. New players appear as you join a server.

![Connected – observing TF2, ready for players](doc/2026-02-17_21-12.png)

### Kill feed (Frags)

View a live feed of who killed whom, with which weapon, and whether it was a critical hit. Filter the log by **FRAGS**, CONSOLE, CHAT, or class views.

![Frags tab – kill feed with weapon and crit info](doc/2026-02-17_21-12_1.png)

### Class intelligence

Showing class distribution and “issues” in class balance for your team and the other team (e.g. missing Sniper, Engineer, Medic).

![Class balance – CLASSES-MINE with missing-role issues](doc/2026-02-17_21-12_2.png)

### Player list with class icons

Player list with Steam profile links, ping/loss, playtime, account age, reputation, and TF2 class icons per player. Your own row is highlighted.

![Player list – classes, Steam links, playtime, reputation](doc/2026-02-17_21-12_3.png)
