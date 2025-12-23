# QuickTube 2.0 - A Python YouTube & SVT Play TUI Helper

A powerful and cross-platform TUI (Terminal User Interface) tool to quickly stream or download videos/audio from YouTube and SVT Play. Rewritten in Python, it features a modern interactive menu system, automatic clipboard detection, and support for Linux, macOS, and Windows.

![demo-gif](https://raw.githubusercontent.com/wulffern/QuickTube/main/img/QuickTube.gif)

## Features

- **Stream Video**: Instantly stream videos in `mpv`.
- **Stream Audio**: Listen to audio-only in `mpv` (great for music/podcasts).
- **Download Video**: 
    - **YouTube**: Auto-detects available resolutions and lets you choose the best quality. Merges video with the best audio track.
    - **SVT Play**: Download episodes with subtitles automatically merged.
- **Download Audio**: Extract high-quality audio (converted to `opus`).
- **Playlist & Series Support**: 
    - **YouTube**: Download full playlists (video or audio), automatically numbered.
    - **SVT Play**: Download full seasons, specific episodes (e.g., `1-5`), or the last X released episodes.
- **Clipboard Detection**: Automatically grabs URLs from your clipboard on startup.
- **Cookie Support**: Option to "borrow" cookies from your browser (Chrome, Firefox, Brave, etc.) to access age-restricted content or premium formats.
- **Built-in Updater**: Easily update `yt-dlp` and `svtplay-dl` binaries directly from the menu.
- **Cross-Platform**: Works on Linux, macOS, and Windows.

## Prerequisites

### External Tools
You need these installed and available in your system PATH:
1.  **[mpv](https://mpv.io/)**: For streaming playback.
2.  **[ffmpeg](https://ffmpeg.org/)**: For merging video/audio and converting formats.
3.  **[yt-dlp](https://github.com/yt-dlp/yt-dlp)**: For YouTube downloads.
4.  **[svtplay-dl](https://svtplay-dl.se/)**: For SVT Play downloads.

*(Note: The script has a built-in helper to download `yt-dlp` and `svtplay-dl` to a local bin folder if you prefer not to install them system-wide, but `mpv` and `ffmpeg` must be installed manually.)*

### Python Dependencies
The tool requires **Python 3** and the libraries listed in `requirements.txt`.

## Installation

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/yourusername/QuickTube2.0.git
    cd QuickTube2.0
    ```

2.  **Set up a Virtual Environment (Recommended):**
    ```bash
    python3 -m venv .venv
    source .venv/bin/activate  # On Windows: .venv\Scripts\activate
    ```

3.  **Install Python requirements:**
    ```bash
    pip install -r requirements.txt
    ```

## How to Use

1.  **Activate your virtual environment** (if not already active).
2.  **Run the script:**
    ```bash
    python quicktube.py
    ```
3.  **Interact:**
    -   If you have a YouTube or SVT Play link in your clipboard, the tool will ask if you want to use it.
    -   Otherwise, select "Paste link" or paste one manually.
    -   Use the arrow keys to navigate the menu and `Enter` to select options.
    -   Press `q` or `Esc` to go back or exit.

## Configuration

-   **Cookies**: If you face issues with age-restricted videos, use the "Select cookie browser" option in the main menu to use cookies from your installed browser.
-   **Updates**: Use "Update tools" in the main menu to fetch the latest versions of the downloaders.

## Disclaimer

This script is for educational purposes to demonstrate Python TUI creation. It is not intended for downloading copyrighted content without permission. Please respect YouTube's and SVT's Terms of Service and copyright laws.
