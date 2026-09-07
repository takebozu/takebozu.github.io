---
layout: default
title: FFEdit Express — User Guide
description: >-
  How to use FFEdit Express: open a video, set in and out points on the
  timeline, scan for black and white frames, and export the range as a
  lossless copy with ffmpeg.
image: /img/og/ffeditexpress.png
lang: en
alternate_lang: ja
alternate_url: /ja/FFEditExpress/guide-ja.html
---

# <img src="../img/icons/ffeditexpress_logo.png" height="32" align="top" alt="FFEdit Express icon"> FFEdit Express — User Guide

## Overview

FFEdit Express is a simple video trimming tool that drives ffmpeg. Set an in point and an out point, and export just that range as a lossless copy — no re-encoding, so it is fast and there is no quality loss.

## Opening a video

- Drag and drop a video file onto the drop zone in the middle of the window
- Or click **Open Video…**, or **Open…** at the top left of the editing screen

## Timeline controls

Drag on the timeline to move the playhead, the in point, or the out point. The handle nearest where you start dragging is selected automatically.

| Handle | Colour | Meaning |
|---|---|---|
| Playhead | White vertical line | Current playback position |
| In point | Green bar | Where the export starts |
| Out point | Red bar | Where the export ends |
| B/W marker | Orange ◇ | A black or white frame found by the scan |

## Playback and navigation

| Control | What it does |
|---|---|
| ▶ / ⏸ | Play / pause |
| ⏮ / ⏭ | Jump to the start / end of the video |
| −30s … +30s | Move backward or forward by the shown amount |
| .000 | Snap the current position to the nearest whole second |

## Setting the in and out points

1. Move to the position you want, using the timeline or the nudge buttons
2. Click **Set In** to put the in point at the current position
3. Click **Set Out** to put the out point at the current position
4. Use **Go to In** / **Go to Out** to jump back to each point

The length between the in and out points is shown in the middle of the screen.

## Scanning for black and white frames (scene-change detection)

FFEdit Express can find black and white frames automatically and mark them on the timeline, which is handy for locating scene changes.

1. Click **Scan B/W Frames** to start the scan
2. When it finishes, orange ◇ markers appear on the timeline
3. Use **◀ Prev** / **Next ▶** to step between markers

> **Note:** Only black or white frames lasting 0.5 seconds or longer are detected. You can stop a scan in progress with **Cancel**.

## Exporting

1. Enter the output path in the **Output** field (a path with `_cut` added is suggested automatically)
2. Or click **Browse…** to choose a location from a dialog
3. Click **Export**

The export is a **lossless copy** using ffmpeg's `-vcodec copy -acodec copy`. Nothing is re-encoded, so it is fast and there is no loss of quality.

If a file with the same name already exists, `_1`, `_2`, … is appended automatically.

### Copying the ffmpeg command

The `$ ffmpeg …` command shown above the Export button can be copied to the clipboard with the button at its right end. You can paste it straight into Terminal and run it there.

## Requirements

- macOS 14 or later
- ffmpeg (install with Homebrew)

```bash
brew install ffmpeg
```

[← Back to FFEdit Express](./)
