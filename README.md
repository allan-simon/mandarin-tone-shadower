# Mandarin Tone Shadower

Practice Mandarin tones by shadowing native audio — visualizes pitch contours and compares them with your recordings in real-time.

## How it works

1. **Load** a reference audio clip of a native speaker
2. **Enter** the Chinese characters and pinyin to see per-syllable alignment
3. **Record** yourself repeating the same phrase (optionally playing the reference simultaneously — this is "shadowing")
4. **Compare** your pitch contour against the reference on a semitone graph

## Technique

Pitch extraction runs entirely in the browser using [SwiftF0](https://swift-f0.github.io/), an ONNX neural pitch estimator loaded via ONNX Runtime WASM. The extracted F0 values are converted to semitones relative to the speaker's median pitch, then aligned using Dynamic Time Warping (DTW) to produce a visual overlay and a similarity score.

No server, no data leaves your browser.

## Credits

Sample sentence and audio from [Tatoeba.org](https://tatoeba.org).
