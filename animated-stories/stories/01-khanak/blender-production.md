# खनक · KHANAK: Blender production plan
Written for a solo creator at beginner-to-intermediate level. ⚠ Menu names can shift a little between Blender versions. If something isn't where this says, search for it with F3.

## 1. Software (all free)
| Job | Tool | Note |
|---|---|---|
| Everything 3D, plus storyboard and animatic | **Blender 5.2 LTS** | Released 14 July 2026 and supported until July 2028. Use **one version for the whole film**, because upgrading halfway can break rigs |
| Textures, the handwritten note, signboards | Krita or GIMP | Write the note with a mouse or your left hand so it looks shaky |
| Audio clean-up | Audacity | |
| Final edit, subtitles, colour | DaVinci Resolve, or Blender's Video Sequencer | |
| Reference photos | Your phone | Buy a real clay gullak (cheap at any potter or mela ⚠ price varies): use it for reference, record its sounds, and smash it for the SFX |

## 2. Project folder (on your computer, not in git)
```
KHANAK/
  01_ref/            photos, the gullak sounds, your acting videos
  02_animatic/       khanak_animatic.blend, animatic.mp4
  03_assets/
    chars/           char_chhotu.blend, char_dadi.blend, char_gupta.blend
    sets/            set_home.blend, set_bazaar.blend, set_school_gate.blend
    props/           props.blend (all small props in one file)
    textures/        note_HI.png, note_EN.png, note_AS.png, signs, labels
  04_shots/          sq01_hook.blend, sq02_home.blend, sq03_bazaar.blend ...
  05_render/         S01/0001.png ... S31/
  06_audio/          voice/, sfx/, music/
  07_edit/           khanak_HI.mp4, khanak_AS.mp4, khanak_EN.mp4
```
- Characters, sets and props live in their own asset files. Shot files **link** them (File > Link), then make a Library Override for anything you animate. Fix a character once and every shot updates.
- Back up `KHANAK/` to Google Drive at the end of every working day.

## 3. Asset list
Priority A means it's needed in many shots, so build it first and best. Priority C can be rough.

### Characters
| ID | What | Priority | Build notes |
|---|---|---|---|
| char_chhotu | Boy, 8, 3.5 heads tall | A | Big head and eyes, a gap in the front teeth, sculpted hair mesh, school shirt, shorts, wrist thread. Face: blink, brows, 6 mouth shapes. Needs a version without the school bag |
| char_dadi | Grandmother, ~70, 4.5 heads tall | A | Saree as a sculpted mesh (no cloth sim). A **pallu with 3–4 bones** so it can sway. Bangles as one object parented to each wrist. A pallu knot (a small bulge). Glasses as a separate object (see props) |
| char_gupta | Optician, ~55 | C | Used in **one shot**, from the chest up behind the counter, so there's no need to rig legs. Moustache, half-moon glasses, pen behind his ear |

### Sets
| ID | What | Priority | Seen in |
|---|---|---|---|
| set_home | Room plus kitchen corner (see story-bible §5) | A | S01–S03, S06–S09, S11–S23, S26–S30 |
| set_bazaar | Two shop fronts, the street, overhead wires | B | S04, S05, S24 |
| set_optician_counter | Glass counter, eye chart, shelves (can be inside set_bazaar) | B | S25 |
| set_school_gate | Green gate, wall, gola cart | C | S10 |

### Props
| ID | What | Notes |
|---|---|---|
| prop_gullak | Clay piggy bank (the classic round pot with a slot) | Model from your real one. Make three versions: whole, pre-fractured for the smash, and new (for S30) |
| prop_coins | ₹1, ₹2, ₹5, ₹10 coins | 4 simple models. Scatter copies for the piles |
| prop_hammer | Small hammer | |
| prop_note | Folded paper note | The texture is per-language (note_HI/EN/AS.png). Make folded and open states (shape keys) |
| prop_glasses_old | Brown frame, cracked left lens, taped bridge | Two versions: whole, and broken (lens in 5–6 pieces) |
| prop_glasses_new | Clean, the same shape | For S26–S29 |
| prop_plank_bat | Plank bat with a rubber-taped handle | |
| prop_red_bat | The dream bat on a stand, with a ₹500 tag | Glossy, slightly rim-lit. It should almost glow |
| prop_needle_thread | Needle and thread | Thread as a curve object |
| prop_newspaper | Folded newspaper | Use a simple bend modifier for the arm's-length shot |
| prop_chai_set | Steel tumbler, saucepan, spoon, jars labelled नमक and चीनी | |
| prop_charpai, prop_almirah, prop_fan, prop_bulb_zero, prop_calendar, prop_photo_dadaji | Room dressing | Find CC0 bases on Poly Haven or BlenderKit (check each licence), then restyle them |
| prop_hanky_bundle | Handkerchief tied around coins | |
| prop_register | Thick old register | Text texture per language |
| prop_gola_cart | Cart with syrup bottles | |
| fx_chalk_bat | Chalk drawing on the wall | A shader mask that fills from the bottom up (see §5 FX) |

## 4. Step-by-step pipeline
### Step 1: Story reel / animatic (week 1). Do not skip this.
1. File > New > **2D Animation**. Set the output to 1080×1920 at 24 fps.
2. Draw each shot from `shot-list.md` as 1–3 rough Grease Pencil frames. Stick figures are fine.
3. Put timeline markers at the frame numbers in the shot list.
4. Add a scratch voice (see `sound-and-voice.md`) and temp music in the Video Sequencer.
5. Export animatic.mp4 and show it to 5 people **without explaining anything** (see `research/audience-research.md` §4). Fix the story now.

### Step 2: Characters (weeks 2–3)
1. **Block out** with primitives (sphere head, capsule body) and check the silhouette in solid black. Is it instantly Chhotu? Is it instantly Dadi?
2. Model with a **Subdivision Surface** modifier. Put edge loops around the eyes, mouth, elbows, knees and shoulders, because those bend.
3. Keep it stylised: big eyes, simple hands (4 fingers is fine), no realistic skin. Toon-ish shading with a soft gradient looks great in EEVEE and hides imperfections.
4. Materials: flat base colours from the story bible (Dadi's saree #F2EAD8 with a maroon #7A1F2B border; Chhotu's shirt #8EC5E8, shorts #2E3A59), plus a little roughness variation.

### Step 3: Rigging (week 3)
1. Enable **Rigify** (Edit > Preferences > Add-ons). Add > Armature > Human (Meta-Rig), scale and fit it to each character, then click **Generate Rig**.
2. Parent the mesh to the rig with **automatic weights**, then fix the shoulders, hips and fingers in Weight Paint mode.
3. **Face, the simple way (recommended):** use **shape keys** instead of a full face rig.
   - Mouth: rest, A (open), E (wide), O (round), M/B/P (closed and pressed), smile, frown.
   - Eyes: blink_L, blink_R, squint (Dadi needs this a lot).
   - Brows: up, down, worried.
   - Drive them with custom bones or just key the sliders directly. With only 14 short lines, hand-keying is fine.
4. **Glasses:** a separate object with a **Child Of** constraint to the head bone. Switch the constraint influence to a hand bone for S08, S16 and S26.
5. **Pallu:** a chain of 3–4 bones. Animate them by hand with a slight delay behind the body (overlapping action), or try a jiggle/wiggle-bone extension ⚠ (test it first).

### Step 4: Sets and props (weeks 3–4)
- **Only build what the camera sees.** Look through each shot's camera before detailing anything.
- A vertical frame is **tall**: you will see the ceiling fan, the floor and the top of the walls. Dress the room top to bottom.
- Add wear everywhere: chipped wall paint, a scuffed floor, a faded calendar. Clean 3D looks fake; old details make it look Indian and lived-in.

### Step 5: Layout (week 4)
1. In each sequence file, add cameras following the shot list (lens and angle) and bind each camera to its marker (Ctrl+B in the timeline).
2. Turn on **Safe Areas** (Camera properties > Viewport Display). Keep faces in the top third and the bottom 20% clear for the app interface.
3. Use stand-in poses only. Play the full film in the viewport against the animatic audio, and check the timing before animating anything.

### Step 6: Animation (weeks 5–7)
1. **Animate the emotional shots first:** S27–S29, S18, S22, S19. If time runs out, these must be the best.
2. **Record yourself acting** each shot on your phone, and act Dadi too. Copy your own timing.
3. **Blocking:** key poses only, with stepped interpolation. Show the film to someone at this stage.
4. **Splining:** switch to Bezier and add in-betweens, eye darts and blinks (on head turns and before a new thought).
5. **Polish:** overlapping action (pallu, hair mop, bangles), and small breathing in held shots so nobody looks frozen.
6. **Lip sync:** key the mouth only on stressed syllables and hold the shapes slightly longer than feels natural. Turn faces away or use backs of heads where you can. S22 is a voice-over, so it needs no lip sync at all.

### Step 7: FX (week 7)
| Effect | Shots | How |
|---|---|---|
| Gullak smash | S02, S21 | Fracture prop_gullak into 10–15 pieces with **Cell Fracture** ⚠ (if it's not listed under add-ons, install it via Get Extensions) or cut the pieces by hand. Rigid Body sim, then **bake** it. S02 is in slow motion, so lower the rigid body world's Speed setting |
| Coins | S02, S21, S25 | A collection of coins as Rigid Bodies dropped onto the floor or counter. Bake it. Use about 80–150 coins, not thousands |
| Floating note | S02 | Animate it by hand and hold it at the freeze frame |
| Dadi's blurry POV | S09, S27 | A camera with **Depth of Field** on, a very low F-Stop (0.5–1.0) and the focus distance set far behind the subject. For S27, keyframe the focus distance onto Chhotu's face over about 8 frames (the rack focus) |
| Chalk bat fill | S06, S11, S30 (static in S15, S19) | The chalk is a texture on the wall. Mix it in with a **Gradient Texture** mask through a Map Range node, and keyframe the cut-off value so the fill rises from bottom to top |
| Breath fog on glass | S04 | A small plane with a Noise texture and alpha. Fade it in and out |
| Light shafts | S20–S23 | A **Principled Volume** box (density 0.02–0.05) around the window area, plus a strong sun lamp through the grill |
| Glasses crack | S17 | Swap prop_glasses_old for the broken version on the impact frame. Hand-animate the 5–6 lens pieces bouncing |

### Step 8: Lighting and rendering (week 8)
- **Engine: EEVEE** (fast). Turn on ray-traced reflections and shadows if your GPU can handle it, motion blur, and volumetrics only in the shots that need them.
- **Colour management:** AgX view (the default). Try the Look presets for contrast.
- **Output:** 1080×1920 at 24 fps, rendered as a **PNG image sequence** into `05_render/Sxx/`. If Blender crashes on frame 900, you keep frames 1–899.
- **Render-time sanity check:** 3,312 frames at about 10 seconds per frame is roughly 9 hours. Render overnight, one sequence at a time.
- Follow the colour script in story-bible §6. The night shots are **blue moonlight from the window plus the orange glow of the zero-watt bulb**; that pair of colours is the film's look.

### Step 9: Edit, sound and export (week 9)
1. Import the image sequences into Resolve (or Blender's Video Sequencer) at 24 fps.
2. Lay in the final voice, SFX and music (see `sound-and-voice.md`).
3. Burn in the subtitles: Hindi audio with English subtitles is the main version. Use a clear sans-serif font, white with a soft shadow, placed just below the centre of the frame.
4. Export **H.264 MP4, 1080×1920, 24 fps**, high bitrate. Make 3 versions: HI audio + EN subs, AS audio + EN subs, and EN audio + EN subs (optional).

## 5. Nine-week schedule
| Week | Goal | Done when |
|---|---|---|
| 1 | Animatic + scratch voice | 5 test viewers understood the story without help |
| 2 | Chhotu and Dadi modelled | Both silhouettes read instantly in black |
| 3 | Rigs + face shape keys | Both can walk, sit, grin, squint and say "चल जाएगा" |
| 4 | Home set, props, layout of all shots | The full film plays with stand-in poses and correct cameras |
| 5 | Animation: payoff and turning point (S16–S29) | Blocking approved |
| 6 | Animation: hook, Act 1 and montage (S01–S15) | Blocking approved |
| 7 | Polish all shots, lip sync, FX | Nothing looks frozen; the smash and the coins are baked |
| 8 | Lighting + rendering | All 31 shots rendered |
| 9 | Final voice, sound, subtitles, 3 language exports, thumbnail | Uploaded and scheduled |

If you're new to Blender, add 2–4 weeks at the start for learning: a beginner modelling course (Blender Guru's "Donut" series is the classic), then a Rigify character-rigging tutorial, then a Grease Pencil storyboarding tutorial.

## 6. Checklist before you render
- [ ] Every shot uses the timing from the final voice recording, not the scratch voice.
- [ ] Both of Dadi's POV shots are blurry, and only S27 snaps into focus.
- [ ] The bangle sound is set up clearly in S07 and is faint but present in S14.
- [ ] Chhotu's plank bat is visible in early shots, so the trip in S16 is set up.
- [ ] The chalk bat's fill level is continuous across shots: a thin strip in S06, rising through S11, then about 60% in S15 and S19. It tracks only Chhotu's own coins, which is why the pile in S21 is a surprise.
- [ ] The note texture is set to the right language for each export.
- [ ] Nothing important sits in the bottom 20% of the frame.
- [ ] Dadi is never shown in pain. She laughs, every time.
