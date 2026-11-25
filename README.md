# Stremio Community for macOS

This is a personal Apple Silicon fork of [nnocte’s macOS port](https://github.com/nnocte/stremio-community-v5-mac), which is based on [Zaarrg’s Stremio Community v5](https://github.com/Zaarrg/stremio-community-v5). It runs the community Stremio v5 web interface in a native macOS window using WKWebView for the controls and libmpv for video playback.

## Download

[![Download v5.0.22-macos-m5.2 for macOS](https://img.shields.io/badge/Download-v5.0.22--macos--m5.2-6f45d4?style=for-the-badge)](https://github.com/chunkiuu/stremio-community-v5-mac/releases/download/v5.0.22-macos-m5.2/Stremio-Community-M5.zip)

[Direct ZIP download](https://github.com/chunkiuu/stremio-community-v5-mac/releases/download/v5.0.22-macos-m5.2/Stremio-Community-M5.zip) · [Release notes](https://github.com/chunkiuu/stremio-community-v5-mac/releases/tag/v5.0.22-macos-m5.2) · [All releases](https://github.com/chunkiuu/stremio-community-v5-mac/releases)

The current download is an **ARM64 pre-release** built for **macOS 27.2 or later**. It uses Homebrew’s `libmpv` and is ad-hoc signed. Local windowed playback was verified on an M5 MacBook with the framebuffer fix. The fullscreen and Space key logic passed automated checks. In-app fullscreen playback, audible feedback, and login persistence still need end-to-end confirmation on this build.

## Install

1. Install mpv with Homebrew if you don’t already have it.

   ```sh
   brew install mpv
   ```

2. Download and unzip `Stremio-Community-M5.zip`, then move **Stremio Community M5** to **Applications**.
3. If you’re upgrading, quit the old copy with **⌘Q** before opening the new app. If you’re coming from a build that changed its local address at each launch, sign in once in the updated app.

## What changed

| Build | Changes |
| --- | --- |
| [`v5.0.22-macos-m5.2`](https://github.com/chunkiuu/stremio-community-v5-mac/releases/tag/v5.0.22-macos-m5.2) | Switches the entire macOS window to fullscreen so the player controls and video stay together. Keeps **Space** for play/pause while suppressing the default alert sound. Includes both fixes from `m5.1`. |
| [`v5.0.22-macos-m5.1`](https://github.com/chunkiuu/stremio-community-v5-mac/releases/tag/v5.0.22-macos-m5.1) | Draws video to Core Animation’s active framebuffer to fix windowed black playback. Gives each built-in web UI a stable local origin so WebKit can restore its sign-in state after relaunch. |

The `5.0.22` part is the upstream Stremio Community version. The `m5.1` and `m5.2` suffixes identify separate builds of this fork.

## Source and credits

See [the macOS build guide](docs/MACOS.md) for the source layout and build instructions. For the broader community project’s features and Windows setup, see [Zaarrg’s repository](https://github.com/Zaarrg/stremio-community-v5). This fork is distributed under the [GPL-3.0 license](LICENSE.md).
