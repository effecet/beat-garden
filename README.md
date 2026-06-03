# 🎵 Beat Garden

[![▶ Play it now](https://img.shields.io/badge/▶_Play_it_now-effecet.github.io-5ddf7a)](https://effecet.github.io/beat-garden/)
[![license: MIT](https://img.shields.io/badge/license-MIT-blue)](LICENSE)
[![no dependencies](https://img.shields.io/badge/dependencies-none-brightgreen)](#)
[![Web Audio](https://img.shields.io/badge/Web%20Audio-API-f97316)](https://developer.mozilla.org/docs/Web/API/Web_Audio_API)

A tiny, friendly **step-sequencer** that runs entirely in the browser. Tap the
squares to place notes, hit play, and every note sounds good — a forgiving little
music toy. Adjust the tempo, switch sounds, and save your songs locally.

**▶ [Play it now in your browser →](https://effecet.github.io/beat-garden/)** — no install, no account.

**One self-contained HTML file. No build, no dependencies, no network.**

## Try it

- **Live:** **https://effecet.github.io/beat-garden/** — runs right in your browser, nothing to install.
- **Local:** just open `index.html` in any modern browser — double-click it, or:

  ```bash
  # optional: serve it (some browsers restrict file:// audio autoplay)
  python3 -m http.server 8080
  # then open http://localhost:8080
  ```

## Features

- **Tap-to-compose** step grid — click cells across the tracks, then ▶ Play.
- **Tempo control** (BPM).
- **Selectable sounds** and a built-in synth voice set (Web Audio oscillators).
- **Save / load** songs to the browser's `localStorage` — no account, no server.
- **Download your song as a WAV** — renders the pattern offline and saves a real
  audio file you can keep; pick Short / Medium / Long in Studio mode.
- **Fully offline** — the whole app is one HTML file with inline CSS + JS.

## How it works

Everything is vanilla JavaScript + the [Web Audio API](https://developer.mozilla.org/docs/Web/API/Web_Audio_API):
an `AudioContext` schedules `OscillatorNode` + `GainNode` voices on each step,
a `requestAnimationFrame` loop drives the playhead, and songs are serialized to
`localStorage`. Audio export re-renders the same voices through an
`OfflineAudioContext` and encodes the result to a 16-bit PCM WAV — no frameworks,
no bundler, no libraries.

## License

MIT — see [LICENSE](LICENSE).
