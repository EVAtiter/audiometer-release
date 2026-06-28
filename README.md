[English](README.md) | [日本語](README.ja.md)

# AudioMeter

A menu-bar app that displays your Mac's audio output on a real analog VU meter.

![AudioMeter](docs/screenshot.png)

## Features

- **Standard VU meter response** — The needle follows the IEC 60268-17 ballistics spec (reaches 99% in ~300 ms with a slight overshoot), moving with the smooth, musical motion of a real mechanical meter rather than the jumpy motion of a digital peak meter.
- **Captures all system audio** — Apple Music, Spotify, YouTube — anything coming from your Mac's speakers is shown on the meters. It uses a Core Audio process tap, so no screen-recording indicator (the orange dot) appears.
- **Follow playback (auto-sleep)** — Dims and rests after a period of silence, and wakes up automatically when playback starts.
- **Fully vector-drawn** — The dial, logarithmic scale, red band, needle, and lighting are all drawn in code. Cream/amber illumination, dual stereo meters.
- **Three display modes** — Normal / Always on Top / Pin to Desktop. Window position is remembered per display.
- **Japanese / English** — Follows the system language (English outside Japanese environments).

## Requirements

- macOS 15 Sequoia or later
- Apple Silicon (arm64) only

## Installation

1. Download the latest `AudioMeter-X.Y.Z.zip` from [Releases](https://github.com/EVAtiter/audiometer-release/releases).
2. Unzip it and move `AudioMeter.app` to your Applications folder.
3. On first launch you'll be asked to allow capturing system audio. Please allow it (it captures playback audio only, not the microphone).

Or with Homebrew:

```
brew install --cask EVAtiter/tap/audiometer
```

The app is Developer ID signed and notarized, so it runs right after download.

## Usage

- Operate it from the waveform icon in the menu bar (it doesn't appear in the Dock).
- With "Follow playback (auto-sleep)" enabled, it rests when there's no sound and wakes on playback.
- Click the meter window to toggle pause / resume.

## Background

This is a modern rewrite of "AudioMeter 2.0," which I originally wrote for PowerPC Macs in 1995. I rebuilt its needle motion (fast attack, slow release) with today's technology, this time matching the standard VU spec.

<img width="403" height="105" alt="audio_meter" src="https://github.com/user-attachments/assets/b0472162-a6b7-4bae-b0cf-bc4c3bd48e07" />

## Datasheet

Compliant with IEC 60268-17 — reaches 99% in 300 ms, overshoot approx. 1.2%

<img width="1600" height="1000" alt="needle_step_response" src="https://github.com/user-attachments/assets/1c1b3df0-121f-4adf-b30c-1dfb29524daf" />

## License

Copyright © 1995–2026 EVA Titer. All rights reserved.
