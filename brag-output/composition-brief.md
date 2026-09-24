# Hyperframes Composition Brief: Clueless

## Objective
Create a short launch-style brag video for Clueless.

## Output
- Composition directory: `brag-output/composition/`
- Rendered video: `brag-output/brag.mp4`
- Format: landscape — 1920x1080
- Duration: 20 seconds

## Source Material
- Project root: `/workspace`
- Primary files read: `README.md`, `src/app/page.tsx`, `src/app/globals.css`, `src/components/ChatWidget.tsx`, `src/lib/seed-data.ts`, `src/app/layout.tsx`
- Product name: Clueless
- Tagline / strongest claim: Your digital closet. Weather-aware, style-driven outfit recommendations. / What to wear today?
- Key UI or visual moment to recreate: Daily pick hero card with weather chip, garment chips, “I’m wearing this” CTA; closet cards; Clueless stylist FAB/chat
- Copy that must appear verbatim:
  - As if!
  - What to wear today?
  - I’m wearing this
  - Hey! I’m your Clueless stylist…
  - Clueless
  - Your digital closet. Daily picks, tuned to the weather.

## Creative Direction
- Tone preset: default
- Creative direction: playful Cher wink meets clean app-store product demo
- Interpretation: warm readable product demo; humor only from As if! and dressing panic
- Angle: Daily “what to wear” panic solved by a weather-tuned pick from your own closet
- Hook: As if! → What to wear today?
- Outro / punchline: Clueless + daily picks tagline + muted As if!
- Avoid:
  - Generic SaaS language
  - Abstract filler visuals
  - Unrelated visual redesign

## Visual Identity
- Background: `#fafaf9`
- Text: `#1c1917`
- Accent: `#ea580c`
- Display font: Outfit (local @font-face or Google Fonts file shipped)
- Body font: DM Sans
- Visual references from the project: stone surfaces, white cards, orange CTAs/pills, sticky header wordmark, FAB chat

## Storyboard
Use `brag-output/brag-plan.md` as the creative contract.

Scene summary:
1. Hook — 2.5s — As if! slam
2. Reveal — 3.0s — Clueless header + What to wear today? + weather chip
3. Daily pick — 5.5s — 3 garment chips + I’m wearing this click
4. Closet + stylist — 5.0s — 4 closet cards + stylist panel
5. Outro — 4.0s — Clueless logo + tagline

## Audio
- Audio role: warm bed
- Audio arc: bed under UI demos; soft clicks; logo hit; fade
- Music: `happy-beats-business-moves-vol-1-by-ende-dot-app.mp3`
- Music treatment: volume ~0.32; fade under final logo ~1.2s
- Music cue guidance: bundled preset `.agents/skills/brag/assets/music/cues/happy-beats-business-moves-vol-1-by-ende-dot-app.music-cues.json`; strong cues ~8.02 / 12.02 / 17.02
- Audio-reactive treatment: subtle; orange glow / card shadow breathe with RMS
- Audio-coupled moments:
  - Scene 1 — soft impact on As if!
  - Scene 3 — card slides for chips; click on CTA
  - Scene 4 — card slides; panel open
  - Scene 5 — logo land
- SFX selection guidance: prefer low HF risk interface/impact; card-slide-1 for chips
- SFX analysis guidance: `.agents/skills/brag/assets/sfx/sfx-analysis.md`
- Exact SFX choice: Hyperframes should choose after animation exists
- Audio files: copy music and selected SFX into `brag-output/composition/assets/`

## Hyperframes Instructions
Load hyperframes-core, hyperframes-animation, hyperframes-creative, hyperframes-keyframes, hyperframes-cli. /brag owns this workflow — do not enter the generic promo interview.

Requirements:
- Show real Clueless UI recreation (daily pick + closet + stylist)
- Keep all text readable
- 15–25 seconds total
- Include music/SFX
- Treat cue metadata as optional timing hints
- Run `hyperframes check` before render
- Ship local font files (Outfit + DM Sans) so lint passes font_family_without_font_face
- Download seed Unsplash images into composition assets (deterministic, offline render)
