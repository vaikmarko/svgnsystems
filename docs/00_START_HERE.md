# DRILL PROTOCOL -- Start Here

> Read this first. Everything else builds on this.

---

## What is Drill Protocol?

A full-ARG (Alternate Reality Game) survival training app disguised as a terminal/hacker interface. It sends you real-time notifications, asks you to photograph your home, analyzes your supplies with AI Vision, and scores your readiness. Scenarios bleed into real life -- you actually walk to your door, sit in the dark, pack a bag, find hiding spots on your street.

**Think:** Duolingo's addiction mechanics + Pokemon Go's real-world interaction + Black Mirror's unsettling realism. For survival.

---

## Who is it for?

**Primary:** 16-22 year olds (Gen Z / TikTok generation)
**Tone:** Scary-real. Not educational. Not preachy. Shocking facts, personal results, social pressure.
**Goal:** So viral that parents ask "please shut this down" -- but can't, because it's teaching their kids actual survival skills.

---

## The Three Layers

```
LAYER 1: QUICK SCAN (30 seconds)
  First-time "Angry Birds moment"
  5 questions, AI photo analysis, Readiness Score
  Immediate sharing trigger ("I got 23/100")

LAYER 2: FLASH DRILLS (3-30 minutes)
  Mind-fuck scenarios + photo validation
  "Is that really your mom?" (AI voice cloning)
  "Your phone is dead" (digital dependency)
  "Pack a bag in 10 minutes" (Grab Bag)

LAYER 3: ARG STORIES (throughout the day)
  Full alternate-reality scenarios
  "Someone is at your door" -- go check, photograph
  "Find a dead drop location" -- go outside, explore
  "Blackout Night" -- lights off for 1 hour, 847 people simultaneously
  Notifications arrive like real events
```

---

## What makes it different from everything else

| Feature | Competitors | Drill Protocol |
|---------|------------|----------------|
| Content type | Static PDFs, checklists | Real-time interactive simulation |
| User action | Read text | Photograph, move, decide, prove |
| AI | None | Vision API analyzes your actual home |
| Social | None | Challenge friends, Squad system, leaderboards |
| Design | Generic app UI | Full terminal/HUD hacker aesthetic |
| Engagement | Open once, forget | Daily briefings, streaks, ARG notifications |
| Virality | None | "What's your Readiness Score?" sharing loop |

---

## How the documents connect

```
00_START_HERE.md (you are here)
  "What is this? Who is it for?"
      │
      ▼
01_CONTENT_BIBLE.md
  "Every screen, every word, every emotion"
  This is the PRODUCT. If you're designing,
  writing content, or building UI -- live here.
      │
      ▼
02_BUILD_ORDER.md
  "What to build, in what order"
  If you're a developer -- this is your task list.
  Each task references specific sections in the Content Bible.
      │
      ▼
03_GLOBAL_VISION.md
  "Where this goes in 1-3 years"
  15 scenario types, Squad system, B2B,
  localization, revenue targets.
  Read this to understand the bigger picture.
```

---

## Key decisions already made

- **Platform:** Web-first (PWA), $0 cost, GitHub Pages
- **Design:** Full terminal/HUD aesthetic (black background, green text, CRT effects, typewriter animations)
- **AI:** Gemini Vision API for photo analysis (free tier)
- **Data:** localStorage (no server needed for MVP)
- **Immersion level:** Full ARG -- app sends notifications as if events are real, user must physically act
- **Safety:** Every ARG notification starts with "This is a drill." Never asks user to do anything dangerous.
- **Controversy strategy:** Edgy enough that media writes about it, safe enough that Apple won't remove it

---

## Current status

- [x] Landing page live at svgnsystems.com
- [x] Brand identity (terminal/tactical green theme)
- [x] Complete content written (Content Bible)
- [x] Build order defined
- [ ] **NEXT: Build Quick Scan experience (SAMM 1)**
