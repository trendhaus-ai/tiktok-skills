---
name: tiktok-comment-mining
description: Read the comments on TikTok posts and pull out what the audience wants - questions, objections, purchase intent, praise and recurring requests - then turn them into content ideas. Use for "what are people saying", audience research, or finding demand in TikTok comments.
---

# TikTok comment mining

Requires the Trendhaus connector (https://trendhaus.ai/docs).

## Steps

1. For one post, call `trendhaus_post_analysis` with `includeComments: true`; it classifies up to 20 comments by purchase intent and category (question, complaint, praise, spam).
2. For more depth, call `tiktok_get_comments` with the post URL (page with `cursor`), and `tiktok_get_replies_comment_of_post` for threads with many replies.
3. For several posts (e.g. a competitor's top videos), repeat per post and merge the themes.
4. Group comments into 4–6 themes. For each: what people say (quote one or two real comments with their like counts), how many comments, and whether it signals buying interest.
5. Finish with content ideas that answer the strongest themes: a reply video, an FAQ post, or a product angle.

## Notes

- Quote comments exactly; don't invent or paraphrase them as quotes.
- Don't identify or profile individual commenters; work at the level of themes.
