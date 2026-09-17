# Accord

A social fragrance‑discovery app built around **pairwise preference** instead of star ratings.

Instead of asking *"rate this 1–10,"* Accord asks **"which of these two would you rather wear?"** Your choices are turned into a personal ranking (bucketed binary‑search insertion + Elo‑style scoring), a taste profile ("Fragrance DNA"), and taste‑matched discovery through people who share your nose ("nose‑twins").

> **Status:** working front‑end prototype. Single self‑contained `index.html` (vanilla JS, no build step), state persisted in `localStorage`.

## Run it

Open `index.html` in any browser, or serve the folder:

```bash
python -m http.server 8000
# then visit http://localhost:8000
```

## What's in it

- **Onboarding** — pick fragrances you've tried → bucket (Love / Fine / Pass) → pairwise comparisons → your ranking.
- **Comparison engine** — bucket‑narrowed binary‑search insertion (≈log₂ n taps to place a fragrance); derived 0–10 scores.
- **Home** — search, segmented **For you / Trending / Friends**, featured guides, and a social feed.
- **Explore** — "explore like [your picks]" + browse by accord family.
- **Activity** — friend recommendations + confidence‑aware taste matches.
- **Profile** — Top 5, Fragrance DNA, **category rankings by family** (you can't compare a fresh to a date‑night on one axis), and Tried / Owned / Want collections.
- **Posts** — short (≤50‑word) updates with an optional fragrance attachment.
- **Fragrance detail** — house monogram, derived rank/score, notes, Tried/Owned/Want, "smells similar."

## Design

Clean, editorial consumer UI: white ground, a sage accent (`#567E70`), angular Space Grotesk type, thin hairline borders, and per‑house typographic **monograms** as tile art. (Real bottle photography is a later step — it needs licensed imagery; the monogram tiles are the deliberate, ship‑now stand‑in.)

## Roadmap

- Real backend (Expo + Supabase) → accounts, sync, and *real* nose‑twins instead of sample profiles.
- Licensed fragrance catalog + bottle imagery.
- Recommend‑to‑a‑friend flow, richer guides.

## Notes

House names shown in the app are plain text references to real fragrance houses; no brand logos or copyrighted artwork are reproduced. Fragrance metadata is a small seeded set for the prototype.
