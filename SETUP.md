ASCII VIDEO PLAYER - SETUP & INSTALLATION
=========================================
Version: 1.4

ABOUT
-----
ASCII Video Player is a Python-based video player that converts
regular video files into animated ASCII art and displays them
directly inside a command prompt or compatible terminal.

It supports both grayscale and colored ASCII playback, with
optional audio playback synchronized alongside the video.

FEATURES
--------
- Converts video frames into ASCII characters in real time.
- Supports grayscale and colored ASCII rendering.
- Plays original video audio alongside the ASCII playback.
- Uses audio playback as the synchronization reference.
- Offers 8 different display scale settings.
- Includes a graphical file browser for selecting videos.
- Automatically removes temporary audio files after playback.
- Supports automatic frame skipping when rendering falls behind.

SUPPORTED VIDEO FORMATS
-----------------------
- MP4
- MKV
- AVI
- MOV
- WebM

REQUIREMENTS
------------
The following software is required:

1. Python 3
2. OpenCV (opencv-python)
3. NumPy
4. Windows Curses (Windows only)
5. FFmpeg (required for audio playback)
6. Pygame (required for audio playback)

INSTALLATION
------------

STEP 1 - INSTALL PYTHON
-----------------------
Download and install Python 3 from:

https://www.python.org/downloads/

During installation on Windows, make sure to enable:

[✓] Add Python to PATH

You can verify the installation by opening Command Prompt
and entering:

python --version

STEP 2 - INSTALL PYTHON DEPENDENCIES
------------------------------------
Open Command Prompt and run:

python -m pip install opencv-python numpy pygame windows-curses

Note:
Windows Curses is only required when running on Windows.
Other operating systems may already provide curses.

STEP 3 - INSTALL FFMPEG
-----------------------
FFmpeg is required to extract audio from video files.

Download FFmpeg from:

https://ffmpeg.org/download.html

Install FFmpeg and make sure its executable is added to
your system PATH.

To verify that FFmpeg is installed correctly, open a new
Command Prompt window and enter:

ffmpeg -version

If FFmpeg is installed correctly, version information
should appear.

STEP 4 - DOWNLOAD THE PROJECT
-----------------------------
Download or clone the ASCII Video Player repository
from GitHub.

If downloading through GitHub:

1. Open the project repository.
2. Select the green Code button.
3. Select Download ZIP.
4. Extract the downloaded ZIP file.
5. Locate the Python script.

STEP 5 - RUN THE PLAYER
-----------------------
Open the folder containing the Python script.

You can launch the player through Command Prompt using:

python ascii_video_player.py

Replace "ascii_video_player.py" with the actual filename
if it is different.

USING THE PLAYER
----------------

1. A file selection window will appear.
2. Select the video you want to play.
3. Choose an ASCII display mode when prompted.

DISPLAY MODES
-------------

NORMAL:
Displays the video using grayscale ASCII characters.

COLOR:
Displays the video using colored ASCII characters that
approximate the original video's colors.

SCALE SETTINGS
--------------

You will be prompted to enter a scale value between 1 and 8.

1 - Smallest display width.
2 - Larger display width.
3 - Larger display width.
4 - Larger display width.
5 - Larger display width.
6 - Larger display width.
7 - Larger display width.
8 - Largest display width.

Higher scale values use more terminal width.

PLAYBACK CONTROLS
-----------------
Q - Quit video playback.

AUDIO PLAYBACK
--------------
The player extracts the video's audio track using FFmpeg
and temporarily converts it into a WAV file.

Pygame handles audio playback while the video is rendered
as ASCII characters.

The audio playback timeline is used to synchronize video
frames.

If audio playback cannot be initialized, the player will
attempt to continue displaying the video silently.

IMPORTANT:
Both Pygame and FFmpeg must be installed and available
for audio playback.

TROUBLESHOOTING
---------------

PROBLEM: Python is not recognized.
SOLUTION:
Make sure Python is installed and added to your system PATH.

PROBLEM: No module named cv2.
SOLUTION:
Run:
python -m pip install opencv-python

PROBLEM: No module named numpy.
SOLUTION:
Run:
python -m pip install numpy

PROBLEM: No module named pygame.
SOLUTION:
Run:
python -m pip install pygame

PROBLEM: No module named curses.
SOLUTION:
On Windows, run:
python -m pip install windows-curses

PROBLEM: FFmpeg was not found.
SOLUTION:
Install FFmpeg and make sure its executable is added to
your system PATH. Restart Command Prompt afterward.

PROBLEM: Audio is unavailable.
SOLUTION:
Verify that Pygame and FFmpeg are installed correctly.
Some video files may also lack an extractable audio track.

PROBLEM: The video is running slowly.
SOLUTION:
Try lowering the scale setting or using a smaller
terminal window resolution.

PROBLEM: Color mode does not work.
SOLUTION:
Make sure your terminal supports colors. Some terminal
environments may not support the required color features.

NOTES
-----
- Audio playback is optional.
- Videos without audio can still be displayed.
- Color rendering depends on terminal color support.
- Playback performance depends on system hardware.
- The player may skip frames when rendering cannot keep
  up with the video's playback speed.
- Temporary WAV files are automatically cleaned up
  after playback.

CREDITS & LICENSE
-----------------
ASCII Video Player is distributed under the MIT License.

You are free to use, modify, and distribute this project
under the terms of the included LICENSE file.

Enjoy watching videos in ASCII!
