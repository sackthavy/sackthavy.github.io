# Games by Zaib

Home / launcher page for Jahan Zaib's browser games — live at **https://wahidzeb.github.io/**

| Game | Genre | Link |
|---|---|---|
| Moto Mayhem | Motorbike combat racer | https://wahidzeb.github.io/moto-mayhem/ |
| Sky Glide | Paper plane flying | https://wahidzeb.github.io/sky-glide/ |
| Horde Breaker | Zombie survival shooter | https://wahidzeb.github.io/horde-breaker/ |
| Goal Frenzy | Arcade football | https://wahidzeb.github.io/goal-frenzy/ |
| Shuttle Smash | Badminton (1P / 2P) | https://wahidzeb.github.io/shuttle-smash/ |
| Kedimz Adventure | Platformer | https://zaibgames.com/kedimz-adventure/ |
| Kedimz Mario | Platformer | https://zaibgames.com/kedimz-mario/ |

Each game lives in its own repo (project site); this repo is only the root user site.

## Adding a game

1. Add a thumbnail to `img/` (600×375 webp, ~10–30 KB).
2. Edit the `GAMES` array near the bottom of `index.template.html`:
   ```js
   { name: "New Game", desc: "One-line pitch.", genre: "Arcade",
     url: "https://wahidzeb.github.io/new-game/", img: "img/new-game.webp", color: "#f59e0b" },
   ```
   Leave `url: null` to show a "Coming soon" card.
3. Run `./build.sh` (inlines the display font → `index.html`), commit and push.

## Files

- `index.html` – the built, fully self-contained page (no external requests besides local images)
- `index.template.html` – source (same as index.html, with a `__FONT__` placeholder)
- `fonts/lilita-subset.woff` – subset of Lilita One (SIL OFL) inlined by `build.sh`
- `img/` – game thumbnails, `og.jpg` (1200×630 share preview), icons
- `#ad-slot` – empty ad banner placeholder (no ads)
- `.nojekyll` – serve files as-is
