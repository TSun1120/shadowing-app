# Shadowing App · 跟读练习

A single-file browser app for shadowing practice — built by a non-native English learner, for non-native English learners.

> **Live demo:** [https://tsun1120.github.io/shadowing-app/shadowing-app.html](https://tsun1120.github.io/shadowing-app/shadowing-app.html)

---

## Why I built this

I'm a credit analyst with 6 years of professional English writing experience. I can write reports and present to committees — but casual, expressive spoken English never came naturally.

I wanted a tool where I could:
- Download YouTube videos of native speakers I actually enjoy listening to
- Practice shadowing sentence by sentence, at my own pace
- See a visual comparison of my rhythm vs. the original
- Collect phrases that felt natural and practice them repeatedly

I couldn't find exactly what I needed, so I built it.

---

## Features

- **Sentence-by-sentence shadowing** — navigate subtitles, record yourself, compare instantly
- **Rhythm comparison chart** — energy envelope overlay (your recording in orange, original in blue)
- **Pitch / intonation curve** — visualize tone contour side by side
- **Rhythm score (0–100)** — DTW-based similarity score per sentence
- **Attempt counter** — tracks how many times you've practiced each sentence
- **Favorites** — star sentences to build a personal review list
- **Word-level subtitle bar** — feel the natural pause between words
- **Playback speed control** — slow down the original to catch details
- **Download audio segments** — export original or your recording as WAV for external review
- **PWA support** — installable on mobile (Android & iOS)
- **Runs entirely in the browser** — no server, no login, no data sent anywhere

---

## How to use

**Option 1 — Open directly (desktop)**
Download `shadowing-app.html` and open it in Chrome or Edge.

**Option 2 — Use the hosted version (mobile-friendly)**
Open the live demo link above on your phone and tap "Add to Home Screen".

**Workflow:**
1. Download a YouTube video as audio (e.g. with [yt-dlp](https://github.com/yt-dlp/yt-dlp))
2. Get or generate an SRT subtitle file (e.g. from YouTube auto-captions)
3. Load both into the app
4. Pick a sentence → listen → record yourself → compare

---

## Tech

Single HTML file. No build step, no dependencies, no backend.

- Web Audio API — recording, waveform analysis, envelope extraction
- DTW (Dynamic Time Warping) — rhythm similarity scoring
- Autocorrelation-based pitch detection
- localStorage — all progress saved locally in your browser

---

## Roadmap ideas

- [ ] Spaced repetition review queue (prioritize low-score sentences)
- [ ] Auto-transcription via Whisper API
- [ ] Session streak / progress calendar
- [ ] Export practice data

Feedback and suggestions welcome — open an issue or start a discussion.
