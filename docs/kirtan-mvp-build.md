# Kirtan Machine MVP — v0.1 "First Chant"

**Goal:** sit down at the Push, launch the set, and sing *Sri Ram Jai Ram* through a full Krishna Das-style arc — opening, kirtan, build, sudden stop, silence. Playable within three bench sessions.

**Scoping rules:**
1. **Thin.** Stock Ableton devices only. No Max for Live, no AI, no vinyl. Everything in [rehearsing-the-crossing.md](rehearsing-the-crossing.md) that costs extra effort is deferred; everything that's free rides along.
2. **Every session ends playable.** No session builds infrastructure you can't chant over that day.
3. **The build is the Push course.** Each session teaches exactly one Push/Live skill. You're learning the instrument by building the instrument.

---

## The set — 4 tracks + 1 return

| Track | Type | Device | Stratum | Push skill it teaches |
|-------|------|--------|---------|----------------------|
| TANPURA | Audio | looping clip(s) | Ground | Session view, clips, launch/loop |
| TABLA+KARTALS | MIDI | one Drum Rack | Wheel | Step sequencing, velocity |
| HARMONIUM | MIDI | reed-organ patch → harmonium samples later | Voice (pitched) | Note mode, scale lock, playing |
| VOICE | Audio | mic in, no devices | Voice | Audio routing, monitoring |
| Return A | Return | Hall reverb (per system-design: ~30ms pre-delay, ~4s decay, low cut 200Hz) | — | Sends on encoders |

Kartals share the tabla Drum Rack (extra pads) — one fewer track to manage.

## The song — Sri Ram Jai Ram Jai Jai Ram

From the existing raga table: **root D, Push scale Minor.** Krishna Das plays this as a two-chord vamp:

- **Dm (i) ↔ C (bVII)** — one chord per 8-beat cycle to start. That's the whole harmony.
- Chant: *Sri Ram Jai Ram Jai Jai Ram* — call and response are the same line; solo, you sing both.
- Reference feel: KD's "Sri Ram Jai Ram" — starts ~80 BPM, spacious; ends ~110+ at full energy.

---

## Session 1 — The Ground and the Wheel (~60–90 min)

*Skill: session view, clips, the Push step sequencer.*

1. New Live set. Tempo 80. Save as `set/kirtan-mvp.als`.
2. **TANPURA:** drop one D tanpura loop (see samples/README.md) into an audio clip. Loop on, launch quantization None, warp off (it's a drone — let it run free of the grid). Launch it. That's the Ground: it never stops for the rest of the build.
3. **TABLA:** MIDI track, Drum Rack. Load tabla hits onto pads: Ge (bass), Na, Ti, Ka minimum; kartal open/closed on two spare pads. Dha = Ge+Na struck together.
4. **Program the keherwa** on the Push step sequencer — one bar, 8 steps. This is where the theory rides free: khali (beat 5) is just how you set the velocities.

| Step | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 |
|------|---|---|---|---|---|---|---|---|
| Bol | **Dha** | Dhi | Na | Dha | **Na** (khali) | Ti | Na | Ka |
| Pads | Ge+Na | Ge+Ti | Na | Ge+Na | Na only — **no bass** | Ti | Na | Ka |
| Velocity | 110 | 90 | 70 | 95 | 60 | 65 | 70 | 80 |

   Sam (1) is the fullest stroke; khali (5) drops the bass hand. The cycle breathes without you doing anything else.
5. Duplicate the clip twice → edit into **soft** (steps 1, 4, 5, 8 only, lower velocities) and **accented** (add flams/doubles on 7-8). Three intensity clips, as per system-design.
6. Lay out 4 scenes and name them with tempos (Live reads tempo from scene names):
   - `1 OPENING 80 BPM` — tanpura + soft tabla
   - `2 KIRTAN 88 BPM` — tanpura + medium tabla
   - `3 BUILD 104 BPM` — tanpura + accented tabla + kartals
   - `4 STOP` — **empty clip slots with Stop buttons on TABLA** (tanpura keeps running)
7. **Play:** launch scenes 1→4 in order. You have the arc and the sudden stop already — scene 4 *is* [issue #5](https://github.com/tkrazik-maya/kirtan-push/issues/5), for free.

**Session 1 ends:** drone + breathing cycle + energy arc + sudden stop, launchable from the Push.

## Session 2 — The Voices (~60–90 min)

*Skill: Note mode, scale lock, playing melody; mic routing.*

1. **HARMONIUM:** MIDI track. Browser-search "reed" / "organ" in Live's library and pick the breathiest reed-organ preset as a placeholder (swap for the Swar Systems harmonium or a Freesound multi-sample later, per samples/README — the set doesn't care).
2. On Push: Note mode → Scale → **D Minor, In Key**. Now no wrong notes exist. Find the vamp:
   - **Dm:** root pad + 2 pads up + 2 more up (stacked thirds land under three fingers in In-Key layout)
   - **C:** same shape, one scale-step down
   - Practice: hold Dm for one 8-beat cycle, C for the next, back. That alternation is the whole song.
3. **VOICE:** audio track, input from the Shure mic channel, monitoring In, no devices. Send generously to Return A.
4. **Monitor on speakers, not headphones.** The mic hears the room and the tanpura bleed — that's by design (spill is absorbency; the room sings too).
5. **Play:** scene 2, vamp Dm↔C with the right hand, sing *Sri Ram Jai Ram*. Sing the call, sing the response. This is the first chant on the instrument.

**Session 2 ends:** you can play and sing the kirtan.

## Session 3 — The full arc (~45–60 min)

*Skill: encoder mapping, performance flow.*

1. Map encoders per system-design: reverb send, harmonium vol, tabla vol, kartal vol (4 spare).
2. Touch strip: master reverb send (right-strip behavior per system-design; skip pitch bend for now).
3. **Rehearse the crossing, end to end (~12–15 min):**
   - Silence → launch TANPURA alone, let it sit a minute (Ground)
   - Scene 1: soft cycle enters, begin the chant low and spacious
   - Scene 2 → 3: energy and tempo climb, kartals in, voice fuller
   - Peak: hold it longer than feels comfortable
   - **Scene 4: the sudden stop.** Tabla and voice cease together; tanpura and reverb tail ring
   - Fade the tanpura by hand (encoder, slow). Then: **don't touch anything for 30 seconds.** The silence after is the point of the whole rig — treat it as part of the set.
4. Record the whole pass (Live's global record). First session capture, day one of the archive.

**Session 3 ends:** the MVP is done. You can perform a complete kirtan arc solo.

---

## Theory → practice map

Where each idea from [rehearsing-the-crossing.md](rehearsing-the-crossing.md) actually lands:

| Theory | Where it lives in the MVP | Cost |
|--------|---------------------------|------|
| Three strata (Ground/Wheel/Voice) | The track layout itself | Free |
| Khali / the breathing cycle | Velocities in the Session-1 drum programming | Free |
| The sudden stop | Scene 4 stop buttons | Free |
| Music without edges / spill | Speakers-not-headphones monitoring choice | Free |
| The silence after | 30-second performance rule after the stop | Free |
| Living tanpura (3 incommensurate loops) | **v0.2** — [issue #2](https://github.com/tkrazik-maya/kirtan-push/issues/2), ~20 min, same skills as Session 1 | Cheap, deferred |
| Accumulate-and-decay voice looper | **v0.3** — [issue #4](https://github.com/tkrazik-maya/kirtan-push/issues/4), only after the arc is comfortable | Deferred |
| Exact Bhairavi scale (M4L) | Deferred — D minor / Phrygian native scales are fine for KD repertoire | Deferred |
| Reincarnation (RAVE), call-and-response AI, vinyl ancestors | **sonic repo**, not this rig | Out of scope |

The pattern: the philosophy's structural ideas were free all along — they're just *how you build it right the first time*. The expensive ideas wait until the instrument has earned them.

## After v0.1

- **v0.2** (each ~20–30 min, any order): living tanpura (#2) · kartal accent one-shots on spare pads · second song: *Om Namah Shivaya*, root D, Push scale Phrygian (same set, new scenes)
- **v0.3:** the voice looper (#4) — the accumulate/decay engine
- **Then** revisit [Push layout properly](https://github.com/tkrazik-maya/sonic/issues/17) — from what your hands actually reached for, per the sonic-profile rule: layout emerges from play, not paper.
