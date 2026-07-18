---
name: sync-event-recordings
description: Cross-reference The Pipeline Conference Eventbrite past events and YouTube channel to create Hugo posts with embedded recordings for any event not yet represented. Use when asked to sync, cross-reference, or add posts for event recordings, or when new event videos have been uploaded to YouTube.
---

# Sync Event Recordings

Create a Hugo post with an embedded YouTube video for each recorded Pipeline Conference event that is on Eventbrite and YouTube but has no post under `content/posts/` yet.

## Sources

- Eventbrite organizer (past events): `https://www.eventbrite.com/o/the-pipeline-conference-21692343871` (click the **Past** tab, then **Show more** until all events are loaded)
- YouTube channel videos: `https://www.youtube.com/@ThePipelineConference/videos`
- Existing posts: `content/posts/` (files named `YYYY-MM-DD-kebab-case.md`)

## Workflow

```
- [ ] 1. List all Eventbrite past events (title + date)
- [ ] 2. List all YouTube uploads (title + video ID)
- [ ] 3. List existing posts and the YouTube IDs already embedded
- [ ] 4. Match events across all three sources
- [ ] 5. Create a post for each unrepresented match
- [ ] 6. Build with Hugo to verify
```

**Step 1 — Eventbrite.** Use the browser tools. Navigate to the organizer URL, click the **Past** tab, click **Show more** until no more load, then extract event titles and links. Get each event's exact date by fetching its event page (the date appears as e.g. "Tuesday, July 15, 2025"). Use the PDT/PST (Los Angeles) date, since CI builds with `TZ: America/Los_Angeles`.

**Step 2 — YouTube.** Navigate to the channel videos URL and extract each video's title and 11-character ID from its `/watch?v=<ID>` link (strip any `&pp=...` suffix).

**Step 3 — Existing posts.** Search `content/posts/` for `{{< youtube ... >}}` shortcodes to collect already-embedded IDs, and read post titles/dates.

**Step 4 — Match.** Pair an Eventbrite event with a YouTube upload by title. Only create posts for events that have BOTH an Eventbrite listing AND an uploaded recording, and that are NOT already represented (by video ID or by an equivalent existing post). Skip:
- Conference session clips that aren't standalone Eventbrite events
- Events with no uploaded recording
- Anything already posted

**Step 5 — Create posts.** One file per match at `content/posts/YYYY-MM-DD-kebab-title.md` using the event's Eventbrite date. Follow the template below.

**Step 6 — Verify.** Run the build and confirm every new video ID appears in the output:

```sh
hugo --gc --minify --destination /tmp/pipedev-build
```

## Post template

```markdown
---
title: "Event Title"
date: YYYY-MM-DD
author: Ryan Bottriell
summary: "One-sentence summary of the recorded session."
---

One or two sentences describing what the session covered.

{{< youtube VIDEO_ID >}}

[View the original event on Eventbrite](EVENTBRITE_URL).
```

## Conventions

- Author is always `Ryan Bottriell`.
- Frontmatter is YAML with `title`, `date`, `author`, `summary`.
- Embed videos with the Hugo shortcode `{{< youtube VIDEO_ID >}}`, not raw `<iframe>`.
- Titles in frontmatter may be cleaned up from marketing phrasing, but keep them recognizable.
- Do not commit unless asked; leave changes for review.
