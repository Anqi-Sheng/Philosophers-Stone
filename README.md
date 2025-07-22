# WallpaperLogic

WallpaperLogic is a dynamic and extensible wallpaper and video background manager for Linux and macOS. It supports both static images and looping videos as wallpapers using lightweight Bash scripts and a configuration-based design.

## 🚀 Features

- Randomly change wallpapers or videos from specified directories
- Caches wallpaper/video lists for faster access
- Tmux integration for persistent background processes
- Configurable with simple `.conf` files
- Works across popular Linux distributions and macOS

## 📦 Dependencies

Install the following dependencies for full functionality:

- `tmux` - for detached wallpaper changing sessions
- `feh` - image background setter (Linux)
- `mpv` - video wallpaper player
- `bash`, `find`, `coreutils`, `xdotool` (for automation logic)
- macOS: `brew install tmux mpv feh coreutils`

## 🛠️ Setup

### 1. Clone the repo

```bash
git clone https://github.com/yourusername/wallpaperlogic.git
cd wallpaperlogic
```

### 2. Edit the Configuration

Open `wallpaperlogic.conf`:

```bash
nano wallpaperlogic.conf
```

And set the following variables:

```bash
WALLPAPER_DIR="$HOME/Pictures/Wallpapers"
VIDPAPER_DIR="$HOME/Videos/WallpaperVids"
MODE="image"        # or "video"
LOCKFILE="/tmp/random_wallpaper.lock"
CACHE_FILE="/tmp/wallpaper_list.txt"
```

### 3. Run It

```bash
chmod +x wallpaperlogic
./wallpaperlogic
```

Or run it in a background `tmux` session via wrapper:

```bash
chmod +x run_wallpaper.sh
./run_wallpaper.sh
```

## 🧪 Supported Distros

### 🐧 Linux

| Distro   | Install Command |
|----------|------------------|
| **Arch** | `sudo pacman -S feh mpv tmux` |
| **Debian/Ubuntu** | `sudo apt install feh mpv tmux` |
| **Fedora** | `sudo dnf install feh mpv tmux` |
| **NixOS** | Add to `environment.systemPackages` |
| **Gentoo** | `emerge --ask feh mpv tmux` |

### 🍏 macOS

```bash
brew install tmux mpv feh coreutils
```

## 📜 License

This project is licensed under the **GNU General Public License v3.0** - see the [LICENSE](LICENSE) file for details.

## 🙌 Contributing

Pull requests, bug reports, and suggestions are welcome! Please open an issue or fork the repo to get started.

---

Created with ❤️ for free desktop environments.
