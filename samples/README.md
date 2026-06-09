# Samples

Audio samples are gitignored. Source them and place in `samples/audio/` before building the Ableton set.

## Directory structure (once sourced)

```
samples/audio/
  tanpura/        Long looping drone samples (Sa-Pa or Sa-Ma)
  harmonium/      Multi-sampled harmonium (velocity layers, sustain)
  tabla/          Multi-velocity hit samples by bol (Dha, Dhi, Na, Ti, Ka, Ge)
  kartals/        Finger cymbal hits (open, closed, accent)
```

## Sourcing guide

### Tanpura
- **Swar Systems** (swar-systems.com) — free tier has tanpura loops
- **Indian Raga apps** — export loops from iTabla Pro or similar
- **Target:** 2-4 min loop, Sa-Pa tuning (root + fifth), no vibrato, clean room tone

### Tabla
Priority instrument — quality matters most for feel.
- **Deep Data Loops "Tabla Loops"** — commercial, high quality, multiple velocity layers
- **Samneet Singh tabla samples** — free, widely shared, good starting point
- **Swar Systems** — tabla sample library available
- **Target:** at minimum Dha, Dhin, Na, Ti, Ka, Ge at 3 velocity layers each

### Harmonium
- **Swar Systems Indian Harmonium** (free VST) — the easiest path
- **Freesound.org** — search "harmonium" for multi-sampled sets
- **Target:** full chromatic range, 2 velocity layers minimum, sustain + release sampled separately

### Kartals (finger cymbals)
- Any finger cymbal or small bell sample works
- **Freesound.org** search "kartals" or "finger cymbals"
- **Target:** open hit, muted hit, accent (3 samples minimum)

## Notes
- Match tanpura root to your harmonium root before building the set
- All samples should be 44.1kHz or 48kHz, 24-bit minimum
- Normalize samples to -6dBFS before importing to avoid clipping
