# खनक · KHANAK: sound and voice
In this film, sound carries the story. Viewers who catch the bangle sound in S14 will rewatch it, and say so in the comments.

## 1. Casting
| Role | Best option | Backup | Why |
|---|---|---|---|
| **Dadi** | A real grandmother: your own dadi, nani or aita, or a neighbour's | An adult woman doing a gentle, older voice | Real age in a voice can't be faked. If it's your own grandmother, the recording session makes a great behind-the-scenes reel |
| **Chhotu** | A real child aged 8–11 (a nephew, niece or neighbour's kid), with a parent present and their consent | An adult who does a convincing kid voice | ⚠ AI voices are adult voices, and an adult voice pitched up sounds strange |
| **Gupta-ji** | Any adult man | Google AI Studio voice (one line only) | |

**Recording kids:** don't make them read. Say the line, let them repeat it, and make it a game. Record 5–6 takes of each line. Short sessions (15 minutes) and a reward afterwards work best. Recording tips for the room and the phone are in `voice/voice-direction-guide.md` §4 (repo root).

## 2. Line-by-line direction
Notation follows `voice/voice-direction-guide.md`: `/` breath, `//` pause, **bold** stress, ↑ pitch up, ↓ pitch down.

| # | Shot | Speaker | Line | Emotion | Delivery |
|---|---|---|---|---|---|
| 1 | S05 | Chhotu | बस थोड़े दिन और… | 😌 dreamy | A whisper to himself, with a smile in it. Trail off on "और…" |
| 2 | S07 | Dadi | ज़रा सुई में धागा डाल दे, छोटू। | 🙂 casual | Mildly fed up with the needle, never with him. Throwaway, like she says it every day |
| 3 | S08 | Chhotu | दादी, नया चश्मा? | 🤔 innocent | Light question ↑, not a complaint |
| 4 | S08 | Dadi | चल जाएगा। | 😄 breezy | Quick and bright, brushing it off. **This is a habit**: she has said it a thousand times. Remember this exact tune, because line 14 copies it |
| 5 | S12 | Chhotu | दादी! नमक! | 😝 spluttering | A coughing laugh in the middle of a sip |
| 6 | S12 | Dadi | हैं? / चीनी ही तो है… | 😅 confused | A real "huh?", then a giggle as she realises |
| 7 | S15 | Chhotu | इतनी जल्दी? | 🤨 puzzled | Half to himself, ↑ on "जल्दी" |
| 8 | S18 | Dadi | (small laugh) / चल जाएगा। | 🙂 covering | **The same words as line 4, but slower and softer.** She's covering embarrassment. The audience should feel the difference |
| 9 | S22 | Dadi (VO) | छोटू के बैट के लिए… | 🥹 tender | Close to the mic, almost a whisper, like reading a letter aloud to herself |
| 10 | S25 | Gupta-ji | बैट नहीं? | 🤨 kind surprise | An eyebrow-raise in the voice ↑ |
| 11 | S25 | Chhotu | दादी का चश्मा। | 💪 sure | Simple and firm, with no hesitation. He has decided |
| 12 | S28 | Dadi | अरे… // तू तो **बड़ा** हो गया रे। | 😢 wonder | Breathless and slow, her voice catching on "बड़ा" ↓ |
| 13 | S29 | Dadi | पगले… / और तेरा बैट? | 😂😢 laugh-cry | She tries to scold him and her voice breaks into a laugh |
| 14 | S29 | Chhotu | चल जाएगा। | 😁 cheeky | **Copy Dadi's breezy tune from line 4 exactly**, like a kid doing an impression of his grandmother. This is the button of the film |

Assamese lines are in `shot-list.md` (dialogue sheet). Use the same direction. ⚠ Get a native speaker to check them before recording.

## 3. Scratch voices in Google AI Studio (for the animatic)
Use these to time the animatic in week 1, then replace them with real voices. Step-by-step setup is in `voice/google-ai-studio-tts.md` (repo root).
1. Open **Generate speech** and choose **Multi-speaker**.
2. **Speaker 1** name: `Dadi`. Voice: **Sulafat** (warm). Also try Gacrux (mature) or Vindemiatrix (gentle).
3. **Speaker 2** name: `Chhotu`. Voice: **Leda** (youthful). Also try Laomedeia (upbeat). ⚠ These are adult voices; fine for timing, not for the final film.
4. Paste the style instructions and the text below. Generate. Download as `khanak_scratch_HI.wav`.

### Hindi: Dadi and Chhotu

**Style instructions**
```
A tender, funny Indian family short film. Dadi is a warm grandmother of about 70 who laughs at herself and always says "chal jayega" to brush off her own needs. Chhotu is her 8-year-old grandson, cheerful and cricket-mad. Natural, conversational Hindi from a small Indian town, not formal and not filmy. Leave natural pauses between lines. Dadi's last lines are emotional: wonder, then a voice breaking into laughter. Chhotu's final "chal jayega" copies Dadi's breezy tone from earlier, like a cheeky impression.
```

**Text**
```
Chhotu: [whispers] बस थोड़े दिन और…
Dadi: ज़रा सुई में धागा डाल दे, छोटू।
Chhotu: [curious] दादी, नया चश्मा?
Dadi: [cheerfully] चल जाएगा।
Chhotu: [coughing] दादी! नमक!
Dadi: [confused] हैं? चीनी ही तो है… [laughs]
Chhotu: [puzzled] इतनी जल्दी?
Dadi: [softly] चल जाएगा।
Dadi: [whispers] छोटू के बैट के लिए…
Chhotu: दादी का चश्मा।
Dadi: [emotional] अरे… तू तो बड़ा हो गया रे।
Dadi: [laughing and crying] पगले… और तेरा बैट?
Chhotu: [cheekily] चल जाएगा।
```

### Gupta-ji (single speaker)
Voice: **Algenib** (gravelly) or Charon.

**Style instructions**
```
A kind, middle-aged small-town Indian optician, gently surprised. Natural conversational Hindi. One short line.
```

**Text**
```
[surprised] बैट नहीं?
```

### Assamese
⚠ Assamese is not confirmed in the TTS language list (see `voice/google-ai-studio-tts.md`). Test line 4 ("চলি যাব।") first. If it sounds Bengali, record the Assamese scratch yourself. For the final film, use real voices.

## 4. Music cue sheet
Instruments: **bansuri** (Chhotu's theme), soft **tabla**, **strings** for the emotion, harmonium pads. Keep it small and acoustic, like a home.

| Cue | Time | Shots | Mood | Notes |
|---|---|---|---|---|
| M1 Hook | 0:00–0:08 | S01–S03 | Tension | A low drone and breath, a sting on the smash, silence on the freeze. Coin spin under the title |
| M2 Chhotu's theme | 0:08–0:35 | S04–S09 | Playful, dreamy | A simple 4–6 note bansuri melody, easy to hum, with light tabla |
| M3 Montage | 0:35–1:03 | S10–S15 | Bouncy, then curious | The same theme, faster. It **drops out completely** for the night shot S14 (crickets and fan only) |
| — | 1:03–1:09 | S16–S17 | — | The music stops on the stumble. **Total silence** after the crack |
| M4 Guilt and decision | 1:09–1:38 | S18–S23 | Sad, then resolve | A low cello note under his look, then solo bansuri, slow, the theme in a minor key. Strings enter at the note reveal |
| M5 The choice | 1:38–1:50 | S24–S25 | Held breath, then release | One held note while he stands between the shops; it resolves as he turns right |
| M6 Payoff | 1:50–2:15 | S26–S30 | Joy and tears | The full theme in a major key. Swell on the rack focus (S27). It drops away to leave the **two final clinks** almost alone |
| M7 Tail | 2:15–2:18 | S31 | Warm | The last soft note under the end card |

**Where to get music:** commission a local flautist (the best option, and truly yours), or use the YouTube Audio Library (check whether each track needs attribution) or other royalty-free libraries ⚠ (read the licence). **Never use a film song.**

## 5. SFX list
Most of these you can record at home with your phone. Recording them yourself sounds more authentic than a library.
| Sound | Shots | How to get it |
|---|---|---|
| Coin into a clay gullak (**the clink**) | S01, S06, S11, S14, S30 | Drop real coins into your real gullak. Record 20 takes and pick the crispest |
| Gullak rattle, thin and heavy | S06, S15 | Shake it with 5 coins, then with 60 |
| Gullak smash | S02, S21 | Smash your real gullak on a towel-covered floor (wear eye protection). Layer in a low thump |
| Coin cascade | S21, S25 | Pour coins onto a steel plate and onto glass |
| **Glass bangles (chhan-chhan)** | S07, S14, S23 | Borrow a set of glass bangles and record the arm movements. For S14, make it very quiet with reverb |
| Glasses crack | S17 | Snap a dry papad close to the mic and layer it with a small glass tap ⚠ (careful) |
| Chalk on a wall | S06 | Real chalk on a real wall |
| Chai spit-take, spoon in a steel glass | S12 | Record at home |
| Paper unfold, newspaper rustle | S13, S22 | Record at home |
| Night: crickets, ceiling fan | S14, S19 | Record at night by an open window |
| Bazaar ambience | S04, S24 | Record at your local market (keep a single voice from being clear and recognisable) |
| Stadium crowd (faint) | S05 | Royalty-free library ⚠ licence |

## 6. Mix
- Dialogue always sits on top. Duck the music under every line.
- **Silences are part of the score:** after the crack (S17), in the night mystery (S14), and before the last two clinks (S30). Don't fill them.
- Target about −14 LUFS integrated for YouTube and Instagram ⚠ (the commonly recommended level; check your final export with a loudness meter).
