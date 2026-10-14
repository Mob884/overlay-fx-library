# Overlay FX Library v1

**10,000 original screen-blend overlay videos** for video editors and creator apps.
720×1280 (9:16) · 24fps · 3s seamless loops · H.264 · black background (composite with **Screen** blend mode).

| Category | Count | | Category | Count |
|---|---|---|---|---|
| grain | 1000 | | vhs | 1000 |
| lightleak | 1000 | | rain | 1000 |
| dust | 1000 | | snow | 1000 |
| bokeh | 1000 | | flare | 1000 |
| glitch | 1000 | | smoke | 1000 |

**Tiers:** 7000 free / 3000 pro · **Collections:** 6 curated packs (Cinematic Film, Retro & VHS, Weather Moods, Glitch & Digital, Dreamy Bokeh, Essentials)

## What's in this repo

- `version.json` — force-update + catalog version check (your app polls this)
- `catalog/overlays.json` — full metadata for all 10,000 overlays
- `catalog/by_category/<cat>.json` — per-category splits for lazy loading
- `generator/build_overlays.py` — the generator script (fully resumable)

## What's NOT in this repo (by design)

The 10,000 MP4s (~7GB) and 10,000 thumbnails live on **Cloudflare R2** (or your own host),
not in git. Each catalog entry has a relative `file` path like `video/dust/dust_0001.mp4`
and a `thumbnail` path like `thumbs/dust/dust_0001.jpg`.

**App integration:**
1. Upload the `video/` and `thumbs/` folders to your host as-is.
2. Set `base_url` in your app config to your host, e.g.
   `https://pub-xxx.r2.dev/overlay-fx/`
3. Full video URL = `base_url + file`; thumbnail URL = `base_url + thumbnail`.

## License

All overlays are original, procedurally generated works — royalty-free for commercial use
in your apps and videos.
