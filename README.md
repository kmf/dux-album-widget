# Dank Album Widget

A DankMaterialShell desktop widget that shows the current track's album art
and playback controls. It talks to the same MPRIS stack DankDash media uses
(`MprisController`, `TrackArtService`, `MediaAccentService`).

Any MPRIS player works: Spotify, Cider, Firefox/Brave tabs, VLC, mpv, and so on.

![Dank Album Widget on the desktop](screenshot.jpg)

## Features

- The widget *is* the album cover: square, full-bleed MPRIS artwork
- Material previous / play-pause / next controls overlaid on the sleeve
- Art from the active MPRIS player, including remote covers and YouTube thumbnails
- Album-art accent color on the play button (when enabled in DMS media settings)
- Scroll up/down on the cover to change system volume
- Empty sleeve when nothing is playing, or hide until media starts

## Requirements

- DankMaterialShell >= 1.2.0
- An MPRIS-compatible media player

## Installation

Symlink this repo into the DMS plugins directory:

```bash
ln -s "$(pwd)" ~/.config/DankMaterialShell/plugins/dankAlbumWidget
```

Then:

1. Open **Settings → Plugins**
2. Click **Scan for Plugins**
3. Enable **Dank Album Widget**
4. Open **Settings → Widgets** and place it on the desired display
5. Reload plugins if needed: `dms ipc plugin-scan reload dankAlbumWidget`

Right-click and drag to move. Drag the corner handle to resize.

## Configuration

Widget settings:

| Setting | Default | Description |
| --- | --- | --- |
| Hide when idle | off | Fade out when no player is active |

DMS **Settings → Media** still owns player exclusions, album-art accent, visualizer, and scroll mode. This widget follows those.
