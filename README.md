# PolyTone 🔉🌀

**PolyTone** is a minimalist web-based audio tool that lets you play multiple sine wave tones **simultaneously**. Toggle any frequency from **1 Hz to 40 kHz** on and off, with a pink‑noise inspired gain curve to balance the spectrum. Includes a master compressor and a sine‑wave tremolo for dynamic volume shaping.

![screenshot](screenshot.png)  
*(Add a screenshot of the interface here)*

---

## ✨ Features

- **Concurrent playback** – Any number of tones can be played at the same time.
- **Wide frequency range** – 1, 10, 25, 50, 100 Hz, then 1.0–40.0 kHz in **500 Hz steps**.
- **Pink‑weighted gain** – Higher frequencies are gently attenuated (∝ 1/√f) to avoid harshness and balance the mix.
- **Toggle on/off** – Click a frequency button to start it; click again to stop.
- **PLAY ALL / STOP ALL** – One‑click full spectrum or silence.
- **Master Compressor** – Fixed‑setting dynamics processor (threshold -20 dB, ratio 4:1) to tame peaks.
- **Sine‑wave Tremolo** – Modulate overall volume with adjustable period (0.1–10 s) and depth (0–100%).
- **No dependencies** – Pure HTML, CSS, and vanilla JavaScript.

---

## 🚀 How to Use

1. Clone the repository or download `index.html`.
2. Open `index.html` in any modern browser (Chrome, Firefox, Safari, Edge).
3. Click any frequency button to start that tone.
4. Click an active button to stop that tone.
5. Use **PLAY ALL** to start every frequency, **STOP ALL** to silence everything.
6. Toggle the compressor and tremolo with their checkboxes and adjust parameters.

> ⚠️ **Note**:  
> - Very low frequencies (1–50 Hz) may be felt as vibrations rather than heard.  
> - Frequencies above ~20 kHz may be inaudible on most consumer speakers/headphones.

---

## 📋 Frequency List

The app includes **84 frequencies** in total:

- **Low**: 1, 10, 25, 50, 100 Hz  
- **High**: 1.0, 1.5, 2.0, … 40.0 kHz (every 500 Hz)

All tones are pure sine waves.

---

## 🧠 Technical Details

- **Audio engine**: Web Audio API (`OscillatorNode` + `GainNode` per tone).  
- **Gain shaping**: `gain = 0.05 * sqrt(1000 / f)` for f > 1 kHz.  
- **Compressor**: Master‑only, fixed preset (`threshold: -20, ratio: 4, attack: 0.003, release: 0.25, knee: 30`).  
- **Tremolo**: Low‑frequency oscillator modulates a master gain node.  
- **Code structure**: Modular `ToneManager` and `UIManager` classes for clean separation.

---

## 🌐 Browser Compatibility

Works in all browsers that support the Web Audio API:

- ✅ Chrome (desktop & Android)
- ✅ Firefox
- ✅ Safari (desktop & iOS 15+)
- ✅ Edge
- ✅ Opera

---

## 📄 License

MIT License – feel free to use, modify, and distribute.

---

**Happy tone‑stacking!** 🎶
