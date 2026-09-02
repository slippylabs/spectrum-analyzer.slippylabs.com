# Audio Spectrum Analyzer

Real-time audio spectrum, waveform and spectrogram from your microphone or an audio file, with peak frequency and note detection. Runs entirely in the browser.

**Live:** <https://spectrum-analyzer.slippylabs.com/>

## What it does

- Real-time spectrum, waveform and scrolling spectrogram views.
- Input from your microphone or from an audio file you drop in.
- FFT size selectable from 512 up to 8192.
- Peak frequency readout with the nearest musical note.

## How it works

Analysis runs on a WebAudio `AnalyserNode`, with the spectrogram drawn column by column into a canvas as frames arrive. The note readout maps the peak bin to the nearest equal-tempered pitch and shows how many cents sharp or flat it is.

## Run it locally

A static site. No build step, no package manager, no dependencies:

```
git clone git@github.com:slippylabs/spectrum-analyzer.slippylabs.com.git
cd spectrum-analyzer.slippylabs.com
python3 -m http.server 8000
```

Then open <http://localhost:8000>.

## Notes

Microphone input needs your permission and a secure context (HTTPS or `localhost`). The audio is analysed in the page and never recorded, stored or transmitted.

---

Part of [Slippy Labs](https://slippylabs.com). Every tool is indexed at
[projects.slippylabs.com](https://projects.slippylabs.com).
