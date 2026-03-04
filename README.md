# PolyTone – Multi‑Frequency Sine Wave Generator

PolyTone is a single‑file HTML web application that lets you play multiple sine wave frequencies simultaneously.  
It covers a wide range from **1 Hz to 40 kHz** with **500 Hz steps above 1 kHz** – perfect for testing audio equipment, psychoacoustic experiments, or just exploring the limits of human hearing.

## Features

- **82 frequencies** in one page:
  - 1 Hz, 10 Hz, 100 Hz (very low, mostly for measurement)
  - 1.0 kHz, 1.5 kHz, 2.0 kHz … 40.0 kHz (500 Hz steps)
- **Click any button** to toggle that tone on/off – multiple tones can play together.
- **PLAY ALL** – instantly start every frequency at once (useful for stress tests).
- **STOP ALL** – kill all tones with one click.
- Visual feedback: active buttons are highlighted, and the status bar shows how many tones are playing.
- Pure sine waves (low distortion) with a moderate gain to avoid clipping.
- Works offline – just save the HTML file and open it in any modern browser (Chrome, Edge, Firefox, Safari).

## How to Use

1. Open the `index.html` file in your browser.
2. Click any frequency button – the tone starts immediately.
3. Click the same button again to stop that tone.
4. Use **PLAY ALL** to enable every frequency at once.
5. Use **STOP ALL** to silence everything.

> **Note:** Frequencies above ~20 kHz may be inaudible on most consumer hardware. The app still generates them, but your speakers/headphones may not reproduce them.

## Technical Details

- Built with the Web Audio API.
- Each frequency runs on its own `OscillatorNode` with a `GainNode` to control volume.
- The gain per tone is set to `0.3` to reduce clipping when many tones are active.
- All oscillers are of type `sine` for clean, harmonic‑free waveforms.

## Compatibility

- Works on all modern desktop and mobile browsers that support the Web Audio API.
- On iOS, make sure the device is not in silent mode and that you interact with the page first (due to autoplay policies).

## License

This project is open source and available under the [MIT License](LICENSE).

---

*Enjoy exploring the world of frequencies!*
