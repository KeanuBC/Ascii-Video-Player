# ASCII Video Player

A Python-based video player that converts regular videos into animated ASCII art and plays them directly inside your command prompt or terminal.

Supports both grayscale and colored ASCII rendering, with optional audio playback synchronized alongside the video.

## Features

- **ASCII Video Rendering** – Converts video frames into animated ASCII characters in real time.
- **Color Mode** – Displays colored ASCII art that approximates the original video's colors.
- **Grayscale Mode** – Traditional black-and-white ASCII playback.
- **Audio Playback** – Plays the original video's audio alongside the ASCII animation.
- **Audio/Video Synchronization** – Uses audio playback as the timing reference to keep video and audio synchronized.
- **Adjustable Scaling** – Choose between 8 different display scale levels.
- **Graphical File Selection** – Browse and select videos through a file selection window.
- **Multiple Video Formats** – Supports MP4, MKV, AVI, MOV, and WebM.
- **Automatic Cleanup** – Temporary audio files are removed after playback.

## Preview

Videos are converted into ASCII characters and displayed directly in the terminal, creating an animated text-based playback experience.

## Requirements

- Python 3
- OpenCV
- NumPy
- Pygame (optional, for audio playback)
- FFmpeg (required for audio playback)
- Windows Curses (Windows only)

## Installation

1. Download or clone this repository.
2. Install the Python dependencies:

   ```bash
   python -m pip install opencv-python numpy pygame windows-curses
   ```

3. Install [FFmpeg](https://ffmpeg.org/download.html) and add it to your system PATH.
4. Run the player:

   ```bash
   python ascii_video_player.py
   ```

For detailed installation instructions and troubleshooting, see [SETUP.txt](SETUP.txt).

## How to Use

1. Launch the Python script.
2. Select a video using the file browser.
3. Choose your preferred ASCII rendering mode:
   - `color` – Colored ASCII rendering.
   - `normal` – Grayscale ASCII rendering.
4. Choose a display scale between 1 and 8.
5. Enjoy your video!

### Controls

| Key | Action |
|---|---|
| Q | Quit playback |

## Supported Formats

- MP4
- MKV
- AVI
- MOV
- WebM

## Additional Notes

- Audio playback requires both Pygame and FFmpeg.
- Without audio dependencies, videos can still play silently.
- Color rendering depends on terminal color support.
- Performance depends on your hardware and terminal rendering speed.
- Frames may be skipped automatically if rendering falls behind playback.

## License

This project is licensed under the [MIT License](LICENSE).

---

**Enjoy watching videos in ASCII!**
