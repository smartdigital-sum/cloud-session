# Making voiceovers in Google AI Studio

Google AI Studio's speech generation uses Gemini TTS (Gemini 3.1 Flash TTS was in preview as of mid-2026). You control it in two ways:
1. **Style instructions**: a plain-English description of how to speak (emotion, pace, accent).
2. **Audio tags** written inside the text in square brackets, e.g. `[whispers]`, `[excited]`, `[short pause]`.
   - Tags must be **in English**, even when the text is Hindi or Assamese.
   - Put a word or punctuation between two tags. Don't write two tags back to back.

## Step by step (first time)
1. Go to https://aistudio.google.com and sign in with your Google account.
2. Open **Generate speech** (it may be under "Playground", or appear as a speech/TTS model choice).
3. Choose the newest **TTS** model in the list (e.g. "Gemini 3.1 Flash TTS").
4. Set mode to **Single speaker**.
5. Choose a **voice** (see the table below) and the **language** if it asks.
6. Paste the **Style instructions** block from the prompt file into the style box.
7. Paste the **Text** block into the text box and click **Run / Generate**.
8. Listen. If one part sounds wrong, generate again (each run is slightly different), or generate only that scene's line.
9. **Download** the audio (WAV) and name it like `01-horn-ok-please_EN.wav`.

## Which voice for which reel type
Voice names come from Google's preset list. Preview 2–3 before choosing, because the list may change.
| Reel type | Try first | Also try | Why |
|---|---|---|---|
| Mystery / origin | **Puck** (upbeat) | Fenrir (excitable), Sadachbia (lively) | playful energy |
| Pride / heritage | **Sulafat** (warm) | Gacrux (mature), Charon (informative) | warm, rich, trustworthy |
| Science / why | **Charon** (informative) | Iapetus (clear), Kore (firm) | clear and confident |
| Myth-busting | **Fenrir** (excitable) | Puck, Zubenelgenubi (casual) | cheeky, fast |

Use **the same voice for all three languages** in a reel so the brand feels consistent. Also keep the same voice per series.

## Language notes
- **English:** add "Indian English accent" to the style instructions so it sounds local.
- **Hindi:** supported. Ask for "natural conversational Hindi, not news-anchor Hindi."
- **Assamese:** ⚠ not confirmed in Google's supported-language list. **Test it first** with just the hook line:
  - If it sounds natural, use it.
  - If the pronunciation is wrong (e.g. it sounds Bengali), record the Assamese track **yourself** using the delivery notes, or ask a native-speaker friend. Don't publish a bad Assamese voice, since Assamese viewers will notice right away.
- Numbers: if a year or number is read wrongly, write it out in words in that language and generate again.

## Fixing common problems
| Problem | Fix |
|---|---|
| Sounds flat or robotic | Add more emotion words to the style instructions ("very expressive, big pitch changes"), and add `[excited]`/`[curious]` tags |
| Too slow for 40s | Add "brisk pace, about 160 words per minute" to the style instructions |
| A tag is spoken aloud | Remove that tag or swap it for a simpler one (`[whispers]`, `[excited]`, `[laughs]`, `[short pause]`) |
| Wrong pronunciation of a name | Spell it the way it sounds, e.g. "Bez-ba-ro-a" |
| Voice changes between runs | Generate the whole reel in one run, then only re-do single lines if needed |

## Timing check
After downloading, check the total length. The target is **38–40 seconds**. If it runs long, cut words from the text (not the scenes), or ask for a faster pace.
