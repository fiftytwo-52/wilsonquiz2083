# 🔬 Wilson Science Quiz 2083

A self-contained, projector-friendly quiz app for **Wilson Academy's** inter-house science championship — built as a single HTML file with zero frameworks and zero build steps. Open it in a browser, press **Let's Play!**, and run the whole show from your desktop.

> **213 questions · 8 rounds · 2 tracks** — [Jump to the format →](#quiz-format)

---

## ✨ Features

- **Junior & Senior tracks** with their own question banks (92 + 121 questions) and rules
- **Full-viewport question boards** with big, tappable number tiles — designed for projectors and touch screens
- **Gold / Diamond / Platinum tier theming** across the Gambling round, from the tier picker down to the question stage
- **Audio Visual round** with image questions and video-first YouTube reveals: play the clip, run the countdown, then reveal the answer (the video pauses itself on reveal)
- **Built-in timer** with ring progress, ticking, and a buzzer when time is up — 30 s for general rounds, 10 s for Audio Visual (40 s for the senior AV bonus question), 60 s for Rapid Fire
- **Suspense background music** that starts with the show and politely mutes itself during Audio Visual questions
- **Rules overlay** with the official senior-quiz rules
- **Keyboard-driven hosting**: jump between questions, restart timers, reveal answers, and throw emoji stickers without touching the mouse
- **Responsive & accessible**: works on laptops, tablets, and narrow screens; respects `prefers-reduced-motion`

## 🎯 Quiz format

| Round | Format |
|---|---|
| Biology · Physics · Chemistry · Geology & Astronomy · Miscellaneous | 8 questions each · 10 marks (5 if passed) · 30 s |
| Audio Visual | Image/video identification · buzzer round · **−5 for a wrong answer** · 10 s (40 s for senior Q9) |
| Rapid Fire | Sets A–D · 15 questions per set · 60 s · no negative marking |
| Gambling | Gold (5) · Diamond (10) · Platinum (15) marks · equal negative marks for wrong answers · teams may skip |

The in-app **Rules** panel (Senior track) carries the full official wording.

## 🚀 Quick start

No install, no build — it's just a web page.

```bash
# Option 1 — open directly
open index.html          # macOS
xdg-open index.html      # Linux
# ...or just double-click index.html

# Option 2 — serve locally (avoids any file:// quirks)
python3 -m http.server 8000
# then visit http://localhost:8000
```

Tested in current Chrome, Edge, and Firefox.

**Optional music:** `quiz-show-suspense.mp3` sits next to `index.html` and loads on demand — delete it and the app runs silently.

## ⌨️ Keyboard shortcuts

| Key | Action |
|---|---|
| `A` | Show / hide the answer |
| `R` | Restart the timer |
| `←` / `→` | Previous / next question |
| `Space` | Throw a random emoji sticker 🎉 |
| `Esc` | Close rules / return to the question board |

## 📁 Project structure

```
├── index.html                  # The entire app (HTML + CSS + JS + question banks)
├── logo.png                    # Wilson Academy crest
├── quiz-show-suspense.mp3      # Optional background music
├── images/                     # Audio Visual round images (alt-text filenames)
├── pdfs/
│   ├── wilson-quiz-junior-qa.pdf   # Junior rules + all Q&A
│   └── wilson-quiz-senior-qa.pdf   # Senior rules + all Q&A
└── README.md
```

## 📄 Q&A sheets

Print-ready question-and-answer sheets for both tracks live in [`pdfs/`](pdfs/) — rules included, handy for the quiz master and for post-show review.

## 🌐 Offline notes

Everything important (questions, styles, images, sounds) ships in the repo, so the quiz runs with **no internet connection**. Two features degrade gracefully online-only:

- **Web fonts** (Google Fonts) — falls back to system fonts offline
- **YouTube video questions** — need a connection to play

---

Built for the **Wilson Academy Science Quiz 2083** · [Repository](https://github.com/fiftytwo-52/wilsonquiz2083)
