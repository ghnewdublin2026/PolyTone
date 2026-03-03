# PolyTone 🔉🎛️

**PolyTone** is a minimalist web-based audio tool that lets you play multiple sine wave tones **simultaneously**. Toggle any frequency from **1 Hz to 40 kHz** on and off, and hear them all blend together in real time. Built with the Web Audio API, it’s perfect for audio experimentation, hearing tests, or just satisfying your curiosity about sound.

---

## ✨ Features

- **Concurrent playback** – Any number of tones can be played at the same time.
- **Wide frequency range** – 1 Hz, 10 Hz, 100 Hz, then 1 kHz … 40 kHz in 1 kHz steps.
- **Toggle on/off** – Click a frequency button to start it; click again to stop.
- **Visual feedback** – Active buttons are highlighted; status bar shows active count and frequencies.
- **Stop all** – One big red button silences everything instantly.
- **No dependencies** – Pure HTML, CSS, and vanilla JavaScript.

---

## 🚀 How to Use

1. Clone the repository or download `index.html`.
2. Open `index.html` in any modern browser (Chrome, Firefox, Safari, Edge).
3. Click any frequency button to start that tone.
4. Click an active button to stop that tone.
5. Use the **STOP ALL** button to silence all oscillators.

> ⚠️ **Note**:  
> - Very low frequencies (1 Hz, 10 Hz) may be felt as vibrations rather than heard.  
> - Frequencies above ~20 kHz may be inaudible on most consumer speakers/headphones.

---

## 📋 Frequency List

The app includes the following frequencies (43 in total):

- **1 Hz**, **10 Hz**, **100 Hz**
- **1 kHz**, **2 kHz**, **3 kHz**, … **40 kHz** (every 1 kHz step)

All tones are pure sine waves.

---

## 🧠 Technical Details

- **Audio engine**: Web Audio API (`OscillatorNode` + `GainNode` per tone).
- **Per‑tone gain**: `0.3` to prevent clipping when many tones are active.
- **Context handling**: AudioContext is created and resumed on first user click.
- **Code structure**:  
  - `ToneManager` – manages audio context, active oscillators, starting/stopping.  
  - `UIManager` – builds the button grid, updates status, handles UI events.  
  - Clean separation of concerns for easy maintenance.

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

This project is licensed under the MIT License – feel free to use, modify, and distribute it.

---

**Happy tone‑stacking!** 🎶
