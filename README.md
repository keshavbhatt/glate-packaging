# Glate - Translator and Text-to-Speech for Desktop

<p align="center">
  <img width="200" height="200" src="https://github.com/keshavbhatt/glate/blob/master/icons/icon-256.png?raw=true">
</p>

Glate is a fast desktop translator with built-in text-to-speech, history, and sharing tools.

## Features

- Translate between 100+ languages
- Line-by-line translation view for structured text
- Text-to-speech playback with voice and gender options
- Export speech to audio formats with advanced controls
- Translation history with search, quick copy, and text export
- Share translations with built-in paste link support
- Global quick-translate hotkey support on X11/XWayland
- Dark and light themes

## Screenshots

![Glate main window with dark theme](https://github.com/keshavbhatt/glate/blob/master/screenshots/1.jpg?raw=true)
![Glate settings window with light theme](https://github.com/keshavbhatt/glate/blob/master/screenshots/2.jpg?raw=true)
![Glate share and export dialog](https://github.com/keshavbhatt/glate/blob/master/screenshots/3.jpg?raw=true)

## Preview

[![Glate desktop preview](https://github.com/keshavbhatt/glate/blob/master/screenshots/preview.jpg?raw=true)](https://www.youtube.com/watch?v=FxTDqcIgk7g "Glate desktop preview")

## Install via Snap

Install from Snap Store:

```bash
snap install glate
```

[![glate](https://snapcraft.io/glate/trending.svg)](https://snapcraft.io/glate)
[![Get it from the Snap Store](https://snapcraft.io/static/images/badges/en/snap-store-black.svg)](https://snapcraft.io/glate)

## Build From Source

### Linux desktop build (Qt + CMake)

```bash
cmake -S . -B cmake-build-release -DCMAKE_BUILD_TYPE=Release
cmake --build cmake-build-release -j
```

## Packaging Instructions

### Flatpak

```bash
./build-flatpak.sh
```

This creates a versioned bundle like `glate-4.1.0.flatpak`.

### Snap

```bash
snapcraft
```

Snap version is derived from the CMake project version during build.

### Windows

```bash
cmake -S . -B cmake-build-release -G Ninja -DCMAKE_BUILD_TYPE=Release
cmake --build cmake-build-release -j
cpack --config cmake-build-release/src/CPackConfig.cmake
```

Windows packaging output is generated through NSIS/ZIP via CPack.

## Global Hotkey Note (Wayland)

Global hotkeys are not available on native Wayland sessions due to compositor security restrictions.
If you need system-wide quick-translate hotkeys, run Glate on an X11 session (or via XWayland where supported).

## Credits

[Alan Pope](https://github.com/popey) of [Canonical](https://github.com/canonical) helped decide the app name.



