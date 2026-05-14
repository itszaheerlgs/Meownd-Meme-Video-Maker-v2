# 🐱 Meownd Meme Video Maker v2

A GUI tool for compositing any video (local file or stream link) directly into a meme template image — no manual video editing required. Drop your template, paste a link, adjust the zone, and render a clean MP4.

---

## ✨ Features

- **Stream-direct rendering** — paste any YouTube/supported link and the video is streamed in-place via yt-dlp; no full download needed.
- **Live draggable zone preview** — see exactly where your video will appear on the template. Drag to move, pull corners to resize.
- **Auto yellow-zone detection** — automatically detects a yellow region in your template image to use as the video placement zone.
- **Flexible video input** — accepts direct MP4/WebM/MOV/AVI URLs, local video files, or any yt-dlp-supported platform link.
- **Customizable output** — choose from preset sizes (1080×1080, 1920×1080, 1080×1920) or set a custom resolution.
- **Border support** — add a colored border around the video zone with configurable thickness and color.
- **Loop mode** — automatically loops short clips to fill up to 60 seconds.
- **Audio control** — optionally keep or strip source audio.
- **MoviePy v1 & v2 compatible** — works across MoviePy versions via runtime shims.
- **Auto-installs dependencies** — missing packages are installed automatically on first run.

---

## 🖥️ Screenshots

> *Add your screenshots here.*

---

## 🚀 Getting Started

### Prerequisites
- Python **3.8+**
- `ffmpeg` must be installed and available on your system PATH (required by MoviePy).

**Install ffmpeg:**
- **Windows:** [https://ffmpeg.org/download.html](https://ffmpeg.org/download.html) (add to PATH)
- **macOS:** `brew install ffmpeg`
- **Linux:** `sudo apt install ffmpeg`

### Installation

```bash
git clone https://github.com/your-username/meownd-meme-maker.git
cd meownd-meme-maker
```

> All Python dependencies are installed automatically on first launch. No manual `pip install` needed.

### Running

```bash
python Meownd_Meme.py
```

---

## 🧑‍💻 Usage

1. **Load Template** — Browse to or paste the path of your meme template image (JPG/PNG).
2. **Adjust Zone** — Drag the overlay rectangle on the preview to position and resize the video zone. Use *Auto-Detect Zone* to automatically find a yellow region in the template.
3. **Set Video Source** — Either:
   - Browse and select a local video file, or
   - Paste a URL (YouTube, direct MP4, etc.) and click **Use this link / file** to resolve it.
4. **Configure Options:**
   - Trim clip with start/end time (seconds)
   - Set output resolution
   - Toggle audio, loop, and border settings
   - Set FPS and output file path
5. **Render** — Click **🎬 RENDER VIDEO** and monitor progress in the log panel. The output MP4 is saved to `meownd_outputs/` by default.

---

## ⚙️ Configuration

| Option | Default | Description |
|---|---|---|
| Output size | 1080×1080 | Resolution presets or custom W×H |
| Start time | 0 s | Clip trim start |
| End time | *(full)* | Clip trim end |
| FPS | 30 | Output frames per second |
| Keep audio | On | Include source audio in output |
| Loop | Off | Loop clip to fill up to 60 s |
| Border thickness | 0 px | Pixel width of zone border |
| Border color | `#000000` | Hex color for the border |

---

## 📦 Dependencies

Installed automatically on first run:

| Package | Purpose |
|---|---|
| `customtkinter` | Modern dark-themed GUI |
| `pillow` | Image loading and compositing |
| `opencv-python` | Yellow-zone auto-detection |
| `numpy` | Array-level image manipulation |
| `moviepy` | Video compositing and export |
| `yt-dlp` | Stream URL resolution (no download) |
| `requests` | HTTP utilities |

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).
