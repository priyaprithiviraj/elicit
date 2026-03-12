# Elicit

Elicit is a browser-based tool for the elicitation and recording of spoken narratives using picture stimuli. It is intended for use in research, clinical, and educational contexts where spoken language samples are collected from participants across a series of images.

## Screenshots

**Step 1: Enter the participant's name using button 1. The name appears immediately in the session bar.**

![Step 1](screenshot_1.png)

**Step 2: Upload story images using button 2. Thumbnails appear in the strip and the first image is displayed automatically.**

![Step 2](screenshot_2.png)

**Step 3: Navigate images using the arrow or keyboard. A tick on the first thumbnail confirms a completed recording. Press Record on the current image to continue. Once all recordings are saved, the Download button becomes active.**

![Step 3](screenshot_3.png)

---

## Overview

Elicit runs entirely in the browser as a single HTML file with no installation, server, or internet connection required. Researchers upload story images, record participant narratives, and download the audio as WAV files for subsequent analysis. Up to ten images may be used per session.

---

## Getting Started

Download `elicit.html` and open it in a modern browser. No installation is required. Chrome or Edge (version 90 or later) are recommended. Firefox and Safari are also supported.

The tool requires microphone access, which the browser will request on first use. Elicit must be opened either as a local file or served over HTTPS for microphone access to function. It is compatible with GitHub Pages.

---

## Usage

Enter the participant's name using button **1** on the left panel. Upload story images using button **2** (JPG, PNG, or GIF; up to ten images). Images are displayed in the order they are loaded and can be navigated using the arrow button or the keyboard right arrow key.

To record, press **Record** and begin the elicitation. Press **Stop** when the participant has finished. A blue border and a tick mark on the thumbnail confirm that a recording has been saved for that image. Once recordings have been made, press **Download** to export all audio files as WAV (16-bit PCM, 44.1 kHz), named sequentially by participant name and image number (e.g., `Aisha_image_01.wav`).

Recording continues across images unless manually stopped. To obtain separate recordings per image, press Stop after each image before advancing to the next.

---

## Notes for Researchers

Elicit does not transmit or store any data. All processing occurs locally in the browser and no participant data leaves the device. The tool does not log sessions, retain recordings between sessions, or require an account.

The WAV format was chosen for compatibility with speech analysis software including CLAN, Praat, and Audacity. The recording is mono, 16-bit, at 44,100 Hz.

Researchers are responsible for obtaining appropriate ethical approval and participant consent prior to use.

---

## Citation

If you use Elicit in research or adapt it for your own work, please cite:

> Prithiviraj, P. (2026). *Elicit: A narrative elicitation tool* [Computer software]. https://priyaprithiviraj.github.io/elicit

---

## License

MIT License © 2026 Priya Prithiviraj. See `LICENSE` for full terms. The MIT License permits free use, modification, and redistribution with attribution.
