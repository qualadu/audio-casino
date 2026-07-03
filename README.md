# 🎰 Audio Casino <sub> Version 2.02 </sub>

An interactive slot machine that plays a random audio clip every time you pull the lever.

Each sound is represented by its own unique emoji, making it easy to identify the selected audio on the display. The remaining reels are filled with six - seven emojis (just for the giggles.

## Usage

Using the Audio Casino couldn't be easier:

1. Turn your speakers or headphones up to the full volume.
2. Pull the lever.
3. Enjoy the randomly selected sound!

## Project Structure

```text
.
├── index.html            Main page containing the slot machine, lever, reels, and display
├── css/
│   └── style.css         Style of the slot machine, ect.
├── js/
│   └── script.js         Slot logic, reel animations, and random sound selection
├── audio/                Add your own audio files here
│   └── testlib/          Test library containing placeholder sounds
│       ├── jackpot.wav
│       ├── coin-rain.wav
│       ├── bell.wav
│       ├── applause.wav
│       └── miss.wav
└── README.md
```

The included `.wav` files are simple synthetic placeholder sounds (sine waves and noise) so the project works immediately after cloning. They are intended for testing and can easily be replaced with your own audio files.

## Adding Your Own Sounds

1. Copy your audio file (for example, `.mp3` or `.wav`) into the `audio/` directory.

   > **Important:** Audio files placed in this folder are subject to copyright. Make sure you have the rights to use them. The bundled custom MP3 files are intended for use by their creator only and must not be redistributed or used by third parties.

2. Add a new entry to the `SOUND_LIBRARY` array in `js/script.js`:

```javascript
const SOUND_LIBRARY = [
  { file: "audio/jackpot.wav", label: "Jackpot!", symbol: "🎉" },
  { file: "audio/my-sound.mp3", label: "My Sound", symbol: "🎵" },
  // Additional entries...
];
```

Each entry consists of:

* **`file`** – Path to the audio file relative to `index.html`
* **`label`** – Text displayed after the reels stop spinning
* **`symbol`** – Emoji or character shown on the center reel

3. Save the file. Your new sound will now be included in the random selection.

To remove a sound, simply delete its entry from `SOUND_LIBRARY` and optionally remove the corresponding audio file from the `audio/` directory.

## License

The source code may be freely used, modified, and incorporated into your own projects.

> [!IMPORTANT]
> Audio files (including MP3 files and externally sourced audio referenced in SOUND_LIBRARY) are not covered by this permission. Unless explicitly stated otherwise, they remain the property of their respective copyright holders and may not be redistributed, modified, or included in third-party projects without permission.

## Version History
### Version 2.02
#### Improvements:
- Added responsive scaling so the slot machine automatically adapts to different screen sizes and device resolutions.
- Improved the overall layout for desktop and mobile devices.
#### JavaScript:
- Reworked the reel logic so the slots now perform an actual spinning animation instead of instantly changing symbols.
- Improved the randomness and timing of the reel stopping sequence for a more authentic slot machine experience.

### Version 2.01
#### Visual Improvements: 
- Added an icy chrome finish to better match the overall background theme.
- Introduced a decorative string of lights spanning the entire width of the machine.
- Repositioned the slot machine toward the lower portion of the screen for improved composition.
#### JavaScript:
- Added automatic sizing for the decorative light string.
- Updated the emoji collection to better match the available sounds and overall visual style.
#### Audio: 
- Expanded the sound library with additional random sound effects sourced from the web.

### Version 2.00
Firt comlpete release of the **Audio Casino**
#### Features
- Interactive slot machine with three spinning reels.
- Pulling the lever randomly selects and plays one sound from the sound library.
- The center reel displays the emoji associated with the selected sound.
- The two outer reels display random emojis from a larger symbol pool for visual variety.
- Fully customizable sound library through the SOUND_LIBRARY array.


### Version 1.00
Initial prototype
#### Features
- Simple embedded audio player
- Supports playing, pausing and downlading a single audio file
- Github Page compatible implementation that envolved into the Audio Casino project.
