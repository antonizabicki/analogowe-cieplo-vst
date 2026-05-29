# 🎛️ Analogowe Ciepło (Analog Warmth) - VST3/AU Audio Plugin

![Main Interface](assets/main.png)

**Analogowe Ciepło** is a custom audio plugin (VST3/AU/Standalone) built using the **JUCE (C++)** framework. Its primary goal is to warm up digital tracks, introduce characteristic lo-fi dirt, and add charming imperfections known from vintage analog gear and vinyl records.

The plugin stands out with its unique graphical interface, which was fully 3D rendered in Blender, preserving realistic lighting, depth, and the exact perspective of every hardware element (custom look & feel).

---

## ✨ Key Features (DSP)

The plugin consists of three main signal processing modules, controlled via a photorealistic GUI:

*   **Chwiejność (Wow & Flutter):**
    *   Dual pitch modulation based on a modulated delay line.
    *   *Slow oscillation (0.25 Hz - 2 Hz):* Simulates the uneven motor speed of a cassette tape machine (Wow effect).
    *   *Fast oscillation (50 Hz - 100 Hz):* Adds specific analog grit and roughness to the signal (Flutter effect).
    
*   **Poszumek (Dynamic Vinyl Noise):**
    *   Vinyl noise and crackle generator.
    *   *Envelope Follower:* The noise amplitude dynamically reacts to the input signal volume (the noise "breathes" along with the instrument).
    *   *Smart Noise Gate:* When no audio signal is passing through the plugin, the noise fades out to absolute zero (preventing unwanted noisy tails in the mix).
    *   *TILT Filter:* Smooth tonal balance adjustment for the generated noise.

*   **Nasycenie (Tape Saturation):**
    *   Analog-style saturation based on the hyperbolic tangent function (`tanh`).
    *   *Auto-Gain:* Built-in automatic volume compensation. Increasing the Drive maintains a consistent perceived output volume, preventing track or master bus clipping.

---

## 🔍 GUI Details

![Focus Detail](assets/focus.png)

All knobs are multi-frame animations (Sprite Sheets / Filmstrips) rendered using the *Render Region* technique in Blender. This workflow allowed for perfect matching of the 3D perspective and lighting angles with the central camera projection within the 2D rendering environment of the JUCE framework.

---

## 🛠️ How to Build from Source

If you want to compile the plugin yourself or modify its code, follow the instructions below.

### Requirements:
1.  **JUCE Framework** (version 7.x or 8.x recommended).
2.  **C++ IDE / Compiler:** 
    *   *Windows:* Visual Studio 2022 / 2026 (with the "Desktop development with C++" workload installed).
    *   *macOS:* Xcode.

### Instructions:
1. Clone this repository to your local machine:
   ```bash
   git clone https://github.com/YourUsername/AnalogoweCieplo.git
