<p align="center"><img src="assets/logo.png" width="72" alt="Trendhaus"></p>

<h1 align="center">TikTok research skills for Claude, ChatGPT and Codex</h1>

<p align="center">
Agent skills that turn your AI into a TikTok researcher: break down any video, find trends a brand can use, audit competitors, mine comments and track sounds. Powered by the <a href="https://trendhaus.ai/?ref=github">Trendhaus</a> TikTok MCP server.
</p>

---

## Why

Paste a TikTok link into ChatGPT or Claude and it can't watch it. With Trendhaus connected, your AI gets the transcript, on-screen text, a scene-by-scene breakdown, the hook, the sound, the comments and how the post did against the creator's usual numbers. These skills package that into repeatable workflows.

## Skills

| Skill | What it does | Example prompt |
|---|---|---|
| [`get-started`](skills/get-started/SKILL.md) | Setup, which tool for which question, reading results faithfully | "What can Trendhaus do?" |
| [`tiktok-video-teardown`](skills/tiktok-video-teardown/SKILL.md) | Hook, scenes, sound, comments and performance of one video, plus what to copy | "Break down this TikTok: [link]" |
| [`tiktok-trend-scout`](skills/tiktok-trend-scout/SKILL.md) | Current TikTok trends with explainer videos and brand fit, turned into ideas | "What's trending on TikTok that my skincare brand could use?" |
| [`tiktok-competitor-audit`](skills/tiktok-competitor-audit/SKILL.md) | Competitors' recent posts, breakouts against their median, shared patterns | "Audit @glossier and @theordinary on TikTok" |
| [`tiktok-comment-mining`](skills/tiktok-comment-mining/SKILL.md) | Questions, objections and purchase intent in comments, turned into content | "What are people asking for in these comments? [link]" |
| [`tiktok-sound-tracker`](skills/tiktok-sound-tracker/SKILL.md) | Who uses a sound, in which niches, and how the top uses perform | "Who is using this sound? [link]" |

## Install

**1. Connect the Trendhaus MCP server** (one sign-in, no TikTok login or API key): [start free with 100 actions](https://trendhaus.ai/start?ref=github), then follow the [setup docs](https://trendhaus.ai/docs?ref=github). Server URL: `https://mcp.trendhaus.ai/mcp`.

**2. Add the skills:**

- **Claude Code**
  ```
  /plugin marketplace add trendhaus-ai/tiktok-skills
  /plugin install trendhaus
  ```
- **Any agent that supports Agent Skills** (Cursor, Codex, Gemini CLI, and others)
  ```
  npx skills add trendhaus-ai/tiktok-skills
  ```
- **Claude.ai / ChatGPT:** connect Trendhaus as a connector ([docs](https://trendhaus.ai/docs?ref=github)); the skills folder can also be uploaded as custom skills.

## What the data covers

Public TikTok data only: posts, creators, comments, sounds, hashtags and the public top-ads library, plus Trendhaus's own analysis (trend detection, video perception, hook extraction, comment classification). Read-only: nothing is posted or changed on any TikTok account.

## Links

- Website: [trendhaus.ai](https://trendhaus.ai/?ref=github)
- Docs: [trendhaus.ai/docs](https://trendhaus.ai/docs?ref=github)
- Can ChatGPT watch TikTok videos? [How it works](https://trendhaus.ai/can-chatgpt-watch-tiktok-videos)
- Support: team@trendhaus.ai

Not affiliated with TikTok. Skills are MIT licensed; using the MCP server requires a Trendhaus account.
