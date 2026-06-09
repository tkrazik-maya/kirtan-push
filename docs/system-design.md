# Kirtan Machine — System Design

Solo kirtan rig for Ableton Push 2.0. Neem Karoli / Ram Dass lineage.

## Core design principle

Tabla and tanpura run as triggered looping clips. Harmonium is played live over the top. You can't hold a harmonium note and play tabla simultaneously on one device — so rhythm is autonomous, melody is live.

## Track layout

| Track | Type | Role |
|-------|------|------|
| TANPURA | Audio | Sa-Pa drone, looping sample, start once at top of set |
| HARMONIUM | Instrument | Push melodic mode, scale-locked to raga |
| TABLA | MIDI / Drum Rack | Looping keherwa clips, 3 intensity levels |
| KARTALS | MIDI / Drum Rack | Looping or one-shot accents |
| RETURN A | Reverb | Hall reverb — all tracks send here |

## Scene structure (energy arc)

| Scene | Name | Tabla | Kartals | Feel |
|-------|------|-------|---------|------|
| 1 | OPENING | Soft keherwa | Off | Spacious, settling in |
| 2 | CALL/RESPONSE | Same | Off | Steady mantra |
| 3 | BUILDING | Slightly fuller | On | Energy rising |
| 4 | CLIMAX | Full keherwa | Full | Peak devotion |
| 5 | WINDING DOWN | Soft keherwa | Off | Return |
| 6 | CLOSING | Off | Off | Drone only, silence |

## Push 2.0 mode map

- **Session mode** — left pad half: launch scenes, trigger tabla clips, mute/unmute
- **Drum mode** (hold Shift + press Drum) — tabla accents and kartal live hits
- **Instrument mode** (hold Shift + press Note) — harmonium, scale-locked
- **Left touch strip** — pitch bend (meend-style glides on harmonium)
- **Right touch strip** — master reverb send
- **Encoders 1-8** — reverb depth, harmonium vol, tabla vol, kartal vol, (spare x4)

## Tabla keherwa pattern (8-beat)

```
Beat:  1    2    3    4    5    6    7    8
Bols:  Dha  Dhi  Na   Dha  Na   Ti   Na   Ka
```

Program three clips per tempo: **soft** (sparse), **medium** (full pattern), **accented** (fills).

## Ragas and Push scale settings

| Kirtan | Root | Push scale | Notes |
|--------|------|-----------|-------|
| Ram Ram / Sri Ram Jai Ram | D | Minor | Standard bhakti feel |
| Om Namah Shivaya | D | Phrygian | Bhairavi approximation (b2 is key) |
| Hare Krishna | G | Minor | |
| Jai Ma | C | Minor | |

For exact Bhairavi (1, b2, b3, 4, 5, b6, b7): use a Max for Live scale-lock device to set custom intervals — Push 2's built-in scales don't cover it precisely.

## Effects

- Hall reverb (Return A): long pre-delay (~30ms), long decay (~4s), low cut at 200Hz
- No compression on harmonium — let the natural dynamics breathe
- Light saturation on tabla for warmth (optional)
