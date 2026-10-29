---
name: tiktok-video-teardown
description: Break down a TikTok video or photo slideshow someone pastes - hook, scenes, on-screen text, sound, comments and how it performed against the creator's usual posts - and turn it into what to copy. Use when the user shares a TikTok link and asks why it worked, what happens in it, or how to make their own version.
---

# TikTok video teardown

Requires the Trendhaus connector (https://trendhaus.ai/docs).

## Steps

1. Call `trendhaus_post_analysis` with the link as `videoUrl`. Set `includeComments: true` when the user cares about the audience (questions, objections, purchase intent).
2. Read the result:
   - `data.visual.hook_window_description` and `hook_type`: what happens in the first seconds.
   - `data.visual.scene_sequence`: the structure, with timestamps.
   - `data.visual.text_overlays`, `data.transcript`, `data.music`: what is shown, said and heard.
   - `computed.views_vs_author_median`: how this post did against the creator's own recent posts (1.0 = typical).
   - `computed.comment_intelligence` (when requested): what commenters ask for.
   - `gaps`: anything missing; say so instead of filling it in.
3. Answer in this order:
   - **Verdict:** one line on whether it over- or under-performed and by how much.
   - **Hook:** the first 1–3 seconds and why they hold attention.
   - **Structure:** the scene beats in a short list.
   - **What the audience says:** two or three comment themes (when available).
   - **What to copy:** three concrete moves the user can reuse, and one to avoid.
4. If the user names their own brand or niche, finish with a one-paragraph brief for their version: hook line, on-screen text for the first frame, and the beat sequence.

## Notes

- Analysis watches the real video and can take up to about 40 seconds.
- Don't describe visuals that aren't in the result.
