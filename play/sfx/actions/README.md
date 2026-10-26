# V2 sounds for new actions

These eight new-action additions were selected and authorized by the owner on 23 October 2026. They use the V2 real-material and richer arcade identity. No current sound identity
or sample is replaced. The owner subsequently authorized a volume-only balance pass
because normal placement was too quiet against the new rewards. Notes, waves, envelope
shape, timing, supplied files and music remain preserved.

| File                                        | New action                                        |
| ------------------------------------------- | ------------------------------------------------- |
| `select.mp3`                                | An actual change in selected card                 |
| `hand-ready.mp3`                            | Next Hand becoming available, once per transition |
| `menu.mp3`                                  | An actual menu/sheet transition                   |
| `tab.mp3`                                   | An accepted tab change                            |
| `combo-3.mp3`, `combo-5.mp3`, `combo-8.mp3` | Sparse earned combo milestones                    |
| `new-best.mp3`                              | A confirmed new personal best                     |

The current placement sound still plays on combo moves. New milestone accents are
optional additions alongside it, never replacements. Existing pile and celebration
sounds take priority; callers suppress or cancel these new additions while those play.
No voices, per-digit ticks, new placement cue or sound on every button is included.

## Sound and delivery

The files come from the finished V2 source kit under
`C:/Users/Wynter/Videos/Tricky Piles/Sound Preview/v2-candidates`. They match the final
`v2-new-actions` listening audition: each receives its shared +4.54 dB preview master
gain before delivery. The authorized mix constants in `src/audio/mix.ts` then raise
the entire existing placement envelope by 6 dB and trim new combo 3/5/8 by 2/3/4 dB,
and new best by 3 dB. Other new routines remain at unity. All other Synth, pile shine,
victory and music gains remain unchanged. MP3 encoding uses libmp3lame quality 2,
48 kHz stereo. All eight files together
are 50,832 bytes; the preview mix measured -23.98 LUFS integrated and -9.46 dBTP. Individual
short cues retain the intended routine/reward hierarchy rather than identical peaks.

The level comparison is under
`C:/Users/Wynter/Videos/Tricky Piles/Sound Preview/balance`. Normal placement's 70 ms
active RMS changes from -32.97 to -26.97 dBFS, with the identical waveform scaled
uniformly. The 12-second after mix with unchanged music peaks at -6.55 dBTP encoded.
A collision stress render adds the unchanged celebration over the rapid placement,
combo and replacing-pile sequence and peaks at -3.75 dBTP encoded. Both have zero
full-scale samples. No global normalization, master compression or limiter is applied;
short-cue identity and dynamic shape remain intact. These measurements establish
headroom rather than subjective phone/headphone quality.

`ActionAudio` uses one lazy, gesture-resumed Web Audio context and caches each decode.
Sound/foreground and caller priority gates are checked at request time and again after
decode/resume. Cancellation invalidates pending requests. New rewards outrank routine
new cues; newer equal-priority cues replace older ones, with at most one current cue and
one 15 ms release tail. These policies concern this new channel only and cannot stop
or attenuate existing Synth or music audio.

## Provenance and supply limits

`provenance.json` records exact local source paths and SHA-256 hashes, delivered asset
hashes, source component names and notes. The source components are:

- Recorded card pickup from the owner's local Sonniss GDC 2026 / 344 Audio Casino Cards
  library, used for selection/readiness material.
- Click, swipe and crystal textures from the owner's local Quute UI sound pack.
- Original procedurally authored damped/modal mallet, harmonic and body layers. Reward
  phrases share a D-major family with short bounded stereo reflections.

The local recordings were supplied through the owner's asset collection. This document
does not claim ownership of those libraries or grant an independent redistribution
license. Original library license terms remain applicable and should accompany the
owner's licensing records. Original sample/library files are unchanged. The existing
placement test from the V2 preview kit is deliberately excluded from delivery.
