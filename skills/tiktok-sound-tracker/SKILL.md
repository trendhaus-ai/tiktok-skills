---
name: tiktok-sound-tracker
description: Track a TikTok sound or song - how many videos use it, which accounts and niches are pushing it, and how the top uses perform - for music marketers, artists and labels. Use when the user shares a TikTok sound link or asks who is using a song on TikTok.
---

# TikTok sound tracker

Requires the Trendhaus connector (https://trendhaus.ai/docs).

## Steps

1. Get the sound ID from the link (`tiktok.com/music/<name>-<id>`). If the user only has a video, call `tiktok_get_post_details` and read its music ID.
2. Call `tiktok_get_music_info` for the title, artist, original-audio flag and total video count.
3. Call `tiktok_get_music_posts` for recent posts using the sound; page with `cursor` for more.
4. Group the posts by kind of account (fan pages, creators, brands, the artist) and niche (for example football edits, beauty, comedy), and list the top uses by views.
5. Run `trendhaus_post_analysis` on the one or two biggest uses to see how the sound is used (lip-sync, background, transition).
6. Answer with: total videos, the niches carrying it, the top 5 uses with links and views, and two or three seeding ideas (which kinds of pages to approach, and with which format).

## Notes

- Re-run later to compare the video count over time; the tool reports the current count, not a history.
