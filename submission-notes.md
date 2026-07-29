# EYFI Ambassador Reward Ladder — Submission Notes

## Tools Used
- **Antigravity (Google DeepMind AI coding assistant)** — analysed the live EYFI and Ambassador websites to extract exact brand tokens, then generated and iteratively refined the full interactive page based on recruiter-level critique of each version.
- **Vanilla HTML + CSS + JavaScript** (zero dependencies, no build step) — instantly droppable into the existing Next.js / Vite site as a standalone page or embedded section.

## How I Did It
1. Fetched the live sites (`eyfichallenge.com` and `ambassador.eyfichallenge.com`) to extract exact design language: dark `#0A0A0A` background, `#FF6B1A` orange accent, `#DFF864` lime secondary, **Bricolage Grotesque** display font, **Space Grotesk** body font, animated marquee ticker.
2. Built six rich tier cards — each with its own accent color, per-card progress bar, perk list with sub-descriptions, cumulative-reward chips, and four distinct visual states: **Locked**, **Next Up**, **Unlocked**, and **Current tier** (with glow + subtle float).
3. Added milestone dots directly on the slider track that glow lime when reached — so at a glance you always know exactly which milestone you're sitting on. The track itself fills green up to your current count.
4. Simulated a backend fetch with a `setTimeout` (with a comment showing how to replace it with a real `fetch()` call) so the page boots with a pre-loaded count of 37, exactly as it would with real DB data — the slider jumps to that value and all cards reflect it automatically.

## File
`reward-ladder.html` — open in any modern browser, no server needed.
