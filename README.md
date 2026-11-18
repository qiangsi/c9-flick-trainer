# Cloud9 Flick Trainer

A 60-second flick-shot / aim trainer mini-game, built for the
**Cloud9 x JetBrains "Sky's the Limit" Hackathon 2026 — Category 3 (Event Mini Game)**.

## What it is

A fast, replayable booth game: targets pop up for one minute, you click them
as fast as you can. It is designed for a Cloud9 event booth — one play session
lasts 60 seconds, controls are a single click, and the game resets cleanly
between players.

- **60-second rounds** — quick sessions keep the booth line moving.
- **Combo multiplier** — chain hits to multiply your score, up to x5. A miss
  breaks the combo.
- **Quick-flick bonus** — hits within 300 ms of a target appearing earn +50.
- **Moving targets** — appear in the second half of the round and are worth
  double points.
- **Booth leaderboard** — top 10 scores stored locally in `localStorage`,
  so it works with no Wi-Fi and can be shown on a second monitor.
- **Attract mode** — after 30 seconds idle on the menu, decorative targets
  drift across the screen to draw in the next player.
- **Clean reset** — "Play Again" starts a fresh round instantly.

## How to run

No build step, no dependencies. Open `index.html` in any modern browser
(Chrome, Edge, Firefox, Safari), or serve the folder with any static server:

```bash
npx serve .
# or
python3 -m http.server
```

## Controls

| Input | Action |
| --- | --- |
| Mouse / touch | Click / tap targets |
| `Enter` / `Space` | Start the game from the menu |
| `Enter` / `R` | Play again from the results screen |

## Scoring

| Event | Points |
| --- | --- |
| Target hit | 100 × combo multiplier (x1–x5) |
| Quick flick (< 300 ms) | +50 bonus |
| Moving target hit | 200 × combo multiplier |
| Miss | Combo resets to x1 |

Ranks: Rookie (< 1,200) · Rising Star (< 2,500) · Contender (< 4,000) ·
Prospect (< 6,000) · Cloud9 Material (6,000+).

## Built with

- **JetBrains WebStorm** — main IDE for the project.
- **JetBrains Air** — in-IDE agent orchestration for development and review.
- **Junie (JetBrains AI coding agent)** — helped write the game loop and tune
  the difficulty ramp.

The `.idea` folder is committed as evidence of the JetBrains tooling used.
See `AI_SHOWCASE.md` for the full AI-powered workflow story (bonus prize).

## Originality

All artwork is drawn in code (canvas). No Riot Games content is used: no
VALORANT or League of Legends names, characters, artwork, or logos.
This project is not affiliated with Cloud9 or Riot Games.

## License

Apache License 2.0 — see `LICENSE`.
