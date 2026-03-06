# DRILL PROTOCOL -- Build Order

> Concrete development tasks. Each step produces a deployable result.
> Full content for each step: [01_CONTENT_BIBLE.md](./01_CONTENT_BIBLE.md)
> Long-term roadmap: [03_GLOBAL_VISION.md](./03_GLOBAL_VISION.md)

---

## Tech Stack

| Layer | Tech | Cost |
|-------|------|------|
| Build | Vite + TypeScript | $0 |
| UI | Terminal CSS (custom) + Web Audio API | $0 |
| AI | Gemini Vision API (free tier: 60 req/min) | $0 |
| Data | localStorage (no server) | $0 |
| Sharing | Canvas API + Web Share API | $0 |
| PWA | manifest.json + Service Worker | $0 |
| Haptic | Vibration API | $0 |
| Hosting | GitHub Pages (already live) | $0 |
| **Total** | | **$0** |

---

## Build Steps

### STEP 1: Quick Scan + Terminal UI + Sound

**Goal:** User opens svgnsystems.com/app, gets scanned, receives Readiness Score in 60 seconds. Full terminal aesthetic with sound.

**Content Bible reference:** Sections "AVAMINE", "QUICK SCAN", "TULEMUSED"

**Deliverables:**
- [ ] `app.html` -- entry point for the interactive app
- [ ] Terminal UI components
  - [ ] TypewriterText (character-by-character with keyboard sound)
  - [ ] ProgressBar (animated, with rising pitch hum)
  - [ ] ScanAnimation ("ANALYZING..." effect)
  - [ ] AlertBox (red flashing text + alarm beep)
  - [ ] SuccessBox (green pulse + positive tone)
  - [ ] HUDHeader (time, score, status bar)
  - [ ] CRT overlay (scanlines CSS effect)
- [ ] Sound system (Web Audio API)
  - [ ] Boot-up hum
  - [ ] Typewriter clicks (randomized pitch)
  - [ ] Scan processing sound
  - [ ] Warning alarm (2 beeps)
  - [ ] Success tone
  - [ ] Haptic feedback on mobile
- [ ] Opening screen
  - [ ] Black screen, cursor blink, typewriter text
  - [ ] IP-based city detection (free API)
  - [ ] Personalized threat message
  - [ ] "FIND OUT IN 60 SECONDS" CTA
- [ ] 5 scan questions (text-only first, AI Vision in Step 2)
  - [ ] Water supply (with self-report fallback)
  - [ ] Emergency lighting
  - [ ] First aid
  - [ ] Food supply
  - [ ] Emergency plan
  - [ ] Each scan: shocking fact + question + response + score
- [ ] Results screen
  - [ ] Readiness Score (0-100)
  - [ ] Survival time estimate
  - [ ] Gap analysis (what's missing)
  - [ ] Percentile rank ("less prepared than 89%")
  - [ ] Three CTAs: Share / Start Drill / Challenge Friend
- [ ] localStorage: save scan results, score, date

**Test:** Open on mobile. Does the terminal feel real? Does the sound create atmosphere? Does the score make you feel something?

---

### STEP 2: AI Vision + Camera

**Goal:** Photo-based validation. User photographs water, first aid kit, food -- AI analyzes and gives terminal-style report.

**Content Bible reference:** Sections "SCAN 1-5" (photo variants), "AI Vision tehniline lahendus"

**Deliverables:**
- [ ] Camera integration (MediaDevices API)
  - [ ] Full-screen camera overlay
  - [ ] Photo capture + preview
  - [ ] Permission handling + fallback to self-report
- [ ] Gemini Vision API integration
  - [ ] Custom prompts per scan type (water, medical, food)
  - [ ] Structured response parsing (detected items, missing items, score)
  - [ ] Terminal-style report generation
  - [ ] 3-8 second response time
- [ ] Privacy: image sent, analyzed, deleted -- never stored
- [ ] Fallback: if camera denied or API down, self-report works fully
- [ ] Update Quick Scan to use camera where available

**Test:** Photograph your kitchen. Does AI correctly identify water bottles? Does the report feel like a real security scan?

---

### STEP 3: Sharing + Friend Experience

**Goal:** User shares Readiness Score. Friend opens link, sees challenge, does their own scan, sees comparison.

**Content Bible reference:** Sections "JAGAMINE: VIRAALNE LOOP", "SOBRA KOGEMUS"

**Deliverables:**
- [ ] Readiness Score share image (Canvas API)
  - [ ] Terminal-style card (black bg, green text, score, survival time)
  - [ ] Personalized (name, city, score)
  - [ ] "How long would YOU last?" tagline
- [ ] Challenge link generation
  - [ ] URL params: `?ref=name&score=23`
  - [ ] Friend landing: "Marko scored 23. Prove him wrong."
- [ ] Friend experience flow
  - [ ] See challenger's score before scan
  - [ ] Complete own scan
  - [ ] Side-by-side comparison ("You are BOTH going to die...")
  - [ ] Three next steps: Challenge someone else / Fix together / Create Squad
- [ ] Web Share API integration
  - [ ] WhatsApp, Instagram Story, TikTok, Copy Link
- [ ] Share counter (localStorage-based, approximate)

**Test:** Share your score with a friend. Do they actually open the link? Do they complete the scan? Do they share their result?

---

### STEP 4: Drill Hub + ARG Scenarios + Flash Drills

**Goal:** After Quick Scan, user enters Drill Hub with multiple scenarios. ARG stories that bleed into real life.

**Content Bible reference:** Sections "MIND-FUCK STSENAARIUMID", "ARG LOOD", "FLASH DRILL GRAB BAG", "DRILL HUB"

**Deliverables:**
- [ ] Drill Hub screen
  - [ ] Available drills (with descriptions, duration, difficulty)
  - [ ] Locked drills (unlock via streak)
  - [ ] Daily Challenge (rotating, with timer)
  - [ ] Squad section (placeholder for future)
  - [ ] Operative profile summary (rank, score, streak)
- [ ] Flash Drills
  - [ ] **Grab Bag** (10 min timer, reminders, bag photo AI analysis, grade A+ to F, Perfect Bag guide)
  - [ ] **Trust Protocol** ("Is that really your mom?" -- AI voice clone scenario, family code word)
  - [ ] **Unplugged** ("Your phone is dead" -- 5 questions about digital dependency)
  - [ ] **Pocket Check** (photograph what's on you right now, AI analysis)
  - [ ] **Who's Next Door?** (do you know your neighbor's name?)
  - [ ] **3AM** (someone breaks in, 45 seconds, what do you do?)
- [ ] ARG Stories (push notification-driven, multi-part)
  - [ ] **Knock Knock** (go to your door, photograph it, AI assesses security, story develops through the day)
  - [ ] **Dead Drop** (go outside, find a hiding spot within 200m, photograph it, tell one person)
  - [ ] **Stranger Danger** (activate on your daily route, count cameras, find safe buildings, "someone is following you" scenario)
  - [ ] **Blackout Night** (21:00 lights off, 1 hour in darkness, tasks in the dark, live participant counter)
- [ ] Each drill/story saves results to localStorage
- [ ] Each drill has share trigger at the end

**Test:** Do the ARG notifications feel real enough to make you get up? Does "Knock Knock" make you actually go to your door? Does "Blackout Night" make you actually turn off the lights?

---

### STEP 5: Retention + Progression + Landing Page

**Goal:** Users come back every day. Score grows over time. Landing page drives new users to Quick Scan.

**Content Bible reference:** Sections "TAGASITULEKU MOOTOR", "PROGRESSIOONISUSTEEM", "DRILL HUB"

**Deliverables:**
- [ ] Daily Briefing (push notification)
  - [ ] Score update, streak status, rank
  - [ ] Today's recommended drill
  - [ ] Fact of the day
  - [ ] Service Worker for push notifications
- [ ] Streak system
  - [ ] Day counter with fire emoji
  - [ ] Streak milestones unlock new drills (3d, 7d, 14d, 30d)
  - [ ] Streak loss notification ("In a real emergency, you can't skip a day")
  - [ ] Streak shield (1 free, earn more)
- [ ] Progression: RECRUIT > OPERATOR > SPECIALIST
  - [ ] Visible rank with progress bar
  - [ ] Each rank changes drill difficulty and AI behavior
  - [ ] RECRUIT: guided, hints available
  - [ ] OPERATOR: harder, fewer hints, Squad unlocks
  - [ ] SPECIALIST: no hints, custom scenarios, can create drills
- [ ] Operative Profile screen
  - [ ] Rank, score, streak, drills completed, badges
  - [ ] Shareable profile card
- [ ] Badge system
  - [ ] first_scan, first_drill, week_streak, blackout_survivor, etc.
- [ ] PWA
  - [ ] manifest.json (name, icons, theme color)
  - [ ] Service Worker (offline support, push notifications)
  - [ ] "Add to Home Screen" prompt
- [ ] Landing page update
  - [ ] New hero: "What's your Readiness Score?"
  - [ ] Direct link to Quick Scan
  - [ ] Social proof counter ("X operatives scanned")
  - [ ] Remove old pricing section (replace with "Free to start")

**Test:** Do you open the app tomorrow because of the Daily Briefing? Does losing a streak hurt? Does reaching OPERATOR feel like an achievement?

---

## Definition of Done (V1)

The MVP is complete when:

- [ ] A user can open svgnsystems.com, complete Quick Scan in 60 seconds, and get a Readiness Score
- [ ] AI Vision analyzes at least 3 photo types (water, first aid, food)
- [ ] User can share score and challenge a friend
- [ ] Friend can complete challenge and see comparison
- [ ] At least 3 Flash Drills are playable (Grab Bag, Trust Protocol, Unplugged)
- [ ] At least 1 ARG story works (Knock Knock or Blackout Night)
- [ ] Daily Briefing brings users back
- [ ] Streak system motivates daily use
- [ ] Works on mobile (375px+) with sound and haptics
- [ ] Terminal aesthetic is consistent and immersive throughout
- [ ] $0 running cost
