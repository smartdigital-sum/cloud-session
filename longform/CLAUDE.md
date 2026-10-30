# Long-form faceless YouTube scripts: project rules
Separate project from the reels at the repo root and from ncert-history/. Ignore the root reel rules (40s, 9:16, scene tables) here.

- Workflow (ScriptForge): 1. pick a sub-niche → 2. 10 video ideas → 3. full script. Never skip a step; wait for the user's choice.
- Length: 3–4 minutes, 450–600 English words (≈150 wpm), 16:9, faceless narrated video (2D animation / B-roll).
- Narration style by niche:
  - Self-improvement: calm, deep, motivational, second person ("you"), short punchy lines, deliberate pauses, empowering close, wise mentor.
  - Psychology: intriguing, slightly mysterious, authoritative; everyday examples, "Have you ever noticed…"; cite real studies accurately.
  - What if: cinematic, escalating, second-person immersion, timeline (seconds → days → years), real science pushed to the extreme.
  - Science: wonder-filled documentary narrator, vivid analogies, no hype beyond the evidence.
  - History: suspenseful storyteller, open mid-scene, real names/dates/places, mini-documentary tension.
- Structure: HOOK 0:00–0:15 (no "hey guys"/intro) → SETUP 0:15–0:40 (why it matters, open a curiosity loop) → MAIN BODY 0:40–3:00 (3–5 escalating beats, each ends on a mini-cliffhanger) → PAYOFF/TWIST 3:00–3:30 → OUTRO 3:30–4:00 (memorable line + comment/subscribe CTA tied to the topic).
- Format: section headers with timestamps, **[NARRATION]** to be spoken, **[VISUAL]** cue under each paragraph, (pause), *emphasis* and tone notes.
- After the script: 3 alternative titles, thumbnail text (2–4 words), 5 tags, word count + runtime, a voice direction table and a fact-check table with sources.
- Facts: never invent statistics, quotes or studies. Mark unverified facts with ⚠. If research is debated or failed to replicate, say so in the narration.
- Psychology/manipulation topics are framed for awareness and self-protection.
- Reel version: every video also gets a ~60s 9:16 reel: hook on screen + voice in the first 2s, timed scene table (time, visual, on-screen text, English VO), voice direction table, last scene loops back to the first and ends on a comment question. Same voice as the long video.
- Voiceover: every long video and reel gets English, Hindi and Assamese VO for Google AI Studio (Gemini TTS):
  - One Style instructions block + a Text block per section, per language; audio tags in English (e.g. [calm], [short pause]); same voice across all three languages.
  - Hindi/Assamese: natural spoken language, years written as words so TTS reads them correctly. Flag translations for native review.
  - AI Studio how-to and fixes: ../voice/google-ai-studio-tts.md (from a video folder: ../../../voice/google-ai-studio-tts.md).
- Layout: one folder per series (`<series-slug>/`, e.g. `productivity-focus/`, `cognitive-biases/`) holding README.md (video index + open fact checks), topic-ideas.md (mark ✅ with a link) and, once the series is done, publishing-kit.md. Inside it, one folder per video, `<NN>-<slug>/`, always with the same four files: long-video-script.md, long-video-voice.md, short-reel-script.md, short-reel-voice.md. List every series in the top-level README.md.
