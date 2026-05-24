# Mulligan Coach — Data Feed

Auto-update feed for the Mulligan Coach overlay (an MTG Arena
mulligan helper). The overlay polls the floating
[`data-current` release](https://github.com/vonbeschwitz/mulligan_coach_data/releases/tag/data-current)
every few hours and atomically downloads any artifacts whose SHA256
hash differs from the local copy.

Each release contains:

- `manifest.json` — the discovery file the overlay fetches first.
- `<SET>-PremierDraft.parquet` — per-set 17Lands ratings.
- `<SET>-parsed-cards.json` — per-set parsed-card encodings.
- `<NAME>.zip` — model bundles (choice_v6 is current).
