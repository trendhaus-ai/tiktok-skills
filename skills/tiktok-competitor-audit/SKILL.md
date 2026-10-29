---
name: tiktok-competitor-audit
description: Audit competitor TikTok accounts - recent posts, which ones broke out against each account's usual views, and what those breakouts have in common - and turn it into moves for the user's own account. Use for competitor research, benchmarking, or "what are @x and @y doing on TikTok".
---

# TikTok competitor audit

Requires the Trendhaus connector (https://trendhaus.ai/docs).

## Steps

1. Get the accounts. If the user named handles, use them; otherwise call `trendhaus_competitor_pulse` without `handles` to use their tracked competitors. Offer to save new handles with `trendhaus_update_my_context` (`add_competitor`).
2. Call `trendhaus_competitor_pulse` (set `postsPerHandle` up to 10 for a fuller picture).
3. For each account, compute the median views of the returned posts and flag posts at 2× the median or more as breakouts. Note posting frequency.
4. Run `trendhaus_post_analysis` on the top one or two breakouts across all accounts (not every post) to see the hook and structure.
5. Answer with:
   - a table per account: followers, posts per week, median views, best post and its multiple;
   - what the breakouts share (format, hook type, topic, length);
   - three moves for the user's account, each tied to a specific example.

## Notes

- Paid-promotion flags are best-effort; a breakout may still be boosted. Say so when a post's views look far above its engagement.
- Data is live account state, not history.
