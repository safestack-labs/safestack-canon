┌──────────────────────────────┐
│          ŽMOGUS              │
│  (ketinimas, ne komanda)     │
└──────────────┬───────────────┘
               │
               ▼
┌──────────────────────────────┐
│     TELEGRAM BOT (bot.py)    │
│ ─────────────────────────── │
│ • anonimizuoja               │
│ • nefiksuoja tapatybės       │
│ • NEvykdo                    │
│ • generuoja INTENCIJĄ        │
└──────────────┬───────────────┘
               │
               ▼
┌──────────────────────────────┐
│     INTENTION LEDGER         │
│  (GitHub / append-only)     │
│ ─────────────────────────── │
│ • JSON (pasiūlymas)          │
│ • vieša / pusiau vieša       │
│ • be vykdymo garantijų       │
│ • be adresato               │
└──────────────┬───────────────┘
               │
     ┌─────────┴─────────┐
     │                   │
     ▼                   ▼
┌───────────────┐   ┌───────────────┐
│   NODE A      │   │   NODE B      │
│ SafeStack    │   │ SafeStack     │
│   NodeOS     │   │   NodeOS      │
│──────────────│   │────────────── │
│ • Canon       │   │ • Canon        │
│ • Identity    │   │ • Identity     │
│ • Manifest    │   │ • Manifest     │
│ • Lifecycle   │   │ • Lifecycle    │
│ • Autonomy    │   │ • Autonomy     │
│               │   │                │
│ skaito, jei   │   │ skaito, jei    │
│ pats nori     │   │ pats nori      │
│               │   │                │
│ sprendžia:    │   │ sprendžia:     │
│ ✓ accept      │   │ ✗ deny         │
│ ○ ignore      │   │ ⌀ silent       │
│               │   │                │
│ rašo tik:     │   │ rašo tik:      │
│ state.json    │   │ state.json     │
└───────┬───────┘   └───────┬───────┘
        │                   │
        └─────────┬─────────┘
                  ▼
        ┌────────────────────────┐
        │   OBSERVER LAYER       │
        │  (R2000 + Pi 5 DSI)    │
        │────────────────────────│
        │ • tik skaitymas        │
        │ • būsenos              │
        │ • alertai              │
        │ • heartbeat            │
        │ • NĖRA kontrolės       │
        └────────────────────────┘
