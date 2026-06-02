# 🎵 Beat Garden

[![license: MIT](https://img.shields.io/badge/license-MIT-blue)](LICENSE)
[![no dependencies](https://img.shields.io/badge/dependencies-none-brightgreen)](#)
[![Web Audio](https://img.shields.io/badge/Web%20Audio-API-f97316)](https://developer.mozilla.org/docs/Web/API/Web_Audio_API)

A tiny, friendly **step-sequencer** that runs entirely in the browser. Tap the
squares to place notes, hit play, and every note sounds good — a forgiving little
music toy. Adjust the tempo, switch sounds, and save your songs locally.

**One self-contained HTML file. No build, no dependencies, no network.**

## Try it

- **Live:** enable GitHub Pages for this repo (Settings → Pages → deploy from `main`),
  then open the published URL.
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
- **Fully offline** — the whole app is one HTML file with inline CSS + JS.

## How it works

Everything is vanilla JavaScript + the [Web Audio API](https://developer.mozilla.org/docs/Web/API/Web_Audio_API):
an `AudioContext` schedules `OscillatorNode` + `GainNode` voices on each step,
a `requestAnimationFrame` loop drives the playhead, and songs are serialized to
`localStorage`. No frameworks, no bundler.

## License

MIT — see [LICENSE](LICENSE).
