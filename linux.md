# SPACEAPP for Linux: Download, Run & Troubleshoot

SPACEAPP is provided for Linux in two formats. Pick whichever suits you; both contain the same application.

| | **AppImage** (recommended) | **tar.gz** |
|---|---|---|
| File | `SPACEAPP-Linux-x86_64.AppImage` | `SPACEAPP-Linux.tar.gz` |
| What it is | A single self-contained file | A folder of files in an archive |
| Install needed | None (optional menu integration) | None (extract and run) |
| Start menu & icon | Yes, via AppImageLauncher / Gear Lever | Manual `.desktop` file |
| Needs FUSE | Yes, unless run with `--appimage-extract-and-run` | No |

---

## 1. System requirements

- **64-bit x86 (x86_64) Linux** with a desktop environment (X11 or Wayland with XWayland).
- **glibc 2.35 or newer.** This is the main compatibility requirement for both formats. Check yours with `ldd --version`.
- A few GB of free disk space for the app and its models.

### Distributions that should work normally

Any distribution with glibc 2.35 or newer, including:

- Ubuntu 22.04 and newer (and derivatives: Linux Mint 21+, Pop!_OS 22.04+, elementary OS 7+)
- Debian 12 and newer
- Fedora 36 and newer
- Arch Linux, Manjaro and other current rolling distributions

> On **Ubuntu 22.04** the AppImage works by double-clicking. On **Ubuntu 24.04 and newer**, and on some other distributions, you may need to install one small FUSE package first (see Section 4).

### Not supported

Distributions older than the list above fail with an error like `GLIBC_2.35 not found`. Examples: Ubuntu 20.04 and older, Debian 11 and older, RHEL / Rocky / AlmaLinux 9 and older. Neither the AppImage nor the tar.gz will run on these.

---

## 2. Models folder

SPACEAPP looks for a `models/` folder **next to the application**. Place your models as follows.

**AppImage**: next to the `.AppImage` file itself:

```
/home/you/SPACEAPP/
├── SPACEAPP-Linux-x86_64.AppImage
└── models/
```

**tar.gz**: inside the extracted `SPACEAPP/` folder, next to the `SPACEAPP` executable:

```
SPACEAPP/
├── SPACEAPP
├── _internal/
└── models/
```

Keep the AppImage in a normal folder you control. If you move the file, move `models/` with it.

---

## 3. Using the AppImage

1. Download `SPACEAPP-Linux-x86_64.AppImage`.
2. Make it executable. Either run:
   ```bash
   chmod +x SPACEAPP-Linux-x86_64.AppImage
   ```
   or right-click the file, open **Properties → Permissions**, and enable **Allow executing file as program**.
3. Put your `models/` folder next to it (see Section 2).
4. Run it by double-clicking, or from a terminal:
   ```bash
   ./SPACEAPP-Linux-x86_64.AppImage
   ```

### Optional: add it to your start menu

Running the file does not add a menu entry or icon by itself. For that, use a helper such as **AppImageLauncher** or **Gear Lever**; they offer to integrate the AppImage when you first open it.

---

## 4. If the AppImage won't start

### Symptom: error mentioning `libfuse.so.2` or "FUSE"

AppImages need the FUSE 2 library on your system. Many newer or minimal installs don't include it. Install the package for your distribution, then try again:

| Distribution | Command |
|---|---|
| Ubuntu 24.04 and newer, Debian 13 | `sudo apt install libfuse2t64` |
| Ubuntu 22.04, Debian 12 | `sudo apt install libfuse2` |
| Fedora, RHEL-family | `sudo dnf install fuse-libs` |
| Arch / Manjaro | `sudo pacman -S fuse2` |
| openSUSE | `sudo zypper install libfuse2` |

Package names change between releases. If yours isn't listed, search your package manager for `fuse2` or `libfuse2`.

### Last-resort fallback: no installation at all

This option avoids FUSE completely. The AppImage unpacks itself to a temporary folder and runs from there:

```bash
./SPACEAPP-Linux-x86_64.AppImage --appimage-extract-and-run
```

Notes:
- Startup is a bit slower, and it needs a couple hundred MB of free space in your temp directory.
- It won't work if your temp directory is mounted `noexec`.
- It still needs glibc 2.35 or newer.

If you'd rather not use AppImage at all, use the **tar.gz** (Section 5).

---

## 5. Using the tar.gz

1. Download `SPACEAPP-Linux.tar.gz`.
2. Extract it:
   ```bash
   tar -xzf SPACEAPP-Linux.tar.gz
   ```
3. Put your `models/` folder inside the new `SPACEAPP/` folder (see Section 2).
4. Run it:
   ```bash
   cd SPACEAPP
   ./SPACEAPP
   ```

If the file isn't executable, run `chmod +x SPACEAPP` inside that folder.

The tar.gz doesn't use FUSE, so it is the safest choice on minimal or locked-down systems.

---

## 6. General troubleshooting

| Problem | What to try |
|---|---|
| `Permission denied` | The file isn't executable. Run `chmod +x <file>`. |
| `GLIBC_2.35 not found` | Your distribution is too old. See Section 1; no workaround is available. |
| Error about the Qt `xcb` platform plugin (`could not load the Qt platform plugin "xcb"`) | Install the missing X11 library. On Debian/Ubuntu: `sudo apt install libxcb-cursor0`. On Fedora: `sudo dnf install xcb-util-cursor`. On Arch: `sudo pacman -S xcb-util-cursor`. |
| Nothing happens when double-clicking | Run it from a terminal to see the error message. |
| Models not found | Check the `models/` folder is in the right place (Section 2) and that you launched the AppImage directly, not through a copied or symlinked path. |
| Won't run from a USB drive or external disk | The drive may be mounted `noexec`. Copy the file to your home folder first. |
| Blank or crashing window on some GPUs | Try `QT_QPA_PLATFORM=xcb ./SPACEAPP-Linux-x86_64.AppImage` (or `./SPACEAPP` for the tar.gz). |

### Reporting a problem

When asking for help, please include:
- Your distribution and version (`cat /etc/os-release`)
- Your glibc version (`ldd --version`)
- Which format you used (AppImage or tar.gz)
- The full error text from running the file in a terminal