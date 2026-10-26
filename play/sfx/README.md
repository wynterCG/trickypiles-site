# Supplied sound effects

Sources were supplied by the project owner on 23 October 2026. Original files in Downloads
remain unchanged. Filenames record the supplied sources without an independent license claim.

- `pile-complete.mp3`: `benkirb-shine-11-268907.mp3`, trimmed from 0.161417 to 1.85 seconds
  with a 20 ms end fade. Its playback gain is 0.63 (4 dB quieter), layered with the original
  synthesized rise, impact, completion and stamp. A new pile interrupts every layer and
  discards the previous pile's queued cues.
- `three-star-celebration.mp3`: `viralaudio-descent-whoosh-long-cinematic-sound-effect-405921.mp3`
  (0.462229-4.485187 seconds), immediately followed by
  `freesound_gamestudio-level-complete-394515.mp3` (0.117563-2.586156 seconds).
  Silent ends are removed; no gap or crossfade is inserted. The combined clip lasts
  6.492 seconds, with victory beginning at 4.023 seconds.

Both files use libmp3lame quality 2. The shine, whoosh and victory were normalized separately
in two passes to -20 LUFS, maximum -3 dBTP and LRA 7 before MP3 encoding. The pile shine is
then attenuated by 4 dB at playback to balance its synthesized layers. Decoded file levels
are -20.01 LUFS for shine and -20.24 LUFS for the combined celebration, before playback gain.

Samples preload after the start gesture and cancel on mute, backgrounding or a new level.
Reduced motion plays only the victory portion. Spoken voices and their assets were removed
at the project owner's request; source files in E:/game_assets/sound/voice are untouched.
