# Animated stories (Blender): project rules
This is a separate project from the reels at the repo root and from ncert-history/. Ignore the root reel rules (40s, trilingual VO tables, reel types) here.

- Short 3D animated story films made in Blender by a solo creator for an Indian audience.
- Format: vertical 9:16, 1080×1920, 24 fps, 1:30–2:30 long (must stay under 3:00 so it counts as a YouTube Short / Instagram Reel).
- Hook in the first 3 seconds: start in the middle of the most dramatic moment, then cut back. No logo or intro; the channel logo goes on the end card only.
- End card: one question or "tag someone" call to action, tied to the story's theme.
- Keep dialogue light: at most ~15 short lines per film. The story must make sense with the sound off (burned-in subtitles). This keeps lip-sync work small and makes dubbing cheap.
- Languages: Hindi dialogue is the main track, with English subtitles. Every dialogue line also gets an Assamese version, flagged ⚠ for native review. Any on-screen text that is part of the story (notes, letters) is a swappable image texture, one per language.
- Cast: at most 3 on-screen characters per film. Reuse existing rigs, sets and props before building new ones.
- Asset IDs: char_*, set_*, prop_*, fx_*. List new assets in the story's blender-production.md.
- Folder layout: animated-stories/stories/NN-<slug>/ with:
  - story-bible.md: logline, theme, characters, world, colour script, beat sheet
  - shot-list.md: shot-by-shot script (shot, time, frames, camera, action, dialogue HI/EN, sound) plus the dialogue sheet in HI/EN/AS
  - blender-production.md: assets, pipeline, settings, schedule, checklist
  - sound-and-voice.md: voice casting, Google AI Studio scratch-voice prompts, music and SFX cues
  - publishing.md: titles, description, hashtags, thumbnail, release plan
- Respect: treat religion and mythology with reverence (never make a deity the butt of a joke). No caste, religion or regional stereotypes. Elders are shown with dignity, even in comedy.
- Mark unverified facts or untested tools with ⚠.
- Music: royalty-free or commissioned only. Never use film songs, because Content ID claims will block or demonetise the video.
- Voices: real people for children and for the emotional lines where possible. Google AI Studio (Gemini TTS) is for scratch tracks in the animatic and for adult side characters.
- Don't commit .blend files, renders or audio to this git repo. Keep them in the local project folder and back them up to Google Drive.
