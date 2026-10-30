# NCERT history videos: project rules
Separate project from the reels at the repo root. Ignore the root reel rules (40s, 9:16, trilingual) here.

- Long-form YouTube explainers, 1920×1080, Hindi voiceover, one NCERT chapter split across 1–2 videos (~10–13 min each).
- Folder layout: ncert-history/class<NN>-<subject>/ch<NN>-<slug>/video<N>-<slug>.md
- Script format (follow the existing episodes exactly):
  - Header: title, NCERT book/chapter/sections, format, scene count, estimated length at 2.35 words/s.
  - YouTube chapters block, then the scene-type legend.
  - Parts `## P<n> · Part <n>: <title>  _(NCERT <section>)_`, scenes `### Scene NNN · m:ss · \`type\` · ~Ns`.
  - Each scene: Hindi VO as a blockquote, then **On screen**, **Emoji**, **Art** (asset IDs or "none").
- Scene types: hook, chapter, stage, map, split, bar, line, pie, pyramid, flow, timeline, quote, pillars, checklist, symbols, counter, concept, quiz, outro.
- Art asset IDs: bg_wide_*, char_*, obj_*, map_*, scene_*. Reuse existing assets before inventing new ones; list any new ones.
- Every fact must match the NCERT textbook; don't add content outside the syllabus without flagging it.
- Show violence without gore or people (silhouettes, objects, fades).
- Structure: hook → chapter card → parts → EXAM KEYWORD cards for key terms → quick revision → timeline of dates → quiz → outro teasing the next video.
- Numbers and years in the VO are written as Hindi words (सत्रह सौ नवासी), so the voice reads them correctly.
