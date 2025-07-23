# Philosophers-Stone

Philosophers-Stone is a dynamic wallpaper and video background randomizer for Linux and macOS. It supports both static images and looping videos as wallpapers using lightweight Bash scripts and a configuration-based design.

---

## 🚀 Features

- Randomly change wallpapers or videos from specified directories
- Caches wallpaper/video lists for faster access
- Tmux integration for persistent background processes
- Configurable with simple `.conf` file
- Works across popular Linux distributions and macOS
- Supports transition effects (Hyprland + swww)

---

## 📦 Dependencies

Install the following dependencies for full functionality:

- `tmux` – for detached wallpaper changing sessions
- `swww` – image background setter (Linux)
- `mpv` – video player
- `mpvpaper` – video wallpaper
- `bash`, `find`, `coreutils` – for automation logic
- `xdg-utils` – for desktop integration (optional, recommended)

### macOS:
```bash
brew install tmux mpv mpvpaper swww coreutils
```

---

## 🛠️ Setup

### 1. Clone the repo
```bash
git clone https://github.com/yourusername/Philosophers-Stone.git
cd Philosophers-Stone
```

### 2. Edit the Configuration

Open `philosophers-stone.conf`:
```bash
nano philosophers-stone.conf
```

And set the following variables:

```bash
WALLPAPER_DIR="$HOME/Pictures/Directory/to/your/Wallpapers"
VIDPAPER_DIR="$HOME/Videos/Directory/to/your/WallpaperVids"
MODE="image"        # or "video" or "random"
LOCKFILE="/tmp/random_wallpaper.lock"
CACHE_FILE="/tmp/wallpaper_list.txt"
SLEEP_INTERVAL=60   # delay between changes (seconds)
TRANSITION_TYPE="any"  # transition type for swww (Hyprland only)
```

### 3. Run It

Make it executable and launch:
```bash
chmod +x prima-materia
./prima-materia
```

Or run it in a background tmux session via wrapper:
```bash
chmod +x philosophers-stone
./philosophers-stone
```

---

## 🎨 Transition Types (for `swww`)

You can set any of the following in the config under `TRANSITION_TYPE`:

- `any`
- `random`
- `none`
- `simple`
- `fade`
- `wipe`
- `wave`
- `outer`
- `circle`
- `grow`
- `split`
- `center`
- `vortex`
- `zoom`
- `slip`
- `glide`
- `slide`
- `crossfade`

> Not all transitions are available on every compositor. These are primarily designed for `swww` with Hyprland or Wayland-compatible environments.

---

## 🧪 Supported Distros

### 🐧 Linux

| Distro      | Install Command |
|-------------|-----------------|
| **Arch**    | `sudo pacman -S swww mpv mpvpaper tmux` |
| **Debian/Ubuntu** | `sudo apt install swww mpv mpvpaper tmux` |
| **Fedora**  | `sudo dnf install swww mpv mpvpaper tmux` |
| **NixOS**   | Add to `environment.systemPackages` |
| **Gentoo**  | `emerge --ask swww mpv mpvpaper tmux` |

### 🍏 macOS
```bash
brew install tmux mpv mpvpaper swww coreutils
```

---

## 📜 License

This project is licensed under the **GNU General Public License v3.0** - see the `LICENSE` file for details.

---

## 🙌 Contributing

Pull requests, bug reports, and suggestions are welcome!  
Please open an issue or fork the repo to get started.
