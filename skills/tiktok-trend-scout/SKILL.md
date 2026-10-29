---
name: tiktok-trend-scout
description: Find TikTok trends a brand or creator can use right now, with an explainer video for each and a clear read on brand fit, then turn the best ones into content ideas. Use for "what's trending on TikTok", "trends for my brand", or trend ideas for a niche.
---

# TikTok trend scout

Requires the Trendhaus connector (https://trendhaus.ai/docs).

## Steps

1. Call `trendhaus_trend_radar` in discovery mode. Pass `usability: "directly_usable"` when the user wants things they can act on; leave it out for a full picture.
2. For each trend you keep, use `trend_name`, `trend_description`, `trend_type`, `usability`, `explainer_video_url` and `latest_validation` (views and video count indicate its scale).
3. Pick 3–5 trends that fit the user's brand or niche. Prefer `directly_usable`; include `use_with_caution` ones only with a note on brand-voice risk; never present `context_only` items as content templates.
4. For the one or two strongest, call `trendhaus_trend_radar` again with `trend_name` to get the full history and `evidence_video_urls`.
5. Answer with a short table (trend, what it is, scale, fit, explainer link), then one content idea per trend: the hook line, the format and how the brand fits in.

## Notes

- `first_seen_at` is when the watchlist first saw the trend, not a forecast; don't call trends "early" or "peaking".
- Results reflect the last scheduled poll. The watchlist is curated, not exhaustive; repeat what `gaps` says about coverage.
