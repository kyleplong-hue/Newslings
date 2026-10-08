# Newslings — Project Brief

## North Star
Kids today have no newspaper lying around. No casual exposure to the outside world — just cartoons with no ads, no real-world contact. Newslings is the newspaper that never existed for this generation: a daily 5-7 minute world news podcast built for kids aged 5-10, designed for the breakfast table.

**Not dumbed-down. Curiosity-led.**

---

## Format

**Duration:** 5–7 minutes daily
**Audience:** Ages 5–10
**Publish time:** 4:00 AM CET (kids listen before school)
**Segment order (fixed):**

1. **Intro** — signature opener + date
2. **World News** — 2–3 stories (never US-dominated)
3. **Inspiring Kid** — always 1 story about a kid making a difference
4. **Good News** — always 1 US story + uplifting angle
5. **Silly Fact** — Guinness record / Wikipedia anecdote / mind-blowing fact (bonus: links to recent news)
6. **Hope Message** — always ends with warmth and optimism
7. **Outro** — short sign-off

**Total scripted:** 8–10 stories (includes 2 backup [OPTIONAL] slots for removal)

---

## Content Rules

- NO murder, famine, graphic violence, death counts
- Wars: high-level only — who, why, how long, peace focus
- Natural disasters: OK — explain the science (educational value)
- Inspiring kid story: what they did, why, who they helped, how
- Good news: 1 always US, never US-dominated overall
- Silly/Guinness: must be genuinely mind-blowing, bonus if it ties to recent news
- Always end on hope

---

## Voice & Production

- **Host:** HeyGen avatar (Kyle's existing Digital Twin)
- **Delivery:** Audio-only for now — architecture ready for video podcast transition
- **Pronunciation:** Hard words get phonetic guide inline — e.g. *"the Himalayas (him-AH-lay-uz)"*
- **Tone:** Like a curious older sibling, not a children's TV presenter

---

## Tech Pipeline

### Step 1 — Story Gatherer (subagent, runs ~10 PM CET nightly)
- Sources: BBC RSS, Reuters RSS, AP RSS, Google News RSS (all free, no API key)
- Searches specifically for: inspiring kids story, US good news, silly/Guinness fact
- Proposes 8–10 stories with category tags + brief summary
- Content filter: flags borderline content automatically

### Step 2 — Script Writer (subagent)
- Writes full script for ALL proposed stories
- Age 5–10 language: short sentences, no jargon, phonetic guides
- Target: 750–950 words = ~5–7 min
- Marks backup stories [OPTIONAL - safe to remove]
- Output: complete ready-to-read script

### Step 3 — Approval Web UI (proposed)
- Private, authenticated approval URL (do not expose an unauthenticated review/publish endpoint)
- Each segment shown as a card with full script text
- Actions: ✅ Keep | ❌ Delete | 📅 Move to Tomorrow
- "Generate Episode" button → immediately triggers Step 4
- Time investment: ~3–5 min per night

### Step 4 — HeyGen (subagent, triggered by approval)
- Submits approved script to HeyGen API v2
- Uses Kyle's existing avatar ID
- Polls until video is ready (~5–15 min)
- Downloads video → extracts MP3 audio via ffmpeg

### Step 5 — Publish
- Uploads MP3 to Spotify for Creators (free, distributes everywhere)
- RSS auto-syncs to Apple Podcasts, Google Podcasts
- Discord ping to Kyle: "Episode ready ✅ [listen link]"

### Step 6 — Video Transition (future, architecture ready)
- Keep the HeyGen video file (don't delete after audio extraction)
- Upload to YouTube as video podcast
- Upload to Spotify as video episode
- No code changes needed — just activate the upload step

---

## Infrastructure

| Component | Tool | Cost |
|---|---|---|
| News sources | BBC/Reuters/AP RSS | Free |
| Script generation | Claude (subagent) | ~$0.05/episode |
| Video generation | HeyGen API (Creator plan) | $29/mo |
| Audio extraction | ffmpeg | Free |
| Podcast hosting | Spotify for Creators | Free |
| Distribution | Spotify → Apple → RSS | Free |
| Approval UI | Simple Node.js on existing VPS | Free |

**Estimated monthly cost: ~$29 (HeyGen) + pennies in API calls**

---

## Branding

**Name:** Newslings
**Domain target:** newslings.fm (podcast standard TLD) — check availability
**Backup:** newslings.io (confirmed available)
**Note:** newslings.com availability must be checked independently; the original brief's expiry date is historical.

**Tagline options:**
- *"Get your kids out of the algorithm, into the world."* ← CHOSEN
- *"The world, in 5 minutes, for curious kids"*
- *"Your morning newspaper — reimagined for little ears"*
- *"Big world. Little explorers."*

**Tone:** Curious older sibling. Not a TV presenter. Not dumbed-down.

---

## Catchphrase (draft)
*"Hey Newslings! Ready to explore the big wide world? Let's go!"*

---

## External accounts (proposed)
- HeyGen API access must be configured outside Git, using a secret manager or local environment variables.
- Podcast hosting: Spotify for Creators (account/setup to verify).
- Distribution destinations and current platform support must be verified before implementation.

---

## Phase 1 — Tomorrow's Episode (test)
Goal: produce audio file for Kyle's kids, no publishing needed yet.
1. Run story gatherer manually
2. Generate full script
3. Submit to HeyGen → extract audio
4. Send MP3 to Kyle via Discord

## Phase 2 — Full Pipeline (week 1)
- Build approval web UI
- Set up Spotify for Creators account
- Automate nightly gather + script
- Wire HeyGen + publish step

## Phase 3 — Scale (month 2+)
- YouTube video podcast
- Website with episode archive
- Newsletter / email digest version
- Multilingual (French first, for Aéllo audience crossover?)

## Website To-Do List
- [ ] Fix "NEW EPISODE OUT NOW" star badge clipping — overflowing outside its parent container (needs `overflow: visible` on parent or repositioning)
